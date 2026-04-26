# Ex01 Portfolio
## Date:26\4\26

## AIM
To create a Portfolio using HTML and CSS.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for introduction, about, projects, and contact details.

### STEP 5
Define global styles for fonts, colors, and layout.

### STEP 6
Style the header, navigation bar, and sections.

### STEP 7
Use Flexbox or CSS Grid for layout design.

### STEP 8
Add hover effects and transitions for interactivity.

### STEP 9
Add Images and Media.

### STEP 10
Use optimized images for a professional look.

### STEP 11
Open the HTML file in a browser to check layout and functionality.

### STEP 12
Fix styling issues and refine content placement.

### STEP 13
Deploy the Portfolio.

### STEP 14
Upload to GitHub Pages for free hosting.

## PROGRAM
portfolio.html
```
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Samritha Portfolio</title>
<link rel="stylesheet" href="style.css">
</head>

<body>

<header>
    <h2 class="logo">SAMRITHA</h2>
    <nav>
        <a href="#" onclick="showSection('home')">Home</a>
        <a href="#" onclick="showSection('about')">About</a>
        <a href="#" onclick="showSection('projects')">Projects</a>
        <a href="#" onclick="showSection('contact')">Contact</a>
    </nav>
</header>

<!-- ================= HOME ================= -->
<section id="home" class="content-section active">
    <div class="home">
        <div class="left">
            <img src="images/sam.jpeg">
        </div>

        <div class="right">
            <h1>My <br> Portfolio</h1>
            <p>I'm Samritha, a B.E CSE student passionate about web development<br>
             and creating modern user interfaces.</p>
        </div>
    </div>
</section>

<!-- ================= ABOUT ================= -->
<section id="about" class="content-section">
    <div class="about-container">

        <h1 class="title">About Me</h1>

        <div class="info-box">
            <h2>Education</h2>
            <p>Hi, I'm Samritha, A B.E Computer Science Engineering student at 
            Saveetha Engineering College. I am passionate about web development and continuously
             improving my technical skills.</p>
        </div>

        <div class="info-box">
            <h2>Skills</h2>
            <ul>
            <p>C Programming, Python</p>
            <p>Web Development, MySQL</p>
            <p>Team Management</p>
        </ul>
        </div>

        <div class="info-box">
            <h2>Internship</h2>
            <p>AI Internship at Appotect</p>
        </div>

    </div>
</section>

<!-- ================= PROJECTS ================= -->
<section id="projects" class="content-section">
    <div class="projects-container">

        <h1 class="title">My Projects</h1>

        <div class="projects-grid">

            <div class="project-card">
                <h2>EmotionTrack</h2>
                <p>Tracks and visualizes user sentiment trends 
                    from social media or review data using sentiment 
                    analysis techniques.</p>
                    <br>
                <span>Python</span>
            </div>

            <div class="project-card">
                <h2>Student Form</h2>
                <p> A responsive form created using HTML and CSS for collecting 
                student details.</p>
                <br>
                <span>HTML | CSS</span>
            </div>

            <div class="project-card">
                <h2>Portfolio</h2>
                <p>Personal portfolio website to showcase skills, projects, and contact details.</p>
                <br>
                <span>HTML | CSS</span>
            </div>

        </div>

    </div>
</section>

<!-- ================= CONTACT ================= -->
<section id="contact" class="content-section">
    <div class="contact-hero">
        <h1>Contact Me</h1>
    </div>

    <div class="contact-details">
        <p>Email: samritha@gmail.com</p>
        <p>Phone: +91 1234567899</p>
        <p>Location: Chennai, India</p>
    </div>
</section>

<!-- ================= JS ================= -->
<script>
function showSection(id) {
    document.querySelectorAll('.content-section').forEach(sec => {
        sec.style.display = "none";
    });

    document.getElementById(id).style.display = "block";
}
</script>

</body>
</html>
```

style.css
```
/* RESET */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

/* HEADER */
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 50px;
    background: #222;
    color: white;
}

.logo {
    font-size: 22px;
    font-weight: bold;
}

nav a {
    color: white;
    margin-left: 25px;
    text-decoration: none;
    font-size: 15px;
    transition: 0.3s;
    cursor: pointer;
}

nav a:hover {
    color: #00ffff;
}

/* SECTION CONTROL (JS) */
.content-section {
    display: none;
    min-height: 100vh;
}

.content-section.active {
    display: block;
}

/* ================= HOME ================= */

.home {
    display: flex;
    height: 90vh;
}

/* LEFT IMAGE */
.left {
    width: 50%;
}

.left img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

/* RIGHT CONTENT */
.right {
    width: 50%;
    background: #111;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    padding: 120px 60px;
}

.right h1 {
    font-size: 60px;
    margin-bottom: 20px;
}

.right p {
    color: #ccc;
    line-height: 1.6;
}

/* ================= ABOUT ================= */

.about-container {
    background: #111;
    color: white;
    padding: 60px;
    text-align: center;
}

.title {
    font-size: 45px;
    margin-bottom: 40px;
}

/* CARD */
.about-card {
    background: #1c1c1c;
    padding: 30px;
    border-radius: 10px;
    max-width: 600px;
    margin: 20px auto;
    box-shadow: 0 0 15px rgba(0,0,0,0.5);
}

/* INFO BOX */
.info-box {
    background: #1c1c1c;
    margin: 20px auto;
    padding: 25px;
    max-width: 600px;
    border-radius: 10px;
}

.info-box h2 {
    margin-bottom: 10px;
}

.info-box p {
    color: #ccc;
}

/* ================= PROJECTS ================= */

.projects-container {
    background: #111;
    color: white;
    padding: 80px 20px;
    text-align: center;
}

.projects-grid {
    display: flex;
    justify-content: center;
    gap: 30px;
    flex-wrap: wrap;
}

/* CARD */
.project-card {
    background: #1c1c1c;
    padding: 25px;
    width: 280px;
    border-radius: 10px;
    box-shadow: 0 0 15px rgba(0,0,0,0.5);
    transition: 0.3s;
}

.project-card h2 {
    margin-bottom: 10px;
}

.project-card p {
    font-size: 14px;
    color: #ccc;
}

.project-card span {
    font-size: 13px;
    color: #00ffff;
}

/* HOVER */
.project-card:hover {
    transform: translateY(-10px);
}

/* ================= CONTACT ================= */

.contact-hero {
    background: #1c1c1c;
    color: white;
    text-align: center;
    padding: 80px 20px;
}

.contact-hero h1 {
    font-size: 50px;
}

/* DETAILS */
.contact-details {
    background: #111;
    color: white;
    text-align: center;
    padding: 50px;
}

.contact-details p {
    margin: 10px 0;
    font-size: 16px;
    color: #ccc;
}

/* ================= RESPONSIVE ================= */

@media (max-width: 768px) {

    .home {
        flex-direction: column;
    }

    .left, .right {
        width: 100%;
        height: 50vh;
    }

    .right {
        padding: 40px;
    }

    .right h1 {
        font-size: 40px;
    }

    nav {
        font-size: 12px;
    }
}

```


## OUTPUT
<img width="1885" height="1114" alt="image" src="https://github.com/user-attachments/assets/32c78d84-9aff-4ea4-a4b0-e35066bef182" />
<img width="1883" height="1117" alt="image" src="https://github.com/user-attachments/assets/f8885758-3883-4f16-a3da-a94d9be365e6" />
<img width="1881" height="1127" alt="image" src="https://github.com/user-attachments/assets/52e41a9d-f758-4579-b647-cb6a10463e3c" />
<img width="1881" height="1123" alt="image" src="https://github.com/user-attachments/assets/a802ffc1-878f-4478-b9c0-0b3b36ff7cd2" />




## RESULT
The program for creating Portfolio using HTML and CSS is executed successfully.
