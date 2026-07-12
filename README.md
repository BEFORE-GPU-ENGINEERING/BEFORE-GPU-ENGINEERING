<div align="center">
  <h1>Before GPU Engineering</h1>
  <p><em>A first-principles climb from the absolute bottom of hardware to the top of GPU architecture.</em></p>
  <br>
  <strong><span style="color: #ff0000; font-size: 1.2em; text-decoration: underline;">
    <a href="https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/" style="color: #ff0000;">READ THE LIVE DIGITAL NOTEBOOK HERE</a>
  </span></strong>
</div>

<br>

> **<span style="color: #ff0000;">New to GPU Engineering? Start Here.</span>**  
> If you are diving into CUDA, kernel programming, or LLM inference, consider this your ultimate prerequisite. Before battling complex textbooks or dense research papers, read this series. You will build a rock-solid, first-principles foundation to actually understand advanced literature and write aggressively fast code.

---

### 📖 The Philosophy
This repository documents my journey learning GPU engineering, built in public, note by note, from the ground up. **No hand-waving or abstract jargon.** Just logic gates, memory buses, and first principles.

### 🎯 Who is this for?
**Developers, students, and self-learners** who want to understand *how* and *why* GPUs are so fast for AI and heavy compute, without getting immediately bogged down in complex CUDA syntax or graphics APIs. If you understand basic programming but GPUs feel like black magic, this is for you.

### 🚀 What will you learn?
<span style="color: #eab308; font-weight: bold;">By the end of this series, you will no longer see the GPU as a black box. You will be able to:</span>
- **Reason from first principles** about architecture (Warps, SMs, Memory Hierarchy, Tensor Cores).
- **Diagnose bottlenecks** intuitively (Compute-bound vs. Memory-bound, latency hiding).
- **Learn CUDA/Triton faster**, by understanding the *why* behind thread blocks and memory coalescing.
- **Optimize AI workloads** with a deep mechanical sympathy for hardware.

### 💡 How to use this resource
Treat this as a structured book. **<span style="color: #ff0000; font-weight: bold;">Start from Chapter 1 and read sequentially.</span>** The concepts build heavily on each other. You cannot understand matrix tiling without understanding shared memory, and you cannot understand shared memory without understanding the memory wall.

---

## Syllabus

### Phase 1

#### Part 1: The Architecture

- [Chapter 1: Why CPUs Can't Have 10,000 Cores](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/architecture/chapter-1.html)
- [Chapter 2: Why a GPU multiplies matrices faster](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/architecture/chapter-2.html)
- [Chapter 3: What "parallelizable" actually means](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/architecture/chapter-3.html)
#### Part 2: Feeding the Beast

- [Chapter 4: Why GPUs care so much about memory bandwidth](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/feeding-the-beast/chapter-4.html)
- [Chapter 5: Compute-bound vs. memory-bound](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/feeding-the-beast/chapter-5.html)
- [Chapter 6: The GPU memory hierarchy](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/feeding-the-beast/chapter-6.html)
#### Part 3: Inside the Silicon

- [Chapter 7: What problem do warps solve?](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/inside-the-silicon/chapter-7.html)
- [Chapter 8: Why branching is bad on GPUs](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/inside-the-silicon/chapter-8.html)
- [Chapter 9: What is SIMT? (and how it differs from SIMD)](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/inside-the-silicon/chapter-9.html)
- [Chapter 10: Why occupancy matters](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/inside-the-silicon/chapter-10.html)
#### Part 4: Putting it Together

- [Chapter 11: why ai runs on gpus but databases dont](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/putting-it-together/chapter-11.html)
- [Chapter 12: What is latency hiding](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/putting-it-together/chapter-12.html)
- [Chapter 13: what if a gpu had cpu-style caches](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/putting-it-together/chapter-13.html)
- [Chapter 14: The memory wall & HBM](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/putting-it-together/chapter-14.html)
- [Chapter 15: Designing an LLM training processor](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/putting-it-together/chapter-15.html)
### Phase 2

#### The Translation Barrier

- [Chapter 16: Why C++ won't auto-compile to GPU](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-translation-barrier/chapter-16.html)
- [Chapter 17: A kernel is not a function](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-translation-barrier/chapter-17.html)
- [Chapter 18: Why thread indexing exists](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-translation-barrier/chapter-18.html)
#### The Hardware Hierarchy

- [Chapter 19: Why threads group into blocks](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-hardware-hierarchy/chapter-19.html)
- [Chapter 20: Why shared memory is fast](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-hardware-hierarchy/chapter-20.html)
- [Chapter 21: Why RAM isn't visible to the GPU](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-hardware-hierarchy/chapter-21.html)
- [Chapter 22: Kernel launch overhead](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-hardware-hierarchy/chapter-22.html)
#### Synchronization & Hazards

- [Chapter 23: What syncthreads protects](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/synchronization-hazards/chapter-23.html)
- [Chapter 24: Why race conditions happen](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/synchronization-hazards/chapter-24.html)
- [Chapter 25: What makes CUDA code "correct"](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/synchronization-hazards/chapter-25.html)
#### Scale & Performance

- [Chapter 26: Why the GPU context switch is free but CPU's is slow](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/scale-and-performance/chapter-26.html)
- [Chapter 27: The step-by-step anatomy of a kernel launch](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/scale-and-performance/chapter-27.html)
- [Chapter 28: Why NVIDIA made CUDA asynchronous](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/scale-and-performance/chapter-28.html)
- [Chapter 29: Coalesced vs strided memory access](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/scale-and-performance/chapter-29.html)
- [Chapter 30: Why GPU programs actually slow down](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/scale-and-performance/chapter-30.html)
- [Chapter 31: Why matrix add scales but a linked list dies](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/scale-and-performance/chapter-31.html)
- [Chapter 32: When NOT to use a GPU, and the reduction tree](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/scale-and-performance/chapter-32.html)
### Phase 3

#### The Memory Wall

- [Chapter 33: Your ALUs are idle. Memory is the real bottleneck.](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-memory-wall/chapter-33.html)
- [Chapter 34: What is arithmetic intensity? The currency of GPU optimization.](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-memory-wall/chapter-34.html)
- [Chapter 35: Two hard ceilings. One tells you to fix your math. The other says: fix your memory.](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-memory-wall/chapter-35.html)
#### The Register Physics

- [Chapter 36: Why not build a GPU entirely from registers?](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-register-physics/chapter-36.html)
- [Chapter 37: Where should data live? The register-occupancy tradeoff.](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-register-physics/chapter-37.html)
- [Chapter 38: What is occupancy, really? It's a ratio, not a count, and 100% is not the goal.](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-register-physics/chapter-38.html)
- [Chapter 39: Why higher occupancy can make performance worse.](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-register-physics/chapter-39.html)
#### Register Spilling

- [Chapter 40: What is register spilling? The cliff between 1 ms and 50 ms.](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/register-spilling/chapter-40.html)
- [Chapter 41: Splitting the giant](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/register-spilling/chapter-41.html)
- [Chapter 42: When spilling is acceptable: and when it destroys performance.](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/register-spilling/chapter-42.html)
#### Global Memory & Coalescing

- [Chapter 43: Why global memory latency is 350 to 1,000 cycles: the physics of distance.](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/global-memory-and-coalescing/chapter-43.html)
- [Chapter 44: What is memory coalescing? 32 threads, 1 transaction vs 32 transactions.](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/global-memory-and-coalescing/chapter-44.html)
- [Chapter 45: DRAM row-buffer thrashing: why scattered access is structurally broken.](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/global-memory-and-coalescing/chapter-45.html)
#### Shared Memory & Tiling

- [Chapter 46: Why shared memory is powerful](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/shared-memory-and-tiling/chapter-46.html)
- [Chapter 47: Bank conflicts: the hidden trap](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/shared-memory-and-tiling/chapter-47.html)
- [Chapter 48: Memory reuse: escape the wall](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/shared-memory-and-tiling/chapter-48.html)
- [Chapter 49: What is tiling?](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/shared-memory-and-tiling/chapter-49.html)
#### GEMM & The Synthesis

- [Chapter 50: Why matmul is king](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/gemm-and-the-synthesis/chapter-50.html)
- [Chapter 51: Throughput vs latency mindset](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/gemm-and-the-synthesis/chapter-51.html)
- [Chapter 52: What is latency hiding?](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/gemm-and-the-synthesis/chapter-52.html)
- [Chapter 53: Why profiling beats intuition](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/gemm-and-the-synthesis/chapter-53.html)
### Phase 4

#### The Measurement Mandate

- [Chapter 54: The 91 missing TFLOPS](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-measurement-mandate/chapter-54.html)
- [Chapter 55: Observe, don't assume](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-measurement-mandate/chapter-55.html)
- [Chapter 56: Nsight Systems vs Compute](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-measurement-mandate/chapter-56.html)
- [Chapter 57: What kernel time measures](https://BEFORE-GPU-ENGINEERING.github.io/BEFORE-GPU-ENGINEERING/the-measurement-mandate/chapter-57.html)

---

## 🤝 How to Contribute

This is a living, public resource, and **<span style="color: #ff0000; font-weight: bold;">community contributions are highly encouraged!</span>**

You can help improve this project in several ways:
- **Adding or Fixing Diagrams:** Many chapters are missing visual aids, or existing diagrams could be made clearer. If you can create a great visual for a concept, feel free to add it!
- **Improving Notes & Information:** If you spot a typo, a technical inaccuracy, or know a better/simpler way to explain a concept, open a PR to update the text.
- **Enhancing the UI:** The custom digital notebook interface itself is open to improvements in design, responsiveness, or readability.

### To contribute:
1. Fork the repository.
2. Create a new branch for your feature or fix (`git checkout -b feature/improve-diagram`).
3. Commit your changes (`git commit -m "Add coalescing diagram to Chapter 44"`).
4. Push to the branch (`git push origin feature/improve-diagram`).
5. Open a Pull Request!

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).
