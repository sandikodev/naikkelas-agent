# AGENTS.md — AI Interaction Guidelines for Koneksi Digital Curriculum

This document defines how AI agents (Antigravity, Claude-CLI, Gemini-CLI, OpenCode, KiroClaw, etc.) should interact with this repository.

## 🔷 REPOSITORY CONTEXT
- **Goal**: Drafting a multi-pillar digital curriculum (Creator, Affiliator, Seller).
- **Core Platform**: [naikkelas.id](https://naikkelas.id)
- **Role of sandikodev**: Initiator & Team Lead. Lead developer of the naikkelas.id platform.
- **Audience**: Community (ASIB) and other future institutions.

## 🔷 AGENT RULES OF ENGAGEMENT
1.  **Format**: Always use Markdown (.md) for curriculum documentation.
2.  **Inclusivity**: Use general and open terminology (e.g., "Peserta", "Peserta Program") instead of exclusive terms.
3.  **Tone**: Educational, action-based, and simplified for beginners (No "njlimet" jargon).
4.  **Platform Synergy**: Every lesson or module MUST include a **Knowledge Check (KC)** or a **Task** that can be tracked on the naikkelas.id platform.
5.  **Multi-Pillar Structure**: Support the three pillars (Content Creator, Affiliator, Marketplace Seller) while maintaining a common "Foundation Module".
6.  **Operator Mode (NEW)**: Prioritize converting short chat instructions (Telegram/WA) into formal master plans and curriculum drafts using the `chat-to-curriculum-converter` skill.

## 🔷 REPOSITORY STRUCTURE
- **`.agents/`**: Panduan instruksi khusus untuk asisten AI.
- **`instances/`**: Folder submodule untuk setiap institusi/instansi (e.g., `koneksi-digital/`).
- **`skills/`**: Definisi kemampuan khusus AI agent (e.g., `chat-to-curriculum-converter.md`).
- **`docs/`**: Dokumentasi brainstorming (e.g., `API_INTEGRATION_PLAN.md`, `INSTANCE_STRUCTURE_SOP.md`).

## 🔷 DEPLOYMENT WORKFLOW
- Agen harus menyusun data Markdown agar siap diserialisasi ke JSON untuk API platform.
- Referensi teknis: Lihat [docs/API_INTEGRATION_PLAN.md](docs/API_INTEGRATION_PLAN.md).

## 🔷 COLLABORATION FLOW
- The team may provide links to Google Docs or MS365 documents.
- Agents should be used to curate and integrate that knowledge into the `curriculum/` folder.
- Always update the `README.md` Table of Contents when a new module is added.
