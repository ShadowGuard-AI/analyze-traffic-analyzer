![Lake Maracaibo at night with no writing anywhere: dark water, steady shore lights, one muted flash inside a cloud tower](intro-banner.png)

# analyze-traffic-analyzer

![Cloud towers over the lake lit from within, one full fork over the water, the name chalked on the dark timber face of the jetty hut](banner.png)

![One forked discharge over a black horizon line, the heading plate](logo.png)

![Lake scene in three bands: cloud interiors brighten and fade, a single bolt appears and is gone, the wind sock stirs and settles](scene.svg)


# analyze-traffic-analyzer

## Project Description

Analyze network traffic patterns. Focused on Data analysis and reporting.


![Section divider](sep-light.svg)

## Installation Instructions

```
pip install -r requirements.txt
```


![Section divider](sep-heavy.svg)

## Usage Examples

```
python3 main.py <input_file> [--output_file <output_file>]
```

The input CSV must have `source_ip` and `data_transferred` columns. The report counts distinct source IPs and sums the data transferred column.

> Watch note: the column names must match exactly. The count rests on source_ip and the sum rests on data_transferred, spelled as the source spells them.


![Section divider](sep-heavy.svg)

## Verified behavior
- A sample with two distinct source IPs and data values 100, 50, and 25 reported 2 unique IPs and a total of 175.
- The results are reported through log lines, not printed output. With `--output_file`, the report is also written as a CSV with columns `Unique IPs` and `Total Data Transferred`.

> Watch note: results are reported through log lines, not printed output. The CSV file is the second destination, not the first.
- A missing input file exits 1.

> Watch note: a missing input file exits 1.
- Only distinct `source_ip` values are counted. Destination addresses are not counted, and the column names must match exactly.


![Section divider](sep-light.svg)

## Security Warnings

Do not use for malicious purposes.


![Section divider](sep-heavy.svg)

## License

GNU General Public License v3.0 - Licensed to CY83R-3X71NC710N
