# 📝 React Notepad App (Notes App)

This project is a **fully functional Notepad / Notes App** built using  **React.js** .

The app allows users to **write notes, store them locally, delete them, and download notes as text files** on their system.

The main goal of this project is to demonstrate  **React state management, component-based design, and browser-based file handling** .

---

## 🎥 Project Overview (From Video)

In this project:

* Users can **add unlimited notes**
* Notes are displayed in a **card-based UI**
* Notes are **stored locally** (no backend required)
* Each note can be:
  * ❌ Deleted
  * 💾 Downloaded as a `.txt` file
* Downloaded file names are **automatically generated** from the first **5 characters** of the note text
* Smooth UI interactions using **icons, transitions, and modal dialogs**

---

## 🚀 Features

* ➕ Add new notes using a dialog box
* ✍️ Write long text notes (no character limit)
* 🗑️ Delete individual notes
* 💾 Download notes as `.txt` files
* 📁 File name auto-generated (max 5 characters)
* ⚡ Fast performance using **Vite**
* 🎨 Clean and modern UI

---

## 🛠️ Tech Stack

* **Frontend:** React.js
* **Build Tool:** Vite
* **Language:** JavaScript (JSX)
* **Styling:** CSS / Utility-based styling
* **Icons:** Lucide React
* **Storage:** Browser Local State (no database)

---

## 📂 Project Structure

<pre class="overflow-visible! px-0!" data-start="1681" data-end="1975"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre!"><span><span>notepad-app/
├── src/
│   ├── components/
│   │   └── NotesCard.jsx   # Displays </span><span>each</span><span> note
│   ├── App.jsx            # Main app logic
│   ├── App.css
│   ├── </span><span>index</span><span>.css
│   └── main.jsx           # Entry </span><span>point</span><span>
├── </span><span>public</span><span>/
├── </span><span>index</span><span>.html
├── package.json
├── vite.config.js
└── README.md
</span></span></code></div></div></pre>

---

## ⚙️ How the App Works

### 1️⃣ Adding Notes

* Click on the **➕ Add button**
* A **dialog box** opens
* Write your note in the text area
* Click **Add**
* If the text is empty, an alert asks you to write something

---

### 2️⃣ State Management

* Notes are stored using `useState`
* Each note contains:
  * `id` (generated using Date)
  * `title` (note text)

---

### 3️⃣ Displaying Notes

* Notes are rendered using `.map()`
* If no notes exist, the message **“No Notes Available”** is shown

---

### 4️⃣ Deleting Notes

* Each note card has a **Delete icon**
* Clicking it removes the note using `.filter()`

---

### 5️⃣ Downloading Notes (Important Feature)

When the **Save icon** is clicked:

* A **Blob** object is created from the note text
* A temporary **Object URL** is generated
* A hidden `<a>` tag is created programmatically
* The file is downloaded as `.txt`
* File name logic:
  * If note length > 5 → first 5 characters used
  * Else → full note text used
* The Object URL is revoked after download

---

## ▶️ How to Run the Project Locally

### Step 1: Clone the repository

<pre class="overflow-visible! px-0!" data-start="3077" data-end="3144"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre! language-bash"><span><span>git </span><span>clone</span><span> https://github.com/Rahul20004/notepad-app.git
</span></span></code></div></div></pre>

### Step 2: Go to project directory

<pre class="overflow-visible! px-0!" data-start="3182" data-end="3208"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre! language-bash"><span><span>cd</span><span> notepad-app
</span></span></code></div></div></pre>

### Step 3: Install dependencies

<pre class="overflow-visible! px-0!" data-start="3243" data-end="3266"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre! language-bash"><span><span>npm install
</span></span></code></div></div></pre>

### Step 4: Start development server

<pre class="overflow-visible! px-0!" data-start="3305" data-end="3328"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre! language-bash"><span><span>npm run dev
</span></span></code></div></div></pre>

### Step 5: Open in browser

<pre class="overflow-visible! px-0!" data-start="3358" data-end="3387"><div class="contain-inline-size rounded-2xl corner-superellipse/1.1 relative bg-token-sidebar-surface-primary"><div class="sticky top-[calc(--spacing(9)+var(--header-height))] @w-xl/main:top-9"><div class="absolute end-0 bottom-0 flex h-9 items-center pe-2"><div class="bg-token-bg-elevated-secondary text-token-text-secondary flex items-center gap-4 rounded-sm px-2 font-sans text-xs"></div></div></div><div class="overflow-y-auto p-4" dir="ltr"><code class="whitespace-pre!"><span><span>http:</span><span>//localhost:5173</span><span>
</span></span></code></div></div></pre>

---

## ❌ Backend Information

* ❌ No backend is used
* ❌ No database required
* ✅ Fully frontend-based project
* ✅ Runs entirely in the browser

---

## 📌 Key Learning Outcomes

* React `useState` and conditional rendering
* Handling user input with controlled components
* Component-based UI design
* File download using **Blob & Object URL**
* Dynamic rendering using `.map()` and `.filter()`

---

## 🔮 Future Improvements

* Persistent storage using LocalStorage / Database
* Search notes feature
* Edit existing notes
* Dark mode support
* Backend integration (Node.js + MongoDB)

---

## 👨‍💻 Author

**Rahul**

B.Tech – Computer Science

GitHub: [https://github.com/Rahul20004]()
