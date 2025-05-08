# Ex.08 Design of Interactive Image Gallery
## Date:08/05/2025

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Interactive Image Gallery</title>
  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body, html {
      height: 100%;
      background: #BEE4D0;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }

    .mainbox {
      width: 80%;
      max-width: 800px;
      height: 550px;
      border: 2px solid #6F826A;
      overflow: hidden;
      border-radius: 15px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.5);
      position: relative;
      background-color: #fff;
    }

    .images {
      display: flex;
      transition: transform 0.5s ease-in-out;
    }

    .slide {
      min-width: 100%;
      text-align: center;
    }

    .slide img {
      width: 100%;
      height: 450px;
      object-fit: cover;
      border-bottom: 1px solid #ccc;
    }

    .caption {
      padding: 15px;
      font-size: 1.4rem;
      font-weight: 600;
      color: #143D60;
      background: #EDE8DC;
    }

    .button {
      top: 50%;
      position: absolute;
      transform: translateY(-50%);
      background: rgba(255, 255, 255, 0.4);
      border: none;
      font-size: 2rem;
      color: #143D60;
      padding: 10px 15px;
      cursor: pointer;
      border-radius: 50%;
      transition: background 0.3s;
      z-index: 2;
    }

    .button:hover {
      background: rgba(255, 255, 255, 0.8);
    }

    .left {
      left: 15px;
    }

    .right {
      right: 15px;
    }

    .txt-up {
      text-align: center;
      color: #143D60;
      font-size: 2rem;
      margin-bottom: 10px;
    }

    .txt-down {
      margin-top: 15px;
      text-align: center;
      color: #27667B;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div class="txt-up"><h1>Interactive Image Gallery</h1></div>

  <div class="mainbox">
    <div class="images" id="images">
      <div class="slide">
        <img src="stellar.webp" alt="img1">
        <div class="caption">Stellar Birthplaces</div>
      </div>
      <div class="slide">
        <img src="planets.jpg" alt="img2">
        <div class="caption">Planetary Portraits</div>
      </div>
      <div class="slide">
        <img src="humantouch.jpg" alt="img3">
        <div class="caption">The Human Touch in Space</div>
      </div>
      <div class="slide">
        <img src="cosmic.jpg" alt="img4">
        <div class="caption">Cosmic Abstracts</div>
      </div>
      <div class="slide">
        <img src="galastic.jpeg" alt="img5">
        <div class="caption">Galactic Vistas</div>
      </div>
    </div>
    <button class="button left" id="left">&lt;</button>
    <button class="button right" id="right">&gt;</button>
  </div>

  <div class="txt-down">
    <h3>NAME: MANJUSRI KAVYA R<br>REGISTER NO: 212224040186</h3>
  </div>

  <script>
    const slider = document.getElementById('images');
    const slides = document.querySelectorAll('.slide');
    const left_bt = document.getElementById('left');
    const right_bt = document.getElementById('right');
    let currentIndex = 0;

    function updateSlider() {
      slider.style.transform = `translateX(-${currentIndex * 100}%)`;
    }

    function nextSlide() {
      currentIndex = (currentIndex + 1) % slides.length;
      updateSlider();
    }

    function prevSlide() {
      currentIndex = (currentIndex - 1 + slides.length) % slides.length;
      updateSlider();
    }

    right_bt.addEventListener('click', nextSlide);
    left_bt.addEventListener('click', prevSlide);
  </script>
</body>
</html>
```

## OUTPUT:
![Screenshot 2025-05-08 094249](https://github.com/user-attachments/assets/45daf383-b06b-4373-97dd-0d87c2fa91f4)
![Screenshot 2025-05-08 094304](https://github.com/user-attachments/assets/2da8bae0-b986-4cb2-8543-4aa79f8756f5)
![Screenshot 2025-05-08 094318](https://github.com/user-attachments/assets/d8c66664-e43a-4892-8b90-f02c7e51afbc)
![Screenshot 2025-05-08 094330](https://github.com/user-attachments/assets/450df247-6b81-4ffd-81ff-5421213ae045)
![Screenshot 2025-05-08 094342](https://github.com/user-attachments/assets/994d5120-fe64-42ce-87f8-72c7b0ed8e32)


## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
