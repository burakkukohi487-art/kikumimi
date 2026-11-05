## ブランチ運用
- main は常に動く状態。main への直接コミットは `docs/`、`README.md`、`CLAUDE.md`、`.specify/memory/constitution.md` のみ許可
- それ以外（コード・`specs/`）は必ず機能ブランチ → PR でマージ
- 機能ブランチは Spec Kit の命名に従う：`001-admin-auth` のように `番号-機能名`
- 修正は `fix/内容`、雑務は `chore/内容`
- 並列開発は git worktree で `../kikumimi-<ブランチ名>` に作成する

## コミット
- Conventional Commits：`feat:` `fix:` `docs:` `test:` `refactor:` `chore:`
- 1コミット = 1つの意味のある変更。tasks.md の1タスク ≒ 1コミットを目安
- フロントとバックの変更が同じ機能なら同じコミットでよい
- メッセージは日本語。例：`feat(backend): 管理グループ作成APIを追加`

## コメント
- 「何をしているか」ではなく「なぜそうしたか」を書く
- Python：関数・クラスに Google スタイルの docstring
- TypeScript：公開関数・コンポーネントに TSDoc（`/** */`）
- LLMのプロンプトは定数化し、意図をコメントで残す
- TODO は `TODO(kikumimi): 内容` の形式