# 密チェッカー 取扱説明書
## 概要
これは３密をチェックする密チェッカーです。  
密閉は二酸化炭素(CO2)濃度で検知し、密集と密接は距離センサーと人感センサーで検知しています。  

## 使い方
1. まずは電源を入れます。サイドにあるスイッチを入れてください。  
2. A STARTと出てきたらAボタンを押します。  
<img src="https://i.imgur.com/R8LWEwq.png" width="400">
3. 上ボタンを押して計測を開始します。  
<img src="https://i.imgur.com/5ZauF0g.png" width="400">
4. 計測完了まで約１５秒かかります。  
<img src="https://i.imgur.com/gJ8ITLh.png" width="400">

5. 計測結果の「Mitsudo: 」のあとの数値が密度です。  
6. 下には各項目の計測結果が表示されます。  
7. 終了する場合はサイドにあるスイッチを切ってください。  再度計測する場合はサイドの黄色いリセットスイッチを押してください。  

## Debug機能について
この密チェッカーにはデバッグ用機能があります。  
Arduino IDE(スケッチエディター)でシリアルモニタを確認すると正確なセンサーの値を見ることができます。
![シリアルモニタ](https://i.imgur.com/sSkcASg.png)  
* シリアルモニタの速度: 9400bps
* 書き方: 「変数名: 変数の値」

### 変数名リファレンス
|変数名|変数内容|  
|---|---|  
|mitsudo|密の度合い|  
|centerMitsu<br>leftMitsu<br>rightMitsu|中央、左、右それぞれの密閉＆密集が当てはまっているか|  
|CO2PPM|二酸化炭素濃度(ppm)|  
|CO2Mitsu|密集が当てはまっているか|  
|centerDistance<br>leftDistance<br>rightDistance|中央、左、右の距離センサーの値|  
|CENTERmotionStatus<br>RIGHTmotionStatus<br>LEFTmotionStatus|中央、左、右の動きセンサーの値(１０回計測)|  
|mippeiTruefalse<br>missyuuTruefalse<br>missetsuTruefalse<br>|密閉、密集、密接のそれぞれ当てはまっているか|  

## 免責事項
この密チェッカーの判定はあくまでも参考値です。  
ご了承ください。

## このリポジトリについて
このファイル（取扱説明書）の最新版は、<https://github.com/nikachu2012/mitsu-checker/blob/main/manual.md> にあります。  
このソフトウェアはオープンソースとして公開しています。  
リポジトリは<https://github.com/nikachu2012/mitsu-checker/>にあります。  
後々回路図等も追加していく予定です。　　

## 更新履歴&バージョン
version: 1.00  

#### version: 1.00
初版公開。
