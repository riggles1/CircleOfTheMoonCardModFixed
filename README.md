# CircleOfTheMoonCardModFixed
I created this git as some people had trouble applying the individual patches (probably related to order applied)
Original Castlevania Circle of the Moon (USA).gba CRC32: 1cc059a4
Patched file CRC32: a9e88e55

This .bps patch has the Card Hack CardUpV3 combined with the following:

NoDSSDrops.ips This patch replaces enemy drops that included DSS cards. 
(Restores the changed drops for potions and meat in the cardup hack, making them drop normally instead at an absurdly high rate).
Devil also drops the Shining Armor (1% drop iirc), as the last card is gotten from the battle arena instead of this armor.

CardCombosRevealed.ips This patch reveals card combination descriptions instead of showing "???" 
until the combination is used. 

CandleFix.ips In lategame, the Trick Candle and Scary Candle load in the Cerberus 
and Iron Golem boss rooms after defeating Camilla and Twin Dragon Zombies respectively. 
If the former bosses have not yet been cleared (i.e., we have sequence broken the 
game and returned to the earlier boss rooms to fight them), the candle enemies will 
cause the bosses to fail to load and soft lock the game.
This patches the candles to appear after the early boss is completed instead. 

GameClearBypass.ips Normally, you must clear the game with each mode to unlock subsequent modes, 
and complete the game at least once to be able to skip the introductory text crawl. 
This allows all game modes to be selected and the introduction to be skipped even without game/mode completion. 

DSSGlitchFix.ips Optional patch created by Fusecavator. Prohibits the DSS glitch. 
You will not be able to update the active effect unless the card combination switched to 
is obtained. For example, if you switch to another DSS combination that you have not obtained 
during DSS startup, you will still have the effect of the original combination you had selected 
when you started the DSS activation. In addition, you will not be able to increase damage and/or 
change the element of a summon attack unless you possess the cards you swap to.

MPComboFix.ips Normally, the MP boosting card combination is useless since it depletes more MP 
than it gains. This patch makes it consume zero MP.

SoftlockBlockFix.ips A Tackle block in Machine Tower will cause a softlock if you access the Machine Tower 
from the Abyss Stairway using the stone tower route with Kick Boots and not Double. 
This is a small level edit that moves that block slightly, removing the potential for a softlock.

Patches are taken from the randomizer git, Credit to calm-palm for these:
https://github.com/calm-palm/cotm-randomizer/tree/master/Program/ips
