# 🛡️ Injectra

Injectra is a powerful CLI-based payload generator and vulnerability testing toolkit designed for penetration testers and bug bounty hunters. 
It supports XSS, SQL Injection, and Command Injection vectors with payload customization, encoding options, and export features.


# 📦 Features

- 🔍XSS Module
  - Reflected, Stored, DOM-Based & Evasion payloads
  - Payload encoding: Base64, URL, Unicode
  - Export payloads to `.json`

- 💉SQL Injection Module
  - Error-Based, Union-Based, Blind & WAF Bypass payloads
  - Payload testing on target URLs
  - Multiple encodings supported

- 🖥️Command Injection Module
  - Linux & Windows payloads
  - Encoding & obfuscation options
  - Clipboard support & export formats
    
# 🚀 Usage

bash

python main.py --xss --target https://example.com

python main.py --sqli --target https://example.com --param id --type error --encode base64

python main.py --cmdinj --os linux --encode url --obfuscate


# 🎯 Flags & Parameters

# XSS

| Flag         | Description                                              |
| ------------ | -------------------------------------------------------- |
| `--xss`      | Run the XSS module                                       |
| `--xss-type` | XSS types: `reflected`, `stored`, `dom`, `all`, `bypass` |
| `--encode`   | Encode payloads: `base64`, `url`, `unicode`              |
| `--target`   | (Optional) Show target in logs                           |


# SQL Injection

| Flag        | Description                                    |
| ----------- | ---------------------------------------------- |
| `--sqli`    | Run the SQL Injection module                   |
| `--target`  | Target URL (required for scanning)             |
| `--param`   | GET parameter to test (default: `id`)          |
| `--type`    | Payload type: `error`, `union`, `blind`, `all` |
| `--encode`  | Encoding method                                |
| `--keyword` | Optional keyword to detect in response         |



# Command Injection

| Flag          | Description                          |
| ------------- | ------------------------------------ |
| `--cmdinj`    | Run the Command Injection module     |
| `--os`        | Target OS: `linux`, `windows`, `all` |
| `--encode`    | Encoding method                      |
| `--obfuscate` | Use `${IFS}` obfuscation             |
| `--export`    | Output format: `cli`, `json`         |
| `--copy`      | Copy output to clipboard             |


# 🖼️ Screenshots

# XSS Payload Generation

![XSS 1](https://github.com/user-attachments/assets/33e045f7-fd1a-460f-b4b6-067b92fe266e)

![XSS 2](https://github.com/user-attachments/assets/eb79dba9-933e-4ba4-b001-1cba3086ffdc)


# SQL Injection Scanning

![SQL 1](https://github.com/user-attachments/assets/f4513b6b-7e2b-427b-b773-4f366fdd78ac)

![SQL 2](https://github.com/user-attachments/assets/d86356ec-0716-4bad-abca-eb104bd7f67c)

![SQL 3](https://github.com/user-attachments/assets/773fae99-94a1-4d0d-9bbd-70efc73bc9f0)

# Command Injection Generation

![Cmd Injection 1](https://github.com/user-attachments/assets/5d3c3949-737a-488d-a200-68b51efcd942)

![Cmd Injection 2](https://github.com/user-attachments/assets/479d7890-0e07-4251-841f-07867935b7d3)

# 🧰 Requirements

Install dependencies using:

pip install requests pyperclip


# ⚠️ Disclaimer

This tool is intended for educational and authorized testing only. Using it on unauthorized targets is illegal.


