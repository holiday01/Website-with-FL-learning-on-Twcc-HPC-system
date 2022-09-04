# Website-with-FL-learning-on-Twcc-HPC-system
使用視覺化網站，讓擁有iService帳號的使用者，可以進行聯邦式學習，此網站將提供一系列不同的醫學影像數據。使用者必須提供與計畫相關的數據才可加入，而聯邦式學習的目的為互相提供訓練模型，因此，不必擔心個資外。

以下將會說明如何加入此計畫、操作方法和結果取得。

## 網站操作
###### 介面介紹與操作
首次進入網站內，以sing up介面，註冊帳號，帳號不會立即開通，會經由後端確認此帳號為iService才能登入。
![image](https://user-images.githubusercontent.com/20851973/183823828-52fa32f2-6377-422c-b031-5843861b8fad.png)
 
## 註冊畫面 (sing up)
除了username之後，其他填入的資訊都登入台灣衫機器相同。
![image](https://user-images.githubusercontent.com/20851973/183824012-78902603-452c-44e9-bd11-52ffac53adf7.png)

OTP可以從iService的網站取得，或者google Authenticator取得。在註冊後，會有系統發訊息通知註冊成功或重新操作。

## 登入 (login)
當網站註冊信取得後，就可以登入網站內，並且加入計畫內容。

![image](https://user-images.githubusercontent.com/20851973/183824857-d8a99452-6525-4250-a7a3-89bbcb5c753d.png)

## 計畫加入 (session)
計畫加入只需要點選標號就可以。

![image](https://user-images.githubusercontent.com/20851973/183824960-09c9c47c-e443-4f6e-bb26-3cf3915c0580.png)

## 查詢加入計畫與時間 (joined)
<img width="1053" alt="image" src="https://user-images.githubusercontent.com/20851973/188294037-2c7e1c05-01dd-48fb-8416-01fb5cffeae6.png">
  
###### 加入訓練伺服器
在計畫加入截止後，系統會發送檔案給各位使用者，並且說明使用方法，請依照使用方法將 1.`數據`放到設定位置。設定為`~/data`中，影像數據放入子檔案夾`images`，標記寫入`~/data/label.csv`中。

## label.csv 格式

    `col1, col2 = ~/data/images/image1.jpg, dog`

## 啟動伺服器

麻煩以終端機 (terminal) 啟動與連線伺服器。指令如下
`poc/site-?/startup/start.sh`


使用台灣衫機器可以由兩個管道
1. 由網站自動產生，須提供secret key
2. 自行加入者，請聯絡 2203048@narlabs.org.tw

###### 結果取得
結果會有一組local model與global model，local model是由個人數據所訓練取得，global model是整合不同團隊模型的參數。

## 使用者上傳訓練log檔案，取得learning curve圖
在upload的頁面，使用者需要輸入 "Title" (自行自訂數據名稱)，上傳後，會前往learning curve網頁取得
<img width="791" alt="image" src="https://user-images.githubusercontent.com/20851973/188294085-eb4883b3-438b-46bc-a178-fedb294d45e5.png">

## 使用者取得learning curve圖
在file name的地方，輸入上傳的名稱，按下search就可以到自己的學習曲線

<img width="828" alt="image" src="https://user-images.githubusercontent.com/20851973/188294126-d08c436b-5c4e-4087-a439-3ddbe8bd7c76.png">

## 離開計畫
在計畫執行之前，使用者如果提前選擇不加入計畫，可以由此介面刪除
<img width="802" alt="image" src="https://user-images.githubusercontent.com/20851973/188294208-9882e518-bd4e-4014-ae04-cca0507e58a3.png">

  
