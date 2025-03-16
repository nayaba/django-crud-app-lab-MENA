# Django CRUD App Lab - Exercise

In this lab, you will **apply what you learned** from the Django CRUD App (Cat_Collector) to build your **own project**.  

Use **Cat_Collector** as a reference to structure your app.  



## **1. Set Up Your Django Application**  

### **Create Your Application**  
- Start a **new Django app** inside your project:  
  ```bash
  python3 manage.py startapp my_app
  ```  
- Register the app in `settings.py` under `INSTALLED_APPS`.  

- Start the **local server** to test if everything is working:  
  ```bash
  python3 manage.py runserver 8080
  ```  
- Go to `http://localhost:8080/` to see your app.  



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



## **2. Implement Full CRUD for a Model**  
Your app should allow users to **Create, Read, Update, and Delete (CRUD)** records.  

Create **views (شاشات أو صفحات)** for:  
- **Home (الصفحة الرئيسية)** – The main page  
- **Index (قائمة العناصر)** – List all items  
- **Detail (تفاصيل العنصر)** – Show one item  
- **Create (إضافة عنصر جديد)** – Form to add a new item  
- **Update (تعديل عنصر)** – Form to edit an item  
- **Delete (حذف عنصر)** – Remove an item  



## **3. Add a Second Model with Relationships**  
- Create a **second model** that connects to the first one (**one-to-many relationship - علاقة واحد إلى متعدد**).  
- Add CRUD functionality for this new model.  



## **4. Add User Authentication (نظام تسجيل الدخول)**  
- Use Django’s **built-in authentication system (نظام المصادقة في Django)** for user logins.  
- Enable the Django **Admin Dashboard (لوحة تحكم المشرف)** to manage users.  
- Protect private data: **Only logged-in users (المستخدمون المسجلون فقط)** should access certain pages.  



## **5. Level Up (Optional - تحسين التطبيق)**  
- Add a **third model** with a **many-to-many relationship (علاقة متعدد إلى متعدد)**.  
- Implement full CRUD for the third model.  

