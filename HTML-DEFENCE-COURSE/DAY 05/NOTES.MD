# **📹Lecture 05 — Deploy Your First Project | Media Tag | Multi Page Website**

Made By @Harshal Chauhan 

## **🎯 FIRST PRINCIPLE: Web Sirf Text & Images Nahin Hai**

### **⚡ Fundamental Truth**

- Webpage ko koi bhi content deliver karna chahiye - videos, audio, animations, etc.
- Pehle ye bahut bada problem tha 😥

### **🚫 Purana Problem: Third-Party Plugins**

- Pehle browsers ko chahiye hota tha:
    - 🔹 Adobe Flash
    - 🔹 QuickTime
    - 🔹 Silverlight

**Problems with Plugins:**

- ❌ Inefficient (Slow)
- ❌ Insecure (Security risks)
- ❌ Inconsistent (Har computer pe alag behavior)

---

## **🎯 CORE PROBLEM**

Kaise embed karein video/audio webpage mein **standardized, native, aur plugin-free** way mein?

**Requirements:**

- ✅ Har modern browser mein kaam kare
- ✅ Desktop se mobile tak same experience
- ✅ User ko kuch install nahi karna pade

---

## **💡 THE SOLUTION: HTML5 <video> & <audio> Tags**

Browser ne banaye dedicated tags media ke liye!

---

# **🎥 PART 1: VIDEO TAG BASICS**

## **🔹 Simplest Video Implementation**

html

```html
<!-- Basic video - sirf first frame dikhega, play nahi hoga -->
<video src="my-video.mp4"></video>
```

**❌ Problem:** Video frame toh dikhega but play/pause/volume controls nahi honge!

## **🔸 Solution: controls Attribute**

html

```html
<!-- Ye hai magic switch! -->
<video src="my-video.mp4" controls></video>
```

**✅ Result:** Ab milega complete video player with:

- ▶️ Play/Pause button
- ⏩ Timeline scrubber
- 🔊 Volume control
- 🖥 Fullscreen option

**💡 Tip:** `controls` ek **boolean attribute** hai - bas likh dena kaafi hai, `controls="true"` likhne ki zarurat nahi.

---

# **🎛 PART 2: ADVANCED VIDEO ATTRIBUTES**

## **🔹 Size Control - width & height**

html

```html
<!-- Exactly image tag ki tarah -->
<video src="video.mp4" width="640" height="360" controls></video>
```

## **🔸 Autoplay - Important Caveat!**

html

```html
<!-- ❌ Ye kaam nahi karega modern browsers mein -->
<video src="video.mp4" autoplay controls></video>

<!-- ✅ Ye kaam karega kyunki sound muted hai -->
<video src="video.mp4" autoplay muted controls></video>
```

**⚠️ CRITICAL RULE:** Modern browsers block karte hain autoplay with sound. Isliye **hamesha `muted` ke saath use karo**.

## **🔹 Other Useful Attributes**

- **🔁 loop:** Video khatam hone ke baad automatically restart ho jayega
- **🖼 poster:** Video play karne se pehle dikhne wala image (YouTube thumbnail ki tarah)

html

```html
<video src="video.mp4" poster="thumbnail.jpg" controls></video>
```

**🎯 Real Life Example:** Background videos ke liye `autoplay muted loop` use karo.

---

# **🔊 PART 3: AUDIO TAG**

## **🔹 Audio Player Basics**

html

```html
<p>Listen to our podcast:</p>
<audio src="audio/podcast.mp3" controls></audio>
```

**✅ Result:** Clean audio player milega with:

- ▶️ Play/Pause
- ⏩ Timeline
- 🔊 Volume control

**💡 Tip:** Audio tag bhi same attributes support karta hai - `autoplay`, `loop`, `muted`

---

# **🚀 PART 4: PROFESSIONAL LEVEL SOLUTIONS**

## **🎯 PROBLEM #1: Browser Format Compatibility**

**❌ Problem:** Har browser alag format prefer karta hai:

- Chrome: `.webm` (Modern format)
- Safari (iPhone): `.mp4` support karta hai
- Firefox: `.webm` prefer karta hai

**✅ Solution: <source> Element**

html

```html
<video controls poster="thumbnail.jpg">
  <!-- Browser top to bottom check karega - jo pehla support karega wohi play hoga -->
  <source src="videos/my-video.webm" type="video/webm">
  <source src="videos/my-video.mp4" type="video/mp4">
  
  <!-- Fallback text - agar browser video tag hi nahi samjhta -->
  Sorry, your browser doesn't support embedded videos.
</video>
```

**🧠 First Principle:** Browser list ko top se bottom check karta hai aur **pehla supported format play karta hai**.

## **🎯 PROBLEM #2: Accessibility**

**❒ Problem Types:**

- 🧏‍♂️ Deaf users audio nahi sun sakte
- 🏢 Noisy/quiet environments mein audio nahi sunai degi
- 🌍 Different language speakers ko translation chahiye

**✅ Solution: <track> Element**

html

```html
<video controls>
  <source src="video.webm" type="video/webm">
  <source src="video.mp4" type="video/mp4">

  <!-- 📝 English Captions - hearing impaired ke liye -->
  <track src="captions_en.vtt" kind="captions" srclang="en" label="English">

  <!-- 🈂 Spanish Subtitles - translation ke liye -->
  <track src="subtitles_es.vtt" kind="subtitles" srclang="es" label="Español">
</video>
```

### **🔍 Track Attributes Breakdown:**

| **Attribute** | **Purpose** | **Example** |
| --- | --- | --- |
| `src` | .vtt file ka path | `captions_en.vtt` |
| `kind` | Track type | `captions`/`subtitles` |
| `srclang` | Track language | `en` (English) |
| `label` | Menu mein dikhne wala name | `English` |

### **🎯 Track Types:**

- **📝 captions:** Dialogue + important sounds transcription
- **🈂 subtitles:** Different language translation
- **🎧 descriptions:** Visually impaired ke liye audio description

---

# **🔄 COMPARISON: TWO METHODS**

## **🆚 Method 1: <source> (Professional Way)**

html

```html
<video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Your browser does not support the video tag.
</video>
```

## **🆚 Method 2: src attribute (Simple Way)**

html

```html
<video src="a.mp4" controls></video>
```

### **📊 Comparison Table:**

| **Feature** | **<source> Method** | **src Method** |
| --- | --- | --- |
| **Browser Compatibility** | 🏆 **Excellent** | 😐 Limited |
| **Flexibility** | 🏆 High | 😐 Low |
| **Simplicity** | 😓 Complex | 🏆 Very Simple |
| **Fallback** | 🏆 Text fallback | ❌ No fallback |
| **Best For** | 🏆 Public websites | 😓 Internal projects |

**🎯 Conclusion:** Professional websites ke liye hamesha **<source> method** use karo!

---

# **🌐 YOUTUBE VIDEOS EMBED KARNA**

## **🔹 YouTube Video Embed Karne ka Best Tarika**

### **Step 1: YouTube Video ki ID Nikalo**

html

```html
<!-- Original YouTube URL: -->
https://www.youtube.com/watch?v=NGYp1zCBthk

<!-- Video ID: NGYp1zCBthk (last 11 characters) -->
```

### **Step 2: iframe mein Convert Karo**

html

```html
<iframe 
  src="https://www.youtube.com/embed/NGYp1zCBthk" 
  allowfullscreen>
</iframe>
```

**💡 Pro Tip:** YouTube pe jaake "Share" → "Embed" click karo, wahan se direct code mil jayega!

## **🔸 Advanced YouTube Embed Options**

html

```html
<iframe 
  width="560" 
  height="315" 
  src="https://www.youtube.com/embed/NGYp1zCBthk" 
  frameborder="0" 
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
  allowfullscreen>
</iframe>
```

**🎯 Real Life Example:** Apne course website mein YouTube tutorials embed kar sakte ho!

---

# **🏗️ MULTI-PAGE WEBSITE BANANA**

## **🔹 Basic Structure - Multiple HTML Files**

text

```
your-website/
├── index.html          (Home Page)
├── about.html          (About Us)
├── contact.html        (Contact Page)
└── courses.html        (Courses Page)
```

## **🔸 Navigation Menu Banana**

html

```html
<header>
  <h1>This is Our Home Page</h1>
  <nav>
    <ul>
      <li><a href="index.html">Home</a></li>
      <li><a href="about.html">About Us</a></li>
      <li><a href="courses.html">Courses</a></li>
      <li><a href="contact.html">Contact</a></li>
    </ul>
  </nav>
</header>
```

## **🔹 Complete Page Structure Example**

html

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Home Page - Our Website</title>
</head>
<body>
    <!-- Header Section -->
    <header>
        <h1>This is Our Home Page</h1>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="about.html">About Us</a></li>
                <li><a href="courses.html">Courses</a></li>
                <li><a href="contact.html">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Main Content Section -->
    <main>
        <h2>This is Our Course Selling Website</h2>
        <img src="images/course-image.jpg" alt="Course Image" width="500">
        
        <!-- Video Integration -->
        <video width="400" controls>
            <source src="videos/intro.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </main>

    <!-- Footer Section -->
    <footer>
        <p>Copyright &copy; 2024 My Awesome Website. All Rights Reserved.</p>
    </footer>
</body>
</html>
```

---

# **📧 CONTACT PAGE BANANA**

## **🔹 Contact Form with Basic Structure**

html

```html
<!-- contact.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Contact Us</title>
</head>
<body>
    <header>
        <h1>Contact Us</h1>
        <!-- Same navigation menu as index.html -->
    </header>

    <main>
        <h2>You Can Connect With Us Directly</h2>
        <img src="images/contact-image.jpg" alt="Contact Image" width="300">
        
        <br><br>
        
        <!-- Contact Form -->
        <form>
            <label for="name">Your Name:</label>
            <input type="text" id="name" name="name">
            
            <br><br>
            
            <label for="phone">Your Phone Number:</label>
            <input type="tel" id="phone" name="phone">
            
            <br><br>
            
            <button type="submit">Submit</button>
        </form>
    </main>

    <footer>
        <p>Copyright &copy; 2024 My Website. All Rights Reserved.</p>
    </footer>
</body>
</html>
```

---

# **🎓 COURSES PAGE BANANA**

## **🔹 Courses Page with YouTube Videos**

html

```html
<!-- courses.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Our Courses</title>
</head>
<body>
    <header>
        <h1>Our Courses</h1>
        <!-- Navigation Menu -->
    </header>

    <main>
        <h2>Web Development Free Videos</h2>
        
        <!-- Table for organizing multiple videos -->
        <table>
            <tr>
                <td>
                    <iframe width="300" height="200" 
                            src="https://www.youtube.com/embed/video_id_1" 
                            allowfullscreen>
                    </iframe>
                </td>
                <td>
                    <iframe width="300" height="200" 
                            src="https://www.youtube.com/embed/video_id_2" 
                            allowfullscreen>
                    </iframe>
                </td>
            </tr>
            <tr>
                <td>
                    <iframe width="300" height="200" 
                            src="https://www.youtube.com/embed/video_id_3" 
                            allowfullscreen>
                    </iframe>
                </td>
                <td>
                    <iframe width="300" height="200" 
                            src="https://www.youtube.com/embed/video_id_4" 
                            allowfullscreen>
                    </iframe>
                </td>
            </tr>
        </table>
    </main>

    <footer>
        <p>Copyright &copy; 2024 My Website. All Rights Reserved.</p>
    </footer>
</body>
</html>
```

---

# **🚀 WEBSITE DEPLOY KARNA (NETLIFY)**

## **🔹 Step-by-Step Deployment Process**

### **Step 1: Netlify Account Banao**

- 🌐 [Netlify.com](https://netlify.com/) pe jao
- 📝 Sign up with Google/GitHub

### **Step 2: Project Upload Karo**

bash

```bash
1. "Add new project" click karo
2. "Deploy manually" choose karo
3. Apna project folder upload karo
4. "Deploy site" click karo
```

### **Step 3: Custom Domain Set Karo (Optional)**

bash

```bash
1. "Site settings" mein jao
2. "Domain management" choose karo
3. Apna custom domain add karo
```

**✅ Result:** Tumhare paas milega live website link jo koi bhi access kar sakta hai!

## **🔸 Netlify Deployment Benefits**

- 🆓 **FREE** hosting
- 🔒 **Automatic HTTPS** security
- ⚡ **Fast** loading speed
- 📱 **Mobile-friendly**
- 🔄 **Easy updates** - just re-upload

---

# **©️ HTML ENTITIES - SPECIAL SYMBOLS**

## **🔹 Copyright Symbol Banane ke Do Tarike:**

### **1. Entity Name (Recommended)**

html

```html
<footer>
  <p>Copyright &copy; 2024 My Website. All Rights Reserved.</p>
</footer>
```

### **2. Entity Number**

html

```html
<footer>
  <p>Copyright &#169; 2024 My Website. All Rights Reserved.</p>
</footer>
```

**✅ Dono same result denge:** Copyright © 2024 My Website

## **📋 Common HTML Entities:**

| **Symbol** | **Description** | **Entity Name** | **Entity Number** |
| --- | --- | --- | --- |
| © | Copyright | `&copy;` | `&#169;` |
| ® | Registered Trademark | `&reg;` | `&#174;` |
| ™ | Trademark | `&trade;` | `&#8482;` |
| < | Less-than | `&lt;` | `&#60;` |
| > | Greater-than | `&gt;` | `&#62;` |
| & | Ampersand | `&amp;` | `&#38;` |

**💡 Important:** `<` aur `>` ko entities ki zarurat kyun? Kyunki browser inhe HTML tags samajh leta hai! Agar `<>` display karna hai toh `&lt;&gt;` likhna padega.

---

# **💡 PRACTICAL PROJECT IDEAS**

## **🏋️‍♂️ Gym Website Project Structure**

text

```coffeescript
gym-website/
├── index.html      (Home - Gym services)
├── diet.html       (Diet information)
├── exercises.html  (Exercise routines)
└── contact.html    (Contact details)
```

## **🎓 Course Selling Website**

text

```objectivec
course-website/
├── index.html      (Home - All courses)
├── web-dev.html    (Web Development course)
├── dsa.html        (DSA course)
└── contact.html    (Enrollment form)
```

---

# **📚 POWERFUL SUMMARY**

## **🎯 Key Takeaways:**

1. **🌐 First Principle:** Web multimedia-friendly hona chahiye - plugins se chhutkara mila
2. **🎥 Video Tag:** `controls` attribute se player milta hai
3. **🔊 Audio Tag:** Video ki tarah hi kaam karta hai
4. **⚡ Attributes:**
    - `autoplay muted` - sound ke saath autoplay blocked
    - `poster` - thumbnail set karta hai
    - `loop` - video repeat karta hai
5. **🏆 Professional Method:**
    - `<source>` - multiple formats ke liye
    - `<track>` - accessibility ke liye (captions/subtitles)
6. **📺 YouTube Embedding:**
    - `iframe` use karo
    - Video ID extract karo
    - `youtube.com/embed/VIDEO_ID` pattern follow karo
7. **🏗️ Multi-Page Website:**
    - Multiple HTML files banao
    - Navigation menu se connect karo
    - Consistent header/footer rakho
8. **🚀 Deployment:**
    - Netlify pe FREE deploy karo
    - Live link share karo doston ke saath
9. **©️ Entities:** Special symbols ke liye `&copy;` jaise codes

## **🚀 Pro Tips:**

- Public website banate time hamesha `<source>` method use karo
- Autoplay ke liye `muted` attribute zaroor add karo
- Accessibility ke liye captions zaroor provide karo
- Multiple formats provide karke maximum compatibility achieve karo
- Netlify pe deploy karke apni website duniya ko dikhao

## **🎉 FINAL ACHIEVEMENT:**

**Ab aap ek complete web developer ki tarah soch sakte ho!**

- ✅ Media embed kar sakte ho
- ✅ Multi-page website bana sakte ho
- ✅ Live internet pe deploy kar sakte ho
- ✅ Professional websites create kar sakte ho

**🎊 Congratulations! Aapne HTML complete kar liya! Ab CSS ki journey shuru hogi!**