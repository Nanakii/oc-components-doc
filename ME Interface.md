# Component: ME Interface

Component name: `me_interface`

## Block Interface

Callbacks:

* `getInterfaceConfiguration([slot:number]):table`
  Get the configuration of the interface.  
  **slot** - Slot number. Slots are numbered 1-9 from left to right.  
  **Returns:** Item stack, see [Inventory Controller] for a list of properties
* `setInterfaceConfiguration([slot:number][, database:address, entry:number[, size:number]]):boolean`  
  Configure the interface.
  **slot** - Slot number.  
  **database** - [Database] address  
  **entry** - Entry number in the database
  **size** - Stack size

## Multipart Interface

* `getInterfaceConfiguration(side:number[, slot:number]):table`  
  Get the configuration of the interface pointing in the specified direction.
  **side** - [Sides] value  
  **slot** - Slot number. Slots are numbered 1-9 from left to right.  
  **Returns:** Item stack, see [Inventory Controller] for a list of properties
* `setInterfaceConfiguration(side:number[, slot:number][, database:address, entry:number[, size:number]]):boolean`  
  Configure the interface pointing in the specified direction.
  **side** - [Sides] value  
  **slot** - Slot number.  
  **database** - [Database] address  
  **entry** - Entry number in the database
  **size** - Stack size

[Sides]: http://ocdoc.cil.li/api:sides
[Inventory Controller]: http://ocdoc.cil.li/component:inventory_controller
[Database]: http://ocdoc.cil.li/component:database
