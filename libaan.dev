local TextChatService = game:GetService("TextChatService")
local Players = game:GetService("Players")
local player = Players.LocalPlayer
local channel = TextChatService.TextChannels and TextChatService.TextChannels.RBXGeneral

local words = {
    "CHUDðŸ¤£",
    "DAFANðŸ¥€ðŸ™ðŸ»",
    "RNDIðŸ¥±",
    "TMKXðŸ¤£ðŸ¥€",
    "ROO MATðŸ˜‚"
}

local index = 1
local enabled = false

-- ===== Mobile GUI =====
local gui = Instance.new("ScreenGui")
gui.Name = "SpamToggleGUI"
gui.ResetOnSpawn = false
gui.Parent = player:WaitForChild("PlayerGui")

local btn = Instance.new("TextButton")
btn.Size = UDim2.fromScale(0.35, 0.08)
btn.Position = UDim2.fromScale(0.325, 0.85)
btn.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
btn.TextColor3 = Color3.fromRGB(255, 255, 255)
btn.TextScaled = true
btn.Text = "SPAM: OFF"
btn.Parent = gui
btn.BorderSizePixel = 0
btn.AutoButtonColor = true

btn.MouseButton1Click:Connect(function()
    enabled = not enabled
    btn.Text = enabled and "SPAM: ON" or "SPAM: OFF"
end)

-- ===== Spam Loop =====
while true do
    if enabled and channel then
        local message =
            "~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~" ..
            "LIBBU H8ERS " .. words[index] .. " ðŸ¤£ðŸ¥€ðŸ™ðŸ»"

        local success, err = pcall(function()
            channel:SendAsync(message)
        end)
        if not success then
            warn("Failed to send message:", err)
        end

        index = index + 1
        if index > #words then
            index = 1
        end
    end
    task.wait(2)
end
