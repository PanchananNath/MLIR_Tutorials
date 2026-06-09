# MLIR tutorials for Deep Learning optimization series

This repository contains a structured series covering MLIR, compiler optimizations, GPU execution, transformers, and deep learning superoptimization.

## Table of Contents

- [Part 1 - What and why MLIR?](#part-1---what-is-mlir)
- [Part 2 - Memory in MLIR](#part-2---memory-in-mlir)
- [Part 3 - Affine Dialect and OpenMP](#part-3---affine-dialect-and-openmp)
- [Part 4 - Linear Algebra and Linalg](#part-4---linear-algebra-and-linalg)
- [Part 5 - Neural Networks and Tensors](#part-5---neural-networks-and-tensors)
- [Part 6 - e-graphs and Term Rewriting](#part-6---e-graphs-and-term-rewriting)
- [Part 7 - NVIDIA GPU Execution](#part-7---nvidia-gpu-execution)
- [Part 8 - Transformer Architecture](#part-8---transformer-architecture)
- [Part 9 - Superoptimizing Deep Learning](#part-9---superoptimizing-deep-learning)

---

# Installing MLIR

MLIR requires a few dependencies to be installed, follow the steps below

# S1- For Linux

apt-get install cmake ninja-build ccache

# S2- Clone the LLVM repository

git clone https://github.com/llvm/llvm-project

# S3- Build MLIR from source, this might take a long time to build

mkdir llvm-project/build
cd llvm-project/build
cmake -G Ninja ../llvm \
   -DLLVM_ENABLE_PROJECTS=mlir \
   -DLLVM_BUILD_EXAMPLES=ON \
   -DLLVM_TARGETS_TO_BUILD="Native;ARM;X86" \
   -DCMAKE_BUILD_TYPE=Release \
   -DLLVM_ENABLE_ASSERTIONS=ON \
   -DCMAKE_C_COMPILER=clang -DCMAKE_CXX_COMPILER=clang++ \
   -DLLVM_CCACHE_BUILD=ON
   
cmake --build . --target check-mlir
cmake --build . --target install


# S4- Check the version of MLIR installed.

mlir-opt --version


# Part 1 - What is MLIR?



---

# Part 2 - Memory in MLIR



---

# Part 3 - Affine Dialect and OpenMP


---

# Part 4 - Linear Algebra and Linalg



---

# Part 5 - Neural Networks and Tensors



---

# Part 6 - e-graphs and Term Rewriting



---

# Part 7 - NVIDIA GPU Execution



---

# Part 8 - Transformer Architecture


---

# Part 9 - Superoptimizing Deep Learning


