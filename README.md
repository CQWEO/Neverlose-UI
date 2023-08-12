# Neverlose-UI

## Creating Window
This function creates a window which creates the main Frame
```lua
local Win = Neverlose_Main:Window({
    Title = "NEVERLOSE",
    CFG = "Neverlose",
    Key = Enum.KeyCode.H,
    External = {
        KeySystem = true,
        Key = {
            "Test",
            "Beta"
        }
    }
})
```
## Creating Tab Sections
This is a Tab section it is being placed in the TabsHolder on the Left side of the Frame
and is being used to get a better look at what type of tabs there is!
```lua
local TabSection1 = Win:TSection("Misc")
```
## Creating a Tab
This is being placed in wich section you would like
```lua
local Autofarm = TabSection1:Tab("Autofarm")
```
## Creating Normal Sections
Here is how you create two normal sections wich holds Toggles, Sliders and Dropdowns
```lua
local FarmSection = Autofarm:Section("Autofarm")
local ConfigSection = Autofarm:Section("Config")
```
## Creating Toggle, Dropdown & Slider

```lua
local AutoFarmVar = FarmSection:Toggle("Auto Farm", function(t)
    ValueToggle = t
end)
AutoFarmVar:Set(true) -- can be true or false

local HelloVar = World:Slider("Hello", 1, 500, 50, function(t)
    ValueSlider = t
end)
HelloVar:Set(75) -- any number within the range 1 - 500 since it has been preseted

local SmallTable = {"Mana64", "Lmao", "HVH"}
local SelectConfigVar = Config:Dropdown("Select Config", SmallTable, function(t)
    ValueDropdown = t
    print(ValueDropdown)
end)
SelectConfigVar:Set("Mana64") -- any type of name that is existing in the table for example "Mana64"
```
