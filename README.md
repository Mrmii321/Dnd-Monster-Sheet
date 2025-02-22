# README

## Overview
This file (`output.xlsx`) contains a dataset related to Dungeons & Dragons (D&D) creatures, including their attributes, abilities, and statistics. The dataset is stored in an Excel spreadsheet format with a single sheet named `Sheet1`.

## File Structure
- **Sheet1**: Contains a list of creatures and their associated data.

## Columns Explanation
The following columns are present in the dataset:
- **name**: The name of the creature.
- **meta**: Description of the creature's size, type, and alignment.
- **Armor Class**: The armor class value and type (e.g., natural armor).
- **Hit Points**: The total hit points (including dice notation).
- **Speed**: Movement speeds including walking, flying, swimming, or burrowing.
- **STR, DEX, CON**: Strength, Dexterity, and Constitution scores.
- **STR_mod, DEX_mod**: The corresponding ability modifiers.
- **Challenge**: The creature’s Challenge Rating (CR) and XP value.
- **Traits**: Special abilities and features of the creature, stored as HTML-formatted text.
- **Actions**: List of actions the creature can take, also in HTML format.
- **Legendary Actions**: Special actions available to legendary creatures, in HTML format.
- **img_url**: A URL linking to an image representation of the creature.
- **Damage Immunities**: Any damage types the creature is immune to.
- **Condition Immunities**: Any conditions the creature is immune to.
- **Damage Resistances**: Types of damage the creature resists.
- **Damage Vulnerabilities**: Types of damage the creature is vulnerable to.
- **Reactions**: Any reaction-based abilities the creature has.

## Notes
- Some fields, such as `Legendary Actions` and `Reactions`, may contain `NaN` if the creature does not have these abilities.
- Traits, Actions, and Legendary Actions are formatted in HTML, which may require parsing for readability.
- The dataset appears to be sourced from an online D&D database, with URLs pointing to images hosted on an external server.

## Usage
This file can be used for:
- Importing into a D&D campaign management tool.
- Extracting creature statistics for game automation.
- Data analysis or visualization of creature attributes.

## Dependencies
To read and manipulate this file in Python, use the `pandas` library:
```python
import pandas as pd
xls = pd.ExcelFile("output.xlsx")
df = xls.parse("Sheet1")
print(df.head())
```

