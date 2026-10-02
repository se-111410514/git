# Git 與 GitHub 協作流程解說

本文件解說如何透過 Git 指令與 GitHub 介面完成「分支」、「合併」、「Fork」與「Pull Request」。

---

## 1. 分支 (Branch)

分支用於在不影響主線（`main`）的情況下獨立開發新功能或修復問題。

### 操作指令：
- 建立並切換到新分支：
  git checkout -b developGitBranch
- 查看目前所在分支：
  git branch
- 提交修改：
  git add .
  git commit -m "feat: 新增分支功能"
- 推送新分支至遠端：
  git push -u origin developGitBranch

---

## 2. 合併 (Merge)

將特定分支的修改合併回主分支。

### 操作指令：
- 切換回主分支：
  git checkout main
- 拉取最新進度：
  git pull origin main
- 將開發分支合併進主分支：
  git merge developGitBranch
- 推送合併結果至遠端：
  git push origin main

---

## 3. Fork（分叉/複製專案）

當沒有原專案的直接寫入權限時，可透過 Fork 將專案完整複製一份至個人帳號下進行修改。

### GitHub 介面步驟：
1. 進入母專案（例如：`se-111410514/git`）。
2. 點選頁面右上角的 Fork 按鈕。
3. 選擇個人帳號為 Owner，並完成 Fork 建立個人子專案（如：`Eason-Xie302/git`）。

---

## 4. Pull Request (PR)

在個人子專案或分支修改完成後，向原專案請求審核並合併程式碼。

### GitHub 介面步驟：
1. 進入子專案頁面，點選 Contribute 下拉選單並選擇 Open pull request。
2. 設定比對方向：
   - base repository（左邊接收端）：母專案（`se-111410514/git`），分支為 `main`。
   - head repository（右邊來源端）：子專案（`Eason-Xie302/git`），分支為 `developGitBranch`。
3. 填寫 PR 標題與修改內容說明。
4. 點選 Create pull request 送出審核。
5. 原專案管理者確認無誤後，點選 Merge pull request 完成合併。
