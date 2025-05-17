---
theme:
  override:
    footer:
      style: template
      left: https://osga.dev
      center: <span class="noice">SCINT 基礎食物🍕課程</span> @ OsGa 
      right: "{current_slide} / {total_slides}"
      height: 3
    palette:
      classes:
        noice:
          foreground: blue
---


<!-- alignment: center -->
<!-- jump_to_middle -->
# SCINT 基礎能力食物🍕課程

author OsGa
---

<!-- alignment: center -->


<!-- end_slide -->

\>_ WHOAMI?
===
<!-- column_layout: [1, 1] -->

<!-- column: 1 -->

![pic](me.png)

<!-- pause -->

<!-- column: 0 -->

## OsGa or os24

---
<!--pause-->
* CTF Player | Developer 
-
<!--pause-->
* A student from NYUST
-
<!--pause-->
* btw I use Vim

---
<!--pause-->
> more on https://osga.dev


<!-- end_slide -->

\>_ 今天要做啥?
===

<!-- incremental_lists: true -->
- 已經熟悉 Linux 操作了 ✅
---
- 但有一些小問題 🤏
	- 🌰. 為什麼 git status 要打那麼長？不能改短一點嗎？
	- 🌰. 為什麼連上遠端主機要打一大串 IP + 帳號？
	- 🌰. 還有什麼工具有助於日常使用呢？
	- 
# DEMO 一下我ㄉ日常好ㄌ
<!--pause-->
## 添加一些設定，省去平常糟做得麻煩 👍
<!--pause-->
> ~~如果講太快的話我可能會帶到下禮拜的內容~~
<!--pause-->
> 可能今天東西比較雜，介紹一下小設定 / 工具可以便於你一些日常操作，下周會著重在使用上。

<!--end_slide-->

\>_ Slido
===

<!-- column_layout: [1, 1] -->
<!-- column: 1 -->
![qrcode](qrcode.png)

<!-- column: 0 -->
---
### 有任何問題都歡迎提問！
> CODE: 9025087
---

<!--end_slide-->

\>_ 前情提要
===
<!--pause-->
#### 預先善其事 必先利其器

<!-- incremental_lists: true-->
- 今天操作會用到很多需要編輯設定的部分
- 好的文字編輯器是非常重要的 ✅
---


<!--alignment: center-->
![nanovsvim](images/nanovsvim.png)
<span style='color: blue'>選擇你的派系 🙌</span>
<!-- pause-->
<span style='color: red'>~~反正我們今天要用 VIM~~</span> 

<!--end_slide-->

\>_ 為什麼是 Vim 不是 nano
===
<!-- column_layout: [1,1] -->
<!--column: 1 -->
![vim](images/Vimlogo.png)
<!-- incremental_lists: true -->
<!-- column: 0 -->
- 不需滑鼠，快速移動、複製、選取文字
- 可以搭配 NeoVim 等擴展更多功能
- 生態系完整，較多人使用
- 還有很多你用了就知道

![qian](images/qian.png)
### ~~用 nano 的都是男娘~~


<!--end_slide-->

\>_ Welcome join Vim world 
===

* 今天只會先教大家基本操作
-
<!--pause-->
* 其餘設定下禮拜會在教各位一些更詳細的操作

<!--end_slide-->

\>_ Welcome join Vim world 
===


# how to install VIM?
<!--pause-->

* VIM 基本上已經是 Linux 標配的套件
- 
<!--pause-->
# How to use VIM
<!--pause-->
* 開啟 VIM
```bash
vim 
```
```bash
vi 
```
<!--pause-->
* 編輯檔案
```bash
vim <file>
```
```bash
vi <file>
```
#### 如果檔案不存在，編輯即創建！
<!--pause-->
---
### 為什麼下面一個 vi 也可以使用到 Vim?
<!--end_slide-->

\>_ Welcome join Vim world 
===
### 為什麼下面一個 vi 也可以使用到 Vim?
<!--column_layout: [1,1] -->
<!--column: 1 -->
![vim](images/Vimlogo.png)


<!--column: 0 -->
* Vi 是最早期的 Unix 編輯器之一
- 
* 出現在 1970s，是 POSIX 標準要求的基本工具。
- 
* Vim（Vi IMproved）於 1991 年推出
- 
* 為 Vi 的加強版，支援更多功能（如多層 undo、syntax highlight）。
- 
* Vim 保留向下相容性
- 
* 使用方式與 Vi 幾乎相同，因此可安全替代。
- 
* Linux 發行版為了統一維護與使用體驗
- 
* 多數預設將 vi 設為 Vim 的 symlink（例如 /usr/bin/vi -> /usr/bin/vim）。
- 
* 便於使用者獲得更多功能而不需額外安裝
- 
* 提供 Vi 介面熟悉度的同時，享有 Vim 強大功能。

<!--end_slide-->

\>_ Welcome join Vim world
===

# 📝 Vim 操作入門指南

## 🎛 模式介紹（Modes）
<!--pause-->

| 模式       | 進入方式        | 用途說明                         |
|------------|-----------------|----------------------------------|
| Normal     | 預設開啟即為此模式 | 移動游標、刪除、複製等操作           |
| Insert     | `i`、`a`、`o` 等   | 編輯文字（像一般編輯器一樣）        |
| Visual     | `v`、`V`、`Ctrl+v` | 選取文字區塊進行複製、刪除等操作     |
| Command    | `:`              | 執行指令（如儲存、離開）            |

---

## 🔁 模式切換

| 操作             | 效果                     |
|------------------|--------------------------|
| `i`              | 插入游標前               |
| `a`              | 插入游標後               |
| `o`              | 在下方開新行並插入       |
| `Esc`            | 回到 Normal 模式         |
| `v`              | Visual 模式（選字元）     |
| `:`              | Command 模式             |

<!--end_slide-->

\>_ Welcome join Vim world
===

# 📝 Vim 操作入門指南

## 🔍 常用移動指令（Normal 模式）

| 指令   | 功能                           |
|--------|--------------------------------|
| `h`    | 向左移動一格                   |
| `l`    | 向右移動一格                   |
| `j`    | 向下移動一行                   |
| `k`    | 向上移動一行                   |
| `w`    | 移動到下一個單字開頭           |
| `0`    | 移到行首                       |
| `$`    | 移到行尾                       |
| `gg`   | 移到檔案最上方                 |
| `G`    | 移到檔案最下方                 |

---

## ✏️ 編輯與操作（Normal 模式）

| 指令      | 功能                         |
|-----------|------------------------------|
| `x`       | 刪除游標所在字元             |
| `dd`      | 刪除整行                     |
| `yy`      | 複製整行                     |
| `p`       | 貼上（在後）                 |
| `u`       | 復原                         |
| `Ctrl + r`| 反復原                       |
| `.`       | 重複上一個編輯動作           |

## https://vim.rtorr.com/

<!--end_slide-->

\>_ Welcome join Vim world
===

# 📝 Vim 操作入門指南

## 💾 儲存與離開（Command 模式）
<!--column_layout: [1,1]-->
<!--column: 1-->
![quit](images/quit.png)
<!--alignment: center-->
https://github.com/hakluke/how-to-exit-vim

<!--column: 0 -->
<span style='color: #808080'>//怎麼退出RRR</span> 

進入 Command 模式先按 `:`，再輸入以下指令：

| 指令    | 功能                         |
|---------|------------------------------|
| `:w`    | 儲存                         |
| `:q`    | 離開                         |
| `:wq`   | 儲存並離開                   |
| `:q!`   | 不儲存強制離開               |

---
<!--alignment: left-->
<!--pause-->
## 🧪 練習
> 創建一個 `*.py`
>
> 使用 Vim 寫一個簡單的 `print("hello world")`


<!--pause-->

1. 開啟檔案：
```bash
vim test.py 
```
2. 嘗試：
   - 使用 `i` 編輯文字，再輸入
```python
print('hello world')
```
   - 按 `ESC` 回到 Normal Mode ，用 `:wq` 儲存離開

<!--end_slide-->


\>_ Welcome join Vim world
===
<!--column_layout: [1,1]-->
<!--column: 1-->
![good](tl.png)
<!--column: 0-->
# 🪄小魔法讓 Vim 更好用一點 
Verrrrrrrrrrrry Gooooooooooooooood 你現在是一個合格的 Vim users 了

<span style="color: #808080">~~趕緊推坑你身邊的朋友入教~~</span>

<!-- pause-->
但現在的 Vim 看起來還很陽春

<!-- pause-->
## 添加一些小設定讓他更方便！
<!-- pause-->
```bash
/etc/vim/vimrc
```
<!--alignment: center-->
<span style="color: #808080">Vim ㄉ設定檔</span>
<!--alignment: left-->
<!--pause-->
### 進入編輯
```bash
sudo vim /etc/vim/vimrc
```
<!--alignment: center-->
<span style="color: #808080">可以都多善用你ㄉ TAB</span>

<!--alignment: left-->
#### FYI 
* vimrc 是 Vim 啟動時預設會讀取的設定檔之一（屬於全域層級）。
* 作用於 所有使用者，除非被使用者的個人設定（如 ~/.vimrc）覆蓋。
* 由系統管理員（如 root）配置，提供預設行為。
<!--end_slide-->

\>_ Welcome join Vim world
===
# 🪄小魔法讓 Vim 更好用一點 
假設說今天有一個程式
```python
def hello(name):
	print(f"hello {name}")

name = input('input user name: ')
hello(name)
```

<!--alignment: center-->
<span style="color: #808080">test.py</span>

<!--pause-->
```bash {0} 
" All Debian-specific settings are defined in $VIMRUNTIME/debian.vim and
" sourced by the call to :runtime you can find below.  If you wish to change
" any of those settings, you should do it in this file or
" /etc/vim/vimrc.local, since debian.vim will be overwritten everytime an
" upgrade of the vim packages is performed. It is recommended to make changes
" after sourcing debian.vim so your settings take precedence.

runtime! debian.vim

" Uncomment the next line to make Vim more Vi-compatible
" NOTE: debian.vim sets 'nocompatible'.  Setting 'compatible' changes
" numerous options, so any other options should be set AFTER changing
" 'compatible'.
"set compatible
```
<span style="color: #808080">/etc/vim/vimrc 的某一段</span>



<!--end_slide-->
\>_ Welcome join Vim world
===
# 🪄小魔法讓 Vim 更好用一點 
```bash {9} 
" All Debian-specific settings are defined in $VIMRUNTIME/debian.vim and
" sourced by the call to :runtime you can find below.  If you wish to change
" any of those settings, you should do it in this file or
" /etc/vim/vimrc.local, since debian.vim will be overwritten everytime an
" upgrade of the vim packages is performed. It is recommended to make changes
" after sourcing debian.vim so your settings take precedence.

runtime! debian.vim
set ai nu
" Uncomment the next line to make Vim more Vi-compatible
" NOTE: debian.vim sets 'nocompatible'.  Setting 'compatible' changes
" numerous options, so any other options should be set AFTER changing
" 'compatible'.
"set compatible
```
<!--alignment: center-->
<span style="color: #808080">/etc/vim/vimrc 的某一段</span>

加上了 `set ai nu `

<!--pause-->
```python +line_numbers
def hello(name):
	print(f"hello {name}")

name = input('input user name: ')
hello(name)
```
多出酷酷的數字了

可以用 `G` 方便跳到對應行數

<!--end_slide-->

\>_ Welcome join Vim world
===
# 🪄小魔法讓 Vim 更好用一點 

當然還有其他參數
| 指令                        | 說明                                                         |
|-----------------------------|--------------------------------------------------------------|
| `set number`                | 顯示行號                                                     |
| `set relativenumber`        | 顯示相對行號（搭配移動更方便）                              |
| `syntax on`                 | 啟用語法高亮                                                 |
| `set tabstop=4`             | 設定 tab 寬度為 4 空格                                       |
| `set shiftwidth=4`          | 設定縮排寬度為 4 空格（影響 `>>`、`<<`）                    |
| `set softtabstop=4`         | 設定按一次 Tab 鍵產生的空格數量                             |
| `set expandtab`             | 使用空格取代 Tab 字元                                       |
| `set autoindent`            | 啟用自動縮排                                                 |
| `set smartindent`           | 根據語法自動判斷縮排（適合程式碼）                          |
| `set nowrap`                | 關閉自動換行（長行不換行）                                   |
| `set scrolloff=5`           | 游標靠近上下邊界時預留 5 行可視範圍                         |
| `set cursorline`            | 突出顯示目前游標所在行                                       |
| `set incsearch`             | 即時搜尋（輸入時立即高亮）                                 |
| `set ignorecase`            | 搜尋時忽略大小寫                                             |
| `set smartcase`             | 若搜尋中含有大寫則開啟大小寫區分                           |
| `set hlsearch`              | 高亮顯示所有搜尋結果                                         |
| `set clipboard=unnamedplus` | 使用系統剪貼簿（可與外部系統互通）                          |
| `set mouse=a`               | 啟用滑鼠操作（選取、拖曳等）                                |
| `set background=dark`       | 適合深色背景主題（自動調整語法配色）                         |
| `filetype plugin indent on` | 啟用語言檔案偵測、自動縮排與對應插件支援                   |

下禮拜會再帶大家多玩玩！

先知道怎麼編輯寫入退出就好

<!--end_slide-->
\>_ 將一大坨的指令設定快捷
===

* 「我們每天都在打一樣的指令：git status, ls -la, cd ../../..，你會不會覺得煩？」
-
* 你會常用哪些重複的指令？

<!--pause-->
---
# 我們可以在 ~/.bashrc or ~/.zshrc 下設定將指令設定快捷

<!--pause-->
 🌰 .
```bash
ping 8.8.8.8
```
<!--pause-->
可以使用 `alias` 將整串指令自定義成自己的習慣
```bash
alias p8='ping 8.8.8.8'
```
<!--pause-->
#### 要寫在哪呢？

<!--end_slide-->
\>_ 將一大坨的指令設定快捷
===

每個 shell 在家目錄底下都有一個 `*rc`

🌰 .
```
.zshrc .bashrc .fishrc
```


<!--pause-->

## 查看現在使用哪個 SHELL
```bash
echo $SHELL
```

<!--pause-->
```bash	
┌──(osga㉿MacKali)-[~]
└─$ echo $SHELL
/usr/bin/zsh
```
<!--alignment: center-->
✅ zsh


<!--end_slide-->
\>_ 將一大坨的指令設定快捷
===
進入設定檔
```bash
vi ~/.zhsrc
```

<!--pause-->
在空白處加上
```bash
alias p8='ping 8.8.8.8'
```
<!--pause-->
套用 / 生效設定

```bash
source ~/.zshrc
```

<!--pause-->
使用
```bash
┌──(osga㉿MacKali)-[~]
└─$ p8
PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data.
64 bytes from 8.8.8.8: icmp_seq=1 ttl=128 time=12.2 ms
64 bytes from 8.8.8.8: icmp_seq=2 ttl=128 time=8.24 ms
```
<!--pause-->
## 🧪 動手試試時間


<!--end_slide-->
\>_ 將一大坨的指令設定快捷
===
### 如果今天是複雜的指令怎麼辦 🤔

<!--pause-->
* 需要輸入到參數
<!--pause-->
-
* 自己寫一個 command ✅

---

ex. 

# linux
* 一個我之前方便連線到不同機器的工具
<!--pause-->
* ssh 到固定主機 

<!--pause-->
```bash {all|3-4|5-6|7-8|9-10|all}+line_numbers
#!/bin/bash

if [ "${1}" = "rk" ]; then
	ssh osga@10.8.0.5
elif [ "${1}" = "lk" ]; then
	ssh osga@192.168.200.131
elif [ "${1}" = "x86" ]; then
	ssh osga@192.168.64.15
else
	echo "ERROR"
fi
```
<!--pause-->
```bash
╭─    ~                                                                                                                                                                     ✔  09:41:27 下午  
╰─ linux lk
Linux MacKali 6.12.13-arm64 #1 SMP Kali 6.12.13-1kali1 (2025-02-11) aarch64

The programs included with the Kali GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Kali GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Fri May 16 21:20:10 2025 from 192.168.200.1
┌──(osga㉿MacKali)-[~]
└─$
```


<!--end_slide-->
\>_ 將一大坨的指令設定快捷
===
### 如果今天是複雜的指令怎麼辦 🤔

將檔案製作完成後，可以放到

```
/usr/local/bin
```

<!--pause-->
## 🧪 動手試試時間

### 1.
寫一個指令叫做 `hello` 

執行指令會輸出 `hello world`
### 2.

承上題.

`hello` 後面可以接字串

執行指令會輸出 `hello ${string}`


<!--end_slide-->

\>_ 將一大坨的指令設定快捷
===
### 如果今天是複雜的指令怎麼辦 🤔

## 🧪 動手試試時間

### 1.
寫一個指令叫做 `hello` 

執行指令會輸出 `hello world`

---
* 創建一個 shell code 叫做 `hello`
```bash
vi hello
```

* 寫 shell code 
```bash
#!/bin/bash

echo hello world
```
* 儲存退出，並且將檔案移至 `/usr/local/bin/`
```bash
sudo mv hello /usr/local/bin
```
<!-- alignment: center-->
<span style='color: #808080'>可能會有權限問題 建議加上 <span style='color: red'>sudo</span></span>
<!--end_slide-->

\>_ 將一大坨的指令設定快捷
===
### 如果今天是複雜的指令怎麼辦 🤔

## 🧪 動手試試時間

### 2.

承上題.

`hello` 後面可以接字串

執行指令會輸出 `hello ${string}`

---
* 創建一個 shell code 叫做 `hello`
```bash
vi hello
```

* 寫 shell code 
```bash
#!/bin/bash

echo hello ${1}
```
* 儲存退出，並且將檔案移至 `/usr/local/bin/`
```bash
sudo mv hello /usr/local/bin
```
<!-- alignment: center-->
<span style='color: #808080'>可能會有權限問題 建議加上 <span style='color: red'>sudo</span></span>

<!-- alignment: left-->
-
<!--pause-->
#### <span style='color: #808080'>用 shell code 寫ㄉ一個 sideproject https://github.com/osga24/Quick-Jump</span>
 

<!-- end_slide -->

\>_ ssh 免密碼連線
===
當你使用進一台機器時...
<!--pause-->

```bash {1-2|1-3|4-15}+line_numbers 
┌──(osga㉿MacKali)-[~]
└─$ ssh osga@localhost
osga@localhost's password:
Linux MacKali 6.12.13-arm64 #1 SMP Kali 6.12.13-1kali1 (2025-02-11) aarch64

The programs included with the Kali GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Kali GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Fri May 16 22:03:34 2025 from 192.168.200.1

┌──(osga㉿MacKali)-[~]
└─$
```
<!--pause-->

如果這台機器你很常連的話呢...

<!--pause-->
### @@ 每次都要重複輸入密碼
## 使用金鑰自動驗證 ✅

<!-- end_slide -->

\>_ ssh 免密碼連線
===
1. 創建金鑰

```bash
┌──(osga㉿MacKali)-[~]
└─$ ssh-keygen
```
```php {all|1-3|4-5|6-7|8-10|11-13|14-26|all}
enerating public/private ed25519 key pair.
Enter file in which to save the key (/home/osga/.ssh/id_ed25519):
// 產生一對 SSH 金鑰（公鑰 + 私鑰），使用 ed25519 演算法
Enter passphrase for "/home/osga/.ssh/id_ed25519" (empty for no passphrase):
// 選擇儲存檔案（預設 ~/.ssh）
Enter same passphrase again:
// 設定 金鑰的密碼保護，如果你輸入密碼，這把私鑰就只有在提供該密碼後才能使用
Your identification has been saved in /home/osga/.ssh/id_ed25519
Your public key has been saved in /home/osga/.ssh/id_ed25519.pub
// 成功儲存私鑰公鑰
The key fingerprint is:
SHA256:veGoRu00O0qpwChoftXpXFgQC9qlGPA03CllnaF4oJk osga@MacKali
// 這是金鑰的指紋（fingerprint），用來在安全交換時確認是否被竄改過
The key's randomart image is:
+--[ED25519 256]--+
| .o=o+o++        |
|  *oXo=+.        |
| E =.= ..        |
|    .    o       |
|      ..S o      |
|.o   ..=++ o     |
|+.o ..=oooo      |
|+  o o.++        |
| .. ..o. .       |
+----[SHA256]-----+
// 金鑰的 視覺指紋（visual hash），目的是讓你在一堆金鑰中快速「肉眼比對」
```
<!--alignment: center-->
# 這邊先全部按 enter 作為範例


<!-- end_slide -->

\>_ ssh 免密碼連線
===

┌──(osga㉿MacKali)-[~]

└─$ cd .ssh
<!--pause-->
id_ed25519 <span style='color: red'>**id_ed25519.pub**</span> known_hosts known_hosts.old

<!--pause-->
可以將你的 *.pub 丟給別人 

#### 我們先在本機 Try Try

<!-- end_slide -->

\>_ ssh 免密碼連線
===

```bash
sudo vi /etc/ssh/sshd_config
```

```php {0|7}
35. #MaxAuthTries 6
36. #MaxSessions 10
37.
38. #PubkeyAuthentication yes
39.
40. # Expect .ssh/authorized_keys2 to be disregarded by default in future.
41. AuthorizedKeysFile	.ssh/authorized_keys .ssh/osga24.keys
42. #AuthorizedPrincipalsFile none
43.
44. #AuthorizedKeysCommand none
45 .#AuthorizedKeysCommandUser nobody
```


<!-- end_slide -->

\>_ ssh 免密碼連線
===

```bash
sudo vi /etc/ssh/sshd_config
```

```php {7}
35. #MaxAuthTries 6
36. #MaxSessions 10
37.
38. #PubkeyAuthentication yes
39.
40. # Expect .ssh/authorized_keys2 to be disregarded by default in future.
41. AuthorizedKeysFile	.ssh/id_ed25519.pub .ssh/osga24.keys
42. #AuthorizedPrincipalsFile none
43.
44. #AuthorizedKeysCommand none
45 .#AuthorizedKeysCommandUser nobody
```
### 儲存退出 重啟服務

```bash
sudo service ssh restart
```
#### 如果沒有開啟的話就
```bash
sudo service ssh start 
```

<!-- end_slide -->

\>_ ssh 免密碼連線
===

現在重先連線
<!--pause-->
```bash
┌──(osga㉿MacKali)-[~]
└─$ ssh osga@localhost
Linux MacKali 6.12.13-arm64 #1 SMP Kali 6.12.13-1kali1 (2025-02-11) aarch64

The programs included with the Kali GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Kali GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Fri May 16 23:08:32 2025 from 192.168.200.1
┌──(osga㉿MacKali)-[~]
└─$
```
<!--pause-->
---
## 🧪 動手試試時間

和你旁邊的夥伴

互相丟公鑰給對方 ssh

#### <span style='color: #808080'>可以使用 scp 互相丟公鑰給對方</span>
<!-- end_slide -->
\>_ 工具分享
===

## 一些好玩的工具可以進化日常的使用或優化其他指令效果


<!-- incremental_lists: true-->
- cowsay
	- 可以讓一隻牛說話
- nyancat
	- 打了就知道ㄌ
- cmatrix
	- 裝完會變駭客
- Quick-Jump
	- 快速在不同目錄跳躍 ~~安麗一下自己工具~~
- bat
	- <span style='color: red'>**b**</span>atter c<span style='color: red'>**at**</span>
- htop
	- 查看 CPU、RAM、Process 的互動介面，比 top 更清楚
- neofetch
	- 顯示系統資訊
- thefuck
	- 打錯指令自動修正

---

- 下次課程會著重在
	- tmux
	- neovim 
	- yazi 

### 推薦大家自己安裝看看或尋找 / 寫符合自己要求的套件
<!-- end_slide -->

<!-- jump_to_middle -->
<!-- alignment: center-->
<span style='color: #98FB98'>薛薛大家，歡迎一起交流終端環境💻</span>

contact to me <span style='color: #4169E1'>https://osga.dev</span>
