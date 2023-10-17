# demo1
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sabit Navbar Örneği</title>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
    <style>
        /* Sabit Navbar Stili */
        body {
            padding-top: 56px; /* Navbar yüksekliği kadar boşluk bırak */
        }

        .navbar-fixed {
            position: fixed;
            top: 0;
            width: 100%;
            
        }
        .gradient-background {
    background: linear-gradient(300deg, #667479, #363435, #07ec40);
    background-size: 180% 180%;
    height: 700px;
    animation: gradient-animation 18s ease infinite;
  }
  
  @keyframes gradient-animation {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }
  
  .icon-square {
    width: 3rem;
    height: 3rem;
    border-radius: 0.75rem;
  }
  
  .profile-img {
    position: relative;
    border-radius: 50%;
    height: 100px;
  }
  h1{
    position: relative;
    top: 200px;
    color: #0a0b0c;
    text-align: center;
    font-size: 50px;
    
  }
  p{
    position: relative;
    text-align: center;
    font-size: 30px;
    top: 250px;
  }
  .navbar{
    background-color: #056e5d;
  }
    </style>
</head>
<body>
    <!-- Sabit Navbar -->
    <nav class="navbar navbar-expand-lg navbar-light bg-custom navbar-fixed">
        <a class="navbar-brand" href="#">Botlift</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li class="nav-item active">
                    <a class="nav-link" href="#" id="home" style="color: aliceblue;">Home <span class="sr-only">(current)</span></a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#" id="about" style="color: aliceblue;">About us</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#" id="services" style="color: aliceblue;">Services</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#" id="contact" style="color: aliceblue;">Contact</a>
                </li>
            </ul>
        </div>
    </nav>

    <!-- Sayfa İçeriği -->
    <div class="gradient-background">
        <h1 style="color: aliceblue;">welcome!</h1>
        <p>Bot website</p>
    </div>

    <!-- Bootstrap ve jQuery Kütüphaneleri -->
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.6/dist/umd/popper.min.js"></script>
    <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
    <script>document.addEventListener('DOMContentLoaded', function () {
        const contentDiv = document.getElementById('content');
        const homeLink = document.getElementById('home');
        const aboutLink = document.getElementById('about');
        const servicesLink = document.getElementById('services');
        const contactLink = document.getElementById('contact');
    
        homeLink.addEventListener('click', function (e) {
            e.preventDefault();
            contentDiv.innerHTML = '<h1>Ana Sayfa</h1><p>Bu, ana sayfa içeriğidir.</p>';
        });
    
        aboutLink.addEventListener('click', function (e) {
            e.preventDefault();
            contentDiv.innerHTML = '<h1>Hakkımızda</h1><p>Şirketimiz hakkında bilgiler burada bulunmaktadır.</p>';
        });
    
        servicesLink.addEventListener('click', function (e) {
            e.preventDefault();
            contentDiv.innerHTML = '<h1>Hizmetler</h1><p>Sunduğumuz hizmetler aşağıda listelenmiştir.</p>';
        });
    
        contactLink.addEventListener('click', function (e) {
            e.preventDefault();
            contentDiv.innerHTML = '<h1>İletişim</h1><p>Bize buradan ulaşabilirsiniz.</p>';
        });
    });
    </script>
</body>
</html>
