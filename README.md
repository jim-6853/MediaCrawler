创建并激活 python 虚拟环境
# 进入项目根目录
cd MediaCrawler

# 创建虚拟环境
python -m venv venv

# macos & linux 激活虚拟环境
source venv/bin/activate

# windows 激活虚拟环境
venv\Scripts\activate
安装依赖库
pip3 install -r requirements.txt
安装 playwright浏览器驱动
playwright install
运行爬虫程序
# 默认没有开启评论爬取模式，有需要请到配置文件中指定
# 从配置文件中读取关键词搜索相关的帖子并爬去帖子信息与评论
python main.py --platform xhs --lt qrcode --type search

# 从配置文件中读取指定的帖子ID列表获取指定帖子的信息与评论信息
python main.py --platform xhs --lt qrcode --type detail

# 打开对应APP扫二维码登录
  
数据保存
支持保存到关系型数据库（Mysql、PgSQL等）
支持保存到csv中（data/目录下）
支持保存到json中（data/目录下）
