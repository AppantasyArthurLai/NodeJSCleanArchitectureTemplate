## 言語

- [English](README.md)

# NodeJS クリーンアーキテクチャ テンプレート

この Express アプリは、クリーンアーキテクチャを使用してスケーラブルな Express アプリケーションを構築するためのボイラープレートです。コントローラー、ドメインロジック、サービスなどの論理的なコンポーネントに懸念事項を分割するように設計された整理された構造を提供します。組み込みのテストと構成管理を備えたこのテンプレートは、堅牢な Web アプリケーションを効率的に開発するためのものです。


## 1. ディレクトリ構造

プロジェクト構造は以下のとおりです。

``` console
my-express-app/
│
├── src/
│   ├── config/            # アプリケーション設定、データベース接続、環境変数など
│   ├── controllers/       # ルートや HTTP リクエスト/レスポンスに関連するコントローラー
│   ├── domain/            # アプリケーションのコアロジックとエンティティ（ビジネスロジック、モデルなど）
│   ├── use_cases/         # 特定の機能を実装するロジック（ユースケース）
│   ├── repositories/      # データアクセス抽象化を格納し、データベースや他の外部データソースにアクセス
│   ├── services/          # 外部サービスに関連するコード、メール送信、支払い処理など
│   ├── middleware/        # 認証、認可、エラー処理などのミドルウェア
│   ├── helpers/           # さまざまなヘルパー関数とユーティリティ
│   └── app.js             # アプリケーションのメインエントリーポイント
│
├── tests/
│   ├── controllers/       # コントローラーのテスト
│   ├── domain/            # ドメインロジックのテスト
│   ├── use_cases/         # ユースケースのテスト
│   ├── repositories/      # データアクセスロジックのテスト
│   └── services/          # サービスのテスト
│
├── .env                   # 環境変数を保存するファイル
├── .gitignore             # Git の無視ルール
├── package.json           # プロジェクトの依存関係とメタデータを格納
└── README.md              # プロジェクトの説明文書
```


## 2. 使い方

このテンプレートを独自のプロジェクトで使用するには、以下の手順に従ってください。

1. リポジトリをクローンし、任意のプロジェクトディレクトリに配置します（`my-express-app`をお好みのディレクトリ名に置き換えてください）: `git clone https://github.com/AppantasyArthurLai/NodeJSCleanArchitectureTemplate.git my-express-app`
2. プロジェクトディレクトリに移動します: `cd my-express-app`
3. 元のリモートを削除し、新しいリモートオリジンとして自分のリポジトリを追加します:
``` console
git remote remove origin
git remote add origin https://github.com/yourusername/your-repo.git
```
4. 依存関係をインストールします: `npm install`
5. `.env`ファイルを作成し、必要な環境変数を設定します。
6. 開発サーバーを起動します: `npm run dev`
7. テストを実行します: `npm test`


## 3. Changelog

### v1.0.0 (2023-05-08)

- 初回リリース

## 4. Contributors

- [Arthur Lai](https://github.com/AppantasyArthurLai)

## 5. ライセンス

このプロジェクトは [MITライセンス](https://opensource.org/licenses/MIT) の下でオープンソース化されています。ライセンスの条件に従って、コードを自由に使用、変更、配布することができます。
