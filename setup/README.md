
# Django CRUD App Lab - Setup

Follow these steps to **set up your project** correctly.  



### **1. Open Your Terminal and Navigate to the Right Folder**  
1. Open your **Terminal (سطر الأوامر)**.  
2. Move to the correct folder:  
   ```bash
   cd ~/code/ga/lessons
   ```  



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


### **6. Deactivate the Virtual Environment**  
When you're done working, **exit the virtual environment**:  
```bash
exit
```  

---
