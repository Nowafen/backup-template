### Backup Template for Nuclei
###### Version:1.4

This **Backup Template** is a [Nuclei](https://github.com/projectdiscovery/nuclei) template that finds exposed **sensitive files**, **backup archives**, and **configuration files** on web servers. It’s useful for:

- Security researchers
- Penetration testers
- Bug bounty hunters
- Blue teams

---

## Usage

1. Install Nuclei 

2. Clone this repository:
   ```bash
   git clone https://github.com/Nowafen/backup-template.git
   ```

3. Run against a single URL:
   ```bash
   nuclei -u https://example.com -t backup-template/
   ```
