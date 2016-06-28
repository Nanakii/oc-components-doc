# Component: ME Controller

Component name: `me_controller`

Callbacks:

* `getAvgPowerInjection():number`  
  Get the average power injection into the network.
* `getAvgPowerUsage():number`  
  Get the average power usage of the network.
* `getCpus():table`  
  Get a list of tables representing the available CPUs in the network.  
  **Returns:** Table of CPUs with the following properties:
  * **busy**:boolean
  * **coprocessors**:number
  * **name**:string
  * **storage**:number
* `getCraftables([filter:table]):table`  
  Get a list of known item recipes. These can be used to issue crafting requests.  
  **filter** - Table with key, value pairs that matches the item stack you want to search for.  
  **Returns:** Table of craftables, see [Craftable](#craftable). 
* `getEnergyStored():number`  
  Returns the total amount of stored energy.
* `getEssentiaInNetwork():table`  
  Get a list of the stored essentia in the network.
* `getFluidsInNetwork():table`  
  Get a list of the stored fluids in the network.
* `getGasesInNetwork():table`  
  Get a list of the stored gases in the network.
* `getIdlePowerUsage():number`  
  Get the idle power usage of the network.
* `getItemsInNetwork([filter:table]):table`  
  Get a list of the stored items in the network.  
  **filter** - Table with key, value pairs that matches the item stack you want to search for.  
  **Returns:** Table of item stacks, see [Inventory Controller] for a list of properties
* `getMaxEnergyStored():number`  
  Returns the maximum amount of stored energy.
* `getMaxStoredPower():number`  
  Get the maximum stored power in the network.
* `getStoredPower():number`  
  Get the stored power in the network. 
* `isEnergyProvider():number`  
  Returns whether this component can provide energy.
* `isEnergyReceiver():number`  
  Returns whether this component can receive energy.
* `store(filter:table, dbAddress:string[, startSlot:number[, count:number]]): Boolean`  
  Store items in the network matching the specified filter in the database with the specified address.
  See [Database] for more information on databases.

## Craftable

Callbacks:

* `getItemStack():table`  
  Returns the item stack representation of the crafting result.
* `request([amount:int[, prioritizePower:boolean[, cpuName:string]]]):userdata`  
  Requests the item to be crafted, returning an object that allows tracking the crafting status.

[Inventory Controller]: http://ocdoc.cil.li/component:inventory_controller
[Database]: http://ocdoc.cil.li/component:database
