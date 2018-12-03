# OTable
The OTable is an extended class of JTable embedded with an ArrayList of Objects used to display and edit regular two-dimensional tables of cells.
It uses a javax.swing.DefaultTableModel.

It allows to insert, remove, update and retrieve row data. Also, which data to display in the table.

## Adding a row

In order to adding a new row to the `OTable`:

    myOTable.addRow(obj, displayData);
    
Where `obj` is the object to be added to the ArrayList of Objects (so we can keep the reference of this object) and where `displayData` is an array of Objects.

By adding the new row it will be added to the end of the `OTable`.

You can insert the new row by using an `Object[]` variable. For example:

    // Example 1: Using initialized array
    Object[] displayData = new Object[2];
    displayData[0] = "My data 1";
    displayData[1] = "My data 2";
    myOTable.addRow(obj, displayData); 
    
    // Example 2: One-line initialization
    Object[] displayData = new Object[]{ "My data 1", "My data 2", ...... };
    myOTable.addRow(obj, displayData);
    
    // Example 3: Using Anonymous array
    myOTable.addRow(obj, new Object[]{ "My data 1", "My data2), ...... });

To keep it simple, `addRow` method uses `displayData` as a Variable Argument ([Learn more about Varargs](https://docs.oracle.com/javase/8/docs/technotes/guides/language/varargs.html)) so we can easily insert the display data separated by comma. For example:

    myOTable.addRow(obj, obj1, obj2, objN, ...);
    
## Inserting a row

In order to inserting a new row to the `OTable`:
    
    myOTable.insertRow(index, obj, displayData);
    
Where `index` is the position of the row we want to insert, `obj` is the object we want to keep reference and `displayData` is the data to be display in the `OTable`.

By inserting the new row it will be added to the index/position specificied.
    
## Removing a row

In order to remove a row: 

    int index = myOTable.getSelectedIndex();
    myOTable.removeRow(index);
    
Where `index` is the position of the row we want to remove. In the example above we removed the selected index in the `OTable`.

## Updating a row

In order to update a row: 

    myOTable.updateRow(index, obj, displayData);
    
Where `index` is the position we want to update, `obj` is the new object we want to keep reference and `displayData` is the new data to be display in the `OTable`.

## Retrieving a row

In order to retrieve/get a row:

    int index = myOTable.getSelectedIndex();
    myOTable.getRow(index);

Where `index` is the position we want to retrieve. In the example above we retrieve the selected index object in the `OTable`.

## Removing/clearing all rows

In order to remove all rows in the `OTable`:

    myOTable.clear();
