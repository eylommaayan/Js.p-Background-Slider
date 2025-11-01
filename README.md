<img width="1868" height="895" alt="image" src="https://github.com/user-attachments/assets/910c10cf-c241-4c69-9bf3-5253af7b87eb" />

---

```markdown
# 🖼️ Image Background Slider (מצגת רקעים מתחלפים)

מצגת רקעים יפהפייה שנבנית ב־HTML, CSS ו־JavaScript.  
המצגת מחליפה את התמונה הראשית של הרקע בכל מעבר, ומוסיפה שכבת כהות (overlay) מעל התמונות כדי לשמור על קונטרסט.

---

## 📸 תצוגה כללית

המצגת מורכבת ממספר **divים עם class בשם `slide`**, שכל אחד מהם כולל תמונת רקע (background-image).  
בעת מעבר ימינה או שמאלה, התמונה הפעילה משתנה, והרקע של העמוד כולו מתעדכן בהתאם.

---

## 🧩 מבנה הפרויקט

```

project-folder/
├── index.html      # מבנה ה־HTML עם כל התמונות והכפתורים
├── style.css       # עיצוב המצגת, אנימציות, מיקום החצים והרקע
├── script.js       # קוד JavaScript שמנהל את ההחלפה בין התמונות
└── README.md       # תיעוד הפרויקט (קובץ זה)

````

---

## 🧠 איך זה עובד

### 1. בחירת אלמנטים
```js
const slides = document.querySelectorAll('.slide')
const leftBtn = document.getElementById('left')
const rightBtn = document.getElementById('right')
````

### 2. לחיצה על חץ ימני / שמאלי

בעת לחיצה על חץ, המונה `activeSlide` גדל או קטן בהתאם.
אם עוברים את הגבול של הרשימה – חוזרים להתחלה או לסוף.

### 3. שינוי רקע המסך

```js
function setBgToBody() {
  body.style.backgroundImage = slides[activeSlide].style.backgroundImage
}
```

כך גם גוף העמוד (body) וגם השקופית משתנים יחד, ליצירת אפקט מעבר חלק.

### 4. הוספת / הסרת מחלקת `active`

```js
function setActiveSlide() {
  slides.forEach((slide) => slide.classList.remove('active'))
  slides[activeSlide].classList.add('active')
}
```

רק שקופית אחת פעילה בזמן נתון.

---

## 🎨 עיצוב (style.css)

* כל שקופית מוגדרת ב־`background-image`.
* שכבת כהות (`body::before`) מוסיפה עומק ומדגישה את התמונה.
* החצים (`.arrow`) ממוקמים באמצע המסך, בצדדים.
* המעבר בין השקופיות נעשה בעזרת `opacity` ו־`transition`.

---

## 🚀 הפעלה מקומית

1. הורד את הקבצים לתיקייה אחת.
2. פתח את הקובץ `index.html` בדפדפן (אין צורך בשרת).
3. לחץ על החצים ← ו־→ כדי לעבור בין השקופיות.

---

## ⚙️ טכנולוגיות בשימוש

* **HTML5** – מבנה ותוכן
* **CSS3** – עיצוב, מיקום ואפקטים
* **JavaScript (Vanilla)** – לוגיקה של המצגת
* **Font Awesome** – אייקונים של חצים
* **Google Fonts (Roboto)** – עיצוב גופנים

---

## 💡 אפשרויות הרחבה

* הוספת **טקסט מעל התמונה** (caption) לכל שקופית.
* הוספת **מעבר אוטומטי** בין תמונות עם `setInterval`.
* הוספת **מעבר fade או slide** עם אנימציות CSS.
* חיבור למקור תמונות חיצוני (Unsplash API).

---

## 🧑‍💻 קרדיט

פרויקט לימודי שנבנה כדי להמחיש עבודה עם:

* DOM
* אירועים (`addEventListener`)
* שינויי CSS בזמן אמת
* עבודה עם `background-image`

---

## 🪄 הדגמה חיה

ניתן להעלות את הפרויקט ל־Vercel / Netlify / GitHub Pages כדי לצפות בו אונליין.

---

**מטרה:** לימוד ניהול מצגות רקעים ב־JavaScript בסיסי

```

---

רוצה שאהפוך את זה לקובץ `README.md` אמיתי שאפשר להוריד (למשל לקובץ מוכן עם עיצוב GitHub)?
```
