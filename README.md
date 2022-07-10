# spike_analyze
### Abstract
In neurobiology, the development and demise of dendritic spines are correlated with memory formation. Traditionally, the researcher labeled the dendritic spines manually, and the existing automatic labeling methods are only appropriate for images captured with high resolution. The brain image of the living brain captured by the two-photon microscope can not be automatically analyzed perfectly due to 1. environmental noises and 2. low resolution in a relatively deep area of the brain. As a result, this article aims to propose a set of algorithms for automatic spine marking, which can effectively detect the location and approximate classification of most spines.
### Method
##### The article has 3 parts, I. Dendrite and Bouton Extraction, II. Spine Extraction及III. Spine Analysis <br>
I. Dendrite and Bouton Extraction，apply Normalization、Multi-Ostu、Fill Holes及Separate Dendrite & Bouton。 <br>
<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161751906-0a30fe6d-6202-4f3c-924a-e58913c9b747.png" width="400">
    <br>
<p/> 
II. Spine Extraction，apply Original Dendrite、Hessian Enhancement & Tophat、Erosion、Multi-Ostu、Fill Holes、Separate Dendrite & Bouton、Skeletonization、Separate Dendrite Body & Spine及Cross Axon & Branched Dendrite Processing。 <br>
<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161751930-9439663a-6855-41cc-8fc9-68deccc2e09e.png" width="400">
    <br>
<p/> 
III. Spine Analysis，apply Spine Positioning, Classification, and Mark Result。 <br>
<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161751954-3c1c88d2-0516-412b-999b-522fd77f2eee.png" width="400">
    <br>
<p/> 


### Result
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

#### 

<p align="center">
    <img src="https://user-images.githubusercontent.com/29053630/161752716-a78d8f6e-a05d-456e-b440-3361c0689827.png" width="600"> <br>
<p/>
