local Logo1 = "rbxassetid://15298567397";
local Logo2 = "rbxassetid://17382040552";

local Name = "Ghost Hub : Blox Fruits";
local Folder = "GhostHub-BloxFruits.json";
local Credits = "By GhostHub";
local DiscordInvite = "https://discord.gg/7aR7kNVt4g";

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/realredz/RedzLibV5/refs/heads/main/Source.lua"))()
local Window = Library:MakeWindow({Name, Credits, Folder})
  
local Tabs = {

  MainFarm = Window:MakeTab({"Farm", "Home"}),
  Sea = Window:MakeTab({"Sea", "Waves"}),
,
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








  })
  
  Discord:AddSection("")
  Discord:AddParagraph({"Mentions:\n Honorable Mention: acsu123\n Honorable Mention 2: XFister"})
end
