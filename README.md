# Shadow Vault

A terminal-based personal knowledge vault with a clean Rich UI. Store, retrieve, edit, and delete text entries that persist locally in a JSON file.

---

## Requirements

- Python 3.10+
- [rich](https://github.com/Textualize/rich)

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Usage

Run the vault:

```bash
python shadow_vault.py
```

You'll be greeted with a command prompt. Type any of the commands below.

---

## Commands

| Command | Description |
|---|---|
| `Shadow Vault: Save` | Add a new entry (prompts for ID and text) |
| `Shadow Vault: Edit` | Update an existing entry by ID |
| `Shadow Vault: Delete` | Remove an entry by ID |
| `Shadow Vault: Recall` | Display one entry (by ID) or all entries |
| `Shadow Vault: List` | Show all entry IDs and descriptions |
| `Shadow Vault: Reinforce` | Re-display core entries (configurable) |
| `Shadow Vault: Help` | Show the command list |
| `Shadow Vault: Exit` | Quit the program |

---

## Multi-line Input

When saving or editing entries, type your text and enter `END` on its own line when finished:

```
Enter text. Type END on its own line when done:
This is line one.
This is line two.
END
```

---

## Data Storage

Entries are saved automatically to `vault.json` in the same directory. The file is created on first save. You can change the path by editing the `ShadowVault("vault.json")` line at the bottom of the script.

---

## Customising Core Entries (Reinforce)

Open the script and edit the `core_ids` list inside `reinforce()`:

```python
core_ids: list[str] = ["001", "007"]  # Add your important entry IDs here
```

---

## File Structure

```
shadow_vault.py   # Main script
vault.json        # Auto-generated data file (created on first save)
requirements.txt  # Python dependencies
README.md         # This file
```
