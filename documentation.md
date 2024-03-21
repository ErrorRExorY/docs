# GuardianV - Documentation

## 🎊 Configuration Explained
### ⏏️ Whitelisting Objects

You get banned for "Blacklisted object detected" ?
That's because you need to add the object model to the whitelisted ones.
You only need to add networked objects (those that everyone can see when spawned).

> You can add the object model hash or the model string.

> Disabling the object whitelist is not recommanded, take the time to whitelist every networked objects that you spawn in your server.

> Tip: You can search through your server for the native CreateObject or CreateObjectNoOffset to see wich ones are spawned in your server.

## 💻 Developers Stuff
### 👉 Exports
#### Exports (Server Side)

GuardianV_CHANGE_TEMP_WHITELIST: This export enables you to add or remove a player from the Temporary Whitelists. For example:
```
-- Add:
exports['GuardianV']:GuardianV_CHANGE_TEMP_WHITELIST(source, true)

-- Remove:
exports['GuardianV']:GuardianV_CHANGE_TEMP_WHITELIST(source, false)
```
GuardianV_CHECK_TEMP_WHITELIST: This export is exclusively for checking a player's status in the Temporary Whitelist. 
For example:
```
-- Check:
exports['GuardianV']:GuardianV_CHECK_TEMP_WHITELIST(source)
```
GuardianV_ACTION: Use this export for performing actions like BAN,KICK, or WARN on a player:
```
-- Ban:
exports['GuardianV']:GuardianV_ACTION(source, "BAN", reason, details)

-- Kick:
exports['GuardianV']:GuardianV_ACTION(source, "KICK", reason, details)

-- Warn:
exports['GuardianV']:GuardianV_ACTION(source, "WARN", reason, details)
```
#### Exports (Client Side)
GuardianV_CHANGE_TEMP_WHHITELIST: This export is designed for adding or removing a player from the Temporary Whitelist on the client side:
```
-- Add:
exports['GuardianV']:GuardianV_CHANGE_TEMP_WHHITELIST(true)

-- Remove:
exports['GuardianV']:GuardianV_CHANGE_TEMP_WHHITELIST(false)
```
GuardianV_CHECK_TEMP_WHITELIST: Similar to the server side, use this export to check a player's status in the Temporary Whitelist:
```
-- Check:
exports['GuardianV']:GuardianV_CHECK_TEMP_WHITELIST()
```
GuardianV_ACTION: On the client side, employ this export for actions such as BAN, KICK, or WARN:
```
-- Ban:
exports['GuardianV']:GuardianV_ACTION("BAN", reason, details)

-- Kick:
exports['GuardianV']:GuardianV_ACTION("KICK", reason, details)

-- Warn:
exports['GuardianV']:GuardianV_ACTION("WARN", reason, details)
```

### 🗑️ Ban Event Handler

## 🛡️Secure your events
> OUTDATED: Just use this feature from the panel and it will secure all your events automatically without editing your code as before.  



You will have to replace your event handler function & also the trigger function.

Copy
--replace (from the client side):
```
TriggerServerEvent("my_awesome_event",999,"test")
```
--with:
```
exports["GuardianV"]:TriggerServerEvent("my_awesome_event",999,"test")
```
Copy
--replace (from the server side):
```
AddEventHandler("my_awesome_event", function(number, string)
    print(number, string)
end)
```
--with:
```
exports["GuardianV"]:AddEventHandler("my_awesome_event", function(source, number, string)
    print(number, string)
end)
```
You can also secure your client events:

Copy
-- replace (from the client side):
```
AddEventHandler("esx_ambulancejob:revive", function(...)
end)
```
-- with:
```
exports["GuardianV"]:AddEventHandler("esx_ambulancejob:revive", function(...)
end)
```
When you secure an event you also need to remove his register function.(RegisterServerEvent or RegisterNetEvent)

We recommand only to secure those that are exploitable (giving advantage, money, weapon, vehicles etc)

## 🤖Commands

```
GuardianV install (you shouldn't need to run it, it does automatically)
GuardianV uninstall

GuardianV baninfo <banId>
GuardianV ban <serverId> <optional:reason>
GuardianV unban <banId> <optional:reason>
GuardianV unban all

GuardianV reload (reload the server config files without restarting the server)
```

## 🥙Adding staffs

```
# server.cfg
add_ace identifier.license:xxx "GuardianV.Admin" allow
add_ace identifier.license:xxx "GuardianV.Commands" allow
add_ace identifier.steam:xxx "GuardianV.Bypass" allow

add_ace group.mod "GuardianV.Bypass" allow
add_ace group.admin "GuardianV.Bypass" allow
add_ace group.admin "GuardianV.Commands" allow

# It works with any identifier or group you defined using ace perms
```