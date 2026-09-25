# RAG 3D Process Animation

An animated 3D walkthrough of how Retrieval-Augmented Generation (RAG) works, using [Pilotfit](https://shueny.github.io) (my AI job-search platform) as the running example. One job posting travels through the whole pipeline: the user's experiences are split and tagged, embedded into vectors, the closest ones are retrieved, and the model's analysis cites the experience it used. It is compared against an LLM that has never seen the user's experience and can only guess.

一個用 3D 動畫說明 RAG（檢索增強生成）運作流程的網頁，以我的 AI 求職平台 Pilotfit 為例：跟著一份職缺，看使用者的經歷如何被切分、向量化、檢索，最後產生有出處的分析，並對照沒有 RAG 時 LLM 只能憑空猜測的情況。

## Live demo

- 繁體中文版: https://shueny.github.io/rag-explainer/
- English version: https://shueny.github.io/rag-explainer/en.html

## Screenshots

![RAG 3D animation, English version](assets/rag-en.png)

![RAG 3D 動畫，繁體中文版](assets/rag-zh.png)

## Features

- Six steps: Prepare, Embed, Ask, Retrieve, Augment, Generate
- Side-by-side result: a generic guess without RAG vs. an analysis that cites the experience it used
- Real Pilotfit details: 1,536-dimension embeddings in pgvector (HNSW index), and hybrid retrieval weighted 60% vector similarity + 40% tech-tag matching
- Play / Pause (or press Space)
- Previous / Next section
- EN / 中文 toggle that keeps the current playback time
- Works offline: open the HTML file directly in a browser

## Tech

Each page is a single self-contained HTML file. All scripts, styles and fonts are inlined, so there is no build step and no external dependency.

## Files

- `index.html`: 繁體中文版
- `en.html`: English version
- `assets/`: screenshots used in this README
