# IpDefender🔒

IpDefenderは、Java 8からJava 17で動作するSpigot/Paperサーバーにおいて、設定されたプレイヤーへの外部IPからの接続を防ぐプラグインです。

* [ダウンロード](https://github.com/tanu-ch1111/IpDefender/releases)
* [セットアップ](https://github.com/tanu-ch1111/IpDefender?tab=readme-ov-file#%E3%82%B5%E3%83%BC%E3%83%90%E3%83%BC%E3%81%ABipdefender%E3%82%92%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95)

## なぜこのプラグインを使うべきなのか？

### BungeeCordを利用している場合

**BungeeCordを何の対策もなしに利用することは非常に推奨されません！**

一般的に、不正アクセスを防ぐための最も一般的な方法はBungeeGuardです。
BungeeGuardとは異なり、このプラグインはBungeeCordから認証情報を取得しません。
代わりに、Spigot/Paper上でプレイヤーのIPアドレスを保存し、保存されたIPアドレスのみがゲームに参加できる仕組みです。
そのため、許可されたプレイヤーであっても、同じネットワークから接続しない限りサーバーに参加することはできません。
これが、このプラグインが非常に強力である理由です！
しかし、もしIPアドレスを偽装する方法が存在する場合、このプラグインは無意味になります。
したがって、BungeeGuardとIpDefenderの両方を導入することをお勧めします。
BungeeCordのデフォルト設定は明らかに安全ではありません。

### BungeeCordを利用していない場合

もし誰かがあなたのMicrosoftアカウントを乗っ取った場合、あなたのサーバーも乗っ取られる可能性が非常に高くなります。
そして、`online-mode=false`の場合、乗っ取られる可能性は極めて高くなります。
IpDefenderを追加することで、同じネットワークからサーバーに接続しない限り、あなたのサーバーが乗っ取られたり、不正にアクセスされたりすることはないと確信できます。

## セットアップ方法

### サーバーにIpDefenderをインストールする方法

IpDefenderをプラグインフォルダに入れてください。
Config.ymlファイルが生成されたら、保護したいプレイヤーのUUIDを入力してください。
UUIDはNameMcなどのサイトから取得できます。
UUIDを入力後、サーバーを再起動すると、保護したいプレイヤーがサーバーに参加した際にIpLog.txtファイルが生成されます。
IpLog.txtファイルに``00000000-0000-0000-0000-000000000000:00.00.00.000``のようなものが記録されていれば成功です！
再起動直後に別のプレイヤーがサーバーに参加した場合、そのプレイヤーのIPアドレスが保存されることに注意してください。

### サーバーに導入後の動作

不正なログインが検出されると、以下のテキストが表示され、接続が拒否されます。
```Internal Exception: java.io.IOException: Connection reset by peer```

---

IpDefender is a plugin that prevents external Ip from joining a configured player running on a Spigot/Paper server from Java 8 to Java 17

* [Download](https://github.com/tanu-ch1111/IpDefender/releases)
* [Setup](https://github.com/tanu-ch1111/IpDefender?tab=readme-ov-file#how-to-install-ipdefender-on-your-server)

## Why should I use this plugin?

### If you are using BungeeCord

**It is highly discouraged to use BungeeCord without any countermeasures!**

Generally, BungeeGuard is the most common way to prevent unauthorized access.
Unlike BungeeGuard, this plugin does not obtain authentication from BungeeCord.
Instead, on Spigot/Paper, it saves the player’s IP address, and only that saved IP address is allowed to join the game.
Therefore, even an authorized player cannot join the server unless they connect from the same network.
This is why it is so powerful!
However, if there is a way to forge IP addresses, this plugin becomes useless.
That’s why I recommend installing both BungeeGuard and IpDefender.
BungeeCord's default settings are clearly unsafe.

### When bungee cords are not used

If someone hijacks your Microsoft account, there is a great possibility that they can hijack your servers.
And if online-mode=false, the possibility of being hijacked is extremely high.
By adding IpDefender, you can be sure that your server will not be hijacked/accessed unless you join the server from the same network.

## Setup Method

### How to install IpDefender on your server

Put IpDefender in the plugin folder
When the Config.yml file is generated, enter the UUID of the player you want to protect
The UUID can be obtained from sites such as NameMc.
After entering the UUID, restart the server and the IpLog.txt file will be generated when the player you want to protect joins the server.
If the IpLog.txt file contains ``00000000-000000-0000-0000-0000-00000000000000000000:00.00.00.000`` or something similar, you have succeeded!
Please note that if a different player joins the server immediately after the restart, the Ip of that player will be saved.

### How it will work once it is put in the server

If an unauthorized login is detected, the following text will be displayed and the connection will be denied
```Internal Exception: java.io.IOException: Connection reset by peer```
