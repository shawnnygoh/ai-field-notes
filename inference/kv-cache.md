# Introduction to KV Cache

## 1. The Autoregressive Bottleneck
Large Language Models generate text autoregressively. This means in order to predict token $t$, the model must attend to all previous tokens from $0$ to $t-1$.

The standard attention mechanism is defined as:
$$\text{Attention}(Q, K, V) = \text{softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V$$

As such, the model has to recalculate the Key ($K$) and Value ($V$) pairs for every single token in its context at every generation step. This results in $O(N^2)$ complexity, making text generation extremely slow.
