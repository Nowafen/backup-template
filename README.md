# Backup Template for Nuclei
###### Version:1.3

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

### Introduction

This **Backup Template** is a [Nuclei](https://github.com/projectdiscovery/nuclei) template that finds exposed **sensitive files**, **backup archives**, and **configuration files** on web servers. It’s useful for:

- Security researchers
- Penetration testers
- Bug bounty hunters
- Blue teams

---

## Usage

1. Install Nuclei (if not already):
   ```bash
   go install -v github.com/projectdiscovery/nuclei/v3/cmd/nuclei@latest
   ```

2. Clone this repository:
   ```bash
   git clone https://github.com/Nowafen/backup-template.git
   ```

3. Run against a single URL:
   ```bash
   nuclei -u https://example.com -t /backup-template
   ```

4. (Optional) Copy into your custom templates folder:
   ```bash
   cd backup-template ; cp backup.yaml ~/nuclei-templates/http/
   nuclei -l targets.txt  -t http/backup.yaml
   ```
