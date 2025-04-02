# M5AtomS3 STEPMotor Base

M5AtomS3でステッピングモーターを制御するためのベースプロジェクトです。

## 概要

このプロジェクトは、M5AtomS3を使用してステッピングモーターを制御するための基本的な実装を提供します。ボタンを押すことで、ステッピングモーターを時計回りに5000ステップ、反時計回りに5000ステップ回転させることができます。

## ハードウェア要件

- M5AtomS3
- ステッピングモーター（200ステップ/回転）
- ステッピングモータードライバー

## ピン接続

- EN (Enable) ピン: GPIO5
- DIR (Direction) ピン: GPIO7
- STEP ピン: GPIO6

## 開発環境

- PlatformIO
- Arduino framework
- M5Unified (v0.2.5以上)

## セットアップ方法

1. このリポジトリをクローンまたはダウンロードします
2. PlatformIOでプロジェクトを開きます
3. `platformio.ini`の設定を確認し、必要に応じて修正します
4. ビルドしてM5AtomS3に書き込みます

## 使用方法

1. 電源を入れると、ディスプレイに「STEP」と表示されます
2. ボタンAを押すと、モーターが以下の動作を行います：
   - 時計回りに5000ステップ回転
   - その後、反時計回りに5000ステップ回転

## カスタマイズ

`main.cpp`の以下の変数を調整することで、モーターの動作をカスタマイズできます：

```cpp
int motor_steps = 200;     // モーターの1回転あたりのステップ数
int step_divisition = 32;  // マイクロステップの分割数
int speed = 300;          // モーターの回転速度
```

## ライセンス

MITライセンスの下で公開されています。詳細は[LICENSE](LICENSE)ファイルを参照してください。