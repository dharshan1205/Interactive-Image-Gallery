# Ex.08 Design of Interactive Image Gallery
# Date:4/11/2025
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
# image.html:
```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive  Cartoons Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="gallery-container">
        <div class="gallery-item">
            <img src="chotta bheem.webp" alt="Image 1">
        </div>
        <div class="gallery-item">
            <img src="doreman.jpg" alt="Image 2">
        </div>
        <div class="gallery-item">
            <img src="grizzly.jpg" alt="Image 3">
        </div>
        <div class="gallery-item">
            <img src="hattorri.jpeg" alt="Image 4">
        </div>
        <div class="gallery-item">
            <img src=" shinchan.png" alt="Image 5">
        </div>
    </div>

    <div class="modal" id="modal">
        <span class="close" id="close">&times;</span>
        <img class="modal-content" id="modal-img">
    </div>
    
    <footer class="footer">
        <p>&copy; Image Gallery | Designed by: <b>RANJITH R</b></p>
    </footer>
       
    <script src="index.js"></script>
</body>
</html>
```
# index.js:
```
const images = document.querySelectorAll('.gallery-item img');
const modal = document.getElementById('modal');
const modalImg = document.getElementById('modal-img');
const closeBtn = document.getElementById('close');

images.forEach((image) => {
    image.addEventListener('click', () => {
        modal.style.display = 'block';
        modalImg.src = image.src; 
    });
});

closeBtn.addEventListener('click', () => {
    modal.style.display = 'none';
});
```
# style.css:
```
body {position: absolute;
    background-color: gray;
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #e3e0e0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    overflow: hidden;
}

.gallery-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 10px;
    padding: 20px;
    max-width: 1200px;
    width: 100%;
}

.gallery-item img {
    width: 100%;
    height: auto;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(255, 255, 255, 0.1);
    transition: transform 0.3s ease;
}

.gallery-item img:hover {
    transform: scale(1.30);
    cursor: pointer;
}

.modal {
    display: none;
    position: fixed;
    z-index: 1;
    padding-top: 100px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0, 0, 0, 0.7);
}

.modal-content {
    margin: auto;
    display: block;
    width: 80%;
    max-width: 700px;
    border-radius: 10px;
}

.close {
    position: absolute;
    top: 10px;
    right: 25px;
    color: #ffffff;
    font-size: 36px;
    font-weight: bold;
    cursor: pointer;
}

.close:hover,
.close:focus {
    color: #ffffff;
    text-decoration: none;
    cursor: pointer;
}
```
# OUTPUT:

![Screenshot 2025-05-09 143750](https://github.com/user-attachments/assets/74ed8d60-9679-4360-88d4-b5a7d61b9f7d)


![Screenshot 2025-05-09 144045](https://github.com/user-attachments/assets/75c35ef4-1b52-4cb8-9148-0754b8436ea0)



# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
