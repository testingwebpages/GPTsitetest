
<html>
<head>
    <title>One Page Website</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .navbar {
            background-color: black;
            height: 50px;
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
        }

        .navbar button {
            color: white;
            background-color: transparent;
            border: none;
            margin: 0 10px;
            cursor: pointer;
        }

        .logo {
            height: 20px;
            width: 40px;
            margin-left: 10px;
        }

        .banner-container {
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 20px;
        }

        .banner img {
            width: 1000px;
            height: 500px;
            margin: 0 10px;
        }

        .scroll-to-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            width: 40px;
            height: 40px;
            background-color: #333;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 20px;
            cursor: pointer;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .scroll-to-top.show {
            opacity: 1;
        }

        .additional-navbar {
            background-color: black;
            height: 50px;
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
            margin-top: 20px;
        }

        .additional-navbar button {
            color: white;
            background-color: transparent;
            border: none;
            margin: 0 10px;
            cursor: pointer;
        }
        .circle {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 200px;
  height: 200px;
  background-color: white;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  opacity: 0;
  transition: opacity 0.5s;
  font-weight: bold;
  font-size: 50px;
  color: black;
}
    </style>
</head>
<body>
    <div class="navbar">
        <img src="logo.png" alt="Logo" class="logo">
        <button id="homeButton">Home</button>
        <button id="shopButton">Shop</button>
        <button id="aboutButton">About Us</button>
        <button id="contactButton">Contacts</button>
    </div>
    <div class="banner-container">
        <img src="Images/ban1 (1).jpg" alt="Banner 1" class="banner">
    </div>
    <div class="banner-container">
        <img src="Images/ban1 (2).jpg" alt="Banner 2" class="banner">
    </div>
    <div class="banner-container">
        <img src="Images/ban1 (3).jpg" alt="Banner 3" class="banner">
    </div>
    <div class="additional-navbar">
        <button>Email: OussamaChatGPT@google.com</button>
        <button>Instagram: Oussema_tt</button>
    </div>
    <div class="scroll-to-top" id="scrollToTop">
        UP
    </div>
    <div class="circle" id="circle" onclick="toggleCircle()">OOPS!</div>
    

    <script>
        const homeButton = document.getElementById('homeButton');
        const shopButton = document.getElementById('shopButton');
        const aboutButton = document.getElementById('aboutButton');
        const contactButton = document.getElementById('contactButton');
        const scrollToTopButton = document.getElementById('scrollToTop');

        homeButton.addEventListener('click', function() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });

        shopButton.addEventListener('click', function() {
            window.scrollTo({
                top: document.getElementsByClassName('banner-container')[2].offsetTop,
                behavior: 'smooth'
            });
        });

        aboutButton.addEventListener('click', function() {
            window.scrollTo({
                top: document.getElementsByClassName('banner-container')[1].offsetTop,
                behavior: 'smooth'
            });
        });

        contactButton.addEventListener('click', function() {
            window.scrollTo({
                top: document.body.scrollHeight,
                behavior: 'smooth'
            });
        });

        scrollToTopButton.addEventListener('click', function() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });

        window.addEventListener('scroll', function() {
            if (window.pageYOffset > 300) {
                scrollToTopButton.classList.add('show');
            } else {
                scrollToTopButton.classList.remove('show');
            }
        });
        function toggleCircle() {
  var circle = document.getElementById("circle");
  if (circle.style.opacity == 0) {
    circle.style.opacity = 1;
  } else {
    circle.style.opacity = 0;
  }
}
    </script>
</body>
</html>
