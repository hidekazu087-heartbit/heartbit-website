# Heartbit Webサイト更新手順（Git / GitHub）

## 1. VS Codeでファイルを編集

作業フォルダ：
`C:\Users\hidek\Documents\GitHub\heartbit-website`

`index.html` などを編集し、Ctrl + S で保存。

## 2. PowerShellで作業フォルダへ移動

```powershell
cd C:\Users\hidek\Documents\GitHub\heartbit-website
```

## 3. 変更内容を確認

```powershell
git status
git diff
```

## 4. 変更をステージング

```powershell
git add .
```

※ `.` は変更したファイルすべて。特定ファイルだけなら `git add index.html`

## 5. 変更をコミット

```powershell
git commit -m "Update website"
```

※ メッセージは変更内容に応じて書き換える。

## 6. GitHubへ反映

```powershell
git push
```

## 7. Webサイトを確認

GitHubへのpushが成功すると、XServer Staticが自動デプロイ。

https://heartbit.co.jp/

ブラウザで更新結果を確認する。

## 8. 最後に状態確認

```powershell
git status
```

`nothing to commit, working tree clean` ならOK。

---

## 覚えておくこと

- `git status`：変更状態を確認
- `git diff`：変更内容を確認
- `git add .`：変更を登録対象にする
- `git commit -m "..."`：ローカルに変更履歴を記録
- `git push`：GitHubへ送信
- `git pull`：GitHub側の変更をローカルへ取り込む

**更新の流れ**

VS Code → 保存 → add → commit → push → GitHub → XServer Static → Webサイト更新