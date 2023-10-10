---
description: >-
  This page will guide you on resolving false positive errors on RMLLauncher,
  ensuring a smoother experience without unnecessary interruptions.
---

# Configuring your antivirus

## **Why is my antivirus suspecting RMLLauncher to be a Trojan/Malware?**

{% hint style="success" %}
**RMLLauncher is completely safe to use.** \
_It's important to note that both RMLLauncher and Core are open-sourced, allowing users to analyze the code._
{% endhint %}

Our launcher behavior might seem unusual to antivirus programs because it involves downloading files, loading code into the game and connects to servers.\
We also do not possess a yearly Microsoft code signing license, which can trigger alerts.

Since our software is open-sourced, If it were a virus, someone would have noticed by now. \
Rest assured, our community has thoroughly examined the software. So, you can trust RMLLauncher without any concerns. 😊

## 1. Adding exclusions in your antivirus

To prevent false positives for the launcher, add these two exclusions to your antivirus settings:

1. **RMLLauncher.exe**
2. **C:\Users\YourUserName\AppData\Roaming\RaftModLoader**

{% tabs %}
{% tab title="Windows Defender" %}
To add the exceptions in Windows Defender you can follow the tutorial [here](https://support.microsoft.com/en-us/help/4028485/windows-10-add-an-exclusion-to-windows-security).\

{% endtab %}

{% tab title="Avast" %}
To add the exceptions in Avast you can follow the tutorial [here](https://support.avast.com/en-ww/article/168/).
{% endtab %}

{% tab title="BitDefender" %}
To add the exceptions in Bitdefender you can follow the tutorial [here](https://www.bitdefender.com/consumer/support/answer/13427/).
{% endtab %}

{% tab title="Norton" %}
1. To add the exceptions in Norton you can follow the tutorial [here](https://support.norton.com/sp/en/us/home/current/solutions/v3672136).
2. If Raft Mod Loader can't connect to the internet, you'll need to add an exception to your firewall too:
   1. Open **My Norton**
   2. Go to **Settings** -> **Firewall** -> **Application Control**
   3. Use the search function to find **`HML`**
   4. Allow network access for **`HML`**
{% endtab %}

{% tab title="Other" %}
Type on google "**How to add an exclusion in** " and the name of your antivirus after, then go on the website of your antivirus and follow the step for the two files above


{% endtab %}
{% endtabs %}

## 2. You should be done !

**Simply restart our launcher and it should be working !**

{% hint style="info" %}
If you encounter any further errors or experience the same issue, please visit the #support channel on our [Discord](https://www.raftmodding.com/discord).\
\
Our team is more than happy to assist you. 🙂
{% endhint %}
