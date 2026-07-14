HotPath - Low-Latency Trading Systems Framework

## Overview

This repository contains a production-grade C++ framework for building ultra-low-latency trading systems, inspired by real-world quantitative finance infrastructure. The project focuses on high performance, modular design, and clean, maintainable code using modern C++ practices. It was built as a challenging systems programming exercise to deepen my understanding of low-latency architectures, performance optimization, and production-quality software engineering

## Key Features
- 🚀 Ultra-low-latency request processing optimized for high-performance execution.
- 🔬 Statistical arbitrage strategy implementation for quantitative trading.
- 🧊 Lock-free concurrent data structures to maximize throughput and minimize contention.
- 📊 Realistic market data simulation for strategy development and testing.
- 🔍 Comprehensive benchmarking suite for evaluating latency and system performance.

## Performance Highlights

### Benchmark Results (M2 Max, macOS Sequoia)

#### Order Book Operations
- **Add Order**: 
  - Mean Latency: 347.20 ns
  - 99.9th Percentile: 2,458 ns
- **Best Bid/Ask Lookup**: 
  - Mean Latency: 14.32 ns
- **Cancel Order**: 
  - Mean Latency: 327.69 ns

#### Lock-Free Queue
- **Push/Pop Operations**: 
  - Mean Latency: ~14.5 ns
  - Consistently under 42 ns at 99th percentile

## Technical Architecture

### Core Components

- **Market Data Handler** – Processes streaming market data with an emphasis on low-latency ingestion and efficient event handling.
- **Strategy Engine** – Generates trading signals using a statistical arbitrage strategy.
- **Execution Engine** – Simulates order execution with a focus on realistic execution flow and performance.
- **Core Infrastructure**
  - Lock-free concurrent queues
  - Memory pool allocator
  - High-resolution timing utilities
  - Performance monitoring and benchmarking tools

### Technologies

- Modern C++20
- Zero-cost abstractions
- Cache-friendly data structures
- Lock-free concurrency
- Statistical arbitrage modeling

---

## Getting Started

### Prerequisites

- CMake 3.20 or later
- A C++20-compatible compiler
  - GCC 10+
  - Clang 10+
  - MSVC 19.2+

### Build

```bash
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release ..
cmake --build .
```

### Run Benchmarks

```bash
./benchmark/latency_benchmark
```

### Run the Market Simulator

```bash
./examples/simulator
```

---

## Design Philosophy

This framework is built with a performance-first mindset. Every component is designed to reduce latency, maximize throughput, and maintain clean, modular, and extensible code suitable for high-performance systems programming.

---

## Potential Applications

- Algorithmic Trading Platforms
- Market Making Systems
- Quantitative Trading Infrastructure
- Backtesting and Strategy Research
- Low-Latency Financial Applications
- Performance-Critical Distributed Systems

 


