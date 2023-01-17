Datapack Search
https://www.planetminecraft.com/data-packs/

OptiFine alternatives
https://lambdaurora.dev/optifine_alternatives/

Hermits Create server modlist
https://docs.google.com/spreadsheets/d/145JMqoj4sVeOHrK1mEQB6V5z-7UnyLps8zFnO87OcFQ/edit#gid=1383401023

Popular CTM Maps
https://ctmrepository.com/index.php?action=popular


# CTM Tveitacraft spillvert
```
server-name=Tveitacraft_CTM
motd=CTM 1.14.4
level-seed=
level-name=World
```


# Ny Tveitacraft server
```
server-name=Tveitacraft
motd=Vanilla 1.19 (pluss)
level-seed=4006223464530337273
level-name=World5
```


# Ny MODDA Tveitacraft
```
server-name=Tveitacraft_Modda
motd=Custom Modpack for 1.19.2
level-name=World
level-seed=-2112805802007182112
level-seed=-3773098126057437624 <-- heftig start!
```

**MODS:**
Create (+ addons?)
Botania
Storage Drawers
Applied Energistics 2
ChiselsBits
Decorative Blocks

Croptopia ? (needs Patchouli)

_QOL:_
RoughlyEnoughItems
The One Probe
Appleskin
Gravestone

_utils:_
BetterAdvancements
BetterF3
Controlling
ModMenu
Freecam
Beenfo ?

_graphics/performance:_
Sodium
Lithium
Indium
Phosphor

_extra_
Disable Custom Worlds Advice
AttributeFix ?
Better Compatibility Checker


---

# Datapacks!

[When Dungeons Arise](https://www.planetminecraft.com/data-pack/when-dungeons-arise-1-19-datapack/)
[Incendium](https://www.planetminecraft.com/data-pack/incendium-nether-expansion/)
[The Bracken Pack (11 dimensions)](https://www.planetminecraft.com/data-pack/the-bracken-pack/)
[Towns & Towers](https://www.planetminecraft.com/data-pack/towns-amp-towers-structure-overhaul/)


---



## Bedrock og Java sammen?

- https://wiki.geysermc.org/geyser/setup/
- https://github.com/GeyserMC/Geyser


## Geyser testing

spillvert server starting on: 194.242.10.234:25825


---



Curseforge API key
===

$2a$10$TInx1b8bMGXiY56pg1llVuVoGYysbbdK2Zh4LHVit3SVT4Yu3usnC




Configs å tenke på
===

FTB Chunks - default ser ut til å være 500 chunker... kanskje redusere litt hvis kidsa skal være med?



subl --command 'sublimerge_compare_paths' {"paths": ["/home/hjh/MultiMC/instances/[UNUSED] Better-Minecraft-v55.5/minecraft/config", "/home/hjh/MultiMC/instances/Better Minecraft [FORGE] 1.16.5 (spillvert2)/minecraft/config"]}


---


VanillaTweaks
===

DataPacks
==

POST til https://vanillatweaks.net/assets/server/zipdatapacks.php

URL-encoded formData Payload:

  Tveita:
    packs: {"hermitcraft":["thunder shrine","wandering trades"],"mobs":["silence mobs","more mob heads","anti enderman grief"],"items":["player head drops","terracotta rotation wrench","redstone rotation wrench"],"survival":["unlock all recipes","track statistics","track raw statistics","durability ping","armor statues","coordinates hud","multiplayer sleep","afk display"]}
	version: 1.18

  Gaaba:
    packs: {"hermitcraft":["thunder shrine","wandering trades"],"mobs":["dragon drops","double shulker shells","silence mobs","more mob heads","anti enderman grief"],"items":["player head drops","terracotta rotation wrench","redstone rotation wrench"],"survival":["graves","unlock all recipes","track statistics","track raw statistics","durability ping","armor statues","coordinates hud","multiplayer sleep"]}
	version: 1.18


CraftingTweaks
==

POST til https://vanillatweaks.net/assets/server/zipcraftingtweaks.php

URL-encoded formData Payload:
  packs: {"craftables":["craftable coral blocks 2x2"],"quality of life":["universal dyeing","dropper to dispenser"]}
  version: 1.18


ResourcePacks
==

POST til https://vanillatweaks.net/assets/server/zipresourcepacks.php

URL-encoded formData Payload:
  packs: {"gui":["NoJavaEditionTitle"],"options backgrounds":["NetheriteBlockBG"],"hud":["PingColorIndicator"],"unobtrusive":["LowerShield","LowerFire","AlternateEnchantGlint","UnobtrusiveSnow","UnobtrusiveRain"],"utility":["GroovyLevers","Age25Kelp","StickyPistonSides","BetterObservers","DirectionalDispensersDroppers","DirectionalHoppers"],"peace and quiet":["QuieterNetherPortals","QuieterRain"],"terrain":["ShorterTallGrass","ShorterGrass","DarkerDarkOakLeaves","BushyLeaves"]}
  version: 1.18

