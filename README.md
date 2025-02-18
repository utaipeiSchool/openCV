# 車牌辨識專案

## 專案描述

這個專案的目的是使用 OpenCV 和 EasyOCR 來辨識車牌號碼。專案會讀取 `test` 資料夾中的圖片，辨識車牌號碼，並將結果儲存到 `testAns` 資料夾中。

## 專案架構

├── test/                 # 存放待辨識的圖片  
├── testAns/              # 存放辨識結果  
├── haar_carplate.xml     # Haar 特徵分類器檔案  
└── 車牌辨識Final.ipynb   # 主程式碼  

## 使用方法

### 1. 本機下載與資料上傳
1. **複製儲存庫：** git clone 
2. **上傳資料到雲端：** 將 `test`、 `haar_carplate.xml` 和 `車牌辨識Final.ipynb` 資料夾上傳到您的 Google 雲端硬碟。

### 2. 在 Google Colab 執行
1. **執行程式碼：** 開啟 `車牌辨識Final.ipynb` 並執行程式碼。

## 程式碼功能說明

### 1. 圖像預處理
* 使用 OpenCV 讀取圖片並轉換為灰階。
* 使用 Haar 特徵分類器偵測車牌區域。
* 將車牌區域裁剪出來並調整大小。
* 使用二值化處理車牌圖像，以便於後續的文字辨識。

### 2. 文字辨識
* 使用 EasyOCR 辨識車牌號碼。
* 對辨識結果進行後處理，例如去除雜訊和格式化。

### 3. 結果儲存
* 將辨識出的車牌號碼儲存到 `testAns` 資料夾中，並以車牌號碼作為檔名。
