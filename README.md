local Logo1 = "rbxassetid://15298567397";
local Logo2 = "rbxassetid://17382040552";

local Name = "Ghost Hub : Blox Fruits";
local Folder = "GhostHub-BloxFruits.json";
local Credits = "By GhostHub";
local DiscordInvite = "https://discord.gg/7aR7kNVt4g";

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/realredz/RedzLibV5/refs/heads/main/Source.lua"))()
local Window = Library:MakeWindow({Name, Credits, Folder})
  
local Tabs = {
  Discord = Window:MakeTab({"Discord", "Info"}),
  MainFarm = Window:MakeTab({"Farm", "Home"}),
  local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoidRootPart = character:FindFirstChild("HumanoidRootPart")
local tool = player.Backpack:FindFirstChildOfClass("Tool")

if not tool then
    print("Nenhuma arma encontrada! Equipe uma antes de executar o script.")
    return
end

-- Auto Attack Loop
while wait(0.5) do
    local enemies = game.Workspace.Enemies:GetChildren()
    for _, enemy in pairs(enemies) do
        if enemy:FindFirstChild("HumanoidRootPart") and enemy:FindFirstChild("Humanoid") then
            if enemy.Humanoid.Health > 0 then
                humanoidRootPart.CFrame = enemy.HumanoidRootPart.CFrame * CFrame.new(0, 0, 3)
                tool:Activate()
                wait(0.2)
            end
        end
    end
end

  Sea = Window:MakeTab({"Sea", "Waves"}),
  RaceV4 = Window:MakeTab({"Race-V4", ""}),
  Islands = Window:MakeTab({"Islands", "PalmTree"}),
  Items = Window:MakeTab({"Quests/Items", "Swords"}),
  FruitRaid = Window:MakeTab({"Fruit/Raid", "Cherry"}),
  Stats = Window:MakeTab({"Stats", "Signal"}),
  Teleport = Window:MakeTab({"Teleport", "Locate"}),
  Status = Window:MakeTab({"Status", "scroll"}),
  Visual = Window:MakeTab({"Visual", "User"}),
  Shop = Window:MakeTab({"Shop", "ShoppingCart"}),
  Misc = Window:MakeTab({"Misc", "Settings"})
}

Window:SelectTab(Tabs.MainFarm)

Window:AddMinimizeButton({
  Button = { Image = Logo1, BackgroundTransparency = 0 },
  Corner = { CornerRadius = UDim.new(0, 6) }
})

local Discord = Tabs.Discord do
  -- Join our discord community to receive Information about the next update, leaks, and Information about Blox Fruits!
  Discord:AddDiscordInvite({
    Name = "Ghost Hub | Community",
    Description = "Join our discord community to receive information about the next update",
    Logo = Logo2,
    Invite = DiscordInvite
  })
  
  Discord:AddSection("")
  Discord:AddParagraph({"Mentions:\n Honorable Mention: acsu123\n Honorable Mention 2: XFister"})
end
