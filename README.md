
# Elementor Exploit Tool

## Overview

This tool targets a known vulnerability (CVE-2022-4953) in the Elementor WordPress plugin, affecting versions <= 3.5.5. It automates the process of identifying vulnerable websites and generates exploit payloads for XSS (Cross-Site Scripting) and iFrame Injection attacks.

## Features

- **Automated Detection**: Quickly identifies if a target website is running a vulnerable version of the Elementor plugin.
- **Custom Payloads**: Users can choose between XSS or iFrame injection payloads and customize their contents.
- **Output to File**: Vulnerable URLs are saved in `vuln_targets.txt` for later reference.

## Requirements

- Python 3.x
- `requests` and `colorama` libraries

Install the required libraries with:
```bash
pip install requests colorama
```

## Google Dork 
```bash
*inurl:"/wp-content/plugins/elementor"
```


## Usage

1. Clone the repository:
    ```bash
    git clone https://github.com/sic4rio/WordPress-Elementor-Exploit-Tool.git
    cd WordPress-Elementor-Exploit-Tool
    ```

2. Run the script:
    ```bash
    python3 exploit.py
    ```

3. Follow the prompts to input the target URL and choose the payload type. The script supports URLs in the following formats:
   - `http://example.com`
   - `https://example.com`
   - `example.com`

4. The script will generate a payload URL if the target is vulnerable and save it to `vuln_targets.txt`.

## Example

```bash
Enter the target URL (e.g., https://example.com): example.com
It's Vulnerable!
Choose payload: (1) XSS or (2) iFrame Injection: 1
Enter the XSS alert message (e.g., 'xss'): Hello
XSS Payload URL: http://example.com/#elementor-action:action=lightbox&settings=...
```
## Thanks

Special thanks to the original exploit author for their work on identifying and documenting the vulnerability. Their efforts have been instrumental in creating this tool.
https://github.com/Wayne-Ker

## Disclaimer

This tool is intended for educational purposes only. Unauthorized use of this script on websites you do not own is illegal. The author assumes no responsibility for any misuse.


