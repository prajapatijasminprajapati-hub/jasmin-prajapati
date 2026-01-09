<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jasmin Prajapati | Portfolio</title>

<!-- Google Font -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
:root{
  --main:#4f46e5;
  --bg:#0f172a;
  --card:#1e293b;
  --text:#e5e7eb;
  --soft:#94a3b8;
}

*{margin:0;padding:0;box-sizing:border-box;font-family:'Poppins',sans-serif}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--text)}

/* Navbar */
nav{
  position:fixed;
  top:0;
  width:100%;
  background:rgba(15,23,42,0.9);
  backdrop-filter:blur(10px);
  padding:15px;
  z-index:1000;
}
nav ul{
  display:flex;
  justify-content:center;
  gap:25px;
  list-style:none;
}
nav a{
  color:var(--text);
  text-decoration:none;
  font-weight:500;
  transition:.3s;
}
nav a:hover{color:var(--main)}

/* Section */
section{
  min-height:100vh;
  padding:100px 10%;
  display:flex;
  flex-direction:column;
  justify-content:center;
}
h1,h2{color:white}
h2{margin-bottom:20px}

/* Hero */
.hero{
  text-align:center;
}
.hero h1{
  font-size:3rem;
  animation:zoom 1s ease;
}
.hero span{color:var(--main)}
.hero p{
  margin-top:15px;
  color:var(--soft);
  animation:fadeUp 1.5s ease;
}

/* Cards */
.card{
  background:var(--card);
  padding:25px;
  border-radius:15px;
  margin-bottom:20px;
  transition:.4s;
}
.card:hover{
  transform:translateY(-10px) scale(1.02);
  box-shadow:0 15px 40px rgba(79,70,229,.3);
}

/* Skills */
.skills{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
  gap:20px;
}

/* Contact */
.contact-box{
  background:var(--card);
  padding:30px;
  border-radius:20px;
  animation:fadeUp 1.2s ease;
}
input,textarea{
  width:100%;
  margin-bottom:15px;
  padding:12px;
  border:none;
  border-radius:10px;
  background:#020617;
  color:white;
}
button{
  background:var(--main);
  border:none;
  padding:12px 25px;
  border-radius:30px;
  color:white;
  cursor:pointer;
  font-weight:600;
  transition:.3s;
}
button:hover{transform:scale(1.1)}

/* Animations */
@keyframes fadeUp{
  from{opacity:0;transform:translateY(30px)}
  to{opacity:1;transform:translateY(0)}
}
@keyframes zoom{
  from{opacity:0;transform:scale(.7)}
  to{opacity:1;transform:scale(1)}
}

/* Responsive */
@media(max-width:768px){
  section{padding:100px 5%}
  .hero h1{font-size:2.2rem}
}
</style>
</head>

<body>

<nav>
  <ul>
    <li><a href="#home">Home</a></li>
    <li><a href="#about">Introduction</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<section class="hero" id="home">
  <h1>Hi, I'm <span>Jasmin Prajapati</span></h1>
  <p>BCA Student | Information Technology</p>
</section>

<section id="about">
  <h2>Introduction</h2>
  <div class="card">
    My name is Jasmin Prajapati, and I am currently a Bachelor of Computer Applications (BCA) student specializing in Information Technology. I am actively developing my technical skills and gaining a strong foundation in computer applications, programming concepts, and modern IT tools. This portfolio represents my academic journey and dedication toward building a successful IT career.
  </div>
</section>

<section id="education">
  <h2>Education</h2>

  <div class="card">
    <b>2024 - Present</b><br>
    Bachelor of Computer Applications (BCA)<br>
    School of Commerce
  </div>

  <div class="card">
    <b>10th & 12th (GSEB Board)</b><br>
    Completed under Gujarat Secondary and Higher Secondary Education Board.
  </div>

  <div class="card">
    <b>2024 - Present</b><br>
    Web & Computer Skills – Digital Academy<br>
    Learning HTML, C++, CCC, Excel (Beginner Level)
  </div>
</section>

<section id="skills">
  <h2>Personal Skills</h2>
  <div class="skills">
    <div class="card">Back-End Support</div>
    <div class="card">Quick Learner</div>
    <div class="card">Time Management</div>
    <div class="card">Writing</div>
    <div class="card">Problem Solving</div>
    <div class="card">Team Collaboration</div>
    <div class="card">Adaptability</div>
    <div class="card">Communication</div>
    <div class="card">Self Motivated</div>
  </div>
</section>

<section id="contact">
  <h2>Let's Work Together</h2>
  <div class="contact-box">
    <p>Email: <b>prajapatijasminprajapati@gmail.com</b></p>
    <p>Phone: <b>+91 99987 75318</b></p>
    <p>Location: Chandlodia, Ahmedabad</p>

    <br>
    <input type="text" id="name" placeholder="Your Name">
    <textarea id="message" rows="4" placeholder="Your Message"></textarea>
    <button onclick="sendMsg()">Send Message</button>
  </div>
</section>

<script>
function sendMsg(){
  let name=document.getElementById("name").value;
  let msg=document.getElementById("message").value;
  let text=`Hello, my name is ${name}. ${msg}`;
  let url=`https://wa.me/919998775318?text=${encodeURIComponent(text)}`;
  window.open(url,"_blank");
}
</script>

</body>
</html>
