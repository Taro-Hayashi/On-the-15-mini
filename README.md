# On the 15 mini
- [キット内容](#キット内容)
- [組み立て](#組み立て)
- [カスタマイズ](#カスタマイズ)
- [その他](#その他)

## キット内容
![パーツ一覧](img/IMG_4844.jpg)  
||部品名|数| |
|-|-|-|-|
|1|メインボード|1||
|2|トッププレート|1||
|3|スイッチプレート|1||
|4|ミドルプレート|2||
|5|ボトムプレート|1||
|6|スペーサー（細）（短）|2|3mm|
|7|スペーサー（太）（長）|6|4mm|
|8|ナベねじ（短）|2|2.5mm|
|9|超低頭ねじ（中）|8|3.5mm|
|10|バインドネジ（長）|6|4mm|
|11|リセットスイッチ|1||
|12|ダイオード|60||
|13|Atmega32u2|1||
|14|Type-C レセプタクル|1||
|15|水晶振動子|1|16MHz|
|16|5.1kΩ|2|R1、R2|
|17|22Ω|2|R3、R4|
|18|10kΩ|2|R5、R6|
|19|22pF|2|C1、C2|
|20|1uF|1|C3|
|21|0.1uF|3|C4、C5、C6|
|22|4.7uF|1|C7|

### キット以外に必要なもの
|部品名|数|
|-|-|
|Kailh LowProfile Switch（Choc V1）|60|
|Choc V1用1Uキーキャップ|60|
|Type-C USB ケーブル|1|
 
### オプション
LED（SK6812MINI-E） 60個
 
### 必要な工具
|工具名||
|-|-|
|はんだごて|D型など細かい作業がしやすいコテ先がおすすめです|
|はんだ||
|フラックス||
|フラックスリムーバー||
|ピンセット||
|精密ドライバー||

## 組み立て
### MCU周辺のはんだ付け
小袋の番号に合わせて基板にはんだ付けしていきます。
ATmega32u2をはんだ付けします。チップの○と基板上の「の方向を合わせてください。
青丸の部分ははんだ付けしなくて構いません。

抵抗とコンデンサーをはんだ付けします。
Type-Cレセプタクルとリセットスイッチをはんだ付けします。
こちらのHEXファイルをダウンロードしてファームウェアを書き込めることを確認しましょう。
- firmware

QMK toolboxでダウンロードしたファイルを開いたら、MCUの欄をATmega3e2U2に変更してリセットスイッチを押し、出てきたFlashのボタンを押します。

動作確認ができたらお好みでエポシキ接着剤で補強すると安心感があります。
### キーボード部品のはんだ付けと組み立て
LEDは最初に取り付けます。足の切り欠きと基板の「の方向を合わせてください。
全て取り付けたら発光を確認しましょう。

ダイオードをはんだ付けします。
全て取り付けたらピンセットでキースイッチのホールを導通させて1〜60が入力されるか確かめてください。

スイッチプレートの保護フィルムを剥がしたら、キースイッチでPCBと挟み込みはんだ付けします。
4隅からはんだ付けすると位置がずれにくいです。

全て取り付けたらもういちど動作を確認しましょう。

PCBにスペーサー（細）（短）をナベねじ（短）で取り付けます。

トッププレートにスペーサー（太）（長）をバインドネジ（長）で取り付けます。

ボトムプレートでミドルプレートを2枚挟み込み、超低頭ねじ（中）で止め、ゴム足を付けます。

キーキャップを差し込んだら完成です。

LEDは左上のキーを押しながら、その下のキーを押すと消灯、横のキーで光り方を変更できます。

## カスタマイズ
キー設定の変更はVIAのwebサイトかアプリケーションを使用します。こちらのJSONファイルをダウンロードしてください。
- json

DESIGNタブのLoadでダウンロードしたJSONファイルを読み込ませるとキーの変更が出来るようになります。  
![](img/VIA_load.jpeg)  
CONFIGUREタブのAuthorize device+からOn the 15 miniを追加してください。

## その他

ファームウェアのフォルダ  
https://github.com/Taro-Hayashi/qmk_firmware/tree/tarohayashi/keyboards/tarohayashi/onthe15mini
  
- BOOTH: https://tarohayashi.booth.pm/items/4500749
