## Independent lab: Apple Neural Engine systems and weight-space optimization

Two benches. Apple Silicon systems work (Neural Engine reverse engineering, on-device
inference, memory subsystems) on a Mac; weight-space optimization science on a Linux GPU
box. Measured numbers with disclosed conditions, preregistered bars where the work is
experimental, and negative results reported as the bottom line.

### Weight-space optimization

- [gradient-bridges](https://github.com/MidasMulli/gradient-bridges): construct a working
  LoRA adapter for a never-trained task from the mean of other tasks' adapters plus one
  gradient at the untrained init. Leave-one-out panels, matched controls at 0/96, and a
  second-family replication (Llama-3.1-8B, 96/96). Status: candidate, one lab.

### Apple Neural Engine: measurement and internals

- [ane-perf](https://github.com/MidasMulli/ane-perf): an IOReport-histogram method for ANE
  DRAM bandwidth, a three-zone SRAM model with a cliff at 32 MB, and a controlled
  refutation of "conv is faster than matmul on ANE". Every finding carries its conditions
  and a named repro.
- [beefface](https://github.com/MidasMulli/beefface): byte-level specification of Apple's
  compiled ANE container, a working binary patcher verified against hardware output, and a
  deterministic hardware LUT fingerprint.
- [ane-toolkit](https://github.com/MidasMulli/ane-toolkit): compile a Python float
  function into a piecewise-linear chain that runs on the ANE's hardware activation tables.
- [ane-dispatch](https://github.com/MidasMulli/ane-dispatch): direct ANE dispatch through
  the private client API, with functional ANE SharedEvents and an ANE-GPU bridge.

### Apple Silicon inference and memory

- [ane-mutable-adapters](https://github.com/MidasMulli/ane-mutable-adapters): hot-swap
  LoRA adapters over a frozen resident base on the ANE via mutable-weight files.
- [four-path-mlx](https://github.com/MidasMulli/four-path-mlx): multi-source speculative
  decoding for MLX. Measured 1 to 4.6x on financial-document tasks, about 1x on novel text.
  Archived.
- [inference-across-metal](https://github.com/MidasMulli/inference-across-metal):
  mmap-streaming a 14 GB model on a 16 GB Apple Silicon machine, with the kernel-level
  findings that made it work.
- [gdn-coreml](https://github.com/MidasMulli/gdn-coreml): a GatedDeltaNet checkpoint
  converted to CoreML for ANE draft decode. Measured result on the owned hardware is 0.94x,
  reported as the bottom line.

Full repo list is below the pinned set. Corrections via issue are welcome on any repo.
