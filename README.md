# 📚 Book Recommendation System

Welcome to the **Book Recommendation System**! This project is a web-based application designed to help users discover new books tailored to their tastes. It utilizes two distinct types of recommendation engines to provide both widely popular suggestions and highly personalized recommendations.

---

## 🚀 Features & Architecture

The application is split into two main pages, each leveraging a different recommendation strategy:

### 1. Home Page (Popularity-Based Filtering)
* **What it does:** Displays the most popular books across the entire platform.
* **How it works:** It aggregates all user ratings and reviews to calculate a global popularity score, ensuring that new visitors are greeted with universally acclaimed titles right away.

### 2. Recommend Page (Collaborative Filtering)
* **What it does:** Delivers personalized book recommendations based on user behavior and preferences.
* **How it works:** This is the core engine of the project. It maps books into a multi-dimensional coordinate space where each user represents a distinct axis/dimension (scaled from 0 to 5 based on ratings). 
    * Each book becomes a distinct data point in this high-dimensional space.
    * By calculating the distance between these points, the system identifies clusters of similar books.
    * When you search for a book, the engine recommends the items that are geographically **closest (nearest neighbors)** to it in that space.

---

## 🧠 Core Concepts: Types of Recommender Systems

To understand where this project fits, here is a quick breakdown of standard recommendation systems:

| Recommender Type | How it Works | Used in this Project? |
| :--- | :--- | :--- |
| **Popularity-Based** | Recommends items that are universally liked or most frequently interacted with by all users. | **Yes** (Home Page) |
| **Content-Based** | Recommends items similar to what a user liked before, based on item attributes. | No |
| **Collaborative Filtering** | Finds patterns and clusters based on how multiple users rate multiple items, treating users/items as data points in a multi-dimensional space. | **Yes** (Recommend Page) |
| **Hybrid** | Combines two or more of the above approaches to build a more robust system. | No |

---

## 🛠️ Tech Stack

* **Frontend:** HTML, CSS, Bootstrap
* **Backend:** Python, Flask
* **Machine Learning / Data Processing:** Pandas, NumPy, Scikit-Learn
