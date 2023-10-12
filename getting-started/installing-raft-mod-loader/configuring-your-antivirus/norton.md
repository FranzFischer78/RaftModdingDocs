---
description: Explaining how to exclude the Raft Mod Loader from the Norton antivirus
---

# Norton

First let's add the exception to the Norton Antivirus:

Open Norton then go to "Settings"-> "Scans and Risks" and scroll down to "Exclusions/Low risks":

<figure><img src="../../../.gitbook/assets/grafik (3).png" alt=""><figcaption></figcaption></figure>

At "Items to Exclude from Scans", click on "Configure"->"Add Files":

<figure><img src="../../../.gitbook/assets/add exclusion norton.png" alt=""><figcaption></figcaption></figure>

Add an exception for the **RMLLauncher.exe** you downloaded:

<figure><img src="../../../.gitbook/assets/grafik (1) (1).png" alt=""><figcaption></figcaption></figure>

As well as for the **HMLCore.exe** located in **C:\Users\YourUserName\AppData\Roaming\RaftModLoader .**

Then click on "Add Folders" to add an exception for the entire **RaftModLoader** folder located at **C:\Users\YourUserName\AppData\Roaming\RaftModLoader .**

This is what your exceptions should look like. Confirm by hitting "Apply" then "Ok":

<figure><img src="../../../.gitbook/assets/grafik (2) (1).png" alt=""><figcaption></figcaption></figure>

Now add the exact same exceptions for "Items to Exclude from Auto-Protect, Script Control, Behavioral Protection and Download Intelligence Detection":

<figure><img src="../../../.gitbook/assets/grafik (3) (1).png" alt=""><figcaption></figcaption></figure>

After you're done hit "Apply" and then "Ok":&#x20;

<figure><img src="../../../.gitbook/assets/grafik (4).png" alt=""><figcaption></figcaption></figure>

If the Raft Mod Loader can't connect to the internet, you'll need to add an exception to your firewall too:

1. Go to **Settings** -> **Firewall** -> **Application Control**
2. Use the search function to find **`HML`**
3. Allow network access for **`HML`**

Finally restart the computer to apply the settings!

## Aaaand you're done !

**Simply restart our launcher and it should be working !** :thumbsup:
