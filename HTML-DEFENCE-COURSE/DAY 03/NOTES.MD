# 🌟 HTML Lecture 03 - **File Path in HTML | HTML BoilerPlate Code | DIV + Class + ID** 🌟

Made By @Harshal Chauhan

## 📁 **1. FILE PATH SYSTEM – Poori Samajh**

### 🔹 **Pehla Principle (Fundamental Truth)**

Website ek single file nahi hoti — balki HTML, CSS, Images, JS jaise multiple files ka collection hoti hai.

Ye files folders me exactly waise hi arranged hoti hain jaise aapke computer me hoti hain.

### 🔹 **Core Problem**

Agar `index.html` ko `logo.png` dikhani hai, to browser ko **exact address** batana padta hai.

❌ Sirf `src="logo.png"` bol dena kaam nahi karega agar file alag folder me ho.

---

## 🗺️ **A) RELATIVE PATHS (99% Use Hoga)**

### 🔸 **Real-life Analogy:**

Relative Path = Apne ghar se padosi ko rasta batana.

"Yahan se straight jao → left → second ghar."

### 🔸 **Folder Structure Example:**

```
my-website/
├── index.html
├── about.html
├── dog.jpg
├── images/
│   ├── logo.png
│   └── hero.jpg
└── pages/
    ├── contact.html
    └── terms.html
```

---

## 🔸 **3 Scenarios with Code:**

### ✅ **Scenario 1: Same Folder me File**

```html
<!-- index.html se about.html ko link karna -->
<a href="about.html">About Us</a>
```

➡️ Sirf filename likhna hota hai.

---

### ✅ **Scenario 2: Sub-folder me File (Neeche jaana)**

```html
<!-- index.html se images/logo.png ko access karna -->
<img src="images/logo.png" alt="Website Logo">
```

➡️ `FolderName/FileName`

---

### ✅ **Scenario 3: Parent Folder me File (Upar jaana)**

```html
<!-- pages/contact.html se images/logo.png access karna -->
<img src="../images/logo.png" alt="Website Logo">
```

➡️ `../` = Ek level upar jao

---

### 💡 **Smart Trick:**

- `../` = Ek level **UPAR** jaana
- `folder/` = Ek level **NEECHE** jaana
- `filename` = Same level ki file

---

# 🌍 **B) ABSOLUTE PATHS (External Files ke Liye)**

### 🔸 **Real-life Analogy:**

Absolute Path = Puri duniya ka address

"Earth → India → Delhi → Chandni Chowk"

### 🔸 **When to Use:**

- Google Fonts
- CDN Images
- External Website Resources

### 🔸 **Examples:**

```html
<a href="https://www.google.com">Google Search</a>
<img src="https://example.com/images/logo.png" alt="External Logo">
```

---

# ⚠️ **CRITICAL SECURITY CONCEPT – Absolute Path Dangerous Kyun?**

### 🔹 **Browser "Prison" Analogy:**

Browser ek secure prison (sandbox) hai.

Koi website aapke computer ki local files access **nahi** kar sakti.

### 🔸 **Malicious Example:**

```html
<img src="C:/Users/HarshalChauhan/MyPasswords.txt">
```

Agar browser allow kare to koi bhi website aapki private files chura sakti hai.

➡️ Isliye browser local absolute paths ko block karta hai.

### 🔹 **Why Relative Paths Safe:**

Relative paths sirf project ke andar hi kaam karte hain — external system access nahi.

---

# 💻 **Windows vs macOS/Linux Absolute Paths**

| Feature    | Windows                  | macOS/Linux            |
| ---------- | ------------------------ | ---------------------- |
| Root Start | C:                       | /                      |
| Separator  | Backslash `\`            | Forward Slash `/`      |
| Example    | `C:\Users\John\file.txt` | `/Users/john/file.txt` |

---

# 🏗️ **2. HTML BOILERPLATE – Kyun Zaroori Hai?**

### 🔹 **Pehla Principle:**

Browser ko **clear instructions** chahiye.

Sirf `<h1>Hello</h1>` likhne se kaam nahi chalega.

---

## 🔸 **Boilerplate Code:**

```html
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meri Website</title>
</head>
<body>
    <!-- Yahan aapka visible content aayega -->
</body>
</html>
```

---

# 🔍 **Har Line ka Deep Explanation:**

### ✅  \<!DOCTYPE html>

- Batata hai ki **HTML5** use ho raha hai.
- Browser ko **standards mode** me laata hai.

---

### ✅ **\<html lang="hi">**

- Search engines aur screen readers ko language ka pata chalta hai.
- `lang="hi"` = Hindi, `lang="en"` = English.

---

### ✅ **\<meta charset="UTF-8">**

- Computer sirf numbers samajhta hai.
- UTF-8 Hindi, English, Emoji sab support karta hai.

❌ Without UTF-8: `रोहित → #%&!@`

✔ With UTF-8: `रोहित` properly show hoga.

---

### ✅ **\<meta name="viewport">**

- Website mobile pe choti na dikhai de, iske liye zaroori.
- `width=device-width` = device width ke hisaab se adjust.
- `initial-scale=1.0` = 100% zoom.

---

### ✅ **Document**

- Browser tab me dikhne wala naam.
- SEO me helpful.

---

# ❓ **Common Doubt: Boilerplate ke bina bhi to kaam chal jata hai!**

### 🔸 **Kyun Chal Jata Hai?**

Browser automatically missing tags add kar deta hai.

### 🔸 **Par Kyun Galat Hai?**

- Mobile-friendly nahi hota
- UTF-8 issues
- SEO down
- Accessibility kharab

➡️ Boilerplate = Proper engineered ghar.

---

# 🎯 **3. DIV, SPAN, CLASS & ID – Poori Power**

## 🔹 **DIV – Generic Box**

```html
<div>
    <h1>Hello</h1>
    <h2>Kaise ho?</h2>
    <p>Main theek hoon</p>
</div>
```

Use: Login forms, profile cards, groups.

---

## 🔹 **CLASS & ID – Labels**

### Analogy:

- **ID = Aadhaar Number (Unique)**
- **CLASS = Job Title (Multiple log same)**

### Code:

```html
<div id="main-header">Website Header</div>
<div class="profile-card">Harshal Profile</div>
<div class="profile-card">Arjun Profile</div>
```

### CSS Targeting:

```css
#main-header { background: blue; }
.profile-card { border: 1px solid gray; }
```

---

## 🔹 **SPAN – Inline Highlighter**

```html
<p>Yeh bahut <span class="highlight">important</span> information hai</p>
```

- `DIV` = block element
- `SPAN` = inline element

---

# 🏢 **4. SEMANTIC HTML – Meaningful Structure**

## Website ke 3 Parts

### ✅ **HEADER**

```html
<header>
    <h2>Website ka Header</h2>
    <nav>
        <a href="home.html">Home</a>
        <a href="about.html">About</a>
    </nav>
</header>
```

### ✅ **MAIN**

```html
<main>
    <h1>Main Content</h1>
    <p>Yeh page ka unique content hai</p>
</main>
```

### ✅ **FOOTER**

```html
<footer>
    <p>Contact Us: 987654310</p>
    <p>© 2025 My Website</p>
</footer>
```

---

# 💡 **Why Semantic Tags?**

- SEO better
- Screen readers friendly
- Code clean and readable

---

# 🛡️ **SECURITY DEEP DIVE**

### ❌ Local Absolute Path Example:

```html
<img src="/Users/Arjun/Desktop/project/dog.jpg" alt="Dog">
```

**Won’t work — security risk.**

Browser system files access nahi karne deta.

---

# 💾 **CHARACTER ENCODING – UTF-8 Magic**

- Computer characters ko numbers me convert karta hai.
- ASCII → Sirf 128 characters
- UTF-8 → Hindi, Chinese, Emoji sab

Examples:

- `A → 65`
- `र → 2350`
- `😂 → 128514`

---

# 🎨 **PRACTICAL FULL EXAMPLE**

```html
<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meri Website</title>
</head>
<body>
    <header>
        <nav>
            <a href="index.html">Home</a>
            <a href="about.html">About</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>
    
    <main>
        <div class="profile-card">
            <h1>Harshal Chauhan</h1>
            <p>Web Developer</p>
            <p>I love to <span class="highlight">code and teach</span></p>
        </div>
    </main>
    
    <footer>
        <p>Contact: harshal@example.com</p>
    </footer>
</body>
</html>
```

---

# 📚 **SUMMARY – Ek Nazar Me Sab Kuch**

## 🎯 FILE PATHS:

- Relative → 99% use
- Absolute → External resources
- Local absolute → ❌ Never use

## 🎯 BOILERPLATE:

- DOCTYPE = HTML5
- lang = Language
- UTF-8 = Universal characters
- Viewport = Mobile-friendly website
- Title = Tab name

## 🎯 ELEMENTS:

- DIV = Grouping
- SPAN = Inline
- CLASS = Multiple elements
- ID = Unique element

## 🎯 SEMANTIC:

Header → Top
Main → Unique content
Footer → Bottom info

## 🎯 SECURITY:

- Local absolute paths blocked
- Relative paths always use

---

# 💡 **FINAL PRO TIPS:**

- `../` = Ek level upar

- `folder/` = Andar

- `filename` = Same folder

- VS Code shortcut → `!` + `Tab`

- Class = School class

- ID = Roll number

- Security mindset: "Kya koi is code ka misuse kar sakta hai?"
