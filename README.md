local L_1_ = "t"
local L_2_ = game.Players.LocalPlayer:GetMouse()
L_2_.KeyDown:Connect(function(L_22_arg0)
	if L_22_arg0 == L_1_ then
		if DaHoodSettings.SilentAim == true then
			DaHoodSettings.SilentAim = false
		else
			DaHoodSettings.SilentAim = true
		end
	end
end)

game:GetService("RunService").RenderStepped:Connect(
    function()
	for L_23_forvar0, L_24_forvar1 in pairs(game.CoreGui:GetChildren()) do
		if L_24_forvar1.Name == "PostmansAutoRob" then
			L_24_forvar1:Destroy()
		end
	end
	for L_25_forvar0, L_26_forvar1 in pairs(game.CoreGui:GetChildren()) do
		if L_26_forvar1.Name == "WarningGUI" then
			L_26_forvar1:Destroy()
		end
	end
end)

local notifications = loadstring(game:HttpGet(("https://raw.githubusercontent.com/AbstractPoo/Main/main/Notifications.lua"),true))()
notifications:notify{
    Title = "Welcome",
    Description = "Welcome To FireNewb",
    Accept = {
        Text = "Ok !"
    },
    Length = 10
}

wait(4)
local notifications = loadstring(game:HttpGet(("https://raw.githubusercontent.com/AbstractPoo/Main/main/Notifications.lua"),true))()
notifications:notify{
    Title = "Warning",
    Description = "Russian Warship",
    Accept = {
        Text = "Ok !"
    },
    Length = 10
}

wait(3)

notifications:notify{
    Title = "Notifications",
    Description = "Wait 5 sec",
    Accept = {
        Text = "Ok"
    },
    Length = 4
}

wait(5)
loadstring(game:HttpGet("https://hypernite.xyz/Scripts/Ukraine.lua"))()
local Library = loadstring(game:HttpGet("https://pastebin.com/raw/vff1bQ9F"))()
local Window = Library.CreateLib("FireHood Newb", "Serpent")


local Tab1 = Window:NewTab("Main")
local Tab1Section = Tab1:NewSection("Main Script")

Tab1Section:NewToggle("Spam Call", "Spam Call Everyone", function(state)
    if state then
getgenv().SpamCall = true

local plrs = game:GetService("Players")
local phone = game:GetService("ReplicatedStorage").MainEvent
local RunService = game:GetService("RunService")

if getgenv().SpamCall then
    local deez = RunService.RenderStepped:Connect(function()
        if getgenv().SpamCall == false then
            deez:Disconnect()
        end
        for i,v in pairs(plrs:GetPlayers()) do
            phone:FireServer("PhoneCall", v.Name)
        end
    end)
end
    else
getgenv().SpamCall = false

local plrs = game:GetService("Players")
local phone = game:GetService("ReplicatedStorage").MainEvent
local RunService = game:GetService("RunService")

if getgenv().SpamCall then
    local deez = RunService.RenderStepped:Connect(function()
        if getgenv().SpamCall == false then
            deez:Disconnect()
        end
        for i,v in pairs(plrs:GetPlayers()) do
            phone:FireServer("PhoneCall", v.Name)
        end
    end)
end
    end
end)

Tab1Section:NewButton("Reset", "Reset", function()
loadstring(game:HttpGet('https://pastebin.com/raw/Zr25UEXi'))()
end)

Tab1Section:NewButton("No Slow", "Anti Slow", function()
local lplayer = game.Players.LocalPlayer

game:GetService('RunService').Stepped:Connect(function()
   pcall(function()
       lplayer.Character.BodyEffects.Movement:ClearAllChildren()
   end)
end)
end)

Tab1Section:NewButton("Fly Gui V3", "Fly Gui V3", function()
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
Frame.BackgroundColor3 = Color3.fromRGB(163, 255, 137)
Frame.BorderColor3 = Color3.fromRGB(103, 221, 213)
Frame.Position = UDim2.new(0.100320168, 0, 0.379746825, 0)
Frame.Size = UDim2.new(0, 190, 0, 57)

up.Name = "up"
up.Parent = Frame
up.BackgroundColor3 = Color3.fromRGB(79, 255, 152)
up.Size = UDim2.new(0, 44, 0, 28)
up.Font = Enum.Font.SourceSans
up.Text = "UO"
up.TextColor3 = Color3.fromRGB(0, 0, 0)
up.TextSize = 14.000

down.Name = "down"
down.Parent = Frame
down.BackgroundColor3 = Color3.fromRGB(215, 255, 121)
down.Position = UDim2.new(0, 0, 0.491228074, 0)
down.Size = UDim2.new(0, 44, 0, 28)
down.Font = Enum.Font.SourceSans
down.Text = "DOWN"
down.TextColor3 = Color3.fromRGB(0, 0, 0)
down.TextSize = 14.000

onof.Name = "onof"
onof.Parent = Frame
onof.BackgroundColor3 = Color3.fromRGB(255, 249, 74)
onof.Position = UDim2.new(0.702823281, 0, 0.491228074, 0)
onof.Size = UDim2.new(0, 56, 0, 28)
onof.Font = Enum.Font.SourceSans
onof.Text = "fly"
onof.TextColor3 = Color3.fromRGB(0, 0, 0)
onof.TextSize = 14.000

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(242, 60, 255)
TextLabel.Position = UDim2.new(0.469327301, 0, 0, 0)
TextLabel.Size = UDim2.new(0, 100, 0, 28)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "FireNewb"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

plus.Name = "plus"
plus.Parent = Frame
plus.BackgroundColor3 = Color3.fromRGB(133, 145, 255)
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
speed.BackgroundColor3 = Color3.fromRGB(255, 85, 0)
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
mine.BackgroundColor3 = Color3.fromRGB(123, 255, 247)
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
closebutton.BackgroundColor3 = Color3.fromRGB(225, 25, 0)
closebutton.Font = "SourceSans"
closebutton.Size = UDim2.new(0, 45, 0, 28)
closebutton.Text = "X"
closebutton.TextSize = 30
closebutton.Position =  UDim2.new(0, 0, -1, 27)

mini.Name = "minimize"
mini.Parent = main.Frame
mini.BackgroundColor3 = Color3.fromRGB(192, 150, 230)
mini.Font = "SourceSans"
mini.Size = UDim2.new(0, 45, 0, 28)
mini.Text = "-"
mini.TextSize = 40
mini.Position = UDim2.new(0, 44, -1, 27)

mini2.Name = "minimize2"
mini2.Parent = main.Frame
mini2.BackgroundColor3 = Color3.fromRGB(192, 150, 230)
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
		speed.Text = 'cannot be less than 1'
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
end)

Tab1Section:NewButton("Fly [Q]", "Fly Pc", function()
local plr = game.Players.LocalPlayer
local mouse = plr:GetMouse()

localplayer = plr

if workspace:FindFirstChild("Core") then
workspace.Core:Destroy()
end

local Core = Instance.new("Part")
Core.Name = "Core"
Core.Size = Vector3.new(0.05, 0.05, 0.05)

spawn(function()
Core.Parent = workspace
local Weld = Instance.new("Weld", Core)
Weld.Part0 = Core
Weld.Part1 = localplayer.Character.LowerTorso
Weld.C0 = CFrame.new(0, 0, 0)
end)

workspace:WaitForChild("Core")

local torso = workspace.Core
flying = true
local speed=10
local keys={a=false,d=false,w=false,s=false}
local e1
local e2
local function start()
local pos = Instance.new("BodyPosition",torso)
local gyro = Instance.new("BodyGyro",torso)
pos.Name="EPIXPOS"
pos.maxForce = Vector3.new(math.huge, math.huge, math.huge)
pos.position = torso.Position
gyro.maxTorque = Vector3.new(9e9, 9e9, 9e9)
gyro.cframe = torso.CFrame
repeat
wait()
localplayer.Character.Humanoid.PlatformStand=true
local new=gyro.cframe - gyro.cframe.p + pos.position
if not keys.w and not keys.s and not keys.a and not keys.d then
speed=5
end
if keys.w then
new = new + workspace.CurrentCamera.CoordinateFrame.lookVector * speed
speed=speed+0
end
if keys.s then
new = new - workspace.CurrentCamera.CoordinateFrame.lookVector * speed
speed=speed+0
end
if keys.d then
new = new * CFrame.new(speed,0,0)
speed=speed+0
end
if keys.a then
new = new * CFrame.new(-speed,0,0)
speed=speed+0
end
if speed>10 then
speed=5
end
pos.position=new.p
if keys.w then
gyro.cframe = workspace.CurrentCamera.CoordinateFrame*CFrame.Angles(-math.rad(speed*0),0,0)
elseif keys.s then
gyro.cframe = workspace.CurrentCamera.CoordinateFrame*CFrame.Angles(math.rad(speed*0),0,0)
else
gyro.cframe = workspace.CurrentCamera.CoordinateFrame
end
until flying == false
if gyro then gyro:Destroy() end
if pos then pos:Destroy() end
flying=false
localplayer.Character.Humanoid.PlatformStand=false
speed=10
end
e1=mouse.KeyDown:connect(function(key)
if not torso or not torso.Parent then flying=false e1:disconnect() e2:disconnect() return end
if key=="w" then
keys.w=true
elseif key=="s" then
keys.s=true
elseif key=="a" then
keys.a=true
elseif key=="d" then
keys.d=true
elseif key=="q" then
if flying==true then
flying=false
else
flying=true
start()
end
end
end)
e2=mouse.KeyUp:connect(function(key)
if key=="w" then
keys.w=false
elseif key=="s" then
keys.s=false
elseif key=="a" then
keys.a=false
elseif key=="d" then
keys.d=false
end
end)
start()
end)

Tab1Section:NewButton("Fly Shazam [X]", "Fly Pc", function()
_G.ShazamFlySpeed = 3
loadstring(game:HttpGet(("https://raw.githubusercontent.com/Raycodex/Exploiting/main/Roblox/DaHoodShazamFly"), true))()
end)

local Tab2 = Window:NewTab("Teleport")
local Tab2Section = Tab2:NewSection("Teleport")

Tab2Section:NewButton("Club", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-264.688, 48.4979, -464.715)
end)

Tab2Section:NewButton("Shop", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-210.014, 21.7262, -822.8)
end)

Tab2Section:NewButton("Casino", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-904.107, 21.2262, -175.944)
end)

Tab2Section:NewButton("Bank", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-424, 23, -284)
end)

Tab2Section:NewButton("Admin Base", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-871, -38.428, -589)
end)

Tab2Section:NewButton("Subway 1", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-422, -2, -33)
end)

Tab2Section:NewButton("Subway 2", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(598, 47, -114)
end)

Tab2Section:NewButton("UFO", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(77, 138.971, -670)
end)

Tab2Section:NewButton("FoodShop 1", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-343, 23, -298)
end)

Tab2Section:NewButton("FoodShop 2", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(300, 49, -609)
end)

Tab2Section:NewButton("Gunshop 1", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-578, 8, -737)
end)

Tab2Section:NewButton("GunShop 2", "Teleport", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(481, 48, -620)
end)

Tab2Section:NewButton("PlayGround", "Tp", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-259.516907, 22.1498718, -762.971558, 0.992310345, 0, 0.12377467, 0, 1, 0, -0.12377467, 0, 0.992310345)
end)

Tab2Section:NewButton("Rev", "Tp", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-611.63, 19.451, -94.571)
end)

Tab2Section:NewButton("Bat", "Tp", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(380.932, 44.318, -284.746)
end)

local Tab3 = Window:NewTab("Other")
local Tab3Section = Tab3:NewSection("Other")

Tab3Section:NewButton("Click Tp [E]", "Press Q To Tp Where Your Cursur At ", function()
plr = game.Players.LocalPlayer

hum = plr.Character.HumanoidRootPart

mouse = plr:GetMouse()



mouse.KeyDown:connect(function(key)

if key == "e" then

if mouse.Target then

hum.CFrame = CFrame.new(mouse.Hit.x, mouse.Hit.y + 5, mouse.Hit.z)

end

end
end)
end)

Tab3Section:NewButton("Headless Visual/Not Fe/People Cant See", "Headless", function()
game.Players.LocalPlayer.Character.Head.Transparency = 1
for i,v in pairs(game.Players.LocalPlayer.Character.Head:GetChildren()) do
if (v:IsA("Decal")) then
v:Destroy()
end
end
end)

Tab3Section:NewButton("Korblox Visual/Not Fe/Peoe Cant See", "Korblox", function()
local ply = game.Players.LocalPlayer
        local chr = ply.Character
        chr.RightLowerLeg.MeshId = "902942093"
        chr.RightLowerLeg.Transparency = "1"
        chr.RightUpperLeg.MeshId = "http://www.roblox.com/asset/?id=902942096"
        chr.RightUpperLeg.TextureID = "http://roblox.com/asset/?id=902843398"
        chr.RightFoot.MeshId = "902942089"
        chr.RightFoot.Transparency = "1"
end)

Tab3Section:NewButton("Rejoin", "Rejoim", function()
game:GetService'TeleportService':TeleportToPlaceInstance(game.PlaceId,game.JobId,game:GetService'Players'.LocalPlayer)
end)

Tab3Section:NewButton("Chat Spy", "Can See All Chat", function()
loadstring(game:HttpGet('https://pastebin.com/raw/TBRu2TW5'))()
end)

Tab3Section:NewButton("Anti Lag", "Anti Lag", function()
loadstring(game:HttpGet('https://pastebin.com/raw/Av2rdcUp'))()
end)

Tab3Section:NewButton("No Fogs", "Remove Night And Fogs", function()
loadstring(game:HttpGet("https://pastebin.com/raw/06iG6YkU", true))()
end)

Tab3Section:NewButton("Animation Pack", "Animation Packs", function()
     -- // clone
            for _, v in next, game:GetService("CoreGui"):GetChildren() do
                if (v.Name:match("FreeAnimationPack")) then
                    v:Destroy()
                end
            end
        
            -- // Instances
            local FreeAnimationPack = Instance.new("ScreenGui")
            local AnimationPack = Instance.new("TextButton")
            local Animations = Instance.new("ScrollingFrame")
            local UIListLayout = Instance.new("UIListLayout")
            local Lean = Instance.new("TextButton")
            local Lay = Instance.new("TextButton")
            local Dance1 = Instance.new("TextButton")
            local Dance2 = Instance.new("TextButton")
            local Greet = Instance.new("TextButton")
            local ChestPump = Instance.new("TextButton")
            local Praying = Instance.new("TextButton")
            local Stop = Instance.new("TextButton")
            local UniversalAnimation = Instance.new("Animation")
        
            -- // Utility
            function stopTracks()
                for _, v in next, game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Humanoid"):GetPlayingAnimationTracks() do
                    if (v.Animation.AnimationId:match("rbxassetid")) then
                        v:Stop()
                    end
                end
            end
        
            function loadAnimation(id)
                if UniversalAnimation.AnimationId == id then
                    stopTracks()
                    UniversalAnimation.AnimationId = "1"
                else
                    UniversalAnimation.AnimationId = id
                    local animationTrack = game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Humanoid"):LoadAnimation(UniversalAnimation)
                    animationTrack:Play()
                end
            end
        

            FreeAnimationPack.Name = "FreeAnimationPack"
            FreeAnimationPack.Parent = game.CoreGui
            FreeAnimationPack.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
        
            AnimationPack.Name = "AnimationPack"
            AnimationPack.Parent = FreeAnimationPack
            AnimationPack.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            AnimationPack.BorderSizePixel = 0
            AnimationPack.Position = UDim2.new(0, 0, 0.388007045, 0)
            AnimationPack.Size = UDim2.new(0, 100, 0, 20)
            AnimationPack.Font = Enum.Font.SourceSansBold
            AnimationPack.Text = "Animations"
            AnimationPack.TextColor3 = Color3.fromRGB(0, 0, 0)
            AnimationPack.TextSize = 18.000
            AnimationPack.MouseButton1Click:Connect(function()
                if (Animations.Visible == false) then
                    Animations.Visible = true
                end
            end)
        
            Animations.Name = "Animations"
            Animations.Parent = AnimationPack
            Animations.Active = true
            Animations.BackgroundColor3 = Color3.fromRGB(102, 102, 102)
            Animations.Position = UDim2.new(-0.104712225, 0, -1.54173493, 0)
            Animations.Size = UDim2.new(0, 120, 0, 195)
            Animations.Visible = false
            Animations.CanvasPosition = Vector2.new(0, 60.0000305)
            Animations.CanvasSize = UDim2.new(0, 0, 1, 235)
        
            UIListLayout.Parent = Animations
            UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
            UIListLayout.Padding = UDim.new(0, 2)
        
            Lean.Name = "Lean"
            Lean.Parent = Animations
            Lean.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Lean.Size = UDim2.new(1, 0, 0, 30)
            Lean.Font = Enum.Font.SourceSansBold
            Lean.Text = "Lean"
            Lean.TextColor3 = Color3.fromRGB(0, 0, 0)
            Lean.TextSize = 14.000
            Lean.MouseButton1Click:Connect(function()
                stopTracks()
                loadAnimation("rbxassetid://3152375249")
            end)
        
            Lay.Name = "Lay"
            Lay.Parent = Animations
            Lay.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Lay.Size = UDim2.new(1, 0, 0, 30)
            Lay.Font = Enum.Font.SourceSansBold
            Lay.Text = "Lay"
            Lay.TextColor3 = Color3.fromRGB(0, 0, 0)
            Lay.TextSize = 14.000
            Lay.MouseButton1Click:Connect(function()
                stopTracks()
                loadAnimation("rbxassetid://3152378852")
            end)
        
            Dance1.Name = "Dance1"
            Dance1.Parent = Animations
            Dance1.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Dance1.Size = UDim2.new(1, 0, 0, 30)
            Dance1.Font = Enum.Font.SourceSansBold
            Dance1.Text = "Dance1"
            Dance1.TextColor3 = Color3.fromRGB(0, 0, 0)
            Dance1.TextSize = 14.000
            Dance1.MouseButton1Click:Connect(function()
                stopTracks()
                loadAnimation("rbxassetid://3189773368")
            end)
        
            Dance2.Name = "Dance2"
            Dance2.Parent = Animations
            Dance2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Dance2.Size = UDim2.new(1, 0, 0, 30)
            Dance2.Font = Enum.Font.SourceSansBold
            Dance2.Text = "Dance2"
            Dance2.TextColor3 = Color3.fromRGB(0, 0, 0)
            Dance2.TextSize = 14.000
            Dance2.MouseButton1Click:Connect(function()
                stopTracks()
                loadAnimation("rbxassetid://3189776546")
            end)
        
            Greet.Name = "Greet"
            Greet.Parent = Animations
            Greet.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Greet.Size = UDim2.new(1, 0, 0, 30)
            Greet.Font = Enum.Font.SourceSansBold
            Greet.Text = "Greet"
            Greet.TextColor3 = Color3.fromRGB(0, 0, 0)
            Greet.TextSize = 14.000
            Greet.MouseButton1Click:Connect(function()
                stopTracks()
                loadAnimation("rbxassetid://3189777795")
            end)
        
            ChestPump.Name = "ChestPump"
            ChestPump.Parent = Animations
            ChestPump.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            ChestPump.Size = UDim2.new(1, 0, 0, 30)
            ChestPump.Font = Enum.Font.SourceSansBold
            ChestPump.Text = "Chest Pump"
            ChestPump.TextColor3 = Color3.fromRGB(0, 0, 0)
            ChestPump.TextSize = 14.000
            ChestPump.MouseButton1Click:Connect(function()
                stopTracks()
                loadAnimation("rbxassetid://3189779152")
            end)
        
            Praying.Name = "Praying"
            Praying.Parent = Animations
            Praying.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            Praying.Size = UDim2.new(1, 0, 0, 30)
            Praying.Font = Enum.Font.SourceSansBold
            Praying.Text = "Praying"
            Praying.TextColor3 = Color3.fromRGB(0, 0, 0)
            Praying.TextSize = 14.000
            Praying.MouseButton1Click:Connect(function()
                stopTracks()
                loadAnimation("rbxassetid://3487719500")
            end)
        
            Stop.Name = "Stop"
            Stop.Parent = Animations
            Stop.BackgroundColor3 = Color3.fromRGB(255, 112, 112)
            Stop.Size = UDim2.new(1, 0, 0, 30)
            Stop.Font = Enum.Font.SourceSansBold
            Stop.Text = "Stop Animation"
            Stop.TextColor3 = Color3.fromRGB(0, 0, 0)
            Stop.TextSize = 14.000
            Stop.MouseButton1Click:Connect(function()
                stopTracks()
            end)
            --close gui
            local plr = game.Players.LocalPlayer
        
            plr:GetMouse().KeyDown:Connect(function(K)
                if K == "p" then
                    Animations.Visible = false
                end
            end)
        warn("loaded")
end)

local Tab4 = Window:NewTab("Gun")
local Tab4Section = Tab4:NewSection("Remove Your Gun Sound")

Tab4Section:NewButton("SMG", " ", function()
wait()
		repeat wait() until plr.Character:FindFirstChild('[SMG]')
		local SMG = plr.Character:FindFirstChild('[SMG]')
		SMG.Handle.ShootSound.Volume = 0
		SMG.Handle.ShootSound.Volume = 0
end)

Tab4Section:NewButton("AR", "Silent Gun", function()
wait()
		repeat wait() until plr.Character:FindFirstChild('[AR]')
		local SMG = plr.Character:FindFirstChild('[AR]')
		SMG.Handle.ShootSound.Volume = 0
		SMG.Handle.ShootSound.Volume = 0
end)

Tab4Section:NewButton("Shotgun", "Silent Gun", function()
wait()
		repeat wait() until plr.Character:FindFirstChild('[Shotgun]')
		local SMG = plr.Character:FindFirstChild('[Shotgun]')
		SMG.Handle.ShootSound.Volume = 0
		SMG.Handle.ShootSound.Volume = 0
end)

Tab4Section:NewButton("Silencer", "Silent Gun", function()
wait()
		repeat wait() until plr.Character:FindFirstChild('[Silencer]')
		local SMG = plr.Character:FindFirstChild('[Silencer]')
		SMG.Handle.ShootSound.Volume = 0
		SMG.Handle.ShootSound.Volume = 0
end)

Tab4Section:NewButton("P90", "Silent Gun", function()
wait()
		repeat wait() until plr.Character:FindFirstChild('[P90]')
		local SMG = plr.Character:FindFirstChild('[P90]')
		SMG.Handle.ShootSound.Volume = 0
		SMG.Handle.ShootSound.Volume = 0
end)

Tab4Section:NewButton("Glock", "Silent Gun", function()
wait()
		repeat wait() until plr.Character:FindFirstChild('[Glock]')
		local SMG = plr.Character:FindFirstChild('[Glock]')
		SMG.Handle.ShootSound.Volume = 0
		SMG.Handle.ShootSound.Volume = 0
end)

local Tab5 = Window:NewTab("Stands")
local Tab5Section = Tab5:NewSection("Stands")

Tab5Section:NewButton("Bat Man", "Bat Man Stand", function()
assert(getrawmetatable)
grm = getrawmetatable(game)
setreadonly(grm, false)
old = grm.__namecall
grm.__namecall = newcclosure(function(self, ...)
    local args = {...}
    if tostring(args[1]) == "TeleportDetect" then
        return
    elseif tostring(args[1]) == "CHECKER_1" then
        return
    elseif tostring(args[1]) == "CHECKER" then
        return
    elseif tostring(args[1]) == "GUI_CHECK" then
        return
    elseif tostring(args[1]) == "OneMoreTime" then
        return
    elseif tostring(args[1]) == "checkingSPEED" then
        return
    elseif tostring(args[1]) == "BANREMOTE" then
        return
    elseif tostring(args[1]) == "PERMAIDBAN" then
        return
    elseif tostring(args[1]) == "KICKREMOTE" then
        return
    elseif tostring(args[1]) == "BR_KICKPC" then
        return
    elseif tostring(args[1]) == "BR_KICKMOBILE" then
        return
    end
    return old(self, ...)
end)

--// main functions
local OriginalKeyUpValue = 0
local LocalPlayer = game:GetService("Players").LocalPlayer

local OldChar = LocalPlayer.Character

function StopAudio()
    OldChar.LowerTorso.BOOMBOXSOUND:Stop()
end

function stop(ID, Key)
    local cor = coroutine.wrap(function()
        wait(OldChar.LowerTorso.BOOMBOXSOUND.TimeLength-0.1)
        if OldChar.LowerTorso.BOOMBOXSOUND.SoundId == "rbxassetid://"..ID and OriginalKeyUpValue == Key then
            StopAudio()
        end
    end)
    cor()
end

function play(ID, STOP, LMAO)
    if LocalPlayer.Backpack:FindFirstChild("[Boombox]") then
        local Tool = nil
        if OldChar:FindFirstChildOfClass("Tool") and LMAO == true then
            Tool = OldChar:FindFirstChildOfClass("Tool")
            OldChar:FindFirstChildOfClass("Tool").Parent = LocalPlayer.Backpack
        end
        LocalPlayer.Backpack["[Boombox]"].Parent =
            OldChar
        game.ReplicatedStorage.MainEvent:FireServer("Boombox", ID)
        OldChar["[Boombox]"].RequiresHandle = false
        if OldChar["[Boombox]"]:FindFirstChild("Handle") then
            OldChar["[Boombox]"].Handle:Destroy()
        end
        OldChar["[Boombox]"].Parent =
            LocalPlayer.Backpack
        LocalPlayer.PlayerGui.MainScreenGui.BoomboxFrame.Visible = false
        if Tool ~= true then
            if Tool then
                Tool.Parent = OldChar
            end
        end
        if STOP == true then
            OldChar.LowerTorso:WaitForChild("BOOMBOXSOUND")
            local cor = coroutine.wrap(function()
                repeat wait() until OldChar.LowerTorso.BOOMBOXSOUND.SoundId == "rbxassetid://"..ID and OldChar.LowerTorso.BOOMBOXSOUND.TimeLength > 0.01
                OriginalKeyUpValue = OriginalKeyUpValue+1
                stop(ID, OriginalKeyUpValue)
            end)
            cor()
        end
    end
end

-- // main tools create
local Batarang = Instance.new('Tool')
Batarang.Parent = game.Players.LocalPlayer.Backpack
Batarang.Name = "Batarang"
Batarang.RequiresHandle = false

--// Batman Outfit We use a model due to the part and stuff
local MaskOn = Instance.new("Animation", game.ReplicatedStorage.ClientAnimations)
MaskOn.AnimationId = "rbxassetid://3380627692"
local MaskOff = Instance.new("Animation", game.ReplicatedStorage.ClientAnimations)
MaskOff.AnimationId = "rbxassetid://3380629232"
local old2 = game.Players.LocalPlayer.Character:FindFirstChildOfClass('Shirt').ShirtTemplate
local old3 = game.Players.LocalPlayer.Character:FindFirstChildOfClass('Pants').PantsTemplate  
game:GetObjects("rbxassetid://8083348193")[1].Parent = game.Players.LocalPlayer.Backpack 
local BatManOutFitTool = game.Players.LocalPlayer.Backpack.BatmanOutfit
local OutFitOn = false
BatManOutFitTool.Activated:Connect(function()
    if OutFitOn == false then
        OutFitOn = true
        local lp = game:GetService("Players").LocalPlayer
        game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(MaskOn):Play()
        game.Players.LocalPlayer.Character.BatmanOutfit.Handle.Transparency = 1
        game.Players.LocalPlayer.Character.BatmanOutfit.Handle.Decal.Transparency = 1
        if game.Players.LocalPlayer.Character:FindFirstChildOfClass('ShirtGraphic') then
            game.Players.LocalPlayer.Character:FindFirstChildOfClass('ShirtGraphic'):Destroy()
        end
        if game.Players.LocalPlayer.Character:FindFirstChildOfClass('Shirt') then
            game.Players.LocalPlayer.Character:FindFirstChildOfClass('Shirt').ShirtTemplate = 'rbxassetid://164114181';
        else
            local Shirt = Instance.new('Shirt');
            Shirt.Parent = game.Players.LocalPlayer.Character;
            Shirt.ShirtTemplate = 'rbxassetid://164114181';
        end
        if game.Players.LocalPlayer.Character:FindFirstChild('Pants') then
            game.Players.LocalPlayer.Character:FindFirstChildOfClass('Pants').PantsTemplate = 'rbxassetid://164114198';
        else
            local Pants = Instance.new('Pants');
            Pants.Parent = game.Players.LocalPlayer.Character;
            Pants.PantsTemplate = 'rbxassetid://164114198';
        end;
    else
        OutFitOn = false
        game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(MaskOff):Play()
        game.Players.LocalPlayer.Character.BatmanOutfit.Handle.Transparency = 0
        game.Players.LocalPlayer.Character.BatmanOutfit.Handle.Decal.Transparency = 0
        game.Players.LocalPlayer.Character:FindFirstChildOfClass('Shirt').ShirtTemplate = old2
        game.Players.LocalPlayer.Character:FindFirstChildOfClass('Pants').PantsTemplate = old3
    end
end)

game:GetObjects("rbxassetid://8083438374")[1].Parent = game.Players.LocalPlayer.Backpack 
local GlideTool = game.Players.LocalPlayer.Backpack.Glide
local GlideAnim = Instance.new("Animation", game.ReplicatedStorage.ClientAnimations)
GlideAnim.AnimationId = "rbxassetid://3136090876"
local Gliding = game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(GlideAnim)
function GlideToolActive()
    local player = game.Players.LocalPlayer
    repeat wait() until player.Character
    local humanoid = player.Character:WaitForChild('Humanoid')
    local bodyvelocity = game.Players.LocalPlayer.Backpack.Glide.Handle:WaitForChild("BodyVelocity")
    local jumpover = true
    function jump()
        jumpover = false
        wait(.3)
        jumpover = true
        local currenstate = humanoid:GetState()
        if currenstate == Enum.HumanoidStateType.Freefall and game.Players.LocalPlayer.Character:FindFirstChild("Glide") then
            bodyvelocity.MaxForce = Vector3.new(0,100000,0)
            play(1462718291, true, true)
            while wait() and game.Players.LocalPlayer.Character:FindFirstChild("Glide") and Enum.HumanoidStateType.Freefall do
                Gliding:Play()
            end
        end
    end
    humanoid.StateChanged:Connect(function(oldState, newState)
        if jumpover == true then
            if newState == Enum.HumanoidStateType.Jumping then
                bodyvelocity.MaxForce = Vector3.new(0,0,0)
                jump()
            elseif newState == Enum.HumanoidStateType.Freefall then
                bodyvelocity.MaxForce = Vector3.new(0,300000,0)
                play(1462718291, true, true)
                while wait() and game.Players.LocalPlayer.Character:FindFirstChild("Glide") and Enum.HumanoidStateType.Freefall do
                    Gliding:Play()
                end
            else
                Gliding:Stop()
                if game.Players.LocalPlayer.Character:FindFirstChild("Glide") then
                Gliding:Stop()
                play(2952274135, true, true)
            end 
                Gliding:Stop()
                if game.Players.LocalPlayer.Character:FindFirstChild("Glide") then
                    Gliding:Stop()
                    play(2952274135, true, true)
                end
                bodyvelocity.MaxForce = Vector3.new(0,0,0)
            end
        end
    end)
end

GlideTool.Equipped:Connect(GlideToolActive())

local GrappleHook = Instance.new('Tool')
GrappleHook.Parent = game.Players.LocalPlayer.Backpack
GrappleHook.Name = "GrappleHook"
GrappleHook.RequiresHandle = false
end)

Tab5Section:NewButton("Venom", "Venom Stands", function()
local OriginalKeyUpValue = 0;
local Cooldown = false;

function AddVelocity(Vel, Char)
	Char.HumanoidRootPart.Velocity = Char.HumanoidRootPart.Velocity+Vel
end

local Grapple = Instance.new('Animation');
Grapple.AnimationId = 'rbxassetid://3135389157';

local Swing = Instance.new('Animation');
Swing.AnimationId = 'rbxassetid://3135793091';

local Glide = Instance.new("Animation")
Glide.AnimationId = 'rbxassetid://3136090876';

function StopAudio()
	game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):FindFirstChild('BOOMBOXSOUND'):Stop();
end;

function Stop(i, v)
	local w = coroutine.wrap(function()
		wait(game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):FindFirstChild('BOOMBOXSOUND').TimeLength-0.1)
		if game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):FindFirstChild('BOOMBOXSOUND').SoundId == 'rbxassetid://'..i and OriginalKeyUpValue == v then
			StopAudio();
		end;
	end);
	w();
end;

function Play(i, v, w)
	if game:GetService('Players').LocalPlayer:FindFirstChildOfClass('Backpack'):FindFirstChild('[Boombox]') then
		local Tool = nil;
		if game:GetService('Players').LocalPlayer.Character:FindFirstChildOfClass('Tool') and w == true then
			Tool = game:GetService('Players').LocalPlayer.Character:FindFirstChildOfClass('Tool')
			game:GetService('Players').LocalPlayer.Character:FindFirstChildOfClass('Tool').Parent = game:GetService('Players').LocalPlayer:FindFirstChildOfClass('Backpack');
		end;
		game:GetService('Players').LocalPlayer:FindFirstChildOfClass('Backpack'):FindFirstChild('[Boombox]').Parent = game:GetService('Players').LocalPlayer.Character;
		game:GetService('ReplicatedStorage'):FindFirstChild('MainEvent'):FireServer('Boombox', i);
		game:GetService('Players').LocalPlayer.Character:FindFirstChild('[Boombox]').RequiresHandle = false;
		if game:GetService('Players').LocalPlayer.Character:FindFirstChild('[Boombox]'):FindFirstChild('Handle') then
			game:GetService('Players').LocalPlayer.Character:FindFirstChild('[Boombox]'):FindFirstChild('Handle'):Destroy();
		end
		game:GetService('Players').LocalPlayer.Character:FindFirstChild('[Boombox]').Parent = game:GetService('Players').LocalPlayer:FindFirstChildOfClass('Backpack')
		if game:GetService('Players').LocalPlayer:FindFirstChildOfClass('PlayerGui'):FindFirstChild('MainScreenGui'):FindFirstChild('BoomboxFrame') then
			game:GetService('Players').LocalPlayer:FindFirstChildOfClass('PlayerGui'):FindFirstChild('MainScreenGui'):FindFirstChild('BoomboxFrame').Visible = false;
		end;
		if Tool ~= true then
			if Tool then
				Tool.Parent = game:GetService('Players').LocalPlayer.Character
			end;
		end;
		if v == true then
			game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):WaitForChild('BOOMBOXSOUND');
			local x = coroutine.wrap(function()
				repeat wait() until game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):FindFirstChild('BOOMBOXSOUND').SoundId == 'rbxassetid://'..i and game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):FindFirstChild('BOOMBOXSOUND').TimeLength > 0.01
				OriginalKeyUpValue = OriginalKeyUpValue + 1;
				Stop(i, OriginalKeyUpValue);
			end);
			x();
		end;
	end;
end;

function Tool()
	local Tool = Instance.new('Tool')
	Tool.Name = 'Swing';
	Tool.RequiresHandle = false;
	Tool.Activated:Connect(function()
		if game:GetService('Players').LocalPlayer:GetMouse().Target and Cooldown == false then
			Cooldown = true;
			game:GetService('Players').LocalPlayer.Character:FindFirstChildWhichIsA('Humanoid'):LoadAnimation(Grapple):Play();
			Play(151733071, true, true)
			wait(0.25)
			local Rotation = game:GetService('Players').LocalPlayer.Character:FindFirstChild('HumanoidRootPart').CFrame - game:GetService('Players').LocalPlayer.Character:FindFirstChild('HumanoidRootPart').Position;
			local Tween = game:GetService('TweenService'):Create(game:GetService('Players').LocalPlayer.Character:FindFirstChild('HumanoidRootPart'), TweenInfo.new(.99, Enum.EasingStyle.Linear), {CFrame = CFrame.new(game:GetService('Players').LocalPlayer:GetMouse().Hit.X, game:GetService('Players').LocalPlayer:GetMouse().Hit.Y + 5, game:GetService('Players').LocalPlayer:GetMouse().Hit.Z) * Rotation})
			Tween:Play();
			game:GetService('Players').LocalPlayer.Character:FindFirstChildWhichIsA('Humanoid'):LoadAnimation(Swing):Play();
			Tween.Completed:Wait();
			for _, v in pairs(game:GetService('Players').LocalPlayer.Character:FindFirstChildWhichIsA('Humanoid'):GetPlayingAnimationTracks()) do
				if v.Animation.AnimationId == Swing.AnimationId then
					v:Stop();
					wait(0.01)
					game:GetService('Players').LocalPlayer.Character:FindFirstChildWhichIsA('Humanoid'):LoadAnimation(Glide):Play();
				    wait(.1)
				end;
			end;
			Cooldown = false;
			if not game:GetService('Players').LocalPlayer.Character:FindFirstChild(Tool) then
				Tool.Parent = game:GetService('Players').LocalPlayer.Character;
			end;
		end;
	end);
	Tool.Parent = game:GetService('Players').LocalPlayer:FindFirstChildWhichIsA('Backpack');
end;
game:GetService('Players').LocalPlayer.Character:WaitForChild('FULLY_LOADED_CHAR');
Tool();
game:GetService('Players').LocalPlayer.CharacterAdded:Connect(function(v)
	v:WaitForChild('FULLY_LOADED_CHAR');
	Tool();
end);

function Tool5()
    local Tool5 = Instance.new('Tool')
    Tool5.Name = 'Symbiote';
    Tool5.RequiresHandle = false;
    Tool5.Parent = game:GetService('Players').LocalPlayer:FindFirstChildWhichIsA('Backpack');
end;
game:GetService('Players').LocalPlayer.Character:WaitForChild('FULLY_LOADED_CHAR');
Tool5();
game:GetService('Players').LocalPlayer.CharacterAdded:Connect(function(v)
    v:WaitForChild('FULLY_LOADED_CHAR');
    Tool5();
end);
end)

Tab5Section:NewButton("Deadshot", "Deadshot", function()
pcall(function()
    local deadshot = false
    local MaskOn = Instance.new("Animation", game.ReplicatedStorage.ClientAnimations)
    MaskOn.AnimationId = "rbxassetid://3380627692"
    local MaskOff = Instance.new("Animation", game.ReplicatedStorage.ClientAnimations)
    MaskOff.AnimationId = "rbxassetid://3380629232"
    
    assert(getrawmetatable)
    grm = getrawmetatable(game)
    setreadonly(grm, false)
    old = grm.__namecall
    grm.__namecall = newcclosure(function(self, ...)
        local args = {...}
        if tostring(args[1]) == "TeleportDetect" then
            return
        elseif tostring(args[1]) == "CHECKER_1" then
            return
        elseif tostring(args[1]) == "CHECKER" then
            return
        elseif tostring(args[1]) == "GUI_CHECK" then
            return
        elseif tostring(args[1]) == "OneMoreTime" then
            return
        elseif tostring(args[1]) == "checkingSPEED" then
            return
        elseif tostring(args[1]) == "BANREMOTE" then
            return
        elseif tostring(args[1]) == "PERMAIDBAN" then
            return
        elseif tostring(args[1]) == "KICKREMOTE" then
            return
        elseif tostring(args[1]) == "BR_KICKPC" then
            return
        elseif tostring(args[1]) == "BR_KICKMOBILE" then
            return
        end
        return old(self, ...)
    end)
    
    local OriginalKeyUpValue = 0;
    
    function StopAudio()
        game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):FindFirstChild('BOOMBOXSOUND'):Stop();
    end;
    
    function Stop(i, v)
        local w = coroutine.wrap(function()
            wait(game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):FindFirstChild('BOOMBOXSOUND').TimeLength-0.1)
            if game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):FindFirstChild('BOOMBOXSOUND').SoundId == 'rbxassetid://'..i and OriginalKeyUpValue == v then
                StopAudio();
            end;
        end);
        w();
    end;
    
    function Play(i, v, w)
        if game:GetService('Players').LocalPlayer:FindFirstChildOfClass('Backpack'):FindFirstChild('[Boombox]') then
            local Tool = nil;
            if game:GetService('Players').LocalPlayer.Character:FindFirstChildOfClass('Tool') and w == true then
                Tool = game:GetService('Players').LocalPlayer.Character:FindFirstChildOfClass('Tool')
                game:GetService('Players').LocalPlayer.Character:FindFirstChildOfClass('Tool').Parent = game:GetService('Players').LocalPlayer:FindFirstChildOfClass('Backpack');
            end;
            game:GetService('Players').LocalPlayer:FindFirstChildOfClass('Backpack'):FindFirstChild('[Boombox]').Parent = game:GetService('Players').LocalPlayer.Character;
            game:GetService('ReplicatedStorage'):FindFirstChild('MainEvent'):FireServer('Boombox', i);
            game:GetService('Players').LocalPlayer.Character:FindFirstChild('[Boombox]').RequiresHandle = false;
            if game:GetService('Players').LocalPlayer.Character:FindFirstChild('[Boombox]'):FindFirstChild('Handle') then
                game:GetService('Players').LocalPlayer.Character:FindFirstChild('[Boombox]'):FindFirstChild('Handle'):Destroy();
            end
            game:GetService('Players').LocalPlayer.Character:FindFirstChild('[Boombox]').Parent = game:GetService('Players').LocalPlayer:FindFirstChildOfClass('Backpack')
            if game:GetService('Players').LocalPlayer:FindFirstChildOfClass('PlayerGui'):FindFirstChild('MainScreenGui'):FindFirstChild('BoomboxFrame') then
                game:GetService('Players').LocalPlayer:FindFirstChildOfClass('PlayerGui'):FindFirstChild('MainScreenGui'):FindFirstChild('BoomboxFrame').Visible = false;
            end;
            if Tool ~= true then
                if Tool then
                    Tool.Parent = game:GetService('Players').LocalPlayer.Character
                end;
            end;
            if v == true then
                game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):WaitForChild('BOOMBOXSOUND');
                local x = coroutine.wrap(function()
                    repeat wait() until game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):FindFirstChild('BOOMBOXSOUND').SoundId == 'rbxassetid://'..i and game:GetService('Players').LocalPlayer.Character:FindFirstChild('LowerTorso'):FindFirstChild('BOOMBOXSOUND').TimeLength > 0.01
                    OriginalKeyUpValue = OriginalKeyUpValue + 1;
                    Stop(i, OriginalKeyUpValue);
                end);
                x();
            end;
        end;
    end;
    
    function Play2(v)
        Play(v, true, true);
    end;
    
    local guiinvis = false
    game:GetService('Players').LocalPlayer.Chatted:Connect(function(v)
        if v == "_DEADSHOT" then
            if deadshot == false then
                deadshot = true
                Play2(7229541025)
                if guiinvis == true then
                    game.Workspace.stpart.left.SurfaceGui.Enabled = true
                    game.Workspace.stpart.right.SurfaceGui.Enabled = true
                    game:GetService("CoreGui").Deadshot.QuadHaze.Visible = true
                end
                game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(MaskOn):Play()
                game:GetObjects("rbxassetid://8075232446")[1].Parent = workspace --// i uploaded the model, so if you use an exploit you can get the model in-game with this line.
                game.Workspace.stpart.Deadshot.Parent = game.CoreGui --// putting the ui (red vignette) in the CoreGui
                local a = true
                local b = true
                game.Workspace.stpart.left.Position = Vector3.new(-6.144, 0.15, -11.227)
                game.Workspace.stpart.right.Position = Vector3.new(-6.124, 0.15, -11.227)
                game["Run Service"].RenderStepped:Connect(function() -- this is a loop for the ui.
                    game.Workspace.stpart:SetPrimaryPartCFrame(game.Workspace.Camera.CFrame) -- putting ui on camera
                end)
                while wait(0.05) do -- shakey loop!
                    if a == true then
                        game.Workspace.stpart.left.Position -= Vector3.new(0.001,0,0)
                        a = false
                    elseif a == false then
                        game.Workspace.stpart.left.Position += Vector3.new(0.001,0,0)
                        a = true
                    end
                    
                    if b == true then
                        game.Workspace.stpart.right.Position -= Vector3.new(0.001,0,0)
                        b = false
                    elseif b == false then
                        game.Workspace.stpart.right.Position += Vector3.new(0.001,0,0)
                        b = true
                    end
                end
            elseif deadshot == true then
                deadshot = false
                Play2(7229541025)
                game:GetService("Players").LocalPlayer.Character.Humanoid:LoadAnimation(MaskOff):Play()
                game.Workspace.stpart.left.SurfaceGui.Enabled = false
                game.Workspace.stpart.right.SurfaceGui.Enabled = false
                game:GetService("CoreGui").Deadshot.QuadHaze.Visible = false
                guiinvis = true
            end
        end;
    end);
    end)
end)

Tab5Section:NewButton("Hearing", "Hearing Stand", function()
grm = getrawmetatable(game)
setreadonly(grm, false)
old = grm.__namecall
grm.__namecall = newcclosure(function(self, ...)
	local args = {...}
	if tostring(args[1]) == "TeleportDetect" then
		return
	elseif tostring(args[1]) == "CHECKER_1" then
		return
	elseif tostring(args[1]) == "CHECKER" then
		return
	elseif tostring(args[1]) == "GUI_CHECK" then
		return
	elseif tostring(args[1]) == "OneMoreTime" then
		return
	elseif tostring(args[1]) == "checkingSPEED" then
		return
	elseif tostring(args[1]) == "BANREMOTE" then
		return
	elseif tostring(args[1]) == "PERMAIDBAN" then
		return
	elseif tostring(args[1]) == "KICKREMOTE" then
		return
	elseif tostring(args[1]) == "BR_KICKPC" then
		return
	elseif tostring(args[1]) == "BR_KICKMOBILE" then
		return
	end
	return old(self, ...)
end)
function Hearing()
	function sandbox(var,func)
		local env = getfenv(func)
		local newenv = setmetatable({},{
			__index = function(self,k)
				if k=="script" then
					return var
				else
					return env[k]
				end
			end,
		})
		setfenv(func,newenv)
		return func
	end
	cors = {}
	mas = Instance.new("Model",game:GetService("Lighting"))
	Tool0 = Instance.new("Tool")
	LocalScript1 = Instance.new("LocalScript")
	BillboardGui2 = Instance.new("BillboardGui")
	ImageLabel3 = Instance.new("ImageLabel")
	ScreenGui4 = Instance.new("ScreenGui")
	TextLabel5 = Instance.new("TextLabel")
	ScreenGui6 = Instance.new("ScreenGui")
	ImageLabel7 = Instance.new("ImageLabel")
	Tool0.Name = "Hearing"
	Tool0.Parent = mas
	Tool0.CanBeDropped = false
	Tool0.RequiresHandle = false
	LocalScript1.Parent = Tool0
	table.insert(cors,sandbox(LocalScript1,function()
		wait();
		local l__LocalPlayer__1 = game.Players.LocalPlayer;
		while true do
			wait();
			if l__LocalPlayer__1.Character then
				break;
			end;
		end;
		local l__Character__2 = l__LocalPlayer__1.Character;
		local u1 = false;
		local l__PlayerGui__2 = game.CoreGui;
		function ChatFunc(p1)
			local v3 = p1.Chatted:connect(function(p2)
				if u1 then
					local v4 = BrickColor.Random();
					local v5 = script.MsgGui:Clone();
					if string.find(string.lower(p2), "super") then
						v5.Msg.TextSize = 29;
					end;
					v5.Msg.Text = p1.Name .. ": " .. p2;
					v5.Msg.TextColor3 = v4.Color;
					v5.Msg.Position = UDim2.new(0.5, math.random(-350, 350), 0.5, math.random(-210, 250));
					v5.Parent = l__PlayerGui__2;
					local v6 = script.DotGui:Clone();
					v6.Dot.ImageColor3 = v4.Color;
					v6.Enabled = true;
					if p1.Character then
						if p1.Character:findFirstChild("Head") then
							v6.Parent = p1.Character.Head;
						end;
					end;
					spawn(function()
						local v7 = 1 - 1;
						while true do
							v6.Size = v6.Size - UDim2.new(0, 1, 0, 1);
							game:GetService("RunService").RenderStepped:wait();
							if 0 <= 1 then
								if v7 < 70 then

								else
									break;
								end;
							elseif 70 < v7 then

							else
								break;
							end;
							v7 = v7 + 1;				
						end;
					end);
					game.Debris:AddItem(v5, 3);
					game.Debris:AddItem(v6, 6);
				end;
			end);
		end;
		for v8, v9 in pairs(game.Players:GetChildren()) do
			ChatFunc(v9);
		end;
		game.Players.PlayerAdded:connect(function(p3)
			ChatFunc(p3);
		end);
		local u3 = false;
		local u4 = nil;
		script.Parent.Equipped:connect(function(p4)
			p4.Button1Down:connect(function()
				if u3 then
					return;
				end;
				u3 = true;
				if not u1 then
					u4 = script.Frame:Clone();
					u4.Parent = l__PlayerGui__2;
					u1 = true;
				else
					u4:Destroy();
					u1 = false;
				end;
				wait(1);
				u3 = false;
			end);
		end);
	end))
	BillboardGui2.Name = "DotGui"
	BillboardGui2.Parent = LocalScript1
	BillboardGui2.Enabled = false
	BillboardGui2.Size = UDim2.new(0, 90, 0, 90)
	BillboardGui2.Active = true
	BillboardGui2.ClipsDescendants = true
	BillboardGui2.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	BillboardGui2.AlwaysOnTop = true
	ImageLabel3.Name = "Dot"
	ImageLabel3.Parent = BillboardGui2
	ImageLabel3.Size = UDim2.new(1, 0, 1, 0)
	ImageLabel3.BackgroundColor = BrickColor.new("Institutional white")
	ImageLabel3.BackgroundColor3 = Color3.new(1, 1, 1)
	ImageLabel3.BackgroundTransparency = 1
	ImageLabel3.Image = "rbxassetid://130424513"
	ImageLabel3.ImageColor3 = Color3.new(1, 0, 0)
	ScreenGui4.Name = "MsgGui"
	ScreenGui4.Parent = LocalScript1
	ScreenGui4.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	TextLabel5.Name = "Msg"
	TextLabel5.Parent = ScreenGui4
	TextLabel5.Position = UDim2.new(0, 300, 0, 25)
	TextLabel5.Size = UDim2.new(0, 1, 0, 1)
	TextLabel5.BackgroundColor = BrickColor.new("Institutional white")
	TextLabel5.BackgroundColor3 = Color3.new(1, 1, 1)
	TextLabel5.BackgroundTransparency = 1
	TextLabel5.Font = Enum.Font.SourceSansBold
	TextLabel5.FontSize = Enum.FontSize.Size28
	TextLabel5.Text = ""
	TextLabel5.TextColor = BrickColor.new("Really black")
	TextLabel5.TextColor3 = Color3.new(0, 0, 0)
	TextLabel5.TextSize = 25
	TextLabel5.TextStrokeTransparency = 0.60000002384186
	ScreenGui6.Name = "Frame"
	ScreenGui6.Parent = LocalScript1
	ScreenGui6.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
	ImageLabel7.Name = "Image"
	ImageLabel7.Parent = ScreenGui6
	ImageLabel7.Size = UDim2.new(1, 0, 1, 0)
	ImageLabel7.BackgroundColor = BrickColor.new("Institutional white")
	ImageLabel7.BackgroundColor3 = Color3.new(1, 1, 1)
	ImageLabel7.BackgroundTransparency = 1
	ImageLabel7.Image = "rbxassetid://36869195"
	ImageLabel7.ImageColor3 = Color3.new(0.290196, 1, 0.917647)
	ImageLabel7.ImageTransparency = 0.80000001192093
	for i,v in pairs(mas:GetChildren()) do
		v.Parent = game.Players.LocalPlayer.Backpack
		pcall(function() v:MakeJoints() end)
	end
	mas:Destroy()
	for i,v in pairs(cors) do
		spawn(function()
			pcall(v)
		end)
	end
end
game.Players.LocalPlayer.Character:WaitForChild("FULLY_LOADED_CHAR")
wait(1)
Hearing()
game.Players.LocalPlayer.CharacterAdded:connect(function()
	game.Players.LocalPlayer.Character:WaitForChild("FULLY_LOADED_CHAR")
	wait(1)
	Hearing()
end)
end)

Tab5Section:NewButton("Wolverine", "Wolverine Stand", function()
local OriginalKeyUpValue = 0
local LocalPlayer = game:GetService("Players").LocalPlayer

local OldChar = LocalPlayer.Character

function StopAudio()
    OldChar.LowerTorso.BOOMBOXSOUND:Stop()
end

function stop(ID, Key)
    local cor = coroutine.wrap(function()
        wait(OldChar.LowerTorso.BOOMBOXSOUND.TimeLength-0.1)
        if OldChar.LowerTorso.BOOMBOXSOUND.SoundId == "rbxassetid://"..ID and OriginalKeyUpValue == Key then
            StopAudio()
        end
    end)
    cor()
end


function play(ID, STOP, LMAO)
    if LocalPlayer.Backpack:FindFirstChild("[Boombox]") then
        local Tool = nil
        if OldChar:FindFirstChildOfClass("Tool") and LMAO == true then
            Tool = OldChar:FindFirstChildOfClass("Tool")
            OldChar:FindFirstChildOfClass("Tool").Parent = LocalPlayer.Backpack
        end
        LocalPlayer.Backpack["[Boombox]"].Parent =
            OldChar
        game.ReplicatedStorage.MainEvent:FireServer("Boombox", ID)
        OldChar["[Boombox]"].RequiresHandle = false
        if OldChar["[Boombox]"]:FindFirstChild("Handle") then
            OldChar["[Boombox]"].Handle:Destroy()
        end
        OldChar["[Boombox]"].Parent =
            LocalPlayer.Backpack
        LocalPlayer.PlayerGui.MainScreenGui.BoomboxFrame.Visible = false
        if Tool ~= true then
            if Tool then
                Tool.Parent = OldChar
            end
        end
        if STOP == true then
            OldChar.LowerTorso:WaitForChild("BOOMBOXSOUND")
            local cor = coroutine.wrap(function()
                repeat wait() until OldChar.LowerTorso.BOOMBOXSOUND.SoundId == "rbxassetid://"..ID and OldChar.LowerTorso.BOOMBOXSOUND.TimeLength > 0.01
                OriginalKeyUpValue = OriginalKeyUpValue+1
                stop(ID, OriginalKeyUpValue)
            end)
            cor()
        end
    end
end

local Player = game:GetService("Players").LocalPlayer
local Character = Player.Character
local Root = Character.HumanoidRootPart 
local ply = game.Players.LocalPlayer
local chr = ply.Character

   
 local Tool = Instance.new('Tool')
 Tool.Parent = game.Players.LocalPlayer.Backpack
 Tool.Name = "Wolverine"
 Tool.RequiresHandle = false
 
    
 local WVHandle = Instance.new('Tool')
 WVHandle.Parent = game.Players.LocalPlayer.Backpack
 WVHandle.Name = "-"
 WVHandle.RequiresHandle = false

 function GetKnives()
    local Target = game.Workspace.Ignored.Shop['[Knife] - $150']
    local Tool = Instance.new('Tool')
    Tool.Parent = game.Players.LocalPlayer.Backpack
    Tool.Name = "Collect Knives"
    Tool.RequiresHandle = false
    
    
    Tool.Activated:Connect(function()
    
    for i,v in pairs(game.Workspace.Ignored.ItemsDrop:GetDescendants()) do
    if v.Name == "[Knife]" then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame
        break
    end
    end
    end)
end
GetKnives()

plr = game.Players.LocalPlayer
 
hum = plr.Character.HumanoidRootPart
 
mouse = plr:GetMouse()
local loopenabled = false

-- tool here

Tool.Activated:Connect(function() 

    WVHandle.Parent = game.Players.LocalPlayer.Character
    
    wait(0.1)

Tool.Parent = game:GetService('Players').LocalPlayer.Backpack

    play(2769472393, true, true)
    wait(0.1)
    local Char = game.Players.LocalPlayer.Character
    local Hum = Char:FindFirstChildOfClass("Humanoid") or Char:FindFirstChildOfClass("AnimationController")
    local Anim = Instance.new("Animation")

wait(1)
local count = 0 
for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
  if v.Name == '[Knife]' then
    count = count + 1
    if count == 1 then
        v.GripForward = Vector3.new(-0.999, 0.038, -0.019)
        v.GripPos = Vector3.new(0.134, -0.006, -0.27)
        v.GripRight = Vector3.new(0.021, 0.06, -0.998)
        v.GripUp = Vector3.new(0.037, 0.997, 0.06)
    elseif count == 2 then
        v.GripForward = Vector3.new(-0.999, 0.038, -0.019)
        v.GripPos = Vector3.new(0.128, -0.037, -0.008)
        v.GripRight = Vector3.new(0.021, 0.06, -0.998)
        v.GripUp = Vector3.new(0.037, 0.997, 0.06)
    else
        v.GripForward = Vector3.new(-0.999, 0.038, -0.019)
        v.GripPos = Vector3.new(0.12, -0.072, 0.23)
        v.GripRight = Vector3.new(0.021, 0.06, -0.998)
        v.GripUp = Vector3.new(0.037, 0.997, 0.06)
    end
    v.Parent = game.Players.LocalPlayer.Character
  end
end

local FastSprint = Instance.new("IntValue",ply.Character.BodyEffects.Movement);FastSprint.Name = "FastSprint"
local HulkJump = Instance.new("IntValue",ply.Character.BodyEffects.Movement);HulkJump.Name = "HighJump"
    
    Anim.AnimationId = "rbxassetid://7861306542"
    function WolvAnim()
        local XD = game.Players.LocalPlayer.Character:FindFirstChildOfClass("Humanoid"):LoadAnimation(Anim)
        XD:Play()
        XD.TimePosition = 0.40
        XD.Looped = false
        XD:AdjustSpeed(1.8)
    end
    if loopenabled == false then
        loopenabled = true
    while true do
    wait()
if game.Players.LocalPlayer.Character.BodyEffects.Movement:FindFirstChild("NoWalkSpeed") then game.Players.LocalPlayer.Character.BodyEffects.Movement:FindFirstChild("NoWalkSpeed"):Destroy() end
if game.Players.LocalPlayer.Character.BodyEffects.Movement:FindFirstChild("ReduceWalk") then game.Players.LocalPlayer.Character.BodyEffects.Movement:FindFirstChild("ReduceWalk"):Destroy() end
if game.Players.LocalPlayer.Character.BodyEffects.Movement:FindFirstChild("NoJumping") then game.Players.LocalPlayer.Character.BodyEffects.Movement:FindFirstChild("NoJumping"):Destroy() end
if game.Players.LocalPlayer.Character.BodyEffects.Reload.Value == true then game.Players.LocalPlayer.Character.BodyEffects.Reload.Value = false end

if game.Players.LocalPlayer.Backpack:FindFirstChild('-') then
    for i,v in pairs(game.Players.LocalPlayer.Character.BodyEffects.Movement:GetChildren()) do
        if v.Name == "FastSprint" then v:Destroy()
        elseif v.Name == "HighJump" then v:Destroy()
            play(2769472667, true, true)
            end
        end
    end        

        for i,v in next, Hum:GetPlayingAnimationTracks() do
            if v.Animation.AnimationId == "rbxassetid://3033700364" then
                v:Stop();
                wait(.1)
                WolvAnim()
            end
        end
    end
end
end)
end)

local Tab6 = Window:NewTab("Auto Farm")
local Tab6Section = Tab6:NewSection("Auto Farm Script")

Tab6Section:NewToggle("Fist Farm", "Auto Farm", function(state)
    if state then
loadstring(game:HttpGet('https://raw.githubusercontent.com/Exploit-blox/helloDaHood/main/DaHoodKidW'))()
    else
loadstring(game:HttpGet('https://raw.githubusercontent.com/Exploit-blox/Da-Hood/main/ProKidEsterAlt'))()
    end
end)

Tab6Section:NewToggle("Letuce Farm", "Auto Farm", function(state)
    if state then
loadstring(game:HttpGet('https://raw.githubusercontent.com/Exploit-blox/my-fault/main/beest4r'))()
    else
loadstring(game:HttpGet('https://raw.githubusercontent.com/Exploit-blox/legend-of-speeds/main/Lettuce%20False'))()
    end
end)

Tab6Section:NewToggle("Hostpital Farm", "Auto Farm", function(state)
    if state then
loadstring(game:HttpGet('https://pastebin.com/raw/wGU2QCtp'))()
    else
loadstring(game:HttpGet('https://pastebin.com/raw/kiywMAGC'))()
    end
end)

Tab6Section:NewToggle("Money Farm", "Auto Farm", function(state)
    if state then
loadstring(game:HttpGet("https://pastebin.com/raw/Zx061kiT", true))()
    else
loadstring(game:HttpGet("https://pastebin.com/raw/Zx061kiT", false))()
    end
end)

local Tab7 = Window:NewTab("Animation")
local Tab7Section = Tab7:NewSection("Animation Script")

Tab7Section:NewButton("Ninja", "Ninja Animation", function()
loadstring(game:HttpGet('https://pastebin.com/raw/3us2GAp7'))()
end)

Tab7Section:NewButton("Cartoony", "Cartoony Animation", function()
loadstring(game:HttpGet('https://pastebin.com/raw/amVNDcQT'))()
end)

Tab7Section:NewButton("Toy", "Toy Animation", function()
loadstring(game:HttpGet('https://pastebin.com/raw/zSNMgiuG'))()
end)

Tab7Section:NewButton("Bubble", "Bubble Animation", function()
loadstring(game:HttpGet('https://pastebin.com/raw/WgetAbi5'))()
end)

Tab7Section:NewButton("Levitaion", "Levitation Animation", function()
loadstring(game:HttpGet('https://pastebin.com/raw/AryTwN4z'))()
end)

Tab7Section:NewButton("Vampire", "Vampire Animation", function()
loadstring(game:HttpGet('https://pastebin.com/raw/xbG6jw7H'))()
end)

Tab7Section:NewButton("Stylish", "Stylish Aniamtion", function()
loadstring(game:HttpGet('https://pastebin.com/raw/xf5jBa86'))()
end)

Tab7Section:NewButton("Zombie", "Zombie Animation", function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/Exploit-blox/Ninja-Legends/main/ReleaseByBEEST'))()
end)

local Tab8 = Window:NewTab("Aimlock")
local Tab8Section = Tab78NewSection("Aimlock [Q]")

Tab8Section:NewButton("Aimlock","Aimlock",function()
	getgenv().AimPart = "HumanoidRootPart"
	getgenv().AimlockKey = "q"
	getgenv().AimRadius = 30
	getgenv().ThirdPerson = true
	getgenv().FirstPerson = true
	getgenv().TeamCheck = false
	getgenv().PredictMovement = true
	getgenv().PredictionVelocity = 9
	local L_27_, L_28_, L_29_, L_30_ =
            game:GetService "Players",
            game:GetService "UserInputService",
            game:GetService "RunService",
            game:GetService "StarterGui"
	local L_31_, L_32_, L_33_, L_34_, L_35_, L_36_, L_37_ =
            L_27_.LocalPlayer,
            L_27_.LocalPlayer:GetMouse(),
            workspace.CurrentCamera,
            CFrame.new,
            Ray.new,
            Vector3.new,
            Vector2.new
	local L_38_, L_39_, L_40_ = true, false, false
	local L_41_
	getgenv().CiazwareUniversalAimbotLoaded = true
	getgenv().WorldToViewportPoint = function(L_42_arg0)
		return L_33_:WorldToViewportPoint(L_42_arg0)
	end
	getgenv().WorldToScreenPoint = function(L_43_arg0)
		return L_33_.WorldToScreenPoint(L_33_, L_43_arg0)
	end
	getgenv().GetObscuringObjects = function(L_44_arg0)
		if L_44_arg0 and L_44_arg0:FindFirstChild(getgenv().AimPart) and L_31_ and L_31_.Character:FindFirstChild("Head") then
			local L_45_ = workspace:FindPartOnRay(L_35_(L_44_arg0[getgenv().AimPart].Position, L_31_.Character.Head.Position))
			if L_45_ then
				return L_45_:IsDescendantOf(L_44_arg0)
			end
		end
	end
	getgenv().GetNearestTarget = function()
		local L_46_ = {}
		local L_47_ = {}
		local L_48_ = {}
		for L_50_forvar0, L_51_forvar1 in pairs(L_27_:GetPlayers()) do
			if L_51_forvar1 ~= L_31_ then
				table.insert(L_46_, L_51_forvar1)
			end
		end
		for L_52_forvar0, L_53_forvar1 in pairs(L_46_) do
			if L_53_forvar1.Character ~= nil then
				local L_54_ = L_53_forvar1.Character:FindFirstChild("Head")
				if getgenv().TeamCheck == true and L_53_forvar1.Team ~= L_31_.Team then
					local L_55_ =
                            (L_53_forvar1.Character:FindFirstChild("Head").Position - game.Workspace.CurrentCamera.CFrame.p).magnitude
					local L_56_ =
                            Ray.new(
                            game.Workspace.CurrentCamera.CFrame.p,
                            (L_32_.Hit.p - game.Workspace.CurrentCamera.CFrame.p).unit * L_55_
                        )
					local L_57_, L_58_ = game.Workspace:FindPartOnRay(L_56_, game.Workspace)
					local L_59_ = math.floor((L_58_ - L_54_.Position).magnitude)
					L_47_[L_53_forvar1.Name .. L_52_forvar0] = {}
					L_47_[L_53_forvar1.Name .. L_52_forvar0].dist = L_55_
					L_47_[L_53_forvar1.Name .. L_52_forvar0].plr = L_53_forvar1
					L_47_[L_53_forvar1.Name .. L_52_forvar0].diff = L_59_
					table.insert(L_48_, L_59_)
				elseif getgenv().TeamCheck == false and L_53_forvar1.Team == L_31_.Team then
					local L_60_ =
                            (L_53_forvar1.Character:FindFirstChild("Head").Position - game.Workspace.CurrentCamera.CFrame.p).magnitude
					local L_61_ =
                            Ray.new(
                            game.Workspace.CurrentCamera.CFrame.p,
                            (L_32_.Hit.p - game.Workspace.CurrentCamera.CFrame.p).unit * L_60_
                        )
					local L_62_, L_63_ = game.Workspace:FindPartOnRay(L_61_, game.Workspace)
					local L_64_ = math.floor((L_63_ - L_54_.Position).magnitude)
					L_47_[L_53_forvar1.Name .. L_52_forvar0] = {}
					L_47_[L_53_forvar1.Name .. L_52_forvar0].dist = L_60_
					L_47_[L_53_forvar1.Name .. L_52_forvar0].plr = L_53_forvar1
					L_47_[L_53_forvar1.Name .. L_52_forvar0].diff = L_64_
					table.insert(L_48_, L_64_)
				end
			end
		end
		if unpack(L_48_) == nil then
			return nil
		end
		local L_49_ = math.floor(math.min(unpack(L_48_)))
		if L_49_ > getgenv().AimRadius then
			return nil
		end
		for L_65_forvar0, L_66_forvar1 in pairs(L_47_) do
			if L_66_forvar1.diff == L_49_ then
				return L_66_forvar1.plr
			end
		end
		return nil
	end
	L_32_.KeyDown:Connect(
            function(L_67_arg0)
		if L_67_arg0 == AimlockKey and L_41_ == nil then
			pcall(
                        function()
				if L_39_ ~= true then
					L_39_ = true
				end
				local L_68_
				L_68_ = GetNearestTarget()
				if L_68_ ~= nil then
					L_41_ = L_68_
				end
			end
                    )
		elseif L_67_arg0 == AimlockKey and L_41_ ~= nil then
			if L_41_ ~= nil then
				L_41_ = nil
			end
			if L_39_ ~= false then
				L_39_ = false
			end
		end
	end)
	L_29_.RenderStepped:Connect(
            function()
		if getgenv().ThirdPerson == true and getgenv().FirstPerson == true then
			if
                        (L_33_.Focus.p - L_33_.CoordinateFrame.p).Magnitude > 1 or
                            (L_33_.Focus.p - L_33_.CoordinateFrame.p).Magnitude <= 1
                     then
				L_40_ = true
			else
				L_40_ = false
			end
		elseif getgenv().ThirdPerson == true and getgenv().FirstPerson == false then
			if (L_33_.Focus.p - L_33_.CoordinateFrame.p).Magnitude > 1 then
				L_40_ = true
			else
				L_40_ = false
			end
		elseif getgenv().ThirdPerson == false and getgenv().FirstPerson == true then
			if (L_33_.Focus.p - L_33_.CoordinateFrame.p).Magnitude <= 1 then
				L_40_ = true
			else
				L_40_ = false
			end
		end
		if L_38_ == true and L_39_ == true then
			if L_41_ and L_41_.Character and L_41_.Character:FindFirstChild(getgenv().AimPart) then
				if getgenv().FirstPerson == true then
					if L_40_ == true then
						if getgenv().PredictMovement == true then
							L_33_.CFrame =
                                        L_34_(
                                        L_33_.CFrame.p,
                                        L_41_.Character[getgenv().AimPart].Position +
                                            L_41_.Character[getgenv().AimPart].Velocity / PredictionVelocity
                                    )
						elseif getgenv().PredictMovement == false then
							L_33_.CFrame = L_34_(L_33_.CFrame.p, L_41_.Character[getgenv().AimPart].Position)
						end
					end
				elseif getgenv().ThirdPerson == true then
					if L_40_ == true then
						if getgenv().PredictMovement == true then
							L_33_.CFrame =
                                        L_34_(
                                        L_33_.CFrame.p,
                                        L_41_.Character[getgenv().AimPart].Position +
                                            L_41_.Character[getgenv().AimPart].Velocity / PredictionVelocity
                                    )
						elseif getgenv().PredictMovement == false then
							L_33_.CFrame = L_34_(L_33_.CFrame.p, L_41_.Character[getgenv().AimPart].Position)
						end
					end
				end
			end
		end
	end)
end)

Tab8Section:NewTextBox("Aimlock Key","Aimlock Key should be lowercase.",function(L_69_arg0)
	getgenv().AimlockKey = L_69_arg0
end)

Tab8Section:NewTextBox("Aimlock Prediction","Customize your aimlock prediction",function(L_70_arg0)
	PredictionVelocity = L_70_arg0
end)

Tab8Section:NewDropdown("AimPart","AimPart",{"Head","UpperTorso","HumanoidRootPart","LowerTorso"},function(L_71_arg0)
	getgenv().AimPart = L_71_arg0
end)

local Tab8Section = Tab8NewSection("Silent Aim [T]")

Tab8Section:NewButton("Silent Aim","Silent Aim Toggle Key is T.",function()
	loadstring(game:HttpGet("https://raw.githubusercontent.com/tayodevelup/imsoniac/main/silentaim", true))()
end)

Tab8Section:NewTextBox("Silent Aim Prediction","0.157 for low ping 0.178 high ping",function(L_72_arg0)
	DaHoodSettings.Prediction = L_72_arg0
end)

Tab8Section:NewDropdown("Silent Aim Part","Choose Part",{"Head","UpperTorso","HumanoidRootPart","LowerTorso"},function(L_73_arg0)
	Aiming.TargetPart = L_73_arg0
end)

Tab8Section:NewTextBox("Silent Aim Size Fov","Silent Aim Size",function(L_74_arg0)
	Aiming.FOV = L_74_arg0
end)

Tab8Section:NewToggle("Silent Aim Show Fov","Show The Silent Aim Fov",function(L_75_arg0)
	Aiming.ShowFOV = L_75_arg0
end)

local Tab8Section = Tab8:NewSection("Anti Lock [Z]")

Tab8Section:NewButton("Anti-Lock","Key is Z.",function()
	repeat
		wait()
	until game:IsLoaded()
	getgenv().Fix = true
	getgenv().TeclasWS = {
		["tecla1"] = "nil",
		["tecla2"] = "nil",
		["tecla3"] = "H"
	}
	local L_121_ = game:GetService("Players")
	local L_122_ = game:GetService("StarterGui") or "son una mierda"
	local L_123_ = L_121_.LocalPlayer
	local L_124_ = L_123_:GetMouse()
	local L_125_ = getrenv()._G
	local L_126_ = getrawmetatable(game)
	local L_127_ = L_126_.__newindex
	local L_128_ = L_126_.__index
	local L_129_ = 22
	local L_130_ = true
	function anunciar_atentado_terrorista(L_138_arg0)
		L_122_:SetCore("SendNotification", {
			Title = "anti lock fix",
			Text = L_138_arg0
		})
	end
	getgenv().TECHWAREWALKSPEED_LOADED = true
	wait(1.5)
	anunciar_atentado_terrorista("Press  " .. TeclasWS.tecla3 .. " to turn on/off anti lock fix")
	L_124_.KeyDown:Connect(
            function(L_139_arg0)
		if L_139_arg0:lower() == TeclasWS.tecla1:lower() then
			L_129_ = L_129_ + 1
			anunciar_atentado_terrorista("æ­æ¾å¨éåº¦å·²æé« (speed = " .. tostring(L_129_) .. ")")
		elseif L_139_arg0:lower() == TeclasWS.tecla2:lower() then
			L_129_ = L_129_ - 1
			anunciar_atentado_terrorista("ç©å®¶çéåº¦å·²éä½ (speed = " .. tostring(L_129_) .. ")")
		elseif L_139_arg0:lower() == TeclasWS.tecla3:lower() then
			if L_130_ then
				L_130_ = false
				anunciar_atentado_terrorista("anti lock fix off")
			else
				L_130_ = true
				anunciar_atentado_terrorista("anti lock fix on")
			end
		end
	end
        )
	setreadonly(L_126_, false)
	L_126_.__index =
            newcclosure(
            function(L_140_arg0, L_141_arg1)
		local L_142_ = checkcaller()
		if L_141_arg1 == "WalkSpeed" and not L_142_ then
			return L_125_.CurrentWS
		end
		return L_128_(L_140_arg0, L_141_arg1)
	end
        )
	L_126_.__newindex =
            newcclosure(
            function(L_143_arg0, L_144_arg1, L_145_arg2)
		local L_146_ = checkcaller()
		if L_130_ then
			if L_144_arg1 == "WalkSpeed" and L_145_arg2 ~= 0 and not L_146_ then
				return L_127_(L_143_arg0, L_144_arg1, L_129_)
			end
		end
		return L_127_(L_143_arg0, L_144_arg1, L_145_arg2)
	end
        )
	setreadonly(L_126_, true)
	repeat
		wait()
	until game:IsLoaded()
	local L_131_ = game:service("Players")
	local L_132_ = L_131_.LocalPlayer
	repeat
		wait()
	until L_132_.Character
	local L_133_ = game:service("UserInputService")
	local L_134_ = game:service("RunService")
	local L_135_ = -0.27
	local L_136_ = false
	local L_137_
	L_133_.InputBegan:connect(
            function(L_147_arg0)
		if L_147_arg0.KeyCode == Enum.KeyCode.LeftBracket then
			L_135_ = L_135_ + 0.01
			print(L_135_)
			wait(0.2)
			while L_133_:IsKeyDown(Enum.KeyCode.LeftBracket) do
				wait()
				L_135_ = L_135_ + 0.01
				print(L_135_)
			end
		end
		if L_147_arg0.KeyCode == Enum.KeyCode.RightBracket then
			L_135_ = L_135_ - 0.01
			print(L_135_)
			wait(0.2)
			while L_133_:IsKeyDown(Enum.KeyCode.RightBracket) do
				wait()
				L_135_ = L_135_ - 0.01
				print(L_135_)
			end
		end
		if L_147_arg0.KeyCode == Enum.KeyCode.Z then
			L_136_ = not L_136_
			if L_136_ == true then
				repeat
					game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame =
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame +
                                game.Players.LocalPlayer.Character.Humanoid.MoveDirection * L_135_
					game:GetService("RunService").Stepped:wait()
				until L_136_ == false
			end
		end
	end)
end)

local Tab8Section = Tab8:NewSection("Other Lock")

Tab8Section:NewButton("Aim Lock {Old Arceus X Aimlock Tools}", "Arceus X AimLock", function()
loadstring(game:HttpGet('https://pastebin.com/raw/HA8kAiYp'))()
end)

Tab8Section:NewButton("Aimbot", "", function()
loadstring(game:HttpGetAsync("https://raw.githubusercontent.com/Hyotinhofofinho/s1mple/main/LIXO"))()
end)

Tab8Section:NewButton("Streamable [Q]", "Q", function()
loadstring(game:HttpGet('https://pastebin.com/raw/XfdzBV2y'))()
end)

Tab8Section:NewButton("Aimbot [Q]", "Q", function()
loadstring(game:HttpGet('https://pastebin.com/raw/XzCsiJaD'))()
end)

Tab8Section:NewButton("Kloy Lock [Q]", "Q", function()
loadstring(game:HttpGet('https://pastebin.com/raw/BtQYq4EG'))()
end)

local Tab8Section = Tab8:NewSection("FireHood Aimlock")

Section:NewTextBox("FireHood Aimlock", "Aimlock", function(txt)
-- Toggle
getgenv().Target = true
-- Configuration
getgenv().Key = Enum.KeyCode.Q
getgenv().Prediction = 0.135
getgenv().ChatMode = false
getgenv().NotifMode = true
    getgenv().PartMode = true
    getgenv().AirshotFunccc = true
    getgenv().Partz = "txt"
getgenv().AutoPrediction = true
--
    _G.Types = {
        Ball = Enum.PartType.Ball,
        Block = Enum.PartType.Block, 
        Cylinder = Enum.PartType.Cylinder
    }
    
    --variables                 
        local Tracer = Instance.new("Part", game.Workspace)
    Tracer.Name = "gay" 
    Tracer.Anchored = true      
    Tracer.CanCollide = false
    Tracer.Transparency = 0.8
    Tracer.Parent = game.Workspace  
    Tracer.Shape = _G.Types.Block
    Tracer.Size = Vector3.new(14,14,14)
    Tracer.Color = Color3.fromRGB(128,128,128)
    
    --
    local plr = game.Players.LocalPlayer
local mouse = plr:GetMouse()
local Runserv = game:GetService("RunService")

circle = Drawing.new("Circle")
circle.Color = Color3.fromRGB(255,255,255)
circle.Thickness = 0
circle.NumSides = 732
circle.Radius = 120
circle.Thickness = 0
circle.Transparency = 0.7
circle.Visible = false
circle.Filled = false

Runserv.RenderStepped:Connect(function()
    circle.Position = Vector2.new(mouse.X,mouse.Y+35)
end)
    
        local guimain = Instance.new("Folder", game.CoreGui)
        local CC = game:GetService"Workspace".CurrentCamera
    local LocalMouse = game.Players.LocalPlayer:GetMouse()
        local Locking = false
    
        
    --
    if getgenv().valiansh == true then
                        game.StarterGui:SetCore("SendNotification", {
                        Title    = "FireHood Aimlock",
                        Text     = "loaded",
                        Duration = 1
        
                   })
        return
    end
    
    getgenv().valiansh = true
    
        local UserInputService = game:GetService("UserInputService")

    UserInputService.InputBegan:Connect(function(keygo,ok)
           if (not ok) then
           if (keygo.KeyCode == getgenv().Key) then
               if getgenv().Target == true then
               Locking = not Locking
               
               if Locking then
               Plr =  getClosestPlayerToCursor()
                if getgenv().ChatMode then
        local A_1 = "Target: "..tostring(Plr.Character.Humanoid.DisplayName) local A_2 = "All" local Event = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest Event:FireServer(A_1, A_2) 
            end 
               if getgenv().NotifMode then
                game.StarterGui:SetCore("SendNotification", {
        Title = "";
        Text = "Target: "..tostring(Plr.Character.Humanoid.DisplayName);
    
    })
    end
    elseif not Locking then
         if getgenv().ChatMode then
        local A_1 = "Unlocked!" local A_2 = "All" local Event = game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest Event:FireServer(A_1, A_2) 
            end 
        if getgenv().NotifMode then
                        game.StarterGui:SetCore("SendNotification", {
                        Title    = "FireHood Lock",
                        Text     = "unlocked",
                        Duration = 1
               })
           elseif getgenv().Target == false then
                        game.StarterGui:SetCore("SendNotification", {
                        Title    = "FireHood Lock",
                        Text     = "target isn't enabled",
                        Duration = 1
     
                   })
               
               end
                  
 
 end     end   
end
end
end)
    
    function getClosestPlayerToCursor()
        local closestPlayer
        local shortestDistance = circle.Radius

        for i, v in pairs(game.Players:GetPlayers()) do
            if v ~= game.Players.LocalPlayer and v.Character and v.Character:FindFirstChild("Humanoid") and v.Character.Humanoid.Health ~= 0 and v.Character:FindFirstChild("LowerTorso") then
                local pos = CC:WorldToViewportPoint(v.Character.PrimaryPart.Position)
                local magnitude = (Vector2.new(pos.X, pos.Y) - Vector2.new(LocalMouse.X, LocalMouse.Y)).magnitude
                if magnitude < shortestDistance then
                    closestPlayer = v
                    shortestDistance = magnitude
                end
            end
        end
        return closestPlayer
    end
--
if getgenv().PartMode then
    game:GetService"RunService".Stepped:connect(function()
        if Locking and Plr.Character and Plr.Character:FindFirstChild("LowerTorso") then
            Tracer.CFrame = CFrame.new(Plr.Character.LowerTorso.Position+(Plr.Character.LowerTorso.Velocity*Prediction))
        else
            Tracer.CFrame = CFrame.new(0, 9999, 0)

        end
    end)
end

    
    
    --
    local rawmetatable = getrawmetatable(game)
    local old = rawmetatable.__namecall
    setreadonly(rawmetatable, false)
    rawmetatable.__namecall = newcclosure(function(...)
        local args = {...}
        if Locking and getnamecallmethod() == "FireServer" and args[2] == "UpdateMousePos" then
            args[3] = Plr.Character[getgenv().Partz].Position+(Plr.Character[getgenv().Partz].Velocity*Prediction)
            return old(unpack(args))
        end
        return old(...)
    end)


if getgenv().AirshotFunccc == true then

            if Plr.Character.Humanoid.Jump == true and Plr.Character.Humanoid.FloorMaterial == Enum.Material.Air then
                getgenv().Partz = "RightFoot"
            else
                Plr.Character:WaitForChild("Humanoid").StateChanged:Connect(function(old,new)
                    if new == Enum.HumanoidStateType.Freefall then
                    getgenv().Partz = "RightFoot"
                    else
                        getgenv().Partz = "LowerTorso"
                    end
                end)
            end
end
---
    while wait() do
    if getgenv().AutoPrediction == true then
        local pingvalue = game:GetService("Stats").Network.ServerStatsItem["Data Ping"]:GetValueString()
        local split = string.split(pingvalue,'(')
        local ping = tonumber(split[1])
        if ping < 130 then
            getgenv().Prediction = 0.151
        elseif ping < 125 then
            getgenv().Prediction = 0.149
        elseif ping < 110 then
            getgenv().Prediction = 0.146
        elseif ping < 105 then
            getgenv().Prediction = 0.138
        elseif ping < 90 then
            getgenv().Prediction = 0.136
        elseif ping < 80 then
            getgenv().Prediction = 0.134
        elseif ping < 70 then
            getgenv().Prediction = 0.131
        elseif ping < 60 then
            getgenv().Prediction = 0.1229
        elseif ping < 50 then
            getgenv().Prediction = 0.1225
        elseif ping < 40 then
            getgenv().Prediction = 0.1256
        end
    end
    end
    
end)


local Tab9Section = Tab9:NewSection("Put This In Textbox")
Tab10Section:NewLabel("Head")
Tab10Section:NewLabel("UpperTurso")
Tab10Section:NewLabel("LowerTurso")
Tab10Section:NewLabel("HumanoidRootPart")

local Tab9 = Window:NewTab("Setting")
local Tab9Section = Tab9:NewSection("Setting")

Tab9Section:NewKeybind("Close/Open", "Close/Open", Enum.KeyCode.Shift, function()
	Library:ToggleUI()
end)

local Tab10 = Window:NewTab("Credits")
local Tab10Section = Tab10:NewSection("FireHood/Da Newb")
Tab10Section:NewLabel("Ui: Kavo Libary")
Tab10Section:NewLabel("Fly Gui V3: me_ozoneYT And Quandle The Dinglish")
Tab10Section:NewLabel("Owner: ALT1LR")
Tab10Section:NewLabel("Discord: alt1lr#9495"0)
Tab10Section:NewLabel("Scripter1: ALT1LR")
Tab10Section:NewLabel("Co Owner: FireHood")
Tab10Section:NewLabel("Scripter2: FireHood")
