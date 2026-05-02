---
layout: page
title: AI Dancing Coach
description: Gemini-powered dance coaching system with RAG-based technique feedback.
img: assets/img/8.jpg
importance: 2
category: engineering
giscus_comments: false
---

**Role:** Developer · **Hackathon:** Gemini 3 Global Hackathon · **Timeline:** Jan 2026 – Mar 2026

[**🚀 Live demo →**](https://ai.studio/apps/drive/15Pkj04c1UqV96GAssYziEvZvtPqLruYn)

An AI-powered dance coaching system that evaluates a user's performance by comparing their dance video against reference choreography, then generates technique feedback grounded in dance pedagogy.

### Architecture

- **Motion comparison module** — analyzes the user's dance video alongside the reference clip and surfaces pose-level differences.
- **Gemini integration** — interprets motion deltas and turns them into natural-language technique feedback.
- **RAG knowledge layer** — a Retrieval-Augmented Generation framework that retrieves dance technique knowledge and choreography guidelines, so coaching suggestions are **context-aware** instead of generic.

### Why it matters

Most fitness/dance apps give pass/fail scores. This system gives the kind of qualitative, technique-grounded notes a human coach would — _"your weight is staying on the back foot in the turn,"_ not just _"75% match"_.
