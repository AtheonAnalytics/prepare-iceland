# Weekly Sales File

## General Report Overview

### Source report: Weekly Sales Report

The report consists of one table of columnar data with one row per SKU. There are 9 attribute columns followed by 12 metric columns. The table has a header row with descriptions of the columns.

The data table is proceeded by a header of 4 rows, which contain data regarding the date and supplier context.&#x20;

## Preparation Procedure

### 1. Add columns to data table

5 new columns must be added to the data table with the following column descriptions added to the table header row:

1. Retail Week
2. Week Commencing
3. Supplier Number
4. Supplier Name
5. Supplier Address

{% hint style="info" %}
If using a spreadsheet application the new columns will be inserted at V:Z or C22:C26 (depending on reference style)
{% endhint %}

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption><p>5 new columns shown in yellow</p></figcaption></figure>

### 2. Extract data from header and populate new columns

1. From the second row of the header, extract the "Retail Week" value.  Populate all rows in the new **Retail Week** column with the value.
2. From the second row of the header, extract the "Commencing" value.  Populate all rows in the new **Week Commencing** column with the value.
3. From the third row of the header, extract the first component (components separated by ":") of the "Supplier" value.  Populate all rows in the new **Supplier Number** column with the value.
4. From the third row of the header, extract the second component (components separated by ":") of the "Supplier" value.  Populate all rows in the new **Supplier Name** column with the value.
5. From the third row of the header, extract the third component (components separated by ":") of the "Supplier" value.  Populate all rows in the new **Supplier Address** column with the value.

{% hint style="warning" %}
All values should be trimmed to remove surrounding white space before being written into the new columns
{% endhint %}

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption><p>Extracted header information in red, populated columns in orange</p></figcaption></figure>

### 3. Remove header rows

Delete the top 4 rows of the file, so that the header of the data table is the first row in the file.

{% hint style="info" %}
If using a spreadsheet application the rows to be removed are 1:4 or R1:R4 (depending on reference style)
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Rows to be removed in yellow</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption><p>Header rows removed</p></figcaption></figure>

### 4. Save the file

Save the file as CSV type with UTF-8 encoding.

## File Attributes

| Aspect        | Attribute                                |
| ------------- | ---------------------------------------- |
| Columns       | 26                                       |
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
| Number of columns | 26                      |
| Number of Rows    | >1                      |
| Date Format       | dd-mm-yyyy              |

## File and Column Definitions

{% content-ref url="weekly-sales-file-definition.md" %}
[weekly-sales-file-definition.md](weekly-sales-file-definition.md)
{% endcontent-ref %}

## Example File

{% content-ref url="example-file.md" %}
[example-file.md](example-file.md)
{% endcontent-ref %}
