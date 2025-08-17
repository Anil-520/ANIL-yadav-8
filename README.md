# ANIL-yadav-8
Identify and Remove Suspicious Browser Extesion 

import os
import json

# Path to Chrome extensions (Windows)
chrome_ext_path = os.path.expanduser(
    r'~\AppData\Local\Google\Chrome\User Data\Default\Extensions'
)

if os.path.exists(chrome_ext_path):
    print("Installed Extensions:\n")
    for ext_id in os.listdir(chrome_ext_path):
        manifest_path = os.path.join(chrome_ext_path, ext_id, "manifest.json")
        if os.path.exists(manifest_path):
            with open(manifest_path, "r", encoding="utf-8") as f:
                data = json.load(f)
                print(f"- {data.get('name', 'Unknown')} | Version: {data.get('version', 'N/A')}")
else:
    print("Chrome extensions folder not found.")
