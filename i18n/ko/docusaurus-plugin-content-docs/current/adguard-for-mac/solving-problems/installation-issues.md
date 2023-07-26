---
title: Installation problems solving
sidebar_position: 5
---

:::info

이 문서는 시스템 수준에서 기기를 보호하는 다기능 광고 차단기인 Mac용 AdGuard에 대해 다룹니다. 어떻게 동작하는지 알고 싶으시다면 [AdGuard 앱을 다운로드](https://adguard.com/download.html?auto=true) 해 보세요.

:::

## "Installation failed" error in macOS Catalina

During the installation you can face an error like this:

![Installation error screen](https://cdn.adtidy.org/content/kb/ad_blocker/mac/macerrorscreenEN.jpg)

Follow this instruction to solve the problem:

1. Restart your Mac
2. As your Mac restarts, press and hold down the *Command(⌘) + R* keys immediately upon hearing the startup chime. Hold the keys until the Apple logo appears to get the computer into Recovery mode.
3. From the top bar select *Utilities* → *Terminal*, and execute this command: `csrutil disable`
4. Restart the Mac and log into Administrator's profile
5. Open the Finder window and select from the top bar *Go* → *Go to Folder* and type `~/private/`
6. Create a folder named *tmp* and type in your password
7. Launch AdGuard installation

As the installation is completed, restart your Mac in Recovery mode using the instruction above and execute `csrutil enable` command in Terminal to enable system protection.
