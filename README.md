# 制作物タイトル
Fushimemo(節めも)

## ディレクトリ構成

このプロジェクトでは、機能単位（Feature-based）で分割したMVCライクな構成を採用しています。

```text
fushimemo/
├── app/                  # ルーティング (App Router)
│   ├── (auth)/login/page.tsx
│   └── books/[id]/page.tsx
│
├── features/             # 機能単位のモジュール (Feature-based MVC)
│   ├── books/            # 「本」機能
│   │   ├── components/   # [View] UIパーツ
│   │   │   ├── BookList.tsx
│   │   │   └── BookCard.tsx
│   │   ├── hooks/        # [Controller] ロジック・状態管理
│   │   │   └── useBookList.ts
│   │   ├── api/          # [Model] データ取得・API
│   │   │   └── getBooks.ts
│   │   └── types/        # [Model] 型定義
│   │       └── index.ts
│   │
│   └── memos/            # 「メモ」機能
│
├── components/           # 汎用的なUI（ボタン、ヘッダーなど）
└── lib/                  # 汎用的な設定（DB接続、axios設定など）
