![Banner](banner.png)

# analyze-traffic-analyzer

## Project Description

Analyze network traffic patterns. Focused on Data analysis and reporting.

## Installation Instructions

```
pip install -r requirements.txt
```

## Usage Examples

```
python3 main.py <input_file> [--output_file <output_file>]
```

The input CSV must have `source_ip` and `data_transferred` columns. The report counts distinct source IPs and sums the data transferred column.

## Verified behavior
- A sample with two distinct source IPs and data values 100, 50, and 25 reported 2 unique IPs and a total of 175.
- The results are reported through log lines, not printed output. With `--output_file`, the report is also written as a CSV with columns `Unique IPs` and `Total Data Transferred`.
- A missing input file exits 1.
- Only distinct `source_ip` values are counted. Destination addresses are not counted, and the column names must match exactly.

## Security Warnings

Do not use for malicious purposes.

## License

GNU General Public License v3.0 - Licensed to CY83R-3X71NC710N
