# Antminer Monitor

Lite Python based Antminer Monitor !!!

  - Add as many miners as you want
  - Supports miners S7, S9, T9, L3, L3+, D3, A3
  - Check their hashrate, temperatures, fan speed, chip condition, HW Error Rate, Uptime
  - Get in-app notifications about miner errors (needs refresh)
  - Log errors to file
  - Display total hashrate grouped by Model

### Screenshot

![Alt text](/app/static/images/screenshot_v0.3.0.png?raw=true "Screenshot v0.3.0")

### Requirements

  - Antminer Monitor requires Python to run. Both Python2 and Python3 are supported !!!
  - Mac and Linux users have Python installed by default on their system
  - Windows users can download Python from https://www.python.org
`** ATTENTION **` While installing Python be sure to check `Add python.exe to Path` in the step `Customize Python`
If you don't select this option you will probably face some errors while installing the requirements

### Fresh Installation

> All commands must be typed without the leading dollar sign `$`
  1. Download the latest official release of #AntminerMonitor from https://github.com/meyrelles/Antminer-dashboard/releases
  2. Unzip the downloaded file in a folder of your preference
  3. Open a windows command prompt or a terminal and navigate to the folder where you unzipped the file using the `cd` command
e.g. If you unzipped the file in the folder `C:\Users\foo\Downloads\antminer-monitor-master` type the following command and press <Enter>
```sh
$ cd C:\Users\foo\Downloads\Antminer-dashboard
```
  > You command prompt or terminal should now look like  `C:\Users\foo\Downloads\Antminer-dashboard>`
  4. **This step apply only to *Mac* users**. If you are a Windows or Linux user continue to step 5.
  > Mac users should run all the commands with sudo eg. `sudo python get_pip.py`
  
Install `pip` using one of the following methods:
 - Download `get-pip.py` from https://bootstrap.pypa.io/get-pip.py and save it inside `Antminer-dashboard`. Run the following command to install it:
 > It will ask for the administrator password. Type it and press <Enter>. While typing your password you won't see the characters on your screen. This is only for security measures.
```sh
$ sudo python get_pip.py
```
or
 - Install pip using `easy_install`. Again it may ask for the administrator password.
```sh
$ sudo easy_install pip
```
  5. Install requirements (Mac users don't forget `sudo`)
```sh
$ python -m pip install -r requirements.txt
$ python create_db.py
```

### Run the app
 (Mac users don't forget `sudo`)
```sh
$ python run.py
```

Fire up a browser and point it to `http://localhost:5000` if you are running the app on the same machine OR `http://<ip>:5000` if you are accesing the app from another machine on the same network, by replacing `<ip>` with the machine's ip running AntminerMonitor.

### Upgrade

##### BEFORE YOU BEGIN: **You can always do a fresh install to upgrade to a newer version but you will have to add your miners again**
 To upgrade AntminerMonitor to a newer version follow the steps below:
 
 - Do a backup of your database (file: `app/db/app.db`) in case something goes wrong
 - Download the latest version of #AntminerMonitor from https://github.com/meyrelles/Antminer-dashboard/archive/Antminer-dashboard.zip
 - Unzip and replace all the files in your current installation
 - Install requirements in case we added something new:
 ```sh
$ python -m pip install -r requirements.txt
```
 - Update your database. This ensures that your installed version supports the latest miner models and configuration settings, while keeping your added miners in the Database.
```sh
$ python update_db.py
```

### Donations

  - BTC: `15Qsg38n1BaXvFfEA42yK3DVfYYjSFM4nX`
  - LTC: `LRMPWkyNFxD1DUKioLz7wLHu5heVbXDbuV`
  - DASH: `XuWW8y1BL7ZHGCBEw3Vwfa1xAgXTQZoBKu`
  - ETH: `0x3ef8dd78b53ef876c482aa10d139941a76d073b6`
