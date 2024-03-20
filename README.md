创建并激活 python 虚拟环境
# 进入项目根目录
cd MediaCrawler

# 创建虚拟环境
python -m venv venv

# macos & linux 激活虚拟环境
source venv/bin/activate

# windows 激活虚拟环境
venv\Scripts\activate

pip3 install -r requirements.txt

playwright install

python main.py --platform xhs --lt qrcode --type search


python main.py --platform xhs --lt qrcode --type detail

# 打开对应APP扫二维码登录
  
数据保存
支持保存到关系型数据库（Mysql、PgSQL等）
支持保存到csv中（data/目录下）
支持保存到json中（data/目录下）
