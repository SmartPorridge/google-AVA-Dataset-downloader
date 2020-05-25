**Download Google AVA Dataset**

——————————————————————————————————————

**分享链接被百度屏蔽了，说是侵权或色情，，，，需要点对点分享，有需要下载的可以添加我微信“smartporridge”，备注ava数据下载，点对点发链接吧。

！！！更新百度云下载链接：链接: https://pan.baidu.com/s/1iUDhSMv9flaQo2ryjRmx7w 提取码: 4zxc

**另外欢迎关注公众号“arXiv每日学术速递”，获取每日CV、NLP、AI等方向的学术信息哦,扫码关注

![image](https://github.com/SmartPorridge/google-AVA-Dataset-downloader/blob/master/%E5%85%AC%E4%BC%97%E5%8F%B7%E6%AF%8F%E6%97%A5%E5%86%85%E5%AE%B9.jpg)
![image](https://github.com/SmartPorridge/google-AVA-Dataset-downloader/blob/master/%E5%85%AC%E4%BC%97%E5%8F%B7%E4%BA%8C%E7%BB%B4%E7%A0%81.jpg)

_______________________________________

**This repository contains the train and test annotations, all the videos' youtube IDs, action_id and some videos may be inaccessible on Youtube from your location.**

**仓库中有AVA的训练和测试annotations，也有所有视频的Youtube ID， 以及所有类别的labels，以及部分因为版权原因下载不到的视频下载方法。**

The AVA dataset densely annotates 80 atomic visual actions in 57.6k movie clips with actions localized in space and time, resulting in 210k action labels with multiple labels per human occurring frequently. The main differences with existing video datasets are: 

1. the definition of atomic visual actions, which avoids collecting data for each and every complex action; 
2. precise spatio-temporal annotations with possibly multiple annotations for each human; 
3. the use of diverse, realistic video material (movies). 

**More details about the dataset and initial experiments can be found in this** [arXiv paper](https://arxiv.org/abs/1705.08421 "悬停显示"). 
  
The AVA dataset contains 192 videos split into 154 training and 38 test videos. Each video has 15 minutes annotated in 3 second intervals, resulting in 300 annotated segments. These annotations are specified by two CSV files: [ava_train_v1.0.csv](https://research.google.com/ava/download/ava_train_v1.0.csv "悬停显示") and [ava_test_v1.0.csv](https://research.google.com/ava/download/ava_test_v1.0.csv "悬停显示"). 

Each row contains an annotation for one person performing an action in an interval, where that annotation is associated with the middle frame. Different persons and multiple action labels are described in separate rows. 

**The format of a row is the following: video_id, middle_frame_timestamp, person_box, action_id**
1. video_id: YouTube identifier
2. middle_frame_timestamp: in seconds from the start of the YouTube.
3. person_box: top-left (x1, y1) and bottom-right (x2,y2) normalized with respect to frame size, where (0.0, 0.0) corresponds to the top left, and (1.0, 1.0) corresponds to bottom right.
4. action_id: identifier of an action class, see [ava_action_list_v1.0.pbtxt](https://research.google.com/ava/download/ava_action_list_v1.0.pbtxt "悬停显示")

**The Youtube video IDs (train split) is** [ava_ytids_train_v1.0.txt](./ava_ytids_train_v1.0.txt)
**The Youtube video IDs (test split) is** [ava_ytids_test_v1.0.txt](./ava_ytids_test_v1.0.txt)

To download youtube videos, you need [youtube-dl](https://github.com/rg3/youtube-dl/) , for example:
 
     youtube-dl -f best -f mp4 55Ihr6uVIDA -o "video_data/55Ihr6uVIDA.mp4"
     
***Please note that some videos may be inaccessible on Youtube from your location.If you are a researcher interested in the whole dataset, click [here](http://thoth.inrialpes.fr/ava/requestaccess.php "悬停显示") for more information. And then you can download this part of videos after aome operations.***

        -FaXLcSFjUI.mp4	2017-07-17 14:50	365M	 
	0f39OWEqJ24.mp4	2017-07-17 14:36	437M	 
	2XeFK-DTSZk.mkv	2017-08-08 03:12	270M	 
	4trIFq61-lk.mkv	2017-07-24 03:13	454M	 
	EQZWzLyx-GM.mkv	2017-09-07 03:22	242M	 
	F_-zE1dQsso.mkv	2017-08-02 03:24	225M	 
	G3nRbyu0gMs.mp4	2017-07-17 14:51	218M	 
	K--hW14uzA0.mkv	2017-09-12 03:29	877M	 
	KHHgQ_Pe4cI.mkv	2017-08-08 03:29	845M	 
	N0Dt9i9IUNg.mkv	2017-07-17 15:00	426M	 
	PmElx9ZVByw.mp4	2017-07-17 15:04	431M	 
	XIx-C22Ewk4.mp4	2017-08-09 03:47	788M	 
	ZFQ3lF6yq_E.mkv	2017-08-01 03:49	459M	 
	_2Isct32Msg.mkv	2017-08-26 03:11	627M	 
	bnW1PXGt5hw.mp4	2017-07-17 14:46	379M	 
	lSCEt_mCHlM.mkv	2017-07-17 14:59	2.6G	 
	nxL0yqWP3H0.mkv	2017-07-17 15:01	659M	


The dataset is made available by Google Inc. under a [Creative Commons Attribution 4.0 International (CC BY 4.0) license](https://creativecommons.org/licenses/by/4.0/ "悬停显示").

-------华丽丽的分割线----------

谷歌发布了新的数据集 AVA（atomic visual actions），提供扩展视频序列中每个人的多个动作标签。AVA 包括 YouTube 公开视频的 URL，使用包含 80 个原子动作（atomic action）集进行标注（如「走路」、「踢（某物）」、「握手」），所有动作都有时空定位，从而产生 57.6k 视频片段、96k 标注人类动作和 210k 动作标签。

部分视频因为版权原因在国内下载不到，谷歌提供了高速缓存供大家下载，可以先在[here](http://thoth.inrialpes.fr/ava/requestaccess.php "悬停显示")注册成为学术用途，非常简单，不需要账号，同意不作商业用途之后，就可以得到账号和密码，既可以下载这部分视频。
