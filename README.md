# BUA451---FinalProject---XixuanChen
Overview:
---------
This project analyzes Bitcoin Cash blockchain data to predict whether a block exceeds 500KB in size using metadata features. A Decision Tree Classifier was trained, achieving 91% test accuracy. The analysis includes exploratory data analysis (EDA), model development, and actionable insights for blockchain operations.

Key Features:
------------
- Data Source: `bigquery-public-data.crypto_bitcoin_cash.blocks` (BigQuery public dataset).
- Target Variable: Binary label indicating block size > 500,000 bytes.
- Features: Block version, block number, and time since the previous block.
- Model: Decision Tree Classifier with 91% accuracy, 0.79 F1-score for large blocks.

Installation & Setup:
---------------------
1. **Environment Setup**:
   - Google Colab or Jupyter Notebook.
   - Install required packages:
     ```
     !pip install pandas-gbq google-cloud-bigquery pandas matplotlib seaborn plotly-express
     ```
   - Authenticate with Google Cloud:
     ```python
     from google.colab import auth
     auth.authenticate_user()
     ```

2. **BigQuery Connection**:
   ```python
   project_id = 'proven-wavelet-457219-u4'  # Replace with your project ID
   client = bigquery.Client(project=project_id)
