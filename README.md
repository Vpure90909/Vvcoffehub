local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local TitleLabel = Instance.new("TextLabel")
local ButtonFarm = Instance.new("TextButton")
local ButtonTeleport = Instance.new("TextButton")
local ButtonResetStats = Instance.new("TextButton")
local ButtonBoost = Instance.new("TextButton")
local ButtonClose = Instance.new("TextButton")

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.Name = "CoffeeHub"

Frame.Parent = ScreenGui
Frame.Size = UDim2.new(0, 300, 0, 400)
Frame.Position = UDim2.new(0, 10, 0, 10)
Frame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)

TitleLabel.Parent = Frame
TitleLabel.Size = UDim2.new(0, 280, 0, 50)
TitleLabel.Position = UDim2.new(0, 10, 0, 0)
TitleLabel.BackgroundColor3 = Color3.fromRGB(255, 165, 0)
TitleLabel.Text = "Coffee Hub"
TitleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TitleLabel.TextSize = 24
TitleLabel.TextAlign = Enum.TextXAlignment.Center
TitleLabel.Font = Enum.Font.SourceSansBold

ButtonFarm.Parent = Frame
ButtonFarm.Size = UDim2.new(0, 280, 0, 50)
ButtonFarm.Position = UDim2.new(0, 10, 0, 60)
ButtonFarm.BackgroundColor3 = Color3.fromRGB(0, 255, 0)
ButtonFarm.Text = "Farm (melhorar automaticamente)"
ButtonFarm.TextColor3 = Color3.fromRGB(255, 255, 255)

ButtonTeleport.Parent = Frame
ButtonTeleport.Size = UDim2.new(0, 280, 0, 50)
ButtonTeleport.Position = UDim2.new(0, 10, 0, 120)
ButtonTeleport.BackgroundColor3 = Color3.fromRGB(0, 0, 255)
ButtonTeleport.Text = "Teleportar"
ButtonTeleport.TextColor3 = Color3.fromRGB(255, 255, 255)

ButtonResetStats.Parent = Frame
ButtonResetStats.Size = UDim2.new(0, 280, 0, 50)
ButtonResetStats.Position = UDim2.new(0, 10, 0, 180)
ButtonResetStats.BackgroundColor3 = Color3.fromRGB(255, 165, 0)
ButtonResetStats.Text = "Resetar Stats"
ButtonResetStats.TextColor3 = Color3.fromRGB(255, 255, 255)

ButtonBoost.Parent = Frame
ButtonBoost.Size = UDim2.new(0, 280, 0, 50)
ButtonBoost.Position = UDim2.new(0, 10, 0, 240)
ButtonBoost.BackgroundColor3 = Color3.fromRGB(255, 165, 0)
ButtonBoost.Text = "Boost de habilidades"
ButtonBoost.TextColor3 = Color3.fromRGB(255, 255, 255)

ButtonClose.Parent = Frame
ButtonClose.Size = UDim2.new(0, 280, 0, 50)
ButtonClose.Position = UDim2.new(0, 10, 0, 300)
ButtonClose.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
ButtonClose.Text = "Fechar"
ButtonClose.TextColor3 = Color3.fromRGB(255, 255, 255)

ButtonFarm.MouseButton1Click:Connect(function()
    print("Farm ativado, melhorando suas habilidades.")
end)

ButtonTeleport.MouseButton1Click:Connect(function()
    print("Teleportando para um novo local.")
    local teleportTo = workspace:FindFirstChild("NomeDoLugar")
    if teleportTo then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = teleportTo.CFrame
    end
end)

ButtonResetStats.MouseButton1Click:Connect(function()
    print("Stats resetados.")
end)

ButtonBoost.MouseButton1Click:Connect(function()
    print("Boost de habilidades ativado!")
end)

ButtonClose.MouseButton1Click:Connect(function()
    ScreenGui:Destroy()
end)
