
# Ex02 Django ORM Web Application
# Date:24-10-2024
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM :
```
modals.py
from django.db import models
from django.contrib import admin

# Create your models here.
class Bank_Loan(models.Model):
    loan_id = models.CharField(max_length=20,primary_key=True)
    loan_type = models.CharField(max_length=30)
    loan_amd = models.FloatField()
    cust_acno = models.IntegerField()
    cust_name = models.CharField(max_length=50)


class Bank_LoanAdmin(admin.ModelAdmin):
  list_display = ('loan_id', 'loan_type','loan_amd','cust_acno','cust_name')


admin.py
from django.contrib import admin
from.models import Bank_Loan, Bank_LoanAdmin

# Register your models here.
admin.site.register( Bank_Loan,Bank_LoanAdmin)

```

# OUTPUT :

Include the screenshot of admin page.
![Screenshot (34)](https://github.com/user-attachments/assets/1d097353-30f0-4ee9-8813-e9f9825c1414)
![Screenshot (33)](https://github.com/user-attachments/assets/eb2baacc-bdd3-42ec-8607-902970033c74)

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
