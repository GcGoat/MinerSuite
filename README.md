# MinerSuite

## Instalation

This is 2 part instalation, one for mining site where your miners are at and one for your dynamic core, aka ship.

### Mining site setup
 You will need:
   * ProgramableBoard
   * Receiver
   * Emmiter

Copy/paste LUA code from HERE into your Programable board (PB), from PB link to all elements, which would be: receiver, emmitter, container (or hub) and all mining units  

**Attention #1** You will need to link FROM receiver to PB in adition to linking PB to receiver, it will have blue and green links between these 2 elements 

Now right click PB and enter into "Edit Lua Parameters" there are 2 ESSENTIAL values you need to update
 * **flowerName** - this defines entire mining flower with unique name, this will allow us to group miners in same area for simpler visualization
 * **emitterChannel** - is unique name you came up to separate your miners from everyone else, make it as unique as posible and keep it same across all your mining sites  

**Attention #2** Mining site core name needs to be unique for this entire flower, so name it acordingly. You can use names like "Coal_1" (without quotes) and then second one like "Coal_2". Format of the name isint essential, but try to keep it short

### Ship setup
 You will need:
   * ProgramableBoard
   * Receiver
   * Emmiter
   * Screen (optional)
   * DataBank

Copy/paste LUA code from HERE into your Programable board (PB). FIRST LINK goes to receiver, remaining can go in any order. So links from PB goes to: Receiver, Emmiter, Databank and Screen.
  
**Attention #1** You will need to link FROM receiver to PB in adition to linking PB to receiver, same as it was for mining site, it will have blue and green links between these 2 elements 
  
Now right click PB and enter into "Edit Lua Parameters" there is only one ESSENTIAL value you need to update
 * **emitterChannel** - same channel name you used for mining sites
   
Adiotional options you need to adjust
* **containerProficiency** - value between 1 and 5 based on your talents levels
* **containerOptimization** - value between 1 and 5 based on yoru talents levels
  
Without providing correct values it will report incorrect container values, will not effect miner status
  
Optionally change **minimalCalibration** value to whatever value you want between 0 and 100. This determines timer report when recalibaration will be needed to keep it above defined percentage amount. 

### Done
At this point you are fully setup and you can startup PB on your ship. Screen should be blank but turn on. Now you will only need to turn on Mining Site PB once, just turn it on and off. (At this time you will need to relaunch ships PB for new mining site to appear).  
When that's done you should get AR mode on you screen showing detected miners and container with their status. Repeat Mining site setup for every mining site you have. This is one time setup, after that mining site status will be updated automatically each time you visit it to calibrate while having ship PB enabled. 
 

