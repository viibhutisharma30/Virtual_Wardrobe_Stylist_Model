👗 Virtual Wardrobe Stylist
A smart AI-powered virtual stylist that recommends outfit combinations tailored to user preferences and body type using Machine Learning and Computer Vision.

🚀 Project Overview
The Virtual Wardrobe Stylist is a personalized fashion recommendation system that helps users choose ideal outfit combinations (e.g., top + bottom) based on:

Item type (shirt, t-shirt, shorts, etc.)

Color

Style (casual, formal, etc.)

Occasion (daily, party, etc.)

Season (summer, winter, etc.)

Body type (automatically detected via webcam)

🧠 Technologies Used
Machine Learning: Random Forest Classifier (scikit-learn)

Computer Vision: Mediapipe for body pose detection

Data Processing: Pandas, LabelEncoder

Model Serialization: Joblib

Webcam Integration: OpenCV

📂 Dataset
The model is trained on a custom fashion dataset (wardrobe_training_large.csv) containing labeled features and target combinations suitable for various body types and occasions.

🔍 Features
💡 Predicts a matching top for a selected bottom or vice versa.

🧍 Detects body type using pose landmarks and classifies (e.g., "athletic", "average").

📸 Uses real-time webcam feed to extract pose features.

✅ Achieves up to 93.55% training accuracy and 75.00% test accuracy for top model predictions.

📌 How It Works
Train models on labeled wardrobe data to recommend outfit combinations.

Use OpenCV and Mediapipe to detect key body landmarks via webcam.

Classify body type based on shoulder width.

Pass inputs (item type, color, etc.) to the model.

Display and recommend the best-matching fashion item.

📈 Model Accuracy

Model	Training Accuracy	Test Accuracy
Top Model	93.55%	75.00%
Bottom Model	89.47%	70.00%
🔧 Setup Instructions
Clone this repository:

bash
Copy
Edit
git clone https://github.com/your-username/virtual-wardrobe-stylist.git
cd virtual-wardrobe-stylist
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Run the model training script:

bash
Copy
Edit
python train_model.py
Start real-time webcam-based prediction:

bash
Copy
Edit
python body_type_and_recommendation.py
📦 File Structure
bash
Copy
Edit
├── train_model.py                 # Trains Random Forest models
├── body_type_and_recommendation.py  # Real-time prediction using webcam
├── wardrobe_training_large.csv   # Dataset
├── top_model.pkl / bottom_model.pkl # Saved ML models
├── le_*.pkl                      # Label encoders
├── README.md                     # Project documentation
📌 Future Enhancements
Add GUI interface for easy user interaction.

Extend dataset to include accessories, footwear, etc.

Integrate with mobile or web platforms.

Improve body type classification with more refined measurements.

🙌 Acknowledgements
Mediapipe

scikit-learn

OpenCV
