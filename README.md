local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Window = OrionLib:MakeWindow({Name = "Jupiter Horizon", HidePremium = false, SaveConfig = true, ConfigFolder = "Jupiter Horizon"})

_G.speed = true
_G.fakespeed = true

--fonction--

function speed()
    while _G.speed == true do
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = _G.fakespeed
wait()
    end
end

--menu--

local baguette = Window:MakeTab({
	Name = "Player",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Credits = Window:MakeTab({
	Name = "Credits",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

--intéractive--

baguette:AddSlider({
	Name = "player speed",
	Min = 16,
	Max = 100,
	Default = 16,
	Color = Color3.fromRGB(255,255,255),
	Increment = 1,
	ValueName = "power",
	Callback = function(Value)
		_G.fakespeed = Value
        speed()
	end    
})

