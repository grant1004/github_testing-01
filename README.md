
# git hub 學習筆記 ( cmd | bash 使用方式 ) ( windows 10 )
# learn how to use github && git 

### git --version 查看版本 

### git config --global init.defaultBranch main 設置 branch 為 main 

### git init 建立數據庫

### git status 查看數據庫狀態 
> 你可以看到 Untracked files 有檔案，
> 
> Untracked 的意思是，Git 偵測到你有新增這筆檔案，但尚未是 Git 追蹤的對象。

### git add .  
> 所以必須先將它加入到 staging area(索引)裡，就可以將檔案加入到追蹤對象。
> 
> . 代表全部內容, 或是可以指定檔名( git add xxx.txt )
> 
> git status 會發現該檔案狀態本來是 Untracked files，
> 
> 變成是Changes to be committed，這樣就表示有成功加入到索引。

### git commit -m "<填寫版本資訊>"   
> 用來更新版本並上傳更新備註
> 
> [master (root-commit) b6c3c77] "<填寫版本資訊>"
> 
> 1 file changed, 0 insertions(+), 0 deletions(-)
> 
> create mode 100644 XXX.txt
> 
> 再次使用 git status 觀察，會獲得以下資訊
> 
> On branch master
> 
> nothing to commit, working tree clean
> 
> 代表沒有任何工作內容

### git log 查看最近有甚麼更新
> commit b6c3c771cd8939bcd25a8c50089fdf0cd3eab98d (HEAD -> master)
> 
> Author: 姓名 <Email>
>
> Date:   版本更新時間
>
> 版本資訊
---

> 本地數據庫 使用方法 
> 1. git init 把此資料夾當做數據庫   
> 2. 自行決定要新增的檔案或資料夾
> 3. 使用 git add 將檔案加進數據庫的 staging area, 讓 git 可以追蹤那些檔案 
> 4. git commit -m "<填寫版本資訊>" 提交檔案並附上更新備註(版本資訊 EX:哪裡改了什麼) 
> *有更新過的檔案要完成提交才可以push到github.com上遠端共享的數據庫*
---
### 本地數據庫 注意事項 !
1. *新增的檔案要執行 add, git才會追蹤到*
2. *add之後,要執行 commit 指令git才會將更新追蹤那些新的的版本
    如果沒有使用commit的話，git追蹤的版本會是舊的版本，而且會不允許上傳到遠端*
---

# 本地連結遠端數據庫 
// 前置作業 : 建立好本地數據庫之後進入本地數據庫的當下資料夾
  
### git remote add origin <github網址> 
> 利用 add 指令連結github.com上面建立好的repository 
>
> origin 是在你的 terminal 或 cmd 裡面，遠端資料庫的名字。
  
### git clone <github網址> 
> clone 會直接將github.com上面已有的內容和資料夾內所有內容全部複製到本地
> 
> 簡單來說就是複製了一整個數據庫進去指定位置，git的追蹤紀錄也會一起 
> 
> *如果用git clone 就不需要提前 git init 一個數據庫*

### git pull <遠端數據庫簡稱> <指定在遠端數據庫的branch>
> pull 會將遠端庫branch的內容都拉近本地的數據庫 // git pull --all 拉取全部分支
> 要注意的一點是 必須先在本建立一個main branch 才能pull 
> 當本地庫沒有main branch 時，要先完成一次commit(建立檔案，add，commit)他才會init main branch。
> 
> 注意 : *如果不是使用 clone 使用 remote 時, pull 並不會合併只會將資料追蹤紀錄拉進來，因為本地和遠端並沒有建立關聯*
>        
>        *要解決這個問題 要使用 git merge origin/main --allow-unrelated-histories 將無關聯的數據庫合併* 







#### ref : [https://ithelp.ithome.com.tw/articles/10214385] 
#### ref : [https://git-scm.com/book/zh-tw/v2/%E9%96%8B%E5%A7%8B-%E9%97%9C%E6%96%BC%E7%89%88%E6%9C%AC%E6%8E%A7%E5%88%B6]
#### ref : [https://www.twblogs.net/a/5c65af43bd9eee06ef3796bb]

