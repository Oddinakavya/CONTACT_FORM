# CONTACT_FORM

DYNAMITE_WEBTECH

TASK 6

COMPANY NAME: DYNAMITE WEBTECH

NAME - ODDINA KAVYA

INTERN ID: u75da

CODE:

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Contact Us</title>
  <script src="https://cdn.jsdelivr.net/npm/emailjs-com@3/dist/email.min.js"></script>
  <style>
    * {
      box-sizing: border-box;
    }

    body {
      background: #f4f4f4;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      padding: 20px;
    }

    .contact-form {
      max-width: 600px;
      margin: auto;
      background: white;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
    }

    h2 {
      text-align: center;
      margin-bottom: 20px;
      color: #333;
    }

    input, textarea {
      width: 100%;
      padding: 14px;
      margin: 10px 0 20px;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 16px;
      resize: vertical;
    }

    input:focus, textarea:focus {
      outline: none;
      border-color: #007BFF;
    }

    button {
      background-color: #007BFF;
      color: white;
      padding: 14px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      font-size: 16px;
      width: 100%;
    }

    button:hover {
      background-color: #0056b3;
    }

    .success-message {
      color: green;
      text-align: center;
      margin-top: 10px;
    }

    .error-message {
      color: red;
      text-align: center;
      margin-top: 10px;
    }
  </style>
</head>
<body>

  <div class="contact-form">
    <h2>Contact Us</h2>
    <form id="contactForm">
      <input type="text" name="user_name" placeholder=" Enter Your Name" required />
      <input type="email" name="user_email" placeholder="Enter Your Email" required />
      <input type="text" name="subject" placeholder="Subject" required />
      <textarea name="message" rows="5" placeholder=" Enter Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
    <div class="success-message" id="successMsg"></div>
    <div class="error-message" id="errorMsg"></div>
  </div>

  <script>
    // Initialize EmailJS
    (function(){
      emailjs.init("YOUR_PUBLIC_KEY"); // Replace with your EmailJS Public Key
    })();

    // Handle form submission
    document.getElementById("contactForm").addEventListener("submit", function(e) {
      e.preventDefault();

      emailjs.sendForm("YOUR_SERVICE_ID", "YOUR_TEMPLATE_ID", this)
        .then(function() {
          document.getElementById("successMsg").textContent = "Message sent successfully!";
          document.getElementById("errorMsg").textContent = "";
          document.getElementById("contactForm").reset();
        }, function(error) {
          document.getElementById("errorMsg").textContent = "Failed to send. Please try again.";
          document.getElementById("successMsg").textContent = "";
        });
    });
  </script>
</body>
</html>

output for task 6: for contact us form
![Image](https://github.com/user-attachments/assets/d5b57cee-26ba-4e8b-9981-3f4c2ae14779)



