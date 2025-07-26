# Intro

This section is a learning companion built around the [amazing work done by Simon Boehm](https://siboehm.com/articles/22/CUDA-MMM) crafting a series of progressively optimized CUDA kernels for GEMM (General Matrix Multiplication)

<br><br>
## Significance
If you ever wondered in your Linear Algebra class, *'When am I ever going to use matrix multiplication?'*, boy, do I have some news for you.

**It might be the single most important operation that exists currently.** Why? - the rise of LLMs. 

If you look at our LLMs section, you will clearly see the enormous amount of matrix multiplication involved in both training and inference of LLMs, so optimizing GEMM is the **key** to reduce training costs for LLMs.

<br><br>
## Game Plan
This section of the repo sets out to be a "read-along" learning guide that aims to make Simon's (fascinating) work slightly more digestible by documenting my own thought process while understanding it - including moments of frustrating confusion, analogies (and diagrams) that helped break the mental blocks, and just other things that I would like to share with the reader.

So, sit back, grab some coffee, maybe a pen and paper, and enjoy the ride. We'll provide visuals for crucial understanding, and it may be helpful to jot down points / make some rough sketches as we try to grasp some of the following concepts, through the kernel optimizations:

<sub>**Note:** honestly, don't even look at these right now, it might deter you because of how scary and foreign they might sound, come back here later to review them</sub>
- Parallelism & CUDA thread hierarchy (grids, blocks, threads and warps)
- Global memory coalescing (why memory access patterns matter)
- Shared memory tiling (reusing data to save bandwidth)
- Warp-level optimizations & Tensor Cores (harnessing specialized hardware)

<br><br>
### Structure
You will notice this section is split into two main directories:
- `kernels/`- Clean, standalone .cu files for each iteration of the optimization, comments are original ones from Simon Boehm
 - `notebooks/`- Interactive Jupyter notebooks where I walk through the code step-wise, combining theory and CUDA code alongside with commentary and diagrams. **This is the recommended place to start for the reader!**

<br><br>
### Preface
Lastly, I just want to talk about how, this is in no means an attempt to discredit or take credit away from Simon Boehm's work, in fact it is quite to the contrary.

Simon's work was an incredible introduction into the world of GEMM optimization for me, but, it took me a while to wrap my head around despite Simon's brilliant efforts with diagrams and more. 

My objective here is to just demystify some of the expert-level explanations, especially for beginners to the topic, to help them avoid the mental roadblocks that I hit, by sharing my experiences and breakthroughs.

<br><br>
## TLDR:
- Iteratively improving CUDA kernels
- My journey making sense of them
- Enjoy!