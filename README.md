# Firewall in PowerShell - Firewall Rules Management

[![View PDF](https://img.shields.io/badge/View-PDF-blue?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](https://alehshehda.github.io/SOS-FW-project/SOS-FW-project.pdf)
[![Download PDF](https://img.shields.io/badge/Download-PDF-success?style=for-the-badge&logo=github&logoColor=white)](https://github.com/alehshehda/SOS-FW-project/releases/download/latest/SOS-FW-project.pdf)

Project documentation for the **Operating Systems Security** course (*Ochrona Systemów Operacyjnych*) at Wrocław University of Science and Technology, Faculty of Information and Communication Technology (Cybersecurity).

**Source Code Repository:** [ruslanhedz/Firewall_in_powershell](https://github.com/ruslanhedz/Firewall_in_powershell)

## Authors

- Aleh Shehda (272277)
- Aliaksei Lapachuk (276711)
- Adam Rola (272194)
- Ruslan Hedz (272212)

**Supervisor:** mgr inż. Adrian Wojciech Florek

## Repository Structure

```text
main.tex                              main LaTeX document file
.github/
  workflows/
    compile.yml                       automated PDF build and release workflow
config/
  metadata.tex                        document metadata and optional section toggles
  theme-pwr.tex                       WUST visual theme and colors
preamble/                             packages, page styles, macros, and table settings
frontmatter/
  titlepage.tex                       title page layout
  abbreviations.tex                   list of abbreviations and acronyms
chapters/
  1_wstep.tex                         Introduction and project assumptions
  2_podstawy_technologiczne.tex       Windows Firewall architecture and PowerShell environment
  3_projekt_rozwiazania.tex           System architecture and solution design
  4_implementacja.tex                 Implementation of functional modules
  5_testy_i_weryfikacja.tex           Testing and verification of operation
  6_podsumowanie.tex                  Summary and conclusions
bib/
  references.bib                      BibTeX bibliography database
  plabbrv-fixed.bst                   Polish bibliography style
images/                               figures and screenshots
logos/                                university logos
```

## Build

The document is automatically compiled to `SOS-FW-project.pdf` and published to GitHub Releases and GitHub Pages via the GitHub Actions CI/CD workflow (`.github/workflows/compile.yml`) on every push to `main`.
