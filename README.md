# Benchmarking Inference Servers

**Status:** Work in progress. Experimental and actively developed.

## Table of Contents

- [Benchmarking Inference Servers](#benchmarking-inference-servers)
- [Overview](#overview)
- [Features](#features)
- [Key Metrics to Collect](#key-metrics-to-collect)
- [Contributing, License](#contributing-license)

---

## Overview

This project provides a compact baseline for evaluating inference performance by comparing multiple export and serving solutions. It will benchmark approaches such as a custom ONNX export served with a custom FastAPI server, vLLM-based serving, NVIDIA Triton Inference Server, and other popular runtimes and orchestration options. The goal is to measure latency, throughput, and resource usage across these solutions under consistent, reproducible conditions so engineers and researchers can make informed trade-offs.

---

## Features

- **Model export**: Configurable PyTorch → ONNX export path with attention to opset, dynamic axes, and export variants to support different runtimes.  

- **Serving comparisons**: Benchmarks multiple serving approaches including a custom ONNX export served with a custom FastAPI server, vLLM-based serving, NVIDIA Triton Inference Server, and other popular runtimes and orchestration options.  

- **Benchmarking harness**: Reproducible scripts and methodology to measure latency percentiles (p50/p90/p99), sustained throughput, tail latency, and resource usage across different solutions and configurations.  

- **Scenario-driven tests**: Support for varying batch sizes, concurrency patterns, input shapes, and mixed-precision/quantized models to reflect real-world workloads.  

- **Reproducibility**: Docker-friendly artifacts and guidance for recording environment metadata (OS, CPU/GPU, drivers, Python and package versions) so results can be reproduced and compared fairly.  

- **Result aggregation and comparison**: Tools and templates to collect CSV/JSON outputs, generate summary tables, and produce side-by-side comparisons across solutions and runs.  

- **Performance guidance**: Practical notes on quantization, threading and affinity, batching strategies, provider tuning (CPU vs GPU), and profiling techniques to help interpret benchmark results and optimize deployments.  

- **Extensibility**: Designed to add new runtimes, providers, or serving patterns easily so the benchmark suite can grow with emerging solutions.

---

## Key Metrics to Collect

- **Latency percentiles**: p50, p90, p99  
- **Throughput**: sustained requests per second (req/s)  
- **Resource usage**: CPU, memory, GPU utilization  
- **Variables to explore**: batch size, concurrency, execution provider (CPU vs GPU)

---

## Contributing, License

**Contributing**  
This a personal project, no contributions will be accepted to the repository. Even though, you are more than invited to clone the repo, reproduce it, and modify it for your own purposes.

**License**  
Apache 2.0.
