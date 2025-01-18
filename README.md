# Building Module V3

Its been a while since i've touched roblox studio, its good to be back.
	
This new Version includes...
tons of new performance improvements, algorithms and methods.
	
the new version, and all the code inside is written by myself without any kind of addition from other developers,
thus the code might be not perfect, but its way better compared to the version before :)
	
### *Please don't use without giving credit to [@MrFearTick]*

Thank you.

#

### Table of Contents

1. [Creating a new Building Object](#creating-a-new-building-object)
2. [Setting up the Structures](#setting-up-the-structures)

#

### Creating a new Building Object:

Basically, you need a *Building Object* that contains all the information (such as the size of the grid, or the Plot BasePart),  
to create a Building Object, use the ```.new(base : BasePart, gridSize : number)``` method

**Example:**

```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local BuildingModule = require(ReplicatedStorage.Modules.BuildingModuleMain)

local buildingObject = BuildingModule.new(game.Workspace.Plots.MrFearTick_PLOT, 5)
```

> [!IMPORTANT]
> Keep in mind that the default *gridSize* is **5**, so when the *gridSize* is not given, it will use **5** as the Grid Size.

#

### Setting up the Structures:

You got to set up a *DataTable* where you can access the Structures (Which are Models that you can place) to properly use this Module.
	
First, Enter the *"Structures"* Module. You should see the *"Models"* dictionary:

```lua
Structures.Models = {

}
```

Right now, there is no Structure added so our Dictionary is empty,
here is how to add structures:

1. Create a new **Models** folder.
2. Add *Structure Models* that you want to use in the Module to the folder. (The Model doesn't require any configurations, the algorithms already handles the rest)
3. Finally, add the Structure Name inside the Dictionary. Assign a **Model** value that references the added Model.
4. If you want, you can assign even more values to use for your own **SanityChecks** or other configurations you might need.

**Example:**

```lua
Structures.Models = {

	-- As said above, the "Type" and "Price" are custom Values added to show in the example,
	-- The ONLY required value is "Model".
	
	["Wall Block"] = {
		["Model"] = modelsFolder.Block1x1,
		["Type"] = "Wall",
		["Price"] = 100
	},
	
	["Roof Tile"] = {
		["Model"] = modelsFolder.Block1x2,
		["Type"] = "Roof",
		["Price"] = 200
	},
	
	["Cool Decoration"] = {
		["Model"] = modelsFolder["Block1.1x2.4"],
		["Type"] = "Decoration",
		["Price"] = 50
	}

}
```

Simple as that, you can now proceed and use these Structures on **Edit Mode**.

#

### Editing on your Plot:

This is where you actually start moving and placing *Structures*.
	
To start **Editing** a *Structure*, you must use the  ```:Edit(modelName : string)``` method.
