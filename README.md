# Kenya Banks Branches Data

This repository contains structured data for bank branches in Kenya, sourced from the Kenya Bankers Association (KBA) website (https://www.kba.co.ke) as of the end of 2025.

## Data Files

- `json/bank_branch.json`: Hierarchical JSON format, grouping branches under each bank.
- `json/flat.json`: Flat JSON format, each record is a single branch.
- `csv/bank_branches.csv`: CSV file with the same columns as the flat JSON file.

## Data Fields
Each branch record contains:
- `bank_code`: Bank code (e.g., "01")
- `bank_name`: Name of the bank
- `branch_code`: Branch code (e.g., "01 231")
- `branch_name`: Name of the branch
- `full_name`: Concatenation of bank and branch name
- `county_code`: County code (e.g., "28")
- `county_name`: County name (e.g., "Elgeyo-Marakwet")

Special handling:
- If a branch had `county_code` "00" and `county_name` "UNKNOWN", it is set to `county_code` "47" and `county_name` "Nairobi County".
- Leading zeros are removed from county codes and names.

## Source
Data is based on the official branch listing from [kba.co.ke](https://www.kba.co.ke) as of the end of 2025.

## Usage
You can use the JSON or CSV files for data analysis, integration, or reporting on Kenyan bank branches.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

**Note:** The data provided in this repository is given AS IS, without warranty or guarantee of accuracy or completeness. Please refer to the Kenya Bankers Association (KBA) for official and up-to-date information.
