if game:GetService("CoreGui"):FindFirstChild("simbahub - Free Fire | "..os.date("%d ")..os.date("%A ")..os.date("%B ")..os.date("%Y")) then
    game:GetService("CoreGui")["Simbahub - Free Fire | "..os.date("%d ")..os.date("%A ")..os.date("%B ")..os.date("%Y")]:Destroy()
end
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/SINBAHUB1/sdasda/main/README.md"))()
local HoverPage = library:CreateWindow("Simbahub - Free Fire | "..os.date("%d ")..os.date("%A ")..os.date("%B ")..os.date("%Y"),Enum.KeyCode.RightControl)

local MainPage = HoverPage:CreateTab("Main")
local Main = MainPage:CreateSector("Main","Left")
local Players = MainPage:CreateSector("Players","Right")
local Pvpmode = MainPage:CreateSector("Pvpmode","Left")
local Visuals = MainPage:CreateSector("Visuals","Right")

Main:AddButton("FPSBOOST",function()
    local decalsyeeted = true -- Leaving this on makes games look shitty but the fps goes up by at least 20.
local g = game
local w = g.Workspace
local l = g.Lighting
local t = w.Terrain
sethiddenproperty(l,"Technology",2)
sethiddenproperty(t,"Decoration",false)
t.WaterWaveSize = 0
t.WaterWaveSpeed = 0
t.WaterReflectance = 0
t.WaterTransparency = 0
l.GlobalShadows = false
l.FogEnd = 9e9
l.Brightness = 0
settings().Rendering.QualityLevel = "Level01"
for i, v in pairs(g:GetDescendants()) do
    if v:IsA("Part") or v:IsA("Union") or v:IsA("CornerWedgePart") or v:IsA("TrussPart") then
        v.Material = "Plastic"
        v.Reflectance = 0
    elseif v:IsA("Decal") or v:IsA("Texture") and decalsyeeted then
        v.Transparency = 1
    elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
        v.Lifetime = NumberRange.new(0)
    elseif v:IsA("Explosion") then
        v.BlastPressure = 1
        v.BlastRadius = 1
    elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
        v.Enabled = false
    elseif v:IsA("MeshPart") then
        v.Material = "Plastic"
        v.Reflectance = 0
        v.TextureID = 10385902758728957
    end
end
for i, e in pairs(l:GetChildren()) do
    if e:IsA("BlurEffect") or e:IsA("SunRaysEffect") or e:IsA("ColorCorrectionEffect") or e:IsA("BloomEffect") or e:IsA("DepthOfFieldEffect") then
        e.Enabled = false
    end
end
end)

Main:AddButton("SUPER FPSBOOST",function()
     local decalsyeeted = true
    local g = game
    local w = g.Workspace
    local l = g.Lighting
    local t = w.Terrain
    t.WaterWaveSize = 0
    t.WaterWaveSpeed = 0
    t.WaterReflectance = 0
    t.WaterTransparency = 0
    l.GlobalShadows = false
    l.FogEnd = 9e9
    l.Brightness = 0
    settings().Rendering.QualityLevel = "Level01"
    for i, v in pairs(g:GetDescendants()) do
        if v:IsA("Part") or v:IsA("Union") or v:IsA("CornerWedgePart") or v:IsA("TrussPart") then 
            v.Material = "Plastic"
            v.Reflectance = 0
        elseif v:IsA("Decal") or v:IsA("Texture") and decalsyeeted then
            v.Transparency = 1
        elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
            v.Lifetime = NumberRange.new(0)
        elseif v:IsA("Explosion") then
            v.BlastPressure = 1
            v.BlastRadius = 1
        elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
            v.Enabled = false
        elseif v:IsA("MeshPart") then
            v.Material = "Plastic"
            v.Reflectance = 0
            v.TextureID = 10385902758728957
        end
    end
    for i, e in pairs(l:GetChildren()) do
        if e:IsA("BlurEffect") or e:IsA("SunRaysEffect") or e:IsA("ColorCorrectionEffect") or e:IsA("BloomEffect") or e:IsA("DepthOfFieldEffect") then
            e.Enabled = false
        end
    end
end)

Main:AddButton("Unfocused CPU + GPU",function()
    local UserInputService = game:GetService("UserInputService")
local RunService = game:GetService("RunService")

local WindowFocusReleasedFunction = function()
	RunService:Set3dRenderingEnabled(false)
	setfpscap(10)
	return
end

local WindowFocusedFunction = function()
	RunService:Set3dRenderingEnabled(true)
	setfpscap(360)
	return
end

local Initialize = function()
	UserInputService.WindowFocusReleased:Connect(WindowFocusReleasedFunction)
	UserInputService.WindowFocused:Connect(WindowFocusedFunction)
	return
end
Initialize()
end)

Main:AddButton("RTX MODE",function()
    getgenv().mode = "Autumn" -- Choose from Summer and Autumn
        settings().Rendering.QualityLevel = 10
        local a = game.Lighting
a.Ambient = Color3.fromRGB(33, 33, 33)
a.Brightness = 6.67
a.ColorShift_Bottom = Color3.fromRGB(0, 0, 0)
a.ColorShift_Top = Color3.fromRGB(255, 247, 237)
a.EnvironmentDiffuseScale = 0.105
a.EnvironmentSpecularScale = 0.522
a.GlobalShadows = true
a.OutdoorAmbient = Color3.fromRGB(51, 54, 67)
a.ShadowSoftness = 0.04
a.GeographicLatitude = -15.525
a.ExposureCompensation = 0.75
local b = Instance.new("BloomEffect", a)
b.Enabled = true
b.Intensity = 0.04
b.Size = 1900
b.Threshold = 0.915
local c = Instance.new("ColorCorrectionEffect", a)
c.Brightness = 0.176
c.Contrast = 0.39
c.Enabled = true
c.Saturation = 0.2
c.TintColor = Color3.fromRGB(217, 145, 57)
if getgenv().mode == "Summer" then
    c.TintColor = Color3.fromRGB(255, 220, 148)
elseif getgenv().mode == "Autumn" then
    c.TintColor = Color3.fromRGB(217, 145, 57)
else
    warn("No mode selected!")
    print("Please select a mode")
    b:Destroy()
    c:Destroy()
end
local d = Instance.new("DepthOfFieldEffect", a)
d.Enabled = true
d.FarIntensity = 0.077
d.FocusDistance = 21.54
d.InFocusRadius = 20.77
d.NearIntensity = 0.277
local e = Instance.new("ColorCorrectionEffect", a)
e.Brightness = 0
e.Contrast = -0.07
e.Saturation = 0
e.Enabled = true
e.TintColor = Color3.fromRGB(255, 247, 239)
local e2 = Instance.new("ColorCorrectionEffect", a)
e2.Brightness = 0.2
e2.Contrast = 0.45
e2.Saturation = -0.1
e2.Enabled = true
e2.TintColor = Color3.fromRGB(255, 255, 255)
local s = Instance.new("SunRaysEffect", a)
s.Enabled = true
s.Intensity = 0.01
s.Spread = 0.146
end)

Main:AddButton("RTX MODE CLOSE",function ()
    local light = game.Lighting
for i, v in pairs(light:GetChildren()) do
    v:Destroy()
end

local ter = workspace.Terrain
local color = Instance.new("ColorCorrectionEffect")
local bloom = Instance.new("BloomEffect")
local sun = Instance.new("SunRaysEffect")
local blur = Instance.new("BlurEffect")

color.Parent = light
bloom.Parent = light
sun.Parent = light
blur.Parent = light

-- enable or disable shit

local config = {

    Terrain = true;
    ColorCorrection = true;
    Sun = true;
    Lighting = true;
    BloomEffect = true;

}

-- settings {

color.Enabled = false
color.Contrast = 0.15
color.Brightness = 0.1
color.Saturation = 0.25
color.TintColor = Color3.fromRGB(255, 222, 211)

bloom.Enabled = false
bloom.Intensity = 0.1

sun.Enabled = false
sun.Intensity = 0.2
sun.Spread = 1

bloom.Enabled = false
bloom.Intensity = 0.05
bloom.Size = 32
bloom.Threshold = 1

blur.Enabled = false
blur.Size = 6

-- settings }


if config.ColorCorrection then
    color.Enabled = true
end


if config.Sun then
    sun.Enabled = true
end


if config.Terrain then
    -- settings {
    ter.WaterColor = Color3.fromRGB(10, 10, 24)
    ter.WaterWaveSize = 0.1
    ter.WaterWaveSpeed = 22
    ter.WaterTransparency = 0.9
    ter.WaterReflectance = 0.05
    -- settings }
end


if config.Lighting then
    -- settings {
    light.Ambient = Color3.fromRGB(0, 0, 0)
    light.Brightness = 4
    light.ColorShift_Bottom = Color3.fromRGB(0, 0, 0)
    light.ColorShift_Top = Color3.fromRGB(0, 0, 0)
    light.ExposureCompensation = 0
    light.FogColor = Color3.fromRGB(132, 132, 132)
    light.GlobalShadows = true
    light.OutdoorAmbient = Color3.fromRGB(112, 117, 128)
    light.Outlines = false
    -- settings }
end

end)

Main:AddButton("SERVERHOP",function()
    local PlaceID = game.PlaceId
        local AllIDs = {}
        local foundAnything = ""
        local actualHour = os.date("!*t").hour
        local Deleted = false
        function TPReturner()
            local Site;
            if foundAnything == "" then
                Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
            else
                Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
            end
            local ID = ""
            if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                foundAnything = Site.nextPageCursor
            end
            local num = 0;
            for i,v in pairs(Site.data) do
                local Possible = true
                ID = tostring(v.id)
                if tonumber(v.maxPlayers) > tonumber(v.playing) then
                    for _,Existing in pairs(AllIDs) do
                        if num ~= 0 then
                            if ID == tostring(Existing) then
                                Possible = false
                            end
                        else
                            if tonumber(actualHour) ~= tonumber(Existing) then
                                local delFile = pcall(function()
                                    -- delfile("NotSameServers.json")
                                    AllIDs = {}
                                    table.insert(AllIDs, actualHour)
                                end)
                            end
                        end
                        num = num + 1
                    end
                    if Possible == true then
                        table.insert(AllIDs, ID)
                        wait()
                        pcall(function()
                            -- writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                            wait()
                            game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                        end)
                        wait(4)
                    end
                end
            end
        end
        function Teleport() 
            while wait() do
                pcall(function()
                    TPReturner()
                    if foundAnything ~= "" then
                        TPReturner()
                    end
                end)
            end
        end
        Teleport()
end)

Pvpmode:AddToggle("Kill All",_G.KillAll,function(value)
    _G.KillAll = value
end)

Pvpmode:AddToggle("Safe Mode",_G.Safe_Mode,function(value)
    _G.Safe_Mode = value
end)

spawn(function()
    pcall(function()
        game:GetService("RunService").Heartbeat:Connect(function()
            if _G.Safe_Mode then
                if not game:GetService("Workspace"):FindFirstChild("YAYY") then
                    local YAY = Instance.new("Part")
                    YAY.Name = "YAYY"
                    YAY.Parent = game.Workspace
                    YAY.Anchored = true
                    YAY.Transparency = 0
                    YAY.Size = Vector3.new(5,0.5,5)
                    YAY.Material = "Neon"
                    while true do             
                        wait(0.1) 
                        game:GetService('TweenService'):Create(
                            YAY,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                        {Color = Color3.fromRGB(255, 0, 0)}):Play() 
                        wait(.5)            
                        game:GetService('TweenService'):Create(
                            YAY,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                        {Color = Color3.fromRGB(255, 155, 0)}):Play() 
                        wait(.5)            
                        game:GetService('TweenService'):Create(
                            YAY,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                        {Color = Color3.fromRGB(255, 255, 0)}):Play() 
                        wait(.5)            
                        game:GetService('TweenService'):Create(
                            YAY,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                        {Color = Color3.fromRGB(0, 255, 0)}):Play() 
                        wait(.5)            
                        game:GetService('TweenService'):Create(
                            YAY,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                        {Color = Color3.fromRGB(0, 255, 255)}):Play() 
                        wait(.5)            
                        game:GetService('TweenService'):Create(
                            YAY,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                        {Color = Color3.fromRGB(0, 155, 255)}):Play() 
                        wait(.5)            
                        game:GetService('TweenService'):Create(
                            YAY,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                        {Color = Color3.fromRGB(255, 0, 255)}):Play() 
                        wait(.5)            
                        game:GetService('TweenService'):Create(
                            YAY,TweenInfo.new(1,Enum.EasingStyle.Linear,Enum.EasingDirection.InOut),
                        {Color = Color3.fromRGB(255, 0, 155)}):Play() 
                        wait(.5)
                    end
                elseif game:GetService("Workspace"):FindFirstChild("YAYY") then
                    game.Workspace["YAYY"].CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Y - 3.92,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
                end
            else
                if game:GetService("Workspace"):FindFirstChild("YAYY") then
                    game:GetService("Workspace"):FindFirstChild("YAYY"):Destroy()
                end
            end
        end)
    end)
end)

spawn(function()
    pcall(function()
       game:GetService("RunService").Stepped:Connect(function()
            if _G.Safe_Mode then
                for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                    if v:IsA("BasePart") then
                        v.CanCollide = false    
                    end
                end
            end
        end)
    end)
end)

spawn(function()
    pcall(function()
        while wait() do
            if _G.Safe_Mode then
                local OldCFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
                repeat wait()
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-371.81918334961, 1881.5601806641, 581.22277832031)
                until _G.Safe_Mode == false
                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = OldCFrame
            end
        end
    end)
end)

function EquipWeapon(ToolSe)
    if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
        Tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
        wait(.1)
        game.Players.LocalPlayer.Character.Humanoid:EquipTool(Tool)
    end
end

spawn(function()
    game:GetService("RunService").RenderStepped:Connect(function()
        pcall(function()
            if _G.KillAll then
                for i, v in pairs(game:GetService("Players"):GetChildren()) do
                    if v.Name ~= game.Players.LocalPlayer.Name and not v.Character:FindFirstChildOfClass("ForceField") and v.Character.Humanoid.Health ~= 0 then
                        EquipWeapon("AK47")
                        local args = {
                            [1] = game:GetService("Players").LocalPlayer.Backpack.AWM,
                            [2] = {
                                ["p"] = nil,
                                ["pid"] = 1,
                                ["part"] = v.Character.Head,
                                ["d"] = 0.27019029855728,
                                ["maxDist"] = 0.027385782450438,
                                ["h"] = v.Character.Humanoid,
                                ["m"] = Enum.Material.Plastic,
                                ["sid"] = 250,
                                ["t"] = 0.0010933135312908,
                                ["n"] = nil
                            }
                        }
                        game:GetService("ReplicatedStorage").WeaponsSystem.Network.WeaponHit:FireServer(unpack(args))
                    end
                end
            end
        end)
    end)
end)

local Animate = game.Players.LocalPlayer.Character.Animate

Pvpmode:AddToggle("ZOMBIE",_G.Loop,function(value)
    
end)

Pvpmode:AddToggle("Aimbot Gun [AWM Only]",_G.Aimbot,function(value)
    _G.Aimbot = value
end)

spawn(function()
	while wait() do
		pcall(function()
			local MaxDistance = math.huge
            local Mouse = game.Players.LocalPlayer:GetMouse()
            for i,v in pairs(game:GetService("Players"):GetPlayers()) do
                if v.Name ~= game.Players.LocalPlayer.Name then
                    local Distance = (v.Character.HumanoidRootPart.Position - Mouse.Hit.p).Magnitude
                    if Distance < MaxDistance then
                        MaxDistance = Distance
                        PlayerSelectAimbot = v.Name
                    end
                end
            end
		end)
	end
end)

local lp = game:GetService('Players').LocalPlayer
local mouse = lp:GetMouse()
mouse.Button1Down:Connect(function()
    pcall(function()
        if _G.Aimbot and game.Players.LocalPlayer.Character:FindFirstChild("AWM") then
            local args = {
                [1] = game:GetService("Players").LocalPlayer.Character.AWM,
                [2] = {
                    ["p"] = nil,
                    ["pid"] = 1,
                    ["part"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Head,
                    ["d"] = 0.27019029855728,
                    ["maxDist"] = 0.027385782450438,
                    ["h"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Humanoid,
                    ["m"] = Enum.Material.Plastic,
                    ["sid"] = 250,
                    ["t"] = 0.0010933135312908,
                    ["n"] = nil
                }
            }
            game:GetService("ReplicatedStorage").WeaponsSystem.Network.WeaponHit:FireServer(unpack(args))
        end
    end)
end)

Pvpmode:AddToggle("Aimbot Gun [AK47 Only]",_G.Aimbot1,function(value)
    _G.Aimbot1 = value
end)

spawn(function()
	while wait() do
		pcall(function()
			local MaxDistance = math.huge
            local Mouse = game.Players.LocalPlayer:GetMouse()
            for i,v in pairs(game:GetService("Players"):GetPlayers()) do
                if v.Name ~= game.Players.LocalPlayer.Name then
                    local Distance = (v.Character.HumanoidRootPart.Position - Mouse.Hit.p).Magnitude
                    if Distance < MaxDistance then
                        MaxDistance = Distance
                        PlayerSelectAimbot = v.Name
                    end
                end
            end
		end)
	end
end)

local lp = game:GetService('Players').LocalPlayer
local mouse = lp:GetMouse()
mouse.Button1Down:Connect(function()
    pcall(function()
        if _G.Aimbot1 and game.Players.LocalPlayer.Character:FindFirstChild("AK47") then
            local args = {
                [1] = game:GetService("Players").LocalPlayer.Character.AK47,
                [2] = {
                    ["p"] = nil,
                    ["pid"] = 1,
                    ["part"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Head,
                    ["d"] = 0.27019029855728,
                    ["maxDist"] = 0.027385782450438,
                    ["h"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Humanoid,
                    ["m"] = Enum.Material.Plastic,
                    ["sid"] = 250,
                    ["t"] = 0.0010933135312908,
                    ["n"] = nil
                }
            }
            game:GetService("ReplicatedStorage").WeaponsSystem.Network.WeaponHit:FireServer(unpack(args))
        end
    end)
end)

Pvpmode:AddToggle("Aimbot Gun [MP40 Only]",_G.Aimbot2,function(value)
    _G.Aimbot2 = value
end)

spawn(function()
	while wait() do
		pcall(function()
			local MaxDistance = math.huge
            local Mouse = game.Players.LocalPlayer:GetMouse()
            for i,v in pairs(game:GetService("Players"):GetPlayers()) do
                if v.Name ~= game.Players.LocalPlayer.Name then
                    local Distance = (v.Character.HumanoidRootPart.Position - Mouse.Hit.p).Magnitude
                    if Distance < MaxDistance then
                        MaxDistance = Distance
                        PlayerSelectAimbot = v.Name
                    end
                end
            end
		end)
	end
end)


local lp = game:GetService('Players').LocalPlayer
local mouse = lp:GetMouse()
mouse.Button1Down:Connect(function()
    pcall(function()
        if _G.Aimbot2 and game.Players.LocalPlayer.Character:FindFirstChild("MP40") then
            local args = {
                [1] = game:GetService("Players").LocalPlayer.Character.MP40,
                [2] = {
                    ["p"] = nil,
                    ["pid"] = 1,
                    ["part"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Head,
                    ["d"] = 0.27019029855728,
                    ["maxDist"] = 0.027385782450438,
                    ["h"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Humanoid,
                    ["m"] = Enum.Material.Plastic,
                    ["sid"] = 250,
                    ["t"] = 0.0010933135312908,
                    ["n"] = nil
                }
            }
            game:GetService("ReplicatedStorage").WeaponsSystem.Network.WeaponHit:FireServer(unpack(args))
        end
    end)
end)

Pvpmode:AddToggle("Aimbot Gun [UMP Only]",_G.Aimbot4,function(value)
    _G.Aimbot4 = value
end)

spawn(function()
	while wait() do
		pcall(function()
			local MaxDistance = math.huge
            local Mouse = game.Players.LocalPlayer:GetMouse()
            for i,v in pairs(game:GetService("Players"):GetPlayers()) do
                if v.Name ~= game.Players.LocalPlayer.Name then
                    local Distance = (v.Character.HumanoidRootPart.Position - Mouse.Hit.p).Magnitude
                    if Distance < MaxDistance then
                        MaxDistance = Distance
                        PlayerSelectAimbot = v.Name
                    end
                end
            end
		end)
	end
end)


local lp = game:GetService('Players').LocalPlayer
local mouse = lp:GetMouse()
mouse.Button1Down:Connect(function()
    pcall(function()
        if _G.Aimbot4 and game.Players.LocalPlayer.Character:FindFirstChild("UMP") then
            local args = {
                [1] = game:GetService("Players").LocalPlayer.Character.UMP,
                [2] = {
                    ["p"] = nil,
                    ["pid"] = 1,
                    ["part"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Head,
                    ["d"] = 0.27019029855728,
                    ["maxDist"] = 0.027385782450438,
                    ["h"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Humanoid,
                    ["m"] = Enum.Material.Plastic,
                    ["sid"] = 250,
                    ["t"] = 0.0010933135312908,
                    ["n"] = nil
                }
            }
            game:GetService("ReplicatedStorage").WeaponsSystem.Network.WeaponHit:FireServer(unpack(args))
        end
    end)
end)

Pvpmode:AddToggle("Aimbot Gun [SCAR Only]",_G.Aimbot5,function(value)
    _G.Aimbot5 = value
end)

spawn(function()
	while wait() do
		pcall(function()
			local MaxDistance = math.huge
            local Mouse = game.Players.LocalPlayer:GetMouse()
            for i,v in pairs(game:GetService("Players"):GetPlayers()) do
                if v.Name ~= game.Players.LocalPlayer.Name then
                    local Distance = (v.Character.HumanoidRootPart.Position - Mouse.Hit.p).Magnitude
                    if Distance < MaxDistance then
                        MaxDistance = Distance
                        PlayerSelectAimbot = v.Name
                    end
                end
            end
		end)
	end
end)


local lp = game:GetService('Players').LocalPlayer
local mouse = lp:GetMouse()
mouse.Button1Down:Connect(function()
    pcall(function()
        if _G.Aimbot5 and game.Players.LocalPlayer.Character:FindFirstChild("SCAR") then
            local args = {
                [1] = game:GetService("Players").LocalPlayer.Character.SCAR,
                [2] = {
                    ["p"] = nil,
                    ["pid"] = 1,
                    ["part"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Head,
                    ["d"] = 0.27019029855728,
                    ["maxDist"] = 0.027385782450438,
                    ["h"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Humanoid,
                    ["m"] = Enum.Material.Plastic,
                    ["sid"] = 250,
                    ["t"] = 0.0010933135312908,
                    ["n"] = nil
                }
            }
            game:GetService("ReplicatedStorage").WeaponsSystem.Network.WeaponHit:FireServer(unpack(args))
        end
    end)
end)

Pvpmode:AddToggle("Aimbot Gun [M1014 Only]",_G.Aimbot6,function(value)
    _G.Aimbot6 = value
end)

spawn(function()
	while wait() do
		pcall(function()
			local MaxDistance = math.huge
            local Mouse = game.Players.LocalPlayer:GetMouse()
            for i,v in pairs(game:GetService("Players"):GetPlayers()) do
                if v.Name ~= game.Players.LocalPlayer.Name then
                    local Distance = (v.Character.HumanoidRootPart.Position - Mouse.Hit.p).Magnitude
                    if Distance < MaxDistance then
                        MaxDistance = Distance
                        PlayerSelectAimbot = v.Name
                    end
                end
            end
		end)
	end
end)


local lp = game:GetService('Players').LocalPlayer
local mouse = lp:GetMouse()
mouse.Button1Down:Connect(function()
    pcall(function()
        if _G.Aimbot6 and game.Players.LocalPlayer.Character:FindFirstChild("M1014") then
            local args = {
                [1] = game:GetService("Players").LocalPlayer.Character.M1014,
                [2] = {
                    ["p"] = nil,
                    ["pid"] = 1,
                    ["part"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Head,
                    ["d"] = 0.27019029855728,
                    ["maxDist"] = 0.027385782450438,
                    ["h"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Humanoid,
                    ["m"] = Enum.Material.Plastic,
                    ["sid"] = 250,
                    ["t"] = 0.0010933135312908,
                    ["n"] = nil
                }
            }
            game:GetService("ReplicatedStorage").WeaponsSystem.Network.WeaponHit:FireServer(unpack(args))
        end
    end)
end)

Pvpmode:AddToggle("Aimbot Gun [xM81 Only]",_G.Aimbot7,function(value)
    _G.Aimbot7 = value
end)

spawn(function()
	while wait() do
		pcall(function()
			local MaxDistance = math.huge
            local Mouse = game.Players.LocalPlayer:GetMouse()
            for i,v in pairs(game:GetService("Players"):GetPlayers()) do
                if v.Name ~= game.Players.LocalPlayer.Name then
                    local Distance = (v.Character.HumanoidRootPart.Position - Mouse.Hit.p).Magnitude
                    if Distance < MaxDistance then
                        MaxDistance = Distance
                        PlayerSelectAimbot = v.Name
                    end
                end
            end
		end)
	end
end)


local lp = game:GetService('Players').LocalPlayer
local mouse = lp:GetMouse()
mouse.Button1Down:Connect(function()
    pcall(function()
        if _G.Aimbot7 and game.Players.LocalPlayer.Character:FindFirstChild("XM81") then
            local args = {
                [1] = game:GetService("Players").LocalPlayer.Character.XM81,
                [2] = {
                    ["p"] = nil,
                    ["pid"] = 1,
                    ["part"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Head,
                    ["d"] = 0.27019029855728,
                    ["maxDist"] = 0.027385782450438,
                    ["h"] = game.Players:FindFirstChild(PlayerSelectAimbot).Character.Humanoid,
                    ["m"] = Enum.Material.Plastic,
                    ["sid"] = 250,
                    ["t"] = 0.0010933135312908,
                    ["n"] = nil
                }
            }
            game:GetService("ReplicatedStorage").WeaponsSystem.Network.WeaponHit:FireServer(unpack(args))
        end
    end)
end)

Pvpmode:AddLabel("Espplayer")

local ESP = loadstring(game:HttpGet("https://raw.githubusercontent.com/SINBAHUB1/ESPPLAYERz/main/README.md"))()

Pvpmode:AddToggle("Playeresp",false,function(State)
    ESP:Toggle(State)
end)

Pvpmode:AddToggle("Tracers Esp",false,function(State)
    ESP.Tracers = State
end)

Pvpmode:AddToggle("Name Esp",false,function(State)
    ESP.Names = State
end)

Pvpmode:AddToggle("Boxes Esp",false,function(State)
    ESP.Boxes = State
end)

Pvpmode:AddButton("Click Tp tools",function()
    local plr = game:GetService("Players").LocalPlayer
local mouse = plr:GetMouse()

local tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "Click Teleport"

tool.Activated:Connect(function()
local root = plr.Character.HumanoidRootPart
local pos = mouse.Hit.Position+Vector3.new(0,2.5,0)
local offset = pos-root.Position
root.CFrame = root.CFrame+offset
end)

tool.Parent = plr.Backpack
end)

Pvpmode:AddButton("Aimbot",function()
    loadstring(game:HttpGet"https://raw.githubusercontent.com/SINBAHUB1/sadad/main/README.md")()
end)

Pvpmode:AddSlider("Hitbox",0,2,100,1,function(Value)
    _G.HeadSize = Value
end)
Pvpmode:AddToggle("Hitbox",false,function(Values)
    _G.Hitbox = Values
game:GetService('RunService').RenderStepped:connect(function()
if _G.Hitbox then
for i,v in next, game:GetService('Players'):GetPlayers() do
if v.Name ~= game:GetService('Players').LocalPlayer.Name then
pcall(function()
v.Character.HumanoidRootPart.Size = Vector3.new(_G.HeadSize,_G.HeadSize,_G.HeadSize)
v.Character.HumanoidRootPart.Transparency = 0.7
v.Character.HumanoidRootPart.BrickColor = BrickColor.new("Really blue")
v.Character.HumanoidRootPart.Material = "Neon"
v.Character.HumanoidRootPart.CanCollide = false
end)
end
end
end
end)
end)

PlayerList = {}
for i,v in pairs(game.Players:GetChildren()) do  
    table.insert(PlayerList ,v.Name)
end

local Player = Players:AddDropdown("Selected Player",PlayerList,"...",false,function(value)
    _G.Selected_Player = value
end)

Players:AddButton("Refresh Player",function()
    for i,v in pairs(game.Players:GetChildren()) do
        Player:Remove(v.Name)
        wait(.1)
        Player:Add(v.Name)
    end
end)

Players:AddButton("Teleport",function(value)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players:FindFirstChild(_G.Selected_Player).Character.HumanoidRootPart.CFrame
end)

Players:AddSlider("WalkSpeed",0,16,100,1,function(yu)
    getgenv().WalkSpeedValue = (yu); --set your desired walkspeed here
local Player = game:service'Players'.LocalPlayer;
Player.Character.Humanoid:GetPropertyChangedSignal'WalkSpeed':Connect(function()
Player.Character.Humanoid.WalkSpeed = getgenv().WalkSpeedValue;
end)
end)
Players:AddSlider("Jumppower",0,30,100,1,function(jp)
    getgenv().JumpPowerValue = (jp); --set your desired walkspeed here
local Player = game:service'Players'.LocalPlayer;
Player.Character.Humanoid:GetPropertyChangedSignal'WalkSpeed':Connect(function()
Player.Character.Humanoid.JumpPower = getgenv().JumpPowerValue;
end)
end)

Visuals:AddButton("Maxzoom",function()
    game:GetService("Players").LocalPlayer.CameraMaxZoomDistance = math.huge
end)

Visuals:AddButton("Click Tp tools",function()
    local plr = game:GetService("Players").LocalPlayer
local mouse = plr:GetMouse()

local tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "Click Teleport"

tool.Activated:Connect(function()
local root = plr.Character.HumanoidRootPart
local pos = mouse.Hit.Position+Vector3.new(0,2.5,0)
local offset = pos-root.Position
root.CFrame = root.CFrame+offset
end)

tool.Parent = plr.Backpack
end)

Visuals:AddButton("HighlightMode",function()
    for i,v in next, game.Players.LocalPlayer.PlayerGui:GetChildren() do
        if v:IsA'ScreenGui' then
        v:Destroy()
        end
        end
end)

Visuals:AddButton("DisableCHAT",function()
    local StarterGui = game:GetService('StarterGui')

StarterGui:SetCoreGuiEnabled(Enum.CoreGuiType.Chat, false)
end)

Visuals:AddButton("OpenCHAT",function()
    local StarterGui = game:GetService('StarterGui')

Visuals:SetCoreGuiEnabled(Enum.CoreGuiType.Chat, true)
end)

Visuals:AddButton("DisbaleInventory",function()
    for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
        v:Destroy()
        end
    end)

-------------------------------------------
