# Introduction to KV Cache

## 1. The Autoregressive Bottleneck
Large Language Models generate text autoregressively. This means in order to predict token $t$, the model must attend to all previous tokens from $0$ to $t-1$.

The standard attention mechanism is defined as:

$$\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V$$

As such, the model has to recalculate the Key ($K$) and Value ($V$) pairs for every single token in its context at every generation step. This results in $O(N^2)$ complexity per token, making text generation extremely slow.

## 2. What is KV Cache?
To eliminate this redundant computation, we can trade compute for memory.

Instead of discarding the computed $K$ and $V$ pairs after the attention calculation for a token, they can be stored in a GPU's VRAM. 

Then, when generating the next token, the model only computes the Query ($Q$), Key ($K$), and Value ($V$) for that single new token. 

The new $K$ and $V$ are then appended to the existing cache to perform attention using the new $Q$ against the entire updated cache of $K$ and $V$.

**KV Cache Update Mechanism**
```
Input: [Token 1] >>> Compute Q1, K1, V1 
Cache: [ K1 ]
       [ V1 ]

Input: [Token 2] >>> Compute Q2, K2, V2
Cache: [ K1, K2 ]   <<< Append new K2
       [ V1, V2 ]   <<< Append new V2

...

Input: [Token n] >>> Compute: Qn, Kn, Vn
Cache: [ K1, K2, ..., Kn ]
       [ V1, V2, ..., Vn ]
```

By projecting $Q$, $K$, and $V$ for only a single token at a time, the per-token complexity for generation drops from $O(N^2)$ to $O(N)$, accelerating inference throughput.