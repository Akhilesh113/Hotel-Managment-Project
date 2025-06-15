# Hotel-Managment-Project
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Akhilesh Singh Hotel Management</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;600&display=swap');
    * {
      box-sizing: border-box;
    }
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: linear-gradient(135deg, #667eea, #764ba2);
      color: #fff;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    header {
      background-color: rgba(0,0,0,0.6);
      padding: 1.5rem 2rem;
      text-align: center;
      box-shadow: 0 2px 10px rgba(0,0,0,0.3);
    }
    header h1 {
      margin: 0;
      font-weight: 600;
      font-size: 2.5rem;
      letter-spacing: 2px;
    }
    nav {
      margin-top: 0.5rem;
    }
    nav a {
      color: #a8cdf0;
      text-decoration: none;
      margin: 0 1rem;
      font-weight: 600;
      transition: color 0.3s ease;
    }
    nav a:hover {
      color: #fff;
    }
    main {
      flex: 1;
      padding: 2rem;
      max-width: 1100px;
      margin: 0 auto;
      background: rgba(255, 255, 255, 0.06);
      border-radius: 12px;
      box-shadow: 0 8px 30px rgba(0,0,0,0.2);
      margin-top: 2rem;
      margin-bottom: 2rem;
    }
    section {
      margin-bottom: 3rem;
    }
    h2.section-title {
      font-size: 2rem;
      border-bottom: 2px solid #a8cdf0;
      padding-bottom: 0.5rem;
      margin-bottom: 1.5rem;
      font-weight: 600;
    }
    /* Hero */
    .hero {
      text-align: center;
    }
    .hero p {
      font-size: 1.2rem;
      line-height: 1.6;
      max-width: 700px;
      margin: 0 auto 1.5rem auto;
      color: #dde8fd;
    }
    /* Rooms */
    .rooms-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(280px,1fr));
      gap: 1.5rem;
    }
    .room-card {
      background: rgba(255,255,255,0.15);
      border-radius: 10px;
      padding: 1rem;
      box-shadow: 0 4px 20px rgb(0 0 0 / 0.15);
      display: flex;
      flex-direction: column;
      transition: transform 0.3s ease;
    }
    .room-card:hover {
      transform: translateY(-6px);
    }
    .room-image {
      width: 100%;
      height: 160px;
      border-radius: 8px;
      object-fit: cover;
      margin-bottom: 1rem;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
    }
    .room-title {
      font-size: 1.25rem;
      margin: 0 0 0.5rem 0;
      font-weight: 600;
    }
    .room-desc {
      flex-grow: 1;
      font-size: 0.95rem;
      margin-bottom: 1rem;
      color: #e0e7ff;
    }
    .room-price {
      font-weight: 700;
      font-size: 1.1rem;
      margin-bottom: 0.5rem;
      color: #ffd166;
    }
    .room-availability {
      font-weight: 600;
      padding: 0.3rem 0.6rem;
      border-radius: 20px;
      font-size: 0.9rem;
      text-align: center;
      width: fit-content;
      color: #fff;
      background-color: #4caf50;
    }
    .room-availability.closed {
      background-color: #e74c3c;
    }
    /* Booking Form */
    form {
      max-width: 600px;
      margin: 0 auto;
      background: rgba(255, 255, 255, 0.12);
      padding: 2rem;
      border-radius: 10px;
      box-shadow: 0 6px 25px rgb(0 0 0 / 0.20);
    }
    form label {
      display: block;
      margin-bottom: 0.3rem;
      font-weight: 600;
    }
    form input, form select {
      width: 100%;
      padding: 0.6rem 0.8rem;
      margin-bottom: 1.2rem;
      border-radius: 6px;
      border: none;
      font-size: 1rem;
    }
    form input[type="submit"] {
      background: #764ba2;
      color: white;
      border: none;
      cursor: pointer;
      font-weight: 700;
      font-size: 1.1rem;
      transition: background-color 0.3s ease;
      border: 2px solid transparent;
    }
    form input[type="submit"]:hover {
      background: #667eea;
      border-color: #fff;
    }
    .booking-success {
      background-color: #4caf50;
      padding: 0.8rem 1rem;
      border-radius: 8px;
      color: white;
      margin-top: 1rem;
      font-weight: 600;
      text-align: center;
    }
    /* Contact */
    .contact-info {
      max-width: 600px;
      margin: 0 auto;
      font-size: 1rem;
      line-height: 1.6;
      color: #dde8fd;
    }
    .contact-info p {
      margin: 0.5rem 0;
    }
    footer {
      text-align: center;
      font-size: 0.9rem;
      padding: 1rem 0;
      background-color: rgba(0,0,0,0.5);
      color: #ccc;
    }
    /* Responsive */
    @media (max-width: 600px) {
      header h1 {
        font-size: 1.8rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Akhilesh Singh Hotel</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#rooms">Rooms</a>
      <a href="#booking">Booking</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>
  <main>
    <section id="home" class="hero">
      <h2 class="section-title">Welcome to Akhilesh Singh Hotel</h2>
      <p>
        Experience luxury and comfort at the heart of the city. Our hotel offers top-notch amenities, elegant rooms, and exceptional service to make your stay unforgettable.
      </p>
    </section>
    <section id="rooms">
      <h2 class="section-title">Our Rooms</h2>
      <div class="rooms-grid">
        <div class="room-card">
          <img src="https://images.unsplash.com/photo-1501117716987-c8f4a3ca0a4f?auto=format&fit=crop&w=600&q=80" alt="Standard Room" class="room-image" />
          <h3 class="room-title">Standard Room</h3>
          <p class="room-desc">Comfortable room with queen-size bed, free Wi-Fi, and city view.</p>
          <p class="room-price">$110 per night</p>
          <span class="room-availability">Available</span>
        </div>
        <div class="room-card">
          <img src="https://images.unsplash.com/photo-1533777324565-a04df0e527b7?auto=format&fit=crop&w=600&q=80" alt="Deluxe Room" class="room-image" />
          <h3 class="room-title">Deluxe Room</h3>
          <p class="room-desc">More spacious with king-size bed, balcony, and premium amenities.</p>
          <p class="room-price">$180 per night</p>
          <span class="room-availability">Available</span>
        </div>
        <div class="room-card">
          <img src="https://images.unsplash.com/photo-1542314831-068cd1dbfeeb?auto=format&fit=crop&w=600&q=80" alt="Suite" class="room-image" />
          <h3 class="room-title">Executive Suite</h3>
          <p class="room-desc">Luxurious suite with separate living area, minibar, and stunning views.</p>
          <p class="room-price">$320 per night</p>
          <span class="room-availability closed">Booked</span>
        </div>
      </div>
    </section>
    <section id="booking">
      <h2 class="section-title">Book Your Stay</h2>
      <form id="bookingForm">
        <label for="name">Full Name *</label>
        <input type="text" id="name" name="name" placeholder="Enter your full name" required />
        
        <label for="email">Email Address *</label>
        <input type="email" id="email" name="email" placeholder="name@example.com" required />
        
        <label for="roomType">Room Type *</label>
        <select id="roomType" name="roomType" required>
          <option value="" disabled selected>Select room type</option>
          <option value="Standard Room">Standard Room</option>
          <option value="Deluxe Room">Deluxe Room</option>
          <option value="Executive Suite" disabled>Executive Suite (Booked)</option>
        </select>
        
        <label for="checkin">Check-in Date *</label>
        <input type="date" id="checkin" name="checkin" required />
        
        <label for="checkout">Check-out Date *</label>
        <input type="date" id="checkout" name="checkout" required />
        
        <input type="submit" value="Book Now" />
      </form>
      <div id="bookingMessage" class="booking-success" style="display:none;"></div>
    </section>
    <section id="contact">
      <h2 class="section-title">Contact Us</h2>
      <div class="contact-info">
        <p><strong>Address:</strong> 123 Horizon Ave, Cityville, Country</p>
        <p><strong>Phone:</strong> +1 (555) 123-4567</p>
        <p><strong>Email:</strong> contact@grandhorizonhotel.com</p>
        <p>We're here to help you 24/7. Reach out anytime!</p>
      </div>
    </section>
  </main>
  <footer>
    &copy; 2024 Grand Horizon Hotel. All rights reserved.
  </footer>
  <script>
    document.getElementById('bookingForm').addEventListener('submit', function(event){
      event.preventDefault();

      const name = this.name.value.trim();
      const email = this.email.value.trim();
      const roomType = this.roomType.value;
      const checkin = this.checkin.value;
      const checkout = this.checkout.value;
      const messageDiv = document.getElementById('bookingMessage');

      // Basic validation
      if (!name || !email || !roomType || !checkin || !checkout) {
        alert('Please fill in all required fields.');
        return;
      }

      if (new Date(checkin) >= new Date(checkout)) {
        alert('Check-out date must be after check-in date.');
        return;
      }

      // Simulate booking success
      messageDiv.style.display = 'block';
      messageDiv.textContent = \`Thank you, \${name}! Your booking for a \${roomType} from \${checkin} to \${checkout} has been received.\`;

      // Reset form
      this.reset();
    });

    // Smooth scroll for nav links
    document.querySelectorAll('nav a').forEach(anchor => {
      anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const targetId = this.getAttribute('href').substring(1);
        document.getElementById(targetId).scrollIntoView({
          behavior: 'smooth'
        });
      });
    });
  </script>
</body>
</html>
