# Django CRUD App Lab


## **Django CRUD App Lab – Setup**  

Before starting, follow these steps to **set up your project** correctly.  

---

### **1. Open Your Terminal and Navigate to the Right Folder**  
1. Open your **Terminal (سطر الأوامر)**.  
2. Move to the correct folder:  
   ```bash
   cd ~/code/ga/lessons
   ```  

---

### **2. Create a New GitHub Repository**  
1. Go to **GitHub** and create a new repository called `django-crud-app-lab`.  
2. Clone it into your computer **(download the repository to your machine)**:  
   ```bash
   git clone https://github.com/<your-username>/django-crud-app-lab.git
   ```  
   🚨 **Do not copy the command above as-is!** Replace `<your-username>` with your actual **GitHub username** before running it.  

3. Move into the new project folder:  
   ```bash
   cd django-crud-app-lab
   ```  

---

### **3. Set Up a Virtual Environment and Install Django**  
1. **Create a virtual environment (بيئة افتراضية)** inside your project folder:  
   ```bash
   pipenv install django
   ```  
   This will create two files, `Pipfile` and `Pipfile.lock`, which store your project dependencies.  

2. **Activate the virtual environment**:  
   ```bash
   pipenv shell
   ```  
   🧠 **Tip:** When the virtual environment is activated, you should see the environment name appear before your command prompt in the terminal.  

---

### **4. Name Your Django Project**  
Before starting, choose a **name** for your Django project.  

#### **Naming Guidelines:**  
✅ The name should describe what the project does.  
❌ Do not use names like `django`, `test`, or `djangoproject`, as these are **reserved words** in Python/Django.  
❌ Do not use hyphens (`-`) in names. Instead, use underscores (`_`) or a single lowercase word.  
✅ Python convention prefers all **lowercase names** to avoid issues on different systems.  

#### **Examples of Good Names:**  
- `finchcollector` (for a bird-collecting app)  
- `nationalparks` (for a park-related app)  
- `bloghub` (for a blogging platform)  

---

### **5. Start a New Django Project**  
1. Inside your virtual environment, **start a Django project** with your chosen name:  
   ```bash
   django-admin startproject <mycoolapp> .
   ```  
   Replace `<mycoolapp>` with your chosen **project name**.  

2. **Open the project folder in your code editor**:  
   ```bash
   code .
   ```  

---

### **6. Deactivate the Virtual Environment**  
When you're done working, **exit the virtual environment**:  
```bash
exit
```  

---


## **Django CRUD App Lab**  
### **Build Your Own Full Stack Django Application**  

In this lab, you will **apply what you learned** from the Django CRUD App (Cat_Collector) to build your **own project**.  

Use **Cat_Collector** as a reference to structure your app.  

---

## **1. Set Up Your Django Application**  

### **Create Your Application**  
- Start a **new Django app** inside your project:  
  ```bash
  python3 manage.py startapp my_app
  ```  
- Register the app in `settings.py` under `INSTALLED_APPS`.  

- Start the **local server** to test if everything is working:  
  ```bash
  python3 manage.py runserver
  ```  

---

### **Configure the Database**  
1. **Create a database** for your app:  
   ```bash
   createdb mycoolapp
   ```  
2. Edit `settings.py` to **connect your database**:  
   ```python
   DATABASES = {
      'default': {
          'ENGINE': 'django.db.backends.postgresql',
          'NAME': 'mycoolapp',
      }
   }
   ```  
3. **Apply database changes** (migrations):  
   ```bash
   python3 manage.py makemigrations  
   python3 manage.py migrate  
   ```  

---

### **Set Up URL Routing**  
1. **Create a `urls.py` file** inside your app.  
2. Modify the project's `urls.py` to **link your app’s URLs**:  
   ```python
   from django.urls import path, include  

   urlpatterns = [  
      path('admin/', admin.site.urls),  
      path('', include('my_app.urls')), # Connect app URLs  
   ]
   ```  

---

## **2. Implement Full CRUD for a Model**  
Your app should allow users to **Create, Read, Update, and Delete (CRUD)** records.  
Create **views (شاشات أو صفحات)** for:  
- **Home (الصفحة الرئيسية)** – The main page  
- **Index (قائمة العناصر)** – List all items  
- **Detail (تفاصيل العنصر)** – Show one item  
- **Create (إضافة عنصر جديد)** – Form to add a new item  
- **Update (تعديل عنصر)** – Form to edit an item  
- **Delete (حذف عنصر)** – Remove an item  

---

## **3. Add a Second Model with Relationships**  
- Create a **second model** that connects to the first one (**one-to-many relationship - علاقة واحد إلى متعدد**).  
- Add CRUD functionality for this new model.  

---

## **4. Add User Authentication (نظام تسجيل الدخول)**  
- Use Django’s **built-in authentication system (نظام المصادقة في Django)** for user logins.  
- Enable the Django **Admin Dashboard (لوحة تحكم المشرف)** to manage users.  
- Protect private data: **Only logged-in users (المستخدمون المسجلون فقط)** should access certain pages.  

---

## **5. Level Up (Optional - تحسين التطبيق)**  
- Add a **third model** with a **many-to-many relationship (علاقة متعدد إلى متعدد)**.  
- Implement full CRUD for the third model.  

