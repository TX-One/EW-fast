# EW-fast
Subdomain & Web Archive Tool

A tool for collecting subdomains and analyzing archived data from Wayback Machine.


---

## 🔹 Overview

Subdomain & Web Archive Tool is an advanced tool for gathering subdomains and analyzing archived data using open-source tools such as Amass, SubFinder, AssetFinder, httpx, and curl.
It provides multiple options for collecting, filtering, and analyzing data to identify active subdomains and live URLs.


---

## 🔹 Why You Need It

This innovative tool simplifies the enumeration process by
 efficiently collecting URLs from various sources. It ensures
 the collected URLs are live and ready for automated validation,
 streamlining the workflow for developers and security
 professionals.

## Key features:

1. Multi-source URL collection
2. Live URL verification
3. Automated validation preparation

By leveraging this tool, users can quickly gather and validate
 URLs across different platforms, saving time and effort in
 their enumeration tasks.

 ---
 
## 🔹 Prerequisites

Before running the tool, ensure that the following dependencies are installed on your system:

→ Amass

→ SubFinder

→ AssetFinder

→ httpx


You can install the missing tools using the following command:
```bash
go install -v github.com/projectdiscovery/subfinder/v2/cmd/subfinder@latest
go install -v github.com/OWASP/Amass/v3/...@master
go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest
go install -v github.com/tomnomnom/assetfinder@latest
```

---

# 🔹 Installation & Usage

```bash
git clone https://github.com/TX-One/EW-fast.git
cd EW-fast
chmod +x ./ewfast
sudo mv ewfast /usr/local/bin
cd ..
ewfast -h
```

# 3️⃣ Run the Tool

ewfast   -d   <domain>   [options]

Example:
```bash
ewfast -d example.com -a -b -f
```

---

# 🔹 Usage Guide

📌 Syntax:

ewfast -d <domain> [options]


---

🔹 Main Features

## 🟢 Subdomain Collection (-a)

This option gathers subdomains using the following tools and saves them to a file:

Amass

SubFinder

AssetFinder


Example:
```bash
ewfast -d example.com -a
```
💾 Subdomains will be saved in: example.com_subdomains.txt


---

## 🟢 Archived Data Collection (-b)

This option retrieves archived links from Wayback Machine and saves them to a file.

Example:
```bash
ewfast -d example.com -b
```
💾 Data will be saved in: example.com_hidden.txt


---

## 🟢 Filtering Live URLs (-f)

This option filters live URLs from the archived data file using httpx.

Example:
```bash
ewfast -d example.com -f
```

💾 Live URLs will be saved in: example.com_live_urls.txt


---

## 🟢 Extracting Active Links (-c)

This option analyzes subdomains and checks for working ones using httpx.

Example:
```bash
ewfast -d example.com -c
```

💾 Active subdomains will be saved in: example.com_working_links.txt


---

🔹 Practical Examples

✅ Example 1: Run all functions on a domain
```bash
ewfast -d example.com -a -b -f -c
```

**This command performs all tasks in one go:**

✔️ Collects subdomains
✔️ Gathers archived data
✔️ Filters live subs
✔️ Extracts active wayback-urls


---

✅ Example 2: Collect only subdomains
```bash
ewfast -d example.com -a
```

This command gathers subdomains using Amass, SubFinder, and AssetFinder only.


---

✅ Example 3: Analyze Wayback Machine data only
```bash
ewfast -d example.com -b
```

This command retrieves all archived data for example.com from the Wayback Machine.

---

# 🔹 Common Issues & Solutions

## ❌ Issue: Required tools not found

✔️ Ensure Amass, SubFinder, AssetFinder, httpx, and curl are properly installed.
✔️ Use which tool-name to check if the tool is available.

---

## ❌ Issue: "permission denied" when running the tool

✔️ Grant the necessary permissions using:
```bash
chmod +x subdomain_tool
```

---

# 🔹 Security Notes

⚠️ Ensure you run this tool only on domains you have explicit permission to scan.
⚠️ Do not use this tool for unauthorized security testing.


---

# 🔹 Contributions & Development

💡 Contributions are welcome! If you'd like to improve the tool or fix issues, submit a Pull Request or report bugs via Issues on the repository.

📧 Contact: https://t.me/TXpOne

---

🔹 License

📝 MIT License – The tool is free to use, but we are not responsible for any misuse.
