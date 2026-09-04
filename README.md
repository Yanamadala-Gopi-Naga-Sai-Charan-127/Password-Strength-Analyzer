# 🔐 Password Strength Analyzer

A browser‑based tool that evaluates the strength of user‑entered passwords in real time.  
It checks **length**, **complexity** (case, numbers, symbols), and **uniqueness** (against common passwords and your personal history).  
It also suggests stronger alternatives and can generate cryptographically strong passwords.

![Screenshot](screenshot.png)  
*(Add a screenshot of your tool here for a better preview)*

---

## ✨ Features

- **Real‑time strength meter** – visual feedback with color‑coded score (Weak → Strong).
- **Detailed analysis** – shows exactly what’s missing (e.g., “no symbols”, “too short”).
- **5‑point badge system** – instant pass/fail indicators for length, case, numbers, symbols, and uniqueness.
- **Actionable suggestions** – specific tips to improve your password.
- **Strong password generator** – creates a 16‑character random password with mixed case, digits, and symbols.
- **Password history** – stores previous passwords in your browser’s `localStorage` (prevents reuse).  
  *Can be easily replaced with a backend database for production use.*
- **Privacy first** – all processing is done client‑side; no passwords are sent over the network.

---

## 🚀 How to Use

1. **Open the tool** – just double‑click the `index.html` file in your browser.  
   No server, no installation – it works offline.

2. **Enter a password** – the strength meter and analysis update instantly.

3. **Generate a strong password** – click the *Generate Strong* button.

4. **Save to history** – double‑click the password field or press `Ctrl+Shift+S` to save the current password.  
   The history panel (toggle with the arrow button) shows all saved passwords and their timestamps.

5. **Clear history** – use the *Clear History* button or the *Reset DB* link in the footer.

---

## 🛠️ Technologies

- **HTML5** – semantic structure.
- **CSS3** – responsive, modern UI with smooth animations.
- **Vanilla JavaScript** – all logic, analysis, and storage.
- **Font Awesome** – icons for visual clarity.
- **Web Crypto API** – for generating cryptographically secure random passwords.

---

## 💾 Local Storage & Backend Integration

By default, password history is stored in your browser’s `localStorage`.  
To connect to a real database (e.g., to prevent reuse across users or devices):

1. Locate the functions `savePasswordToHistory()` and `renderHistory()` in the `<script>` section.
2. Replace `localStorage` calls with `fetch()` calls to your own API endpoints.
3. **Never store plain‑text passwords** – always hash them (e.g., with bcrypt, Argon2) before sending to the server.

---

## 📁 Project Structure

Since it’s a single‑file HTML application, the structure is simple:
