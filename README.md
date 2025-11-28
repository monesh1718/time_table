# Ex03 Time Table
# Date:28.11.2025
# AIM
To write a html webpage page to display your slot timetable.

# ALGORITHM
## STEP 1
Create a Django-admin Interface.

## STEP 2
Create a static folder and inert HTML code.

## STEP 3
Create a simple table using `<table>` tag in html.

## STEP 4
Add header row using `<th>` tag.

## STEP 5
Add your timetable using `<td>` tag.

## STEP 6
Execute the program using runserver command.

# PROGRAM

urls.py
```
from django.contrib import admin
from django.urls import path
from slotapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('tt/', views.slot)
]
```

views.py
```
from django.shortcuts import render

def slot(request):
    return render(request,'slot.html')
```

slot.html

```
{% load static %}

<!DOCTYPE html>

<html>
    <head>
        <title>TIMETABLE</title>
        <style>
        table,th,td
        {
        border: 3PX SOLID black;
        margin-left: auto;
        margin-right: auto;
        background-color:crimson;
        padding: 10px;
        }
        img{
            height: 200px;
            width: 1000px;
            margin-left: auto;
            margin-right: auto;
            display:block;
        }
        h1
        {
            font-size: 40px;
            color: brown;
            font-family: 'Times New Roman', Times, serif;
            font-style: bold;
            text-align: center;
        }
        </style>
    </head>
    <body>
        <img src="{%static 'seclogo.png'%}">
        <table style="border-collapse: collapse;border:4px ;">
            <h1>TIMETABLE</h1>
            <tr>
                <th>Time</th>
                <th>Monday</th>
                <th>Tuesday</th>
                <th>Wednesday</th>
                <th>Thursday</th>
                <th>Friday</th>
                <th>Saturday</th>
            </tr>
            <tr>
                <td STYLE="color: black;">8AM-10AM</td>
                <TD colspan="3"STYLE="text-align:center;">WEB</TD>
                <TD colspan="2"style="text-align:center;">FREE SLOT</TD>
                <TD rowspan="2"style="text-align:center;">PUBLIC SPEAKING</TD>
            </tr>
            <TR>
                <TD STYLE="color: black;">10AM-12AM</TD>
                <td colspan="2" style="text-align:center ;">FREE SLOT</td>
                <TD>PUBLIC SPEAKING</TD>
                <TD colspan="2"STYLE="text-align:center;">FREE SLOT</TD>
            </TR>
            <TR>
                <TD style="color: black;">12PM-1PM</TD>
                <TD colspan="6" style="text-align: center;">LUNCH BREAK</TD>
            </TR>
            <TR>
                <TD>1PM-3PM</TD>
                <TD>WEB</TD>
                <TD>FREE SLOT</TD>
                <TD>MENTOR MEET</TD>
                <TD>PUBLIC SPEAKING</TD>
                <TD>WEB</TD>
                <TD>PUBLIC SPEAKING</TD>           
            </TR>
            <tr>
                <td style="color: black;">3PM-5PM</td>
                <TD colspan="4"style="text-align:center;">PYTHON</TD>
                <TD>FREE SLOT</TD>
                <TD>PYTHON</TD>
            </tr>
            </table>
            <br>
            <br>
            <table style="border:4:"style="border:double;"cellpadding="10"cellspacing="3" width="900"height="30">
            <tr>
                <th>s.no</th>
                <th>SUBJECT CODE</th>
                <th>SUBJECT NAME</th>
            </tr>
            <tr>
                <td>1.</td>
                <td>19A1414</td>
                <td>Fundamnetals of web Application development(FWAD)</td>
            </tr>
            <TR>
                <td>2.</td>
                <TD>19A1301</td>
                <td>python programming</td>
            </TR>
            <tr>
                <td>3.</td>
                <td>19EN101</td>
                <td>public speaking</td>
            </tr>
        </table>
    </body>
    
</html>

```

# OUTPUT
<img width="1890" height="967" alt="Screenshot 2025-11-27 221256" src="https://github.com/user-attachments/assets/911e3855-a1fe-4f16-9222-aca35798f793" />

# RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
