# Ex02 Django ORM Web Application
# Date:18-10-2024
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

# PROGRAM
```from django.db import models
from django.contrib import admin


class Loan(models.Model):
    customer_id = models.IntegerField(primary_key='true')
    loan_type = models.CharField(max_length=50)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)
    interest_rate = models.DecimalField(max_digits=5, decimal_places=2)
    loan_term_in_years = models.IntegerField()
    start_date = models.DateField()

class LoanAdmin(admin.ModelAdmin):
    list_display=('customer_id', 'loan_type', 'loan_amount', 'interest_rate', 'loan_term_in_years', 'start_date')
# Register your models here.
from django.contrib import admin
from .models import Loan, LoanAdmin

admin.site.register(Loan, LoanAdmin)
```
# OUTPUT
![pn1](https://github.com/user-attachments/assets/08e59789-2f82-4d41-b0ce-75f22df8c9a6)
![pn](https://github.com/user-attachments/assets/4d16dea6-a29a-4706-b3ba-75b99395488c)

Include the screenshot of your admin page.

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
