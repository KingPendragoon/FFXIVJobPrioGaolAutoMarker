**Set Up**

You need triggernometry for this Version 1.1.4.1 Or higher: https://github.com/paissaheavyindustries/Triggernometry

Please make sure that Default party sort is enabled in FF (Tank, Healer, DPS)
![alt text](https://github.com/KingPendragoon/FFXIVJobPrioGaolAutoMarker/blob/main/InGamePartyOrder.png?raw=true)

In triggernometry it is configured under "Options > Edit Configuration > Final Fantasy XIV" that player list set to "Custom Order" and is in the proper order as well of Tanks, Healers, DPS. 

 ![alt text](https://github.com/KingPendragoon/FFXIVJobPrioGaolAutoMarker/blob/main/PartyListTriggerStep1.png?raw=true)
 
 ![alt text](https://github.com/KingPendragoon/FFXIVJobPrioGaolAutoMarker/blob/main/PartyListTriggerStep2.png?raw=true)
 
 ![alt text](https://github.com/KingPendragoon/FFXIVJobPrioGaolAutoMarker/blob/main/PartyListTriggerStep3.png?raw=true)
 

The following Macros will need to be created and added to the F1-F9 keys

F1: /mk attack <1>

F2: /mk attack <2>

F3: /mk attack <3>

F4: /mk attack <4>

F5: /mk attack <5>

F6: /mk attack <6>

F7: /mk attack <7>

F8: /mk attack <8>



F9

/mk clear <1>
/mk clear <2>
/mk clear <3>
/mk clear <4>
/mk clear <5>
/mk clear <6>
/mk clear <7>
/mk clear <8>


**Testing**
If you want to test if the plugin works before you reach the fight by running those echo's you will need to go to
Regular expressions in the "Players and Jobs" tab and replace the regular expression there with the following. 

`\[.{22}15:[A-F0-9]{8}:[^:]*:2B6[BC]:[^:]*:[A-F0-9]{8}:(?<name>[a-zA-Z-' ]{1,31}):` 
  
You will then need to make a macro with the following text and replace "Name1-Name3" with the players name.  Make sure the line ends with a colon `:`

**You will need an 8 man party in the same instance for the test to work.**

`/e 15:88888888:Titan:2B6C:Rock Throw:88888888:Name1:`
`/e 15:88888888:Titan:2B6C:Rock Throw:88888888:Name2:`
`/e 15:88888888:Titan:2B6C:Rock Throw:88888888:Name3:`

For live testing the regular expression in "Players and Jobs" needs to be
  
`\[.{14}15:[A-F0-9]{8}:[^:]*:2B6[BC]:[^:]*:[A-F0-9]{8}:(?<name>[a-zA-Z-'  ]{1,31}):`

**Editing**

If you wish to Edit the Keybindings from F1-F9 you will need to go into Mark1-3 as well as Wipe Reset. Change keycode for each trigger (25 in total, 8 in each Mark1-3 and one in Wipe reset) to the desired keybinding. Reference https://docs.microsoft.com/en-us/dotnet/api/system.windows.forms.keys?view=net-5.0 for Keycodes.
![alt text](https://github.com/KingPendragoon/FFXIVJobPrioGaolAutoMarker/blob/main/HowToEditKeybinding.png?raw=true)

![alt text](https://github.com/KingPendragoon/FFXIVJobPrioGaolAutoMarker/blob/main/WipeResetMarker.png?raw=true)

If you wish to edit the priority list you will need to go into each of the triggers 
Job1Priority-Job3Priority and change the numbers assigned to them there
  
MNK: 1

DRG: 2
 
NIN: 3 
 
SAM: 4 
 
PLD: 5 
 
WAR: 6 
 
DRK: 7 
 
GNB: 8  

BRD: 9 
 
MCH: 10 
 
DNC: 11 
 
BLM: 12 
 
SMN: 13 
 
RDM: 14 
 
WHM: 15 
 
SCH: 16 
 
AST: 17
