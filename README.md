# TradePaper Export Templates

Reusable **commercial invoice**, **packing list** and **shipping mark** templates, with a small worked shipment example.

**[Open TradePaper — free export document tools](https://tradepapertools.com/)**

Use these files to organize shipment information in a text editor or spreadsheet. For a browser-based workflow, use [TradePaper](https://tradepapertools.com/) to prepare and review your documents.

## Choose a template

| Document | Blank template | Worked example | Use it for |
| --- | --- | --- | --- |
| Commercial invoice | [Markdown template](templates/commercial-invoice.md) | [Example invoice](examples/commercial-invoice.md) | Parties, goods, quantities, prices and totals |
| Packing list | [CSV template](templates/packing-list.csv) | [Example packing list](examples/packing-list.csv) | Contents, weights and dimensions of each physical carton |
| Shipping mark | [Plain-text template](templates/shipping-mark.txt) | [Example carton mark](examples/shipping-mark.txt) | Identifying cartons against the packing list |

## Quick start

1. Download this repository using **Code → Download ZIP**, or open an individual file and save its raw contents.
2. Copy the blank templates and replace every bracketed placeholder with your shipment details. Open the packing list CSV in Excel, LibreOffice or Google Sheets.
3. Use the same order reference, product names and carton numbers across all three documents.
4. Work through the [document review checklist](docs/review-checklist.md) before sharing the files.

The CSV files are simple preparation worksheets. TradePaper does not currently import these files directly; enter the prepared details in the corresponding browser tool.

## Try the browser tools

- [Commercial Invoice Generator](https://tradepapertools.com/commercial-invoice-generator/)
- [Packing List Generator](https://tradepapertools.com/packing-list-generator/)
- [TradePaper homepage and all tools](https://tradepapertools.com/)

## A shipment that you can check by hand

All names, references and shipment details in the examples are fictional. The example is a learning worksheet, with explicit placeholders for shipment-specific details.

| Product | Cartons | Units per carton | Total units | Unit price | Line value |
| --- | --- | --- | --- | --- | --- |
| Plain notebook | 1–4 | 10 | 40 | USD 3.50 | USD 140.00 |
| Canvas pouch | 5–6 | 12 | 24 | USD 2.25 | USD 54.00 |
| **Total** | **6** | | **64** | | **USD 194.00** |

The example prices exclude freight, insurance and other charges. The invoice shows those example charges as zero; replace them for your shipment.

### Check weight and carton volume

The packing list uses **one row per physical carton**. Its dimension and weight columns apply to that carton, not to each item inside it.

| Carton group | Outer dimensions | Net weight per carton | Gross weight per carton | Group CBM |
| --- | --- | --- | --- | --- |
| Cartons 1–4 | 40 × 30 × 25 cm | 2.00 kg | 2.40 kg | 0.120 m³ |
| Cartons 5–6 | 50 × 40 × 30 cm | 1.20 kg | 1.50 kg | 0.120 m³ |
| **Shipment total** | **6 cartons** | **10.40 kg** | **12.60 kg** | **0.240 m³** |

For dimensions in centimetres:

```text
CBM per carton = length_cm × width_cm × height_cm / 1,000,000
Group CBM = CBM per carton × number of cartons
Shipment CBM = sum of all carton groups
```

For example, `40 × 30 × 25 / 1,000,000 × 4 = 0.120 m³`.
Do not multiply carton volume by the number of units inside the carton. Measure the outer package. This is geometric volume, not a carrier's billable or dimensional weight.

## Adapting the files

- Keep the CSV header row. Dimensions are in **cm** and weights are in **kg**.
- Copy a row for each additional carton. If a carton holds several products, adapt the layout to show the item breakdown while counting its physical dimensions and weight only once.
- Confirm product descriptions, origin, classification, trade terms and any destination-specific fields with the people handling your actual shipment. A generic template cannot determine those values for you.
- The sample shipping mark is for carton 1 of 6. Change its carton number and contents for the remaining cartons.
- Keep real buyer details and shipment files out of public issues and pull requests.

## About TradePaper

[TradePaper](https://tradepapertools.com/) provides browser tools for commercial invoices, packing lists, shipping marks and related export-document preparation. This repository contains companion templates and examples; the hosted application's source code is separate.

Suggestions for clearer templates or documentation are welcome through GitHub issues and pull requests. Use fictional data in examples.

## License

The original templates and documentation in this repository are available under the [MIT License](LICENSE). You may adapt and reuse them with the license notice.

中文说明：本仓库提供商业发票、装箱单和货箱唛头的空白模板、虚构示例与核对清单。在线工具请访问 [TradePaper 官网](https://tradepapertools.com/)。
