# 原神 Discord Bot

原神のキャラクターを使った Discord Bot です。ランダムチーム編成やキャラクターのフレーズを返すことができます。

## 機能

- **ランダムチーム編成**: 指定した条件でランダムなチームを生成
- **アルハイゼン構文**: アルハイゼン風の構文を返す
- **煙緋のボイス**: 煙緋のセリフを返す
- **パイモン反応**: 「えへ」に反応
- **トーマの反応**: 「俺」が含まれた場合にトーマのセリフを返す

## セットアップ

1. プロジェクトをクローンまたはダウンロード
2. 依存関係をインストール：
   ```bash
   npm install
   ```
3. 環境変数を設定：
   ```bash
   export TOKEN=your_discord_bot_token
   ```
4. ボットを起動：
   ```bash
   npm start
   ```

## 使い方

### チーム編成コマンド

```
/チーム /チーム数 3
```

#### オプション
- `/レア度 4星` または `/レア度 5星` - レア度でフィルタ
- `/元素 炎,水,風` - 元素でフィルタ（複数指定は`,`で区切る）
- `/性別 男` または `/性別 女` - 性別でフィルタ
- `/所持 所持` または `/所持 未所持` - 所持状況でフィルタ

#### 完全例
```
/チーム /チーム数 2 /レア度 5星 /元素 炎,雷 /性別 女 /所持 所持
```

### その他のコマンド

- `/アルハイゼン` - アルハイゼン構文を返す
- `/煙緋` - 煙緋のセリフを返す
- `/終了` - ボットを終了する
- メンション - ボットにメンションすると反応する
- 「えへ」 - パイモンが反応する
- 「俺」 - トーマが反応する

## プロジェクト構造

```
src/
├── index.js              # メインファイル
├── config/
│   └── config.js         # 設定ファイル
├── data/
│   ├── characters.js     # キャラクターデータ
│   └── phrases.js        # フレーズデータ
├── commands/
│   ├── teamCommand.js    # チームコマンド
│   ├── phraseCommands.js # フレーズコマンド
│   └── systemCommands.js # システムコマンド
└── utils/
    ├── messageUtils.js   # メッセージユーティリティ
    └── httpServer.js     # HTTPサーバー
```

## 環境変数

- `TOKEN` - Discord Bot のトークン（必須）
- `PORT` - HTTPサーバーのポート（デフォルト: 3000）

## 開発

開発モードで起動：
```bash
npm run dev
```

## ライセンス

MIT
