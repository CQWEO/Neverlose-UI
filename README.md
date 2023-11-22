local Neverlose_Main = loadstring(game:HttpGet"https://github.com/Mana42138/Neverlose-UI/blob/main/Source.lua")()

local Neverlose_Main = loadstring(game:HttpGet"https://github.com/Mana42138/Neverlose-UI/blob/main/Source.lua")()
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
local TabSection1 = Win:TSection("Misc")
local Autofarm = TabSection1:Tab("Autofarm")

local FarmSection = Autofarm:Section("Autofarm")
local ConfigSection = Autofarm:Section("Config")

local AutoFarmVar = FarmSection:Toggle("Auto Farm", function(t)
    ValueToggle = t
end)
AutoFarmVar:Set(true) -- can be true or false

local SmallTable = {"Mana64", "Lmao", "HVH"}
local SelectConfigVar = Config:Dropdown("Select Config", SmallTable, function(t)
    ValueDropdown = t
    print(ValueDropdown)
end)
SelectConfigVar:Set("Mana64") -- any type of name that exists in the table, e.g., "Mana64"
SelectConfigVar:Refresh({"New Mana64", "Legit"} -- Refresh the dropdown with new table values

local HelloVar = World:Slider("Hello", 1, 500, 50, function(t)
    ValueSlider = t
end)
HelloVar:Set(75) -- any number within the range 1 - 500 since it has been preset

World:Button("Press Me", function()
    Neverlose_Main:Notify({
    Title = "Neverlose",
    Text = "Yay you pressed me :DD",
    Time = 2 -- in seconds
    })
end)

World:TextBox("Password here!", function(t)
    if t == "Mana" then
    Neverlose_Main:Notify({
        Title = "Welcome",
        Text = "Welcome | ".. game.Players.LocalPlayer.Name,
        Time = 2
    })
    else
        game.Players.LocalPlayer:Kick("Wrong key NOOB")
    end
end)

Config:Colorpicker("Background", Color3.fromRGB(0,20,38), function(t)
    print(t)
end)

Config:Bind("On-Shot", function(t)
    print("Lol", tostring(t))
end, {
    { -- This is each keybind you want to setup when the user executes your script!
        key = Enum.KeyCode.P, -- Set the start key (the user can change this)
        Toggled = false -- set true if you want it to be toggled (the user can change this)
    },
    {
        key = Enum.KeyCode.R,
        Toggled = true
    }
})

local NoLove = getgenv().Lua

local FarmSection = NoLove:Section("Autofarm")
local ConfigSection = NoLove:Section("Config")

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
