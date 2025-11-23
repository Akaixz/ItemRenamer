# ItemRenamer

<p align="center">
  <img src="https://img.shields.io/badge/Status-Active-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Game-Fallout%204-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Platform-Synthesis-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Author-Empyrean-purple?style=flat-square"/>
</p>

---

## Description

**ItemRenamer** is a Synthesis Patcher for Fallout 4 designed to adjust item names to match those specified in user-configurable files. Its primary goal is to facilitate item renaming based on custom renaming rules.

A default config file is provided with support for **FJX-Imperium** and **MCPR 300**, serving as a base for future renamings.

---

## Features

- **Flexible Renaming:** Adjust item names based on FormID and Origin Plugin.
- **Modular Configuration:** Supports multiple JSON files read in alphabetical order.
- **Broad Support:** Works with various record types.

### Currently Supported Mods
- MW2022 - MCPR 300 - Barrett MRAD
- MW2022 - FJX-Imperium

### Supported Record Types
- 🔫 Weapons
- 💊 Ammunition
- 🛡️ Armor
- 📚 Books
- ⚙️ Components
- 📦 Misc items

---

## Configuration

To add support for additional mods or to change a name definition, simply create one or more `.json` files in the patcher data directory. The patcher reads all files in alphabetical order.

**Example Directory:**
You could create a file called `CustomRules.json` in:
`C:/../Synthesis/Data/Fallout 4/ItemRenamer`

### JSON Structure

The format uses the `FormID` (without the load order index) and the `Plugin/Master` filename where the item was originally defined.

**Example:**
If you want to change the name of the "10mm" item from *Gold* to *10mm Cool Pistol*:

```json
{
  "004822:Fallout4.esm": "10mm Cool Pistol"
}
```
- 004822: The FormID of the item (as seen in xEdit).

- Fallout4.esm: The Plugin or Master file where the item is defined.

- 10mm Cool Pistol: The new desired name.

Note: Remember to add commas after every line except the last one, and ensure the file is enclosed in opening { and closing } braces. You can browse the Default folder in the patcher data directory for more examples.
