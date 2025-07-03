# Final Project and Deployment

## Objectives
Build a fully functional web application.
Apply HTML, CSS, and JavaScript concepts learned.
Deploy the project using GitHub Pages, Netlify, or Vercel.

## Instructions
Choose one of the following project ideas:
Blog Website: Implement a multi-page site with navigation.
Ecommerce Website: Implement a multi-page site with navigation.

>[!NOTE]
> - Include at least:
> - A responsive design.
> - JavaScript interactivity.
> - A deployment link.

## Tasks

Create a well-structured HTML5 document.
Use at least 5 different HTML elements.
Ensure semantic correctness.

Good luck and happy coding! 🚀💻
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Awesome Blog - Home</title>
    <!-- Link to the external CSS file for styling -->
    <link rel="stylesheet" href="style.css">
    <!-- Font Awesome for icons (e.g., hamburger menu) -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header class="site-header">
        <div class="header-content container">
            <a href="index.html" class="site-logo">MyBlog</a>
            <button class="menu-toggle" aria-label="Toggle navigation">
                <i class="fas fa-bars"></i>
            </button>
            <nav class="main-nav">
                <ul>
                    <li><a href="index.html">Home</a></li>
                    <li><a href="about.html">About</a></li>
                    <li><a href="contact.html">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main class="container">
        <section class="blog-posts-list">
            <h1>Recent Articles</h1>

            <article class="blog-post-summary">
                <img src="https://placehold.co/600x300/E0F2F7/000000?text=Web+Design" alt="Abstract web design illustration" class="post-image">
                <h2><a href="post.html">The Future of Responsive Web Design</a></h2>
                <p class="post-meta">Published on <time datetime="2025-07-03">July 3, 2025</time> by Jane Doe</p>
                <p>Responsive web design continues to evolve, adapting to an ever-growing array of devices and screen sizes. This article explores the latest trends and techniques shaping the future of web development...</p>
                <a href="post.html" class="read-more">Read More &rarr;</a>
            </article>

            <article class="blog-post-summary">
                <img src="https://placehold.co/600x300/FFF3E0/000000?text=JavaScript+Tips" alt="Code snippets on a screen" class="post-image">
                <h2><a href="post.html">Mastering JavaScript Closures</a></h2>
                <p class="post-meta">Published on <time datetime="2025-06-28">June 28, 2025</time> by John Smith</p>
                <p>Closures are a fundamental concept in JavaScript that can be tricky to grasp initially. This deep dive will demystify closures, showing practical examples and common use cases...</p>
                <a href="post.html" class="read-more">Read More &rarr;</a>
            </article>

            <article class="blog-post-summary">
                <img src="https://placehold.co/600x300/E8F5E9/000000?text=CSS+Grids" alt="Grid layout lines" class="post-image">
                <h2><a href="post.html">CSS Grid vs. Flexbox: When to Use Which</a></h2>
                <p class="post-meta">Published on <time datetime="2025-06-20">June 20, 2025</time> by Alice Johnson</p>
                <p>Both CSS Grid and Flexbox are powerful layout modules, but understanding their strengths helps in choosing the right tool for the job. We'll compare them side-by-side...</p>
                <a href="post.html" class="read-more">Read More &rarr;</a>
            </article>
        </section>
    </main>

    <footer class="site-footer">
        <div class="container">
            <p>&copy; 2025 My Awesome Blog. All rights reserved.</p>
            <nav class="footer-nav">
                <ul>
                    <li><a href="#">Privacy Policy</a></li>
                    <li><a href="#">Terms of Service</a></li>
                </ul>
            </nav>
        </div>
    </footer>

    <script>
        // JavaScript for mobile navigation toggle
        document.addEventListener('DOMContentLoaded', function() {
            const menuToggle = document.querySelector('.menu-toggle');
            const mainNav = document.querySelector('.main-nav');

            menuToggle.addEventListener('click', function() {
                mainNav.classList.toggle('active');
                // Toggle the icon between bars and times (X)
                const icon = menuToggle.querySelector('i');
                if (mainNav.classList.contains('active')) {
                    icon.classList.remove('fa-bars');
                    icon.classList.add('fa-times');
                } else {
                    icon.classList.remove('fa-times');
                    icon.classList.add('fa-bars');
                }
            });

            // Close nav when a link is clicked (for single-page feel on mobile)
            mainNav.querySelectorAll('a').forEach(link => {
                link.addEventListener('click', () => {
                    if (mainNav.classList.contains('active')) {
                        mainNav.classList.remove('active');
                        menuToggle.querySelector('i').classList.remove('fa-times');
                        menuToggle.querySelector('i').classList.add('fa-bars');
                    }
                });
            });
        });
    </script>
</body>
</html>
