# OTable
The OTable is an extended class of JTable embedded with an ArrayList of Objects used to display and edit regular two-dimensional tables of cells.
It uses a javax.swing.DefaultTableModel.

It allows to insert, remove, update and retrieve row data. Also, which data to display in the table.

## Inserting/Adding a row

In order to inserting/adding a new row to the `OTable` you simply do:

    OTable myOTable = new OTable();
    // More code here...
    myOTable.addRow(obj, displayData);
    
Where `obj` is the object to be added to the ArrayList of Objects (so we can keep the reference of this object) and where `displayData` is an array of Objects.

You can insert the new row by using an `Object[]` variable. For example:

    // Example 1: Using initialized array
    Object[] displayData = new Object[2];
    displayData[0] = "My data 1";
    displayData[1] = "My data 2";
    myOTable.addRow(obj, displayData); 
    
    // Example 2: One-line initialization
    Object[] displayData = new Object[]{ "My data 1", "My data 2", ...... };
    myOTable.addRow(obj, displayData);

To keep it simple, `addRow` method uses `displayData` as a Variable Argument ([Learn more about Varargs](https://docs.oracle.com/javase/8/docs/technotes/guides/language/varargs.html)) so we can easily insert the display data separated by comma. For example:

    myOTable.addRow(obj, obj1, obj2, objN, ...);
    

