# EHT-dataset

此英文手写文本数据集是为研究手写文本修改(通常由于文本互换与字符删除.替换.插入而产生的重叠)而收集,由九名成年自愿者书写.文本内容来自随机从互联网上搜索的英文名言.新闻报告.书籍内容等,每名成年人被要求在特定的空白框里书写十页文本.每页纸为标准的A4纸,被分割为20行,预设的印刷体文本内容与空白框间隔依次排列,自愿者根据文本内容,在相应的下面空白框进行书写.同时书写者被要求随机产生文本互换与文本重叠.

(1)原始篇章级文本经过扫描后保存在/original_images目录,每名写字人所写文本单独建立目录保存,编号依次为:1,2...9,其中第4号写字人因某种原因只有9页文本被保留.目录里除了提供原始的文本图片*.jpg,还有对应的手写文本行框标注文件*.json.
<div align=center>
<img src=https://github.com/Wukong90/EHT-dataset/blob/main/original_images/page_sample.png>
</div>


(2)目录/train与/test为我们在论文“Leveraging Structure Knowledge and Deep Models for the Detection of Abnormal Handwritten Text”(已被 第七届中国模式识别与计算机视觉大会 录取)中使用到的训练集与测试集文本行,训练集与测试集来自不同的写字人,即同一写字人的样本不可能同时出现的训练集与测试集.在论文中,我们滤掉了原始样本中书写字符明显超出规定框中的样例.

&emsp;训练集目录包含总的训练样本列表total_list.txt与文本行图片及标注目录/train/imags.在论文中,作者随机从全部训练样本提取其70%做为训练(train_list.txt与train.json);提取剩余的30%做为验证(val_list.txt与val.json)./train/character_box为对应的字符框标注目录.

<div align=center>
<img src=https://github.com/Wukong90/EHT-dataset/blob/main/train/sample_sw.png height=60>
  
<img src=https://github.com/Wukong90/EHT-dataset/blob/main/train/sample_ov.png height=60>

<img src=https://github.com/Wukong90/EHT-dataset/blob/main/train/sample_char.png height=60>
</div>

&emsp;类似的,测试集目录包含有测试样本列表/test/test_list.txt及标注文件/test/test.json,文本行图像与标注位于/test/imgs.测试集未提供相应的字符框标注.
