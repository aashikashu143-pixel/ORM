# Ex01 Django ORM Web Application
## Date: 

## AIM
To develop a Django Application to store and retrieve data from a E-Commerce Website Database for Amazon or Flipkart using Object Relational Mapping(ORM).








## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Detect changes and create migration files that describe how to modify the database schema

### STEP 5:
Execute the migration files and update the database schema to match your Django models

### STEP 6:
Create a superuser with full access rights to all models and data through the admin interface.

### STEP 7:
Apply the migration files of the created app to the database

### STEP 8:
Execute Django admin using localhost and create details for 10 entries

## PROGRAM
```
from django.db import models
from django.db import models
from django.contrib import admin
class ecom(models.Model):
    pro_ID=models.CharField(primary_key=True,max_length=7)
    pname=models.CharField(max_length=30)
    cost=models.CharField(max_length=10)
    brand=models.CharField(max_length=1)
    expdate=models.DateTimeField()
    helpcentre=models.EmailField()
    shipdate=models.DateTimeField()

class ecomAdmin(admin.ModelAdmin):
    list_display=["pro_ID","pname","cost","brand","expdate","helpcentre","shipdate"]

from django.contrib import admin
from .models import ecom,ecomAdmin
admin.site.register(ecom,ecomAdmin)

```


## OUTPUT
(<Screenshot 2025-11-26 155535.png>)




## RESULT
Thus the program for creating E-commerce website database using ORM hass been executed successfully
