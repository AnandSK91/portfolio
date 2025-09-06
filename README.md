<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>IIT Hyderabad Library App</title>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@picocss/pico@1/css/pico.min.css">
  <style>
    body {
      background: #fafafa;
      font-family: system-ui, sans-serif;
    }
    header {
      text-align: center;
      padding: 2rem 1rem;
      background: #f36f21;
      color: white;
    }
    nav.bottom-nav {
      position: fixed;
      bottom: 0;
      left: 0;
      right: 0;
      background: white;
      border-top: 1px solid #ddd;
      display: flex;
      justify-content: space-around;
      padding: 0.5rem 0;
    }
    nav.bottom-nav a {
      text-decoration: none;
      color: #333;
      font-size: 0.9rem;
    }
    main.container {
      padding-bottom: 4rem; /* space for nav */
    }
    .card {
      padding: 1rem;
      background: white;
      border-radius: 8px;
      margin-bottom: 1rem;
      box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    }
    .grid-2 {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1rem;
    }
  </style>
</head>
<body>

  <!-- Splash / Header -->
  <header>
    <h1>IIT Hyderabad Library</h1>
    <p>Knowledge for All</p>
  </header>

  <!-- Main Area -->
  <main class="container">

    <!-- Home Dashboard -->
    <section class="card">
      <hgroup>
        <h2>Welcome</h2>
        <h3>Quick Access</h3>
      </hgroup>
      <div class="grid-2">
        <a class="card" href="#search">📖 Catalog</a>
        <a class="card" href="#account">👤 My Account</a>
        <a class="card" href="#digital">💻 Digital Library</a>
        <a class="card" href="#notices">📢 Notices</a>
      </div>
    </section>

    <!-- Search -->
    <section id="search" class="card">
      <hgroup>
        <h2>Search Catalog</h2>
        <h3>Books, Journals & More</h3>
      </hgroup>
      <form>
        <input type="text" placeholder="Enter title, author, or keyword" required>
        <button type="submit" onclick="event.preventDefault()">Search</button>
      </form>
    </section>

    <!-- Account -->
    <section id="account" class="card">
      <hgroup>
        <h2>My Account</h2>
        <h3>Borrowed Books</h3>
      </hgroup>
      <ul>
        <li>Book 1 – Due: Sept 15 <button>Renew</button></li>
        <li>Book 2 – Due: Sept 20 <button>Renew</button></li>
      </ul>
    </section>

    <!-- Digital Library -->
    <section id="digital" class="card">
      <hgroup>
        <h2>Digital Resources</h2>
        <h3>Access e-Journals & Databases</h3>
      </hgroup>
      <ul>
        <li><a href="#">IEEE Xplore</a></li>
        <li><a href="#">Scopus</a></li>
        <li><a href="#">Springer</a></li>
      </ul>
    </section>

    <!-- Notices -->
    <section id="notices" class="card">
      <hgroup>
        <h2>Library Notices</h2>
        <h3>Updates & Announcements</h3>
      </hgroup>
      <p>📅 Workshop on Research Tools – Sept 10</p>
      <p>📢 New Arrivals in Science Collection</p>
    </section>

  </main>

  <!-- Bottom Navigation -->
  <nav class="bottom-nav">
    <a href="#">🏠 Home</a>
    <a href="#search">🔍 Search</a>
    <a href="#account">👤 Account</a>
    <a href="#digital">💻 Digital</a>
    <a href="#notices">📢 More</a>
  </nav>

</body>
</html>
