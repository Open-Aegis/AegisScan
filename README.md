# AegisScan

AegisScan is an open-source, advanced **secret scanning tool** designed to detect sensitive information **anywhere**—including APIs, public endpoints, JavaScript files, websites, repositories, and other content sources. Whether you're a security researcher, developer, or bug bounty hunter, AegisScan helps you **proactively identify and mitigate leaked secrets** before attackers exploit them.

## 🚀 Features
- **Universal Scanning** – Detect secrets in APIs, JavaScript files, HTTP responses, web pages, public repositories, and more.
- **High-Speed Crawling** – Efficiently scrapes and analyzes web content for hidden credentials.
- **Multi-Format Detection** – Supports API keys, OAuth tokens, JWTs, hardcoded credentials, database connection strings, and more.
- **Custom Regex Rules** – Extend detection with your own patterns.
- **Integrations** – Works with Burp Suite, OpenAPI specs, and CLI for automation.
- **Real-Time Alerts** – Get instant notifications when secrets are found.

## 📌 Use Cases
- **Bug Bounty & Pentesting** – Find exposed API keys, AWS secrets, and tokens in web assets.
- **DevSecOps & CI/CD** – Prevent sensitive data leaks in your code and infrastructure.
- **Security Research** – Identify misconfigurations and vulnerabilities in public APIs and JavaScript files.
- **Automated Recon** – Enhance your reconnaissance workflows with deep scanning capabilities.

## 🛠 Installation
AegisScan is built with **Python** and requires minimal setup.

```bash
# Clone the repository
git clone https://github.com/OpenAegis/AegisScan.git
cd AegisScan

# Install dependencies
pip install -r requirements.txt
```

## 🚀 Usage
Run a basic scan on a target URL:
```bash
python aegisscan.py --url https://example.com
```

Scan a list of URLs:
```bash
python aegisscan.py --list urls.txt
```

Enable deep scanning for JavaScript files:
```bash
python aegisscan.py --url https://example.com --deep-js
```

Check for API keys in a public GitHub repo:
```bash
python aegisscan.py --github https://github.com/example/repo
```

## 🔍 Supported Secret Types
AegisScan detects various sensitive data types, including:
- **API Keys** (AWS, Google, Twilio, Stripe, GitHub, etc.)
- **OAuth Tokens & JWTs**
- **Hardcoded Passwords**
- **Database Connection Strings**
- **SSH Private Keys**
- **Cloud Credentials**

## 🛡️ How It Works
1. **Content Extraction** – Fetches web pages, API responses, JavaScript files, and repositories.
2. **Regex & Heuristic Matching** – Uses prebuilt and custom patterns to detect secrets.
3. **Entropy Analysis** – Identifies high-entropy strings likely to be sensitive.
4. **Verification** – Cross-checks validity where possible (e.g., API key validation).
5. **Reporting** – Outputs findings in JSON, CLI, or sends alerts via integrations.

## ⚙️ Configuration
You can configure AegisScan using a YAML file:
```yaml
scan:
  depth: 3
  include_js: true
  check_git: true
  alert_webhook: "https://your-alert-system.com"
```

## 📡 Future Roadmap
- 🔹 **Machine Learning-based Secret Detection**
- 🔹 **Live API Traffic Scanning**
- 🔹 **Burp Suite & ZAP Plugin**
- 🔹 **GitHub Actions Integration**

## 🤝 Contributing
We welcome contributions from the security community! To get started:
1. Fork the repository.
2. Create a new branch.
3. Submit a pull request.

## ⚠️ Disclaimer
AegisScan is intended for **legal security testing** and **ethical use only**. Unauthorized scanning of systems **without permission** may violate terms of service or laws in your region.

---

🔗 **GitHub Repo**: [https://github.com/OpenAegis/AegisScan](https://github.com/OpenAegis/AegisScan)  
💬 **Join the Community**: [Discord | Slack | Twitter]

