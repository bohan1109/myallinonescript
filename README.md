# all in one script
## windows系統
需先安裝chocolatey
用系統管理員身分開啟powershell，並下以下命令
```
$ Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
安裝完成後下以下命令查看是否安裝成功
```
$ choco -v
```
安裝成功後就可以將install.bat以系統管理員身分執行，開始安裝檔案

## linux-ubuntu系統
需在終端機下更新命令
```
$ apt-get update
```
安裝homebrew事前準備
```
$ sudo apt-get install build-essential curl file git
```
安裝homebrew
```
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/Linuxbrew/install/master/install.sh)" 
```
設定環境變數
```
export PATH="/home/linuxbrew/.linuxbrew/bin:$PATH"
```
下以下命令看是否安裝完成
```
$ brew -v
```
安裝完成後到linux資料夾下命令執行install.sh
```
$ bash install.sh
```