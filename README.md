# 就職可否予測AI
大学生の諸データ（GPA、インターン経験、スキル等）に基づき、その学生が就職可能かどうかを予測する二値分類モデルです。

## 概要
Kaggleの「College Student Placement Factors Dataset」を使用し、PyTorchを用いてニューラルネットワークを構築しました。
学生の学業成績や課外活動が、最終的な就職決定（Placement）にどのように寄与するかをモデル化しています。

## 使用データセット
- **データセット:** [College Student Placement Factors Dataset](https://www.kaggle.com/datasets/sahilislam007/college-student-placement-factors-dataset) (Kaggle)
- **特徴量:** IQ, 前学期の成績, CGPA, 学業成績評価, インターン経験, 課外活動スコア, コミュニケーションスキル, 完了プロジェクト数

## 技術スタック
- **Language:** Python 3.12.12
- **Framework:** PyTorch
- **Libraries:** NumPy, Pandas, Scikit-learn, Matplotlib, Tqdm
- **Tool:** Google Colab / Jupyter Notebook

## モデル構造
シンプルな2層の全結合ニューラルネットワークを採用しています。
- Input Layer: 8 units
- Hidden Layer: 128 units (Activation: Sigmoid)
- Output Layer: 1 unit (Activation: Sigmoid)
- Optimizer: SGD (Learning Rate: 0.1)
- Loss Function: Binary Cross Entropy Loss

## 実行結果
- **Training Accuracy:** ~99.6%
- **Test Loss:** ~0.02007

### 学習曲線
![Train Loss & Accuracy](images/train_result.png)  

## セットアップ
```bash
git clone [https://github.com/koki01150124/placement-prediction-ai.git](https://github.com/koki01150124/placement-prediction-ai.git)
cd placement-prediction-ai
pip install -r requirements.txt
