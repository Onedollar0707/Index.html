<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>CampBridge Services</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #f2f2f2;
      color: #333;
    }

    header {
      background-color: #2C7CEE;
      color: white;
      padding: 20px;
      text-align: center;
    }

    .container {
      max-width: 800px;
      margin: 30px auto;
      padding: 20px;
      background: white;
      border-radius: 12px;
      box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
    }

    .service-card {
      border: 1px solid #ddd;
      padding: 15px;
      border-radius: 10px;
      margin-bottom: 20px;
    }

    .service-card h3 {
      margin: 0;
      color: #2C7CEE;
    }

    .service-card p {
      margin: 10px 0;
    }

    .service-card button {
      background: #2C7CEE;
      color: white;
      padding: 10px 16px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }

    .form-section {
      display: none;
      flex-direction: column;
      gap: 12px;
      margin-top: 20px;
    }

    input, textarea {
      padding: 10px;
      font-size: 1rem;
      border-radius: 6px;
      border: 1px solid #ccc;
    }

    .submit-btn {
      background: #1c5abe;
      color: white;
      padding: 10px 16px;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }
  </style>
</head>
<body>

<header>
  <h1>🎓 CampBridge Services</h1>
  <p>Select a service and follow the steps to book.</p>
</header>

<div class="container">

  <div class="service-card">
    <h3>🎯 Admission Research - ₦2,000</h3>
    <p>We help you find the best schools, courses, and requirements.</p>
    <button onclick="showForm('Admission Research', 2000)">Get Started</button>
  </div>

  <div class="service-card">
    <h3>📝 Application Assistance - ₦3,500</h3>
    <p>We assist you with filling and submitting your applications correctly.</p>
    <button onclick="showForm('Application Assistance', 3500)">Get Started</button>
  </div>

  <div class="service-card">
    <h3>🎤 Interview Coaching - ₦3,000</h3>
    <p>Prepare confidently with our mock interviews and coaching.</p>
    <button onclick="showForm('Interview Coaching', 3000)">Get Started</button>
  </div>

  <form class="form-section" id="bookingForm" action="https://formspree.io/f/mwkgbakz" method="POST">
    <input type="text" name="name" placeholder="Your Name" required />
    <input type="email" name="email" placeholder="Your Email" required />
    <input type="tel" name="phone" placeholder="WhatsApp Number" required />
    <textarea name="message" rows="4" placeholder="Additional Notes (Optional)"></textarea>
    <input type="hidden" id="selectedService" name="service" value="" />
    <button class="submit-btn" type="submit">Submit & Proceed to Payment</button>
  </form>

</div>

<script>
  function showForm(service, price) {
    document.getElementById('selectedService').value = service + ' - ₦' + price;
    document.getElementById('bookingForm').style.display = 'flex';
    window.scrollTo({ top: document.body.scrollHeight, behavior: 'smooth' });
  }
</script>

</body>
</html>
