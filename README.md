# Excel Name Cleaner

A lightweight Python script to **clean, normalize, and standardize name columns** in Excel files. It ensures that the **Last Name** column contains **only one name**, and that any extra names are correctly placed in the **First Name** column.

---

## Features

* Automatically detects and splits names in the `First Name` column  
* Moves the last word of `First Name` to `Last Name` when needed  
* If `Last Name` has multiple names, moves all except the last one to `First Name`  
* Ensures **only one name** remains in `Last Name`  
* Works directly with Excel (`.xlsx`) files  
* Simple and fast built with `pandas` and `openpyxl`

---

## Example

| Before (input.xlsx) | → | After (output.xlsx) |
|----------------------|---|----------------------|
| `Mbuyi wa mbombo KALONJI` | → | **First Name**: `Mbuyi wa mbombo`<br>**Last Name**: `KALONJI` |
| `Wa kabamba KABAMBA` | → | **First Name**: `Wa kabamba`<br>**Last Name**: `KABAMBA` |
| `Joseph MVIOKI BABUTANA` | → | **First Name**: `Joseph MVIOKI`<br>**Last Name**: `BABUTANA` |
| `Ya kanunkatu tshiabo MAMPU` | → | **First Name**: `Ya kanunkatu tshiabo`<br>**Last Name**: `MAMPU` |

---

## Installation

- Make sure you have **Python 3.8+** installed.
- **VS Code** with [**Jupyter**](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) Extension for Visual Studio Code *(optional but recommended)*


```bash
pip install pandas openpyxl
