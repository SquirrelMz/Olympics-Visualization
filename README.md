# Olympics-Visualization
Course Project of Data Analysis and Visualization

# 文件说明

代码的文件结构如下：

```
.
|--- 文本可视化部分    # 文本部分可视化代码
	|--- data   # 所用数据
		|--- ...
	|--- spider # 爬虫代码
		|--- ...
		
	|--- chinesestopword.txt
	
	|--- ceremony.ipynb
	|--- winterOlympic.ipynb

|--- Ma.xlsx
|--- Olimpic.csv
|--- pingpong.xlsx

|--- vis_code.ipynb  # 数据部分可视化代码
```



------

# 环境

python版本为3.9

数据和文本类型的可视化相对独立，单独说明

## 1. 数据可视化（除文本）部分

```
matplotlib                3.3.4
pyecharts                 1.9.1
seaborn                   0.11.2
IPython                   7.29.0
numpy                     1.20.3
pandas                    1.3.4
scipy                  	  1.7.1
```

## 2. 文本可视化部分

* 爬虫代码，在`spider`文件夹中，针对`getText_wb.ipynb`、`getText_bb.ipynb`和`getText_ceremony.ipynb`文件，这部分在可视化时不需要运行，仅为获取文本数据所用，所需的第三方包：

```py
selenium                  4.1.0
beautifulsoup4            4.10.0
```

* 文本可视化代码，针对`winterOlympic.ipynb`和`ceremony.ipynb`文件：

```py
matplotlib                3.4.3 
seaborn                   0.11.2
jieba                     0.42.1
pyecharts                 1.9.1
gensim                    3.8.3
snownlp                   0.12.3
```

------

# 数据集

1. 第一部分主要为以下三个文件：

* `Olympic.csv`：将原本从kaggle下载的两个数据集进行合并与中英文翻译后得到，包括在各届奥运会的名称、年份、季节、开设城市等信息，以及各运动员的姓名、性别、国家、年龄、身高等一系列数据

* `Ma.xlsx`和`pingpong.xlsx`：用于可视化中“中国优势项目与选手——以男子乒乓球单打为例”部分。前者为中国男子乒乓球选手马龙的比赛数据，后者包括了中国男子乒乓球队多年来各选手的比赛数据

2. 第二部分（文本）所用数据：

   在`文本可视化部分/data`文件夹中查看

* `text_data_bb.csv`是通过爬虫在bilibili视频网站的“冬奥会”关键字搜索结果中获取，包括搜索结果中每个视频的发表日期、标题、播放量和点赞数，可以通过运行`getText_bb.ipynb`获取
* `text_data_wb.csv`是通过爬虫在微博的北京冬奥会超话上获取，包括超话下每个帖子的内容、发表日期和发表时间，可以通过运行`getText_wb.ipynb`获取
* `bj_ceremony.csv`和`dj_ceremony.csv`和`text_data_bb.csv`相同，通过爬虫在bilibili视频网站搜索结果中获取，关键字分别为“北京奥运会开幕式”和“东京奥运会开幕式”



