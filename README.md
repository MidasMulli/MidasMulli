## Independent lab: neuromorphic learning, predictive memory and ML systems

I build and test small systems across BrainChip AKD1500, Jetson/NVIDIA and Apple Silicon. The aim is useful capability with inspectable evidence: matched controls, conditions stated, failures preserved and a clear line between measured results and the next idea.

### Native learning and predictive memory

- [akd1500-lab](https://github.com/MidasMulli/akd1500-lab): native learning, connected memory and an interactive Network Explorer. Recent work connects AKD memory to a frozen world model on the Nano. Repeated-context corrections work; generalization and native memory allocation remain open. Recorded data, controls, videos and limits are indexed in the repo.

### Apple Neural Engine: internals and instruments

- [beefface](https://github.com/MidasMulli/beefface): compiled-container specification, hardware-checked binary patching and a deterministic lookup-table fingerprint.
- [ane-toolkit](https://github.com/MidasMulli/ane-toolkit): PWL activation-table tools and custom activation deployment.
- [ane-perf](https://github.com/MidasMulli/ane-perf): IOReport bandwidth measurement and SRAM/dispatch characterization. Conditions and shared prior art are stated in the repo.
- [ane-dispatch](https://github.com/MidasMulli/ane-dispatch) and [ane-compiler](https://github.com/MidasMulli/ane-compiler): private dispatch and MIL compilation tools. These use Apple's private/CoreML paths, not a CoreML bypass.
- [ane-mutable-adapters](https://github.com/MidasMulli/ane-mutable-adapters): mutable LoRA adapters over a frozen resident base.
- [kev-ane](https://github.com/MidasMulli/kev-ane): a small decision model on the ANE, with the gates used to verify it.

### Inference, memory and hardware behavior

- [ngram-engine](https://github.com/MidasMulli/ngram-engine): MLX speculative-decoding server with an N-gram drafter and prefix KV cache.
- [inference-across-metal](https://github.com/MidasMulli/inference-across-metal): model streaming and custom Metal kernels on a memory-limited Mac.
- [dual-path-inference](https://github.com/MidasMulli/dual-path-inference), [apple-slc-cache-hints](https://github.com/MidasMulli/apple-slc-cache-hints) and [gdn-coreml](https://github.com/MidasMulli/gdn-coreml): heterogeneous execution, cache hints and a converter with its negative measured result preserved.
- [subconscious](https://github.com/MidasMulli/subconscious), [cognitive-stack-ane (Orion)](https://github.com/MidasMulli/cognitive-stack-ane) and [phantom-memory](https://github.com/MidasMulli/phantom-memory): local-agent memory systems and experiments.
- [drift-probe-cpu](https://github.com/MidasMulli/drift-probe-cpu): induced/out-of-distribution hidden-state drift detection, not a claim to detect organic hallucinations.
- [tcprobe](https://github.com/MidasMulli/tcprobe): NVIDIA GB10 tensor-core instruction probes. Read its corrections before interpreting historical rates.

### Weight-space research and historical work

- [gradient-bridges](https://github.com/MidasMulli/gradient-bridges): candidate LoRA construction from other task adapters plus one gradient. One lab; external replication remains open.
- [four-path-mlx](https://github.com/MidasMulli/four-path-mlx): archived heterogeneous speculative-decoding experiments. Historical measurements remain available.

Start with the pinned projects or browse the full repository list. Corrections and independent replications are welcome.
