---
title: "Bizport"
permalink: /bizport/
excerpt: "Bizport"
toc: true
sidebar:
  title: "Index"
  nav: docs
---

## Bizport

*Bizport* is a powerful feature to allow sophisticated bulk data
manipulation and offline data maintenance. If existing data is exported,
the internal UUIDs will be exported in an Excel workbook, in the *bizId*
column and also where references between records exist.

On import, if the *bizId* of the row of data is recognised by the
system, the system interprets this as an attempt to update the data row.
If the UUID is not recognised, the system assumes that the value in the
*bizId* is actually a business key which will need to be replaced with a
UUID to guarantee uniqueness.

For safety, Bizport does not support data deletion.

To bulk-delete data, export and remove the data you want from the
*Bizport* workbook then delete the source data completely. Then import
the workbook. Note that once the source data has been deleted, the
*bizId* values in the workbook will no longer be recognised and new
UUIDs will be assigned.

Re-importing deleted data is effectively the same as creating an
entirely new data.

### Using Bizport

Enter the data into the template workbook ensuring that you enter values
into the *bizId* columns of each sheet.

Where data in other sheets is referenced, ensure that you reference the
data using the value you entered in the *bizId* column in the source
sheet.

Importing the workbook will create a new data because the values you
entered into the *bizId* columns will not be recognised, and new UUID
values will be generated.

### To enter bulk data using Bizport

Export the data.

Enter the data into the workbook ensuring that you enter values into the
*bizId* columns of each sheet.

Where data in other sheets is referenced, ensure that you reference the
data using the value you entered in the *bizId* column in the source
sheet.

Import the data. Any new records will be inserted because the system
will not recognise the values you have entered into the *bizId* and
reference columns.

Note however that once the new data has been imported, new UUIDs will be
generated for each row. To continue to manipulate this new data once it
has been imported, you need to export the data again so that you have
the newly created UUIDs.

### To remove bulk data using Bizport

Export the data.

Once the data has been successfully exported, delete the data from the
system, update the workbook and re-import the data. Because the source
data has been deleted from the system, only the data present in the
workbook will be imported.

Note that on import, the data will not be recognised by the system
because the source data was deleted. Even though your workbook may have
UUIDs in the *bizId* columns, these UUIDs will not be recognised and new
UUIDs will be created as the data is imported.

**[⬆ back to top](#bizport)**

---
**Next [WILDCAT Conversion Tool](./../_pages/wildcat-conversion-tool.md)**<br>
**Previous [Content Repository Tools](./../_pages/content-repository-tools.md)**  

