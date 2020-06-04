# Todo

- [x] 提供数据集百度云链接
- [x] 数据集转换为统一格式(检测和识别)
    - [x] icdar2015
    - [x] MLT2019
    - [x] COCO-Text_v2
    - [x] ReCTS
    - [x] SROIE
    - [x] ArT	
    - [x] LSVT
    - [x] Synth800k
    - [x] icdar2017rctw
    - [x] MTWI 2018
    - [x] 百度中文场景文字识别
    - [x] mjsynth
    - [x] Synthetic Chinese String Dataset(360万中文数据集)
    - [ ] CTW
    - [ ] SVHN
    - [ ] 百度中文场景文字识别技术创新大赛
    - [ ] Total-Text
    - [ ] Google FSNS
    - [ ] Synthetic Data for Text Localisation
    - [ ] IIIT 5K-Words 2012
    - [ ] KAIST Scene_Text Database 2010
    - [ ] 阿语和英语混合的PPT中的文本
    - [ ] NEOCR
- [x] 提供读取脚本

# 下载

[百度云](https://pan.baidu.com/s/1mRepVEvMa-U4e9ThiskVXg) 提取码：9s4x 
# 数据集

| 数据集                                             | 链接                                                         | 适用情况  | 数据情况                                                     | 标注形式                                                     | 说明                                                         |
| -------------------------------------------------- | ------------------------------------------------------------ | --------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| ICDAR2015                                          | [官网](https://rrc.cvc.uab.es/?ch=4)                         | 检测&识别 | 语言: 英文     train:1,000     test:500                      | x1, y1, x2, y2, x3, y3, x4, y4, transcription                | 坐标: x1, y1, x2, y2, x3, y3, x4,  y4     transcription : 框内的文字信息 |
| MLT2019                                            | [官网](https://rrc.cvc.uab.es/?ch=15)                        | 检测&识别 | 语言: 混合     train:10,000     test:10,000                  | x1,y1,x2,y2,x3,y3,x4,y4,script,transcription                 | 坐标: x1, y1, x2, y2, x3, y3, x4,  y4     script: 文字所属语言     transcription : 框内的文字信息 |
| COCO-Text_v2                                       | [github](https://bgshih.github.io/cocotext/)                 | 检测&识别 | 语言: 混合     train:43,686     validation:10,000     test:10,000 | json                                                         |                                                              |
| ReCTS                                              | [官网](https://rrc.cvc.uab.es/?ch=12&com=introduction)       | 检测&识别 | 语言: 混合     train:20,000     test:5,000                   | {       “chars”: [         {“points”:  [x1,y1,x2,y2,x3,y3,x4,y4], “transcription” : “trans1”, "ignore":0  },         {“points”:  [x1,y1,x2,y2,x3,y3,x4,y4], “transcription” : “trans2”, " ignore ":0  }],       “lines”: [         {“points”:  [x1,y1,x2,y2,x3,y3,x4,y4] , “transcription” : “trans3”, "ignore ":0  }],     } | points: x1,y1,x2,y2,x3,y3,x4,y4       chars: 字符级别的标注     lines: 行级别的标注.      transcription : 框内的文字信息     ignore: 0:不忽略，1:忽略 |
| SROIE                                              | [官网](https://rrc.cvc.uab.es/?ch=13)                        | 检测&识别 | 语言: 英文     train:699     test:400                        | x1, y1, x2, y2, x3, y3, x4, y4, transcription                | 坐标: x1, y1, x2, y2, x3, y3, x4,  y4     transcription : 框内的文字信息 |
| ArT(已包含Total-Text和SCUT-CTW1500)                | [官网](https://rrc.cvc.uab.es/?ch=14)                        | 检测&识别 | 语言: 混合     train: 5,603     test: 4,563                  | {     “gt_1”: [  {“points”: [[x1, y1], [x2, y2], …, [xn,  yn]], “transcription” : “trans1”, “language” : “Latin”,  "illegibility": false },             {“points”: [[x1, y1],  [x2, y2], …, [xn, yn]], “transcription” : “trans2”, “language” : “Chinese”,  "illegibility": false }],     } | points:  x1,y1,x2,y2,x3,y3,x4,y4…xn,yn      transcription : 框内的文字信息     language: 语言信息     illegibility: 是否模糊 |
| LSVT                                               | [官网](https://rrc.cvc.uab.es/?ch=16)                        | 检测&识别 | 语言: 混合     全标注     train: 30,000     test: 20,000     只标注文本     400,000 | {     “gt_1”: [  {“points”: [[x1, y1], [x2, y2], …, [xn,  yn]], “transcription” : “trans1”, "illegibility": false },             {“points”: [[x1, y1],  [x2, y2], …, [xn, yn]], “transcription” : “trans2”, "illegibility":  false }],     } | points:  x1,y1,x2,y2,x3,y3,x4,y4…xn,yn      transcription : 框内的文字信息     illegibility: 是否模糊 |
| Synth800k                                          | [官网](http://www.robots.ox.ac.uk/~vgg/data/scenetext/)      | 检测&识别 | 语言: 英文     800,000                                       | imnames:      wordBB:      charBB:      txt:                 | imnames: 文件名称     wordBB: 2*4*n,每张图像内的文本框     charBB: 2*4*n,每张图像内的字符框     txt: 每张图形内的字符串 |
| icdar2017rctw                                      | [博客](https://blog.csdn.net/wl1710582732/article/details/89761818)<br />[官网](https://rrc.cvc.uab.es/) | 检测&识别 | 语言: 混合     train:8,034     test:4,229                    | x1,y1,x2,y2,x3,y3,x4,y4,<识别难易程度>,transcription         | 坐标: x1, y1, x2, y2, x3, y3, x4,  y4     transcription : 框内的文字信息 |
| MTWI 2018                                          | [识别](https://tianchi.aliyun.com/competition/entrance/231684/introduction)      <br />[检测](https://tianchi.aliyun.com/competition/entrance/231684/introduction) | 检测&识别 | 语言: 混合     train:10,000     test:10,000                  | x1, y1, x2, y2, x3, y3, x4, y4, transcription                | 坐标: x1, y1, x2, y2, x3, y3, x4,  y4     transcription : 框内的文字信息 |
| 百度中文场景文字识别                               | [比赛页面](https://aistudio.baidu.com/aistudio/competition/detail/20) | 识别      | 语言: 混合     train:未统计     test:未统计                  | h,w,name,value                                               | h: 图片高度     w: 图片宽度     name: 图片名     value: 图片上文字 |
| mjsynth                                            | [官网](http://www.robots.ox.ac.uk/~vgg/data/text/)           | 识别      | 语言: 英文     9,000,000                                     | -                                                            | -                                                            |
| Synthetic Chinese String  Dataset(360万中文数据集) |                                                              | 识别      | 语言: 混合     300k                                          | -                                                            | -                                                            |
| Chinese Text in the Wild(CTW)                      | [介绍页面](https://ctwdataset.github.io/)<br />[微云下载链接](https://share.weiyun.com/50hF1Cc) | 检测&识别 |                                                              |                                                              |                                                              |
| SVHN                                               | [官网](http://ufldl.stanford.edu/housenumbers/)              | 识别      |                                                              |                                                              |                                                              |
| 百度中文场景文字识别技术创新大赛                   | [比赛页面](https://aistudio.baidu.com/aistudio/competition/detail/8) | 检测&识别 |                                                              |                                                              |                                                              |
| Total-Text                                         | [下载链接](http://www.cs-chan.com/source/ICDAR2017/totaltext.zip) | 检测&识别 |                                                              |                                                              |                                                              |
| Google FSNS(谷歌街景文本数据集)                    | [下载页面](http://rrc.cvc.uab.es/?ch=6&com=downloads)        | 识别      |                                                              |                                                              |                                                              |
| Synthetic Data for Text Localisation               | [官网](http://www.robots.ox.ac.uk/~vgg/data/scenetext/)      | 检测&识别 |                                                              |                                                              |                                                              |
| IIIT 5K-Words 2012                                 | [官网](http://cvit.iiit.ac.in/projects/SceneTextUnderstanding/IIIT5K.html) | 识别      |                                                              |                                                              |                                                              |
| KAIST Scene_Text Database 2010                     | [官网](http://www.iapr-tc11.org/mediawiki/index.php/KAIST_Scene_Text_Database) | 检测&识别 |                                                              |                                                              |                                                              |
| 阿语和英语混合的PPT中的文本                        | [gitlab](https://gitlab.com/rex-yue-wu/ISI-PPT-Dataset)      | 检测&识别 |                                                              |                                                              |                                                              |
| NEOCR                                              | [官网](http://www.iapr-tc11.org/mediawiki/index.php/NEOCR:_Natural_Environment_OCR_Dataset) | 检测&识别 |                                                              |                                                              |                                                              |

# 数据生成工具

https://github.com/TianzhongSong/awesome-SynthText 

 # 数据集读取脚本
- [检测读取脚本](dataset/det.py)
- [识别读取脚本](dataset/rec.py)