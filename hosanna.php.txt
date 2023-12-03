<?php
$servername = "localhost";
$username = "root";
$password = "";
$database="realestate";

$conn = mysqli_connect($servername, $username, $password,$database);

if (!$conn) {
  die("Connection failed: " . mysqli_connect_error());
}

if ($_SERVER['REQUEST_METHOD'] == 'POST'){
  $name=$_POST["username"];
  $email=$_POST["email"];
  $message=$_POST["message"];
  $phone=$_POST["phone"];
  $sql = "INSERT into contact (name,email,message,phone) VALUES('" . $name . "','" . $email . "','" . $message . "','" . $phone . "')";
  $success = $conn->query($sql);
  if (!$success) {
      die("Couldn't enter data: ".$conn->error);
  }
  echo "Thank You For Contacting Us ";
  $conn->close();
}
?>

<html>
    <head>
        <title>ANKIT AND VISHAL Web</title>
    <link rel="stylesheet" href="home.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/js/bootstrap.bundle.min.js"></script>
    
    <head>

    <body>
        <!---Navigation Bar-->
        <section id="nav-bar">
            <nav class="navbar navbar-expand-lg navbar-light">
  <a class="navbar-brand" href="#"><img src=".png file"></a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav ml-auto">
      <li class="nav-item ">
        <a class="nav-link" href="#top">Home </a>
      </li>
      <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link" href="#about">About Us</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#services">Services</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#team">Our Team</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#price">Price Plans</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#testimonial">Testimonials</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#getintouch">Contact</a>
      </li>
    </ul>
  </div>
</nav>
    </section>

    <!--Slider-->
    
        <div id="slider">
        <div id="headerSlider" class="carousel slide" data-ride="carousel">
  <ol class="carousel-indicators">
    <li data-target="#headerSlider" data-slide-to="0" class="active"></li>
    <li data-target="#headerSlider" data-slide-to="1"></li>
    <li data-target="#headerSlider" data-slide-to="2"></li>
  </ol>
  <div class="carousel-inner">
    <div class="carousel-item active">
    <img src="C:\xampp\htdocs\RealEstate\img2.jpg">
      <div class="carousel-caption">
      <h5>re-construction Design and Estimating.</h5>
      </div>
    </div>
    <div class="carousel-item">
      <img src="C:\xampp\htdocs\RealEstate\img3.jpg" class="d-block img2-fluid" alt="Mid Bar">
      <div class="carousel-caption">
      <h5>Construction Services.</h5>
      </div>
    </div>
    <div class="carousel-item">
      <img src="C:\xampp\htdocs\RealEstate\photos\img4.jpg" class="d-block img3-fluid" alt="Right Bar">
      <div class="carousel-caption">
      <h5>Sales</h5>
      </div>
    </div>
  </div>
  <a class="carousel-control-prev" href="#headerSlider" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="carousel-control-next" href="#headerSlider" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>
        </div>

<!---About-->
    <section id="about">
    <div class="container">
        <div class="row">
        <div class="col-md-6">
        <h2>About Us</h2>
        <div class="about-content">
        Company where precision, reliability, competence, integrity
        and quality is taken care with utmost importance. Our laboratory
        in India is committed to customer satisfaction; and over the
        years, has been recognized as a pioneer in the field of calibration
        and testing. We are meticulous about serving the industries with 
        competent calibration and testing services with new and innovative methods.
        </div>   
            <button type="button" class="btn btn-primary">Read more>></button>
        </div>

        <div class="col-md-6 skills-bar">
            <p>Construction with Material</p>
            <div class="progress">
                <div class="progress-bar" style="width:80%;">80%</div>
            </div>
            <p>Brokering</p>
            <div class="progress">
                <div class="progress-bar" style="width:90%;">90%</div>
            </div>
            <p>Builder</p>
            <div class="progress">
                <div class="progress-bar" style="width:75%;">75%</div>
            </div>
            <p>Construction without Material</p>
            <div class="progress">
                <div class="progress-bar" style="width:50%;">50%</div>
            </div>
        </div>
        </div>
        </div>
      </section>

<!---Services-->
<section id="services">
  <div class="container">
    <center><h1>Our Services</h1></center>
    <div class="row services">
    <div class="col-md-3 text-center">
    <div class="icon">
    <i class="fas fa-desktop"></i>
    </div>
    <h3>Construction with Material</h3>
    <p>Piramal Glass Private Limited is a global specialist in design,
        production, and decoration of glass packaging. We
        lead the way globally.</p>
    </div>

    <div class="col-md-3 text-center">
    <div class="icon">
    <i class="fas fa-tablet"></i>
    </div>
    <h3>Brokering</h3>
    <p>Piramal Glass Private Limited is a global specialist in design,
        production, and decoration of glass packaging. We
        lead the way globally.</p>
    </div>
    <div class="col-md-3 text-center">
    <div class="icon">
    <i class="fas fa-line-chart"></i>
    </div>
    <h3>Builer</h3>
    <p>Piramal Glass Private Limited is a global specialist in design,
        production, and decoration of glass packaging. We
        lead the way globally.</p>
    </div>
    <div class="col-md-3 text-center">
    <div class="icon">
    <i class="fas fa-paint-brush"></i>
    </div>
    <h3>Construction without Material</h3>
    <p>Piramal Glass Private Limited is a global specialist in design,
        production, and decoration of glass packaging. We
        lead the way globally.</p>
    </div>

    </div>
    </div>    
</section>   

<!---Team Member-->
<section id="team">
  <div class="container">
    <center><h1>Our Team</h1></center>
    <div class="row">
      <div class="col-md-3 profile-pic text-center">
      <div class="img-box">
      <img src="" class="img-responsive">
      <ul>
        <a href="#"><li><i class="fa fa-facebook"></i></li></a>
        <a href="#"><li><i class="fa fa-twitter"></i></li></a>
        <a href="#"><li><i class="fa fa-linkedin"></i></li></a>
        <a href="#"><li><i class="fa fa-instagram"></i></li></a>
        </ul>
      </div>
      <h2>RAHUL VIJAY</h2>
      <h3>Founder/CEO</h3>
      <p>As a founder i have many responsibilities on me.</p>
      </div>

      <div class="col-md-3 profile-pic text-center">
        <div class="img-box">
        <img src="C:\xampp\htdocs\RealEstate\img3.jpg" class="img-responsive">
        <ul>
          <a href="#"><li><i class="fa fa-facebook"></i></li></a>
          <a href="#"><li><i class="fa fa-twitter"></i></li></a>
          <a href="#"><li><i class="fa fa-linkedin"></i></li></a>
          <a href="#"><li><i class="fa fa-instagram"></i></li></a>
          </ul>
        </div>
        <h2>MAYANK JAIN</h2>
        <h3>Business Founder</h3>
        <p>As a founder i have many responsibilities on me.</p>
        </div>

        <div class="col-md-3 profile-pic text-center">
          <div class="img-box">
          <img src="C:\xampp\htdocs\RealEstate\photos\pexels-pixabay-159306" class="img-responsive">
          <ul>
            <a href="#"><li><i class="fa fa-facebook"></i></li></a>
            <a href="#"><li><i class="fa fa-twitter"></i></li></a>
            <a href="#"><li><i class="fa fa-linkedin"></i></li></a>
            <a href="#"><li><i class="fa fa-instagram"></i></li></a>
            </ul>
          </div>
          <h2>ANKIT LALAWAT</h2>
          <h3>Marketing Head</h3>
          <p>As a founder i have many responsibilities on me.</p>
          </div>

          <div class="col-md-3 profile-pic text-center">
            <div class="img-box">
            <img src="Hosanna Web/mem2.jpg" class="img-responsive">
            <ul>
              <a href="#"><li><i class="fa fa-facebook"></i></li></a>
              <a href="#"><li><i class="fa fa-twitter"></i></li></a>
              <a href="#"><li><i class="fa fa-linkedin"></i></li></a>
              <a href="#"><li><i class="fa fa-instagram"></i></li></a>
              </ul>
            </div>
            <h2>VISHAL TIWARI</h2>
            <h3>Website Handler</h3>
            <p>As a founder i have many responsibilities on me.</p>
            </div>
      </div>
  </div>
  </section>
  <!---Promo--->
  <section id="promo">
    <div class="container">
      <p>Owning a home is a keystone of wealth.. both financial affluence and emotional security.</p>
      <a href="#" class="btn-btn-primary">Contact Us</a>
    </div>
  </section>

  <!---Price plans-->
  <section id="price">
    <div class="container">
      <h1>Price Plans</h1>
      <div class="row">
        <div class="col-md-3">
        <div class="single-price">
          <div class="price-head">
            <h2>DELHI</h2>
            <p>250<span> sq feet</span></p>
          </div>
          <div class="price-content">
            <ul>
              <li><i class="fa fa-check-circle"></i>3BHK</li>
              <li><i class="fa fa-check-circle"></i>FREE WIFI</li>
              <li><i class="fa fa-check-circle"></i>RESERVED PARKING</li>
              <li><i class="fa fa-times-circle"></i>POOL FACILITES</li>
              <li><i class="fa fa-times-circle"></i>PRIME LOCATION</li>
            </ul>
          </div>
          <div class="price-button">
            <a class="buy-btn" href="#">BOOK YOUR SLOT</a>
          </div>
        </div>  
        </div>

        <div class="col-md-3">
          <div class="single-price">
            <div class="price-head">
              <h2>LUCKNOW</h2>
              <p>210<span> sq feet</span></p>
            </div>
            <div class="price-content">
              <ul>
                <li><i class="fa fa-check-circle"></i>3BHK</li>
                <li><i class="fa fa-check-circle"></i>FREE WIFI</li>
                <li><i class="fa fa-check-circle"></i>READY TO SHIFT</li>
                <li><i class="fa fa-check-circle"></i>EVERY WEEKEND PARTY</li>
                <li><i class="fa fa-check-circle"></i>Unlimited Support</li>
              </ul>
            </div>
            <div class="price-button">
              <a class="buy-btn" href="#">BOOK YOUR SLOT</a>
            </div>
          </div>  
          </div>

          <div class="col-md-3">
            <div class="single-price">
              <div class="price-head">
                <h2>JAIPUR </h2>
                <p>300<span> sq feet</span></p>
              </div>
              <div class="price-content">
                <ul>
                  <li><i class="fa fa-check-circle"></i>C-SCHEME</li>
                  <li><i class="fa fa-check-circle"></i>Unlimited WIFI</li>
                  <li><i class="fa fa-times-circle"></i>READY TO SHIFT</li>
                  <li><i class="fa fa-times-circle"></i>RESERVED PARKING</li>
                  <li><i class="fa fa-times -circle"></i>BUS STAND</li>
                </ul>
              </div>
              <div class="price-button">
                <a class="buy-btn" href="#">BOOK YOUR SLOT</a>
              </div>
            </div>  
            </div>

            <div class="col-md-3">
              <div class="single-price">
                <div class="price-head">
                  <h2>MUMBAI</h2>
                  <p>250<span> sq feet</span></p>
                </div>
                <div class="price-content">
                  <ul>
                    <li><i class="fa fa-check-circle"></i>Unlimited WIFI</li>
                    <li><i class="fa fa-check-circle"></i>10GB Bandwidth</li>
                    <li><i class="fa fa-times-circle"></i>READY TO SHIFT</li>
                    <li><i class="fa fa-times-circle"></i>BUS STAND</li>
                    <li><i class="fa fa-check-circle"></i>PRIME LOCATION</li>
                  </ul>
                </div>
                <div class="price-button">
                  <a class="buy-btn" href="#">BOOK YOUR SLOT</a>
                </div>
              </div>  
              </div>
      </div>
    </div>
  </section>
  <!---Testimonial--->
  <section id="testimonial">
    <div class="container">
      <h1>Testimonials</h1>
      <p class="text-center">Please follow this page and get most benefit out of it!</p>
    <div class="row">
      <div class="col-md-4 text-center">
        <div class="profile">
        <img src=".jpg" alt="Trulli" width="500" height="333">
          <bockquote>Piramal Glass Private Limited is a global specialist in design,
            production, and decoration of glass packaging. We
            lead the way globally.</bockquote>
            <h3>ANKIT LALAWAT<span> Co-founder at UDB</span></h3>
          </div>
      </div>

      <div class="col-md-4 text-center">
        <div class="profile">
        <img src="C:\Users\Welcome\Pictures\PROJEC\img3.jpg">
          <bockquote>Piramal Glass Private Limited is a global specialist in design,
            production, and decoration of glass packaging. We
            lead the way globally.</bockquote>
            <h3>VISHAL TIWARI<span> Co-founder at UDB</span></h3>
          </div>
      </div>

      <div class="col-md-4 text-center">
        <div class="profile">
          <img src="Hosanna Web/mem.jpg" class="user">
          <bockquote>Piramal Glass Private Limited is a global specialist in design,
            production, and decoration of glass packaging. We
            lead the way globally.</bockquote>
            <h3>AYUSH AGRAWAL<span> Co-founder at UDB</span></h3>
          </div>
      </div>
    </div>
    </div>
  </section>
  <!---Get in touch-->
  <section id="getintouch">
    <div class="container">
      <h1>Get in Touch</h1>
    <div class="row">
      <div class="col-md-6">
        <form class="contact-form" method="POST">
        <div class="form-group">
          <input type="text" class="form-control" required="" placeholder="ENTER NAME" name="username">
        </div>
        
        <div class="form-group">
          <input type="number" class="form-control" required="" placeholder="PHONE NO." name="phone">
        </div>

        <div class="form-group">
          <input type="email" class="form-control" required="" placeholder="EMAIL ID" name="email">
        </div>
        
        <div class="form-group">
          <textarea class="form-control" required="" placeholder="MESSAGE US" name="message"></textarea>
        </div>
        <button type="submit" class="btn btn-primary">Send Message</button>
      </form>
      </div>
    
    </div>
    </div>
  </section>
  <script src="smooth-scroll.js"></script>
  <script>var scroll = new SmoothScroll('a[href*="#"]');</script>
    </body>
</html>