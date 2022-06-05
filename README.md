-- Start
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("RobILGame Hub", "Ocean")

-- Welcome
local Tab = Window:NewTab("Welcome")

local Tab = Window:NewTab("Player")
local ScriptsSection = Tab:NewSection("Player")

--  Player Buttons
ScriptsSection:NewSlider("WalkSpeed", "More Speed", 500, 16, function(s)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)

ScriptsSection:NewSlider("JumpPower", "More Jump", 500, 50, function(s)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = s
end)

ScriptsSection:NewButton("Spam Chat", "Spam The Chat", function()
    while true do wait(1) 
 
local A_1   = "LOL" local A_2 = "All" 
local Event = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest Event:FireServer(A_1, A_2) end
end)

ScriptsSection:NewButton("Infinity Jump", "Give You Infinity Jump", function()
    -- Make sure to copy aLL of this!

-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local main = Instance.new("Frame")
local TextLabel = Instance.new("TextLabel")
local Frame = Instance.new("Frame")
local INFJUMP = Instance.new("TextButton")
local TextLabel_2 = Instance.new("TextLabel")

--Properties:

ScreenGui.Parent = game.CoreGui

main.Name = "main"
main.Parent = ScreenGui
main.Active = true
main.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
main.BorderSizePixel = 0
main.Position = UDim2.new(0.119258665, 0, 0, 0)
main.Size = UDim2.new(0, 146, 0, 28)
main.Active = true
main.Draggable = false

TextLabel.Parent = main
TextLabel.BackgroundColor3 = Color3.fromRGB(38, 38, 38)
TextLabel.BorderSizePixel = 0
TextLabel.Size = UDim2.new(0, 146, 0, 28)
TextLabel.Font = Enum.Font.SciFi
TextLabel.Text = "Misc"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 17.000
TextLabel.TextWrapped = true

Frame.Parent = main
Frame.BackgroundColor3 = Color3.fromRGB(86, 86, 86)
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0, 0, 1, 0)
Frame.Size = UDim2.new(0, 146, 0, 61)

INFJUMP.Name = "INFJUMP"
INFJUMP.Parent = main
INFJUMP.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
INFJUMP.BorderSizePixel = 0
INFJUMP.Position = UDim2.new(0.794520497, 0, 1.6785717, 0)
INFJUMP.Size = UDim2.new(0, 21, 0, 21)
INFJUMP.Font = Enum.Font.SourceSans
INFJUMP.Text = ""
INFJUMP.TextColor3 = Color3.fromRGB(0, 0, 0)
INFJUMP.TextSize = 14.000
INFJUMP.MouseButton1Down:connect(function()
local Player = game:GetService'Players'.LocalPlayer;
local UIS = game:GetService'UserInputService';
 
_G.JumpHeight = 50;
 
function Action(Object, Function) if Object ~= nil then Function(Object); end end
 
UIS.InputBegan:connect(function(UserInput)
    if UserInput.UserInputType == Enum.UserInputType.Keyboard and UserInput.KeyCode == Enum.KeyCode.Space then
        Action(Player.Character.Humanoid, function(self)
            if self:GetState() == Enum.HumanoidStateType.Jumping or self:GetState() == Enum.HumanoidStateType.Freefall then
                Action(self.Parent.HumanoidRootPart, function(self)
                    self.Velocity = Vector3.new(0, _G.JumpHeight, 0);
                end)
            end
        end)
    end
end)
end)

TextLabel_2.Parent = main
TextLabel_2.BackgroundColor3 = Color3.fromRGB(38, 38, 38)
TextLabel_2.BorderSizePixel = 0
TextLabel_2.Position = UDim2.new(0.0547945201, 0, 1.57142854, 0)
TextLabel_2.Size = UDim2.new(0, 94, 0, 28)
TextLabel_2.Font = Enum.Font.SciFi
TextLabel_2.Text = "Inf jump"
TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.TextSize = 17.000
TextLabel_2.TextWrapped = true

-- Scripts:

local function TKDWQ_fake_script() -- INFJUMP.LocalScript 
local script = Instance.new('LocalScript', INFJUMP)

function zigzag(X) return math.acos(math.cos(X*math.pi))/math.pi end

counter = 0

while wait(0.1)do
script.Parent.BackgroundColor3 = Color3.fromHSV(zigzag(counter),1,1)
 
counter = counter + 0.01
end
end
coroutine.wrap(TKDWQ_fake_script)()
end)

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

-- Refresh
ScriptsSection:NewButton("Refresh", "Refresh Player", function()
    table.clear(players)
for i,v in pairs(game:GetService("Players"):GetChildren()) do
    table.insert(players,v.Name)
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

TeleportsSection:NewButton("Microphone", "Teleport To The Microphone", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(170.51446533203125, -16.974998474121094, 167.9423828125)
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
local ScriptsSection = Tab:NewSection("Admin Script")


ScriptsSection:NewButton("Infinite Yield", "Give You Infinite Yield Admim", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
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

-- Stats
local Tab            = Window:NewTab("Stats")
local ScriptsSection = Tab:NewSection("Hub: RobILGame")
local ScriptsSection = Tab:NewSection("Version: 1.0.0")
local ScriptsSection = Tab:NewSection("Developers: RobILGame Community")
local ScirptsSection = Tab:NewSection("Attach Game: בוא ללמוד עדכון ענק")
local ScirptsSection = Tab:NewSection("Exploit Use: Any")
