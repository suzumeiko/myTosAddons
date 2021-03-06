#Quick Menu
## command 
1. `/qm open` : UIを開く
1. `/qm [number] [titleText] [msgText]`：指定ナンバーのテキストとメッセージを変更する 
1. `/qm title  [number]　[titleText]`：指定ナンバーのタイトルを変更する 
1. `/qm msg  [number]　[msgText]`： 指定ナンバーのメッセージを変更する
1. `/qm interval [number]` ：入力後の非受付時間の設定。デフォルトは５。遅延が気になる場合は下げてください  
インターバル以外の数字はボタンの配置です。ボタンの配置は以下のとおりです。

```
1 7
2 8
3 9
4 10
5 11
6 12
```

## 使い方
このアドオンではデフォルトではF10に設定されているヘルプを開く機能を殺し、このアドオンを表示する関数に変えています  
F10以外のボタンに設定したい場合は、システムの設定からヘルプ表示の部分を好みのボタンに設定して下さい  
パッドの場合はHotkeyAbilityForJoyなどの関数で/qm openを設定するか、ToSインストールフォルダのReleaseにある`hotkey_joystick.xml`を編集し、好みのボタンの`DownScp`の中身をを`UI_TOGGLE_HELPLIST`に書き換えてください  
おすすめは35行目のWeponSwapです。  

`<HotKey ID="WeaponSwap1" Name="무기 스왑" DownScp="WEAPONSWAP_HOTKEY_ENTERED()" UpScp="None" Key="JOY_BTN_11" PressedKey="None" Mode="Key" UseAlt="NO" UseCtrl="NO" OnEdit="NO" Category="Basic"/>`  
これを  
`	<HotKey ID="WeaponSwap1" Name="무기 스왑" DownScp="UI_TOGGLE_HELPLIST()" UpScp="None" Key="JOY_BTN_11" PressedKey="None" Mode="Key" UseAlt="NO" UseCtrl="NO" OnEdit="NO" Category="Basic"/>`  
こうする
### v1.1 新機能
* 設定をキャラクター固有と全体の2種類に分けました。キャラクター固有の設定が優先的に表示されます。
* v1.1では2つの機能を追加しました
1. 設定用UI
    * 対象のアイテムを右クリックすることで設定用UIを表示させることができます 
    ![](https://raw.githubusercontent.com/writ312/myTosAddons/master/quickmenu/img2.jpg) 
    ![](https://raw.githubusercontent.com/writ312/myTosAddons/master/quickmenu/img1.jpg)
    1. チャットメッセージの登録を行えます。タイトルとメッセージを登録したあと③のセーブを押して下さい
    2. スキルまたはアイテムの登録を行えます。ドラッグ・アンド・ドロップで設定できます。
    3. ①,②で設定されたものを保存します
    4. 保存はアイテム・スキル＞チャットメッセージの順に優先されます
    5. 現在の設定を削除します。キャラクター固有の設定＞全体の設定の順番に削除されます

1. スキルとアイテムを設定可能に

* 要望があったので追加しました。
* アイテムは全体の設定及びキャラクター個別の設定が可能です
* スキルはキャラクター固有の設定のみです
