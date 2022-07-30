local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Player = game.Players.LocalPlayer
local Window = OrionLib:MakeWindow({Name = "Key Sistem", HidePremium = false, SaveConfig = true, IntroEnabled = false})

OrionLib:MakeNotification({
	Name = "Loggin!"..Player.Name..".",
	Content = "EnterCorrectKey",
	Image = "rbxassetid://4483345998",
	Time = 5
})

_G.Key = "hitfodaskdkawsm!@#$"
_G.KeyInput = "string"

function MakeScriptHub()
    local Roblox = loadstring(game:HttpGet(('https://raw.githubusercontent.com/amonguscode/Roblox/main/README.md')))()
    local Window = Roblox:MakeWindow({Name = "Roblox", HidePremium = false, SaveConfig = true, IntroEnabled = false, IntroText = "Roblox"})
end

function CorrectKeyNotification()  
    OrionLib:MakeNotification({
	Name = "CorrectKey!",
	Content = "You have entered the correct key!",
	Image = "rbxassetid://4483345998",
	Time = 5
})
end

function InCorrectKeyNotification()  
    OrionLib:MakeNotification({
	Name = "Incorrect Key!",
	Content = "You have entered the incorrect key",
	Image = "rbxassetid://4483345998",
	Time = 5
})
    
    end

local Tab = Window:MakeTab({
	Name = "Key",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddTextbox({
	Name = "Enter Key",
	Default = "",
	TextDisappear = true,
	Callback = function(Value)
	_G.KeyInput = Value
	end	  
})

Tab:AddButton({
	Name = "Check Key!",
	Callback = function()
      		if _G.KeyInput == _G.Key then
      		    MakeScriptHub()
                CorrectKeyNotification()
            else
                IncorrectKeyNotification()
      	end
  	end    
})


