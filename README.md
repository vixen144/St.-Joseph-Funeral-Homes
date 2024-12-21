<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ST. JOSEPH FUNERAL SERVICE</title>
    <link rel="stylesheet" href="/funeral.css">
</head>
<body>

    <header class="sticky-header">
        <table width="100%" class="header">
            <tr>
                <td id="imglogo">
                    <!-- LOGO -->
                    <img src="/IMAGES/LOGO/ST.JOSEPH LOGO.png" alt="Logo">
                </td>
                <td align="right" class="navigator">
                    <!-- NAVIGATOR -->
                    <a href="FUNERAL.html">HOME</a>
                    <a href="#aboutus">ABOUT US</a>
                    <a href="#typeofservice">TYPE OF SERVICE</a>
                    <a href="#contactus" id="contact">CONTACT US</a>
                </td>
            </tr>
        </table>
        </div>
    </header>
    

<main>
    <table align="center" class="banner">
        <tr>
            <td>
                <div class="banner-content">
                    <img src="/IMAGES/HOMEPAGE PIC/HOMEPAGE PIC.jpg" alt="homepagebanner" id="hpbanner">
                    <div class="text-overlay">
                        <div class="text-left">
                            <h1>ST.JOSEPH</h1>
                            <p id="banner2">FUNERAL HOMES</p>
                        </div>
                        <div class="text-right">
                            <p>guiding you through with grace and compassion.</p>
                        </div>
                    </div>
                </div>
            </td>
        </tr>
    </table>
    
  
    <br>
    <!-- Table displaying service options -->
     
    <table class="tos" id="typeofservice">
        <tr>
            <td>
                <h1> TYPE OF SERVICE</h1>
                <p>St. Joseph Funeral Service provides a complete package that include a coffin, hearse, and floral arrangement</p>
            </td>
        </tr>
    </table>
    <div class="image-container">
        <div class="image-item">
            <a href="/COFFIN.html"><p>COFFIN</p></a>
            <a href="/COFFIN.html">
                <img class="hover-effect" src="/IMAGES/COFFIN/WOODEN CASKET/FLAT/ETERNAL FLIGHT.jpg" alt="Coffin Pictures">
            </a>
        </div>
        <div class="image-item">
            <a href="/FLOWER.html"><p>FLOWERS</p></a>
            <a href="/FLOWER.html">
                <img class="hover-effect" src="/IMAGES/FLOWERS/f1.jpg" alt="Flowers Pictures">
            </a>
        </div>
        <div class="image-item">
            <a href="/HEARSE.html"><p>HEARSE</p></a>
            <a href="/HEARSE.html">
                <img class="hover-effect" src="/IMAGES/HEARSE/h1.jpg" alt="Hearse Pictures">
            </a>
        </div>
    </div>
    

    <br>
    <br>
    <br>
    <br>
    <br>

   <table class="aboutus" id="aboutus">
    <tr>
        <td>
            <h1 id="aboutus1">ST.JOSEPH</h1>
            <p id="aboutus2">
                Funeral Homes
            </p>
        </td>
        <td>
            <h1 id="aboutush">
                ABOUT US
            </h1>
            <p id="aboutusp">
                Saint Joseph Funeral Homes originated from a <br> proposal by a City of Calamba councilor, urging <br>
                Barangay Looc to offer complimentary funeral <br> service for residents. Motivated by concern for <br> 
                families facing financial hardships during times of <br> loss, the councilor envisioned a service that 
                would  <br> ease the financial burgen and promoted solidarity <br> within the community, This initiative laid the foundation <br>
                for Saint Joseph Funeral Homes, dedicated <br> to providing dignified, compassionated funeral service <br> to all, regardless of 
                financial circumstances.

            </p>
        </td>
    </tr>
   </table >

   <div class="container" id="contactus">
    <form id="registrationForm">
        <h2 id="form">Registration Form</h2>
        
        <label for="firstname">First Name</label>
        <input type="text" name="firstname" class="input" placeholder="Enter your first name" required id="firstname">

        <label for="lastname">Last Name</label>
        <input type="text" name="lastname" class="input" placeholder="Enter your last name" required id="lastname">

        <label for="email">Email</label>
        <input type="email" name="email" class="input" placeholder="Enter your email" required id="email">

        <label for="contactnumber">Contact Number</label>
        <input type="text" name="contactnumber" class="input" placeholder="Enter your contact number" required id="contactnumber">

        <label for="address">Address</label>
        <input type="text" name="address" class="input" placeholder="Enter your address" required id="address">

        <button type="button" class="input" id="register" onclick="validateForm()"> 
            Register
        </button>
    </form>
    
    <p id="error-message" style="color: red; display: none;"></p> <!-- For error message -->
</div>

<script>
    function validateForm() {
        let email = document.getElementById('email');
        let contactnumber = document.getElementById('contactnumber');
        let errorMessage = '';
        
        // Clear any previous error messages
        document.getElementById('error-message').style.display = 'none';

        // Clear all red borders
        email.style.border = '';
        contactnumber.style.border = '';

        // Email validation
        if (!email.value.includes('@')) {
            errorMessage = 'Error: Please enter a valid email with "@" symbol.';
            email.style.border = '2px solid red'; // Add red border to email
        }

        // Contact number validation
        if (/\D/.test(contactnumber.value)) { // Check for non-digits
            errorMessage = 'Error: Please enter a valid contact number (numbers only).';
            contactnumber.style.border = '2px solid red'; // Add red border to contact number
        }

        // If there's an error, display it
        if (errorMessage) {
            document.getElementById('error-message').innerText = errorMessage;
            document.getElementById('error-message').style.display = 'block';
        } else {
            // If no errors, show success (form can be submitted here if needed)
            alert('Form submitted successfully!');
        }
    }

    document.addEventListener("DOMContentLoaded", function() {
        const links = document.querySelectorAll("a[href^='#']");
        
        links.forEach(link => {
            link.addEventListener("click", function(event) {
                event.preventDefault();
                
                const targetId = this.getAttribute("href").substring(1);
                const targetElement = document.getElementById(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop,
                        behavior: "smooth"
                    });
                }
            });
        });
    });
    
</script>



    <footer>
        <table class="footer">
            <td align="left">
                <p>&copy;St.JosephFuneralHomes.All rights reserved</p>
            </td>
            <td align="right">
                <a href="/team.html" id="contact">TEAM</a>
            </td>
        </table>
       
    </footer>

</body>

</html>
