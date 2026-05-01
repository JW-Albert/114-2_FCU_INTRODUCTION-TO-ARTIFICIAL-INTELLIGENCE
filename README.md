# 114-2 FCU 人工智慧導論

逢甲大學「人工智慧導論」課程（114-2 學期）的講義與 Lab 程式碼。

## 目錄結構

```
.
├── docs/          # 課程投影片（章節講義 + Lab 說明）
└── src/           # Lab Jupyter Notebook 程式碼
```

## 課程進度

| Lab | 主題 | 檔案 |
|-----|------|------|
| Lab 1 | Python 基礎：計算機、九九乘法表 | `lab_1_Q1.ipynb`, `lab_1_Q2.ipynb` |
| Lab 2 | 影像處理：裁切、負片轉換 | `lab_2_Q1.ipynb`, `lab_2_Q2.ipynb`, `lab_2_Q3.ipynb` |
| Lab 3 | 監督式學習：線性回歸 | `lab_3.ipynb` |
| Lab 4 | 非監督式學習：K-Means 分群 | `lab_4.ipynb` |
| Lab 5 | MNIST 資料集探索 | `lab_5-MNIST.ipynb` |
| Lab 6 | MNIST 全連接神經網路 + 混淆矩陣 | `lab_6_MNIST_Q1.ipynb`, `lab_6_MNIST_Q2.ipynb` |
| Lab 7 | MNIST 互動式錯誤分析（ipywidgets） | `lab_7_MNIST.ipynb` |
| Lab 8 | CIFAR-10 卷積神經網路（1D / 2D / 3D） | `lab_8_CIFAR_1D.ipynb`, `lab_8_CIFAR_2D.ipynb`, `lab_8_CIFAR_3D.ipynb` |

## Lab 內容說明

### Lab 1 — Python 基礎
- **Q1**：以 `match-case` 實作四則運算計算機
- **Q2**：巢狀迴圈印出九九乘法表

### Lab 2 — 影像處理
- **Q1**：依比例裁切圖片
- **Q2**：依起始座標裁切圖片
- **Q3**：負片轉換（`255 - pixel`）

### Lab 3 — 線性回歸
使用 scikit-learn `LinearRegression` 對隨機生成的資料進行訓練，並計算預測誤差。

### Lab 4 — K-Means 分群
使用 scikit-learn `KMeans` 對隨機 2D 點群進行分群，透過 matplotlib 視覺化結果。

### Lab 5–7 — MNIST 手寫數字辨識
- 資料集：60,000 張訓練圖、10,000 張測試圖（28×28 灰階）
- 前處理：攤平為 784 維、歸一化（÷255）、One-hot Encoding

| Lab | 架構 | 準確率 |
|-----|------|--------|
| Lab 6 Q1 | Dense(784→256→10) | ~97.6% |
| Lab 6 Q2 | 同上 + 混淆矩陣分析 | ~97.6% |
| Lab 7 | 同上 + ipywidgets 互動視覺化 | ~97.6% |

### Lab 8 — CIFAR-10 影像分類
- 資料集：50,000 張訓練圖、10,000 張測試圖（32×32 RGB，10 類）
- 10 類別：airplane、automobile、bird、cat、deer、dog、frog、horse、ship、truck

| 版本 | 架構 | 參數量 | 準確率 |
|------|------|--------|--------|
| 1D（1 層 Conv） | Conv(32)→Pool→Dense(1024)→Dense(10) | 8,400,778 | ~66% |
| 2D（2 層 Conv） | Conv(32)→Pool→Conv(64)→Pool→Dense(1024)→Dense(10) | 4,224,970 | ~71.8% |
| 3D（3 層 Conv） | Conv(32)→Pool→Conv(64)→Pool→Conv(128)→Pool→Dense(1024)→Dense(10) | 2,201,674 | ~74.3% |

> 加深網路層數在減少參數的同時提升了準確率，展示特徵萃取的重要性。

## 技術環境

- Python 3
- TensorFlow / Keras
- scikit-learn
- NumPy
- Matplotlib
- ipywidgets
- Google Colab（推薦執行環境）

## 執行方式

建議於 [Google Colab](https://colab.research.google.com/) 開啟各 Notebook，無需本地安裝即可執行。

1. 至 Colab 選擇「上傳筆記本」
2. 選取 `src/` 目錄下對應的 `.ipynb` 檔案
3. 依序執行各儲存格

## 授權

MIT License — Copyright 2026 Albert Wang
