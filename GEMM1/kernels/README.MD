# Intro
Standalone, raw CUDA '.cu' files showing each stage of Simon Boehm's GPU optimization process. Kernel comments are the original ones included by Simon himself.

### Note
<sub>Highly advised to go through the notebooks section first, especially the introductory notebooks [**`cuda_preface.ipynb`**](../notebooks/cuda_preface.ipynb)and [**`blas_preface.ipynb`**](./notebooks/blas_preface.ipynb). If you're too stubborn for all that and want to jump straight into the kernels, at least understand the structure of CUDA files, to see how these .cu files work -> [Click here](../notebooks/cuda_preface.ipynb#cuda-project-structure)</sub>

## Kernal Index
<sub>*Highly advised to follow the order*</sub>
1. [**`naive_gemm.cu`**](naive_gemm.cu): 
2. [**`coalesced_gemm.cu`**](coalesced_gemm.cu): 
3. [**`smem_gemm.cu`**](smem_gemm.cu): 
4. [**`blocktiling_gemm.cu`**](blocktiling_gemm.cu): 
5. [**`vectorized_gmem.cu`**](vectorized_gmem.cu): , same code used for the next optimization, just parameter tuning on the same algorithm
6. [**`warptiling_gemm.cu`**](warptiling_gemm.cu):



## Setup
