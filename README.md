# Fine-Tuning-BERT-for-Text-Classification

Training a BERT-based model to classify sentences into one of 6 categories using PyTorch and Hugging Face Transformers.

---

## ✅ Steps Completed:

### 📁 Data Preparation
- Loaded and cleaned dataset.
- Tokenized the input sentences using `BertTokenizer`.
- Converted text into `input_ids` and `attention_masks`.
- Encoded labels and split the data into training and validation sets.

### 🔄 Tensor Conversion
- Converted `input_ids`, `attention_masks`, and `labels` to PyTorch tensors.
- Created `TensorDataset` and `DataLoader` objects for batching.

### 🧠 Model Setup
- Loaded `BertForSequenceClassification` with `num_labels=6`.
- Set up the `AdamW` optimizer (with weight decay).
- Added a learning rate scheduler using `get_linear_schedule_with_warmup`.

### 🏋️ Training Loop
Repeated for multiple epochs:
- For each batch:
  - Performed a forward pass
  - Calculated loss
  - Did backward pass
  - Clipped gradients
  - Updated weights
  - Adjusted learning rate
- Tracked and printed training loss and learning rate.

### 📊 Evaluation Phase
- Switched model to `eval` mode.
- Initialized variables to track evaluation accuracy and MCC (if used).
- Prepared to run validation loop without updating weights.

---

## 📦 Final Output:
A fine-tuned BERT model capable of classifying new sentences into one of 6 categories with learned weights and training history (loss, learning rate, etc.).
