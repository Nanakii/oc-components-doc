# Component: ME Import Bus

Component name: `me_importbus`

Callbacks:

* `getImportConfiguration(side:number[, slot:number]):table`  
  Get the configuration of the import bus pointing in the specified direction.  
  **side** - [Sides] value  
  **slot** - [Slot](#slots) number  
  **Returns:** Item stack, see [Inventory Controller] for a list of properties
* `setImportConfiguration(side:number[, slot:number][, database:address, entry:number]):boolean`  
  Configure the import bus pointing in the specified direction to import item stacks matching the specified descriptor.  
  **side** - [Sides] value  
  **slot** - [Slot](#slots) number  
  **database** - [Database] address  
  **entry** - Entry number in the database

## Slots

The slots are numbered like this

    6 4 7
    2 1 3
    8 5 9

[Sides]: http://ocdoc.cil.li/api:sides
[Inventory Controller]: http://ocdoc.cil.li/component:inventory_controller
[Database]: http://ocdoc.cil.li/component:database
