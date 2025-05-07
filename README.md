# Kochin_gentleman
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Kochin Gentleman Freelancer</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; }
    header { background-color: #0077cc; color: white; padding: 20px; text-align: center; }
    nav { background-color: #005fa3; padding: 10px; text-align: center; }
    nav a { color: white; margin: 0 15px; text-decoration: none; font-weight: bold; }
    .container { padding: 20px; }
    form input, form select, form textarea { display: block; margin: 10px 0; width: 100%; padding: 8px; }
    .card { border: 1px solid #ccc; padding: 15px; margin-bottom: 10px; }
    footer { background-color: #f1f1f1; text-align: center; padding: 10px; }
    img { max-width: 100%; height: auto; border-radius: 8px; margin-bottom: 10px; }
  </style>
</head>
<body>
  <header>
    <h1>Kochin Gentleman Freelancer</h1>
    <p style="font-size: 18px; color: #ffe600; font-weight: bold; margin-top: -10px;">Trust & Verify</p>
    <p>Find or offer rooms, jobs, and taxi services in Kochi</p>
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/56/Kochi_City.jpg/800px-Kochi_City.jpg" alt="Kochi City" />
  </header>
  <nav>
    <a href="#home">Home</a>
    <a href="#post">Post Service</a>
    <a href="#listings">Browse Listings</a>
    <a href="#contact">Contact</a>
  </nav>
  <div class="container" id="home">
    <h2>Welcome to Kochin Gentleman Freelancer</h2>
    <p>Kochin Gentleman Freelancer is your local hub for connecting people across Kochi. Whether you're searching for a room to rent, a job opportunity, or a reliable taxi service — this platform brings it all to one place. Designed for ease and speed, our site helps individuals and businesses in Kochi post, browse, and connect without hassle.</p>
    <h3>Service Categories</h3>
    <p>Explore the different services available on our platform:</p>
    <ul>
      <li><strong>Commercial/Residential Rooms:</strong> Find or rent spaces in and around Kochi, from apartments to shops.</li>
      <li><strong>Jobs in Kochi:</strong> Post or discover job vacancies suited for locals and newcomers.</li>
      <li><strong>Call Taxi / Driver Services:</strong> Hire a taxi, find a driver, or offer your driving services to the city.</li>
    </ul>
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/7e/Cab_driver_waiting.jpg/800px-Cab_driver_waiting.jpg" alt="Taxi Driver" />
  </div>
  <div class="container" id="post">
    <h2>Post a Service</h2>
    <form id="postForm">
      <input type="text" id="title" placeholder="Service Title" required />
      <select id="category">
        <option>Room</option>
        <option>Job</option>
        <option>Taxi</option>
      </select>
      <textarea id="description" placeholder="Service Description" required></textarea>
      <input type="text" id="contact" placeholder="Contact Info" required />
      <button type="submit">Post</button>
    </form>
  </div>
  <div class="container" id="listings">
    <h2>Available Listings</h2>
    <div id="listingsContainer"></div>
  </div>
  <div class="container" id="about">
    <h2>About Us</h2>
    <p>Hi, I’m Yasar Arafath from Malappuram. I have 10 years of experience in sales and management, and I speak five languages fluently. If you need any help in Kochi, I’m here for you. Trust and verify my services, and let’s build a reliable connection. 🤝</p>
    <p>Feel free to reach out through my <a href="https://www.instagram.com/yasar_arafath_cv">Instagram</a> or <a href="https://wa.me/8660274654">WhatsApp</a> links.</p>
  </div>
    <h2>Contact Us</h2>
    <p>Email: support@kochi-services.com</p>
    <p>Phone: 8660274654</p>
  </div>
  <footer>
    <p>&copy; 2025 Kochin Gentleman Freelancer</p>
  </footer>

  <script>
    const form = document.getElementById('postForm');
    const listingsContainer = document.getElementById('listingsContainer');

    form.addEventListener('submit', function(event) {
      event.preventDefault();

      const title = document.getElementById('title').value;
      const category = document.getElementById('category').value;
      const description = document.getElementById('description').value;
      const contact = document.getElementById('contact').value;

      const card = document.createElement('div');
      card.className = 'card';
      card.innerHTML = `<h3>${title} (${category})</h3><p>${description}</p><p><strong>Contact:</strong> ${contact}</p>`;

      listingsContainer.appendChild(card);
      form.reset();
    });
  </script>
</body>
</html>