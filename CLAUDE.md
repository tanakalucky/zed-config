# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

Zed エディタのユーザー設定リポジトリ（`~/.config/zed`）。主な設定ファイルは以下の2つ:

- **settings.json** — エディタのグローバル設定（テーマ、フォント、UI、vim_mode等）
- **keymap.json** — キーバインド設定
- **.zed/settings.json** — プロジェクト単位の設定（LSP、フォーマッター、言語別設定）

## Key Configuration Decisions

- **Vim mode** が有効。キーバインドはVimスタイルで統一されている
- **Leader key** は `space` を使用（`space f` でファイル検索、`space s` で保存など）
- **Pane移動** は `ctrl-h/j/k/l` で統一（Editor, Terminal, ProjectPanel, AgentPanel, EmptyPane 全てのコンテキストで設定）
- **Insert mode脱出** は `j j`
- **テーマ**: Catppuccin Mocha (No Italics)
- **フォーマッター**: prettier を無効化し、全言語で **oxfmt** (oxc) を使用
- **リンター**: **oxlint** を使用（typeAware有効、onType実行）
- **Agent (AI機能)** は無効化されている

## File Format Notes

- settings.json と keymap.json は **JSONC**（コメント付きJSON）形式
- .zed/settings.json はプロジェクト固有のオーバーライド用（trailing comma許容のJSONC）
- keymap.json の各エントリには `context` フィールドでスコープを限定できる

## Development Workflow

設定ファイル（`settings.json`, `keymap.json`, `.zed/settings.json`）を変更した後は、以下のフローに従うこと:

1. `README.md` と `CLAUDE.md` の内容を確認し、変更内容との乖離がないかチェックする
2. 乖離がある場合は、ドキュメントも合わせて更新する
   - 例: キーバインドの追加/変更 → README のキーバインド表と CLAUDE.md の Key Configuration Decisions を更新
   - 例: テーマやフォーマッターの変更 → 両ドキュメントの該当箇所を更新
