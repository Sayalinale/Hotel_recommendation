# **Hotel Recommendation System** 🏨✨  

This repository contains a **content-based hotel recommendation system** that suggests hotels based on their features, including room amenities, property type, location, and descriptions. The system utilizes **TF-IDF vectorization** and **cosine similarity** to find similar hotels efficiently.  


✅ Loads and cleans hotel data from CSV files.  
✅ Uses **TF-IDF Vectorization** to process hotel features.  
✅ Implements a **Nearest Neighbors Model** for fast recommendations.  
✅ Suggests similar hotels based on amenities, room type, and location.  
✅ Optimized for large datasets without memory issues.  

---

## **📂 Repository Structure**
```
📁 Hotel-Recommendation-System/
│── 📄 README.md               # Project documentation
│── 📄 hotel_recommendation.ipynb  # Jupyter Notebook with full code
│── 📄 requirements.txt        # Required Python libraries
│── 📂 data/                   # Folder containing hotel data (CSV files)
│── 📄 hotel_details.csv        # Hotel details dataset
│── 📄 hotel_room_attributes.csv  # Room attributes dataset
│── 📄 hotel_price.csv          # Hotel price dataset
│── 📄 hotels_room_price.csv    # Room price dataset
```


## **📊 Dataset**
The system processes hotel data from multiple CSV files, including:  
✔ `hotel_details.csv` - Basic hotel information (name, location, type).  
✔ `hotel_room_attributes.csv` - Room types and amenities.  
✔ `hotel_price.csv` - Minimum and maximum price range.  
✔ `hotels_room_price.csv` - Individual room pricing.  

---

## **🧠 How It Works**
1️⃣ **Load Data**: Reads hotel information from CSV files.  
2️⃣ **Clean & Preprocess**: Removes duplicates, handles missing values, and extracts meaningful features.  
3️⃣ **Feature Engineering**: Combines room amenities, property types, and locations into a **single text-based feature** (`tags`).  
4️⃣ **TF-IDF Vectorization**: Converts text-based features into **numerical vectors** for comparison.  
5️⃣ **Nearest Neighbors Model**: Finds the **top 5 most similar hotels** based on cosine similarity.  
6️⃣ **User Query**: Takes a hotel name and returns similar hotels.  

---

## **🔍 Usage**
### **Find Similar Hotels**
Modify the hotel name and run:
```python
hotel_name = "Hotel XYZ"  # Replace with an actual hotel name
recommendations = recommend_hotels(hotel_name, num_recommendations=5)
print(recommendations)
```

### **Example Output**
```
      hotelname     starrating      city      country    similarity_score
1  Hotel Alpha          4       New York       USA            0.87
2  Hotel Beta           3       New York       USA            0.83
3  Hotel Gamma          4       New York       USA            0.81
4  Hotel Delta          5       New York       USA            0.78
5  Hotel Omega          4       Boston         USA            0.76
```


---

## **📝 To-Do List**
✅ Basic recommendation system.  
✅ Handle missing data & duplicates.  
🔄 Add price & user review-based filtering.  
🔄 Implement deep learning-based similarity model.  


