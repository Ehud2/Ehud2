-- Start
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Yohav Hub", "Ocean")

-- Welcome
local Tab = Window:NewTab("Welcome")
local ScriptsSection = Tab:NewSection("Welcome To Yohav Hub!")
local ScriptsSection = Tab:NewSection("Freeilaygame is Copy Games!")
local ScriptsSection = Tab:NewSection("So Let's Destroy His Games!")
local ScriptsSection = Tab:NewSection("Have Enjoy!")

-- LocalOptions
local Tab = Window:NewTab("LocalOptions")
local ScriptsSection = Tab:NewSection("Map")

ScriptsSection:NewButton("Alaways Day", "Set Alaways Day", function()
    game.Lighting.ClockTime = 14
end)

ScriptsSection:NewButton("Alaways Night", "Set Alaways Night", function()
    game.Lighting.ClockTime = 1
end)

local ScriptsSection = Tab:NewSection("ForceField")

ScriptsSection:NewButton("FF All", "Set FF For All Players", function()
    -- This Script will work in script builder

for i, v in pairs(game.Players:GetPlayers()) do
	

    ff = Instance.new("ForceField", v.Character)
    
    
    end
end)

local ScriptsSection = Tab:NewSection("Speed/Jump")

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

-- Reset
local ScriptsSection = Tab:NewSection("Reset")

ScriptsSection:NewButton("Kill Me", "Kill Your Player", function()
    game.Players.LocalPlayer.Character.Humanoid.Health = 0
end)




    -- Spectator Players
local ScriptsSection = Tab:NewSection("Spectator Players")

ScriptsSection:NewButton("Spectator Players", "Spectator The Players", function()
       local runDummyScript = function(f,scri)
local oldenv = getfenv(f)
local newenv = setmetatable({}, {
__index = function(_, k)
if k:lower() == 'script' then
return scri
else
return oldenv[k]
end
end
})
setfenv(f, newenv)
ypcall(function() f() end)
end
cors = {}
mas = Instance.new("Model",game:GetService("Lighting")) 
mas.Name = "CompiledModel"
o1 = Instance.new("ScreenGui")
o2 = Instance.new("Frame")
o3 = Instance.new("TextButton")
o4 = Instance.new("TextButton")
o5 = Instance.new("TextLabel")
o6 = Instance.new("ImageButton")
o7 = Instance.new("LocalScript")
o1.Name = "SpectateGui"
o1.Parent = mas
o2.Name = "Bar"
o2.Parent = o1
o2.Position = UDim2.new(-1,-100,0.87999999523163,-50)
o2.Size = UDim2.new(0,200,0,50)
o2.Position = UDim2.new(-1,-100,0.87999999523163,-50)
o2.BackgroundColor3 = Color3.new(0, 0, 0)
o2.BackgroundTransparency = 0.20000000298023
o2.BorderSizePixel = 5
o3.Name = "Previous"
o3.Parent = o2
o3.Size = UDim2.new(0.25,0,1,0)
o3.Text = "<"
o3.BackgroundColor3 = Color3.new(0.52549, 0.52549, 0.52549)
o3.BorderColor3 = Color3.new(0.509804, 0.796079, 1)
o3.BorderSizePixel = 0
o3.Font = Enum.Font.SourceSans
o3.FontSize = Enum.FontSize.Size48
o3.TextColor3 = Color3.new(1, 1, 1)
o4.Name = "Next"
o4.Parent = o2
o4.Position = UDim2.new(1,0,0,0)
o4.Size = UDim2.new(-0.25,0,1,0)
o4.Text = ">"
o4.Position = UDim2.new(1,0,0,0)
o4.BackgroundColor3 = Color3.new(0.52549, 0.52549, 0.52549)
o4.BorderColor3 = Color3.new(0.509804, 0.796079, 1)
o4.BorderSizePixel = 0
o4.Font = Enum.Font.SourceSans
o4.FontSize = Enum.FontSize.Size48
o4.TextColor3 = Color3.new(1, 1, 1)
o5.Name = "Title"
o5.Parent = o2
o5.Position = UDim2.new(0.27500000596046,0,0,0)
o5.Size = UDim2.new(0.44999998807907,0,1,0)
o5.Text = ""
o5.Position = UDim2.new(0.27500000596046,0,0,0)
o5.BackgroundColor3 = Color3.new(1, 1, 1)
o5.BackgroundTransparency = 1
o5.Font = Enum.Font.SourceSans
o5.FontSize = Enum.FontSize.Size14
o5.TextColor3 = Color3.new(1, 1, 1)
o5.TextScaled = true
o5.TextWrapped = true
o6.Name = "Button"
o6.Parent = o1
o6.Position = UDim2.new(0,0,0.5,-25)
o6.Size = UDim2.new(0,50,0,50)
o6.Position = UDim2.new(0,0,0.5,-25)
o6.BackgroundColor3 = Color3.new(1, 1, 1)
o6.BackgroundTransparency = 0.30000001192093
o6.BorderSizePixel = 5
o6.Image = "http://www.roblox.com/asset/?id=176106970"
o7.Parent = o1
table.insert(cors,coroutine.create(function()
wait()
runDummyScript(function()

cam = game.Workspace.CurrentCamera

local bar = script.Parent.Bar
local title = bar.Title
local prev = bar.Previous
local nex = bar.Next
local button = script.Parent.Button

function get()
	for _,v in pairs(game.Players:GetPlayers())do
		if v.Name == title.Text then
			return(_)
		end
	end
end


local debounce = false
button.MouseButton1Click:connect(function()
	if debounce == false then debounce = true
		bar:TweenPosition(UDim2.new(.5,-100,0.88,-50),"In","Linear",1,true)
		pcall(function()
				title.Text = game.Players:GetPlayerFromCharacter(cam.CameraSubject.Parent).Name
		end)
	elseif debounce == true then debounce = false
		pcall(function() cam.CameraSubject = game.Players.LocalPlayer.Character.Humanoid end)
			bar:TweenPosition(UDim2.new(-1,-100,0.88,-50),"In","Linear",1,true)
		end
end)

prev.MouseButton1Click:connect(function()
	wait(.1)
	local players = game.Players:GetPlayers()
	local num = get()
	if not pcall(function() 
		cam.CameraSubject = players[num-1].Character.Humanoid
		end) then
		cam.CameraSubject = players[#players].Character.Humanoid
	end
pcall(function()
				title.Text = game.Players:GetPlayerFromCharacter(cam.CameraSubject.Parent).Name
		end)
end)

nex.MouseButton1Click:connect(function()
	wait(.1)
	local players = game.Players:GetPlayers()
	local num = get()
	if not pcall(function() 
		cam.CameraSubject = players[num+1].Character.Humanoid
		end) then
		cam.CameraSubject = players[1].Character.Humanoid
	end
pcall(function()
				title.Text = game.Players:GetPlayerFromCharacter(cam.CameraSubject.Parent).Name
		end)
end)


end,o7)
end))
mas.Parent = workspace
mas:MakeJoints()
local mas1 = mas:GetChildren()
for i=1,#mas1 do
	mas1[i].Parent = game:GetService("Players").LocalPlayer.PlayerGui 
	ypcall(function() mas1[i]:MakeJoints() end)
end
mas:Destroy()
for i=1,#cors do
coroutine.resume(cors[i])
end
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

-- Rejoin
local ScriptsSection = Tab:NewSection("Rejoin")

ScriptsSection:NewButton("Rejoin", "Rejoin Game", function()
    game:GetService("TeleportService"):Teleport(game.PlaceId, game:GetService("Players").LocalPlayer)
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

local player = game.Players.LocalPlayer
 
if player.Character then
 
if player.Character:FindFirstChild("Humanoid") then
 
player.Character.Humanoid.Name = "1"
 
end
 
local l = player.Character["1"]:Clone()
 
l.Parent = player.Character
 
l.Name = "Humanoid"; wait(0.1)
 
player.Character["1"]:Destroy()
 
workspace.CurrentCamera.CameraSubject = player.Character.Humanoid
 
player.Character.Animate.Disabled = true; wait(0.1)
 
player.Character.Animate.Disabled = false
 
end
 
print("finished.")
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

TeleportsSection:NewButton("Secretariat", "Teleport To The Secretariat", function()
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

local ScriptsSection = Tab:NewSection("Fling All")

ScriptsSection:NewButton("Fling All", "Fling All Players", function()
	loadstring(game:HttpGet('https://github.com/DigitalityScripts/roblox-scripts/raw/main/loop%20fling%20all'))()
end)

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
