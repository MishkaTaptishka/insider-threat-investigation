## 🛑 Exfiltration Script Overview

This PowerShell script demonstrates a realistic data exfiltration technique used by attackers. It simulates internal data generation, compression, and upload to a cloud storage endpoint — following the typical chain of collection ➝ compression ➝ exfiltration ➝ cleanup.

### 🔍 What the Script Does

1. **Generates Fake PII**
   - Creates a CSV file with fake employee data including names, SSNs, phone numbers, and salaries.

2. **Compresses the Data**
   - Downloads and installs 7-Zip silently.
   - Uses 7-Zip to compress the CSV into a `.zip` file.

3. **Exfiltrates to Azure Blob Storage**
   - Authenticates with a base64-encoded access key to a hardcoded Azure Blob Storage endpoint.
   - Uploads the zipped file using the REST API and `Invoke-WebRequest`.

4. **Cleans Up Evidence**
   - Moves the CSV and ZIP to `C:\ProgramData\backup` to hide from casual inspection.
   - Logs all activity to a hidden `.log` file.

---

### 📂 File Artifacts Created

| File Path                         | Purpose                           |
|----------------------------------|-----------------------------------|
| `C:\ProgramData\employee-data-<timestamp>.csv`   | Raw fake data file               |
| `C:\ProgramData\employee-data-<timestamp>.zip`   | Zipped exfil data                |
| `C:\ProgramData\backup\`                        | Final hiding place for artifacts |
| `C:\ProgramData\entropygorilla.log`             | Log of script execution          |

