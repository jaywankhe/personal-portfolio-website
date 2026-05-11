# personal-portfolio-website
Features Animated Background Dark/Light Mode Toggle Skills Section Project Cards Responsive Design Hover Effects
Technologies
* HTML
* CSS
* JavaScript
<img width="1901" height="1022" alt="Screenshot 2026-05-11 190523" src="https://github.com/user-attachments/assets/73c0c231-9529-4d5b-8597-8f95dad77d4c" />
Code:- HTML:- <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jay Portfolio</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="background-animation"></div>

    <header>
        <h1>Jay Wankhede</h1>
        <p>BCA Graduate | Aspiring Software Developer</p>

        <button onclick="toggleMode()">!Dark Theme!</button>
    </header>

    <section>
        <h2>About Me</h2>
        <p>
            Passionate about Software Development,
            Cloud Computing, and Web Development.
             </p>
    </section>

    <section>
        <h2>Skills</h2>

        <div class="skills">
            <span>Java</span>
            <span>C</span>
            <span>SQL</span>
            <span>HTML</span>
            <span>CSS</span>
            <span>GitHub</span>
        </div>
    </section>

    <section>
        <h2>Projects</h2>

        <div class="card">
            <h3>Cloud Computing Project</h3>
            <p>Project based on cloud computing concepts.</p>
        </div>
          <div class="card">
            <h3>Student Management System</h3>
            <p>Java based student management application.</p>
        </div>
    </section>

    <section>
        <h2>Contact</h2>

        <p>Email: jay.s.w.321098@gmail.com</p>

        <p>
            GitHub:
            <a href="https://github.com/jaywankhe" target="_blank">
                github.com/jaywankhe
            </a>
        </p>
    </section>

    <script src="script.js"></script>

</body>
</html>

CSS:- {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background: #0f172a;
    color: white;
    overflow-x: hidden;
}

.background-animation {
    position: fixed;
    width: 100%;
    height: 100%;
    background: linear-gradient(45deg, #0f172a, #1e293b, #334155);
    background-size: 400% 400%;
    animation: gradientBG 10s ease infinite;
    z-index: -1;
}
@keyframes gradientBG {
    0% {
        background-position: 0% 50%;
    }
    50% {
        background-position: 100% 50%;
    }
    100% {
        background-position: 0% 50%;
    }
}

header {
    text-align: center;
    padding: 50px;
}

header h1 {
    font-size: 45px;
    margin-bottom: 10px;
}
button {
    margin-top: 20px;
    padding: 10px 20px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    font-weight: bold;
}

section {
    background: rgba(255,255,255,0.1);
    margin: 20px;
    padding: 25px;
    border-radius: 15px;
    backdrop-filter: blur(10px);
}

.skills span {
    display: inline-block;
    background: #38bdf8;
    color: black;
    padding: 10px 15px;
    border-radius: 20px;
    margin: 10px;
     font-weight: bold;
}

.card {
    background: rgba(255,255,255,0.15);
    padding: 20px;
    border-radius: 12px;
    margin-top: 15px;
    transition: 0.3s;
}

.card:hover {
    transform: scale(1.03);
}

a {
    color: #38bdf8;
    text-decoration: none;
}

Java:- function toggleMode() {

    document.body.classList.toggle("light-mode");

    if(document.body.classList.contains("light-mode")) {
        document.body.style.background = "#f4f4f4";
        document.body.style.color = "black";
    }
    else {
        document.body.style.background = "#0f172a";
        document.body.style.color = "white";
    }
}
