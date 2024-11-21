# Roj-ni-rogari-2
<!DOCTYPE html>
<html lang="gu">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>રોજ ની રોજગારી</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
  <style>
    /* General Styles */
    body {
      font-family: 'Noto Sans Gujarati', sans-serif;
      margin: 0;
      padding: 0;
    }

    /* Splash Screen */
    #splash-screen {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background: linear-gradient(135deg, #4caf50, #2e7d32);
      color: white;
      flex-direction: column;
    }

    #splash-logo {
      font-size: 3rem;
      font-weight: bold;
      margin-bottom: 20px;
      animation: bounce 2s infinite;
    }

    #splash-text {
      font-size: 1.2rem;
      font-style: italic;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-20px); }
    }

    /* Themes for each page */
    .page {
      display: none;
      padding: 20px;
      min-height: 100vh;
    }

    .active {
      display: block;
    }

    #home-page {
      background: linear-gradient(135deg, #2196f3, #21cbf3);
      color: white;
    }

    #job-posts-page {
      background: linear-gradient(135deg, #ff5722, #ff9800);
      color: white;
    }

    #earning-page {
      background: linear-gradient(135deg, #673ab7, #9c27b0);
      color: white;
    }

    /* Header with Logo */
    .header {
      text-align: center;
      padding: 10px;
      background-color: #4caf50;
      color: white;
    }

    .header-logo {
      font-size: 1.8rem;
      font-weight: bold;
    }

    /* Buttons and Chatbot */
    .btn-whatsapp {
      color: white;
      background: #25D366;
      border: none;
      padding: 10px 15px;
      border-radius: 5px;
      text-decoration: none;
      display: inline-block;
    }

    .chatbot-container {
      position: fixed;
      bottom: 10px;
      right: 10px;
      background: white;
      border-radius: 15px;
      padding: 15px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
      display: none;
    }

    .chatbot-container.active {
      display: block;
    }

    .nav-button {
      position: absolute;
      bottom: 20px;
      right: 20px;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 10px;
      background-color: #f4f4f4;
    }
  </style>
</head>
<body>
  <!-- Splash Screen -->
  <div id="splash-screen">
    <div id="splash-logo">રોજ ની રોજગારી</div>
    <div id="splash-text">Your Future Starts Here</div>
  </div>

  <!-- Header -->
  <div class="header">
    <div class="header-logo">રોજ ની રોજગારી</div>
  </div>

  <!-- Home Page -->
  <div id="home-page" class="page active">
    <h2>Welcome to Roj Ni Rojgari</h2>
    <p>We are working for you tirelessly to connect you with the best opportunities.</p>
    <button class="btn btn-primary" onclick="goToPage('job-posts-page')">Job Posts</button>
    <button class="btn btn-success" onclick="goToPage('earning-page')">Earning Opportunities</button>
    <button class="btn btn-secondary" onclick="toggleChatbot()">AI Chatbot</button>
  </div>

  <!-- Job Posts Page -->
  <div id="job-posts-page" class="page">
    <h2>Job Posts</h2>
    <div class="job-post">
      <p><strong>Position:</strong> Data Entry</p>
      <p><strong>Details:</strong> Full-time, Remote</p>
      <a href="https://wa.me/919409960989" class="btn-whatsapp">WhatsApp for Details</a>
    </div>
    <button class="btn btn-secondary" onclick="goToPage('home-page')">Back to Home</button>
  </div>

  <!-- Earning Opportunities Page -->
  <div id="earning-page" class="page">
    <h2>Earning Opportunities</h2>
    <p>Complete surveys and small tasks to earn rewards.</p>
    <button class="btn btn-secondary" onclick="goToPage('home-page')">Back to Home</button>
  </div>

  <!-- AI Chatbot -->
  <div id="chatbot-container" class="chatbot-container">
    <h5>AI Chatbot</h5>
    <p>Ask me anything about the app or job opportunities!</p>
    <input type="text" class="form-control" placeholder="Your question...">
    <button class="btn btn-primary btn-sm mt-2">Ask</button>
  </div>

  <!-- Footer -->
  <footer>
    <p>© 2024 Roj Ni Rojgari | Contact: +91 94099 60989</p>
    <a href="https://www.instagram.com/rojnirojgari/profilecard" target="_blank">Instagram</a> |
    <a href="https://www.facebook.com/profile.php?id=100089337703808" target="_blank">Facebook</a>
  </footer>

  <!-- JavaScript -->
  <script>
    // Splash Screen Logic
    setTimeout(() => {
      document.getElementById('splash-screen').style.display = 'none';
      document.getElementById('home-page').classList.add('active');
    }, 2000);

    // Page Navigation
    function goToPage(pageId) {
      document.querySelectorAll('.page').forEach(page => page.classList.remove('active'));
      document.getElementById(pageId).classList.add('active');
    }

    // Chatbot Toggle
    function toggleChatbot() {
      document.getElementById('chatbot-container').classList.toggle('active');
    }
  </script>
</body>
</html>
