# Cosmetic Insights: Navigating Cosmetics Trends and Consumer Insights with Tableau

## Flask Web Application Code

The following code demonstrates how to integrate the **Cosmetics** dataset with a **Flask** web application and embed a **Tableau Public Dashboard**. The application displays summary statistics and provides an interactive interface for exploring cosmetic trends and consumer insights.

# app.py

from flask import Flask, render_template_string
import pandas as pd

app = Flask(__name__)

# Load Cosmetics Dataset
df = pd.read_csv("cosmetics.csv")

# HTML Template
HTML_TEMPLATE = """
<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">

<title>Cosmetic Insights Dashboard</title>

<style>

body{
    font-family: Arial, Helvetica, sans-serif;
    background:#f4f4f4;
    margin:0;
    padding:20px;
}

.container{
    width:95%;
    margin:auto;
    text-align:center;
}

.cards{
    display:flex;
    justify-content:center;
    gap:20px;
    margin:30px 0;
    flex-wrap:wrap;
}

.card{
    background:white;
    width:220px;
    padding:20px;
    border-radius:10px;
    box-shadow:0px 2px 10px rgba(0,0,0,0.2);
}

.card h3{
    color:#333;
}

.card p{
    font-size:28px;
    font-weight:bold;
    color:#0077cc;
}

iframe{
    width:100%;
    height:850px;
    border:none;
}

</style>

</head>

<body>

<div class="container">

<h1>Cosmetic Insights</h1>

<h2>Navigating Cosmetics Trends and Consumer Insights with Tableau</h2>

<div class="cards">

<div class="card">
<h3>Total Products</h3>
<p>{{ total_products }}</p>
</div>

<div class="card">
<h3>Total Brands</h3>
<p>{{ total_brands }}</p>
</div>

<div class="card">
<h3>Average Price</h3>
<p>${{ average_price }}</p>
</div>

<div class="card">
<h3>Average Rank</h3>
<p>{{ average_rank }}</p>
</div>

</div>

<hr>

<h2>Interactive Tableau Dashboard</h2>

<!-- Replace the URL below with your Tableau Public dashboard link -->

<iframe
src="https://public.tableau.com/views/YOUR_DASHBOARD_NAME?:showVizHome=no">
</iframe>

</div>

</body>

</html>
"""

@app.route("/")
def home():

    total_products = len(df)

    total_brands = df["Brand"].nunique()

    average_price = round(df["Price"].mean(),2)

    average_rank = round(df["Rank"].mean(),2)

    return render_template_string(

        HTML_TEMPLATE,

        total_products=total_products,

        total_brands=total_brands,

        average_price=average_price,

        average_rank=average_rank

    )

if __name__ == "__main__":
    app.run(debug=True)
```

---

## Install Required Packages

```bash
pip install flask pandas
```

---

## Run the Application

```bash
python app.py
```

---

## Open the Browser

```
http://127.0.0.1:5000/
```

---

## Features

- Loads the **Cosmetics** dataset using **Pandas**.
- Calculates:
  - Total Products
  - Total Brands
  - Average Price
  - Average Product Rank
- Displays KPI cards on the homepage.
- Embeds a **Tableau Public Dashboard** inside the Flask application.
- Provides an interactive web interface for exploring cosmetic trends and consumer insights.

> **Note:** Replace the iframe URL:
>
> ```
> https://public.tableau.com/views/YOUR_DASHBOARD_NAME?:showVizHome=no
