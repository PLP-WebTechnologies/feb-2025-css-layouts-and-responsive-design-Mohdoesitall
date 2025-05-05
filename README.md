# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨




<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Layout with Flexbox</title>
  <style>
    /* General Styles */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: Arial, sans-serif;
    }

    header {
      background-color: #333;
      color: white;
      padding: 10px 0;
    }

    .navbar ul {
      display: flex;
      justify-content: center;
      list-style: none;
    }

    .navbar ul li {
      margin: 0 15px;
    }

    .navbar ul li a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }

    /* Main Content Layout using Flexbox */
    main {
      display: flex;
      justify-content: center;
      padding: 20px;
    }

    .content {
      display: flex;
      justify-content: space-between;
      width: 100%;
      max-width: 1200px;
    }

    .left, .right {
      width: 45%;
    }

    .left {
      background-color: #f4f4f4;
      padding: 20px;
    }

    .right {
      background-color: #e2e2e2;
      padding: 20px;
    }

    /* Footer */
    footer {
      background-color: #333;
      color: white;
      text-align: center;
      padding: 10px 0;
    }

    /* Media Queries for Responsiveness */

    /* Mobile (default) */
    @media (max-width: 600px) {
      .navbar ul {
        flex-direction: column;
        align-items: center;
      }

      .content {
        flex-direction: column;
        align-items: center;
      }

      .left, .right {
        width: 100%;
        margin-bottom: 20px;
      }
    }

    /* Tablet */
    @media (max-width: 900px) {
      .content {
        flex-direction: column;
        align-items: center;
      }

      .left, .right {
        width: 100%;
      }
    }

    /* Desktop (optional) */
    @media (min-width: 1200px) {
      .content {
        justify-content: space-between;
      }

      .left, .right {
        width: 45%;
      }
    }
  </style>
</head>
<body>
  <header>
    <nav class="navbar">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Services</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="content">
      <div class="left">
        <h1>Welcome to Our Website</h1>
        <p>This is an example of a responsive layout using Flexbox.</p>
      </div>
      <div class="right">
        <h2>Our Services</h2>
        <p>We offer great services to help you grow your business.</p>
      </div>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 Responsive Design Example</p>
  </footer>
</body>
</html>
