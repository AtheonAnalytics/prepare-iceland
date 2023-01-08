# Weekly Estate Stock File

## General Report Overview

### Source report: Weekly Stock Report

The report consists of one table of columnar data with one row per SKU. There are 9 attribute columns followed by a variable number of metric columns, depending on the number of depots referenced. The table has a header row with descriptions of the columns.

The data table is proceeded by a header of 4 rows, which contain data regarding the date and supplier context.&#x20;

## Preparation Procedure

### 1. Remove Depot Specific Columns

All "On Hand Cases" columns that pertain to a specific depot must be removed. The column description in the header will contain the name of the depot e.g.

> On Hand Cases Deeside

where "Deeside" is the name of the depot.

There are 3 "On Hand Cases" columns following the depot specific columns that are suffixed  "Depots", "Store", "Company" respectively. All other columns prefixed with "On Hand Cases" can be assumed to be depot specific and therefore should be removed.

{% hint style="info" %}
If using a spreadsheet application the columns to be removed begin at Q or R17 (depending on reference style)
{% endhint %}

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Columns to be removed in yellow</p></figcaption></figure>

### 2. Add columns to data table

5 new columns must be added to the data table with the following column descriptions added to the table header row:

1. Retail Week
2. Week Commencing
3. Supplier Number
4. Supplier Name
5. Supplier Address

{% hint style="info" %}
If using a spreadsheet application the new columns will be inserted at U:Y or C21:C25 (depending on reference style)
{% endhint %}

<figure><img src="../../.gitbook/assets/image (3) (2).png" alt=""><figcaption><p>5 new columns to be added in yellow</p></figcaption></figure>

### 3. Extract data from header and populate new columns

1. From the second row of the header, extract the "Retail Week" value.  Populate all rows in the new **Retail Week** column with the value.
2. From the second row of the header, extract the "Commencing" value.  Populate all rows in the new **Week Commencing** column with the value.
3. From the third row of the header, extract the first component (components separated by ":") of the "Supplier" value.  Populate all rows in the new **Supplier Number** column with the value.
4. From the third row of the header, extract the second component (components separated by ":") of the "Supplier" value.  Populate all rows in the new **Supplier Name** column with the value.
5. From the third row of the header, extract the third component (components separated by ":") of the "Supplier" value.  Populate all rows in the new **Supplier Address** column with the value.

{% hint style="warning" %}
All values should be trimmed to remove surrounding white space before being written into the new columns
{% endhint %}

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption><p>Extracted header information in red, populated columns in orange</p></figcaption></figure>

### 4. Remove header rows

Delete the top 4 rows of the file, so that the header of the data table is the first row in the file.

<figure><img src="../../.gitbook/assets/image (7) (1).png" alt=""><figcaption><p>Rows to be removed in yellow</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption><p>Header rows removed</p></figcaption></figure>

### 4. Save the file

Save the file as CSV type with UTF-8 encoding.

## Output Attributes

| Aspect        | Attribute                                |
| ------------- | ---------------------------------------- |
| Columns       | 25                                       |
| Rows          | 1 -> \~500 (depending on number of SKUs) |
| Header Row    | Yes                                      |
| Data Protocol | File                                     |
| File Type     | CSV                                      |
| Encoding      | UTF-8                                    |
| Date Format   | dd-mm-yyyy                               |

## Test Regime

| Test              | Expected Output         |
| ----------------- | ----------------------- |
| File Type         | CSV with UTF-8 encoding |
| File Size         |                         |
| Number of columns | 25                      |
| Number of Rows    | >1                      |
| Date Format       | dd-mm-yyyy              |

## Output File and Column Definitions

{% content-ref url="weekly-estate-stock-file-definition.md" %}
[weekly-estate-stock-file-definition.md](weekly-estate-stock-file-definition.md)
{% endcontent-ref %}

## Example Output File

{% content-ref url="example-output-file.md" %}
[example-output-file.md](example-output-file.md)
{% endcontent-ref %}
