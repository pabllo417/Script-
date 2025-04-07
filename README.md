
-- Configurações
local player = game.Players.LocalPlayer
local character = player.Character

-- Funções
local function criarMenu()
    local menu = Instance.new("ScreenGui")
    menu.Name = "Menu"
    menu.Parent = game.StarterGui

    local frame = Instance.new("Frame")
    frame.Name = "Frame"
    frame.Parent = menu
    frame.BackgroundColor3 = Color3.new(0, 0, 0)
    frame.BackgroundTransparency = 0.5
    frame.Size = UDim2.new(0, 200, 0, 200)

    local texto = Instance.new("TextLabel")
    texto.Name = "Texto"
    texto.Parent = frame
    texto.Text = "Bem-vindo ao menu!"
    texto.Font = Enum.Font.SourceSansBold
    texto.FontSize = Enum.FontSize.Size24
    texto.TextColor3 = Color3.new(1, 1, 1)

    local botao = Instance.new("TextButton")
    botao.Name = "Botao"
    botao.Parent = frame
    botao.Text = "Clique aqui!"
    botao.Font = Enum.Font.SourceSansBold
    botao.FontSize = Enum.FontSize.Size18
    botao.TextColor3 = Color3.new(1, 1, 1)
    botao.BackgroundColor3 = Color3.new(0, 1, 0)
end

-- Eventos
game:GetService("UserInputService").InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode.F1 then
        criarMenu()
    end
end)# Script-
