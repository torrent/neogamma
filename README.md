## 📘 Specification Overview: `#5chdat` Directive

This document outlines the basic functionality and usage of the `#5chdat` directive, designed to simplify the embedding and referencing of 5ch (formerly 2ch) thread data within PukiWiki pages or similar environments.

---

### 🔍 What is `#5chdat`?

The `#5chdat` directive allows users to embed or link to archived 5ch thread data using a simplified syntax. It is particularly useful for referencing threads stored in `.dat` format or mirrored content, enabling easier navigation and integration into wiki-based documentation or archival projects.
## 🌐 Related Wiki Page

You can view a working example of the `#5chdat` directive and the enhanced `#amazon()` plugin on the public wiki:

- 🔗 [REQUIEM AND SILENCE – neogamma.loader.jp](https://neogamma.loader.jp/?REQUIEM+AND+SILENCE.html)
- ## 📌 Related Documents

- 🔧 [Planned Feature](./Planned%20Feature) – Upcoming improvements and design goals  
- 🔐 [Security-Oriented Design](./Security-Oriented%20Design) – Safe plugin practices and password handling  
- 🧭 [wikiinfomateion](./wikiinfomateion) – Plugin behavior and known issues  
- 📖 [introduce.md](./introduce.md) – Project introduction and background  
- 📄 [ACKNOWLEDGEMENTS.md](./ACKNOWLEDGEMENTS.md) – Credits and inspirations  
- 🧪 [他のdat取得](./%E4%BB%96%E3%81%AEdat%E5%8F%96%E5%BE%97) – Notes on `.dat` parsing and legacy compatibility
- 
## 🔐 Planned Feature: Manual Password Verification

To ensure secure handling of `.dat` file attachments and avoid unintended behavior, we are shifting away from automated processes.

Instead, we plan to implement a manual verification step:

- When a user initiates a `.dat` file operation (e.g., upload or parse), the plugin will pause and display a password input form  
- The user must enter the correct password manually  
- The plugin will verify the password using the same hashing method as PukiWiki (`md5(md5($pass) . $salt)`)  
- If the password is valid, the operation proceeds; otherwise, it is aborted

This approach avoids storing or exposing password hashes and ensures that all sensitive operations require explicit user intent.

We believe this strikes a good balance between usability and security, especially since `.dat` operations are infrequent and typically performed by trusted users.



---

### 🧾 Syntax

```pukiwiki
#5chdat(URL)




<meta name="google-site-verification" content="3D2d_X8a5FfW9HUcLd21U-FQt1p4Dp7bpGebYuCUQs8" />

[5chdat](https://neogamma.loader.jp/?5chdat.html)

*NeoGamma 起動方法 [#ue3f6a6e]
***Wiikeyと現在の改造事情 [#wiikey]

**Wiikeyとは：** [#ccadec3b]
- 任天堂Wii用の改造チップ（ModChip）
- 本体に直接はんだ付けして取り付け
- 海外ソフトやバックアップ起動、自作ソフトの実行が可能

**問題点：** [#kf82262a]
- コピーガード回避目的で、法的にグレー〜違法
- 任天堂から訴訟を受けた例もあり

**現在（Switch 2時代）：** [#m1250c03]
- MIGフラッシュカートなどが登場
- 使用すると**本体がBANされるリスク**
- 任天堂は**不正ハードウェアの使用を厳しく取り締まり中**

***softchip氏のコメント [#softchip]
- 「Wiikeyって名前、**チップの名前そのままハンドルにしてたの面白いよね**」
- 「昔は“いけないこと”だったけど、**今やると本体ごとBANされる時代**」
- 「時代が変わっても、**改造の誘惑とリスクは変わらない**なぁ…」

#2chdat
#dat2ch
#dot2ch
#dat2chdat
入力URL: https://medaka.5ch.net/test/read.cgi/gameurawaza/1366108733/158
preg_match 結果:
$m[0] = https://medaka.5ch.net/test/read.cgi/gameurawaza/1366108733/158
$m[1] = medaka.5ch.net
$m[2] = gameurawaza
$m[3] = 1366108733
$m[4] = 158
DAT URL: https://medaka.5ch.net/gameurawaza/dat/1366108733.dat
✅ DAT取得成功
Server = medaka.5ch.net
Board = gameurawaza
Thread = 1366108733
DATサイズ = 122942 bytes
文字コード = SJIS-win
[neogamma起動法](*NeoGamma 起動方法 [#ue3f6a6e]
***Wiikeyと現在の改造事情 [#wiikey]

**Wiikeyとは：** [#ccadec3b]
- 任天堂Wii用の改造チップ（ModChip）
- 本体に直接はんだ付けして取り付け
- 海外ソフトやバックアップ起動、自作ソフトの実行が可能

**問題点：** [#kf82262a]
- コピーガード回避目的で、法的にグレー〜違法
- 任天堂から訴訟を受けた例もあり

**現在（Switch 2時代）：** [#m1250c03]
- MIGフラッシュカートなどが登場
- 使用すると**本体がBANされるリスク**
- 任天堂は**不正ハードウェアの使用を厳しく取り締まり中**

***softchip氏のコメント [#softchip]
- 「Wiikeyって名前、**チップの名前そのままハンドルにしてたの面白いよね**」
- 「昔は“いけないこと”だったけど、**今やると本体ごとBANされる時代**」
- 「時代が変わっても、**改造の誘惑とリスクは変わらない**なぁ…」

#2chdat
#dat2ch
#dot2ch
#dat2chdat
入力URL: https://medaka.5ch.net/test/read.cgi/gameurawaza/1366108733/158
preg_match 結果:
$m[0] = https://medaka.5ch.net/test/read.cgi/gameurawaza/1366108733/158
$m[1] = medaka.5ch.net
$m[2] = gameurawaza
$m[3] = 1366108733
$m[4] = 158
DAT URL: https://medaka.5ch.net/gameurawaza/dat/1366108733.dat
✅ DAT取得成功
Server = medaka.5ch.net
Board = gameurawaza
Thread = 1366108733
DATサイズ = 122942 bytes
文字コード = SJIS-win
DAT行数: 537
1行目フィールド数: 5)
DAT行数: 537
1行目フィールド数: 5
[neogammak起動法](https://neogamma.loader.jp/?NeoGamma+%E8%B5%B7%E5%8B%95%E6%96%B9%E6%B3%95.html)

DATサイズ = 122942 bytes

文字コード = SJIS-win
DAT行数: 537
1行目フィールド数: 5)
DAT行数: 537
1行目フィールド数: 5
[neogammak起動法]([https://neogamma.loader.jp/?NeoGamma+%E8%B5%B7%E5%8B%95%E6%96%B9%E6%B3%95.html](https://neogamma.loader.jp/?%E3%81%AF%E3%81%BE%E5%AF%BF%E5%8F%B8%E3%81%AE%E7%A6%8F%E8%A2%8B.html)
