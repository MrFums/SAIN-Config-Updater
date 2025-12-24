# SAIN SPT Config Updater

A **simple config migration tool** for SAIN (SPT-AKI).

You give it:
1. A folder with your **current SAIN configs**
2. A folder with the **new / default SAIN configs**
3. An **output folder** where the merged configs will be written

The script updates **all JSON files** in the folder structure  
➡️ **except `Info.json`, which is always copied as-is**.

---

## What This Does

- Uses your **current config values**
- Applies them onto the **new default configs**
- Keeps **new options** added by SAIN updates
- Processes **every JSON file automatically**
- Writes results to a **separate output folder**
- Generates a `diff_log.txt` showing what changed

Your original configs are **never modified**.

---

## Requirements

- Python 3.8+
- No external libraries

---

## Folder Setup (Important)

You need **three folders**:

```text
OLD_CONFIGS     → your current SAIN config folder
NEW_CONFIGS     → fresh/default SAIN config folder
OUTPUT_CONFIGS  → merged configs will be written here
```

## How To Run

From a terminal in the script folder:

`python sainupdater.py OLD_CONFIGS NEW_CONFIGS OUTPUT_CONFIGS`

Example:
`python sainupdater.py "C:/SAIN/old/SAIN" "C:/SAIN/new/SAIN" "C:/SAIN/output/SAIN"`
