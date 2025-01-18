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

#

### Creating a new Building Object:

Basically, you need a *Building Object* that contains all the information (such as the size of the grid, or the Plot BasePart),
to create a Building Object, use the **.new(base : BasePart, gridSize : number)** 

Example:

```lua
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local BuildingModule = require(ReplicatedStorage.Modules.BuildingModuleMain)

local buildingObject = BuildingModule.new(game.Workspace.Plots.MrFearTick_PLOT, 5)
```

> [!IMPORTANT]
> Keep in mind that the default *gridSize* is **5**, so when the *gridSize* is not given, it will use **5** as the Grid Size.
