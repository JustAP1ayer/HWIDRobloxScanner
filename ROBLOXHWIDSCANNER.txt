local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local Frame_2 = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local TextButton = Instance.new("TextButton")
local UICorner_2 = Instance.new("UICorner")
local TextLabel = Instance.new("TextLabel")
local UICorner_3 = Instance.new("UICorner")
local UIGradient = Instance.new("UIGradient")
local UICorner_4 = Instance.new("UICorner")

ScreenGui.Parent = game.CoreGui

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame.Position = UDim2.new(0.151718095, 0, 0.78247869, 0)
Frame.Size = UDim2.new(0, 300, 0, 160)
Frame.Active = true
Frame.Draggable = true

Frame_2.Parent = Frame
Frame_2.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Frame_2.BorderColor3 = Color3.fromRGB(0, 0, 0)
Frame_2.Position = UDim2.new(0.021843059, 0, 0.0311091393, 0)
Frame_2.Size = UDim2.new(0, 286, 0, 150)

UICorner.Parent = Frame_2

TextButton.Parent = Frame_2
TextButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextButton.Position = UDim2.new(0.0403846651, 0, 0.439725757, 0)
TextButton.Size = UDim2.new(0, 262, 0, 75)
TextButton.Font = Enum.Font.SourceSansBold
TextButton.Text = "Hwid Scanner (coiied to clipboard)"
TextButton.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton.TextSize = 20.000
TextButton.TextWrapped = true
TextButton.MouseButton1Down:connect(function()
        		local CoreGui = game:GetService("StarterGui") -- Variable of StarterGui

	CoreGui:SetCore("SendNotification", {
		Title = "Hwid Copied!",
		Text = "The HWID has been copied to your clipboard",
		Duration = 10, -- Set the duration to how much you want this to stay
	})
    setclipboard(game:GetService("RbxAnalyticsService"):GetClientId())
end)

UICorner_2.Parent = TextButton

TextLabel.Parent = Frame_2
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.Position = UDim2.new(0.0438933372, 0, 0.0711441636, 0)
TextLabel.Size = UDim2.new(0, 261, 0, 50)
TextLabel.Font = Enum.Font.SourceSansBold
TextLabel.Text = "HWID Scanner by P|ayer"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextSize = 20.000

UICorner_3.Parent = TextLabel

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(255, 255, 255)), ColorSequenceKeypoint.new(0.16, Color3.fromRGB(255, 255, 255)), ColorSequenceKeypoint.new(0.29, Color3.fromRGB(255, 255, 255)), ColorSequenceKeypoint.new(0.53, Color3.fromRGB(0, 0, 0)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(0, 0, 0))}
UIGradient.Parent = Frame

UICorner_4.Parent = Frame


local function RMLLPZG_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	local currentrot = script.Parent.UIGradient.Rotation -- Gets the initial rotation of the UIGradient
	local TweenService = game:GetService("TweenService") -- Gets the Roblox TweenService to move things smoothly.
	local TweenInformation = TweenInfo.new(2, Enum.EasingStyle.Linear,Enum.EasingDirection.In,-1,false) -- This creates the TweenInfo. The parameters are in the following order: TimeToTween, EasingStyle, EasingDirection, RepeatCount (-1 for infinite), and reverses.
	local Goal = {Rotation = currentrot + 360} -- This is our goal for the tween. 360 makes the rotation go an entire circle.
	local Tween = TweenService:Create(script.Parent.UIGradient, TweenInformation, Goal) -- Creates the tween and the parameters are: UIGradient (object) location, TweenInformation, and Goal.
	Tween:Play() -- Plays the Tween
end
coroutine.wrap(RMLLPZG_fake_script)()