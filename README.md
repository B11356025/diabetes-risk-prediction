# diabetes-risk-prediction
糖尿病風險預測與類別不平衡處理比較（期中專題）

資料集來源

OpenML「diabetes」（version 1，Pima Indians Diabetes），共 768 筆、8 項臨床特徵。 https://www.openml.org/d/37

檔案說明

diabetes_risk_prediction.ipynb：期中版（E1–E3）。

diabetes_risk_prediction_v2.ipynb：依評語補做的合併版（E1–E6，含 10 種子、重複交叉驗證、超參數搜尋、SHAP）。

outputs/v2/：強化實驗的輸出（對應表 4-4 至 4-6、圖 4-2、4-3）。

執行方式

用 Colab 開啟 diabetes_risk_prediction.ipynb Open In Colab
選擇「執行階段 → 全部執行」，依序執行即可（不需要 GPU）

主要結果摘要

Random Forest 並未穩定優於 Logistic Regression，三個模型的 AUC-ROC 介於 0.789 至 0.813。
加入類別權重後，三個模型的陽性 Recall 皆提升（例如 Logistic Regression 由 0.500 升至 0.704），Precision 持平或下降。
被 Random Forest 漏判的患者，平均血糖明顯較低（117.8，對比正確辨識者的 157.8）。
