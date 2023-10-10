---
description: >-
  The Mod class serves as the base class for all mods, containing essential
  information about your mod, customizable events, and more. All mods inherit
  from this class.
---

# Mod

## Allows mods to determine if they can be unloaded at the said moment.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.CanUnload(System.String@)
public virtual bool CanUnload(ref string message)
```
{% endtab %}{% tab title="Example" %}
```cs
bool stillLoading = true;
public override bool CanUnload(ref string message)
{
    if (stillLoading)
    {
        message = "The mod is still loading";
        return false;
    }
    return base.CanUnload(ref message);
}
```
{% endtab %}
{% endtabs %}
***

## Unloads the mod.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.UnloadMod()
public virtual void UnloadMod()
```
{% endtab %}
***

## Gets the bytes of an embedded file in the mod.

`Returns the bytes of the embedded file, or null if the file doesn't exist.`
{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.GetEmbeddedFileBytes(System.String)
public virtual byte[] GetEmbeddedFileBytes(string path)
```
{% endtab %}{% tab title="Example" %}
```cs
byte[] myBundleBytes = GetEmbeddedFileBytes("mybundle.assets");
AssetBundle bundle = AssetBundle.LoadFromMemory(myBundleBytes);
```
{% endtab %}
{% endtabs %}
***

## Gets the mod information.

`Returns the mod information from the modinfo.json file.`
{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.GetModInfo()
public JsonModInfo GetModInfo()
```
{% endtab %}{% tab title="Example" %}
```cs
Debug.Log("Mod version: "+GetModInfo().version);
```
{% endtab %}
{% endtabs %}
***

## Logs a message with the mod name as a prefix.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.Log(System.Object)
public void Log(object message)
```
{% endtab %}{% tab title="Example" %}
```cs
Log("This is a message"); // Outputs: "[ModName] This is a message".
```
{% endtab %}
{% endtabs %}
***

## The WorldEvent_WorldLoaded event triggers on world load complete.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.WorldEvent_WorldLoaded()
public virtual void WorldEvent_WorldLoaded()
```
{% endtab %}{% tab title="Example" %}
```cs
public override void WorldEvent_WorldLoaded()
{
    Debug.Log("The world has loaded");
}
```
{% endtab %}
{% endtabs %}
***

## The WorldEvent_WorldSaved event triggers on world save.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.WorldEvent_WorldSaved()
public virtual void WorldEvent_WorldSaved()
```
{% endtab %}{% tab title="Example" %}
```cs
public override void WorldEvent_WorldSaved()
{
    Debug.Log("The world has been saved");
}
```
{% endtab %}
{% endtabs %}
***

## The LocalPlayerEvent_Hurt event triggers when the local player takes damage.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.LocalPlayerEvent_Hurt(System.Single,UnityEngine.Vector3,UnityEngine.Vector3,EntityType)
public virtual void LocalPlayerEvent_Hurt(float damage, Vector3 hitPoint, Vector3 hitNormal, EntityType damageInflictorEntityType)
```
{% endtab %}{% tab title="Example" %}
```cs
public override void LocalPlayerEvent_Hurt(float damage, Vector3 hitPoint, Vector3 hitNormal, EntityType damageInflictorEntityType)
{
    Debug.Log("Player hurt: " + damage + " damage taken");
}
```
{% endtab %}
{% endtabs %}
***

## The LocalPlayerEvent_Death event triggers when the local player dies.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.LocalPlayerEvent_Death(UnityEngine.Vector3)
public virtual void LocalPlayerEvent_Death(Vector3 deathPosition)
```
{% endtab %}{% tab title="Example" %}
```cs
public override void LocalPlayerEvent_Death(Vector3 deathPosition)
{
    Debug.Log("Player died at: " + deathPosition);
}
```
{% endtab %}
{% endtabs %}
***

## The LocalPlayerEvent_Respawn event triggers when the local player respawns.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.LocalPlayerEvent_Respawn()
public virtual void LocalPlayerEvent_Respawn()
```
{% endtab %}{% tab title="Example" %}
```cs
public override void LocalPlayerEvent_Respawn()
{
    Debug.Log("Player respawned");
}
```
{% endtab %}
{% endtabs %}
***

## The LocalPlayerEvent_ItemCrafted event triggers when the local player crafts an item.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.LocalPlayerEvent_ItemCrafted(Item_Base)
public virtual void LocalPlayerEvent_ItemCrafted(Item_Base item)
```
{% endtab %}{% tab title="Example" %}
```cs
public override void LocalPlayerEvent_ItemCrafted(Item_Base item)
{
    Debug.Log("Item crafted: " + item.UniqueName);
}
```
{% endtab %}
{% endtabs %}
***

## The LocalPlayerEvent_PickupItem event triggers when the local player picks up a dropped item.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.LocalPlayerEvent_PickupItem(PickupItem)
public virtual void LocalPlayerEvent_PickupItem(PickupItem item)
```
{% endtab %}{% tab title="Example" %}
```cs
public override void LocalPlayerEvent_PickupItem(PickupItem item)
{
    Debug.Log("Picked up item: " + item.itemInstance?.UniqueName);
}
```
{% endtab %}
{% endtabs %}
***

## The LocalPlayerEvent_DropItem event triggers when the local player drops an item.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.LocalPlayerEvent_DropItem(ItemInstance,UnityEngine.Vector3,UnityEngine.Vector3,System.Boolean)
public virtual void LocalPlayerEvent_DropItem(ItemInstance item, Vector3 position, Vector3 direction, bool parentedToRaft)
```
{% endtab %}{% tab title="Example" %}
```cs
public override void LocalPlayerEvent_DropItem(ItemInstance item, Vector3 position, Vector3 direction, bool parentedToRaft)
{
    Debug.Log("Dropped item: " + item.UniqueName + " at position: " + position);
}
```
{% endtab %}
{% endtabs %}
***

## The WorldEvent_OnPlayerConnected event triggers when a player connects to the world.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.WorldEvent_OnPlayerConnected(Steamworks.CSteamID,RGD_Settings_Character)
public virtual void WorldEvent_OnPlayerConnected(CSteamID steamid, RGD_Settings_Character characterSettings)
```
{% endtab %}{% tab title="Example" %}
```cs
public override void WorldEvent_OnPlayerConnected(CSteamID steamid, RGD_Settings_Character characterSettings)
{
    Debug.Log("Player connected: " + steamid);
}
```
{% endtab %}
{% endtabs %}
***

## The WorldEvent_OnPlayerDisconnected event triggers when a player disconnects from the world.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.WorldEvent_OnPlayerDisconnected(Steamworks.CSteamID,DisconnectReason)
public virtual void WorldEvent_OnPlayerDisconnected(CSteamID steamid, DisconnectReason disconnectReason)
```
{% endtab %}{% tab title="Example" %}
```cs
public override void WorldEvent_OnPlayerDisconnected(CSteamID steamid, DisconnectReason disconnectReason)
{
    Debug.Log("Player disconnected: " + steamid + " Reason: " + disconnectReason);
}
```
{% endtab %}
{% endtabs %}
***

## The WorldEvent_WorldUnloaded event triggers on world unload.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.WorldEvent_WorldUnloaded()
public virtual void WorldEvent_WorldUnloaded()
```
{% endtab %}{% tab title="Example" %}
```cs
public override void WorldEvent_WorldUnloaded()
{
    Debug.Log("World unloaded");
}
```
{% endtab %}
{% endtabs %}
***

## The ModEvent_OnModLoaded event triggers when a mod is loaded.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.ModEvent_OnModLoaded(HMLLibrary.Mod)
public virtual void ModEvent_OnModLoaded(Mod mod)
```
{% endtab %}{% tab title="Example" %}
```cs
public override void ModEvent_OnModLoaded(Mod mod)
{
    Debug.Log("Mod loaded: " + mod.name);
}
```
{% endtab %}
{% endtabs %}
***

## The ModEvent_OnModUnloaded event triggers when a mod is unloaded.

{% tabs %}
{% tab title="Method" %}
```csharp
// Mod.ModEvent_OnModUnloaded(HMLLibrary.Mod)
public virtual void ModEvent_OnModUnloaded(Mod mod)
```
{% endtab %}{% tab title="Example" %}
```cs
public override void ModEvent_OnModUnloaded(Mod mod)
{
    Debug.Log("Mod unloaded: " + mod.name);
}
```
{% endtab %}
{% endtabs %}