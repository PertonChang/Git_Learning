#  Git 執行環境的三個層級

設定 Git 執行環境的三個層級 ( 註: 執行 git config --help 可以取得完整指令說明 )

系統層級 (System-level configuration) (設定於整台電腦，所有使用者的預設值)
git config --system --list
預設路徑: C:\Program Files (x86)\Git\etc\gitconfig
或是路徑: %LOCALAPPDATA%\VirtualStore\Program Files (x86)\Git\etc\gitconfig 
補充參考: VirtualStore - Inside Windows Vista User Account Control
使用者層級 (User-level configuration) (設定於目前登入的使用者)
git config --global --list
預設路徑: C:\Users\<使用者帳號>\.gitconfig      (這是個檔案)
常用指令
最常見的設定就是 user 區段下的 name 與 email 參數，第一次用 Git 一定要設定!
git config --global user.name "John Doe"
git config --global user.email "johndoe@example.com"
在 Linux 底下可以指定編輯器
git config --global core.editor vim
在Windows底下，最好打開 core.autocrlf 選項，讓 commit 的檔案沒有 CR 字元 
( 純 Windows 開發環境，可以設定為 false；跨平台協同開發，建議設定為 true )
git config --global core.autocrlf true
自動訂正打錯的參數，例如 git statsu 會自動修正為 git status 讓你不用重打一次
git config --global help.autocorrect 1
儲存區層級 (Repository-level configuration)
git config --list
預設路徑: <Git儲存區>\.git\config
