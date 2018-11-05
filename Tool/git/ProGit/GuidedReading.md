[Pro Git](https://git-scm.com/book/zh-tw/v2) 的簡易導讀，請搭配本文服用。  
這裏有 [v1](https://git-scm.com/book/zh-tw/v1)，中文支援度比 v2 高一點點，可以參考一下。  
不過程度允許的話還是看英文比較好，畢竟 git 指令的說明書都是寫英文。

- 開始
  - 關於版本控制  
    了解一下什麼是版本控制。
  - Git 的簡史  
    故事。
  - Git 基礎要點  
    對於 git 的使用上，三種狀態的觀念很重要。其他部分如果不想深入理解 git 底層的話可以簡略看過。
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
    - 指令 `git init`: 將資料夾初始成 git repository。
    - 指令 `git clone`: 複製一個 repository。
  - 紀錄變更到版本庫中  
    - 指令 `git status`: 檢查檔案狀態。
    - 指令 `git add`: 將檔案加至預存區(staging area)。
    - 檔案 `.gitignore`: 用來設定讓 git 忽略不需要的檔案。
    - 指令 `git diff`: 檢視修改。
    - 指令 `git commit`: 提交修改。
  - 檢視提交的歷史記錄  
    指令 `git log` 的各種選項、參數應用，可以簡略看過，有需求再來這找找或者是自己看 manual。
  - 復原  
    - `git commit` 選項 `--amend`: 建一個新的 commit 取代當前最新 commit。
    - 指令 `git reset HEAD <file>`: 將檔案移出 staging area。
    - 指令 `git checkout -- <file>`: 捨棄工作目錄的修改。
  - 與遠端協同工作  
    - remote repository: 存在其他某處的版本庫。
    - `git remote` 的相關指令可以稍微玩一下，但應該多數情況下遠端只會有一個預設的 origin。
    - 指令 `git fetch`: 從遠端拉取資料。
    - 指令 `git push`: 更新遠端。
  - 標籤  
    標籤，可以對 commit 打上標籤(較 commit sha 值有識別度)。
  - Git Aliases  
    簡單看過，有需要可以自行設定。
  - 總結
- 使用 Git 分支
  - 簡述分支  
    - 分支，`branch`。
    - commit 結構可能很難懂，不過看不懂也不影響使用 git XD。簡單說 branch 是一個指向某提交的可移動指標。
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
  如果你對架設自己的伺服器沒興趣，就不用深究本章。大部分情況會使用 github 作為 git 伺服器。
  - 通訊協定  
    常用的應該是 ssh 協議。
  - 在伺服器上佈署 Git  
    `bare repository` 是用來儲存 git repository 相關資訊的。
  - 產生你的 SSH 公鑰  
    文末有[鏈結](https://help.github.com/articles/connecting-to-github-with-ssh/)可以看如何使用 ssh 連接到 github。
  - 設定伺服器  
    伺服器相關，沒興趣的話看看就好。讓其他人可以透過 ssh 取用你的 git server。
  - Git 常駐程式  
    伺服器相關，沒興趣的話看看就好。設定 git 協議的 daemon。
  - Smart HTTP  
    伺服器相關，沒興趣的話看看就好。
  - GitWeb  
    伺服器相關，沒興趣的話看看就好。將自己的 git server 用 web 介面表示。
  - GitLab  
    伺服器相關，沒興趣的話看看就好。
  - 第3方 Git 託管方案
  - 總結
- 分散式的 Git
  這章節可以等熟悉各種常用的 git 指令之後再來看。
  - 分散式工作流程  
    常見的是整合式管理員工作流程 Integration-manager workflow，github 就是這種流程。
  - 對專案進行貢獻  
    介紹一些工作流程。
  - 維護一個專案  
    一些情境及指令應用。感覺大部分不是很重要。可以等有一些經驗或理解再來看。
  - Summary
- GitHub
  - 建立帳戶及設定  
    自己看。
  - 參與一個專案  
    前面提到的整合式管理員工作流程 Integration-manager workflow 和一些 github 上的操作。
  - 維護專案  
    看看就好，使用時慢慢摸也行。
  - Managing an organization  
    有需要再看。
  - Scripting GitHub  
    webhook, github services 和 github api 的應用。另外 services 要沒了: [Announcing the deprecation of GitHub Services](https://developer.github.com/changes/2018-04-25-github-services-deprecation/)
  - 總結
