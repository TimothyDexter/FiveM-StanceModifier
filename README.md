Disclaimer:

To utilize these file(s) you will need to strip project methods (mostly logging) and compile a .dll to use a resource on your server.  Otherwise, you are best served using the source code to derive your own implementation in the language of your choice.

Stance modifier (crouch and prone) for GTA V: FiveM

 * Usage 
  * Control.Duck (Ctrl) is used to modify stance.  
  * Holding Ctrl while in Idle, Stealth, or Crouch will immediately transfer to Prone 
  * Player will dive if transferring to prone while sprinting
  * Control.Sprint (Shift) while prone will toggle between on front and on back
  * Control.Jump (Space) will set the stance state back to Idle
  * States: Idle -> Stealth -> Crouch -> Prone -> Idle
  * If you want to go from Prone -> Crouch -> Stealth -> Idle use below for Prone -> Crouch transition:
       await Game.PlayerPed.Task.PlayAnimation("get_up@directional@transition@prone_to_knees@crawl",
           "front", 8f, -8f, -1, AnimationFlags.None, 0);
           
