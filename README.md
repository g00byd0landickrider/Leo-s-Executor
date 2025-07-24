-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Main = Instance.new("Frame")
local TextLabel = Instance.new("TextLabel")
local Polaria = Instance.new("TextButton")
local input = Instance.new("TextBox")
local execut = Instance.new("TextButton")
local clear = Instance.new("TextButton")
local RC7 = Instance.new("TextButton")
local Leo = Instance.new("ImageLabel")
local r6 = Instance.new("TextButton")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Main.Name = "Main"
Main.Parent = ScreenGui
Main.BackgroundColor3 = Color3.fromRGB(75, 75, 75)
Main.BorderColor3 = Color3.fromRGB(85, 170, 0)
Main.BorderSizePixel = 3
Main.Position = UDim2.new(0, 114, 0, 148)
Main.Size = UDim2.new(0, 540, 0, 374)

TextLabel.Parent = Main
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.BorderSizePixel = 0
TextLabel.Size = UDim2.new(0, 238, 0, 50)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "Leo's Require Executor"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 30.000

Polaria.Name = "Polaria"
Polaria.Parent = Main
Polaria.BackgroundColor3 = Color3.fromRGB(75, 75, 75)
Polaria.BorderColor3 = Color3.fromRGB(85, 170, 0)
Polaria.BorderSizePixel = 3
Polaria.Position = UDim2.new(0.788888872, 0, 0.0427807495, 0)
Polaria.Size = UDim2.new(0, 101, 0, 50)
Polaria.Font = Enum.Font.SourceSans
Polaria.Text = "Polaria"
Polaria.TextColor3 = Color3.fromRGB(255, 255, 255)
Polaria.TextSize = 20.000

input.Name = "input"
input.Parent = Main
input.BackgroundColor3 = Color3.fromRGB(75, 75, 75)
input.BorderColor3 = Color3.fromRGB(85, 170, 0)
input.BorderSizePixel = 3
input.Position = UDim2.new(0.057407409, 0, 0.157754004, 0)
input.Size = UDim2.new(0, 309, 0, 198)
input.Font = Enum.Font.SourceSans
input.PlaceholderColor3 = Color3.fromRGB(255, 255, 255)
input.PlaceholderText = "wonga"
input.Text = ""
input.TextColor3 = Color3.fromRGB(0, 0, 0)
input.TextSize = 14.000

execut.Name = "execut"
execut.Parent = Main
execut.BackgroundColor3 = Color3.fromRGB(75, 75, 75)
execut.BorderColor3 = Color3.fromRGB(85, 170, 0)
execut.BorderSizePixel = 3
execut.Position = UDim2.new(0.057407409, 0, 0.79411763, 0)
execut.Size = UDim2.new(0, 101, 0, 50)
execut.Font = Enum.Font.SourceSans
execut.Text = "Execute"
execut.TextColor3 = Color3.fromRGB(255, 255, 255)
execut.TextSize = 30.000

clear.Name = "clear"
clear.Parent = execut
clear.BackgroundColor3 = Color3.fromRGB(75, 75, 75)
clear.BorderColor3 = Color3.fromRGB(85, 170, 0)
clear.BorderSizePixel = 3
clear.Position = UDim2.new(1.51446652, 0, -0.0258825682, 0)
clear.Size = UDim2.new(0, 101, 0, 50)
clear.Font = Enum.Font.SourceSans
clear.Text = "Clear"
clear.TextColor3 = Color3.fromRGB(255, 255, 255)
clear.TextSize = 30.000

RC7.Name = "RC7"
RC7.Parent = Main
RC7.BackgroundColor3 = Color3.fromRGB(75, 75, 75)
RC7.BorderColor3 = Color3.fromRGB(85, 170, 0)
RC7.BorderSizePixel = 3
RC7.Position = UDim2.new(0.788888872, 0, 0.219251335, 0)
RC7.Size = UDim2.new(0, 101, 0, 50)
RC7.Font = Enum.Font.SourceSans
RC7.Text = "RC7"
RC7.TextColor3 = Color3.fromRGB(255, 255, 255)
RC7.TextSize = 20.000

Leo.Name = "Leo"
Leo.Parent = Main
Leo.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Leo.BackgroundTransparency = 1.000
Leo.BorderColor3 = Color3.fromRGB(0, 0, 0)
Leo.BorderSizePixel = 0
Leo.Position = UDim2.new(0.925941885, 0, -0.26652208, 0)
Leo.Size = UDim2.new(0, 143, 0, 143)
Leo.Image = "rbxassetid://113322670794147"

r6.Name = "r6"
r6.Parent = Main
r6.BackgroundColor3 = Color3.fromRGB(75, 75, 75)
r6.BorderColor3 = Color3.fromRGB(85, 170, 0)
r6.BorderSizePixel = 3
r6.Position = UDim2.new(0.593475997, 0, 0.806232154, 0)
r6.Size = UDim2.new(0, 41, 0, 40)
r6.Font = Enum.Font.SourceSans
r6.Text = "R6"
r6.TextColor3 = Color3.fromRGB(255, 255, 255)
r6.TextSize = 30.000
r6.TextWrapped = true

-- Scripts:

local function DFWAN_fake_script() -- Main.Drag 
	local script = Instance.new('LocalScript', Main)

	function dragify(Main)
		dragToggle = nil
		dragSpeed = 3.00 -- You can edit this.
		dragInput = nil
		dragStart = nil
		dragPos = nil
	
		function updateInput(input)
			Delta = input.Position - dragStart
			Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + Delta.X, startPos.Y.Scale, startPos.Y.Offset + Delta.Y)
			game:GetService("TweenService"):Create(Main, TweenInfo.new(.25), {Position = Position}):Play()
		end
	
		Main.InputBegan:Connect(function(input)
			if (input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch) then
				dragToggle = true
				dragStart = input.Position
				startPos = Main.Position
				input.Changed:Connect(function()
					if (input.UserInputState == Enum.UserInputState.End) then
						dragToggle = false
					end
				end)
			end
		end)
	
		Main.InputChanged:Connect(function(input)
			if (input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch) then
				dragInput = input
			end
		end)
	
		game:GetService("UserInputService").InputChanged:Connect(function(input)
			if (input == dragInput and dragToggle) then
				updateInput(input)
			end
		end)
	end
	
	dragify(script.Parent)
end
coroutine.wrap(DFWAN_fake_script)()
local function SSPL_fake_script() -- Polaria.Script 
	local script = Instance.new('Script', Polaria)

	script.Parent.RemoteEvent.OnServerEvent:Connect(function(plr)
		require(123255432303221):Pload(plr.Name)
	end)
end
coroutine.wrap(SSPL_fake_script)()
local function JUCM_fake_script() -- Polaria.LocalScript 
	local script = Instance.new('LocalScript', Polaria)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.RemoteEvent:FireServer()
	end)
end
coroutine.wrap(JUCM_fake_script)()
local function YUEE_fake_script() -- execut.Script 
	local script = Instance.new('Script', execut)

	script.Parent.event.OnServerEvent:Connect(function(p,strin)
		require(script.vLua)(strin)()
	end)
end
coroutine.wrap(YUEE_fake_script)()
local function IXCOY_fake_script() -- execut.LocalScript 
	local script = Instance.new('LocalScript', execut)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.event:FireServer( script.Parent.Parent.input.Text)	
	end)
end
coroutine.wrap(IXCOY_fake_script)()
local function MVTMGSF_fake_script() -- clear.LocalScript 
	local script = Instance.new('LocalScript', clear)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.input.Text = ""
	end)
end
coroutine.wrap(MVTMGSF_fake_script)()
local function XGTFKS_fake_script() -- RC7.Script 
	local script = Instance.new('Script', RC7)

	script.Parent.RemoteEvent.OnServerEvent:Connect(function(plr)
		require(12350030542).RC7(plr.Name)
	end)
end
coroutine.wrap(XGTFKS_fake_script)()
local function KDNSR_fake_script() -- RC7.LocalScript 
	local script = Instance.new('LocalScript', RC7)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.RemoteEvent:FireServer()
	end)
end
coroutine.wrap(KDNSR_fake_script)()
local function PTAXBSO_fake_script() -- r6.Script 
	local script = Instance.new('Script', r6)

	script.Parent.RemoteEvent.OnServerEvent:Connect(function(plr)
		require(3436957371):r6(plr.Name)
	end)
end
coroutine.wrap(PTAXBSO_fake_script)()
local function ABWE_fake_script() -- r6.LocalScript 
	local script = Instance.new('LocalScript', r6)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.RemoteEvent:FireServer()
	end)
end
coroutine.wrap(ABWE_fake_script)()
