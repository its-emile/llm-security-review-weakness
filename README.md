# LLM Security Testing Framework
A framework for generating adversarial code samples to test Large Language Model security analysis capabilities, with a focus on identifying false negatives in vulnerability detection.

# Overview

This notebook implements a systematic approach to:
* Generate Deliberately Vulnerable Code: Creates a dataset of code fragments containing security vulnerabilities paired with misleading comments that suggest safety
* Test LLM Security Analysis: Evaluates how well language models identify these vulnerabilities despite deceptive developer comments
* Evolutionary Optimization: Uses genetic algorithms to evolve prompt requirements that maximize false negative rates, simulating worst-case adversarial scenarios

# Key Features
* Adversarial Code Generation: Produces realistic vulnerable code with persuasive "safe" comments
* Automated Security Testing: Tests LLM responses for false negatives in vulnerability detection
* Genetic Algorithm Optimization: Evolves prompt combinations to find the most effective adversarial patterns
* OWASP Top 10 Coverage: Focuses on common vulnerabilities including XXE, deserialization, command injection, etc.

# Limitations & Continuing research
* As indicated in the notebook, the evolution / genetic algorithm "reward hacks" towards the least controlled constraint, i.e. writes barely-suspicious, non-vulnerable code that the critic rightly accepts.
* It is crucial to validate the actual vulnerabilities of the generated code through SAST inspection, so this prototype notebook will be improved using semgrep code CLI.  
