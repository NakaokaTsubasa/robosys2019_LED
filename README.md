# ロボットシステム学 − 課題1
17C1102　中岡翼
## 概要
入力する値(0,1)によってLEDが点灯・消灯し、`led.sh`を実行することによって入力したアルファベットのモールス信号が発信されます。
sleepの動作をC言語内で実装し、また、モールス信号をおこなう際の短点、長点の動作を関数化しました。
## 動画
- URL − https://youtu.be/zCBZ2dDzIzU
## 使用するもの
- Raspberry Pi 3 Model B+
  - Raspbian
- LED
- 抵抗：300[Ω]
## 使い方
1. リポジトリをクローンしてローカルリポジトリの作成
   ```
   $ git clone https://github.com/NakaokaTsubasa/robosys2019_LED.git
   $ cd robosys2019_LED
   ```
2. コンパイル、インストール
   ```
   $ sh make.sh
   ```
   コマンドでおこなう場合
   ```
   $ make
   $ sudo insmod myled.ko
   $ sudo chmod 666 /dev/myled0
   ```
3. モールス信号の発信
   ```
   $ sh led.sh
   ```
4. 後始末
   ```
   $ sh clean.sh
   ```
   コマンドでおこなう場合
   ```
   $ sudo rm /dev/myled0
   $ sudo rmmod myled
   ```
