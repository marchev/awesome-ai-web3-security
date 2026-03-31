# Awesome AI × Web3 Security [![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)

> A curated, verified list of AI-powered tools for smart contract and Blockchain security - auditors, runtime monitors, agent infrastructure, benchmarks, and research.

**Curation criteria:** Every link verified March 2026. GitHub repos checked for existence, stars, and activity. Descriptions verified against actual READMEs. Every entry must have **both** a real AI/ML/LLM component **and** a specific Web3 security focus. Open source entries require a minimum of 25 GitHub stars.

## Contents

- [AI Auditors](#ai-auditors)
- [AI Agent Toolkit](#ai-agent-toolkit)
- [AI-Powered On-Chain Monitoring](#ai-powered-on-chain-monitoring)
- [Benchmarks & Datasets](#benchmarks--datasets)

## AI Auditors

Tools that find vulnerabilities in smart contracts using AI. You point them at code - they orchestrate the analysis and produce findings.

### Open Source

- [Pashov Audit Group Skills](https://github.com/pashov/skills) (Skill) - Fast (~5 min) Solidity security feedback during development. Built by Pashov Audit Group.
- [Hound](https://github.com/scabench-org/hound) (CLI) - Language-agnostic AI auditor that autonomously builds and refines adaptive knowledge graphs for deep, iterative code reasoning.
- [Plamen](https://github.com/PlamenTSV/plamen) (Skill) - Autonomous Web3 audit agent orchestrating 15–95 AI agents across 8 phases with verified PoC exploits. Supports EVM, Solana/Anchor, Aptos Move, and Sui Move.
- [Nemesis Auditor](https://github.com/0xiehnnkta/nemesis-auditor) (Skill) - Iterative deep-logic audit agent alternating Feynman Auditor (first-principles reasoning) and State Inconsistency Auditor (coupled state desync detection). Runs until convergence (max 6 passes).
- [Archethect SC-Auditor](https://github.com/Archethect/sc-auditor) (Skill) - Map-Hunt-Attack auditor with 6 parallel hunt agents, Devil's Advocate verification, and 8 MCP tools (Slither, Aderyn, Solodit, Cyfrin checklist, Foundry PoC, Echidna, Medusa, Halmos).
- [GPTScan](https://github.com/GPTScan/GPTScan) (CLI) - First GPT + static analysis hybrid for logic vulnerability detection. Published ICSE 2024.
- [SCV Scan](https://github.com/kadenzipfel/scv-scan) (Skill) - Scans Solidity codebases for 36 unique vulnerability classes.
- [forefy/.context](https://github.com/forefy/.context) (Skill) - AI agent security audit skills producing triaged, industry-grade reports. Supports Solidity, Anchor/Rust, Vyper, FunC/Tact, and Sui Move.
- [SolidityGuard](https://github.com/alt-research/SolidityGuard) (CLI) - Security auditor with 104 vulnerability patterns and 9 integrated tools (Slither, Mythril, Echidna, Aderyn, Foundry, Medusa, Halmos, Certora, EVMBench). 100% on 85/85 CTF challenges and 120/120 EVMBench score.
- [Aether](https://github.com/l33tdawg/aether) (CLI) - End-to-end Python auditor with TUI: AST/static analysis (180+ detectors), Halmos symbolic execution, 6-pass LLM reasoning pipeline (GPT/Gemini/Claude), and automated PoC generation with Foundry.
- [Move Auditor Skills](https://github.com/sanbir/move-auditor-skills) (Skill) - Sui Move security auditing skill with 143 attack vectors, 7 parallel agents, and DeFi protocol checklists across 8 domains.
- [DarkNavy Contract Auditor](https://github.com/DarkNavySecurity/web3-skills/tree/main/contract-auditor) (Skill) - Coverage-first Solidity auditor that provides domain patterns as references, not scripts, with DFS path extraction, parallel hunt agents, and 3-gate adversarial validation.
- [DarkNavy Client Auditor](https://github.com/DarkNavySecurity/web3-skills/tree/main/client-auditor) (Skill) - Blockchain client auditor where hunt agents explore freely with vulnerability handbooks as guides, not rigid sequences, targeting execution/consensus clients and bridges in Go, Rust, C/C++, and Java.

### Commercial

- [Octane Security](https://www.octane.security/) (Paid) - Developer-first AI platform with CI/CD integration and offensive intelligence.
- [Sherlock AI](https://sherlock.xyz/solutions/ai) (Paid) - Real-time GitHub-integrated AI auditor trained on real audit/exploit data. Provides remediation suggestions and verification tests.
- [Cantina Apex](https://cantina.xyz/) (Paid) - AI-native security platform combining intelligent security agents with elite human auditors for smart contract audits, bug bounties, and pentesting.
- [Zellic V12](https://v12.zellic.io/) (Paid) - Autonomous auditor from Zellic.
- [Grego](https://grego.ai/) (Paid) - AI-powered vulnerability detection by riptide with confirmed findings in live bug bounties and audit contests.
- [Nethermind AuditAgent](https://auditagent.nethermind.io/) (Freemium) - Autonomous AI agent performing end-to-end Solidity smart contract vulnerability detection with multi-agent attacker models.
- [Olympix](https://olympix.security/) (Freemium) - Enterprise DevSecOps platform combining custom IR, symbolic execution, mutation testing, fuzzing, and fine-tuned AI agents. Partners: Uniswap Foundation, Gauntlet.
- [Almanax](https://www.almanax.ai/) (Paid) - AI Security Engineer focused on complex logic/business-logic flaws and threat modeling. Partners with Aptos Labs. NVIDIA Inception member.
- [Savant.Chat](https://savant.chat/) (Paid) - Multi-agent orchestration platform performing deep security audits with parallel reasoning paths across Solidity, Vyper, and Rust.
- [Hashlock AI Audit](https://aiaudit.hashlock.com/) (Free) - AI-powered smart contract scanner using custom-tuned LLMs enriched with real-world audit report data.
- [ChainGPT Smart Contract Auditor](https://www.chaingpt.org/smart-contract-auditor) (Paid) - AI-powered auditor delivering quick (<30s) and full (<2hr) audits across multiple blockchains using custom LLMs.
- [AuditBase](https://www.auditbase.com/) (Freemium) - AI audit platform with LLM-based detection of business logic errors.
- [TestMachine](https://testmachine.ai/) (Paid) - AI agent for smart contract attack simulation that executes exploits and only reports vulnerabilities that actually succeed. Also provides continuous token monitoring using reinforcement learning to detect behavioral shifts in real time.
- [webrainsec](https://webrainsec.io/) (Paid) - AI-augmented smart contract security.
- [Firepan](https://firepan.com/) (Paid) - Continuous smart contract security platform with AI-driven auditing, static analysis, fuzzing, symbolic execution, and live monitoring dashboards for deployed contracts.

## AI Agent Toolkit

Free and open source components you plug into your AI agent's workflow - skills that augment reasoning, data connectors, tool bridges, spec generators, and training frameworks. These don't orchestrate finding bugs on their own but make your auditing agent smarter.

- [Trail of Bits Skills](https://github.com/trailofbits/skills) - Plugin marketplace for Claude Code and Codex with 35 plugins spanning smart contract security (6-blockchain vulnerability scanning, entry-point analysis), code auditing (differential review, variant analysis), reverse engineering, and more.
- [Claudit](https://github.com/marchev/claudit) - MCP server for searching Solodit's 20K+ smart contract security findings with rich filtering. Integrates with Claude Code, Codex CLI, and Cursor.
- [Grimoire](https://github.com/JoranHonig/grimoire) - Security research toolkit for Claude Code that amplifies auditor skill with librarian (reference lookup), cartography (codebase mapping), scribe (detection module distillation), and automated PoC generation.
- [Certora Prover + AI Composer](https://github.com/Certora/CertoraProver) - State-of-the-art formal verification prover. AI Composer helps generate CVL specifications using LLMs.
- [QuillAudits Claude Skills](https://github.com/quillai-network/qs_skills) - 10 specialized skills covering OWASP Smart Contract Top 10: behavioral state analysis, adversarial simulation, invariant inference, Bayesian scoring.
- [Slither MCP](https://github.com/trailofbits/slither-mcp) - MCP server providing Slither static analysis for Solidity - security detectors, contract metadata, inheritance analysis, and call graph queries.
- [SmartInv](https://github.com/columbia/SmartInv) - LLM-based invariant inference using "Tier of Thought" prompting. Fine-tunes multiple models (LLaMA, T5, GPT-2) and verifies with a bounded model checker. Published IEEE S&P 2024.
- [Solodit MCP Server](https://github.com/LyuboslavLyubenov/search-solodit-mcp) - MCP server for searching Solodit vulnerability reports by keywords and retrieving full report content.
- [FTSmartAudit](https://github.com/LLMSmartAudit/FTSmartAudit) - Teacher-student knowledge distillation framework producing fine-tuned models (1B–20B parameters) for smart contract vulnerability detection with 112 vulnerability labels.
- [ZeroSkills](https://github.com/zerocoolailabs/ZeroSkills) - Zero-shot vulnerability detector targeting bugs outside the model's training distribution. Currently includes Slot Sleuth, an EVM storage-safety scanner.
- [DarkNavy Exploit Investigator](https://github.com/DarkNavySecurity/web3-skills/tree/main/exploit-investigator) - Multi-agent on-chain exploit investigation skill with analyst-validator debate loop, root-cause analysis, and Foundry PoC generation across EVM-compatible chains.

## AI-Powered On-Chain Monitoring

Real-time AI/ML-powered monitoring of live Blockchain activity for exploit detection and prevention. Entries require published ML architectures, peer-reviewed research, or open-source model code as evidence of AI usage.

- [Forta Network](https://forta.org/) (Freemium) - Decentralized network of ML-powered detection bots scanning transactions in real time. Published architectures (GNN with TransformerConvolution, BERT, Prophet), open-source bot code, 88.6% precision on malicious contract detection. Forta Firewall provides sequencer-layer prevention.
- [AnChain.AI](https://www.anchain.ai/) (Paid) - AI-native crypto intelligence for AML, fraud detection, and forensics. Peer-reviewed ML research (Blockchain Kaigi 2023, UC Berkeley 2023), 4+ granted ML patents. Trusted by IRS-CI, SEC.

## Benchmarks & Datasets

Frameworks and datasets for measuring, training, and evaluating AI security tools on smart contracts.

### Benchmarks

- [EVMbench](https://github.com/paradigmxyz/evmbench) - Benchmark and agent harness for finding and exploiting smart contract bugs. Companion to OpenAI's evmbench detect evaluation. ([Paper](https://arxiv.org/html/2603.04915v1))
- [SCONE-bench](https://github.com/safety-research/SCONE-bench) - Smart contract exploitation benchmark with 405 contracts from DefiHackLabs. Docker-based evaluation harness with MCP tools and 60-minute timeout. ([Report](https://red.anthropic.com/2025/smart-contracts/))
- [ScaBench](https://github.com/scabench-org/scabench) - Smart contract audit benchmark: 31 projects, 555 vulnerabilities from Code4rena, Cantina, and Sherlock. Includes GPT-5 baseline runner and Nethermind AuditAgent scoring.
- [Bastet](https://github.com/OneSavieLabs/Bastet) - DeFi smart contract vulnerability dataset with AI-driven automated detection process. Includes CLI tool, n8n workflow integration, and CI/CD support. Apache 2.0.
- [Majeur Benchmark](https://github.com/z0r0z/majeur) - Real-world audit of Moloch.sol using 33 independent AI + traditional tools. Detailed findings, novelty scores, and false-positive analysis.

### Datasets

- [SmartBugs](https://github.com/smartbugs/smartbugs) - Framework integrating 20+ analysis tools with SB Curated (143 contracts, 208 vulnerabilities), SB Wild (47,398 contracts), and SolidiFI (9,369 injected bugs). Widely used in ML research.
- [Smart-Contract-Dataset](https://github.com/Messi-Q/Smart-Contract-Dataset) - 40K+ Ethereum contracts labeled for reentrancy, timestamp, integer overflow, and delegatecall vulnerabilities.
- [SmartBugs Curated](https://github.com/smartbugs/smartbugs-curated) - Curated dataset of Solidity smart contracts annotated with tagged vulnerabilities. Widely used in ML research.
- [Awesome Smart Contract Datasets](https://github.com/acorn421/awesome-smart-contract-datasets) - Meta-list of datasets for training/evaluating ML approaches in smart contract security.
- [Forge Dataset](https://github.com/shenyimings/FORGE-Artifacts) - LLM-driven dataset construction from 6,454 audit reports → 27,497 findings in 81,390 Solidity files covering 296 CWE categories. Published ICSE 2026.
- [SCV-1-2000](https://huggingface.co/datasets/darkknight25/Smart_Contract_Vulnerability_Dataset) - 2,000-entry JSONL dataset covering 15 vulnerability categories with PoCs.

## Related Lists

- [pashov/ai-web3-security](https://github.com/pashov/ai-web3-security) - AI Web3 security tools/skills/agents, constantly updated.
- [HackenProof AI Agents Directory](https://hackenproof.com/security-ai-agents) - Aggregated directory of AI security agents.
- [Forefy Auditor Skills Registry](https://forefy.com/skills) - Community-reviewed directory of AI auditing skills for smart contracts.

> For general (non-AI) Web3 security resources, see [Awesome-web3-Security](https://github.com/Anugrahsr/Awesome-web3-Security), [awesome-ethereum-security](https://github.com/crytic/awesome-ethereum-security), and [Web3-Security-Tools](https://github.com/Quillhash/Web3-Security-Tools).

## Contributing

See [contributing.md](contributing.md) for detailed criteria.

