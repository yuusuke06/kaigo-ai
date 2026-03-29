# ケアノートAI — デプロイ手順書
石崎さんへ。この手順通りに進めれば30分以内に完了します。

## ファイル構成
```
kaigo-ai/
├── api/
│   └── generate.js   ← APIキーを隠すサーバー
├── public/
│   └── index.html    ← スマホ用アプリ本体
├── vercel.json       ← Vercel設定
└── README.md         ← この手順書
```

## 手順1: このファイルをGitHubにアップロード
1. github.com/yuusuke06/kaigo-ai を開く
2. 「uploading an existing file」をクリック
3. 4ファイルを全部アップロード
4. 「Commit changes」をクリック

## 手順2: VercelにデプロイするGitHubリポジトリはすでに作成済みなのでImportするだけ
1. vercel.com を開く
2. 「Add New Project」→「Import」
3. kaigo-ai リポジトリを選択
4. 「Deploy」をクリック（設定変更不要）

## 手順3: APIキーを環境変数に設定（最重要）
1. Vercelのプロジェクトページを開く
2. 「Settings」→「Environment Variables」
3. 以下を追加:
   - Name: ANTHROPIC_API_KEY
   - Value: sk-ant-api03-（ここに実際のキーを貼り付け）
4. 「Save」をクリック
5. 「Deployments」→「Redeploy」で反映

## 手順4: 動作確認
発行されたURL（例: kaigo-ai.vercel.app）をスマホで開いて
記録を生成できれば完了です。

## スタッフへの共有
URLをLINEで送るだけでOKです。
インストール不要・APIキー入力不要で全員が使えます。

## 困ったときは
Vercelのログは「Deployments」→「Functions」で確認できます。
