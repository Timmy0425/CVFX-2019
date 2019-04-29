# Homework 4 report - Team3
1. A sequence of moving-forward images in NTHU campus.
在資電館一樓走廊拍的照片，光線和角度都有些微的差距。
但是取景可能需要有連續的感覺，例如最後一張需要拍到一點牆壁，和第一張有點接口，才不會導致後面連接圖片有斷層感。

| 1 | 2 | 3 | 4 | 5 | 6 | 7 |
| -------- | -------- | -------- | -------- | -------- | -------- | -------- | 
|   ![](https://i.imgur.com/GK0Xt8N.jpg)|  ![](https://i.imgur.com/GhqqJHi.jpg)|   ![](https://i.imgur.com/AqoHTS1.jpg)| ![](https://i.imgur.com/5EMlMnZ.jpg) | ![](https://i.imgur.com/QdqfJ10.jpg) |![](https://i.imgur.com/gr4j90e.jpg)|![](https://i.imgur.com/h3U6fx3.jpg)

2. Feature extraction and matching results between two images
這是經過 feature extraction 後，取出 matching score 最高的幾個，相連接的結果。
雖然線有點細，看不太清楚，但仔細看還是能看出兩張圖片的 feature 都有 match 到，每個 matching 花的時間也不會太久。
![](https://i.imgur.com/yb34ggS.jpg)
![](https://i.imgur.com/yhRKvq4.jpg)
![](https://i.imgur.com/jpcD0VT.jpg)
![](https://i.imgur.com/9rxYCuY.jpg)
![](https://i.imgur.com/fjWYEl4.jpg)
![](https://i.imgur.com/XnYw3Nf.jpg)


3. Perform image alignment and generate infinite zooming effect
因為gif的檔案太大無法上傳，所以放上google drive連結：
[Link](https://drive.google.com/open?id=1o_INA0NdejyJtAP4yYQHJMGyWYo_Wi2B)
每張圖片的連接感並沒有很好，邊邊的黑框也沒有處理掉，所以導致整體看起來是斷斷續續的，沒有 infinite zooming的感覺，但還是可以看到大致上是有 align 好，如果做 stitching 結果應該會更好看。


4. implement different feature extrators, e.g. SIFT, SURF, and compare the results

FLANN匹配(https://www.jianshu.com/p/42b61d42e0bc):
![](https://i.imgur.com/6Ze9LmD.png)
匹配的特徵比ORB還多，更加的精確 
是三個方法中唯一有匹配到右邊的牆壁的門的


SIFT匹配
由於方法被註冊過專利了，要使用3.4.3之前的opencv-python
(https://blog.csdn.net/dcrmg/article/details/78817988):
![](https://i.imgur.com/3Nb44ZA.png)
跑起來比ORB還慢很多(ORB約比SIFT快100倍)
三個方法中唯一對右邊的椅子部分完全沒取點的
