---
title: "cirrus"
description: "CLI tool for AI-coached essay revision. Multi-component architecture with a dependency graph pre-flight step."
date: 2024-04-01
status: active
tags: ["python", "cli", "writing", "ai"]
---

A command-line tool for structured essay revision using AI as a coach rather than a ghostwriter.

## Architecture

Five components, each with a distinct role:

- **Diagnoser** — reads the essay and identifies specific failure modes
- **Eval-generator** — produces a rubric based on the diagnostic
- **Writer** — proposes targeted revisions against the rubric
- **Evaluator** — scores the revision against the original rubric
- **Structural Briefer** — produces a high-level structural summary for context

A dependency graph runs before execution to validate that each stage has what it needs. This prevents partial runs where a bad Diagnoser output contaminates everything downstream.

## Philosophy

The goal is to preserve the writer's voice and reasoning while improving clarity and structure. The AI should feel like a rigorous editor, not a co-author.
