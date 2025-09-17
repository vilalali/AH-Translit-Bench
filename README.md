# AH-Translit_Bench: Arabic to Hindi Transliteration Benchmark Dataset

[![PyPI version](https://badge.fury.io/py/AH-Translit_Bench.svg)](https://pypi.org/project/AH-Translit_Bench/)
[![GitHub license](https://img.shields.io/github/license/vilalali/AH-Translit-Bench.svg)](https://github.com/vilalali/AH-Translit-Bench/blob/main/LICENSE)

## Repository Description

AH-Translit_Bench is a 2000-entry Arabic to Hindi transliteration benchmark dataset covering Al-Quran, bibliographical, and Modern Standard Arabic (MSA) domains. Provided as a pip-installable Python package for model testing and research.

## Dataset Overview

A benchmark dataset for Arabic to Hindi transliteration, providing parallel transliterated text pairs across diverse domains.

## Dataset Curators

This dataset was curated by:
*   **Vilal Ali**  
    Research Scholar at Data Sciences And Analytics Centre, IIIT Hyderabad
    Email: vilal.ali@research.iiit.ac.in
*   **Mohd Hozaifa Khan**  
    Research Scholar at Center for Visual Information Technology (CVIT) IIIT Hyderabad
    Email: mohd.hozaifa@research.iiit.ac.in
    
## Dataset Usage

This dataset is ideal for training, validating, and testing models for Arabic to Hindi transliteration tasks.

## Content Type

Text, specifically Arabic source text and its corresponding Hindi transliterated target text.

## Dataset Description

The AH-Translit_Bench dataset provides a collection of parallel text pairs for evaluating and developing Arabic to Hindi transliteration systems. It comprises text from three distinct domains: Al-Quran, bibliographical entries, and Modern Standard Arabic (MSA), ensuring a broad coverage for robust model development. Each entry consists of an Arabic string and its manually curated transliteration into Hindi (Devanagari script). The dataset's structure allows for straightforward loading and integration into various machine learning frameworks.

## Version Name

AH-Translit_Bench_v1.0

## File Type

CSV (Comma Separated Values)

## Version Overview

This is the initial release of the AH-Translit_Bench dataset, offering a foundational benchmark for Arabic to Hindi transliteration research.

## Version Description

This inaugural version of the AH-Translit_Bench dataset, version 1.0, provides a comprehensive collection of 2000 Arabic-Hindi transliteration pairs. The dataset is segmented into three domain-specific files to cater to varied research needs: `al-quran_test_bench_mark_500.csv` containing 500 entries from the Al-Quran domain, `biblo_test_bench_mark_1000.csv` with 1000 entries from the bibliographical domain, and `msa_test_bench_mark_500.csv` offering 500 entries from the Modern Standard Arabic (MSA) domain. Each entry consists of an Arabic string and its corresponding, carefully transliterated Hindi equivalent, making it suitable for training and evaluating transliteration models.

## Dataset Structure

The dataset is provided as a zip file (though usually downloaded directly via pip) containing three separate `.csv` files, each corresponding to a different domain. The structure within each CSV file is simple: the first column contains the Arabic text, and the second column contains its transliterated Hindi equivalent.

```AH-Translit_Bench.zip (Conceptual; files are installed directly)
├── al-quran_test_bench_mark_500.csv
├── biblo_test_bench_mark_1000.csv
└── msa_test_bench_mark_500.csv
```

**File Descriptions:**
*   `al-quran_test_bench_mark_500.csv`: Contains 500 entries from the domain of Al-Quran.
*   `biblo_test_bench_mark_1000.csv`: Contains 1000 entries from the bibliographical domain.
*   `msa_test_bench_mark_500.csv`: Contains 500 entries from the Modern Standard Arabic (MSA) domain.

**DIR Descriptions:**
```
AH-Translit-Bench
├── AH_Translit_Bench
│   ├── data
│   │   ├── al-quran_test_bench_mark_500.csv
│   │   ├── biblo_test_bench_mark_1000.csv
│   │   └── msa_test_bench_mark_500.csv
│   └── __init__.py
├── setup.py
├── README.md
└── LICENSE
```

## How to Use This Dataset

To use this dataset, first install it via pip:

```bash
pip install AH-Translit_Bench
```

Then, in your Python code, you can load specific domains:

```python
import pandas as pd
from AH_Translit_Bench import load_dataset, get_available_domains

# See what domains are available
print("Available domains:", get_available_domains())
# Expected output: Available domains: ['al-quran', 'biblo', 'msa']

# Load the Al-Quran dataset
al_quran_df = load_dataset('al-quran')
print("\nAl-Quran Dataset Head:")
print(al_quran_df.head())
print(f"Al-Quran Dataset Shape: {al_quran_df.shape}") # Expected: (500, 2)

# Load the Bibliographical dataset
biblo_df = load_dataset('biblo')
print("\nBibliographical Dataset Head:")
print(biblo_df.head())
print(f"Bibliographical Dataset Shape: {biblo_df.shape}") # Expected: (1000, 2)

# Load the Modern Standard Arabic (MSA) dataset
msa_df = load_dataset('msa')
print("\nMSA (Modern Standard Arabic) Dataset Head:")
print(msa_df.head())
print(f"MSA Dataset Shape: {msa_df.shape}") # Expected: (500, 2)

# Example of accessing data
first_arabic_text = al_quran_df['Arabic'].iloc # Corrected to access value
first_hindi_translit = al_quran_df['Hindi'].iloc # Corrected to access value
print(f"\nFirst Al-Quran entry: Arabic='{first_arabic_text}', Hindi='{first_hindi_translit}'")
```

## Example Data Snippet

Here's an example of how the data looks within the CSV files:

```csv
Arabic,Hindi
المطبعة الحيدرية،,"अल-मतबअह अल-हैदरियह,"
```

## License

This Python package code is licensed under the MIT License.

The dataset content (the CSV files) is released under the Creative Commons Attribution 4.0 International License (CC BY 4.0).
You are free to:
*   **Share** — copy and redistribute the material in any medium or format for any purpose, even commercially.
*   **Adapt** — remix, transform, and build upon the material for any purpose, even commercially.
Under the following terms:
*   **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
*   No additional restrictions — You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.
For the full license text, see: [https://creativecommons.org/licenses/by/4.0/](https://creativecommons.org/licenses/by/4.0/)


## Acknowledgements

The AH-Translit team at, IIIT Hyderabad, is happy to share this benchmark dataset. We extend our sincere thanks to **India Data** for hosting this dataset on their platform.

