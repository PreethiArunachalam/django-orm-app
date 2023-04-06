# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Create a new Django project using "django-admin startproject",get into the project's terminal and use "python3 manage.py startapp project" command.

### STEP 2:
Define a model for the myapp in the models.py and allow host access and add the app name under the installed apps in settings.py 

### STEP 3:
Register the models with the Django admin site. In admin.py under app folder, register the models with Django admin site.

## PROGRAM
```
#IN models.py:

from django.db import models
from django.contrib import admin
#Create your model here.

class Patient_detail(models.Model):
    Token_number = models.IntegerField(primary_key=True)
    Name = models.CharField(max_length=100)
    age = models.IntegerField()
    email = models.EmailField()
    phone_number = models.IntegerField()

class Patient_detailAdmin(admin.ModelAdmin):
    list_display = ('Token_number','Name','age','email','phone_number')
    
#IN admin.py:


from django.contrib import admin
from .models import Patient_detail,Patient_detailAdmin
# Register your models here.
admin.site.register(Patient_detail,Patient_detailAdmin)
```

## OUTPUT

![Screenshot 2023-04-06 094910](https://user-images.githubusercontent.com/120115840/230271098-3ecef67c-0476-4f5e-b94c-84725b7fc267.png)

![Screenshot 2023-04-06 093853](https://user-images.githubusercontent.com/120115840/230270756-defd3384-ad25-4879-b0f9-44e58189a068.png)

## RESULT
Thus a Django application to store and retrieve data from a database using Object Relational Mapping(ORM) is developed.
