# 疫情前後來臺旅客消費行為變遷之分析

專案簡介
本研究利用交通部觀光署「來臺旅客消費及動向調查」資料，分析 2015–2023 年來臺旅客之消費行為，探討 COVID-19 對旅客消費模式之影響，並結合 K-Means 群集分析 與 機器學習模型 建立旅客市場分類及消費預測模型。

一、研究問題
本研究主要探討以下問題：
疫情前後旅客消費行為是否改變？
疫情是否影響旅遊目的結構？
是否能利用 K-Means 建立旅客市場分類？
是否能利用機器學習模型預測旅客每日消費金額？
哪些因素最能影響旅客消費？


二、資料來源
資料來源：
交通部觀光署《來臺旅客消費及動向調查》

資料期間：
2015–2023 年

Merge Key：
年份
來源國／地區


三、資料欄位
目標變數（Target）
每人每日消費（美元）
特徵變數（Features）
平均停留夜數
業務比例
觀光比例
探親比例
會議比例
求學比例
展覽比例
醫療比例


四、分析流程
                                                      
資料蒐集
      │
      ▼
資料前處理
      │
      ▼
資料合併
      │
      ▼
EDA 探索性分析
      │
      ├─────────────┐
      ▼             ▼
K-Means        機器學習模型
      │             │
      ▼             ▼
PCA          Linear Regression
             Decision Tree
      │
      ▼
模型評估
      │
      ▼
研究結果
       

五、使用方法
1. 安裝套件
pip install -r requirements.txt
2. 執行資料前處理
3. 執行群集分析
4. 執行機器學習模型


六、研究結果
Exploratory Data Analysis（EDA）
不同來源國具有不同消費能力。
平均停留夜數與每日消費呈負相關。
COVID-19 改變旅客消費模式。
旅遊目的比例於疫情前後產生變化。
K-Means 群集分析

將旅客市場分為三類：
| Cluster   | 市場類型    |
| --------- | ------- |
| Cluster 0 | 混合型市場   |
| Cluster 1 | 高消費觀光市場 |
| Cluster 2 | 長期停留市場  |

機器學習模型
| 模型                | R²    | RMSE  | MAE   |
| ----------------- | ----- | ----- | ----- |
| Linear Regression | 0.853 | 14.86 | 11.41 |
| Decision Tree     | 0.871 | 13.91 | 11.49 |

得 Decision Tree Regression 具有較佳之預測能力。


七、結果圖
本專案輸出圖表包括：
1. 各來源國平均每日消費金額
2. 停留夜數與每日消費關係圖
3. 疫情前後每日消費比較
4. 疫情前後停留夜數比較
5. 旅遊目的比例分析
6. Correlation Matrix
7. Elbow Method
8. PCA 群集分析
9. Linear Regression 預測結果
10. Decision Tree 預測結果
11. Decision Tree 特徵重要性分析


八、研究限制
1. 樣本數有限（63 筆）
2. 使用國家層級彙整資料，缺乏個人層級資訊
3. 僅比較 Linear Regression 與 Decision Tree 兩種模型
4. 未納入匯率、GDP、航班數等外部因素


九、未來改進方向
1. 擴充更多年度資料
2. 加入更多影響因子（GDP、CPI、匯率、航班數等）
3. 比較 Random Forest、XGBoost、LightGBM 等模型
4. 建立即時旅遊消費預測模型
5. 針對不同來源國建立專屬預測模型


十、參考資料
交通部觀光署（2025）。來臺旅客消費及動向調查。https://admin.taiwan.net.tw/businessinfo/IssuePage?a=14693 
國境事務大隊（2026）。我國近10年出入境人次。https://servicestation.immigration.gov.tw/2275/2281/11505/11508/412756/cp_news
Pedregosa, F., Varoquaux, G., Gramfort, A., Michel, V., Thirion, B., Grisel, O., ... & Duchesnay, É. (2011). Scikit-learn: Machine learning in Python. Journal of Machine Learning Research, 12, 2825–2830. 
Scikit-learn developers. (2025). Scikit-learn documentation. https://scikit-learn.org/stable/
The pandas development team. (2025). pandas documentation. https://pandas.pydata.org/
黃韻勳（2026）。大數據分析與資料探勘課程講義。國立成功大學。（未出版教材）
