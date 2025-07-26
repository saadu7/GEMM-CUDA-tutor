# Intro
Jupyter notebooks that pair theory, CUDA code, and performance analysis (+ a bit of rambling from me). Designed as a "read-along" guide to understand the iterative kernel optimization step-by-step.

<br><br>
## Notebooks Index
<sub>*Highly advised to follow the order*</sub>

1. [**`cuda_preface.ipynb`**](cuda_preface.ipynb): Intro to CUDA - syntax, execution model, more.
2. [**`naive_gemm.ipynb`**](naive_gemm.ipynb): 
2. [**`coalesced_gemm.ipynb`**](coalesced_gemm.ipynb): 
3. [**`smem_gemm.ipynb`**](smem_gemm.ipynb): 
4. [**`blocktiling_gemm.ipynb`**](blocktiling_gemm.ipynb): 
5. [**`vectorized_gmem.ipynb`**](vectorized_gmem.ipynb): , same code used for the next optimization, just parameter tuning on the same algorithm
6. [**`warptiling_gemm.ipynb`**](warptiling_gemm.ipynb):oo

<br><br>
## Setup
None needed! Just run the .pyinb files

<br><br>
## AI Usage
Found the best way to use AI for notebooks is
1. First write out as much as I could based on my original notes, trying to add any personal thoughts ( + attempts at humor) so it could feel like a personalized discussion between me and the reader
2. Proofread (and if necessary, refine) the actual technical parts, ensuring I did not make any mistakes. as last thing to have in this
#### Example Usage
I wrote the following MD cell in [**`cuda_preface.ipynb`**](cuda_preface.ipynb) when trying to introduce the idea of threads: ** <br><br>
Then, after being somewhat satisfied with its message, I fed it to ChatGPT with the prompt: *"Simply provide objective accuracy on the information detailed here, point any and every (even if minor) inaccuracy, or even misused terminology. I don't want a rewritten version, just simply point out the parts you have a gripe with and I will fix them myself"*

Based on some valid points raised against some of the concepts and wording by ChatGPT, I crafted this revised version: **
#####  Which you now see in the final version of [**`cuda_preface.ipynb`**](cuda_preface.ipynb)