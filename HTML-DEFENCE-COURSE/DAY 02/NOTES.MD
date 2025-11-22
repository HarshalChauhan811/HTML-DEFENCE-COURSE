# 📚 HTML Lecture 02 - Nested Lists & Tables

### Made By @Harshal Chauhan

---

## 🎯 Kya Seekhenge Aaj?

- ✅ Nested Lists - Lists ke andar lists banana
- ✅ Tables - Professional data display
- ✅ Advanced Features - COLSPAN, ROWSPAN
- ✅ Real Projects ke liye ready ho jaoge

---

# 📋 PART 1: NESTED LISTS 🎯

## 🔹 Basic Lists Recap 📝

**Do Types ki Lists:**

```html
<!-- Ordered List (Numbered) -->
<ol>
  <li>First Item</li>
  <li>Second Item</li>
</ol>

<!-- Unordered List (Bulleted) -->
<ul>
  <li>Apple</li>
  <li>Orange</li>
</ul>
```

## 🔹 Nested List Kya Hai? 🤔

**List ke andar dusri list banana**

### Real Example:

```
• India
    • Delhi
    • Mumbai
    • Goa
• USA
    • California
    • Texas
```

---

## 🔹 Step-by-Step Banaye Nested List 🛠️

### **Step 1: Basic List**

```html
<ul>
  <li>India</li>
  <li>USA</li>
  <li>England</li>
</ul>
```

### **Step 2: India ke Andar Cities**

```html
<ul>
  <li>India
    <ul>
      <li>Delhi</li>
      <li>Mumbai</li>
      <li>Goa</li>
    </ul>
  </li>
  <li>USA</li>
  <li>England</li>
</ul>
```

### **Step 3: USA ke Andar Cities**

```html
<ul>
  <li>India
    <ul>
      <li>Delhi</li>
      <li>Mumbai</li>
      <li>Goa</li>
    </ul>
  </li>
  <li>USA
    <ul>
      <li>California</li>
      <li>Texas</li>
    </ul>
  </li>
  <li>England</li>
</ul>
```

### **Step 4: Complete Code ✅**

```html
<ul>
  <li>India
    <ul>
      <li>Delhi</li>
      <li>Mumbai</li>
      <li>Goa</li>
    </ul>
  </li>
  <li>USA
    <ul>
      <li>California</li>
      <li>Texas</li>
    </ul>
  </li>
  <li>England
    <ul>
      <li>London</li>
      <li>Oval</li>
      <li>Yorkshire</li>
    </ul>
  </li>
</ul>
```

---

## 🔹 Mixed Lists Example 🔄

```html
<ul>
  <li>India
    <ul>
      <li>Delhi
        <ol>
          <li>Dwarka</li>
          <li>Vikas Puri</li>
        </ol>
      </li>
      <li>Mumbai</li>
    </ul>
  </li>
</ul>
```

---

## 🔹 Real Project - Course Curriculum 💼

```html
<h2>Course Topics</h2>
<ul>
  <li>DSA
    <ul>
      <li>Array</li>
      <li>Linked List</li>
      <li>Stack</li>
      <li>Queue</li>
    </ul>
  </li>
  <li>Web Technology
    <ul>
      <li>HTML</li>
      <li>CSS</li>
      <li>JavaScript</li>
    </ul>
  </li>
  <li>Aptitude</li>
  <li>Git</li>
  <li>Placement</li>
</ul>
```

---

# 📊 PART 2: TABLES - Complete Guide 🎯

## 🔹 Table Kya Hai? 🤔

**Data ko rows aur columns mein organize karna**

### Real Uses:

- 🕐 Time Table
- 💰 Price List
- 👨‍🎓 Student Data
- 👨‍💼 Employee Information

---

## 🔹 Basic Table Structure 🏗️

**Required Tags:**

- `<table>` → Complete table
- `<tr>` → Table Row
- `<td>` → Table Data
- `<th>` → Table Header

### Simple Example:

```html
<table border="1">
  <tr>
    <th>Name</th>
    <th>Role</th>
  </tr>
  <tr>
    <td>Harshal</td>
    <td>Frontend Developer</td>
  </tr>
  <tr>
    <td>Mohit</td>
    <td>Backend Developer</td>
  </tr>
</table>
```

### Output:

```
Name    | Role
-------------------
Harshal   | Frontend Developer
Mohit   | Backend Developer
```

---

## 🔹 Professional Table Structure 💼

- `<thead>` → Header
- `<tbody>` → Body
- `<tfoot>` → Footer

### Professional Example:

```html
<table border="1">
  <thead>
    <tr>
      <th>Item</th>
      <th>Quantity</th>
      <th>Price</th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td>Apple</td>
      <td>10</td>
      <td>$1</td>
    </tr>
    <tr>
      <td>Orange</td>
      <td>5</td>
      <td>$0.5</td>
    </tr>
  </tbody>
  
  <tfoot>
    <tr>
      <td>Total</td>
      <td>15</td>
      <td>$1.5</td>
    </tr>
  </tfoot>
</table>
```

---

# 🎯 ADVANCED TABLE FEATURES ⚡

## 🔹 **COLSPAN** - Ek Cell Multiple Columns Cover Kare 📏

```html
<table border="1">
  <thead>
    <tr>
      <th>Name</th>
      <th colspan="2">Contact Info</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>John Doe</td>
      <td>1234567890</td>
      <td>john@example.com</td>
    </tr>
  </tbody>
</table>
```

### Output:

```
Name      | Contact Info
          | 1234567890 | john@example.com
```

---

## 🔹 **ROWSPAN** - Ek Cell Multiple Rows Cover Kare 📐

```html
<table border="1">
  <tr>
    <td rowspan="2">Row 1 Cell 1 (2 rows)</td>
    <td>Row 1 Cell 2</td>
    <td>Row 1 Cell 3</td>
  </tr>
  <tr>
    <td>Row 2 Cell 2</td>
    <td>Row 2 Cell 3</td>
  </tr>
</table>
```

### Output:

```
Row 1 Cell 1 | Row 1 Cell 2 | Row 1 Cell 3
(2 rows)     | Row 2 Cell 2 | Row 2 Cell 3
```

---

## 🔹 Complex Table - Shopping Cart 🛒

```html
<table border="1">
  <thead>
    <tr>
      <th>Item</th>
      <th>Quantity</th>
      <th>Price</th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td>Apple</td>
      <td>10</td>
      <td>$1</td>
    </tr>
    <tr>
      <td>Orange</td>
      <td>5</td>
      <td>$0.5</td>
    </tr>
    <tr>
      <td>Banana</td>
      <td>8</td>
      <td>$0.3</td>
    </tr>
  </tbody>
  
  <tfoot>
    <tr>
      <td>Total</td>
      <td>23</td>
      <td>$14.90</td>
    </tr>
  </tfoot>
</table>
```

---

# 🚀 COMPLEX TABLE PROJECTS 💻

## 🔹 Student Information Table 👨‍🎓

```html
<table border="1">
  <thead>
    <tr>
      <th>Name</th>
      <th colspan="2">Contact Info</th>
      <th>Course</th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td>Rahul Sharma</td>
      <td>9876543210</td>
      <td>rahul@email.com</td>
      <td>Web Development</td>
    </tr>
    <tr>
      <td>Priya Singh</td>
      <td>9123456780</td>
      <td>priya@email.com</td>
      <td>Data Science</td>
    </tr>
  </tbody>
</table>
```

---

## 🔹 Multi-level Organization Table 🏢

```html
<table border="1">
  <thead>
    <tr>
      <th>Department</th>
      <th>Team</th>
      <th>Employee</th>
      <th>Role</th>
    </tr>
  </thead>
  
  <tbody>
    <tr>
      <td rowspan="3">Technology</td>
      <td rowspan="2">Frontend</td>
      <td>Rahul</td>
      <td>React Developer</td>
    </tr>
    <tr>
      <td>Neha</td>
      <td>UI Designer</td>
    </tr>
    <tr>
      <td>Backend</td>
      <td>Amit</td>
      <td>Node.js Developer</td>
    </tr>
  </tbody>
</table>
```

---

# 💡 PRO TIPS & BEST PRACTICES 🌟

## 🔹 Nested Lists Tips: 📝

- Hierarchy Maintain Karo
- Proper Indentation
- Mixed Lists Use Karo
- Practice

## 🔹 Tables Tips: 📊

- Semantic Tags Use Karo
- Border Attribute for visibility
- Colspan/Rowspan for complex layouts
- TH for headings

## 🔹 Common Mistakes ❌

- Missing Closing Tags
- Wrong rowspan/colspan values
- No semantic structure

## 🔹 Debugging Strategy 🐛

- Pehle Simple Structure
- Phir Complex Features
- Step-by-step Test
- Browser Preview

---

# 📚 QUICK REFERENCE CHEATSHEET 🎯

## 🔹 Nested Lists Syntax:

```html
<ul>
  <li>Parent Item
    <ul>
      <li>Child Item 1</li>
      <li>Child Item 2</li>
    </ul>
  </li>
</ul>
```

## 🔹 Basic Table Syntax:

```html
<table>
  <tr>
    <th>Header 1</th>
    <th>Header 2</th>
  </tr>
  <tr>
    <td>Data 1</td>
    <td>Data 2</td>
  </tr>
</table>
```

## 🔹 Advanced Table Syntax:

```html
<table>
  <thead>
    <tr><th>Head</th></tr>
  </thead>
  <tbody>
    <tr><td>Body</td></tr>
  </tbody>
  <tfoot>
    <tr><td>Footer</td></tr>
  </tfoot>
</table>
```

## 🔹 Rowspan/Colspan Syntax:

```html
<td rowspan="2">2 Rows</td>
<td colspan="3">3 Columns</td>
```

---

# 🎯 KEY TAKEAWAYS ✨

### 🔸 Nested Lists:

- Lists ke andar lists
- Mixed types allowed
- Unlimited nesting
- Real projects mein useful

### 🔸 Tables:

- Data organize karne ka best way
- thead/tbody/tfoot
- Rowspan/Colspan for complex layouts
- SEO friendly

### 🔸 Advanced Concepts:

- Rowspan → Multiple rows
- Colspan → Multiple columns
- Complex tables require planning

---

# 🚀 HOMEWORK & PRACTICE 📝

### 🔹 Assignment 1: Nested List

Apne state ke districts aur cities ki nested list banao

### 🔹 Assignment 2: Professional Table

Family details ka table with proper headers

### 🔹 Assignment 3: Complex Table

School timetable using rowspan & colspan

### 🔹 Pro Tip:

"Pehle khud try karo, phir solution dekho!"

---

# 💫 FINAL WORDS 🌟

"Aaj humne dekha ki kaise hum professional-level nested lists aur tables bana sakte hain! Ye concepts initially thode complex lag sakte hain, lekin practice ke saath ye butter ki tarah smooth ho jayenge!

