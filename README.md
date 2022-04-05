# spike_analyze
### 摘要
Dendritic spine的生長與消亡在神經生物學上被認為相當重要，與學習與記憶形成非常有關。傳統的Dendritic spine標記方法多採用人工標記，現有的自動標記方法也往往只適用於解析度較高之共軛交顯微鏡所拍攝的體外腦切片影像。
利用雙光子顯微鏡所拍攝的活體的腦部影像由於1.環境雜訊多 2.拍攝構造較為深層，進而導致Dendritic spine解析度較低，無法利用傳統的影像分析方法或是現有的軟體來進行自動spine的定位與分類，因此本文提出一套算法進行自動化spine的標記，有效地偵測出大部分spine出現的位置以及大致的分類，可提供之後作為資料集的前處理，來進行如機器學習或深度學習等方式的後續分析。
### 實驗方法
##### 我們所設計的算法分成可分成3個部分，分別是 I. Dendrite and Bouton Extraction、II. Spine Extraction及III. Spine Analysis <br>
I. Dendrite and Bouton Extraction，會依序進行Normalization、Multi-Ostu、Fill Holes及Separate Dendrite & Bouton。 <br>
<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161751906-0a30fe6d-6202-4f3c-924a-e58913c9b747.png" width="400">
    <br>
<p/> 
II. Spine Extraction，會依序進行Get Original Dendrite、Hessian Enhancement & Tophat、Erosion、Multi-Ostu、Fill Holes、Separate Dendrite & Bouton、Skeletonization、Separate Dendrite Body & Spine及Cross Axon & Branched Dendrite Processing。 <br>
<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161751930-9439663a-6855-41cc-8fc9-68deccc2e09e.png" width="400">
    <br>
<p/> 
III. Spine Analysis，會依序進行Spine Positioning and Classification及Mark Result。 <br>
<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161751954-3c1c88d2-0516-412b-999b-522fd77f2eee.png" width="400">
    <br>
<p/> 


### 實驗結果
<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161752272-e047c80e-8db1-46be-9179-ffcd08f320b3.png" width="400">
    <br>
<p/>
<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161752387-f1ec2972-f8c7-4673-a93a-7b9c6d1fa9af.png" width="400">
    <br>
<p/>
<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161752513-0be0b44e-252f-4d71-a081-38dc42afc87f.png" width="600">
    <br>
<p/>
<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161752482-5e511106-4faf-431e-abe5-4f99243a4c90.png" width="400">
    <br>
<p/>

#### 此算法的標記precision及recall，True spine共有123個，其中被偵測出的有114個，錯誤偵測的spine共65個，每一組實驗沒有被偵測到的spine id 稱為FN id

<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161752716-a78d8f6e-a05d-456e-b440-3361c0689827.png" width="600"> <br>
<p/>
