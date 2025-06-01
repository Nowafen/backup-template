# Backup Template

[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## Overview

**Backup Template** is a Nuclei template for scanning and detecting exposed sensitive files, credentials, configuration files, backups, logs, and potential information leakage on web servers.

This template helps security researchers, pentesters, and bug bounty hunters to quickly identify common sensitive files and backups accidentally exposed to the internet.

---

## Template Details

- Detects files like `.env`, `config.php`, `credentials.json`, database dumps, backup archives, logs, CI/CD configs, and more.
- Matches HTTP 200 responses containing keywords related to passwords, secrets, keys, tokens, and other sensitive information.
- Includes deep paths, old backups, and version control files.

---

## Usage

1. **Prerequisites**

Make sure you have [Nuclei](https://github.com/projectdiscovery/nuclei) installed and set up on your system.

2. **Clone this repository**

```bash
git clone https://github.com/Nowafen/backup-template.git
cd backup-template
