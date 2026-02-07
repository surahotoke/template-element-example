# `template`要素の使い方

`template`要素を活用したモダンで宣言的なDOM操作

詳細はページとコードを見てください

## 使用パターン

### 1. テンプレートクローン（`/pattern-clone`）
`documentFragment`と`replaceChildren`を組み合わせた、高速でメモリ効率の良いリストレンダリング手法です。

- **ポイント**
    - **`template`要素**：HTML構造を不活性な状態で保持し、再利用を容易にします。
    - **`DocumentFragment`**：メモリ上でDOMを構築し、一括で追加することでリフローを最小限に抑えます。
    - **`replaceChildren`**：既存の子要素を安全かつ高速に新しいコンテンツへ置換します。

ページ：https://surahotoke.github.io/template-element-example/pattern-clone

### 2. ウェブコンポーネント（`/pattern-component`）
Web Components (Custom Elements) を活用した、カプセル化されたUI部品の実装手法です。

- **ポイント**
    - **`slot`**：コンポーネント外部から任意のコンテンツを挿入可能にします。
    - **`host`**：コンポーネント自身（カスタム要素）の状態に応じたスタイリングを定義します。
    - **`part`**：カプセル化されたShadow DOM内の特定要素を、外部CSSから操作できるように公開します。
    - **`exportparts`**：ネストされたコンポーネント間で `part` を転送し、親から孫要素へのスタイリングを可能にします。

ページ：https://surahotoke.github.io/template-element-example/pattern-component

## 構成
```
.
├── pattern-clone/
│   └── index.html
├── pattern-component/
│   └── index.html
└── README.md
```