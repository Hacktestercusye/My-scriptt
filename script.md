# My-scriptt
--GUI
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Scripthub", "BloodTheme")

--MAIN
local Main = Window:NewTab("Main")
local MainSection = Main:NewSection("Main")


MainSection:NewButton("Noclip", "Press Q to work", function()
    loadstring(game:HttpGet('https://pastebin.com/YsvkQycq'))()
end)

--LOCAL PLAYER
local Player = Window:NewTab("Player")
local PlayerSection = Player:NewSection("Player")


PlayerSection:NewSlider("Walkspeed", "GO FASTER!", 1000, 16, function(s)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)


PlayerSection:NewSlider("Jumppower", "JUMP HIGHER!", 150, 1, function(s)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = s
end)


PlayerSection:NewToggle("Super-Human", "go fast and jump high", function(state)
    if state then
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 120
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = 120
    else
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = 50
    end
end)


PlayerSection:NewButton("Reset WS/JP", "Resets to all defaults", function()
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = 50
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
end)


 --OTHER
 local Other = Window:NewTab("Other")
 local OtherSection = Other:NewSection("Other")

 OtherSection:NewButton("Chat Spoofer", "Lets you chat for other people", function()
     loadstring(game:HttpGet(('https://pastebin.com/raw/djBfk8Li'),true))()
 end)

 OtherSection:NewButton("Bypassed Fly", "bird mode", function()
     loadstring(game:HttpGet("https://raw.githubusercontent.com/Nicuse/RobloxScripts/main/BypassedFly.lua"))() 

     Fly(true)
 end)


 OtherSection:NewButton("Infinite Yeild", "Fe Admins.", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end)

OtherSection:NewButton("Silent Aim", "Shoot at people without shooting them.", function()
    loadstring(game:HttpGet('https://github.com/Averiias/Universal-SilentAim/blob/main/main.lua'))()
end)



OtherSection:NewButton("Owlhub", "Arsenal hack", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/CriShoux/OwlHub/master/OwlHub.txt"))();
end)





--COSTUMIZABLE UI
local Customizable UI = Window:NewTab("Customizable Ui")
local OtherSection = Customizable UI:NewSection("CustomizableUi")


for theme, color in pairs(themes) do
    Section:NewColorPicker(theme, "Change your "..theme, color, function(color3)
        Library:ChangeColor(theme, color3)
    end)
end

