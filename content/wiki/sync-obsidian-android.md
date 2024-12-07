---
title: "Sync Obsidian to Android"
slug: "sync-obsidian-android"
toc: true
tocBorder: true
---

[返回目录](/wiki/)

---

> 本文内容：将 Windows 的 Obsidian 和安卓手机的 Obsidian 同步
> 
> 本文发布于 2023-01-23，部分内容可能过期了

# Step1: Prepare the followings

- [Obsidian](https://play.google.com/store/apps/details?id=md.obsidian) on Windows and Android
- [FolderSync](https://play.google.com/store/apps/details?id=dk.tacit.android.foldersync.lite) on Android
- Cloud service account
	- *Note:* I will use WebDAV by [Nutstore](https://www.jianguoyun.com/) for exampl*e, you can use any other Cloud service you like.*

# Step2: Authorize Nutstore applications

- Open the [Nutstore](https://www.jianguoyun.com/) - Preferences - Manage third-party apps.
- Click the “Acquire current key”, and then fill a name in the blank. Copy the key.
	- *Note: we will use the information in Figure 1.*

{{<figure src="/wiki/sync-obsidian-android-1.png" caption="Figure 1">}}

# Step3: Set authorization in FolderSync

- Click the “Accounts” in FolderSync and “Add account”
- Then, choose the “WebDav” for the account type
- Fill the blank in Figure 2 using the information in Figure 1

{{<figure src="/wiki/sync-obsidian-android-2.png" caption="Figure 2">}}

# Step4: Sync your Obsidian folder to Nutstore in Windows

- Sync your Obsidian folder to Nutstore in Windows like Figure 3. Then you will see the folder in nutstore.

{{<figure src="/wiki/sync-obsidian-android-3.png" caption="Figure 3">}}

# Step5: Build a folder to sync the Obsidian folder in Windows

- Build a special folder in your smartphone.

# Step6: Sync the folders you set in step5 and step4

- Back to FolderSync - “account”. Choose “Folderpair”.
- Follow the settings in Figure 4. You can refer my example settings in Figure 5.

{{<figure src="/wiki/sync-obsidian-android-4.png" caption="Figure 4" >}}

{{<figure src="/wiki/sync-obsidian-android-5.png" caption="Figure 5">}}

# Step7: Set basic items in FolderSync

- Set basic items in FolderSync as you like.

# Step8: Begin the synchronization！

- Choose the “Sync” after the settings in Step7, click “Sync” in Figure 6, and wait for a while. If the blue box turn to green like Figure 7, your synchronization is successful. You can also click the little icon in Figure 7, where shows synchronization details.

{{<figure src="/wiki/sync-obsidian-android-6.png" caption="Figure 6">}}

{{<figure src="/wiki/sync-obsidian-android-7.png" caption="Figure 7">}}

# Step9: Open the synchronization folder in the Android Obsidian

- Follow the settings in Figure 8 to Figure 9. Then you can see all the files in your smartphone!

{{<figure src="/wiki/sync-obsidian-android-8.png" caption="Figure 8">}}

{{<figure src="/wiki/sync-obsidian-android-9.png" caption="Figure 9">}}

# Reference

- [How to Sync Your Obsidian Vault Across Devices for Free](https://facedragons.com/foss/sync-obsidian-across-devices/)
- [Sync Obsidian note between windows and android on google drive](https://forum.obsidian.md/t/sync-obsidian-note-between-windows-and-android-on-google-drive/32624)
- [Sync Mobile app through Google Drive (Android-Windows10)](https://forum.obsidian.md/t/sync-mobile-app-through-google-drive-android-windows10/20891)
- [Setting up Git syncing for Obsidian on Android](https://lucidhacker.substack.com/p/setting-up-git-syncing-for-obsidian)
- [To Windows + iOS users, how do you sync Obsidian with Obsidian mobile without paying?](https://www.reddit.com/r/ObsidianMD/comments/ojbl9i/to_windows_ios_users_how_do_you_sync_obsidian/)
- [Jianguoyun Website](https://help.jianguoyun.com/?p=2887)
- [obsidian移动端库同步：FolderSync搭配坚果云的第三方WebDAV](https://zhuanlan.zhihu.com/p/431124370)
- [Obsidian&FolderSync 创作格外丝滑](https://blog.csdn.net/qq_53937391/article/details/126803780)
