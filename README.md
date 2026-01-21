# 制作物タイトル
Fushimemo(節めも)

# ディレクトリ構成
Feature-based(機能ごとに分割するディレクトリ構成)で作成しています。
個人開発で機能ごとに付け足していく時に継続開発が行いやすいと思い、このようにすることにしました。

fushimemo/
├── app/                  # ルーティング
│   ├── (auth)/login/page.tsx
│   └── books/[id]/page.tsx
│
├── features/             
│   ├── books/            # 「本」機能
│   │   ├── components/   # UIパーツ
│   │   │   ├── BookList.tsx
│   │   │   └── BookCard.tsx
│   │   ├── hooks/        # ロジック・状態管理
│   │   │   └── useBookList.ts
│   │   ├── api/          # データ取得・API
│   │   │   └── getBooks.ts
│   │   └── types/        # 型定義
│   │       └── index.ts
│   │
│   └── memos/            # 「メモ」機能
│
├── components/           # 汎用的なUI（ボタン、ヘッダー）
└── lib/                  # 汎用的な設定（DB接続、axios設定）
