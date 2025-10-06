# Ex.08 Design of Interactive Image Gallery
# Date:06.10.2025
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
image.html
{% load static%}
<html>
    <head>
        <title> IMAGE GALLERY</title>
    </head>
    <style>
        h1{ text-align: center; text-decoration: underline; -webkit-text-fill-color: goldenrod;}
        h2{ text-align: center; ; -webkit-text-fill-color: #fee92a;}
        body{
            background-image: url(https://img.freepik.com/free-photo/background-gradient-lights_23-2149304985.jpg); background-repeat: no-repeat; background-size: cover;}
        .win{ display: flex; flex-direction: row; padding: 10px; gap: 50px; align-items: center;}   
        .ten{ border: 3px solid orange; border-radius: 20px; padding: auto; height: 270px;px; object-fit: cover; }
       .main {
            display: flex; 
            position: fixed;
            z-index: 10; 
            left: 0;
            top: 0;
            width: 100%; 
            height: 100%;
            background-color: rgba(102, 14, 233, 0.9);
            justify-content: center; 
            align-items: center;      
        }
        .mainimage { 
            width: 60%; 
            height: 60%;
            border-radius: 10px;
            object-fit: contain; 
        }
        .close {
            position: absolute;
            top: 20px;
            right: 35px;
            color:bisque;
            cursor: pointer;
        }
    </style>
    <body>
        <h1> IMAGE GALLERY</h1>
        <h2> THEME: OCEAN</h2>
        <div class="win">
        <img class="ten" src="{% static 'images (1).jpg'%}" alt="image1" onclick="openModal(this)">
        <img class="ten" src="{% static 'images (2).jpg'%}" alt="image2" onclick="openModal(this)">
        <img class="ten" src="{% static 'images.jpg'%}" alt="image3"onclick="openModal(this)" >
        <img class="ten" src="{% static 'sddefault.jpg'%}" alt="image4"onclick="openModal(this)">
         </div>
        <div id="main" class="main" style="display: none;"> 
        <span class="close" onclick="closeModal()">&times;</span>
        <img class="mainimage" id="mainimage">
    </div>
 <script>
    function openModal(imgElement) {
    let one = document.getElementById("main");
    let two = document.getElementById("mainimage");

    two.src = imgElement.src;     
    one.style.display = "flex";  
}
function closeModal() {
    document.getElementById("main").style.display = "none";  
}
</script>
 </body>
</html>


```
# OUTPUT:
![alt text](<../Screenshot (67).png>)
![alt text](<../Screenshot (68).png>)
![alt text](<../Screenshot (69).png>)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
