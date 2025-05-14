# Spectral Similarity Measures
- Spectral Angle Mapper (SAM)
- Spectral Information Divergence (SID)
- Constrained Energy Minimization (CEM)

這些方法廣泛應用於高光譜影像分析、目標偵測與分類。

---

## 📐 Spectral Angle Mapper (SAM)

SAM 用來計算兩個光譜向量之間的夾角，量測其相似性。角度越小，表示越相似。

<!-- SAM 公式圖片 -->
<img src="sam_formula_dark.png#gh-dark-mode-only" alt="SAM公式 (深色)" />
<img src="sam_formula_light.png#gh-light-mode-only" alt="SAM公式 (淺色)" />

**符號說明：**

- θ：SAM 計算出的角度（以弧度表示）
- t：目標光譜向量（Target spectrum vector）
- r：參考或背景光譜向量（Reference spectrum vector）
- t_i, r_i：在第 i 個波段上的光譜值
- n：光譜維度（波段數）

---

## 📊 Spectral Information Divergence (SID)

SID 是基於 Kullback-Leibler 散度的非對稱度量，考慮光譜向量的機率分佈，適合處理類別之間的差異性。

<!-- SID 公式圖片 -->
<img src="sid_formula_dark.png#gh-dark-mode-only" alt="SID公式 (深色)" />
<img src="sid_formula_light.png#gh-light-mode-only" alt="SID公式 (淺色)" />

**符號說明：**

- \( SID(t, r) \)：目標與背景的光譜資訊散度
- \( t, r \)：目標與背景光譜向量
- \( t_i, r_i \)：在第 \(i\) 個波段上的光譜值，已正規化為機率值
- log：自然對數（以 \( e \) 為底）
- n ：光譜維度（波段數）

---

## ⚡ Constrained Energy Minimization (CEM)

CEM 是一種濾波器設計方法，用來在壓制背景能量的同時強化目標光譜訊號。常用於高光譜目標偵測。

<!-- CEM 公式圖片 -->
<img src="cem_formula_dark.png#gh-dark-mode-only" alt="CEM公式 (深色)" />
<img src="cem_formula_light.png#gh-light-mode-only" alt="CEM公式 (淺色)" />

**符號說明：**

- **w_CEM**：CEM 計算出的濾波器權重向量  
- **R**：背景像素資料的協方差矩陣（Covariance matrix）  
- **R⁻¹**：R 的反矩陣（inverse）  
- **d**：目標光譜向量（Desired target signature）  
- **dᵀ**：d 的轉置  


---

![avatar](./output.png)
