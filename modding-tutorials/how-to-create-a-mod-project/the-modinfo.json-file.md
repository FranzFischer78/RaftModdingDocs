---
description: >-
  This page aims to give you all the needed information about the modinfo.json
  file.
---

# The modinfo.json file

Here is a list of all the fields of the modinfo.json file and a small description/usage of them. More info about them below this table.

| Field Name               | Description                                                                                                                                                                                                                                                                                   |
| ------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                 | <p>Type : <strong>String</strong></p><p>Description : <strong>The display name of your mod.</strong></p>                                                                                                                                                                                      |
| **author**               | <p>Type : <strong>String</strong></p><p>Description : <strong>Your username.</strong></p>                                                                                                                                                                                                     |
| **description**          | <p>Type : <strong>String</strong></p><p>Description : <strong>A small description of your mod.</strong></p>                                                                                                                                                                                   |
| **requiredByAllPlayers** | <p>Type : <strong>Bool</strong></p><p>Description : <strong>Is the mod required by all players to work?</strong></p>                                                                                                                                                                          |
| **version**              | <p>Type : <strong>String</strong></p><p>Description : <strong>The current version of your mod.</strong></p><p>Usage : <strong>We recommend using</strong> <a href="https://semver.org/"><strong>Semantic Versioning 2.0.0</strong></a><strong>​</strong></p>                                  |
| **license**              | <p>Type : <strong>String</strong></p><p>Description : <strong>The license of your mod.</strong></p><p>Usage : <strong>You can find many licenses on</strong> <a href="https://choosealicense.com/"><strong>choosealicense.com</strong></a><strong>​</strong></p>                              |
| **icon**                 | <p>Type : <strong>String / Path</strong></p><p>Description : <strong>An icon for your mod. (Can be seen in the mod manager list)</strong></p><p>Usage : <strong>We recommend you a 512x512 png or jpg image.</strong></p>                                                                     |
| **banner**               | <p>Type : <strong>String / Path</strong></p><p>Description : <strong>A banner for your mod. (Can be seen in the mod manager list)</strong></p><p>Usage : <strong>We recommend you a 660 x 200 png or jpg image.</strong></p>                                                                  |
| **gameVersion**          | <p>Type : <strong>String</strong></p><p>Description : <strong>The version of Green Hell that you made was made for.</strong></p><p>Usage : <strong>This is just for info, Mods should remain compatible across versions</strong>.</p>                                                         |
| **updateUrl**            | <p>Type : <strong>String / Url</strong></p><p>Description : <strong>A link that returns the latest available version of your mod.</strong></p><p>Usage : <strong>Our site provides you an url when you release your mod.</strong></p>                                                         |
| **isModPermanent**       | <p>Type : <strong>Boolean (true or false)</strong></p><p>Description : <strong>Defines if your mod is permanent. Permanent mods are loaded by default and can't be unloaded. This is needed when mods add new items/blocks that can't really be unloaded without causing issues.</strong></p> |
| **excludedFiles**        | <p>Type : <strong>Array of strings / List of strings</strong></p><p>Description : <strong>Allows you to specify files to not load. This doesn't support wildcards yet.</strong></p><p>Usage : <strong>Useful when you want to exclude files like readme or source files.</strong></p>         |

&#x20;**Icon & Banner Fields :** \
**Just add an image to your solution folder where your** **`.cs`** **files and the** **`.csproj`** **file is and edit the** **`modinfo.json`** **file as shown below.**

![](https://gblobscdn.gitbook.com/assets%2F-M5KKfkIqMO\_EFPortVm%2F-M5eDSsjwiUWaLaLvoJ2%2F-M5eLQxSe2MfTv4wdoCA%2Fimage.png?alt=media\&token=1dde7eaa-2c04-457f-8dba-f6bb9104b52d)

**UpdateUrl Field :** \
**RaftModLoader fetch this link to know what is the latest available version of your mod, if the currently installed version is not equal to the version returned by this url it will say that the mod is outdated.**\
**Our website offer this service with a nice automation system. Available on the following link once you have a mod slug.**\
&#x20;`https://www.raftmodding.com/api/v1/mods/`**`YOURMODSLUG`**`/version.txt`

**requiredByAllPlayers Field :**\
**If this field is set to true and the mod is loaded it will kick any player attempting to join that does not have the same mod and the same version. If your mod adds new items or new blocks, this definitely needs to be true! So nobody will be able to join with missing blocks!**

**ExcludedFiles Field :** \
**This is a simple list of excluded files as shown below.**

![](https://gblobscdn.gitbook.com/assets%2F-M5KKfkIqMO\_EFPortVm%2F-M5eDSsjwiUWaLaLvoJ2%2F-M5eMfiNdAlpQcRRqPZ9%2Fimage.png?alt=media\&token=a8ed217b-34d5-4e8d-aa92-b0ca01f6f0f2)
