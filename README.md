**Flask** is a lightweight, yet powerful web framework written in Python. It is designed to be easy to use and extend, making it a popular choice for web developers who want to build web applications quickly and efficiently. Flask provides the basic tools needed to get a web app running but gives developers the flexibility to add only the tools they need as their project grows.

Flask is ideal for small to medium-sized applications and provides useful features like routing, request handling, and template rendering. Its simplicity and modularity allow developers complete control over their applications while providing enough functionality to support complex web services.

This tutorial will teach you how to set up a Flask environment and run a basic Flask application.

### **Step 1: Create Folder**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727180290210/01aa47f4-f5f4-4496-a250-1e4d9add7c65.png)

### **Step 2: Type CMD in the search bar:**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727180350119/9db59d59-7591-43fa-9aa7-5d130830da8b.png)

### **Step 3: Check Python Version**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727180379090/b75c924c-69d3-4b69-8fcf-df0a4c34b31f.png)

Make sure to check your folder directory to ensure you are in your project folder. So in my case, I’m in the C:\\Users\\gayar\\OneDrive\\Desktop\\python-list-flask

### **Step 4: Check Pip Version**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727180579321/b8438dcf-15e4-4ea6-afd6-4126f55e12b3.png)

### **Step 5: Create a Virtual Environment**

A **virtual environment** in Python is a self-contained directory that contains a specific version of Python along with a set of installed packages. It helps developers manage dependencies for different projects, ensuring that the libraries and Python versions used in one project do not interfere with others.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727180739817/0e7abd56-c40b-4e42-9497-2488e6e5de2f.png)

The command `python -m venv venv` creates a new virtual environment in a folder named "venv" inside your project directory. This environment will have its own Python interpreter and libraries.

**Verify the venv folder to your project folder**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727180759832/1efa5e52-bd15-4c4f-b642-32f23b421bb9.png)

### **Step 6: Activate Virtual Environment**

```typescript
venv\Scripts\activate
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727181466345/b4f11905-f4f5-48c2-b7ff-476424046bed.png)

Once activated, the terminal prompt changes to show the name of the environment (in this case, `(venv)`), indicating that you are now working within the virtual environment.

### **Step 7: Install Flask**

```typescript
pip install Flask
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727181830133/8caef551-a806-493d-8633-e4960c1e9e3a.png)

### **Step 8: add venv on gitignore**

Adding the `venv` directory to `.gitignore` is essential to prevent the virtual environment files from being tracked by version control tools like Git. Since the `venv` directory contains environment-specific files that are not necessary for the application’s source code, it is a good practice to exclude it from version control to keep the repository clean and reduce clutter.

**Steps to add** `venv` **to** `.gitignore`**:**

```typescript
nul > .gitignore
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727181980101/b0fe819a-980d-4f09-9bd0-ca285ceb5148.png)

Open the `.gitignore` file with a text editor.

1. Add the following line:

```typescript
venv/
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727182043557/e1ec395c-61e3-4c29-a649-c1c0c480da66.png)

2. Save the file.


By adding `venv/` to the `.gitignore` file, you ensure that the virtual environment folder is not included in the repository, keeping your Git history clean and only containing necessary code and dependencies.

---

### **Step 9: Open your Project in Pycharm**

I recommend using **PyCharm** as your IDE (Integrated Development Environment) for Python projects. PyCharm is a powerful tool developed by JetBrains, designed specifically for Python development

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727182505735/09edaa0c-5ff7-4ced-95f3-1b6bb0110e94.png)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727182536645/c0725dbc-56ce-4394-a759-45bc203bf3b6.png)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727182562869/4be1e9d0-ac58-4d41-82b6-d1d62e79d955.png)

---

### **Step 10: Create app.py**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727194876862/b77c73a1-2aab-4ff5-860e-a66badb1e3df.png)

---

### Step 11: Create Directory `“templates”`

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727194914548/bac47856-607b-412a-bef3-8508e3158cc9.png)

---

### Step 12: add `index.html` in the templates folder

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727195083030/59e1bc79-fdd8-4681-ac5f-c119846c8b72.png)

---

### Step 13: In your [`app.py`](http://app.py), import `Flask` and `render_template`

```typescript
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def hello_world():
return render_template('index.html', message="Hello, World!")

if __name__ == '__main__':
app.run(debug=True)
```

### Step 14: In your `index.html` file, use the passed variable:

```typescript
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Hello Page</title>
</head>
<body>
<h1>{{ message }}</h1>
</body>
</html>
```

In this example, the string `"Hello, World!"` is passed as a variable (`message`) from the Python script to the HTML template. The template renders the variable inside the HTML content.

### Step 14: Run app.py in cmd

```typescript
python app.py
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727195470905/a04a669a-8091-4e0d-b3e3-11257828d1ce.png)

make sure the venv is activated

---

**Access the Web Application**:

* Open your browser and go to [`http://127.0.0.1:5000/`](http://127.0.0.1:5000/) to view your running application.


![](https://cdn.hashnode.com/res/hashnode/image/upload/v1727195557345/ec95735c-35c0-44cd-bb91-e4b33268a3c6.png)

### Github Repository

[thirdygayares/python-flask-getting-started (github.com)](https://github.com/thirdygayares/python-flask-getting-started)
