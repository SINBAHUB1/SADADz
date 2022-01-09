-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local ZOMBIE = Instance.new("TextButton")
local Animate = game.Players.LocalPlayer.Character.Animate

--Properties:

ScreenGui.Parent = game:WaitForChild("CoreGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(0, 255, 127)
Frame.Position = UDim2.new(0.822404385, 0, 0.934579432, 0)
Frame.Size = UDim2.new(0, 130, 0, 35)

ZOMBIE.Name = "ZOMBIE"
ZOMBIE.Parent = ScreenGui
ZOMBIE.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ZOMBIE.BackgroundTransparency = 1.000
ZOMBIE.Position = UDim2.new(0.822000027, 0, 0.935000002, 0)
ZOMBIE.Size = UDim2.new(0, 130, 0, 35)
ZOMBIE.Font = Enum.Font.SourceSans
ZOMBIE.Text = "ZOMBIE"
ZOMBIE.TextColor3 = Color3.fromRGB(255, 0, 0)
ZOMBIE.TextSize = 32.000
ZOMBIE.MouseButton1Click:Connect(function()
Animate.idle.Animation1.AnimationId = "http://www.roblox.com/asset/?id=616158929"
Animate.idle.Animation2.AnimationId = "http://www.roblox.com/asset/?id=616160636"
Animate.walk.WalkAnim.AnimationId = "http://www.roblox.com/asset/?id=616168032"
Animate.run.RunAnim.AnimationId = "http://www.roblox.com/asset/?id=616163682"
Animate.jump.JumpAnim.AnimationId = "http://www.roblox.com/asset/?id=616161997"
Animate.climb.ClimbAnim.AnimationId = "http://www.roblox.com/asset/?id=616156119"
Animate.fall.FallAnim.AnimationId = "http://www.roblox.com/asset/?id=616157476"
game.Players.LocalPlayer.Character.Humanoid.Jump = true
end)
