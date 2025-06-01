## Backup Template for Nuclei

[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## Introduction

This **Backup Template** is a [Nuclei](https://github.com/projectdiscovery/nuclei) template that finds exposed **sensitive files**, **backup archives**, and **configuration files** on web servers. It’s useful for:

- Security researchers
- Penetration testers
- Bug bounty hunters
- Blue teams

---

## What It Detects

Common files and endpoints such as:
- `.env`, `.git/config`
- `config.php`, `credentials.json`
- `db.sql`, `backup.sql`, `.dump`
- `error.log`, `debug.log`, `laravel.log`
- `backup.zip`, `.tar.gz`, `.bak`, `.7z`
- Editor temp files (`.swp`, `.bak`)

Matchers look for HTTP 200 responses and keywords like:
- `password`
- `secret`
- `token`
- `Authorization:`


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
   nuclei -t backup-template/ -u https://example.com
   ```

4. (Optional) Copy into your custom templates folder:
   ```bash
   cp -r backup-template/ ~/nuclei-templates/custom/backup-template
   nuclei -t http/backup-template -l targets.txt
   ```
