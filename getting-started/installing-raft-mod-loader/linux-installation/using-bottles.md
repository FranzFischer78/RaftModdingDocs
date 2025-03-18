---
description: >-
  Installing the mod loader on Linux or the Steam Deck using Bottles (basically
  a managed and more user friendly version of Wine)
---

# Using Bottles

Starting note for the Steam Deck users: To access the Linux Desktop on the Steam Deck do the following: [https://help.steampowered.com/en/faqs/view/0872-C5FA-C31E-FE63](https://help.steampowered.com/en/faqs/view/0872-C5FA-C31E-FE63)



Now let's get started :)

1. First let's open bottles. If you don't have bottles installed on your system you can get it here: [https://usebottles.com/](https://usebottles.com/)
2.  Now let's create a new custom Bottle running on Soda:\


    <figure><img src="../../../.gitbook/assets/grafik (35).png" alt=""><figcaption></figcaption></figure>


3.  Once the Bottle is created, open it and click on dependencies:\


    <figure><img src="../../../.gitbook/assets/Screenshot 2023-10-16 174522.png" alt=""><figcaption></figcaption></figure>

    Then install .NET Framework 4.6:\


    <figure><img src="../../../.gitbook/assets/grafik.png" alt=""><figcaption></figcaption></figure>
4.  Next go back to your Bottle and click on "Install Programs..."\


    <figure><img src="../../../.gitbook/assets/grafik (1).png" alt=""><figcaption></figcaption></figure>

    and install Steam:\


    <figure><img src="../../../.gitbook/assets/grafik (2).png" alt=""><figcaption></figcaption></figure>


5.  Download the game on steam as usual and see if it runs. If the game or steam fails to start, try enabling dxvk in the bottle's settings (this can also be useful to improve the performance in general):\


    <figure><img src="../../../.gitbook/assets/grafik (30).png" alt=""><figcaption></figcaption></figure>

    If that still doesn't fix it (mostly on steam decks), try disabling steam runtime in the compatibility settings: \


    <figure><img src="../../../.gitbook/assets/grafik (31).png" alt=""><figcaption></figcaption></figure>


6.  Next we need to do one last thing before we're set. Back in the main menu of the Bottle, scroll down to "Legacy Wine tools" and open "Configuration":\


    <figure><img src="../../../.gitbook/assets/grafik (32).png" alt=""><figcaption></figcaption></figure>

    Then head over to the "Libraries" tab and enter the following in the field under "New override for Library": "\*winhttp"\
    \
    ![](<../../../.gitbook/assets/grafik (33).png>)\
    \
    Click on "Add" -> "Apply" -> "Ok".
7.  Aaaand you're set! Now you just need to run the "RMLLauncher.exe" by clicking on "Run Executable": \


    <figure><img src="../../../.gitbook/assets/grafik (34).png" alt=""><figcaption></figcaption></figure>


8.  **ENJOY!!!**\


    <figure><img src="../../../.gitbook/assets/spaces_bUQfC6JPDbsyAF18yxAF_uploads_git-blob-7aef095370dfe2cdb137ac1bd808bf79177e001a_image (4) (1).png" alt=""><figcaption><p>The Raft Mod Loader main menu</p></figcaption></figure>



P.S. Installing mods probably needs to be done manually by downloading the rmod files on the website and placing them in the "mods" folder next to the game executable.&#x20;

{% hint style="info" %}
If you encounter any issues or the guide doesn't seem to work for you, please visit the            _#linux-support_ channel on our [Discord](https://www.raftmodding.com/discord).\
\
Our team is more than happy to assist you. 🙂
{% endhint %}
