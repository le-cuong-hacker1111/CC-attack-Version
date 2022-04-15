  _      ______ _____ _    _  ____  _   _  _____ _______   _      _             _____  _____              _   _             _    
| |    |  ____/ ____| |  | |/ __ \| \ | |/ ____|__   __| (_)    | |           |  __ \|  __ \            | | | |           | |   
| |    | |__ | |    | |  | | |  | |  \| | |  __   | |_ __ _  ___| | _____ _ __| |  | | |  | |______ __ _| |_| |_ __ _  ___| | __
| |    |  __|| |    | |  | | |  | | . ` | | |_ |  | | '__| |/ __| |/ / _ \ '__| |  | | |  | |______/ _` | __| __/ _` |/ __| |/ /
| |____| |___| |____| |__| | |__| | |\  | |__| |  | | |  | | (__|   <  __/ |  | |__| | |__| |     | (_| | |_| || (_| | (__|   < 
|______|______\_____|\____/ \____/|_| \_|\_____|  |_|_|  |_|\___|_|\_\___|_|  |_____/|_____/       \__,_|\__|\__\__,_|\___|_|\_\
Tool by Le Cuong Piano
DD-attack  
A script for using socks4/5 or http proxies to attack http(s) server.

News:

 Added Support of HTTP proxies
 Added More proxies api to download
Info:

 Using Python3
 Added more human-like options
 Http Get/Head/Post/Slow Flood
 Random Http Header/Data
 Socks4/5 Proxies Downloader
 Socks4/5 Proxies Checker
 Customize Cookies
 Customize Post Data
 Support HTTPS
 Support Socks4/5
Showcase
Using multiproc.sh with socks4 on a vps 

Install
pip3 install requests pysocks
git clone https://github.com/le-cuong-hacker1111/DD-attack
cd DD-attack
Usage
python3 DD-attck.py <arguments>
===============  CC-attack help list  ===============
   -h/giúp đỡ   | hiển thị tin nhắn này
   -url         | đặt url mục tiêu
   -m/cách thức | đặt chế độ chương trình
   -data        | đặt đường dẫn dữ liệu bài đăng (chỉ hoạt động ở chế độ bài đăng)
                | (Ví dụ: -data data.json)
   -cookies     | đặt cookie (Ví dụ: 'id: xxx; ua: xxx')
   -v           | đặt loại proxy (4/5 / http, mặc định: 5)
   -t           | đặt số chủ đề (mặc định: 800)
   -f           | đặt tệp proxy (mặc định: proxy.txt)
   -b           | bật / tắt chế độ vũ phu
                | Bật = 1 Tắt = 0 (mặc định: 0)
   -s           | đặt thời gian tấn công (mặc định: 60)
   -down        | tải xuống proxy
   -check       | kiểm tra proxy
=====================================================
Usage of multiproc.sh
This script is using for increasing the performance of DD-attack.py.
Due to the suck performance of python since it has a GIL lock,
And I am lazy to make a multiprocess version.
There is a option for linux user to increase their performance of cc.py

This script basicly just run DD-attack.py multiple times to make it "multi-processing"

First, put this script and DD-attack.py in the same folder.

Then prepare the proxies list by yourself or just run "python3 DD-attack.py -down -v 4" (-v socks version)

After that, change the number of process.

At last, change atk_cmd to your command and run the script by "bash multiproc.sh"
Example setup of multiproc.sh (-v socks version) (-s attack time)

atk_cmd="python3 cc.py -url http://target.com -v 4 -s 60"

#number of process that you want
process=10

© 2022 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
