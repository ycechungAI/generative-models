## 2025-02-18 - Command Injection in Streamlit Demo
**Vulnerability:** Found `os.system` using formatted strings with user input (`save_path`) in `scripts/demo/streamlit_helpers.py`.
**Learning:** Even in demo scripts, user input must be sanitized or handled safely. `os.system` is dangerous with formatted strings.
**Prevention:** Use `subprocess.run` with list arguments to avoid shell injection.
