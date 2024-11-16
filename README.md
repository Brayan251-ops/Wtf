local autoFarmEnabled = true
local desiredItems = {"Fruit", "Money", "Exp"}

local function collectItems()
    for _, item in pairs(game:GetDescendants()) do
        if table.contains(desiredItems, item.Name) then
            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = item.CFrame
            wait(0.5)
        end
    end
end

-- Main loop
while true do
    if autoFarmEnabled then
        collectItems()
    end
    wait(1)
end
