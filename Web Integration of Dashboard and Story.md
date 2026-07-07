# Cosmetic Insights: Navigating Cosmetics Trends and Consumer Insights with Tableau

## Web Integration of Dashboard and Story

### Description

This section demonstrates how to integrate **Tableau Dashboards** and **Stories** into a **Flask** web application, enabling users to access interactive cosmetic trends and consumer insights directly through a web browser. By combining Tableau's powerful data visualization capabilities with Flask's lightweight web framework, the application provides an intuitive and responsive interface for exploring cosmetic product performance, brand comparisons, pricing trends, customer preferences, and market insights in real time.

Embedding Tableau dashboards within a Flask application improves accessibility, simplifies sharing, and allows users to interact with visualizations without opening Tableau Desktop. This integration makes the project suitable for business presentations, online portfolios, and decision-support applications.

---

## Flask Application Code

```python
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def home():
    return render_template("index.html")

if __name__ == "__main__":
    app.run(debug=True)
```

---

## Explanation

### 1. Import Required Modules

The Flask application begins by importing the required modules.

- `Flask` is used to create the web application.
- `render_template` is used to render HTML pages stored in the `templates` folder.

---

### 2. Create the Flask Application

```python
app = Flask(__name__)
```

This statement creates an instance of the Flask application.

---

### 3. Define the Home Route

```python
@app.route('/')
def home():
    return render_template("index.html")
```

- The root URL (`/`) is mapped to the `home()` function.
- When users visit the application, Flask renders the **index.html** page.
- The HTML page contains the embedded Tableau Dashboard or Story.

---

### 4. Run the Application

```python
if __name__ == "__main__":
    app.run(debug=True)
```

- Starts the Flask development server.
- `debug=True` enables debugging and automatically reloads the application whenever code changes are made.

---

## Benefits of Web Integration

- Enables users to access Tableau dashboards from any web browser.
- Provides interactive exploration of cosmetic trends and consumer insights.
- Simplifies sharing dashboards with stakeholders through a web application.
- Supports embedding dashboards into websites or business portals.
- Enhances accessibility without requiring Tableau Desktop installation.

---

## Outcome

Integrating Tableau with Flask creates a simple yet powerful web-based analytics platform. Users can interact with cosmetic dashboards and stories in real time, explore visual insights, and make data-driven decisions through an accessible and user-friendly web interface.
