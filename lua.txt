

local player = game.Players.LocalPlayer 
local OrionLib =
loadstring(game:HttpGet(('https://raw.githubusercontent.com/thanhdat4461/OrionMoblie/main/source')))()local Window = OrionLib:MakeWindow({Name = "Orion", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"}) local Window = OrionLib:MakeWindow({Name = "Bryntt's Private Gui", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"}) --[[ Name = - The name of the UI. HidePremium = - Whether or not the user details shows Premium status or not. SaveConfig = - Toggles the config saving in the UI. ConfigFolder = - The name of the folder where the configs are saved. IntroEnabled = false - Whether or not to show the intro animation. IntroText = - Text to show in the intro animation. IntroIcon = - URL to the image you want to use in the intro animation. Icon = - URL to the image you want displayed on the window. CloseCallback = - Function to execute when the window is closed. ]] local Tab = Window:MakeTab({ Name = "Script", Icon = "rbxassetid://4483345998", PremiumOnly = false }) --[[ Name = - The name of the tab. Icon = - The icon of the tab. PremiumOnly = - Makes the tab accessible to Sirus Premium users only. ]] local Section = Tab:AddSection({ Name = "LocalPlayer" }) --[[ Name = - The name of the section. ]] OrionLib:MakeNotification({ Name = "Welcome!", Content = "Welcome to my hub!", Image = "rbxassetid://4483345998", Time = 5 }) --[[ Title = - The title of the notification. Content = - The content of the notification. Image = - The icon of the notification. Time = - The duration of the notfication. ]] 

Tab:AddButton({
	Name = "No Cooldown",
	Callback = function()
g = hookfunction(wait, function(seconds) return g(0) end)
      		print("button pressed")
  	end    
})

--[[
Nam
e = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

Tab:AddButton({
	Name = "Get perm Food",
	Callback = function()
while wait(0.5) do fireclickdetector(game.Workspace.Food.Main.ClickDetector) end
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name
 of the button.
Callback = <function> - The function of the button.
]]

Tab:AddButton({
	Name = "Kill Aura",
	Callback = function()
local lp = game:FindFirstChildOfClass("Players").LocalPlayer
local chr = lp.Character
while chr["Right Arm"] and wait(0.25) do
local lowest = math.huge
local NearestPlayer = nil
for _,plr in pairs(game:FindFirstChildOfClass("Players"):GetPlayers()) do
    if plr ~= lp and plr.Character:FindFirstChildOfClass("Humanoid").Health ~= 0 and plr.Team ~= lp.Team and not lp:IsFriendsWith(plr.UserId) then
        local distance = plr:DistanceFromCharacter(chr.HumanoidRootPart.Position)
        if distance < lowest then
            lowest = distance
            NearestPlayer = {plr}
        end
    end
end
for i,v in pairs(NearestPlayer) do
local args = {
    [1] = chr,
    [2] = v.Character.HumanoidRootPart,
    [3] = chr:FindFirstChildOfClass("Tool")
}
wait()
game:GetService("ReplicatedStorage"):WaitForChild("Combat"):FireServer(unpack(args))
end
end

      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

Tab:AddButton({
	Name = "Open Door Aura",
	Callback = function()
while wait(0.1) do local args = {
    [1] = "Door1",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
local args = {
    [1] = "Door2",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
local args = {
    [1] = "Door3",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
local args = {
    [1] = "Door4",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
local args = {
    [1] = "Door5",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
local args = {
    [1] = "Door6",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
local args = {
    [1] = "Door7",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
local args = {
    [1] = "Door8",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
local args = {
    [1] = "Door9",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
local args = {
    [1] = "Door10",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
local args = {
    [1] = "Door12",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
local args = {
    [1] = "Door13",
    [2] = "Open"
}

game:GetService("ReplicatedStorage"):WaitForChild("DoorOpener"):FireServer(unpack(args))
end
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

Tab:AddButton({
	Name = "Drop Flashlights",
	Callback = function()
local lp = game:FindFirstChildOfClass("Players").LocalPlayer
for i=1,20 do
fireclickdetector(workspace["Flashlight"].ClickDetector)
for i,v in lp.Backpack:GetChildren() do if v.Name=="Flashlight" then
        v.Parent = lp.Character
end end
fireclickdetector(workspace["Flashlight"].ClickDetector)
wait()
for i,v in lp.Character:GetChildren() do if v.Name=="Flashlight" then
        v.Parent = workspace
end end
end
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

Tab:AddButton({
	Name = "Drop Food",
	Callback = function()
local lp = game:FindFirstChildOfClass("Players").LocalPlayer
for i=1,20 do
fireclickdetector(workspace["Food"].Main.ClickDetector)
for i,v in lp.Backpack:GetChildren() do if v.Name=="Food" then
        v.Parent = lp.Character
end end
fireclickdetector(workspace["Food"].Main.ClickDetector)
wait()
for i,v in lp.Character:GetChildren() do if v.Name=="Food" then
        v.Parent = workspace
end end
end

      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

Tab:AddButton({
	Name = "Auto Heal",
	Callback = function()
Autoheal = true
plr = game:FindFirstChildOfClass("Players").LocalPlayer
    while Autoheal and wait(0.5) do
        local hp = plr.character.Humanoid.Health
        if hp ~= 100 then
            local food = plr.Backpack:FindFirstChild("Food")
            local old = plr.character:FindFirstChildOfClass("Tool")
            
            plr.character.Humanoid:EquipTool(food)
            plr.character.Food:Activate()
            
            wait()
            
            if old ~= nil then
                plr.character.Humanoid:EquipTool(old)
                end
            end
        end
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

Tab:AddButton({
	Name = "Lag Server(will also lag u)",
	Callback = function()
game:FindFirstChildOfClass("RunService").Heartbeat:Connect(function()
local args = {
    [1] = 46,
    [2] = 13352926142,
    [3] = "Bobux Blaster",
    [4] = "13352926142"
}

game:GetService("ReplicatedStorage"):WaitForChild("Import"):FireServer(unpack(args))
end)
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

local Tab = Window:MakeTab({
	Name = "Local Player",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]

local Tab = Window:MakeTab({
	Name = "Extra useful scripts",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]

Tab:AddButton({
	Name = "Keyboard",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/GGH52lan/GGH52lan/main/keyboard.txt"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

Tab:AddButton({
	Name = "fly gui",
	Callback = function()
-- fly gui modded --

local main = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local up = Instance.new("TextButton")
local down = Instance.new("TextButton")
local onof = Instance.new("TextButton")
local TextLabel = Instance.new("TextLabel")
local plus = Instance.new("TextButton")
local speed = Instance.new("TextLabel")
local mine = Instance.new("TextButton")
local closebutton = Instance.new("TextButton")
local mini = Instance.new("TextButton")
local mini2 = Instance.new("TextButton")

main.Name = "main"
main.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
main.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
main.ResetOnSpawn = false

Frame.Parent = main
Frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame.BorderColor3 = Color3.fromRGB(0, 0, 0)
Frame.Position = UDim2.new(0.100320168, 0, 0.379746825, 0)
Frame.Size = UDim2.new(0, 190, 0, 57)

up.Name = "up"
up.Parent = Frame
up.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
up.Size = UDim2.new(0, 44, 0, 28)
up.Font = Enum.Font.SourceSans
up.Text = "↑"
up.TextColor3 = Color3.fromRGB(0, 0, 0)
up.TextSize = 14.000

down.Name = "down"
down.Parent = Frame
down.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
down.Position = UDim2.new(0, 0, 0.491228074, 0)
down.Size = UDim2.new(0, 44, 0, 28)
down.Font = Enum.Font.SourceSans
down.Text = "↓"
down.TextColor3 = Color3.fromRGB(0, 0, 0)
down.TextSize = 14.000

onof.Name = "onof"
onof.Parent = Frame
onof.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
onof.Position = UDim2.new(0.702823281, 0, 0.491228074, 0)
onof.Size = UDim2.new(0, 56, 0, 28)
onof.Font = Enum.Font.Michroma
onof.Text = "FLY"
onof.TextColor3 = Color3.fromRGB(0, 0, 0)
onof.TextSize = 14.000

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.Position = UDim2.new(0.469327301, 0, 0, 0)
TextLabel.Size = UDim2.new(0, 100, 0, 28)
TextLabel.Font = Enum.Font.Michroma
TextLabel.Text = "Fly gui modded"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

plus.Name = "plus"
plus.Parent = Frame
plus.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
plus.Position = UDim2.new(0.231578946, 0, 0, 0)
plus.Size = UDim2.new(0, 45, 0, 28)
plus.Font = Enum.Font.SourceSans
plus.Text = "+"
plus.TextColor3 = Color3.fromRGB(0, 0, 0)
plus.TextScaled = true
plus.TextSize = 14.000
plus.TextWrapped = true

speed.Name = "speed"
speed.Parent = Frame
speed.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
speed.Position = UDim2.new(0.468421042, 0, 0.491228074, 0)
speed.Size = UDim2.new(0, 44, 0, 28)
speed.Font = Enum.Font.SourceSans
speed.Text = "1"
speed.TextColor3 = Color3.fromRGB(0, 0, 0)
speed.TextScaled = true
speed.TextSize = 14.000
speed.TextWrapped = true

mine.Name = "mine"
mine.Parent = Frame
mine.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
mine.Position = UDim2.new(0.231578946, 0, 0.491228074, 0)
mine.Size = UDim2.new(0, 45, 0, 29)
mine.Font = Enum.Font.SourceSans
mine.Text = "-"
mine.TextColor3 = Color3.fromRGB(0, 0, 0)
mine.TextScaled = true
mine.TextSize = 14.000
mine.TextWrapped = true

closebutton.Name = "Close"
closebutton.Parent = main.Frame
closebutton.BackgroundColor3 = Color3.fromRGB(255, 5, 5)
closebutton.Font = "Michroma"
closebutton.Size = UDim2.new(0, 45, 0, 28)
closebutton.Text = "x"
closebutton.TextSize = 30
closebutton.Position =  UDim2.new(0, 0, -1, 27)

mini.Name = "minimize"
mini.Parent = main.Frame
mini.BackgroundColor3 = Color3.fromRGB(117, 117, 117)
mini.Font = "Michroma"
mini.Size = UDim2.new(0, 45, 0, 28)
mini.Text = "-"
mini.TextSize = 40
mini.Position = UDim2.new(0, 44, -1, 27)

mini2.Name = "minimize2"
mini2.Parent = main.Frame
mini2.BackgroundColor3 = Color3.fromRGB(117, 117, 117)
mini2.Font = "SourceSans"
mini2.Size = UDim2.new(0, 45, 0, 28)
mini2.Text = "+"
mini2.TextSize = 40
mini2.Position = UDim2.new(0, 44, -1, 57)
mini2.Visible = false

speeds = 1

local speaker = game:GetService("Players").LocalPlayer

local chr = game.Players.LocalPlayer.Character
local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")

nowe = false

game:GetService("StarterGui"):SetCore("SendNotification", { 
	Title = "FLY GUI MODDED(Bryntt)";
	Text = "Fly gui Modded v1 by bryntt";
	Icon = "rbxthumb://type=Asset&id=5107182114&w=150&h=150"})
Duration = 5;

Frame.Active = true -- main = gui
Frame.Draggable = true

onof.MouseButton1Down:connect(function()

	if nowe == true then
		nowe = false

		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Climbing,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.FallingDown,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Flying,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Freefall,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.GettingUp,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Landed,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Physics,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.PlatformStanding,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Ragdoll,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Running,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.RunningNoPhysics,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.StrafingNoPhysics,true)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Swimming,true)
		speaker.Character.Humanoid:ChangeState(Enum.HumanoidStateType.RunningNoPhysics)
	else 
		nowe = true



		for i = 1, speeds do
			spawn(function()

				local hb = game:GetService("RunService").Heartbeat	


				tpwalking = true
				local chr = game.Players.LocalPlayer.Character
				local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")
				while tpwalking and hb:Wait() and chr and hum and hum.Parent do
					if hum.MoveDirection.Magnitude > 0 then
						chr:TranslateBy(hum.MoveDirection)
					end
				end

			end)
		end
		game.Players.LocalPlayer.Character.Animate.Disabled = true
		local Char = game.Players.LocalPlayer.Character
		local Hum = Char:FindFirstChildOfClass("Humanoid") or Char:FindFirstChildOfClass("AnimationController")

		for i,v in next, Hum:GetPlayingAnimationTracks() do
			v:AdjustSpeed(0)
		end
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Climbing,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.FallingDown,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Flying,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Freefall,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.GettingUp,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Landed,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Physics,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.PlatformStanding,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Ragdoll,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Running,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.RunningNoPhysics,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.StrafingNoPhysics,false)
		speaker.Character.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Swimming,false)
		speaker.Character.Humanoid:ChangeState(Enum.HumanoidStateType.Swimming)
	end




	if game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R6 then



		local plr = game.Players.LocalPlayer
		local torso = plr.Character.Torso
		local flying = true
		local deb = true
		local ctrl = {f = 0, b = 0, l = 0, r = 0}
		local lastctrl = {f = 0, b = 0, l = 0, r = 0}
		local maxspeed = 50
		local speed = 0


		local bg = Instance.new("BodyGyro", torso)
		bg.P = 9e4
		bg.maxTorque = Vector3.new(9e9, 9e9, 9e9)
		bg.cframe = torso.CFrame
		local bv = Instance.new("BodyVelocity", torso)
		bv.velocity = Vector3.new(0,0.1,0)
		bv.maxForce = Vector3.new(9e9, 9e9, 9e9)
		if nowe == true then
			plr.Character.Humanoid.PlatformStand = true
		end
		while nowe == true or game:GetService("Players").LocalPlayer.Character.Humanoid.Health == 0 do
			game:GetService("RunService").RenderStepped:Wait()

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
				bv.velocity = Vector3.new(0,0,0)
			end
			--	game.Players.LocalPlayer.Character.Animate.Disabled = true
			bg.cframe = game.Workspace.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*speed/maxspeed),0,0)
		end
		ctrl = {f = 0, b = 0, l = 0, r = 0}
		lastctrl = {f = 0, b = 0, l = 0, r = 0}
		speed = 0
		bg:Destroy()
		bv:Destroy()
		plr.Character.Humanoid.PlatformStand = false
		game.Players.LocalPlayer.Character.Animate.Disabled = false
		tpwalking = false




	else
		local plr = game.Players.LocalPlayer
		local UpperTorso = plr.Character.UpperTorso
		local flying = true
		local deb = true
		local ctrl = {f = 0, b = 0, l = 0, r = 0}
		local lastctrl = {f = 0, b = 0, l = 0, r = 0}
		local maxspeed = 50
		local speed = 0


		local bg = Instance.new("BodyGyro", UpperTorso)
		bg.P = 9e4
		bg.maxTorque = Vector3.new(9e9, 9e9, 9e9)
		bg.cframe = UpperTorso.CFrame
		local bv = Instance.new("BodyVelocity", UpperTorso)
		bv.velocity = Vector3.new(0,0.1,0)
		bv.maxForce = Vector3.new(9e9, 9e9, 9e9)
		if nowe == true then
			plr.Character.Humanoid.PlatformStand = true
		end
		while nowe == true or game:GetService("Players").LocalPlayer.Character.Humanoid.Health == 0 do
			wait()

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
				bv.velocity = Vector3.new(0,0,0)
			end

			bg.cframe = game.Workspace.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*speed/maxspeed),0,0)
		end
		ctrl = {f = 0, b = 0, l = 0, r = 0}
		lastctrl = {f = 0, b = 0, l = 0, r = 0}
		speed = 0
		bg:Destroy()
		bv:Destroy()
		plr.Character.Humanoid.PlatformStand = false
		game.Players.LocalPlayer.Character.Animate.Disabled = false
		tpwalking = false



	end





end)

local tis

up.MouseButton1Down:connect(function()
	tis = up.MouseEnter:connect(function()
		while tis do
			wait()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,1,0)
		end
	end)
end)

up.MouseLeave:connect(function()
	if tis then
		tis:Disconnect()
		tis = nil
	end
end)

local dis

down.MouseButton1Down:connect(function()
	dis = down.MouseEnter:connect(function()
		while dis do
			wait()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,-1,0)
		end
	end)
end)

down.MouseLeave:connect(function()
	if dis then
		dis:Disconnect()
		dis = nil
	end
end)


game:GetService("Players").LocalPlayer.CharacterAdded:Connect(function(char)
	wait(0.7)
	game.Players.LocalPlayer.Character.Humanoid.PlatformStand = false
	game.Players.LocalPlayer.Character.Animate.Disabled = false

end)


plus.MouseButton1Down:connect(function()
	speeds = speeds + 1
	speed.Text = speeds
	if nowe == true then


		tpwalking = false
		for i = 1, speeds do
			spawn(function()

				local hb = game:GetService("RunService").Heartbeat	


				tpwalking = true
				local chr = game.Players.LocalPlayer.Character
				local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")
				while tpwalking and hb:Wait() and chr and hum and hum.Parent do
					if hum.MoveDirection.Magnitude > 0 then
						chr:TranslateBy(hum.MoveDirection)
					end
				end

			end)
		end
	end
end)
mine.MouseButton1Down:connect(function()
	if speeds == 1 then
		speed.Text = '-1 speed fly bruh'
		wait(1)
		speed.Text = speeds
	else
		speeds = speeds - 1
		speed.Text = speeds
		if nowe == true then
			tpwalking = false
			for i = 1, speeds do
				spawn(function()

					local hb = game:GetService("RunService").Heartbeat	


					tpwalking = true
					local chr = game.Players.LocalPlayer.Character
					local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")
					while tpwalking and hb:Wait() and chr and hum and hum.Parent do
						if hum.MoveDirection.Magnitude > 0 then
							chr:TranslateBy(hum.MoveDirection)
						end
					end

				end)
			end
		end
	end
end)

closebutton.MouseButton1Click:Connect(function()
	main:Destroy()
end)

mini.MouseButton1Click:Connect(function()
	up.Visible = false
	down.Visible = false
	onof.Visible = false
	plus.Visible = false
	speed.Visible = false
	mine.Visible = false
	mini.Visible = false
	mini2.Visible = true
	main.Frame.BackgroundTransparency = 1
	closebutton.Position =  UDim2.new(0, 0, -1, 57)
end)

mini2.MouseButton1Click:Connect(function()
	up.Visible = true
	down.Visible = true
	onof.Visible = true
	plus.Visible = true
	speed.Visible = true
	mine.Visible = true
	mini.Visible = true
	mini2.Visible = false
	main.Frame.BackgroundTransparency = 0 
	closebutton.Position =  UDim2.new(0, 0, -1, 27)
end)
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

local Tab = Window:MakeTab({
	Name = "Personal Scripts",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]

Tab:AddButton({
	Name = "Remove Tools",
	Callback = function()
local humanoid=game.Players.LocalPlayer.Character.Humanoid for i,v in workspace:GetChildren() do if v:IsA("Tool")then humanoid:EquipTool(v)end end


      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

Tab:AddButton({
	Name = "Firerate Taser",
	Callback = function()
while wait(0.1) do local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(293.488525390625, 3.6236164569854736, -123.87115478515625), [4] = Vector3.new(320.31268310546875, 11.536121368408203, -119.47604370117188)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(293.4723815917969, 3.888279676437378, -123.8556137084961), [4] = Vector3.new(320.71270751953125, 17.230005264282227, -105.72592163085938)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(287.93988037109375, 4.237425327301025, -136.69821166992188), [4] = Vector3.new(318.90765380859375, 23.57677459716797, -144.21343994140625)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(288.7957763671875, 3.517001152038574, -132.997314453125), [4] = Vector3.new(320.31268310546875, 11.054224014282227, -125.25593566894531)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(289.19134521484375, 2.3129255771636963, -117.75687408447266), [4] = Vector3.new(314.1751708984375, 0.14328402280807495, -92.62419891357422)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(283.41644287109375, 2.831026554107666, -123.76801300048828), [4] = Vector3.new(311.64581298828125, 4.308165550231934, -177.77713012695312)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(286.3594055175781, 2.374783515930176, -117.54442596435547), [4] = Vector3.new(245.72067260742188, 0.08828246593475342, -127.77269744873047)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(286.4200134277344, 2.6156299114227295, -117.4356918334961), [4] = Vector3.new(250.1805419921875, 0.08828246593475342, -86.25298309326172)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(286.45806884765625, 3.148256301879883, -117.26486206054688), [4] = Vector3.new(273.9097900390625, 11.92141056060791, -147.35818481445312)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(243.3400421142578, 2.536106586456299, -123.88346099853516), [4] = Vector3.new(234.5050506591797, 5.284335613250732, -111.89228820800781)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Recharge", [2] = game:GetService("Players").LocalPlayer.Character.Taser}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(196.78436279296875, 2.8602700233459473, -103.96239471435547), [4] = Vector3.new(179.12063598632812, 6.223569869995117, -82.45277404785156)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(221.24917602539062, 2.751197099685669, -46.498226165771484), [4] = Vector3.new(226.90577697753906, 7.243437767028809, -3.6979620456695557)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(289.1665954589844, 3.4861936569213867, -38.16948318481445), [4] = Vector3.new(296.5570373535156, 6.295042037963867, -14.110631942749023)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(255.87843322753906, 3.471940279006958, -38.028751373291016), [4] = Vector3.new(274.2921447753906, 5.687755584716797, -4.136838912963867)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(303.52227783203125, 3.3330469131469727, -25.82371711730957), [4] = Vector3.new(316.0497741699219, 3.528512954711914, -30.155494689941406)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(296.826904296875, 3.998159885406494, -25.71263885498047), [4] = Vector3.new(316.24365234375, 9.641960144042969, -17.032814025878906)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(365.5941162109375, 3.678797483444214, -70.44840240478516), [4] = Vector3.new(393.2484130859375, 6.970439910888672, -67.18344116210938)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(411.7159729003906, 6.474987506866455, -87.19078826904297), [4] = Vector3.new(436.5423889160156, 14.617170333862305, -84.57024383544922)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(405.3244323730469, 4.921108245849609, -126.59774780273438), [4] = Vector3.new(413.0510559082031, 24.389671325683594, -102.53115844726562)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(421.7029724121094, 3.5816776752471924, -129.517333984375), [4] = Vector3.new(432.6357421875, 10.710941314697266, -102.53115844726562)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(415.3357849121094, 4.323906898498535, -129.3115997314453), [4] = Vector3.new(386.8388671875, 34.236881256103516, -57.215606689453125)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(400.136474609375, 3.125710964202881, -131.47962951660156), [4] = Vector3.new(381.9361267089844, 0.7973626852035522, -119.53941345214844)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(362.04296875, 3.8965835571289062, -131.87362670898438), [4] = Vector3.new(352.02996826171875, 11.287894248962402, -96.75381469726562)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(355.96978759765625, 4.224085330963135, -129.61512756347656), [4] = Vector3.new(321.71270751953125, 16.482755661010742, -119.17753601074219)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(331.3363342285156, 4.177181720733643, -121.33940124511719), [4] = Vector3.new(322.47772216796875, 14.78603744506836, -152.47010803222656)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(348.25079345703125, 3.8889243602752686, -127.68216705322266), [4] = Vector3.new(367.2822570800781, 9.69821834564209, -108.78102111816406)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(371.0882263183594, 3.868664264678955, -145.61557006835938), [4] = Vector3.new(379.43353271484375, 9.483856201171875, -173.20123291015625)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(390.8217468261719, 3.629869222640991, -127.46498107910156), [4] = Vector3.new(406.3428955078125, 6.575023651123047, -91.9364013671875)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(397.459716796875, 3.634531021118164, -127.70938873291016), [4] = Vector3.new(382.28106689453125, 6.656655788421631, -96.75381469726562)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(406.9524841308594, 4.290699005126953, -162.211669921875), [4] = Vector3.new(438.3789978027344, 18.483055114746094, -187.90028381347656)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(400.7513732910156, 4.818333148956299, -161.83035278320312), [4] = Vector3.new(420.938232421875, 19.103286743164062, -165.73130798339844)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(407.37628173828125, 2.364859104156494, -160.1947021484375), [4] = Vector3.new(407.24365234375, 0.1382824033498764, -167.4492950439453)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(420.0647888183594, 5.799650192260742, -97.49076843261719), [4] = Vector3.new(436.39190673828125, 6.782283306121826, -93.88101196289062)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(420.2024841308594, 5.975165367126465, -97.71304321289062), [4] = Vector3.new(436.39190673828125, 8.40818977355957, -94.98495483398438)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(421.8370361328125, 5.668764591217041, -92.79476165771484), [4] = Vector3.new(436.5423889160156, 5.778575897216797, -99.77526092529297)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(467.07415771484375, -5.201163291931152, -95.16835021972656), [4] = Vector3.new(480.26788330078125, -4.577347278594971, -101.34725952148438)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(465.9250183105469, -5.235780239105225, -91.46246337890625), [4] = Vector3.new(480.14788818359375, -4.878503322601318, -87.06195831298828)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(468.39984130859375, -4.464741230010986, -90.60575103759766), [4] = Vector3.new(478.5010986328125, 0.9402191638946533, -79.05272674560547)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(467.3834228515625, -5.324757099151611, -80.6892318725586), [4] = Vector3.new(456.10821533203125, -5.227901458740234, -77.48258972167969)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(463.87060546875, -4.923851013183594, -87.50238037109375), [4] = Vector3.new(452.8207702636719, -2.776632070541382, -95.64520263671875)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(287.974853515625, 3.3540167808532715, -249.90235900878906), [4] = Vector3.new(290.49169921875, 9.558609008789062, -272.9654541015625)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(267.4780578613281, 3.16227126121521, -266.83990478515625), [4] = Vector3.new(240.67189025878906, 8.817177772521973, -292.6222839355469)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(240.5333709716797, 3.552541494369507, -259.6960144042969), [4] = Vector3.new(217.3238067626953, 16.250816345214844, -231.123779296875)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(236.4614715576172, 3.022730588912964, -252.4449462890625), [4] = Vector3.new(215.07643127441406, 6.975266933441162, -212.66795349121094)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(241.0052947998047, 3.0054845809936523, -245.3392791748047), [4] = Vector3.new(262.2690124511719, 10.680765151977539, -116.1404800415039)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(261.9715576171875, 3.3259880542755127, -289.6903381347656), [4] = Vector3.new(269.9447937011719, 0.8195689916610718, -247.33233642578125)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(293.04412841796875, 4.023926258087158, -311.0821228027344), [4] = Vector3.new(325.3068542480469, 12.274492263793945, -304.3267822265625)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(337.6983642578125, 3.651660203933716, -362.0594177246094), [4] = Vector3.new(380.2926940917969, 7.660664081573486, -370.5499572753906)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(350.0098571777344, 3.5570929050445557, -355.8807678222656), [4] = Vector3.new(367.4047546386719, 3.1497673988342285, -304.4180908203125)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(367.90606689453125, 3.7612972259521484, -329.6940612792969), [4] = Vector3.new(427.8011474609375, 13.518989562988281, -291.1977844238281)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(396.0306396484375, 3.812753200531006, -222.22862243652344), [4] = Vector3.new(430.3147888183594, 10.665536880493164, -192.7845916748047)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(369.8858337402344, 3.744117021560669, -215.1697998046875), [4] = Vector3.new(345.191162109375, 8.833724975585938, -187.05715942382812)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(317.7271423339844, 3.8929004669189453, -182.47314453125), [4] = Vector3.new(318.6141662597656, 9.728710174560547, -156.601806640625)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(314.6407165527344, 3.221569061279297, -189.94895935058594), [4] = Vector3.new(343.43682861328125, 0.08828246593475342, -207.56964111328125)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(290.4998779296875, 2.5537290573120117, -384.8448791503906), [4] = Vector3.new(263.1203308105469, 0.121668741106987, -460.15234375)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(222.87954711914062, 2.712430000305176, -435.96466064453125), [4] = Vector3.new(222.81483459472656, 0.12173032015562057, -445.429443359375)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(203.21775817871094, 3.7429428100585938, -447.9443054199219), [4] = Vector3.new(187.59078979492188, 6.873525619506836, -421.9060363769531)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(317.3943176269531, 4.919466495513916, -353.9983215332031), [4] = Vector3.new(242.54312133789062, 228.0289306640625, -64.48150634765625)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(345.9506530761719, 4.463437080383301, -319.4868469238281), [4] = Vector3.new(414.20709228515625, 200.56007385253906, -60.44331741333008)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(335.3523254394531, 5.22838020324707, -210.04287719726562), [4] = Vector3.new(247.35125732421875, 228.0289306640625, -31.508270263671875)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Recharge", [2] = game:GetService("Players").LocalPlayer.Character.Taser}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(296.46307373046875, 4.194726467132568, -119.8091812133789), [4] = Vector3.new(320.31268310546875, 16.253177642822266, -118.8762435913086)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(286.1639404296875, 3.765148162841797, -122.67891693115234), [4] = Vector3.new(320.71270751953125, 12.20571231842041, -145.6624755859375)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(292.5986633300781, 3.452502489089966, -96.7906723022461), [4] = Vector3.new(312.2837829589844, 8.6138277053833, -63.41773986816406)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(267.7732238769531, 4.028219223022461, -78.55516052246094), [4] = Vector3.new(271.50775146484375, 14.91615104675293, -46.26365661621094)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(233.02699279785156, 2.6952078342437744, -54.22157669067383), [4] = Vector3.new(179.12063598632812, 7.710941314697266, -4.021385192871094)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(221.99034118652344, 4.934342861175537, -58.46061706542969), [4] = Vector3.new(181.30885314941406, 40.486576080322266, -60.67402267456055)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(195.37161254882812, 2.669403314590454, -80.66047668457031), [4] = Vector3.new(174.25958251953125, 6.730836868286133, -118.29132843017578)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(56.176185607910156, 3.611405372619629, -96.01075744628906), [4] = Vector3.new(47.347286224365234, 6.281316757202148, -75.23035430908203)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(70.16273498535156, 3.9933724403381348, -53.281951904296875), [4] = Vector3.new(92.32494354248047, 12.069648742675781, -28.110671997070312)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(74.53706359863281, 3.738377809524536, -57.38486099243164), [4] = Vector3.new(109.2300033569336, 8.41930103302002, -54.43914031982422)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(56.50430679321289, 3.471004009246826, -91.89537048339844), [4] = Vector3.new(47.29317855834961, 4.646622180938721, -108.97433471679688)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(125.83399200439453, 4.569541931152344, -102.67715454101562), [4] = Vector3.new(107.69578552246094, 14.617288589477539, -106.41986846923828)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(125.39130401611328, 4.290585041046143, -102.38668823242188), [4] = Vector3.new(105.34573364257812, 12.267080307006836, -98.15277099609375)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(123.55168151855469, 3.404416799545288, -102.13298034667969), [4] = Vector3.new(101.95696258544922, 3.6545886993408203, -100.15316772460938)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(128.91741943359375, 3.6872081756591797, -64.52847290039062), [4] = Vector3.new(110.93998718261719, 7.511792182922363, -38.476661682128906)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(128.86062622070312, 3.8067524433135986, -40.48637771606445), [4] = Vector3.new(144.33009338378906, 6.281427383422852, -39.141963958740234)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(124.73735046386719, 3.899360418319702, -63.798500061035156), [4] = Vector3.new(112.44068145751953, 11.049653053283691, -95.27388000488281)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(106.92240905761719, 3.913116216659546, -77.71387481689453), [4] = Vector3.new(62.34610366821289, 13.294581413269043, -70.0728759765625)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(217.54505920410156, 4.098665237426758, -126.48066711425781), [4] = Vector3.new(226.55810546875, 11.56459903717041, -148.14175415039062)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(209.51513671875, 4.880582332611084, -173.4777374267578), [4] = Vector3.new(180.82826232910156, 40.01205062866211, -211.58383178710938)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(256.381103515625, 3.5500996112823486, -172.01242065429688), [4] = Vector3.new(229.035400390625, 5.202381134033203, -182.93455505371094)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(311.377685546875, 3.78222393989563, -191.4596405029297), [4] = Vector3.new(425.2679138183594, 20.52068328857422, -300.6525573730469)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(370.64056396484375, 3.8014090061187744, -432.8194885253906), [4] = Vector3.new(398.09857177734375, 10.157447814941406, -470.3283386230469)}local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(371.3664245605469, 3.93414044380188, -499.1506652832031), [4] = Vector3.new(398.09857177734375, 10.701713562011719, -525.96337890625)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(370.3072204589844, 4.5741753578186035, -606.0076904296875), [4] = Vector3.new(397.00689697265625, 21.198179244995117, -626.9213256835938)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(350.9964294433594, 4.10738468170166, -621.8009033203125), [4] = Vector3.new(333.4554748535156, 11.984189987182617, -600.2156372070312)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(317.96380615234375, 5.1473469734191895, -617.1064453125), [4] = Vector3.new(288.729736328125, 38.49993896484375, -641.8557739257812)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(271.6837158203125, 3.800870656967163, -618.2557983398438), [4] = Vector3.new(238.2863311767578, 9.609771728515625, -642.0678100585938)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(225.10865783691406, 3.815854549407959, -623.4359130859375), [4] = Vector3.new(188.42428588867188, 9.478862762451172, -629.0072021484375)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(222.07894897460938, 4.053826332092285, -613.1334838867188), [4] = Vector3.new(218.8302459716797, 11.08009147644043, -641.5673217773438)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(227.33482360839844, 3.5875959396362305, -124.85994720458984), [4] = Vector3.new(197.13726806640625, 6.490198135375977, -87.35039520263672)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(236.39857482910156, 3.0920889377593994, -90.44949340820312), [4] = Vector3.new(211.68185424804688, 0.14328402280807495, -95.79894256591797)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(260.59600830078125, 3.6416661739349365, -86.57865142822266), [4] = Vector3.new(238.8112335205078, 6.873586177825928, -106.81209564208984)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(261.0709228515625, 3.6911137104034424, -145.6476287841797), [4] = Vector3.new(281.85125732421875, 8.052488327026367, -181.72938537597656)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(300.8964538574219, 3.3009512424468994, -169.92906188964844), [4] = Vector3.new(270.12353515625, 1.6194905042648315, -170.42665100097656)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(261.60205078125, 4.230282783508301, -181.10614013671875), [4] = Vector3.new(234.11624145507812, 14.73120403289795, -174.0978240966797)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(246.9937744140625, 3.12669038772583, -89.51327514648438), [4] = Vector3.new(224.07052612304688, 0.08828246593475342, -75.93582916259766)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(265.782470703125, 3.2666268348693848, -85.4658203125), [4] = Vector3.new(279.0924377441406, 2.0689797401428223, -68.19539642333984)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(265.14056396484375, 4.193469524383545, -92.38336944580078), [4] = Vector3.new(281.81439208984375, 10.365386009216309, -86.80146026611328)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(260.63629150390625, 5.2032294273376465, -89.546875), [4] = Vector3.new(307.1333312988281, 89.20529174804688, -13.41339111328125)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(288.23236083984375, 4.846540927886963, -121.46021270751953), [4] = Vector3.new(461.79302978515625, 126.00726318359375, -167.06895446777344)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(279.38604736328125, 5.948452472686768, -128.9891357421875), [4] = Vector3.new(320.4443054199219, 228.0289306640625, -163.44515991210938)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(215.0507049560547, 5.920003414154053, -125.46469116210938), [4] = Vector3.new(184.5655059814453, 228.0289306640625, -157.428466796875)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(216.75341796875, 4.200573921203613, -171.5404815673828), [4] = Vector3.new(187.01364135742188, 22.802663803100586, -212.01278686523438)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(226.39547729492188, 3.681288242340088, -215.52847290039062), [4] = Vector3.new(267.16473388671875, 12.304887771606445, -289.27252197265625)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(289.66241455078125, 3.6694560050964355, -219.0732421875), [4] = Vector3.new(324.7108459472656, 7.9877448081970215, -219.06170654296875)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(359.028076171875, 3.6942977905273438, -202.0592041015625), [4] = Vector3.new(427.547119140625, 12.383111953735352, -243.68743896484375)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(387.6783447265625, 3.796376943588257, -229.65170288085938), [4] = Vector3.new(430.98931884765625, 15.600563049316406, -279.2987060546875)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(367.0774841308594, 3.8979978561401367, -212.19642639160156), [4] = Vector3.new(385.660888671875, 15.463701248168945, -258.3392333984375)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(372.2125244140625, 3.787266731262207, -193.12713623046875), [4] = Vector3.new(436.6592712402344, 12.445539474487305, -195.09393310546875)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(378.93450927734375, 3.592879056930542, -186.04310607910156), [4] = Vector3.new(437.9947204589844, 7.341453552246094, -213.1947021484375)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(370.779052734375, 4.18286657333374, -210.0006561279297), [4] = Vector3.new(367.50714111328125, 13.058692932128906, -183.24900817871094)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(325.48052978515625, 4.8344035148620605, -204.25970458984375), [4] = Vector3.new(302.8755798339844, 20.933258056640625, -206.33840942382812)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(312.6532287597656, 4.208272933959961, -192.99388122558594), [4] = Vector3.new(295.0404357910156, 11.788938522338867, -180.39097595214844)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(294.50372314453125, 4.597314357757568, -149.46250915527344), [4] = Vector3.new(276.1626892089844, 26.755096435546875, -116.76615905761719)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(278.26385498046875, 4.894931793212891, -112.54779052734375), [4] = Vector3.new(254.48281860351562, 98.654052734375, 16.979217529296875)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))local args = { [1] = "Generate", [2] = game:GetService("Players").LocalPlayer.Character.Taser, [3] = Vector3.new(225.7486114501953, 12.333763122558594, -188.09353637695312), [4] = Vector3.new(177.8989715576172, 178.7074737548828, -401.20281982421875)}
game:GetService("ReplicatedStorage"):WaitForChild("Tase"):FireServer(unpack(args))end
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

local Tab = Window:MakeTab({
	Name = "Private Guis",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--[[
Name = <string> - The name of the tab.
Icon = <string> - The icon of the tab.
PremiumOnly = <bool> - Makes the tab accessible to Sirus Premium users only.
]]

Tab:AddButton({
	Name = "Local player's GUI",
	Callback = function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/voidy434343/Zeouron-Mainiatic/main/Tlk%20prison%20obf.txt'))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - T
he function of the button.
]]

Tab:AddButton({
	Name = "mer TLK Panel",
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/CheaterMeralt/robloxscr/main/tlkScript.lua"))()
      		print("button pressed")
  	end    
})

--[[
Name = <string> - The name of the button.
Callback = <function> - The function of the button.
]]

OrionLib:Init()

