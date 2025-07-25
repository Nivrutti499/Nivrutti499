# Hi 👋, I'm Nivrutti Chaudhari  
**B.E. ENTC Student | Web Developer | Tech Explorer**

---

## 👨‍🎓 About Me  
🎓 I'm pursuing **B.E. in Electronics & Telecommunication** at **Sinhgad College of Engineering, Pune**  
🌐 I enjoy developing **web applications** that solve real-world problems  
💡 Passionate about learning **modern tech stacks** and enhancing my coding skills  
🌱 Currently learning **new technologies** and exploring **open source contributions**

---

## 🛠️ Tech Stack & Tools  
`HTML5`, `CSS3`, `JavaScript`, `React.js`, `Java`, `Python`, `Git`, `GitHub`, `C++`, `MySQL`

---

## 🌐 index.html

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Nivrutti Chaudhari | Web Developer</title>
  <canvas id="stars"></canvas>
  <link rel="stylesheet" href="style.css" />
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code&display=swap" rel="stylesheet">
</head>
<body>
  <div class="container">
    <h1>Hi 👋, I'm Nivrutti Chaudhari</h1>
    <h2>B.E. ENTC Student | Web Developer | Tech Explorer</h2>
    <div class="typing-container">
      <span id="typed-text"></span>
    </div>
    <section class="about">
      <h3>👨‍🎓 About Me</h3>
      <ul>
        <li>🎓 I'm pursuing <strong>B.E. in Electronics & Telecommunication</strong> at Sinhgad College of Engineering, Pune.</li>
        <li>🌐 I enjoy developing <strong>web applications</strong> that solve real-world problems.</li>
        <li>💡 Always exploring <strong>new technologies</strong> and improving my development skills.</li>
        <li>🌱 Currently learning <strong>New Technologies</strong>.</li>
      </ul>
    </section>
    <section class="stack">
      <h3>🛠️ Tech Stack & Tools</h3>
      <div class="stack-list">
        <span>HTML5</span><span>CSS3</span><span>JavaScript</span><span>React.js</span><span>Java</span>
        <span>Python</span><span>Git</span><span>GitHub</span><span>C++</span><span>MySQL</span>
      </div>
    </section>
    <section class="contact">
      <h3>📫 Connect With Me</h3>
      <p>📧 Email: <a href="mailto:chaudharinivrutti@gmail.com">chaudharinivrutti@gmail.com</a></p>
      <p>🔗 GitHub: <a href="https://github.com/nivruttichaudhari">github.com/nivruttichaudhari</a></p>
      <p>🔗 LinkedIn: <a href="https://linkedin.com/in/nivruttichaudhari">linkedin.com/in/nivruttichaudhari</a></p>
    </section>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

---

## 🎨 style.css

```css
body {
  margin: 0;
  padding: 0;
  font-family: 'Fira Code', monospace;
  background-color: #0f172a;
  color: #e2e8f0;
  overflow-x: hidden;
}

.container {
  max-width: 900px;
  margin: auto;
  padding: 2rem;
  text-align: center;
  animation: fadeIn 1.5s ease-in;
}

h1 {
  font-size: 2.8rem;
  color: #38bdf8;
  animation: slideDown 1s ease-in-out;
}

h2 {
  font-size: 1.4rem;
  color: #94a3b8;
  margin-top: 0.5rem;
  animation: slideUp 1.2s ease-in-out;
}

.typing-container {
  margin: 1.5rem 0;
  font-size: 1.2rem;
  color: #22d3ee;
  height: 30px;
  text-shadow: 0 0 5px #22d3ee;
  animation: glow 2s infinite alternate;
}

section {
  margin-top: 3rem;
  text-align: left;
  background-color: #1e293b;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.4);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  animation: fadeUp 1.2s ease-in-out;
}

section:hover {
  transform: scale(1.02);
  box-shadow: 0 6px 16px rgba(0,0,0,0.6);
}

.about ul {
  list-style: none;
  padding-left: 0;
  line-height: 1.8;
}

.stack-list {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 1rem;
}

.stack-list span {
  background-color: #0f172a;
  padding: 10px 14px;
  border-radius: 8px;
  font-size: 0.95rem;
  border: 1px solid #334155;
  transition: 0.3s ease;
}

.stack-list span:hover {
  background-color: #334155;
  color: #38bdf8;
}

a {
  color: #38bdf8;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes slideDown {
  from { transform: translateY(-40px); opacity: 0; }
  to { transform: translateY(0); opacity: 1; }
}

@keyframes slideUp {
  from { transform: translateY(40px); opacity: 0; }
  to { transform: translateY(0); opacity: 1; }
}

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(40px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes glow {
  from {
    text-shadow: 0 0 10px #22d3ee, 0 0 20px #22d3ee;
  }
  to {
    text-shadow: 0 0 20px #38bdf8, 0 0 30px #38bdf8;
  }
}
```

---

## ⚙️ script.js

```js
const textArray = [
  "Passionate Web Developer",
  "Tech Explorer 🚀",
  "Lifelong Learner 📚",
  "Open to Opportunities"
];

let currentIndex = 0;
let charIndex = 0;
const typingSpeed = 100;
const eraseDelay = 1200;
const typingElement = document.getElementById("typed-text");

function type() {
  if (charIndex < textArray[currentIndex].length) {
    typingElement.textContent += textArray[currentIndex].charAt(charIndex);
    charIndex++;
    setTimeout(type, typingSpeed);
  } else {
    setTimeout(erase, eraseDelay);
  }
}

function erase() {
  if (charIndex > 0) {
    typingElement.textContent = textArray[currentIndex].substring(0, charIndex - 1);
    charIndex--;
    setTimeout(erase, typingSpeed / 2);
  } else {
    currentIndex = (currentIndex + 1) % textArray.length;
    setTimeout(type, typingSpeed);
  }
}

document.addEventListener("DOMContentLoaded", () => {
  if (textArray.length) setTimeout(type, 500);
});

const canvas = document.getElementById("stars");
if (canvas) {
  const ctx = canvas.getContext("2d");
  let stars = [];
  const starCount = 100;

  canvas.width = window.innerWidth;
  canvas.height = window.innerHeight;

  for (let i = 0; i < starCount; i++) {
    stars.push({
      x: Math.random() * canvas.width,
      y: Math.random() * canvas.height,
      radius: Math.random() * 1.5,
      speed: Math.random() * 0.5 + 0.1,
    });
  }

  function drawStars() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    ctx.fillStyle = "#ffffff";
    stars.forEach(star => {
      ctx.beginPath();
      ctx.arc(star.x, star.y, star.radius, 0, 2 * Math.PI);
      ctx.fill();
    });
    moveStars();
  }

  function moveStars() {
    stars.forEach(star => {
      star.y += star.speed;
      if (star.y > canvas.height) {
        star.y = 0;
        star.x = Math.random() * canvas.width;
      }
    });
  }

  function animateStars() {
    drawStars();
    requestAnimationFrame(animateStars);
  }

  animateStars();

  window.addEventListener("resize", () => {
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
  });

  canvas.style.position = "fixed";
  canvas.style.top = 0;
  canvas.style.left = 0;
  canvas.style.zIndex = "-1";
}
```
