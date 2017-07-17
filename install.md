## 安裝 python3
### Windows 7/8/10

請到: https://www.python.org/downloads/release/python-362/

移到最下面 選擇 Windows x86-64 executable installer 或者 Windows x86 executable installer 下載。

雙擊下載回來的檔案。

**務必勾選 Add Ptyhon 3.6 to PATH。**

安裝完成後，按下 <kbd> Win + R </kbd> 鍵入 `cmd` 按下 <kbd> Enter </kbd> 會出現俗稱的黑盒子。

在黑盒子內鍵入 pip 如有以下資訊代表成功了。


```
C:\Users\username> pip
Usage:
  pip <command> [options]

Commands:
...下略
```

如果之前已經自己裝過但是無法使用 pip 請解除安裝後照著以上步驟重新安裝。

### Linux Debian

開啟 terminal

```
apt-get install python3 python3-pip
```

權限如果不足記得使用 `sudo -H`

### Mac OS X

開啟 terminal (<kbd> &#8984; command </kbd> + <kbd> space </kbd>，然後輸入 `terminal`，按 <kbd> return </kbd>)

如果你已經安裝 Homebrew 可以跳過此步驟

安裝 Homebrew

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

安裝 Python3

```
brew install python3
```

## 安裝本課程需要使用的套件

如果你使用的作業系統是 Mac OS X 或者 Linux 請使用 pip3

### 首先升級 pip

```
Windows: python -m pip install --upgrade pip
Mac OS X or Linux: pip3 install --upgrade pip
```

### 開始安裝套件： (如使用 Mac OS X 或 Linux 請用 pip3)

```
pip install send2trash
pip install requests
pip install lxml
pip install beautifulsoup4
pip install selenium
pip install openpyxl
pip install PyPDF2
pip install imapclient
pip install twilio
pip install pillow
pip install pyautogui
pip install mss
```

**如果是 Linux / Mac OS X**

- 將 `pip` 改成 `pip3`
- 如果不是 root 用戶，基本上都需要在 `pip3` 前面加 `sudo -H` 指令以提權 (看不懂了話就加ㄅ)

### Troubleshooting
- [pyautogui](http://pyautogui.readthedocs.io/en/latest/) 套件安裝問題
  需要先安裝其他相關套件
  - Linux
    ```shell
    sudo apt-get install scrot python3-tk python3-dev
    pip3 install python3-xlib
    ```
  - Mac OS X
    ```shell
    pip3 install pyobjc pyobjc-core
    ```
  其他 pyautogui 安裝問題可參考 [官網安裝說明](http://pyautogui.readthedocs.io/en/latest/install.html)

- [imapclient](https://github.com/mjs/imapclient) 套件安裝問題
  Linux 下可能會需要先裝 Xlib
  ```shell
  pip3 install python-Xlib
  ```
