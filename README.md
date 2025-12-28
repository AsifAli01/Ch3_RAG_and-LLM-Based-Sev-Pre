Code for LLM-based Severity Prediction of Bug Report (RAG-GPT-SBR) with all Machine Learning (LR, RF, AdaBoost) and Deep Learning (BERT, CNN, RNN, LSTM, NN) baselines, including preprocessing, under-sampling, and over-sampling. All experiments are executed using Google Colab. The baselines appraoches are same as BERT-SBR but we also included some recent baslines approaches from litrature as well. 
1. Open Google Colab and enable GPU: Runtime → Change runtime type → Hardware accelerator → GPU.
2. #Install all required libraries by running the following commands in Colab: !pip install numpy pandas scipy tqdm !pip install scikit-learn !pip install torch torchvision torchaudio !pip install transformers datasets tokenizers accelerate sentencepiece !pip install nltk spacy regex !pip install matplotlib seaborn evaluate imbalanced-learn ,
3. Download NLP resources import nltk, nltk.download('punkt') , nltk.download('stopwords') ,!python -m spacy download en_core_web_sm
4.
5. Download the dataset by running the notebook: https://huggingface.co/datasets/sealuzh/app_reviews
6.
7. After downloading, perform text cleaning and preprocessing (tokenization, normalization, label encoding). The preprocessed dataset is saved automatically during execution inside the notebooks.
8.
9. Handle class imbalance using oversampling by running: Oversampling_on_50000_swn.ipynb Run Machine Learning baseline models using TF-IDF features by executing: Machine_Learning_on_50000_(Preprocessed+embeddings).ipynb
10.
11. Run Deep Learning baseline models by executing: (PA)Project_on_50000_swn_402_.ipynb This notebook trains and evaluates: CNN, RNN, LSTM and Feed-Forward Neural Network (NN) Run the RAG fine-tuning experiment by executing. 
12.
13. This notebook includes: BERT tokenization, Fine-tuning on bug report text, GPU-accelerated training, Final severity prediction results Ensure reproducibility by: Running all notebooks in the same order, Using Google Colab with GPU enabled, Not skipping any preprocessing cells and Using the default hyperparameters provided
