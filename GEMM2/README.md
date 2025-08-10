# Intro
This section is a learning guide built around [Alex Armbruster's Great Efforts](https://alexarmbr.github.io/2024/08/10/How-To-Write-A-Fast-Matrix-Multiplication-From-Scratch-With-Tensor-Cores.html#introduction) to write an optimized HGEMM (Half-Precision General Matrix Multiplication) kernel (function) in CUDA using tensor cores on NVIDIA Tesla T4 GPU. He iteratively improves his implementation of the kernel, to squize more juice out of the GPU.

<br><br>
## Significance
Let's not kid ourselves, if you ever thought about doing computer science, it's probably for one or two reasons. The first, you heard there's a massive amount of money in the industry, or the second you're a massive nerd.

Now, if you fit in both categories, like me, I have great news for you. Writing Kernels for performance programming by leveraging a GPU's architechture, is where the moneys going to be. Why you may ask? 
Two reasons:
1. *"It's not enough to write good code anymore, Perfomance programming is where you need to be"* - Arvinddh
    - The reason being the saturated market of software developers, as well as the emergence of A.I.
    - Realistically, a lot of programmers will be replaced by AI in the near future, simply because of efficiency, and output.
        - Basically A.I can write code faster, and better than you. So Goodluck trying to be a software developer
2. Writing kernel functions is a niche
    - Why? Because it's hard
        - Writing basic kernel functions that use our GPU to perform computations isn't too demanding
        - However, writing Kernel functions that aim to optimize GPU's throughput, is where it get's tricky
        - Because it's such a niche, it's in high demand

So what does this mean for you? If you like taking on challenges, and you like money, then you're in luck.

<br><br>
## Game Plan
This section of the repo sets out to be a "read-along" learning guide to facilitate in understanding Alex's work. Think of it like that one friend who can explain everything the teacher explains, but it just makes sense. You'll find definitions, and examples throughout the text in order to help you as you navigate through these complex topics. You'll also notice many analogies in order to break down topics into more digestable content. Illustrations and anotations are also available. 

<br><br>
## Structure
You will notice this section is split into two main directories:
- `kernels/`- Clean, standalone .cu files for each iteration of the optimization, comments are original ones from Alex Armbruster
 - `notebooks/`- Interactive Jupyter notebooks where I walk through the code step-by-step, combining theory and CUDA code alongside with commentary and diagrams. **This is the recommended place to start for the reader!**


<br><br>
## Preface
Lastly, I just want to talk about how, this is in no means an attempt to discredit or take credit away from Alex Armbruster's work, in fact it is quite to the contrary.

While reading through Alex's work, you might find yourself getting stumped at the very beggining, or at simple questions. Don't feel ashamed, don't be discouraged, we came across similar questions, and we'll explain them thoroughly until you are able to grasp the concept. Don't expect to get through this in one read, unless you are an expert **Your Not!**. So take as much time as you need, read, and re-read until you fully grasp each section. This will make it easier for you to move onto the next section.

My objective here is to make this as digestable as possible to avoid you scratching your head for most of the read-along.

<br><br>
## TLDR:
- Iteratively improving CUDA kernels
- My journey making sense of them
- Enjoy!