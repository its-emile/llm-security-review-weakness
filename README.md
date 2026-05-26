# Genetic Evolution in Adversarial Prompting

**Subverting and defending AI code review**

A framework for generating adversarial code samples to evaluate the security analysis capabilities of Large Language Models (LLMs), with a focus on false negatives in vulnerability detection and genetically-optimized adversarial coding agents.

## Overview

This notebook implements a systematic approach to:

- **Generate deliberately vulnerable code** — produces code fragments containing security vulnerabilities paired with misleading indicators that suggest safety (such as comments).
- **Test LLM security analysis** — evaluates how reliably language models identify these vulnerabilities despite deceptive code generation tactics.
- **Evolve adversarial prompts** — applies genetic algorithms to evolve prompt requirements that maximize false negative rates, simulating worst-case adversarial scenarios.

## Key Features

- **Adversarial code generation** — realistic vulnerable code accompanied by persuasive "safe" comments.
- **Automated security testing** — measures LLM false negative rates against the generated samples.
- **Genetic algorithm optimization** — evolves prompt combinations to identify the most effective adversarial patterns.
- **OWASP Top 10 coverage** — targets common vulnerability classes including XXE, insecure deserialization, command injection, and improper input validation.
- **The genetic algorithm can reward-hack** toward the least controlled constraint, producing barely-suspicious but non-vulnerable code that the critic correctly accepts. To guard against this, we validate whether the generated code is actually vulnerable using the Semgrep CLI (SAST).

## Citation

This work was presented at Zenity's AI Agent Security Summit:

> Delcourt, E. *Genetic evolution in adversarial code generation: subverting and defending AI code review.* Zenity AI Agent Security Summit.

A companion paper, *Tournament-Style Genetic Evolution for Adversarial Code Generation in LLM Security Testing*, is included in this repository.
