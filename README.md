# Zed Editor Configuration

Zed エディタのユーザー設定リポジトリ (`~/.config/zed`)

## ファイル構成

| ファイル | 説明 |
|---|---|
| `settings.json` | エディタのグローバル設定 (テーマ、フォント、UI、vim_mode 等) |
| `keymap.json` | キーバインド設定 |
| `.zed/settings.json` | プロジェクト固有の設定 (LSP、フォーマッター、言語別設定) |

全ての設定ファイルは JSONC (コメント付き JSON) 形式。

## 主な設定

- **テーマ**: Catppuccin Mocha (No Italics)
- **Vim mode**: 有効 (相対行番号)
- **フォント**: UI / バッファ共に 16px
- **スクロールバー**: 非表示
- **Agent (AI 機能)**: 無効

## ツールチェイン

| 用途 | ツール |
|---|---|
| フォーマッター | [oxfmt](https://oxc.rs/) (prettier 無効化、保存時に実行) |
| リンター | [oxlint](https://oxc.rs/) (typeAware 有効、入力時に実行) |

対象言語: JavaScript, TypeScript, TSX, JSON, JSONC, CSS, HTML, Markdown, YAML

## キーバインド

### Pane 移動 (全コンテキスト共通)

| キー | アクション |
|---|---|
| `ctrl-h` | 左の Pane へ移動 |
| `ctrl-j` | 下の Pane へ移動 |
| `ctrl-k` | 上の Pane へ移動 |
| `ctrl-l` | 右の Pane へ移動 |

### Leader key (`space`) — Normal / Visual mode

| キー | アクション |
|---|---|
| `space f` | ファイル検索 |
| `space o` | タブスイッチャー |
| `space s` | 保存 |
| `space t` | 新規ターミナル |
| `space c` | アクティブタブを閉じる |
| `space b c` | 他のタブを閉じる |
| `space b C` | 全タブを閉じる |

### Pane Split (Terminal)

| キー | アクション |
|---|---|
| `cmd-alt-h` | 左に分割 |
| `cmd-alt-j` | 下に分割 |
| `cmd-alt-k` | 上に分割 |
| `cmd-alt-l` | 右に分割 |

### その他

| キー | コンテキスト | アクション |
|---|---|---|
| `j j` | Insert mode | Normal mode に戻る |
| `shift-j` / `shift-k` | Normal / Visual | 前 / 次のタブ |
| `s s` | Normal / Visual | アウトライン切替 |
| `ctrl-space` | Terminal | Vi mode 切替 |
| `space f` | EmptyPane | ファイル検索 |

### メニュー操作

| キー | アクション |
|---|---|
| `ctrl-j` | 次の項目 |
| `ctrl-k` | 前の項目 |
| `ctrl-l` | 確定 |

### Project Panel

| キー | アクション |
|---|---|
| `a` | 新規ファイル |
| `o` | 新規ディレクトリ |
| `r` | リネーム |
| `d` | 削除 |
| `x` / `y` / `p` | カット / コピー / ペースト |

### Tab Switcher

| キー | アクション |
|---|---|
| `j` / `k` | 次 / 前の項目 |
| `l` | 確定 |
| `x` | 選択タブを閉じる |
