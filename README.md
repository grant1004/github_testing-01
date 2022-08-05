# github_testing 
# learn how to use github && git 

## git --version 查看版本 

## git config --global init.defaultBranch main 設置 branch 為 main 

## git init 建立數據庫

## git status 查看數據庫狀態 
> 你可以看到 Untracked files 有檔案，
> Untracked 的意思是，Git 偵測到你有新增這筆檔案，但尚未是 Git 追蹤的對象。( 代表 working )

## git add .  
> 所以必須先將它加入到 staging area(索引)裡，就可以將檔案加入到追蹤對象。
> . 代表全部內容, 或是可以指定檔名( git add xxx.txt )
> git status 會發現該檔案狀態本來是 Untracked files，
> 變成是Changes to be committed，這樣就表示有成功加入到索引。

## git commit -m "<填寫版本資訊>" 
> [master (root-commit) b6c3c77] "<填寫版本資訊>"
> 1 file changed, 0 insertions(+), 0 deletions(-)
> create mode 100644 XXX.txt
> 再次使用 git status 觀察，會獲得以下資訊
> On branch master
> nothing to commit, working tree clean
> 代表沒有任何工作內容

## git log 查看最近有甚麼更新
> commit b6c3c771cd8939bcd25a8c50089fdf0cd3eab98d (HEAD -> master)
> Author: 姓名 <Email>
> Date:   版本更新時間
---

總結 : 以下都是在同一個資料夾下面完成 
1. git init 把此資料夾當做數據庫   
2. 建立檔案並撰寫完 ( working area ) 
3. 使用 git add 將檔案加進數據庫的 staging area 
4. git commit -m "<填寫版本資訊>" 完成更新數據庫 
  
> 單一檔案加入索引：git add <檔案名稱>
> 所有檔案加入索引：git add .
> 提交版本：git commit -m "填寫版本資訊"
> 觀看當前狀態：git status
> 瀏覽歷史紀錄：git log
---

# 連結遠端數據庫
// 前置作業 : 先將此資料夾利用 git init 建立成數據庫(repository)
git remote add origin <github網址>




