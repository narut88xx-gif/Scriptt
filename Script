-- LocalScript داخل StarterGui
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")
local rootPart = character:WaitForChild("HumanoidRootPart")
 Instance.new("ScreenGui")
screenGui.Parent = player:WaitForChild("PlayerGui")
local hubFrame = Instance.new("Frame")
hubFrame.Size = UDim2.new(0, 250, 0, 300)
hubFrame.Position = UDim2.new(0.5, -125, 0.5, -150)
hubFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
hubFrame.Visible = false
hubFrame.Parent = screenGui
local toggleButton = Instance.new("TextButton")
toggleButton.Size = UDim2.new(0, 100, 0, 50)
toggleButton.Position = UDim2.new(0, 10, 0, 10)
toggleButton.Text = "Hub"
toggleButton.Parent = screenGui

toggleButton.MouseButton1Click:Connect(function()
	hubFrame.Visible = not hubFrame.Visible
end)
local savedPosition = nil
local saveButton = Instance.new("TextButton")
saveButton.Size = UDim2.new(0, 200, 0, 40)
saveButton.Position = UDim2.new(0, 25, 0, 50)
saveButton.Text = "حفظ المكان"
saveButton.Parent = hubFrame

saveButton.MouseButton1Click:Connect(function()
	savedPosition = rootPart.Position
	print("تم حفظ المكان!")
end)
local teleportButton = Instance.new("TextButton")
teleportButton.Size = UDim2.new(0, 200, 0, 40)
teleportButton.Position = UDim2.new(0, 25, 0, 100)
teleportButton.Text = "الانتقال للبيت"
teleportButton.Parent = hubFrame

teleportButton.MouseButton1Click:Connect(function()
	if savedPosition then
		rootPart.CFrame = CFrame.new(savedPosition)
		print
	else
		print
	end
end)
local speedButton = Instance.new("TextButton")
speedButton.Size = UDim2.new(0, 200, 0, 40)
speedButton.Position = UDim2.new(0, 25, 0, 150)
speedButton.Text = "سرعة"
speedButton.Parent = hubFrame

speedButton.MouseButton1Click:Connect(function()
	humanoid.WalkSpeed = 50 -- الرقم الطبيعي 16
	wait(5) -- مدة البوست 5 ثواني
	humanoid.WalkSpeed = 16
end)
local jumpButton = Instance.new("TextButton")
jumpButton.Size = UDim2.new(0, 200, 0, 40)
jumpButton.Position = UDim2.new(0, 25, 0, 200)
jumpButton.Text = "قفز عالي"
jumpButton.Parent = hubFrame

jumpButton.MouseButton1Click:Connect(function()
	humanoid.JumpPower = 150 -- الرقم الطبيعي 50
	wait(5) -- مدة البوست 5 ثواني
	humanoid.JumpPower = 50
end)
