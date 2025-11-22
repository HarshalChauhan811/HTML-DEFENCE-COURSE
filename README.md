🌐 HTML Complete Notes – By Harshal Chauhan
Beginner to Advanced in One README
📘 Lecture 01 — HTML Basics
🔹 What is HTML?

HTML = HyperText Markup Language

HyperText → Linked pages

Markup → Tags give structure

🔹 First Website

No design, only text + links

Manual navigation

🔹 Setup

Install VS Code → Extensions: Live Server, Live Preview, Prettier

🔹 Core Tags

Headings: <h1>…<h6>

Paragraphs: <p>

Lists: <ul>, <ol>, <li>

Links: <a href="">

Images: <img src="" alt="">

Line breaks: <br>

Horizontal line: <hr>

🔹 BEST PRACTICES

Semantic hierarchy

Only one <h1>

Always add alt in images

📘 Lecture 02 — Nested Lists & Tables
🔹 Nested Lists
<ul>
  <li>Country
    <ul><li>City</li></ul>
  </li>
</ul>

🔹 Mixed Lists

UL inside OL

Unlimited levels

🔹 Tables (Basic)
<table>
  <tr><th>Name</th><th>Role</th></tr>
  <tr><td>Harshal</td><td>Frontend Dev</td></tr>
</table>

🔹 Professional Table

<thead> <tbody> <tfoot>

Use for SEO + structure

🔹 Advanced

colspan → merge columns

rowspan → merge rows

📘 Lecture 03 — File Paths, Boilerplate & DIV
🔹 Relative Paths (MOST USED)

Same folder → file.jpg

Go inside folder → images/logo.png

Go outside folder → ../logo.png

🔹 Absolute Paths

Full URL

Used only for external resources

🔹 HTML Boilerplate
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Document</title>
</head>
<body></body>
</html>

🔹 DIV, SPAN, CLASS, ID

<div> = block container

<span> = inline text wrapper

class = reusable

id = unique

🔹 Semantic Tags

header, main, footer, nav, section, article

📘 Lecture 04 — HTML Forms (Master Guide)
🔹 Form Structure
<form action="" method="POST"></form>

🔹 Input Types

text, password, email, number

date, file, color, range

radio → single choice

checkbox → multiple choices

🔹 MOST IMPORTANT RULES

id ↔ for → accessibility

name → backend data key

value → actual data sent

🔹 Select & Textarea
<select><option value=""></option></select>
<textarea rows="" cols=""></textarea>

🔹 Buttons

type="submit"

type="reset"

type="button"

🔹 Validation

required

pattern="[0-9]{10}"

🔹 Data Flow

Form → Browser → name=value → Backend → Database

📘 Lecture 05 — Media Tags, Multi-Page Sites & Deployment
🎥 Video Tag
<video src="" controls></video>


Autoplay requires muted

Add poster: poster="img.jpg"

🎵 Audio Tag
<audio src="" controls></audio>

🎬 Professional Video (Recommended)
<video controls>
  <source src="file.webm" type="video/webm">
  <source src="file.mp4" type="video/mp4">
</video>

🌍 YouTube Embed
<iframe src="https://www.youtube.com/embed/VIDEO_ID" allowfullscreen></iframe>

🗂 Multi-Page Website
index.html
about.html
contact.html
courses.html


All pages linked using:

<nav>
  <a href="index.html">Home</a>
</nav>

🚀 Deployment (Netlify)

Create account

Upload folder

Get live link

Done

© HTML Entities

© = &copy;

< = &lt;

= &gt;

🧠 HTML in One Table (Super Summary)
Concept	Tag	Purpose
Structure	html, head, body	Base of webpage
Headings	h1-h6	Hierarchy
Text	p, br, hr	Content
Media	img, video, audio	Visuals
Lists	ul, ol, li	Organised items
Links	a	Navigation
Tables	table, tr, td, th	Data display
Forms	form, input, select	User input
Layout	div, span	Grouping
Semantic	header, footer	Meaningful structure
Paths	relative/absolute	File linking
🎉 **Congratulations!

You Completed Full HTML (Beginner → Pro).**
Next: CSS Mastercourse 💥🔥
