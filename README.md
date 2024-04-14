


if not getconnections or not hookmetamethod or not getnamecallmethod or not ((getgenv and getgenv()) or _G) then
	game:GetService("StarterGui"):SetCore("SendNotification", {Title = "Tiger Admin",Text = "Executor is not supported!",Duration = 10,})
end
if not workspace:FindFirstChild("Criminals Spawn") or not workspace:FindFirstChild("Criminals Spawn"):FindFirstChild("SpawnLocation") then
	game:GetService("StarterGui"):SetCore("SendNotification", {Title = "Tiger Admin",Text = "Criminals spawn not found! Please rejoin.",Duration = 10,})
end
game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart")
if game:FindFirstChild("Tiger_revamp_loaded") then  ((getgenv and getgenv()) or _G).NotifTiger("Tiger admin is already executed!",false) return warn("Already loaded") end
local Player, plr,Folder = game:GetService("Players").LocalPlayer, game:GetService("Players").LocalPlayer,Instance.new("Folder",game)
local OldHook, hookmetamethod, getnamecallmethod = nil, hookmetamethod, getnamecallmethod
local HasGamepass,UserInputService = game:GetService("MarketplaceService"):UserOwnsGamePassAsync(Player.UserId, 96651),game:GetService("UserInputService")
local GlobalVar = ((getgenv and getgenv()) or _G)
local Unloaded = false
local CriminalCFRAME = workspace["Criminals Spawn"].SpawnLocation.CFrame
local API_Prem = loadstring(game:HttpGet("https://raw.githubusercontent.com/dalloc2/Roblox/main/Listing.lua"))()
local PremiumActivated = API_Prem.CheckPremium()

local Temp = {}
local API = {}
local Reload_Guns = {}
local Prefix = "!"

--------
Folder.Name = "Tiger_revamp_loaded"
ScreenGui = Instance.new("ScreenGui")
CmdBarFrame = Instance.new("Frame")
UICorner = Instance.new("UICorner")
Out = Instance.new("ImageLabel")
UICorner_2 = Instance.new("UICorner")
CommandBar = Instance.new("TextBox")
UIStroke = Instance.new("UIStroke")
Commands = Instance.new("ImageLabel")
UICorner_3 = Instance.new("UICorner")
UIStroke_2 = Instance.new("UIStroke")
CommandsList = Instance.new("ScrollingFrame")
UIListLayout = Instance.new("UIListLayout")
TEMP_CMD = Instance.new("TextLabel")
SearchBar = Instance.new("TextBox")
ScreenGui.Parent = (game:GetService("CoreGui") or gethui())
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
ScreenGui.Name = math.random()

CmdBarFrame.Name = "CmdBarFrame"
CmdBarFrame.Parent = ScreenGui
CmdBarFrame.AnchorPoint = Vector2.new(0.5, 0.5)
CmdBarFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
CmdBarFrame.BackgroundTransparency = 1.000
CmdBarFrame.BorderSizePixel = 0
CmdBarFrame.Position = UDim2.new(0.5, 0, 0.899999998, 0)
CmdBarFrame.Position = CmdBarFrame.Position+UDim2.new(0,0,1.1,0)
CmdBarFrame.Size = UDim2.new(0, 457, 0, 65)

UICorner.CornerRadius = UDim.new(0, 3)
UICorner.Parent = CmdBarFrame
Temp.Esps = {}
do
	CmdsIcon = Instance.new("ImageLabel")
	UICornera = Instance.new("UICorner")
	UIStroke12 = Instance.new("UIStroke")
	CmdButton = Instance.new("ImageButton")

	CmdsIcon.Name = "CmdsIcon"
	CmdsIcon.Parent = CmdBarFrame
	CmdsIcon.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
	CmdsIcon.Position = UDim2.new(-0.132423401, 0, 0.0226149559, 0)
	CmdsIcon.Size = UDim2.new(0.121672593, 0, 0.945454538, 0)
	CmdsIcon.Image = "rbxassetid://12661800163"
	CmdsIcon.ImageTransparency = 0.030

	UICornera.CornerRadius = UDim.new(0, 6)
	UICornera.Parent = CmdsIcon

	UIStroke12.Parent = CmdsIcon

	CmdButton.Name = "CmdButton"
	CmdButton.Parent = CmdsIcon
	CmdButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	CmdButton.BackgroundTransparency = 1.000
	CmdButton.Position = UDim2.new(0.298999995, 0, 0.27700001, 0)
	CmdButton.Size = UDim2.new(0, 27, 0, 27)
	CmdButton.Image = "rbxassetid://11570802781"
	CmdButton.ImageTransparency = 0.430
	CmdButton.MouseButton1Up:Connect(function()
		if not Temp.CmdsC then
			Temp.CmdsC = true
			if Commands.Visible == false then
				Commands:TweenPosition(SavedCmdsPosition,"Out","Quart",1)
				Commands.Visible = true
			else
				Commands:TweenPosition(SavedCmdsPosition+UDim2.new(0,0,1,0),"Out","Quart",1)
				wait(.5)
				Commands.Visible = false
			end
			wait(.7)
			Temp.CmdsC = false
		end
	end)
	CmdButton.MouseEnter:Connect(function()
		CmdButton.ImageColor3 = Color3.new(0.588235, 0.588235, 0.588235)
	end)
	CmdButton.MouseLeave:Connect(function()
		CmdButton.ImageColor3 = Color3.new(1, 1, 1)
	end)
end
do
	Toggles = Instance.new("ImageLabel")
	local Stokeee = Instance.new("UIStroke")
	local Corrrer = Instance.new("UICorner")
	local ToggleScroll = Instance.new("ScrollingFrame")
	local kewkfwe = Instance.new("UIListLayout")
	local tempb = Instance.new("TextButton")
	local UIStroke = Instance.new("UIStroke")
	local UICorner = Instance.new("UICorner")

	Toggles.Name = "Toggles"
	Toggles.Parent = ScreenGui
	Toggles.AnchorPoint = Vector2.new(0.5, 0.5)
	Toggles.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
	Toggles.Position = UDim2.new(0.499593854, 0, 0.499376595, 0)+UDim2.new(0,0,1,0)
	Toggles.Size = UDim2.new(0, 539, 0, 409)
	Toggles.Visible = false
	Toggles.Image = "rbxassetid://12011977394"
	Toggles.ImageTransparency = 0.260

	Stokeee.Parent = Toggles
	Stokeee.Name = "Stokeee"

	Corrrer.Name = "Corrrer"
	Corrrer.Parent = Toggles

	ToggleScroll.Name = "ToggleScroll"
	ToggleScroll.Parent = Toggles
	ToggleScroll.Active = true
	ToggleScroll.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	ToggleScroll.BackgroundTransparency = 1.000
	ToggleScroll.Size = UDim2.new(0, 539, 0, 408)
	ToggleScroll.ScrollBarThickness = 4

	kewkfwe.Name = "kewkfwe"
	kewkfwe.Parent = ToggleScroll
	kewkfwe.SortOrder = Enum.SortOrder.LayoutOrder
	kewkfwe.Padding = UDim.new(0, 5)

	tempb.Name = "tempb"
	tempb.Parent = ScreenGui
	tempb.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
	tempb.BackgroundTransparency = 0.550
	tempb.Position = UDim2.new(0, 0, -7.47979882e-08, 0)
	tempb.Size = UDim2.new(0, 539, 0, 44)
	tempb.Visible = false
	tempb.Font = Enum.Font.SourceSans
	tempb.Text = "Autorespawn [OFF]"
	tempb.TextColor3 = Color3.fromRGB(255, 255, 255)
	tempb.TextSize = 14.000

	UIStroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
	UIStroke.Parent = tempb

	UICorner.CornerRadius = UDim.new(0, 3)
	UICorner.Parent = tempb

end

Out.Name = "Out"
Out.Parent = CmdBarFrame
Out.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Out.Position = UDim2.new(0.0200897697, 0, 0.022615375, 0)
Out.Size = UDim2.new(0.974358976, 0, 0.945454538, 0)
Out.Image = "rbxassetid://11789397066"
Out.ImageTransparency = 0.240

UICorner_2.CornerRadius = UDim.new(0, 6)
UICorner_2.Parent = Out

CommandBar.Name = "CommandBar"
CommandBar.Parent = Out
CommandBar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
CommandBar.BackgroundTransparency = 1.000
CommandBar.BorderSizePixel = 0
CommandBar.Position = UDim2.new(0.0359953903, 0, 0.128254473, 0)
CommandBar.Size = UDim2.new(0, 519, 0, 46)
CommandBar.Font = Enum.Font.SourceSans
CommandBar.PlaceholderColor3 = Color3.fromRGB(178, 178, 178)
CommandBar.PlaceholderText = "Command bar"
CommandBar.Text = ""
CommandBar.TextColor3 = Color3.fromRGB(255, 255, 255)
CommandBar.TextSize = 24.000
CommandBar.TextTransparency = 0.140
CommandBar.TextWrapped = true

UIStroke.Parent = Out

Commands.Name = "Commands"
Commands.Parent = ScreenGui
Commands.AnchorPoint = Vector2.new(0.5, 0.5)
Commands.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Commands.Position = UDim2.new(0.5, 0, 0.5, 0)
Commands.Size = UDim2.new(0, 455, 0, 297)
Commands.Image = "rbxassetid://12011977394"
Commands.ImageTransparency = 0.200
Commands.Visible = false

UICorner_3.CornerRadius = UDim.new(0, 6)
UICorner_3.Parent = Commands

UIStroke_2.Parent = Commands

CommandsList.Parent = Commands
CommandsList.Active = true
CommandsList.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
CommandsList.BackgroundTransparency = 1.000
CommandsList.Position = UDim2.new(0, 0, 0.077441074, 0)
CommandsList.Size = UDim2.new(0, 455, 0, 274)
CommandsList.ScrollBarThickness = 5
CommandsList.AutomaticCanvasSize="Y"
UIListLayout.Parent = CommandsList
UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
UIListLayout.Padding = UDim.new(0, 8)

TEMP_CMD.Parent = Folder
TEMP_CMD.BackgroundColor3 = Color3.fromRGB(62, 62, 62)
TEMP_CMD.BackgroundTransparency = 0.750
TEMP_CMD.Size = UDim2.new(0, 455, 0, 14)
TEMP_CMD.Font = Enum.Font.SourceSans
TEMP_CMD.Text = "sex"--//yes
TEMP_CMD.TextColor3 = Color3.fromRGB(255, 255, 255)
TEMP_CMD.TextSize = 14.000
SavedCmdsPosition = Commands.Position
SearchBar.Parent = Commands
SearchBar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
SearchBar.BackgroundTransparency = 1.000
SearchBar.Size = UDim2.new(0, 455, 0, 17)
SearchBar.Font = Enum.Font.SourceSans
SearchBar.PlaceholderColor3 = Color3.fromRGB(178, 178, 178)
SearchBar.PlaceholderText = "Search here"
SearchBar.Text = ""
SearchBar.TextColor3 = Color3.fromRGB(234, 234, 234)
SearchBar.TextSize = 14.000

Folder.Parent = game

do
	--Load guis
	game:GetService("ContentProvider"):PreloadAsync({
		Commands,
		Out,
	})
end

for i,v in pairs(ScreenGui:GetDescendants()) do v.Name = game:GetService("HttpService"):GenerateGUID(true) end
local AmmountCurrent = 0
local commandsLol = {}
function API:CreateCmd(Header, Description, Callback,IsHide,Extra,IsPre,plsdonotlower)
	local CloneTXT = TEMP_CMD:Clone()
	CloneTXT.Text = Prefix..Header.." "..(Extra or "").." | "..Description
	if IsHide then
		CloneTXT.Parent =nil
	else
		CloneTXT.Parent = CommandsList
	end
	if IsPre then
		CloneTXT.TextColor3 = Color3.new(1, 0.796078, 0.0666667)
	end
	AmmountCurrent=AmmountCurrent+1
    commandsLol[Header] = Callback
	local function FactCheck(TheText)
		if Unloaded then return end
		local Text = nil
		if not plsdonotlower then
			Text=TheText:lower()
		else
			Text = TheText
		end
		local Split = Text:split(" ")
		local First = Split[1]
		local Second = Split[2]

		if First:lower() == Header:lower() or First:lower() == Prefix..Header:lower() then
			local a,b = pcall(function()
				Callback(Split)
			end)
			if not a and b then
				warn("--> TIGER ADMIN DETECTED AN ERROR")
				warn("COMMAND: "..Prefix..Header)
				warn("ERROR: "..tostring(b))
			end
		end
	end
	Player.Chatted:Connect(function(c)
		if c and not Unloaded then
			local Subbed = string.sub(c,1,1)
			if Subbed == Prefix then
				FactCheck(c)
			end
		end
	end)
	CommandBar.FocusLost:Connect(function(EnterKey)
		if EnterKey and not Unloaded then
			FactCheck(CommandBar.Text)
			task.wait(.04)
			CommandBar.Text = ""
		end
	end)
end

function API:Tween(Obj, Prop, New, Time)
	if not Time then
		Time = .5
	end
	local TweenService = game:GetService("TweenService")
	local info = TweenInfo.new(
		Time, 
		Enum.EasingStyle.Quart, 
		Enum.EasingDirection.Out, 
		0, 
		false,
		0
	)
	local propertyTable = {
		[Prop] = New,
	}

	TweenService:Create(Obj, info, propertyTable):Play()
end
function API:Notif(Text,Dur)
	task.spawn(function()
		if not Dur then
			Dur = 1.5
		end
		local Notif = Instance.new("ScreenGui")
		local Frame_1 = Instance.new("Frame")
		local TextLabel = Instance.new("TextLabel")
		Notif.Parent = (game:GetService("CoreGui") or gethui())
		Notif.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
		Frame_1.Parent = Notif
		Frame_1.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		Frame_1.BackgroundTransparency=1
		Frame_1.BorderSizePixel = 0
		Frame_1.Position = UDim2.new(0, 0, 0.0500000007, 0)
		Frame_1.Size = UDim2.new(1, 0, 0.100000001, 0)
		TextLabel.Parent = Frame_1
		TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		TextLabel.BackgroundTransparency = 1.000
		TextLabel.TextTransparency =1
		TextLabel.Size = UDim2.new(1, 0, 1, 0)
		TextLabel.Font = Enum.Font.Highway
		TextLabel.Text = Text or "Text not found"
		TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
		TextLabel.TextSize = 21.000
		API:Tween(Frame_1,"BackgroundTransparency",0.350,.5)
		API:Tween(TextLabel,"TextTransparency",0,.5)
		wait(Dur+.7)
		API:Tween(Frame_1,"BackgroundTransparency",1,.5)
		API:Tween(TextLabel,"TextTransparency",1,.5)
		wait(.7)
		Notif:Destroy()
	end)
	return
end
GlobalVar.NotifTiger = function(t,v)
	API:Notif(t,v)
end
local States = {}
local Settings = {
	Prefix = "!",
	ValidCommands = {},
}
local OrginMenuPos = Player.PlayerGui.Home.hud.MenuButton.Position
local OrginGunPos = Player.PlayerGui.Home.hud.GunFrame.Position
do
	States.loopkillinmates = false
	States.loopkillcriminals = false
	States.DraggableGuis = false
	States.spawnguns = false
	States.loopkillguards = false
	States.Antishield = false
	States.DoorsDestroy = false
	States.antipunch = false
	States.AutoRespawn = true
	States.AutoItems = false
	States.ClickKill = false
	States.ClickArrest = false
	States.AntiTase = false
	States.AntiArrest = false
	States.OnePunch = false
	States.killaura = false
	States.anticrash = false
	States.AntiTouch = false
	States.ShootBack = false
	States.AntiFling = false
	States.AutoInfAmmo = false
	States.joinlogs = false
	States.noclip = false
	States.Godmode = false
	States.loopopendoors = false
	States.SilentAim = false
	States.ArrestAura = false
	States.OneShot = false
	States.ff = false
	States.esp = false
	States.earrape = false
	--
	Temp.IsBringing = false
	Temp.Loopkilling = {}
	Temp.ArrestOldP = false
	Temp.KillAuras = {}
	API.Whitelisted = {}
	Temp.Admins = {}
	Temp.LoopmKilling = {}
	Temp.Viruses = {}
	Temp.SavedAdmins = {}
	Running = false
end

if writefile and makefolder and readfile and isfile then
	if isfile("Tiger Admin") == false or isfile("Tiger_Admin/Invite.json") == false then
		makefolder("Tiger_Admin")
		if isfile("Tiger_Admin/Invite.json") == false then
			writefile("Tiger_Admin/Invite.json",game:GetService("HttpService"):JSONEncode({
				Invite_To_Server = true
			}))
		end
		if isfile("Tiger_Admin/SavedAdmins.json") == false then
			writefile("Tiger_Admin/SavedAdmins.json",game:GetService("HttpService"):JSONEncode({}))
		else
			local Content = game:GetService("HttpService"):JSONDecode(readfile("Tiger_Admin/SavedAdmins.json"))
			for i,v in pairs(Content) do
				if v then
					table.insert(Temp.Admins, v)
				end
			end
		end
	end
end

task.spawn(function()
	if writefile and makefolder and readfile and isfile then
		if game:GetService("HttpService"):JSONDecode(readfile("Tiger_Admin/Invite.json")).Invite_To_Server then
			local Request_ = (syn and syn.request) or http_request or request
			Request_({
				Url = 'http://127.0.0.1:6463/rpc?v=1',
				Method = 'POST',
				Headers = {
					['Content-Type'] = 'application/json',
					Origin = 'https://discord.com'
				},
				Body = game:GetService("HttpService"):JSONEncode({
					cmd = 'INVITE_BROWSER',
					nonce = game:GetService("HttpService"):GenerateGUID(false),
					args = {code = 'zj5xRp3ZKn'}
				})
			})
		end
	end
end)

function API:CreateBulletTable(Amount, Hit, IsTrue)
	local Args = {}
	for i = 1, tonumber(Amount) do
		if IsTrue then
			Args[#Args + 1] = {
				["RayObject"] = Ray.new(Vector3.new(990.272583, 101.489975, 2362.74878), Vector3.new(-799.978333, 0.23157759, -5.88794518)),
				["Distance"] = 198.9905242919922,
				["Cframe"] = CFrame.new(894.362549, 101.288307, 2362.53491, -0.0123058055, 0.00259522465, -0.999920964, 3.63797837e-12, 0.999996722, 0.00259542116, 0.999924302, 3.19387436e-05, -0.0123057645),
			}
		else
			Args[#Args + 1] = {
				["RayObject"] = Ray.new(Vector3.new(), Vector3.new()),
				["Distance"] = 0,
				["Cframe"] = CFrame.new(),
				["Hit"] = Hit,
			}
		end
	end
	return Args
end
function DragifyGui(Frame,Is)
	coroutine.wrap(function()
		local dragToggle = nil
		local dragSpeed = 0.50
		local dragInput = nil
		local dragStart = nil
		local dragPos = nil
		local startPos = nil
		local function updateInput(input)
			if not Is then
				if not States.DraggableGuis then
					return
				end
			end
			local Delta = input.Position - dragStart
			local Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + Delta.X, startPos.Y.Scale, startPos.Y.Offset + Delta.Y)
			game:GetService("TweenService"):Create(Frame, TweenInfo.new(0.30), {Position = Position}):Play()
		end
		Frame.InputBegan:Connect(function(input)
			if not Is then
				if States.DraggableGuis then
					if (input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch) and game:GetService("UserInputService"):GetFocusedTextBox() == nil then
						dragToggle = true
						dragStart = input.Position
						startPos = Frame.Position
						input.Changed:Connect(function()
							if input.UserInputState == Enum.UserInputState.End then
								dragToggle = false
							end
						end)
					end
				end
			end
		end)
		Frame.InputChanged:Connect(function(input)
			if States.DraggableGuis then
				if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
					dragInput = input
				end
			end
		end)
		game:GetService("UserInputService").InputChanged:Connect(function(input)
			if States.DraggableGuis then
				if input == dragInput and dragToggle then
					updateInput(input)
				end
			end
		end)
	end)()
end
DragifyGui(Out)
DragifyGui(Commands)
DragifyGui(CmdsIcon)
local IsBringing = false
function API:swait()
	game:GetService("RunService").Stepped:Wait()
end
function API:bring(Target,TeleportTo,MoreTP,DontBreakCar)
	local BringingFromAdmin = nil
	if table.find(Temp.Admins,Target.Name) then
		BringingFromAdmin = true
	end
	if not IsBringing and Target and Target.Character:FindFirstChildOfClass("Humanoid") and Target.Character:FindFirstChildOfClass("Humanoid").Health>0 and Target.Character:FindFirstChildOfClass("Humanoid").Sit == false then
		if not TeleportTo then
			TeleportTo = API:GetPosition()
		end
		local Orgin = API:GetPosition()
		local CarPad = workspace.Prison_ITEMS.buttons["Car Spawner"]
		local car = nil
		local Seat = nil
		local Failed = false
		local CheckForBreak = function()
			if not Target or not Target.Character:FindFirstChildOfClass("Humanoid") or Target.Character:FindFirstChildOfClass("Humanoid").Health<1 or Player.Character:FindFirstChildOfClass("Humanoid").Health<1 then
				Failed = true
				return true
			else
				return nil
			end
		end

		for i,v in pairs(game:GetService("Workspace").CarContainer:GetChildren()) do
			if v then
				if v:WaitForChild("Body"):WaitForChild("VehicleSeat").Occupant == nil then
					car = v
				end
			end
		end
		if not car then
			coroutine.wrap(function()
				if not car then
					car = game:GetService("Workspace").CarContainer.ChildAdded:Wait()
				end
			end)()
			repeat wait()
				game:GetService("Players").LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(-524, 55, 1777))
				task.spawn(function()
					workspace.Remote.ItemHandler:InvokeServer(game:GetService("Workspace").Prison_ITEMS.buttons:GetChildren()[7]["Car Spawner"])
				end)
				if CheckForBreak() then
					break
				end
			until car
		end
		car:WaitForChild("Body"):WaitForChild("VehicleSeat")
		car.PrimaryPart = car.Body.VehicleSeat
		Seat = car.Body.VehicleSeat
		repeat wait()
			Seat:Sit(Player.Character:FindFirstChildOfClass("Humanoid"))
		until Player.Character:FindFirstChildOfClass("Humanoid").Sit == true
		wait() --// so it doesnt break
		repeat API:swait()
			if CheckForBreak() or not Player.Character:FindFirstChildOfClass("Humanoid") or Player.Character:FindFirstChildOfClass("Humanoid").Sit == false then
				break
			end
			car.PrimaryPart = car.Body.VehicleSeat
			if Target.Character:FindFirstChildOfClass("Humanoid").MoveDirection.Magnitude >0 then
				car:SetPrimaryPartCFrame(Target.Character:GetPrimaryPartCFrame()*CFrame.new(0,-.2,-6))
			else
				car:SetPrimaryPartCFrame(Target.Character:GetPrimaryPartCFrame()*CFrame.new(0,-.2,-5))
			end
		until Target.Character:FindFirstChildOfClass("Humanoid").Sit == true
		if Failed then
			API:Notif("Failed to bring the player!")
			if BringingFromAdmin then
				local ohString1 = "/w "..Target.Name.." ".."ADMIN: Bring has failed! Try again later."
				local ohString2 = "All"
				game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(ohString1, ohString2)
			end
			return
		end
		for i =1,10 do
			car:SetPrimaryPartCFrame(TeleportT.
