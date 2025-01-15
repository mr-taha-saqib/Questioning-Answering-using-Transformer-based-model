# MedQuAD (Medical Question Answering Dataset)

The MedQuAD dataset provides a comprehensive source of medical questions and answers for natural language processing. With over **43,000 patient inquiries** from real-life situations categorized into **31 distinct types of questions**, the dataset offers an invaluable opportunity to research correlations between treatments, chronic diseases, medical protocols, and more.

Answers provided in this database come not only from doctors but also other healthcare professionals such as nurses and pharmacists, offering a broader perspective to help researchers unlock deeper insights within the realm of healthcare. This incredible trove of knowledge is just waiting to be mined—so grab your data mining tools and start exploring!

## How to Use the Dataset

1. **Understanding the Columns**
   - `qtype`: The type of medical question.
   - `Question`: The question itself.
   - `Answer`: The expert response.

   Use the `qtype` column to categorize questions based on desired topics. Once filtered, analyze the dataset to answer key questions such as:
   - *"What treatments do most patients search for?"*
   - *"Are there correlations between chronic conditions and protocols?"*

2. **Sample Query**
   Use SQL or similar tools for querying the dataset. For example:
   ```sql
   SELECT Answer FROM MedQuad WHERE qtype = 'Treatment' AND Question LIKE '%pain%';
   ```

3. **Taking Action**
   After gaining insights from the dataset, you can:
   - Develop educational materials.
   - Implement suggested changes for better healthcare delivery.

Additional columns may be periodically added to enhance analysis capabilities.

**Dataset Link**: [Kaggle - Comprehensive Medical Q&A Dataset](https://www.kaggle.com/datasets/thedevastator/comprehensive-medical-q-a-dataset/data)

---

## Task: Question Answering Using Transformer-Based Models

### Models to Implement
1. **BERT**
2. **MobileBERT**
3. **RoBERTa**

Use the guidelines provided at [SimpleTransformers QA Documentation](https://simpletransformers.ai/docs/qa-specifics/) to fine-tune these models.

### Dataset Split
- **Training**: 75%
- **Testing**: 25%

### Experimentation
1. **Hyperparameter Tuning**
   - Experiment with different hyperparameters, such as:
     - Number of Encoder Layers
     - Dropout Rates (e.g., 0.3 and 0.7)
     - Learning Rate
   - Set `n_best_size = 5` and show the top 5 predicted answers alongside the actual answers for select questions.

2. **Visualization**
   - Use `wandb` (Weights and Biases) for recording and visualizing training progress.

3. **Evaluation Metrics**
   - Calculate **BLEU Score** and **ROUGE** for each model.
   - Report the results in a comparative table, including the hyperparameter values used to achieve the best results.

---
