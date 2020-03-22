# Assembly instructions

Palette Keyboard, Palette Keyboard Alpha の組立説明書です。

This is an assembly manual common to Palette Keyboard and Palette Keyboard Alpha.

## Tools 道具

![_MG_8063](https://user-images.githubusercontent.com/617057/77240626-4aa5e100-6c2b-11ea-9ac3-c7e08831e65e.jpg)
![_MG_8035](https://user-images.githubusercontent.com/617057/77240634-50032b80-6c2b-11ea-81b3-f28258ad17cc.jpg)
![_MG_8047](https://user-images.githubusercontent.com/617057/77240635-509bc200-6c2b-11ea-9a4d-ba730807d2e1.jpg)

## Parts パーツ
![_MG_8050](https://user-images.githubusercontent.com/617057/77240633-4f6a9500-6c2b-11ea-8922-59581f6de701.jpg)
### Mandatory 必ず必要なもの
| Parts | Amount |
----|----
| PCB | 2 |
| Top plate | 2 |
| Bottom plate | 2 |
| ProMicro Cover Plate | 2 |
| ProMicro | 2 |
| TRRSジャック | 2 |
| タクトスイッチ	| 2 |
| ダイオード（チップ部品）	| 46 |
| Kailh PCBソケット（MX用） | 44 |
| キースイッチ（CherryMX互換にのみ）	| 44 |
| キーキャップ 1u	| 40 |
| キーキャップ 1.5u	| 4 |
| OLEDモジュール |	2 |
| ピンヘッダ 4連 | 2 |
| ピンソケット4連 | 2 |
| スペーサー M2 6.5mm	| 10 |
| スペーサー M2 8mm	| 4 |
| ネジ M2 4mm	| 28 |
| クッションゴム	| 16 |
| TRS(3極)ケーブル	| 1 |
| Micro USBケーブル	| 1 |
### Optional 追加で使うもの



## How to assemble 組み立て方

### ファームウェアのコンパイル
```sh
git clone git@github.com:Yuichiroh/qmk_firmware.git
git checkout palette_on_custom_drashna
make git-submodule
```

### ダイオードの取り付け
PCBはリバーシブルです。はじめにそれぞれどちら側に使うかを決めます。
![_MG_8054](https://user-images.githubusercontent.com/617057/77240630-4d083b00-6c2b-11ea-86f2-854fdad36761.jpg)
![_MG_8053](https://user-images.githubusercontent.com/617057/77240631-4da0d180-6c2b-11ea-96b6-728c84005a2e.jpg)

ダイオードを付けます。裏表どちらにつけても構いませんが、ホコリ等の観点から裏側を推奨します。
![_DSC0018](https://user-images.githubusercontent.com/617057/77240637-51ccef00-6c2b-11ea-8557-30881020ff65.jpg)
サイズ感はこのくらいです。指で扱うのはかなり厳しいのでピンセットを使います。
![_MG_8057](https://user-images.githubusercontent.com/617057/77240632-4ed1fe80-6c2b-11ea-826f-db16dd579ea1.jpg)
ダイオードには向きがあります。PCBにプリントされている表示とダイオードの表示の縦棒がそろうように配置します。逆向きにつけるとキーが反応しませんので注意してください。
![_DSC0025](https://user-images.githubusercontent.com/617057/77240629-4c6fa480-6c2b-11ea-963a-23acc1bfc678.jpg)

ダイオードを置く前に先にランドの片側に予備ハンダをしておくとつけやすいでしょう。
![_DSC0028](https://user-images.githubusercontent.com/617057/77240628-4bd70e00-6c2b-11ea-9e8e-417311d90094.jpg)
ダイオードを適切な位置にピンセットで抑えながらランドの予備ハンダを溶かしてダイオードを固定していきます。位置がずれたら一度溶かして取り外し、またピンセットで固定しながら正しい位置でランドのハンダを溶かして固定します。この時点でまっすぐ真ん中に付けられているときれいに仕上がります。
![_DSC0032](https://user-images.githubusercontent.com/617057/77240627-4b3e7780-6c2b-11ea-86da-5642b360fea4.jpg)
片側固定できたら、反対側をはんだ付けしていきます。
![_DSC0034](https://user-images.githubusercontent.com/617057/77240625-4a0d4a80-6c2b-11ea-99a4-4d2b5f43671f.jpg)

### TRRS ジャック、リセットスイッチの取り付け
**表側** にTRRSジャックとリセットスイッチをつけます（写真は右手側です）。パーツが浮かないように表面側にマスキングテープを貼って固定します。
![_DSC0036](https://user-images.githubusercontent.com/617057/77241240-9dcf6200-6c32-11ea-9e48-dcdeb84f386a.jpg)
![_DSC0037](https://user-images.githubusercontent.com/617057/77241251-c8b9b600-6c32-11ea-8f45-1f6f0081b204.jpg)

OLEDを付ける場合はOLED用のソケットをつけます。OLEDは設置の高さがシビアに設計されていますので、ソケットがPCBから浮かないように必ずマスキングテープで固定してからハンダ付けしてください。
![_DSC0040](https://user-images.githubusercontent.com/617057/77240620-4679c380-6c2b-11ea-9a65-a19219b78124.jpg)
横から見て浮いていないことを確認してください。次にOLED用のジャンパをつなぎます。ハンダを多めに盛るとくっつきます。ハンダのフラックスが揮発する前になでると丸くつながります。難しい場合は別途フラックスを塗ってから行うと簡単です。
![_DSC0048](https://user-images.githubusercontent.com/617057/77240621-47125a00-6c2b-11ea-9c58-8270757f7244.jpg)

### ProMicro の取り付け
ProMicroにスプリングピンヘッダをハンダ付けします。スプリングピンヘッダとProMicroの向きを確実に確認してください。スプリングピンヘッダには上下の向きがあります。窓があるので、この窓がProMicro側になるようにつけます。
![_DSC0052](https://user-images.githubusercontent.com/617057/77240617-437ed300-6c2b-11ea-8a92-4210d7d672ad.jpg)
さらに、スプリングピンヘッダには左右の向きもあります。写真のように窓が同じ側を向くようにつけます。付ける前に必ず基盤のパーツがピンヘッダ側にきていることを確認してください。
![_DSC0054](https://user-images.githubusercontent.com/617057/77240619-45e12d00-6c2b-11ea-81cb-204b00173c1d.jpg)
取り付けは表面側に挿します。PCBのプリントに従い、黒い枠線がある側に差し込みます（反対に挿すと動きません）。
![_DSC0058](https://user-images.githubusercontent.com/617057/77240615-42e63c80-6c2b-11ea-9529-53e3e8658e1c.jpg)

OLEDを付ける場合、この時点でOLEDをハンダ付けします。まず、写真のように先にピンヘッダを差し込みます。
![_DSC0060](https://user-images.githubusercontent.com/617057/77240614-424da600-6c2b-11ea-9a60-e24da1fede21.jpg)
ピンヘッダの上にOLEDを置き、これも浮かないようにマスキングテープでしっかりと固定してからハンダ付けします。
![_DSC0064](https://user-images.githubusercontent.com/617057/77240616-437ed300-6c2b-11ea-9db1-eda470bd62e0.jpg)
最終的にこのようになります。
![_DSC0069](https://user-images.githubusercontent.com/617057/77240613-41b50f80-6c2b-11ea-9729-0a94f345db5c.jpg)
この時点で一度ファームウェアを書き込み動作テストします。ピンセット等でスイッチソケットのランドを連絡してキー入力が行えるか確認します。
![_DSC0072](https://user-images.githubusercontent.com/617057/77240612-411c7900-6c2b-11ea-897f-2810afa5327f.jpg)

ファームウェアの書き込みを行うには、PCと一方のProMicroをUSBケーブルでつなぎ、次のコマンドを打ちます。その後、コンソールに表示される指示のタイミングでリセットスイッチを２回押します。
```
# 左手用
make palette_alpha:default:avrdude-split-left

# 右手用
make palette_alpha:default:avrdude-split-right
```

### キーソケットの取り付け
最初にランド両側にかなり厚めにハンダを盛っておきます（写真下）。その後、写真上のようにキーソケットを置いていき、片側ずつハンダをしっかり溶かしながら浮きがないように接合させていきます。
![_DSC0076](https://user-images.githubusercontent.com/617057/77240611-4083e280-6c2b-11ea-94e8-b7ca5da78f8c.jpg)
このように横から見て浮きがないか確認してください。
![_DSC0081](https://user-images.githubusercontent.com/617057/77240609-3feb4c00-6c2b-11ea-94e2-e6ee39335910.jpg)

### LED の取り付け
動画を置きます。
![_DSC0083](https://user-images.githubusercontent.com/617057/77240608-3f52b580-6c2b-11ea-8ca8-0a75121bdef2.jpg)

### ロータリーエンコーダーの取り付け
必ずプレートを付ける直前に行ってください。他のパーツの取付の邪魔になります。
![_DSC0087](https://user-images.githubusercontent.com/617057/77240607-3eba1f00-6c2b-11ea-8d74-5a61ffb4676e.jpg)
![_DSC0089](https://user-images.githubusercontent.com/617057/77240605-3cf05b80-6c2b-11ea-800b-d5beb873dbfb.jpg)

### プレート類の取り付け
最初にマイコン部保護プレートを取り付けてください。
![_DSC0109](https://user-images.githubusercontent.com/617057/77240600-382ba780-6c2b-11ea-8b42-8e11610c00b2.jpg)
なぜならネジがバックプレートより内側に来るからです。
![_DSC0111](https://user-images.githubusercontent.com/617057/77240599-37931100-6c2b-11ea-91c6-c6a9d62ddab1.jpg)
次にバックプレートをつけます。
![_DSC0095](https://user-images.githubusercontent.com/617057/77240604-3c57c500-6c2b-11ea-9194-05f37a471a26.jpg)

![_DSC0113](https://user-images.githubusercontent.com/617057/77240598-36fa7a80-6c2b-11ea-9b3e-7171361f7761.jpg)


<!-- ![_DSC0108](https://user-images.githubusercontent.com/617057/77240601-38c43e00-6c2b-11ea-905e-9fc244818ec1.jpg) -->

![_MG_8140](https://user-images.githubusercontent.com/617057/77240593-306c0300-6c2b-11ea-9912-b9583f40c354.jpg)
