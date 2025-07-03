Netflix Content Analysis – EDA with Pandas

 📌 Project Overview

This project performs Exploratory Data Analysis (EDA) on the **Netflix Titles Dataset** to uncover trends and insights in Netflix's content. The analysis focuses on identifying the distribution of content types, release patterns, country-wise production, and viewer rating trends.

The purpose is to build a strong, hands-on portfolio project using **Python and Pandas** that demonstrates practical data cleaning and analysis skills using **Visual Studio Code (VS Code)**.

---

🧠 Key Insights

* Netflix hosts **more Movies than TV Shows**.
* The majority of content originates from **United States, India, and the United Kingdom**.
* Most content is rated **TV-MA** or **TV-14**, indicating a strong adult/teenage target audience.
* Peak content addition occurred between **2018–2020**.
* Netflix adds the most content on **Fridays**, followed by **Tuesdays**.

---

 🛠 Tools & Technologies Used

* Python
* Pandas
* Visual Studio Code (VS Code)
* Netflix Titles Dataset (from [Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows))

---

⚙️ Project Structure

```
Netflix_EDA_Project/
├── Netflix_EDA.py            # Python script with all code & insights
├── README.md                # Project summary and reflection
├── netflix_titles.csv       # Dataset
└── output_images/           # (Optional) Saved charts or logs
```

---

 ⚠️ Challenges Faced & What I Learned

 ❌ Issue with Date Parsing

Initially, while trying to convert `date_added` to datetime format, I accidentally overwrote the original column with integer values (days), which broke further `.dt` operations. This caused errors like:

```
AttributeError: Can only use .dt accessor with datetimelike values
```

✅ **Fix:** Reloaded the dataset and used `pd.to_datetime()` properly before extracting features.

---

❌ Missing Values

Columns like `director`, `cast`, and `country` had many null values.
✅ **Fix:** Replaced with `'Unknown'` where appropriate, and dropped where necessary (like `date_added`).

---

❌ Overwriting Columns by Mistake

At one point, the `date_added` column was overwritten during feature engineering (assigning `.dt.day`), which again caused cascading issues.
✅ **Fix:** Created new columns (`year_added`, `month_added`, etc.) instead of overwriting `date_added`.

---

 📁 How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/A-iftikhar02/Netflix_EDA_Project.git
```

2. Navigate into the project folder:

```bash
cd Netflix_EDA_Project
```

3. Open `Netflix_EDA.py` in Visual Studio Code and run it line by line.

---

 🚀 Final Thoughts

This project helped me:

* Practice real-world EDA skills
* Learn from mistakes and debugging
* Strengthen my project portfolio for data analyst roles

> 📌 This project is a part of my skill-building journey in data science. More coming soon!

