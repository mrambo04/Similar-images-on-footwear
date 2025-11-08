# 👟 Footwear Image Similarity Detection using Deep Learning & Computer Vision

## 📘 Overview  
This project implements an image similarity pipeline to find visually similar footwear images. It uses deep learning feature extraction + similarity metrics to rank similar shoes based on design, color, style and pattern.

## 🎯 Objective  
To develop a system capable of:  
- Extracting meaningful visual features from footwear images  
- Comparing these features to identify the most visually similar footwear items  
- Enabling applications such as: “Find shoes that look like this”, fashion-search, e-commerce visual search, style recommendation

## 🧰 Tools & Technologies  
- Python  
- TensorFlow / Keras (CNN feature extractor)  
- OpenCV & PIL (image processing)  
- NumPy  
- Scikit-Learn (cosine similarity, nearest neighbours)  
- Jupyter Notebook  
- (Optional) Faiss or Annoy for fast similarity search

## 🧮 Approach  
1. Data collection & image preprocessing: load images, resize, normalize, perform augmentations if needed  
2. Feature extraction: use pre-trained CNN (e.g., ResNet50, MobileNet) to extract embeddings from the image dataset  
3. Embedding storage & indexing: build a feature database for all images  
4. Similarity calculation: for a query image compute distances (cosine/Euclidean) between its embedding and database embeddings  
5. Ranking & retrieval: return top-k similar images and display results  
6. Evaluation & visualization: show example query + retrieved images, measure retrieval precision (if ground truth available)  

## 📈 Key Results  
- Achieved **Precision**  
- Example: Query image “Red Runner Sneaker” returned 5 visually similar shoes (same silhouette & color family)  
- Demonstrated business value: faster visual search for e-commerce, improved user engagement by showing “Look-alikes”

## 📂 Dataset  
 (custom image collection)  

## 🚀 Usage  
```bash
# Clone repository
git clone https://github.com/mrambo04/Similar-Images-on-Footwear.git
cd Similar-Images-on-Footwear

# (Optional) Create a virtual environment and install dependencies
pip install -r requirements.txt

# Run feature extraction notebook or script
jupyter notebook Footwear_Similarity.ipynb

# To try inference: place a query image in /query/, run query script to get top-k similar shoes
python query_similar.py --image query/shoe1.jpg --top 5
