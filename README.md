-- Start
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Yohav Hub", "Ocean")

-- Welcome
local Tab = Window:NewTab("Welcome")
local ScriptsSection = Tab:NewSection("Welcome To Yohav Hub!")
local ScriptsSection = Tab:NewSection("Freeilaygame is Copy Games!")
local ScriptsSection = Tab:NewSection("So Let's Destroy His Games!")
local ScriptsSection = Tab:NewSection("Have Enjoy!")


local Tab = Window:NewTab("Player")
local ScriptsSection = Tab:NewSection("Speed/Jump")

--  Player Buttons
ScriptsSection:NewSlider("WalkSpeed", "More Speed", 500, 16, function(s)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)

ScriptsSection:NewSlider("JumpPower", "More Jump", 500, 50, function(s)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = s
end)

local ScriptsSection = Tab:NewSection("Chat")

ScriptsSection:NewButton("Spam Chat", "Spam The Chat", function()
    while true do wait(1) 
 
local A_1   = "LOL" local A_2 = "All" 
local Event = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest Event:FireServer(A_1, A_2) end
end)

local ScriptsSection = Tab:NewSection("Infinity Jump")

ScriptsSection:NewButton("Infinity Jump", "Give You Infinity Jump", function()
   
local infjmp = true
game:GetService("UserInputService").jumpRequest:Connect(function()
    if infjmp then
        game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass"Humanoid":ChangeState("Jumping")
    end
end)
end)

local ScriptsSection = Tab:NewSection("Fly/Noclip")

-- Toggles
ScriptsSection:NewToggle("E To Fly", "Press E To Fly", function(state)
    if state then
        repeat wait() 
    until game.Players.LocalPlayer and game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:findFirstChild("Torso") and game.Players.LocalPlayer.Character:findFirstChild("Humanoid") 
local mouse = game.Players.LocalPlayer:GetMouse() 
repeat wait() until mouse
local plr = game.Players.LocalPlayer 
local torso = plr.Character.Torso 
local flying = false
local deb = true 
local ctrl = {f = 0, b = 0, l = 0, r = 0} 
local lastctrl = {f = 0, b = 0, l = 0, r = 0} 
local maxspeed = 50 
local speed = 0 

function Fly() 
local bg = Instance.new("BodyGyro", torso) 
bg.P = 9e4 
bg.maxTorque = Vector3.new(9e9, 9e9, 9e9) 
bg.cframe = torso.CFrame 
local bv = Instance.new("BodyVelocity", torso) 
bv.velocity = Vector3.new(0,0.1,0) 
bv.maxForce = Vector3.new(9e9, 9e9, 9e9) 
repeat wait() 
plr.Character.Humanoid.PlatformStand = true 
if ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0 then 
speed = speed+.5+(speed/maxspeed) 
if speed > maxspeed then 
speed = maxspeed 
end 
elseif not (ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0) and speed ~= 0 then 
speed = speed-1 
if speed < 0 then 
speed = 0 
end 
end 
if (ctrl.l + ctrl.r) ~= 0 or (ctrl.f + ctrl.b) ~= 0 then 
bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (ctrl.f+ctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(ctrl.l+ctrl.r,(ctrl.f+ctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed 
lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r} 
elseif (ctrl.l + ctrl.r) == 0 and (ctrl.f + ctrl.b) == 0 and speed ~= 0 then 
bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (lastctrl.f+lastctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(lastctrl.l+lastctrl.r,(lastctrl.f+lastctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed 
else 
bv.velocity = Vector3.new(0,0.1,0) 
end 
bg.cframe = game.Workspace.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*speed/maxspeed),0,0) 
until not flying 
ctrl = {f = 0, b = 0, l = 0, r = 0} 
lastctrl = {f = 0, b = 0, l = 0, r = 0} 
speed = 0 
bg:Destroy() 
bv:Destroy() 
plr.Character.Humanoid.PlatformStand = false 
end 
mouse.KeyDown:connect(function(key) 
if key:lower() == "e" then 
if flying then flying = false 
else 
flying = true 
Fly() 
end 
elseif key:lower() == "w" then 
ctrl.f = 1 
elseif key:lower() == "s" then 
ctrl.b = -1 
elseif key:lower() == "a" then 
ctrl.l = -1 
elseif key:lower() == "d" then 
ctrl.r = 1 
end 
end) 
mouse.KeyUp:connect(function(key) 
if key:lower() == "w" then 
ctrl.f = 0 
elseif key:lower() == "s" then 
ctrl.b = 0 
elseif key:lower() == "a" then 
ctrl.l = 0 
elseif key:lower() == "d" then 
ctrl.r = 0 
end 
end)
Fly()
    else
        print("Toggle Off")
    end
end)

local ScriptsSection = Tab:NewSection("Character")

-- Refresh
ScriptsSection:NewButton("Refresh", "Refresh Player", function()
    table.clear(players)
for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(players,v.Name)
end
end)

-- Gode Mode
ScriptsSection:NewButton("Gode Mode", "Gode Mode Player", function()
    -- Godmode Jake11Price and JasonKaranikYoutube. Universalized by EthanMcBloxxer @ gist.github.com/EthanMcBloxxer/22676838e35bdab12a1c1d331e6f2ee7
-- Script saves your position, speed, and tools.

local PlayerName = (game.Players.LocalPlayer.Name)
local SavedTools = Instance.new('Folder',game:GetService('ReplicatedStorage'))
SavedTools.Name = 'SavedTools'
local TargetPlayer = 'LocalPlayer'
_G.Looop = true
while _G.Looop == true do
    wait(0.01)
    local saved = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
    local A_1 = "LocalPlayer"
    local SavedSpeed = game.Players.LocalPlayer.Character.Humanoid.WalkSpeed
    if game:GetService("Workspace")[PlayerName].Humanoid.Health == 0 then
        for i, v in pairs(game:GetService('Players').LocalPlayer.Backpack:GetChildren()) do
            if v then
                v.Parent = SavedTools
            end
        end
        for i,v in pairs(game:GetService('Players')[TargetPlayer].Character:GetChildren()) do
            if v:IsA('Tool') then
                v.Parent = SavedTools
            end
        end
        local Event = game:GetService("Workspace").Remote.loadchar
        Event:InvokeServer(A_1)
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = saved
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = SavedSpeed
        for i, v in pairs(SavedTools:GetChildren()) do
            if v then
                v.Parent = game:GetService('Players')[TargetPlayer].Backpack
            end
        end
        SavedTools:ClearAllChildren()
    end
end
end)

-- New Teleports Tab
local Tab = Window:NewTab("Teleports")
local TeleportsSection = Tab:NewSection("Teleports")

--Teleports Parts
TeleportsSection:NewButton("Owner Room", "Teleport To The Owner Room", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(137.461914, -15.4626942, 179.545563, 0.0353118256, -1.30889588e-09, 0.999376357, 7.54262737e-06, 1, -2.65200413e-07, -0.999376357, 7.54728808e-06, 0.0353118256)
end)

TeleportsSection:NewButton("Guard Room", "Teleport To The  Guard Room", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(176.817535, -30.4848118, 264.669189, 0, 0, 1, 0, 1, -0, -1, 0, 0)
end)

TeleportsSection:NewButton("Microphone", "Teleport To The Secretariat", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(170.51446533203125, -16.974998474121094, 167.9423828125)
end)

TeleportsSection:NewButton("Microphone", "Teleport To The Microphone", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-3505.71, 20.23, 273.51)
end)

-- Teleport Tool
local TeleportsSection = Tab:NewSection("Teleport Tool")
TeleportsSection:NewButton("Teleport Tool", "Teleport Tool", function()
    local LocalPlayer = game.Players.LocalPlayer
local rp = LocalPlayer.Character.HumanoidRootPart
local tool = Instance.new("Tool",LocalPlayer.Backpack)
local mouse = LocalPlayer:GetMouse()
tool.Name = "click tp"
tool.RequiresHandle = false
tool.Activated:Connect(function()
    rp.CFrame = CFrame.new(mouse.Hit.X,mouse.Hit.Y + 4,mouse.Hit.Z)
end)
end)

local Section = Tab:NewSection("Select Player")
players = {}

for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(players,v.Name)
end

Section:NewDropdown("Select Player", "Click To Name", players, function(abc)
    Select = abc
end)

Section:NewButton("Teleport", " ", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[Select].Character.HumanoidRootPart.CFrame
end)

-- Others Players
local Tab = Window:NewTab("OtherPlayers")

-- Admin
local Tab            = Window:NewTab("Admin")
local ScriptsSection = Tab:NewSection("Infinite Yield")


ScriptsSection:NewButton("Infinite Yield", "Give You Infinite Yield Admim", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
end)


local ScriptsSection = Tab:NewSection("CMD-X")
ScriptsSection:NewButton("CMD-X", "Give You CMD-X Admim", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/CMD-X/CMD-X/master/Source",true))()
end)

local ScriptsSection = Tab:NewSection("Reviz Admin")

ScriptsSection:NewButton("Reviz Admin", "Give You Reviz Admin", function()
    loadstring(game:HttpGet(('https://pastebin.com/raw/pyzjWNhk'),true))()
end)

local ScriptsSection = Tab:NewSection("Fates Admin")

ScriptsSection:NewButton("Fates Admin", "Give You Fates Admin", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/fatesc/fates-admin/main/main.lua"))();
end)

-- ESP
local Tab            = Window:NewTab("ESP")
local ScriptsSection = Tab:NewSection("ESP Light")

ScriptsSection:NewButton("ESP Light", "Give You ESP Light", function()

local localPlayer=game.Players.LocalPlayer

function highlightModel(objObject)
    for i,v in pairs(objObject:children())do
        if v:IsA'BasePart'and v.Name~='HumanoidRootPart'then
            local bHA=Instance.new('BoxHandleAdornment',v)
            bHA.Adornee=v
            bHA.Size= v.Name=='Head' and Vector3.new(1.25,1.25,1.25) or v.Size
            bHA.Color3=v.Name=='Head'and Color3.new(1,0,0)or v.Name=='Torso'and Color3.new(0,1,0)or Color3.new(0,0,1)
            bHA.Transparency=.5
            bHA.ZIndex=1
            bHA.AlwaysOnTop=true
        end
        if #v:children()>0 then
            highlightModel(v)
        end
    end
end

function unHighlightModel(objObject)
    for i,v in pairs(objObject:children())do
        if v:IsA'BasePart' and v:findFirstChild'BoxHandleAdornment' then
            v.BoxHandleAdornment:Destroy()
        end
        if #v:children()>0 then
            unHighlightModel(v)
        end
    end
end

function sortTeamHighlights(objPlayer)
    repeat wait() until objPlayer.Character
    if objPlayer.TeamColor~=localPlayer.TeamColor then
        highlightModel(objPlayer.Character)
    else
        unHighlightModel(objPlayer.Character)
    end
    if objPlayer~=localPlayer then
        objPlayer.Changed:connect(function(strProp)
            if strProp=='TeamColor'then
                if objPlayer.TeamColor~=localPlayer.TeamColor then
                    unHighlightModel(objPlayer.Character)
                    highlightModel(objPlayer.Character)
                else
                    unHighlightModel(objPlayer.Character)
                end
            end
        end)
    else
        objPlayer.Changed:connect(function(strProp)
            if strProp=='TeamColor'then
                wait(.5)
                for i,v in pairs(game.Players:GetPlayers())do
                    unHighlightModel(v)
                    if v.TeamColor~=localPlayer.TeamColor then
                        highlightModel(v.Character)
                    end
                end
            end
        end)
    end
end

for i,v in pairs(game.Players:GetPlayers())do
    v.CharacterAdded:connect(function()
        sortTeamHighlights(v)
    end)
    sortTeamHighlights(v)
end
game.Players.PlayerAdded:connect(function(objPlayer)
    objPlayer.CharacterAdded:connect(function(objChar)
        sortTeamHighlights(objPlayer)
    end)
end)
end)

-- ESP NickName
local ScriptsSection = Tab:NewSection("ESP NickName")
ScriptsSection:NewButton("ESP NickName", "Give You ESP NickName", function()
    local function API_Check()
    if Drawing == nil then
        return "No"
    else
        return "Yes"
    end
end

local Find_Required = API_Check()

if Find_Required == "No" then
    game:GetService("StarterGui"):SetCore("SendNotification",{
        Title = "Exunys Developer";
        Text = "ESP script could not be loaded because your exploit is unsupported.";
        Duration = math.huge;
        Button1 = "OK"
    })

    return
end

local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local UserInputService = game:GetService("UserInputService")
local Camera = workspace.CurrentCamera

local Typing = false

_G.SendNotifications = true   -- If set to true then the script would notify you frequently on any changes applied and when loaded / errored. (If a game can detect this, it is recommended to set it to false)
_G.DefaultSettings = false   -- If set to true then the ESP script would run with default settings regardless of any changes you made.

_G.TeamCheck = false   -- If set to true then the script would create ESP only for the enemy team members.

_G.ESPVisible = true   -- If set to true then the ESP will be visible and vice versa.
_G.TextColor = Color3.fromRGB(255, 80, 10)   -- The color that the boxes would appear as.
_G.TextSize = 14   -- The size of the text.
_G.Center = true   -- If set to true then the script would be located at the center of the label.
_G.Outline = true   -- If set to true then the text would have an outline.
_G.OutlineColor = Color3.fromRGB(0, 0, 0)   -- The outline color of the text.
_G.TextTransparency = 0.7   -- The transparency of the text.
_G.TextFont = Drawing.Fonts.UI   -- The font of the text. (UI, System, Plex, Monospace) 

_G.DisableKey = Enum.KeyCode.Q   -- The key that disables / enables the ESP.

local function CreateESP()
    for _, v in next, Players:GetPlayers() do
        if v.Name ~= Players.LocalPlayer.Name then
            local ESP = Drawing.new("Text")

            RunService.RenderStepped:Connect(function()
                if workspace:FindFirstChild(v.Name) ~= nil and workspace[v.Name]:FindFirstChild("HumanoidRootPart") ~= nil then
                    local Vector, OnScreen = Camera:WorldToViewportPoint(workspace[v.Name]:WaitForChild("Head", math.huge).Position)

                    ESP.Size = _G.TextSize
                    ESP.Center = _G.Center
                    ESP.Outline = _G.Outline
                    ESP.OutlineColor = _G.OutlineColor
                    ESP.Color = _G.TextColor
                    ESP.Transparency = _G.TextTransparency
                    ESP.Font = _G.TextFont

                    if OnScreen == true then
                        local Part1 = workspace:WaitForChild(v.Name, math.huge):WaitForChild("HumanoidRootPart", math.huge).Position
                        local Part2 = workspace:WaitForChild(Players.LocalPlayer.Name, math.huge):WaitForChild("HumanoidRootPart", math.huge).Position or 0
                        local Dist = (Part1 - Part2).Magnitude
                        ESP.Position = Vector2.new(Vector.X, Vector.Y - 25)
                        ESP.Text = ("("..tostring(math.floor(tonumber(Dist)))..") "..v.Name.." ["..workspace[v.Name].Humanoid.Health.."]")
                        if _G.TeamCheck == true then 
                            if Players.LocalPlayer.Team ~= v.Team then
                                ESP.Visible = _G.ESPVisible
                            else
                                ESP.Visible = false
                            end
                        else
                            ESP.Visible = _G.ESPVisible
                        end
                    else
                        ESP.Visible = false
                    end
                else
                    ESP.Visible = false
                end
            end)

            Players.PlayerRemoving:Connect(function()
                ESP.Visible = false
            end)
        end
    end

    Players.PlayerAdded:Connect(function(Player)
        Player.CharacterAdded:Connect(function(v)
            if v.Name ~= Players.LocalPlayer.Name then 
                local ESP = Drawing.new("Text")
    
                RunService.RenderStepped:Connect(function()
                    if workspace:FindFirstChild(v.Name) ~= nil and workspace[v.Name]:FindFirstChild("HumanoidRootPart") ~= nil then
                        local Vector, OnScreen = Camera:WorldToViewportPoint(workspace[v.Name]:WaitForChild("Head", math.huge).Position)
    
                        ESP.Size = _G.TextSize
                        ESP.Center = _G.Center
                        ESP.Outline = _G.Outline
                        ESP.OutlineColor = _G.OutlineColor
                        ESP.Color = _G.TextColor
                        ESP.Transparency = _G.TextTransparency
    
                        if OnScreen == true then
                            local Part1 = workspace:WaitForChild(v.Name, math.huge):WaitForChild("HumanoidRootPart", math.huge).Position
                        local Part2 = workspace:WaitForChild(Players.LocalPlayer.Name, math.huge):WaitForChild("HumanoidRootPart", math.huge).Position or 0
                            local Dist = (Part1 - Part2).Magnitude
                            ESP.Position = Vector2.new(Vector.X, Vector.Y - 25)
                            ESP.Text = ("("..tostring(math.floor(tonumber(Dist)))..") "..v.Name.." ["..workspace[v.Name].Humanoid.Health.."]")
                            if _G.TeamCheck == true then 
                                if Players.LocalPlayer.Team ~= Player.Team then
                                    ESP.Visible = _G.ESPVisible
                                else
                                    ESP.Visible = false
                                end
                            else
                                ESP.Visible = _G.ESPVisible
                            end
                        else
                            ESP.Visible = false
                        end
                    else
                        ESP.Visible = false
                    end
                end)
    
                Players.PlayerRemoving:Connect(function()
                    ESP.Visible = false
                end)
            end
        end)
    end)
end

if _G.DefaultSettings == true then
    _G.TeamCheck = false
    _G.ESPVisible = true
    _G.TextColor = Color3.fromRGB(40, 90, 255)
    _G.TextSize = 14
    _G.Center = true
    _G.Outline = false
    _G.OutlineColor = Color3.fromRGB(0, 0, 0)
    _G.DisableKey = Enum.KeyCode.Q
    _G.TextTransparency = 0.75
end

UserInputService.TextBoxFocused:Connect(function()
    Typing = true
end)

UserInputService.TextBoxFocusReleased:Connect(function()
    Typing = false
end)

UserInputService.InputBegan:Connect(function(Input)
    if Input.KeyCode == _G.DisableKey and Typing == false then
        _G.ESPVisible = not _G.ESPVisible
        
        if _G.SendNotifications == true then
            game:GetService("StarterGui"):SetCore("SendNotification",{
                Title = "Exunys Developer";
                Text = "The ESP's visibility is now set to "..tostring(_G.ESPVisible)..".";
                Duration = 5;
            })
        end
    end
end)

local Success, Errored = pcall(function()
    CreateESP()
end)

if Success and not Errored then
    if _G.SendNotifications == true then
        game:GetService("StarterGui"):SetCore("SendNotification",{
            Title = "Exunys Developer";
            Text = "ESP script has successfully loaded.";
            Duration = 5;
        })
    end
elseif Errored and not Success then
    if _G.SendNotifications == true then
        game:GetService("StarterGui"):SetCore("SendNotification",{
            Title = "Exunys Developer";
            Text = "ESP script has errored while loading, please check the developer console! (F9)";
            Duration = 5;
        })
    end
    TestService:Message("The ESP script has errored, please notify Exunys with the following information :")
    warn(Errored)
    print("!! IF THE ERROR IS A FALSE POSITIVE (says that a player cannot be found) THEN DO NOT BOTHER !!")
end
end)

-- Stats
local Tab            = Window:NewTab("Stats")
local ScriptsSection = Tab:NewSection("Hub: Yohav")
local ScriptsSection = Tab:NewSection("Version: 1.0.0")
local ScriptsSection = Tab:NewSection("Developers: Yohav Community")
local ScirptsSection = Tab:NewSection("Attach Game: בוא ללמוד חזר")
local ScirptsSection = Tab:NewSection("Exploit Use: Any")

-- Tools
local Tab            = Window:NewTab("Tools")
local ScriptsSection = Tab:NewSection("Btools")

ScriptsSection:NewButton("Btools", "Give You Btools", function()
    a = Instance.new("HopperBin", game.Players.LocalPlayer.Backpack)
a.BinType = 2
b = Instance.new("HopperBin", game.Players.LocalPlayer.Backpack)
b.BinType = 3
c = Instance.new("HopperBin", game.Players.LocalPlayer.Backpack)
c.BinType = 4
end)
