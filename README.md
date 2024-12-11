# GPT News Classification

📰 A news article classification model using the pre-trained OpenAI GPT model with the AG_News dataset. This project explores modifications to address training issues and enhance model performance.

## 💡 Project Overview
This project demonstrates:
- Using GPT for multi-class classification of news articles.
- Adjustments to token representation and loss functions tailored to GPT's architecture.
- Modifications to improve training stability and performance.

## 🔧 Key Skills and Tools
- Pre-trained Language Models (OpenAI GPT)
- Gradient Clipping for Stability
- Learning Rate Scheduling (ReduceLROnPlateau)
- Multi-class Classification with CrossEntropyLoss

## 🚀 How to Use
1. Clone the repository:
```bash
   git clone https://github.com/Choi0619/GPT-News-Classification.git
   ```
2. Install required libraries:
```bash
   pip install torch transformers datasets matplotlib
   ```
3. Open the Jupyter Notebook:
```bash
   jupyter notebook GPT_News_Classification.ipynb
   ```

## 🔄 Modifications
During training, an issue was observed where both train and test accuracies dropped to ~25%, indicating abnormal behavior. The following changes were implemented to resolve this:
- Reduced the learning rate to 0.00001.
- Applied Gradient Clipping to prevent gradient explosion.
- Introduced a learning rate scheduler to reduce the learning rate when performance improvement stalls.

## 📊 Results
After the modifications:
- **Initial Test Accuracy:** ~25%
- **Final Test Accuracy:** ~93%

The adjustments stabilized training and significantly improved model performance.

## 👤 Author
[Gyuhwan Choi](https://github.com/Choi0619)
