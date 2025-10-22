# SQLLER v7.0 🔥

![Version](https://img.shields.io/badge/version-7.0-red.svg)
![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![License](https://img.shields.io/badge/license-Educational-green.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

> **Advanced SQL Injection Detection Tool with Genetic Algorithm Evolution, Real Playwright Crawling, and WAF Bypass Capabilities**

---

## 🚀 Features

### Core Capabilities
- ✅ **Real Genetic Algorithm** - Payload evolution through generations with mutation and crossover
- ✅ **Playwright Automation** - JavaScript/SPA rendering and API discovery
- ✅ **Statistical Analysis** - Pattern matching with Z-score anomaly detection
- ✅ **WAF Detection & Bypass** - Signature-based WAF identification and evasion strategies
- ✅ **Multi-threaded Testing** - Concurrent request handling for speed
- ✅ **False Positive Elimination** - Statistical validation of findings

### Security Features
- 🔒 **Domain Restriction** - Only tests target domain and subdomains
- 🛡️ **WAF Bypass Engine** - Automatic evasion technique generation
- 📊 **Confidence Scoring** - Statistical reliability metrics
- 🧬 **Adaptive Payloads** - Evolution-based payload optimization

### Detection Techniques
- **Boolean-based Blind SQLi**
- **Time-based Blind SQLi**
- **Error-based SQLi**
- **UNION-based SQLi**

### Supported DBMS
- MySQL/MariaDB
- PostgreSQL
- Microsoft SQL Server
- Oracle
- SQLite

---

## 📋 Requirements

### System Requirements
- Python 3.8 or higher
- 2GB RAM minimum
- Internet connection

### Python Dependencies
```bash
rich>=13.0.0
aiohttp>=3.9.0
beautifulsoup4>=4.12.0
playwright>=1.40.0
```

---

## 🔧 Installation

### 1. Clone Repository
```bash
git clone https://github.com/yourusername/sqller.git
cd sqller
```

### 2. Install Python Dependencies
```bash
pip install rich aiohttp beautifulsoup4 playwright
```

### 3. Install Playwright Browsers
```bash
playwright install chromium
```

### 4. Verify Installation
```bash
python sqller.py --help
```

---

## 🎯 Usage

### Basic Scan
```bash
python sqller.py -d example.com
```

### Advanced Scan
```bash
python sqller.py -d example.com --depth 5 --max-urls 200 -t 20
```

### Command Line Options

| Option | Description | Default |
|--------|-------------|---------|
| `-d, --domain` | Target domain (required) | - |
| `--depth` | Crawl depth | 3 |
| `--max-urls` | Maximum URLs to crawl | 50 |
| `-t, --threads` | Concurrent threads | 10 |

---

## 📖 Examples

### Example 1: Quick Scan
```bash
python sqller.py -d testsite.com
```

### Example 2: Deep Scan
```bash
python sqller.py -d testsite.com --depth 5 --max-urls 300
```

### Example 3: High-Speed Scan
```bash
python sqller.py -d testsite.com -t 30
```

### Example 4: Subdomain Testing
```bash
# Automatically includes subdomains
python sqller.py -d example.com
# Tests: example.com, api.example.com, www.example.com, etc.
```

---

## 🔒 Domain Restriction

SQLLER v7.0 implements **strict domain restriction** for ethical testing:

### ✅ Allowed
- Target domain: `example.com`
- Subdomains: `api.example.com`, `www.example.com`

### ❌ Blocked
- External domains: `google.com`, `facebook.com`
- All third-party resources

**Security Note**: The tool automatically blocks and logs any external URL attempts.

---

## 📊 Output

### Terminal Output
- Real-time vulnerability detection
- Crawling progress with statistics
- WAF detection notifications
- Genetic algorithm evolution status

### JSON Report
Automatically saved as: `sqller_v7_reality_{domain}_{timestamp}.json`

```json
{
  "tool": "SQLLER v7.0 Reality - 100% Functional",
  "domain": "example.com",
  "domain_restriction": "ONLY example.com + subdomains",
  "scan_duration": 120.5,
  "vulnerabilities": [...]
}
```

---

## 🧬 Genetic Algorithm Engine

### How It Works

1. **Initial Population** - Generates diverse payload population
2. **Fitness Evaluation** - Tests payloads and calculates fitness scores
3. **Selection** - Tournament selection of best performers
4. **Crossover** - Combines genetic material from parents
5. **Mutation** - Applies random mutations for diversity
6. **Evolution** - Iterates through generations

### Mutation Strategies
- Case mutation (uPpEr/LoWeR)
- Encoding mutation (URL encoding variations)
- Comment insertion (`/**/` injection)
- Whitespace mutation (tab, newline alternatives)
- Keyword obfuscation (bypassing filters)

---

## 🛡️ WAF Detection

### Supported WAFs
- Cloudflare
- AWS WAF
- Akamai
- Imperva/Incapsula
- ModSecurity

### Detection Method
- Header signature analysis
- Response body pattern matching
- Status code correlation
- Confidence scoring

### Bypass Strategies
- Automatic evasion technique generation
- Adaptive payload mutation
- Real-time strategy adjustment

---

## 📈 Statistical Analysis

### Anomaly Detection
- **Z-score Analysis** - Detects response length anomalies
- **Time Variance** - Identifies timing attacks
- **Pattern Matching** - SQL error signature detection
- **Jaccard Similarity** - Response comparison

### False Positive Elimination
- Baseline establishment (3 requests)
- Statistical validation
- Confidence scoring
- Multi-technique verification

---

## ⚠️ Legal Disclaimer

**IMPORTANT**: This tool is for **educational and authorized testing purposes only**.

### Legal Use Cases
✅ Testing your own applications
✅ Authorized penetration testing
✅ Security research with permission
✅ Bug bounty programs

### Illegal Use Cases
❌ Unauthorized access attempts
❌ Testing without explicit permission
❌ Malicious activities
❌ Violation of computer fraud laws

**By using this tool, you agree to:**
- Only test systems you own or have explicit written permission to test
- Comply with all applicable laws and regulations
- Accept full responsibility for your actions

---

## 🔧 Technical Architecture

### Phase 1: Reconnaissance (Playwright Crawler)
```
Target Domain → JavaScript Rendering → Link Extraction → 
Form Discovery → API Endpoint Detection → Parameter Extraction
```

### Phase 2: Exploitation (Genetic Testing)
```
Generate Population → Test Payloads → Calculate Fitness → 
Selection → Crossover → Mutation → Evolution → Vulnerability Detection
```

### Phase 3: Analysis (Statistical Validation)
```
Baseline Establishment → Anomaly Detection → 
Pattern Matching → Confidence Scoring → False Positive Elimination
```

---

## 📝 Troubleshooting

### Common Issues

#### Playwright Installation Error
```bash
# Solution
playwright install chromium
```

#### Permission Denied
```bash
# Solution (Linux/Mac)
chmod +x sqller.py
```

#### ModuleNotFoundError
```bash
# Solution
pip install -r requirements.txt
```

#### SSL Certificate Errors
The tool automatically handles SSL verification. If issues persist:
```python
# Already configured: ssl=False in session
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow PEP 8 style guide
- Add docstrings to functions
- Include unit tests
- Update documentation

---

## 📚 Resources

### Learning Resources
- [OWASP SQL Injection Guide](https://owasp.org/www-community/attacks/SQL_Injection)
- [PortSwigger SQL Injection Labs](https://portswigger.net/web-security/sql-injection)
- [Genetic Algorithms Explained](https://en.wikipedia.org/wiki/Genetic_algorithm)

### Related Tools
- SQLMap
- Havij
- jSQL Injection

---

## 📄 License

This project is licensed for **educational purposes only**. 

**NO WARRANTY**: This software is provided "as is" without warranty of any kind.

---

## 👨‍💻 Author

**MUHAMMED FARHAN**

- GitHub: [@VIRTUAL-VIRUZ](https://github.com/VIRTUAL-VIRUZ)
- Twitter: [@7H3CYF4RX](https://twitter.com/7H3CYF4RX)

---

## 🙏 Acknowledgments

- OWASP Foundation for security research
- Playwright team for browser automation
- Rich library for beautiful terminal output
- Security research community

---

## 📞 Support

### Bug Reports
Open an issue on GitHub with:
- System information
- Error messages
- Steps to reproduce

### Feature Requests
Submit via GitHub Issues with:
- Detailed description
- Use case examples
- Expected behavior

---

## 🔄 Changelog

### v7.0 (Current)
- ✨ Genetic algorithm payload evolution
- ✨ Real Playwright automation
- ✨ Statistical analysis engine
- ✨ WAF detection and bypass
- ✨ Domain restriction security
- ✨ Multi-threaded testing
- ✨ False positive elimination

---

## ⭐ Star History

If you find this tool useful, please consider giving it a star! ⭐

---

## 📱 Stay Updated

Watch this repository for updates and new features!

```bash
# Check for updates
git pull origin main
```

---

**Remember**: With great power comes great responsibility. Use this tool ethically and legally.

🔥 Happy (Ethical) Hacking! 🔥
