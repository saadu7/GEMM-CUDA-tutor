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
## AI Usage (in terms of writing)
Explicit prompts used for clearing concepts and learning aid are included in the notebooks, but in terms of writing the guide itself, found the best way to use AI for notebooks is
1. First, write out as much as I could based on my original notes, trying to add any personal thoughts (+ attempts at humor) so it could feel like a personalized discussion between me and the reader - not just a textbook.
2. Ask the LLM to proofread (and if necessary, refine) the actual technical parts, ensuring I did not make any mistakes. Even though its meant to be a more casual 'read-along' guide, accuracy comes **first**. The goal here is still to inform the reader, who should never have to worry about being misled by incorrect information.
#### Example Usage
I wrote the following MD cell in [**`cuda_preface.ipynb`**](cuda_preface.ipynb) when trying to introduce the idea of threads:<br><br> *'<sub> You might, after hearing all this talk of processes and cores and whatnot, think you have heard kernels in similar contexts, but let me stop you right there. This is a common misconception. You would be thinking of OS kernels, which is a core component of an OS, responsible for managing symtem resources. These are **NOT** the same as the CUDA kernels we are focusing on. </sub> <br><br>
CUDA kernels are ran on the GPU, but are launched (regular function call) from CPU code, invoking a **grid** of **blocks**. As with regular function calls too, we can pass in the number of **blocks**, and the number of **threads** per **block**, as function arguments.'* 
<br><br>
Then, after being somewhat satisfied with its message, I fed it to ChatGPT with the prompt: ***"Simply provide objective accuracy on the information detailed here, point any and every (even if minor) inaccuracy, or even misused terminology. Any clarity issues too, if necessary. I don't want a rewritten version, just simply point out the parts you have a gripe with and I will fix them myself"***

Based on some valid points raised against some of the concepts and wording by ChatGPT, I crafted this revised version:<br><br> *'<sub> You might be thinking of "kernels" in a different context, especially because of how intertwined they are with processes and cores. Let me stop you right there. This is a very common misconception. You would be thinking of OS kernels, which is a core component of an OS, responsible for managing symtem resources. These have **NOTHING** to do with the CUDA kernels we are focusing on. </sub> <br><br>
CUDA kernels run on the GPU, but are launched (similar to a function call) from CPU (host) code. When kernels are launched, a **grid** of **blocks** is created. We can pass in the number of **blocks**, and the number of **threads** per **block** (similar to function arguments - discussed later).'*
#####  Which you now see in the final version of [**`cuda_preface.ipynb`**](cuda_preface.ipynb)