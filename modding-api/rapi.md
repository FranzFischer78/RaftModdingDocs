---
description: >-
  The RAPI class provides convenient methods for various actions, including
  adding new items and showing the cursor, making modding tasks easier and more
  accessible.
---

# RAPI

## Checks if the game is running on a dedicated server.

`Returns true if the game is running on a dedicated server, false otherwise.`
{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.IsDedicatedServer()
public static bool IsDedicatedServer()
```
{% endtab %}
***

## Checks if the current active scene is the main menu.

`Returns true if the current active scene is the main menu, false otherwise.`
{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.IsCurrentSceneMainMenu()
public static bool IsCurrentSceneMainMenu()
```
{% endtab %}
***

## Checks if the current active scene is the main game scene.

`Returns true if the current active scene is the main game scene, false otherwise.`
{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.IsCurrentSceneGame()
public static bool IsCurrentSceneGame()
```
{% endtab %}
***

## Gets the username associated with a SteamID.

`Returns the player's username.`
{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.GetUsernameFromSteamID(Steamworks.CSteamID)
public static string GetUsernameFromSteamID(CSteamID steamid)
```
{% endtab %}{% tab title="Example" %}
```cs
string username = RAPI.GetUsernameFromSteamID(playerSteamID);
Debug.Log("Player username: " + username);
```
{% endtab %}
{% endtabs %}
***

## Toggle the mouse cursor with high priority (mostly used by the mod loader).

{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.TogglePriorityCursor(System.Boolean)
public static void TogglePriorityCursor(bool status)
```
{% endtab %}{% tab title="Example" %}
```cs
RAPI.ToggleCursor(true); // This will show the cursor.
RAPI.ToggleCursor(false); // This will hide the cursor.
```
{% endtab %}
{% endtabs %}
***

## Toggle the mouse cursor.

{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.ToggleCursor(System.Boolean)
public static void ToggleCursor(bool status)
```
{% endtab %}{% tab title="Example" %}
```cs
RAPI.ToggleCursor(true); // This will show the cursor.
RAPI.ToggleCursor(false); // This will hide the cursor.
```
{% endtab %}
{% endtabs %}
***

## Gets the local player object from the network.

`Returns the local player object.`
{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.GetLocalPlayer()
public static Network_Player GetLocalPlayer()
```
{% endtab %}{% tab title="Example" %}
```cs
Network_Player player = RAPI.GetLocalPlayer();
// The player variable will contain the local player script.
```
{% endtab %}
{% endtabs %}
***

## Broadcasts a chat message to all players.

{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.BroadcastChatMessage(System.String)
public static void BroadcastChatMessage(string message)
```
{% endtab %}{% tab title="Example" %}
```cs
RAPI.BroadcastChatMessage("I'm a message");
// Will send "I'm a message" to every player.
```
{% endtab %}
{% endtabs %}
***

## Gives a specified amount of items to the local player.

{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.GiveItem(Item_Base,System.Int32)
public static void GiveItem(Item_Base item, int amount)
```
{% endtab %}{% tab title="Example" %}
```cs
RAPI.GiveItem(ItemManager.GetItemByName("item_name"), 5);
// Gives 5 items of "item_name" to the local player.
```
{% endtab %}
{% endtabs %}
***

## Allows an item to be placed on a specific block quad type.

{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.AddItemToBlockQuadType(Item_Base,RBlockQuadType)
public static void AddItemToBlockQuadType(Item_Base item, RBlockQuadType quadtype)
```
{% endtab %}{% tab title="Example" %}
```cs
RAPI.AddItemToBlockQuadType(YourNewItem, RBlockQuadType.quad_foundation);
// Allow "YourNewItem" to be placed on foundations.
```
{% endtab %}
{% endtabs %}
***

## Disallows an item from being placed on a specific block quad type.

{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.RemoveItemFromBlockQuadType(System.String,RBlockQuadType)
public static void RemoveItemFromBlockQuadType(string itemUniqueName, RBlockQuadType quadtype)
```
{% endtab %}{% tab title="Example" %}
```cs
RAPI.RemoveItemFromBlockQuadType("YourItemUniqueName", RBlockQuadType.quad_foundation);
// Disallow the item with the uniquename "YourItemUniqueName" to be placed on foundations.
```
{% endtab %}
{% endtabs %}
***

## Registers a new item.

{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.RegisterItem(Item_Base,System.Boolean)
public static void RegisterItem(Item_Base item, bool ignoreMaxValues = false)
```
{% endtab %}{% tab title="Example" %}
```cs
RAPI.RegisterItem(yourItem); // Replace with actual item initialization
```
{% endtab %}
{% endtabs %}
***

## Unregisters an item, removing it from inventories and world.

{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.UnregisterItem(Item_Base)
public static void UnregisterItem(Item_Base item)
```
{% endtab %}{% tab title="Example" %}
```cs
RAPI.UnregisterItem(ItemManager.GetItemByName("item_name"));
```
{% endtab %}
{% endtabs %}
***

## Sets the in-hand prefab object for a specific item.

{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.SetItemObject(Item_Base,UnityEngine.GameObject,RItemHand)
public static void SetItemObject(Item_Base item, GameObject prefab, RItemHand parent = RItemHand.rightHand)
```
{% endtab %}{% tab title="Example" %}
```cs
Item_Base newItem = new Item_Base(); // Replace with actual item initialization
GameObject itemPrefab = new GameObject(); // Replace with actual prefab initialization
RAPI.RegisterItem(newItem);
RAPI.SetItemObject(newItem, itemPrefab);
```
{% endtab %}
{% endtabs %}
***

## Sends a network message to all players.

{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.SendNetworkMessage(Message,System.Int32,Steamworks.EP2PSend,Target,Steamworks.CSteamID)
public static void SendNetworkMessage(Message message, int channel = 0, EP2PSend ep2psend = EP2PSend.k_EP2PSendReliable, Target target = Target.Other, CSteamID fallbackSteamID = new CSteamID())
```
{% endtab %}{% tab title="Example" %}
```cs
public enum CustomMessages
{
    MyCustomMessage = 8000
}
// This will send your network message to all players.
RAPI.SendNetworkMessage(new YourMessageClass((Messages)CustomMessages.MyCustomMessage)); // Replace with your own message class.
```
{% endtab %}
{% endtabs %}
***

## Listens for network messages on a specific network channel.

`Returns the received network message.`
{% tabs %}
{% tab title="Method" %}
```csharp
// RAPI.ListenForNetworkMessagesOnChannel(System.Int32)
public static NetworkMessage ListenForNetworkMessagesOnChannel(int channel = 2)
```
{% endtab %}{% tab title="Example" %}
```cs
public enum CustomMessages
{
    MyCustomMessage = 8000
}
NetworkMessage netMessage = RAPI.ListenForNetworkMessagesOnChannel(15);
if (netMessage != null)
{
    CSteamID id = netMessage.steamid;
    Message message = netMessage.message;
    // Here we use 8000 because we can't modify an enum, you can use any values 
    // as long as its not in the Messages enum already. Bigger than 1000 is perfect.
    if(message.Type == (Messages)CustomMessages.MyCustomMessage){
        // Do your stuff with the message now that you know 
        // its yours and its the wanted type.
        YourMessageClass msg = message as YourMessageClass;
    }
}
```
{% endtab %}
{% endtabs %}