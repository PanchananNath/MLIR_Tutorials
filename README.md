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

MLIR requires a few dependencies to be installed. Follow the steps below.

## Step 1: Install Dependencies (Linux)

Install the required build tools:

```bash
sudo apt-get update
sudo apt-get install -y cmake ninja-build ccache
```

## Step 2: Clone the LLVM Repository

Clone the LLVM project repository, which contains MLIR:

```bash
git clone https://github.com/llvm/llvm-project.git
```

## Step 3: Build MLIR from Source

> **Note:** Building MLIR can take a significant amount of time depending on your system.

Create a build directory and configure the project:

```bash
mkdir -p llvm-project/build
cd llvm-project/build

cmake -G Ninja ../llvm \
  -DLLVM_ENABLE_PROJECTS=mlir \
  -DLLVM_BUILD_EXAMPLES=ON \
  -DLLVM_TARGETS_TO_BUILD="Native;ARM;X86" \
  -DCMAKE_BUILD_TYPE=Release \
  -DLLVM_ENABLE_ASSERTIONS=ON \
  -DCMAKE_C_COMPILER=clang \
  -DCMAKE_CXX_COMPILER=clang++ \
  -DLLVM_CCACHE_BUILD=ON
```

Build and run MLIR tests:

```bash
cmake --build . --target check-mlir
```

Install MLIR:

```bash
cmake --build . --target install
```

## Step 4: Verify the Installation

Check the installed MLIR version:

```bash
mlir-opt --version
```

If the installation was successful, the command will print the installed MLIR version information.


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


