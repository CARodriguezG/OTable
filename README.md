# OTable
The OTable is an extended class of JTable embedded with an ArrayList of Objects used to display and edit regular two-dimensional tables of cells.
It uses a javax.swing.DefaultTableModel.

It allows to insert, remove, update and retrieve row data. Also, which data to display in the table.

## Inserting/Adding a row

In order to inserting/adding a new row to the `OTable` you simply do:

    OTable myOTable = new OTable();
    // More code here...
    myOTable.addRow(data, displayData);
    
Where `data` is the object to be added to the ArrayList of Objects (so we can keep the reference of this object) and where `displayData` is an array of Object. ([Learn more about Varargs](https://docs.oracle.com/javase/8/docs/technotes/guides/language/varargs.html))
