local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Knife Clicker Simulator", "GrapeTheme")

local Tab = Window:NewTab("AutoFarm")
local Section = Tab:NewSection("Farm-Knives")

Section:NewToggle("Auto Knives", "Toggle-Auto", function(Value)
_G.Punch = Value
while _G.Punch do wait()
    game:GetService("ReplicatedStorage"):WaitForChild("Knives"):WaitForChild("Clicker"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Click"):InvokeServer()

    end
end)

Section:NewToggle("Auto BuyKnives", "Toggle-Auto", function(Value)
_G.Buy = Value
while _G.Buy do wait(0.1)
    game:GetService("ReplicatedStorage"):WaitForChild("Knives"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer()
game:GetService("ReplicatedStorage"):WaitForChild("Knives"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("SelectBest"):InvokeServer()

    end
end)

Section:NewToggle("Auto Rebirth", "Toggle-Auto", function(Value)
_G.Rebirth = Value
while _G.Rebirth do wait(0.1)
   game:GetService("ReplicatedStorage"):WaitForChild("Rebirths"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Rebirth"):InvokeServer()

    end
end)

Section:NewToggle("Auto BuyDoor [World 1]", "Toggle-Auto", function(Value)
_G.World1 = Value
while _G.World1 do wait()
    local args = {
    [1] = "1"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "2"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "3"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "4"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "5"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "6"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "7"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "8"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "9"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "10"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
    end
end)

Section:NewToggle("Auto BuyDoor [World 2]", "Toggle-Auto", function(Value)
_G.World2 = Value
while _G.World2 do wait()
local args = {
    [1] = "11"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "12"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "13"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "14"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "15"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))
local args = {
    [1] = "16"
}

game:GetService("ReplicatedStorage"):WaitForChild("Areas"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))

    end
end)

Section:NewToggle("Auto Mega-Rebirth", "Toggle-Auto", function(Value)
_G.Mega = Value
while _G.Mega do wait()
    game:GetService("ReplicatedStorage"):WaitForChild("MegaRebirths"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Rebirth"):InvokeServer()

    end
end)

local Tab = Window:NewTab("BuyEgg")
local Section = Tab:NewSection("Select Boxes!")
Eggs = {}
for i,v in pairs(game:GetService("Workspace").Boxes:GetChildren()) do
    table.insert(Eggs,v.Name) 
end
local drop = Section:NewDropdown("Select Boxes", "Click To Select", Eggs, function(t)
   PlayerTP = t
end)

Section:NewToggle("Auto Buy", "Toggle-Egg", function(t)
_G.Boxes = t
while _G.Boxes do wait()
    local args = {
    [1] = PlayerTP
}

game:GetService("ReplicatedStorage"):WaitForChild("Boxes"):WaitForChild("Core"):WaitForChild("Default"):WaitForChild("Remotes"):WaitForChild("Buy"):InvokeServer(unpack(args))

end
end)

local Tab = Window:NewTab("Player")
local Section = Tab:NewSection("Select Player!")

Plr = {}
for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(Plr,v.Name) 
end

local drop = Section:NewDropdown("Select Player!", "Click To Select", Plr, function(t)
   PlayerTP = t
end)
Section:NewButton("TP", "", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[PlayerTP].Character.HumanoidRootPart.CFrame
end)

Section:NewButton("Refresh [PlayerServer]","Refresh Dropdown", function()
  drop:Refresh(Plr)
end)

local Tab = Window:NewTab("Ui")
local Section = Tab:NewSection("Ui-ON/OFF")

Section:NewKeybind("On/Off-Ui", "KeybindInfo-Ui", Enum.KeyCode.F, function()
	Library:ToggleUI()
end)

repeat wait() until game:IsLoaded()
game:GetService("Players").LocalPlayer.Idled:connect(function()
game:GetService("VirtualUser"):ClickButton2(Vector2.new())
end)
