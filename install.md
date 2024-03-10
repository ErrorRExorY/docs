# GuardianV - Documentation

> [GuardianV](https://guardianv.de/) AntiCheat, definieren Sie Ihr FiveM-Erlebnis neu.

## Installation

### Download

Download the latest version of GuardianV from FiveM [Keymaster-Assets](https://keymaster.fivem.net/assets?search=GuardianV)


![](/img/image4.png)

### Redeem the License you got via Email

You'll get an email wich will contain a key based on the model you chose.

Go to [Licenses] (https://guardianv.de/license) as shown down below and your Resource is almost ready to start and ban some cheaters!

![](/img/licenses.png)



### Extract and Copy
Extract the zip and you will get something like this:

![](/img/image.png)


#### Copy into resources/

Now you have to copy the whole extracted `'GUARDIANV'` folder into your `resources/` folder.

>NOTE: The foldername has to stay like it is, otherwise the Resource will not work.


## Configuration

### Basic Informations

>We are currently assuming that you already added GUARDIANV to your servers .cgf file.

In the extraxted `GUARDIANV` folder on your server, there are only two files which are in interest of yours. 

They are located in the subfolder configs (as shown below):

![](/img/image2.png)

![](/img/image3.png)

>You can set the values inside, but keep in mind, if you dont set `GUARDIANV.Local = true`
the values will get replaced with the ones from the Cloudpanel.

### Cloudpanel

You will have to get your ApiKey from the Profile-Page and your Username in order to sync the config with the Cloudpanel
![](/img/7.png)


>It's recommended to use the Cloudpanel. Alot of features are coming soon.
![](/img/1.png)
![](/img/2.png)
![](/img/3.png)
![](/img/4.png)
![](/img/5.png)
![](/img/6.png)

### Basic config.lua

```
GUARDIANV                          = {}

GUARDIANV.ApiKey = ""
GUARDIANV.Username = ""

--【 𝗩𝗲𝗿𝘀𝗶𝗼𝗻 𝗖𝗵𝗲𝗰𝗸 】--
GUARDIANV.Version                  = "7.0.0"

--【 𝗦𝗲𝗿𝘃𝗲𝗿 𝗦𝗲𝘁𝘁𝗶𝗻𝗴𝘀 】--
GUARDIANV.ServerConfig             = {
    Name = "TestServer",
    Port  = 30120
}

--【 𝗖𝗵𝗮𝘁 𝗦𝗲𝘁𝘁𝗶𝗻𝗴𝘀 】--
GUARDIANV.ChatSettings             = {
    Enable      = true,
    PrivateWarn = true,
}

--【 𝗦𝗰𝗿𝗲𝗲𝗻𝗦𝗵𝗼𝘁 】--
GUARDIANV.ScreenShot               = {
    Enable  = true,
    Format  = "PNG",
    Quality = 1,
}

--【 𝗖𝗼𝗻𝗻𝗲𝗰𝘁𝗶𝗼𝗻 𝗦𝗲𝘁𝘁𝗶𝗻𝗴𝘀 】--
GUARDIANV.Connection               = {
    AntiBlackListName = false,
    AntiVPN  = false,
    HideIP = false
}

--【 𝗠𝗲𝘀𝘀𝗮𝗴𝗲 】--
GUARDIANV.Message                  = {
    Kick = "⚡️You are kicked from the Server!⚡️ Protection By GUARDIANV®. Don't Try to Cheat on this Server",
    Ban  = "⛔️You are banned from the Server!⛔️ Please create a Supportticket on our Server, if you think this was a mistake"
}

--【 𝗔𝗱𝗺𝗶𝗻 𝗠𝗲𝗻𝘂 】--
GUARDIANV.AdminMenu                = {
    Enable         = true,
    Key            = "F9",
    MenuPunishment = "BAN",
}

--【 𝗔𝗻𝘁𝗶 𝗧𝗿𝗮𝗰𝗸 𝗣𝗹𝗮𝘆𝗲𝗿 】--
GUARDIANV.AntiTrackPlayer          = true
GUARDIANV.MaxTrack                 = 10
GUARDIANV.TrackPunishment          = "KICK"                                        

--【 𝗔𝗻𝘁𝗶 𝗛𝗲𝗮𝗹𝘁𝗵 𝗛𝗮𝗰𝗸 】--
GUARDIANV.AntiHealthHack           = true
GUARDIANV.MaxHealth                = 200
GUARDIANV.HealthPunishment         = "KICK"     

--【 𝗔𝗻𝘁𝗶 𝗔𝗿𝗺𝗼𝗿 𝗛𝗮𝗰𝗸 】--
GUARDIANV.AntiArmorHack            = true
GUARDIANV.MaxArmor                 = 100
GUARDIANV.ArmorPunishment          = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗧𝗮𝘀𝗸𝘀 】--
GUARDIANV.AntiBlacklistTasks       = true
GUARDIANV.TasksPunishment          = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗣𝗹𝗮𝘆 𝗔𝗻𝗶𝗺𝘀 】--
GUARDIANV.AntiBlacklistAnims       = true
GUARDIANV.AnimsPunishment          = "KICK"  

--【 𝗦𝗮𝗳𝗲 𝗣𝗹𝗮𝘆𝗲𝗿𝘀 】--
GUARDIANV.SafePlayers              = true
GUARDIANV.AntiInfinityAmmo         = true

--【 𝗔𝗻𝘁𝗶 𝗦𝗽𝗲𝗰𝘁𝗮𝘁𝗲 】--
GUARDIANV.AntiSpectate             = true
GUARDIANV.SpactatePunishment       = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗪𝗲𝗮𝗽𝗼𝗻 】--
GUARDIANV.AntiBlackListWeapon      = true
GUARDIANV.AntiAddWeapon            = true
GUARDIANV.AntiRemoveWeapon         = true
GUARDIANV.AntiWeaponsExplosive     = true
GUARDIANV.WeaponPunishment         = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗚𝗼𝗱𝗠𝗼𝗱𝗲 】--
GUARDIANV.AntiGodMode              = true
GUARDIANV.GodPunishment            = "BAN"                                                            

--【 𝗔𝗻𝘁𝗶 𝗜𝗻𝘃𝗶𝘀𝗶𝗯𝗹𝗲 】--
GUARDIANV.AntiInvisible            = true
GUARDIANV.InvisiblePunishment      = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗖𝗵𝗮𝗻𝗴𝗲 𝗦𝗽𝗲𝗲𝗱 】--
GUARDIANV.AntiChangeSpeed          = true
GUARDIANV.SpeedPunishment          = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗙𝗿𝗲𝗲 𝗖𝗮𝗺 】--
GUARDIANV.AntiFreeCam              = true
GUARDIANV.CamPunishment            = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗥𝗮𝗶𝗻𝗯𝗼𝘄 𝗩𝗲𝗵𝗶𝗰𝗹𝗲 】--
GUARDIANV.AntiRainbowVehicle       = true
GUARDIANV.RainbowPunishment        = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗣𝗹𝗮𝘁𝗲 】--
GUARDIANV.AntiPlateChanger         = true
GUARDIANV.AntiBlackListPlate       = true
GUARDIANV.PlatePunishment          = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗩𝗶𝘀𝗶𝗼𝗻 】--
GUARDIANV.AntiNightVision          = true
GUARDIANV.AntiThermalVision        = true
GUARDIANV.VisionPunishment         = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗦𝘂𝗽𝗲𝗿 𝗝𝘂𝗺𝗽 】--
GUARDIANV.AntiSuperJump            = true
GUARDIANV.JumpPunishment           = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗧𝗲𝗹𝗲𝗽𝗼𝗿𝘁 】--
GUARDIANV.AntiTeleport             = true
GUARDIANV.MaxFootDistance          = 200
GUARDIANV.MaxVehicleDistance       = 600
GUARDIANV.TeleportPunishment       = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗡𝗼𝗰𝗹𝗶𝗽 】--
GUARDIANV.AntiNoclip               = true
GUARDIANV.NoclipPunishment         = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗣𝗲𝗱 𝗖𝗵𝗮𝗻𝗴𝗲𝗿 】--
GUARDIANV.AntiPedChanger           = true
GUARDIANV.PedChangePunishment      = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗜𝗻𝗳𝗶𝗻𝗶𝘁𝗲 𝗦𝘁𝗮𝗺𝗶𝗻𝗮 】--
GUARDIANV.AntiInfiniteStamina      = true
GUARDIANV.InfinitePunishment       = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗥𝗮𝗴𝗱𝗼𝗹𝗹 】--
GUARDIANV.AntiRagdoll              = true
GUARDIANV.RagdollPunishment        = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗠𝗲𝗻𝘆𝗼𝗼 】--
GUARDIANV.AntiMenyoo               = true
GUARDIANV.MenyooPunishment         = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗔𝗶𝗺 𝗔𝘀𝘀𝗶𝘀𝘁 】--
GUARDIANV.AntiAimAssist            = true
GUARDIANV.AimAssistPunishment      = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗥𝗲𝘀𝗼𝘂𝗿𝗰𝗲 】--
GUARDIANV.AntiResourceStopper      = true
GUARDIANV.AntiResourceStarter      = true
GUARDIANV.AntiResourceRestarter    = true
GUARDIANV.ResourcePunishment       = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗖𝗵𝗮𝗻𝗴𝗲 𝗙𝗹𝗮𝗴 】--
GUARDIANV.AntiTinyPed              = true
GUARDIANV.PedFlagPunishment        = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗦𝘂𝗶𝗰𝗶𝗱𝗲 】--
GUARDIANV.AntiSuicide              = true
GUARDIANV.SuicidePunishment        = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗖𝗼𝗹𝗹𝗲𝗰𝘁𝗲𝗱 𝗣𝗶𝗰𝗸𝘂𝗽 】--
GUARDIANV.AntiPickupCollect        = true
GUARDIANV.PickupPunishment         = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗖𝗵𝗮𝘁 】--
GUARDIANV.AntiSpamChat             = true
GUARDIANV.MaxMessage               = 10
GUARDIANV.CoolDownSec              = 3
GUARDIANV.ChatPunishment           = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗖𝗼𝗺𝗺𝗮𝗻𝗱 】--
GUARDIANV.AntiBlackListCommands    = true
GUARDIANV.CMDPunishment            = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗖𝗵𝗮𝗻𝗴𝗲 𝗗𝗮𝗺𝗮𝗴𝗲 】--
GUARDIANV.AntiWeaponDamageChanger  = true
GUARDIANV.AntiVehicleDamageChanger = true
GUARDIANV.DamagePunishment         = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗪𝗼𝗿𝗱 】--
GUARDIANV.AntiBlackListWord        = true
GUARDIANV.WordPunishment           = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗕𝗿𝗶𝗻𝗴 𝗔𝗹𝗹 】--
GUARDIANV.AntiBringAll             = true
GUARDIANV.BringAllPunishment       = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗧𝗿𝗶𝗴𝗴𝗲𝗿 】--
GUARDIANV.AntiBlackListTrigger     = true
GUARDIANV.AntiSpamTrigger          = true
GUARDIANV.TriggerPunishment        = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗖𝗹𝗲𝗮𝗿 𝗣𝗲𝗱 𝗧𝗮𝘀𝗸𝘀 】--
GUARDIANV.AntiClearPedTasks        = true
GUARDIANV.MaxClearPedTasks         = 5
GUARDIANV.CPTPunishment            = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗧𝗮𝘇𝗲 𝗣𝗹𝗮𝘆𝗲𝗿𝘀 】--
GUARDIANV.AntiTazePlayers          = true
GUARDIANV.MaxTazeSpam              = 3
GUARDIANV.TazePunishment           = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗜𝗻𝗷𝗲𝗰𝘁 】--
GUARDIANV.AntiInject               = true
GUARDIANV.InjectPunishment         = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗘𝘅𝗽𝗹𝗼𝘀𝗶𝗼𝗻 】--
GUARDIANV.AntiBlackListExplosion   = true
GUARDIANV.AntiExplosionSpam        = true
GUARDIANV.MaxExplosion             = 10
GUARDIANV.ExplosionSpamPunishment  = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗘𝗻𝘁𝗶𝘁𝘆 𝗦𝗽𝗮𝘄𝗻𝗲𝗿 】--
GUARDIANV.AntiBlackListObject      = true
GUARDIANV.AntiBlackListPed         = true
GUARDIANV.AntiBlackListBuilding    = true
GUARDIANV.AntiBlackListVehicle     = true
GUARDIANV.EntityPunishment         = "BAN"                                                            

--【 𝗔𝗻𝘁𝗶 𝗘𝗻𝘁𝗶𝘁𝘆 𝗦𝗽𝗮𝗺𝗲𝗿 】--
GUARDIANV.AntiSpawnNPC             = true

GUARDIANV.AntiSpamVehicle          = true
GUARDIANV.MaxVehicle               = 10

GUARDIANV.AntiSpamPed              = true
GUARDIANV.MaxPed                   = 4

GUARDIANV.AntiSpamObject           = true
GUARDIANV.MaxObject                = 15

GUARDIANV.SpamPunishment           = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗖𝗵𝗮𝗻𝗴𝗲 𝗣𝗲𝗿𝗺 】--
GUARDIANV.AntiChangePerm           = true
GUARDIANV.PermPunishment           = "KICK"  

--【 𝗔𝗻𝘁𝗶 𝗣𝗹𝗮𝘆 𝗦𝗼𝘂𝗻𝗱 】--
GUARDIANV.AntiPlaySound            = true
GUARDIANV.SoundPunishment          = "KICK"  

```