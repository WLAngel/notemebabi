[Pro Git](https://git-scm.com/book/zh-tw/v1) 的簡易筆記，簡單說明重點、需要搭配本文服用。

- 開始
  - 關於版本控制  
    版本控制。
  - Git 的簡史  
    故事。
  - Git 基礎要點  
    三種狀態是重點，很重要。其他部分如果不想深入理解 git 底層的話可以簡略看過。
  - 命令列  
    - Mac: 打開 spotlight 敲上 `terminal`
    - Windows: 開始的搜尋框敲上 `cmd` 或 `powershell`
  - Git 安裝教學  
    找到自己的作業系統照做。
  - 初次設定 Git  
    - 可以稍微筆記一下 git config 參數存放的檔案位置，或者記得有這件事以後來這找。
    - 設定 email 時可以設定和 github 帳號相同的 email。([ref](https://help.github.com/articles/why-are-my-commits-linked-to-the-wrong-user/))
  - 取得說明文件  
    `git help`。
  - 摘要
- Git 基礎
  - 取得一個 Git 倉儲  
    - repository 就是儲存東西的地方。
    - 指令 `git init`: 可以將資料夾初始成 git repository。
    - 指令 `git clone`: 複製一個 repository。
  - 紀錄變更到版本庫中  
    - 指令 `git status`: 檢查檔案狀態。
    - 指令 `git add`: 將檔案加至預存區(staging area)。
    - 檔案 `.gitignore`: 忽略不需要的檔案。
    - 指令 `git diff`: 檢視修改。
    - 指令 `git commit`: 提交修改。
  - 檢視提交的歷史記錄  
    指令 `git log` 的各種選項、參數應用，可以簡略看過，有需求再來這找找。
  - 復原  
    - `git commit` 選項 `--amend`: 建一個新的 commit 取代當前最新 commit。
    - 指令 `git reset HEAD <file>`: 將檔案移出 staging area。
    - 指令 `git checkout -- <file>`: 捨棄工作目錄的修改。
  - 與遠端協同工作  
    - remote repository: 存在其他某處的版本庫。
    - 指令 `git fetch`: 從遠端拉取資料。
    - 指令 `git push`: 更新遠端。
  - 標籤  
    標籤，可以對 commit 打上標籤(較 commit sha 值有識別度)。
  - Git Aliases  
    簡單看過，有需要可以自行設定。
  - 總結
- 使用 Git 分支
  - 簡述分支  
    - 分支，`branch`
    - 很難懂，不過看不懂也不影響使用 git XD。簡單說 branch 是一個指向某提交的可移動指標。
  - 分支和合併的基本用法  
    - 指令 `git branch`: 列出 branch。
    - 指令 `git branch <branch-name>`: 以 <branch-name> 建一個新的 branch。
    - 指令 `git branch -d <branch-name>`: 刪除 <branch-name> branch。
    - 指令 `git checkout <branch-name>`: 切換 branch。
    - 指令 `git checkout -b <branch-name>`: 相當於 git branch <branch-name> && git checkout <branch-name>。
    - 指令 `git merge <branch-name>`: 合併 <branch-name> 到當前 branch 中。
  - 分支管理  
    詳情請看 `git help branch`。
  - 分支工作流程  
    延伸閱讀: [Git flow 開發流程](https://ihower.tw/blog/archives/5140)，看看觀念即可，工具只是輔助而不是重點。
  - 遠端分支  
    重要，花點功夫理解。簡單說 branch 是一個指向某 commit 的可移動指標。
  - 衍合  
    - 指令 `git rebase`: 將 commits 重新套用在別的 branch 上。
  - 總結
- 伺服器上的 Git
  - 通訊協定
  - 在伺服器上佈署 Git
  - 產生你的 SSH 公鑰
  - 設定伺服器
  - Git 常駐程式
  - Smart HTTP
  - GitWeb
  - GitLab
  - 第3方 Git 託管方案
  - 總結
- 分散式的 Git
  - 分散式工作流程
  - 對專案進行貢獻
  - 維護一個專案
  - Summary
- GitHub
  - 建立帳戶及設定
  - 參與一個專案
  - 維護專案
  - Managing an organization
  - Scripting GitHub
  - 總結
