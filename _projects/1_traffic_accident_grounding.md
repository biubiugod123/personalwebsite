---
layout: page
title: Multimodal Traffic Accident Grounding System
description: Zero-shot accident time/location/type grounding from real CCTV using frozen VLMs (Qwen3-VL + Gemini 3.1).
importance: 1
category: research
giscus_comments: false
---

**Role:** Researcher · **Timeline:** Mar 2026 – May 2026 · **Benchmark:** ACCIDENT @ CVPR 2026

A **zero-shot multimodal accident grounding pipeline** that predicts **accident time, impact location, and collision type** directly from real CCTV footage — no task-specific training, just frozen vision-language models orchestrated in a coarse-to-fine framework.

### Architecture

- **Pass 1 — Coarse temporal-spatial grounding** with **Qwen3-VL**: locates _when_ and _where_ the accident occurs in the clip.
- **Pass 2 — Fine-grained classification** with **Gemini 3.1**: identifies the collision type (rear-end, side-swipe, T-bone, etc.).
- **Confidence gating**: when VLM confidence drops below threshold, the pipeline falls back to a deterministic stack — **YOLO + ByteTrack** for object detection/tracking plus a **physics-based scoring** module that reasons about velocity, trajectory, and impact geometry.

### Evaluation

Tested on the **2,027-video real-CCTV split of the ACCIDENT @ CVPR 2026 benchmark**. The fallback design ensures the system degrades gracefully when VLMs fail on unusual viewpoints or weather conditions, rather than producing confident wrong answers.

### Why it matters

Accident grounding is exactly the kind of task where collecting labeled training data is prohibitive (variety of camera angles, jurisdictions, accident types). Showing that a **frozen-VLM coarse-to-fine pipeline with deterministic fallbacks** can perform competitively suggests a path to **deployable safety systems** that don't require massive supervised datasets.
