# Website-with-FL-learning-on-Twcc-HPC-system
使用視覺化網站，讓擁有iService帳號的使用者，可以進行聯邦式學習，此網站將提供一系列不同的醫學影像數據。使用者必須提供與計畫相關的數據才可加入，而聯邦式學習的目的為互相提供訓練模型，因此，不必擔心個資外。

以下將會說明如何加入此計畫、操作方法和結果取得。

## 網站操作
###### 介面介紹與操作
首次進入網站內，以sing up介面，註冊帳號，帳號不會立即開通，會經由後端確認此帳號為iService才能登入。
![image](https://user-images.githubusercontent.com/20851973/183823828-52fa32f2-6377-422c-b031-5843861b8fad.png)
 
* 註冊畫面 (sing up)
除了username之後，其他填入的資訊都登入台灣衫機器相同。
![image](https://user-images.githubusercontent.com/20851973/183824012-78902603-452c-44e9-bd11-52ffac53adf7.png)

OTP可以從iService的網站取得，或者google Authenticator取得。在註冊後，會有系統發訊息通知註冊成功或重新操作。

* 登入 (login)
當網站註冊信取得後，就可以登入網站內，並且加入計畫內容。

![image](https://user-images.githubusercontent.com/20851973/183824857-d8a99452-6525-4250-a7a3-89bbcb5c753d.png)

* 計畫加入 (session)
計畫加入只需要點選標號就可以。

![image](https://user-images.githubusercontent.com/20851973/183824960-09c9c47c-e443-4f6e-bb26-3cf3915c0580.png)

* 查詢加入計畫與時間 (joined)
  
###### 加入訓練伺服器
在計畫加入截止後，系統會發送檔案給各位使用者，並且說明使用方法，請依照使用方法將 1.`數據`放到設定位置。設定為`~/data`中，影像數據放入子檔案夾`images`，標記寫入`~/data/label.csv`中。

* label.csv 格式

    `col1, col2 = ~/data/images/image1.jpg, dog`

* 啟動伺服器

麻煩以終端機 (terminal) 啟動與連線伺服器。指令如下
`poc/site-?/startup/start.sh`

```
使用台灣衫機器可以由兩個管道
1. 由網站自動產生，須提供secret key
2. 自行加入者，請聯絡 2203048@narlabs.org.tw
```

###### 結果取得
結果會有一組local model與global model，local model是由個人數據所訓練取得，global model是整合不同團隊模型的參數。

