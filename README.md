# PSFirewallManager - Project Documentation

[![View PDF](https://img.shields.io/badge/View-PDF-blue?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](https://alehshehda.github.io/OSS-FW-project/OSS-FW-project.pdf)
[![Download PDF](https://img.shields.io/badge/Download-PDF-success?style=for-the-badge&logo=github&logoColor=white)](https://github.com/alehshehda/OSS-FW-project/releases/download/latest/OSS-FW-project.pdf)
[![Source Code](https://img.shields.io/badge/Code-PSFirewallManager-informational?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ruslanhedz/PSFirewallManager)

Comprehensive technical documentation for **PSFirewallManager** - an enterprise-grade PowerShell tool for Microsoft Windows Defender Firewall management, built with transactional write-ahead logging (WAL), tamper-evident SHA-256 audit trails, NLA profile binding, and remote Linux pull-model backups.

---

## Key Highlights

- **Interactive CLI & Validation (Module 1):** Robust input validation (IPv4/IPv6, CIDR, ports 1-65535, directional port binding) with structured rule naming (`<NR>-OSO-<Action>-<Direction>-<timestamp>`).
- **NLA & Network Profiles (Module 2):** Real-time Network Location Awareness diagnostics with multi-profile rule scoping (*Domain*, *Private*, *Public*, *Any*).
- **Transactional Audit & Watcher (Module 3):** Registry/GPO differential snapshots (`FirewallPolicy`, `WindowsFirewall`), write-ahead logging (`intent` $\rightarrow$ `change` $\rightarrow$ `result`), continuous SHA-256 hash chaining, background event interception (`Watcher`), and fail-closed/fail-open policies.
- **Secure Remote Backup (Module 4):** Automated pre-change exports in an inverted pull model over SSH (`forced command`), read-only SFTPGo storage (port 2022), 30-version retention, and two-phase restore with safety snapshots (`pre-restore`).

---

## Course & Authors

Project developed for the **Operating Systems Security** (*Ochrona Systemów Operacyjnych* - OSO) course at **Wrocław University of Science and Technology** (WUST / PWr), Faculty of Information and Communication Technology (Cybersecurity).

| Author | Student ID | Area of Responsibility |
| :--- | :---: | :--- |
| **Aleh Shehda** | 272277 | Module 3: Transactional WAL Audit, Hash Chain, Watcher, Fail-Closed/Open |
| **Aliaksei Lapachuk** | 276711 | Module 2: NLA Integration, Network Location Profiles, Protocol Selection |
| **Adam Rola** | 272194 | Module 1: Interactive CLI Wizard, IPv4/IPv6 & Port Validation, Rule Indexing |
| **Ruslan Hedz** | 272212 | Module 4: Client-Server Backup Engine, SSH Pull Agent, SFTPGo Integration |

**Project Supervisor:** mgr inż. Adrian Wojciech Florek

---

## Repository Structure

```text
├── main.tex                         # Master LaTeX document
├── .github/workflows/compile.yml    # Automated PDF compilation & GitHub Pages release
├── config/                          # Metadata, title, theme, and optional section toggles
├── preamble/                        # Typography, macros, tables, listings, and styling
├── frontmatter/                     # Title page and abbreviations table
├── chapters/
│   ├── 1_wstep.tex                  # Introduction, motivation, and problem statement
│   ├── 2_podstawy_technologiczne.tex# WFP architecture, MpsSvc, registry, NLA, and event logs
│   ├── 3_architektura_i_dzialanie.tex # Functional modules, WAL audit engine, and backup flows
│   ├── 4_srodowisko_i_weryfikacja.tex# Topology, CI/CD pipeline, unit tests, and acceptance
│   └── 5_podsumowanie.tex           # Security limitations, compensations, and conclusions
├── bib/                             # BibTeX references (references.bib) and Polish bst style
└── images/                          # High-resolution screenshots and topology diagram (PNG + SVG)
```

---

## Compilation

The document is automatically compiled to **`OSS-FW-project.pdf`** and published to GitHub Releases and GitHub Pages on every push to `main`.

To build locally using `pdflatex` and `bibtex`:

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```
