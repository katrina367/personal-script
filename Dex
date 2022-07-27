local loaded, dex = pcall(game.GetObjects, game, "rbxassetid://3567096419")
if not loaded or (loaded and (not dex[1] or typeof(dex[1]) ~= "Instance")) then
    return warn(not loaded and dex or "Failed to load '3567096419'")
end
dex = dex[1]
if syn and type(syn) == "table" and syn.protect_gui and type(syn.protect_gui) == "function" then
    pcall(syn.protect_gui, dex)
end
math.randomseed(os.clock())
local name = ""
for _ = 1, math.random(24, 33) do
    name = name .. string.char(math.random(33, 126))
end
dex.Name = name
dex.Parent = (get_hidden_ui and get_hidden_ui()) or (gethui and gethui()) or (get_hidden_gui and get_hidden_gui()) or game:GetService("CoreGui")
local meta = {__index = getfenv()}
local function sandbox(v)
    task.spawn(setfenv(loadstring(v.Source, "=" .. v:GetFullName()), setmetatable({script = v}, meta)))
end
if dex:IsA("LuaSourceContainer") then
    sandbox(v)
end
for _, v in ipairs(dex:GetDescendants()) do
    if v:IsA("LuaSourceContainer") then
        sandbox(v)
    end
end
return dex
