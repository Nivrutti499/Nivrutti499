## 📄 index.html
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
        <span>HTML5</span>
        <span>CSS3</span>
        <span>JavaScript</span>
        <span>React.js</span>
        <span>Java</span>
        <span>Python</span>
        <span>Git</span>
        <span>GitHub</span>
        <span>C++</span>
        <span>MySQL</span>
      </div>
    </section>
    <section class="contact">
      <h3>📫 Connect With Me</h3>
      <p>📧 Email: <a href="mailto:chaudharinivrutti@gmail.com">chaudharinivrutti@gmail.com</a></p>
      <p>🔗 GitHub: <a href="https://github.com/nivruttichaudhari" target="_blank">github.com/nivruttichaudhari</a></p>
      <p>🔗 LinkedIn: <a href="https://linkedin.com/in/nivruttichaudhari" target="_blank">linkedin.com/in/nivruttichaudhari</a></p>
    </section>
  </div>
  <script src="script.js"></script>
</body>
</html>
```

## 🎨 style.css
```css
body {
  margin: 0;
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
}
.typing-container {
  margin: 1.5rem 0;
  font-size: 1.2rem;
  color: #22d3ee;
  height: 30px;
  animation: glow 2s infinite alternate;
}
.stack-list {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}
.stack-list span {
  background-color: #334155;
  padding: 10px 14px;
  border-radius: 8px;
  font-size: 0.95rem;
  border: 1px solid #0f172a;
}
@keyframes glow {
  from {
    text-shadow: 0 0 10px #22d3ee;
  }
  to {
    text-shadow: 0 0 20px #38bdf8;
  }
}
```

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
const typingElement = document.getElementById("typed-text");

function type() {
  if (charIndex < textArray[currentIndex].length) {
    typingElement.textContent += textArray[currentIndex].charAt(charIndex);
    charIndex++;
    setTimeout(type, 100);
  } else {
    setTimeout(erase, 1200);
  }
}

function erase() {
  if (charIndex > 0) {
    typingElement.textContent = textArray[currentIndex].substring(0, charIndex - 1);
    charIndex--;
    setTimeout(erase, 60);
  } else {
    currentIndex = (currentIndex + 1) % textArray.length;
    setTimeout(type, 100);
  }
}

document.addEventListener("DOMContentLoaded", () => {
  if (textArray.length) setTimeout(type, 500);
});
```
