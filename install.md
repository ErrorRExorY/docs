# GuardianV - Documentation

> [GuardianV](https://guardianv.de/) AntiCheat, definieren Sie Ihr FiveM-Erlebnis neu.

## Installation

### Download

Download the latest version of GuardianV from FiveM [Keymaster-Assets](https://keymaster.fivem.net/assets?search=GuardianV)


![](/img/image4.png)

### Redeem the License you got via Email

You'll get an email wich will contain a key based on the model you chose.

Go to [Licenses](https://guardianv.de/license) as shown down below and your Resource is almost ready to start and ban some cheaters!

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
GuardianV              = {}

GuardianV.ApiKey = "0"
GuardianV.Username = ""

-- GuardianV Version
GuardianV.Version      = "1.1.0"

-- Server Configuration
GuardianV.ServerConfig = {
    Name = "Mein Server",
    Port  = 30120
}

-- ACE
GuardianV.ACE             = {
    Enable = true,
    Admin = "GuardianV.Admin",
    Bypass = "GuardianV.Bypass",
    Unban = "GuardianV.Unban"
}

-- Chat Settings
GuardianV.ChatSettings             = {
    Enable      = true, -- Enable chat features
    PrivateWarn = true  -- Warn players for private messages
}

-- Screenshot Settings
GuardianV.ScreenShot               = {
    Enable  = true,  -- Enable screenshot feature
    Format  = "PNG", -- Screenshot format
    Quality = 1      -- Screenshot quality
}

-- Connection Settings
GuardianV.Connection               = {
    AntiBlackListName = true,
    AntiVPN  = true,
    HideIP = true
}

-- Spawn Settings
GuardianV.Spawn                    = {
    LongSpawnMode = true -- Enable long spawn mode
}

-- Message Settings
GuardianV.Message                  = {
    Kick = "⚡️😮‍💨You are kicked from the Server!⚡️ Protection By GUARDIANV®. Don't Try to Cheat on this Server",
    Ban  = "⛔️😮‍💨You are banned from the Server!⛔️ Please create a Supportticket on our Server, if you think this was a mistake"
}

-- Admin Menu Settings
GuardianV.AdminMenu                = {
    Enable         = true, -- Enable admin menu
    Key            = "F9", -- Admin menu activation key
    MenuPunishment = "KICK" -- Punishment for unauthorized access
}

-- Anti-Track Player Settings
GuardianV.AntiTrackPlayer          = true
GuardianV.MaxTrack                 = 10
GuardianV.TrackPunishment          = "WARN"

-- Anti-Health Hack Settings
GuardianV.AntiHealthHack           = true
GuardianV.MaxHealth                = 200
GuardianV.HealthPunishment         = "KICK"

-- Anti-Armor Hack Settings
GuardianV.AntiArmorHack            = true
GuardianV.MaxArmor                 = 100
GuardianV.ArmorPunishment          = "KICK"

-- Anti-Blacklist Tasks Settings
GuardianV.AntiBlacklistTasks       = true
GuardianV.TasksPunishment          = "KICK"

-- Anti-Blacklist Anims Settings
GuardianV.AntiBlacklistAnims       = true
GuardianV.AnimsPunishment          = "KICK"

-- Safe Players Settings
GuardianV.SafePlayers              = true
GuardianV.AntiInfinityAmmo         = true

-- Anti-Spectate Settings
GuardianV.AntiSpectate             = true
GuardianV.SpectatePunishment       = "KICK"

-- Anti-BlackList Weapon Settings
GuardianV.AntiBlackListWeapon      = true
GuardianV.AntiAddWeapon            = true
GuardianV.AntiRemoveWeapon         = true
GuardianV.AntiWeaponsExplosive     = true
GuardianV.WeaponPunishment         = "KICK"

-- Anti-God Mode Settings
GuardianV.AntiGodMode              = true
GuardianV.GodPunishment            = "BAN"

-- Anti-Invisible Settings
GuardianV.AntiInvisible            = true
GuardianV.InvisiblePunishment      = "KICK"

-- Anti-Change Speed Settings
GuardianV.AntiChangeSpeed          = true
GuardianV.SpeedPunishment          = "KICK"

-- Anti-Free Cam Settings
GuardianV.AntiFreeCam              = false
GuardianV.CamPunishment            = "KICK"

-- Anti-Rainbow Vehicle Settings
GuardianV.AntiRainbowVehicle       = true
GuardianV.RainbowPunishment        = "KICK"

-- Anti-Plate Changer Settings
GuardianV.AntiPlateChanger         = true
GuardianV.AntiBlackListPlate       = true
GuardianV.PlatePunishment          = "KICK"

-- Anti-Vision Settings
GuardianV.AntiNightVision          = true
GuardianV.AntiThermalVision        = true
GuardianV.VisionPunishment         = "KICK"

-- Anti-Super Jump Settings
GuardianV.AntiSuperJump            = true
GuardianV.JumpPunishment           = "KICK"

-- Anti-Teleport Settings
GuardianV.AntiTeleport             = true
GuardianV.MaxFootDistance          = 200
GuardianV.MaxVehicleDistance       = 600
GuardianV.TeleportPunishment       = "KICK"

-- Anti-Noclip Settings
GuardianV.AntiNoclip               = true
GuardianV.NoclipPunishment         = "KICK"

-- Anti-Ped Changer Settings
GuardianV.AntiPedChanger           = true
GuardianV.PedChangePunishment      = "KICK"

-- Anti-Infinite Stamina Settings
GuardianV.AntiInfiniteStamina      = false
GuardianV.InfinitePunishment       = "KICK"

-- Anti-Ragdoll Settings
GuardianV.AntiRagdoll              = true
GuardianV.RagdollPunishment        = "KICK"

-- Anti-Menyoo Settings
GuardianV.AntiMenyoo               = true
GuardianV.MenyooPunishment         = "KICK"

-- Anti-Aim Assist Settings
GuardianV.AntiAimAssist            = true
GuardianV.AimAssistPunishment      = "KICK"

-- Anti-Resource Stopper Settings
GuardianV.AntiResourceStopper      = true
GuardianV.AntiResourceStarter      = false
GuardianV.AntiResourceRestarter    = false
GuardianV.ResourcePunishment       = "WARN"

-- Anti-Tiny Ped Settings
GuardianV.AntiTinyPed              = true
GuardianV.PedFlagPunishment        = "KICK"

-- Anti-Suicide Settings
GuardianV.AntiSuicide              = true
GuardianV.SuicidePunishment        = "KICK"

-- Anti-Pickup Collect Settings
GuardianV.AntiPickupCollect        = true
GuardianV.PickupPunishment         = "KICK"

-- Anti-Spam Chat Settings
GuardianV.AntiSpamChat             = true
GuardianV.MaxMessage               = 10
GuardianV.CoolDownSec              = 3
GuardianV.ChatPunishment           = "KICK"

-- Anti-BlackList Commands Settings
GuardianV.AntiBlackListCommands    = true
GuardianV.CMDPunishment            = "KICK"

-- Anti-Change Damage Settings
GuardianV.AntiWeaponDamageChanger  = true
GuardianV.AntiVehicleDamageChanger = true
GuardianV.DamagePunishment         = "KICK"

-- Anti-BlackList Word Settings
GuardianV.AntiBlackListWord        = true
GuardianV.WordPunishment           = "KICK"

-- Anti-Bring All Settings
GuardianV.AntiBringAll             = true
GuardianV.BringAllPunishment       = "KICK"

-- Anti-Trigger Settings
GuardianV.AntiBlackListTrigger     = true
GuardianV.AntiSpamTrigger          = true
GuardianV.TriggerPunishment        = "KICK"

-- Anti-Clear Ped Tasks Settings
GuardianV.AntiClearPedTasks        = true
GuardianV.MaxClearPedTasks         = 5
GuardianV.CPTPunishment            = "KICK"

-- Anti-Taze Players Settings
GuardianV.AntiTazePlayers          = true
GuardianV.MaxTazeSpam              = 3
GuardianV.TazePunishment           = "KICK"

-- Anti-Inject Settings
GuardianV.AntiInject               = true
GuardianV.InjectPunishment         = "KICK"

-- Anti-Explosion Settings
GuardianV.AntiBlackListExplosion   = true
GuardianV.AntiExplosionSpam        = true
GuardianV.MaxExplosion             = 10
GuardianV.ExplosionSpamPunishment  = "KICK"

-- Anti-Entity Spawn Settings
GuardianV.AntiBlackListObject      = true
GuardianV.AntiBlackListPed         = true
GuardianV.AntiBlackListBuilding    = true
GuardianV.AntiBlackListVehicle     = true
GuardianV.EntityPunishment         = "BAN"

-- Anti-NPC Spawn Settings
GuardianV.AntiSpawnNPC             = true

-- Anti-Spam Entity Settings
GuardianV.AntiSpamVehicle          = true
GuardianV.MaxVehicle               = 10

GuardianV.AntiSpamPed              = true
GuardianV.MaxPed                   = 4

GuardianV.AntiSpamObject           = true
GuardianV.MaxObject                = 15

GuardianV.SpamPunishment           = "KICK"

-- Anti-Change Permission Settings
GuardianV.AntiChangePerm           = true
GuardianV.PermPunishment           = "KICK"

-- Anti-Play Sound Settings
GuardianV.AntiPlaySound            = true
GuardianV.SoundPunishment          = "KICK"


```