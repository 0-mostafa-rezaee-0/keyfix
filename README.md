# keyfix
KeyFix — A lightweight Windows tool that fixes text typed with the wrong keyboard layout. It supports Persian ↔ English out of the box and is fully extensible: add any language by editing a layout dictionary. Highlight text, press a hotkey, and KeyFix rewrites it instantly — no retyping needed.


Perfect 👌 Let’s make you a professional, developer-friendly **README.md** for your `KeyFix` project.
I’ll keep it clear, structured, and emphasize **why `venv` is best practice here**, while also explaining why **Docker, Conda, and uv are not recommended** for this specific case.

---

# README.md

````markdown
# KeyFix  

**KeyFix** — A lightweight Windows tool that instantly corrects text typed with the wrong keyboard layout.  
Out of the box, it supports **Persian ↔ English**, but the design is fully extensible: add mappings for any other language by editing a simple layout dictionary.  
Highlight text, press a hotkey, and KeyFix rewrites it instantly — no retyping needed.  

---

## ✨ Features  
- 🔄 Instant correction between Persian ↔ English layouts  
- ⚡ Hotkey-based workflow: highlight + shortcut = corrected text  
- 🖥️ Native Windows integration (clipboard + global hotkeys)  
- 🛠️ Built in Python with a clean mapping engine (`fix_keyboard_layout`)  
- 📦 Packaged as a standalone `.exe` (no Python required for end users)  
- 🌍 Extensible: easily add support for new languages via mapping dictionary  

---

## 🚀 Installation  

1. Clone the repo:  
   ```bash
   git clone https://github.com/yourusername/keyfix
   cd keyfix
````

2. Create a virtual environment (recommended):

   ```bash
   python -m venv .venv
   source .venv/bin/activate   # Linux/macOS
   .venv\Scripts\activate      # Windows PowerShell
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Run the app:

   ```bash
   python main.py
   ```

5. Build as Windows executable (optional):

   ```bash
   pyinstaller --onefile --noconsole main.py
   ```

---

## 🧑‍💻 Why `venv` is Best Practice Here

This project is a **Windows desktop app** — not a server or a data science pipeline. That changes the choice of environment tool.

### ✅ Why `venv`

* Built into Python — no extra tools needed
* Lightweight, fast, and portable
* Works seamlessly with **PyInstaller** for packaging into `.exe`
* Perfect for small, clean projects where dependencies are simple
* Universally supported (Windows, Linux, macOS)

### ❌ Why not Docker

* Docker is great for servers and reproducible ML environments — but overkill for a Windows desktop app.
* End users won’t run Docker to use a hotkey utility; they expect a **double-clickable `.exe`**.
* Clipboard and hotkey integration don’t play nicely inside containers.
* Adds complexity without benefit for this project.

### ❌ Why not Conda

* Conda is powerful for ML/AI projects (managing binary libraries, CUDA, etc.).
* But it is heavier, slower, and often complicates packaging into `.exe`.
* Our project doesn’t need Conda’s advanced dependency management.

### ❌ Why not uv

* `uv` is a modern, fast dependency manager.
* Still new, less mature on Windows, and adds little benefit here.
* For long-term reproducibility, `venv` + `requirements.txt` is the stable choice.

👉 For **KeyFix**, `venv` strikes the best balance between simplicity, reproducibility, and compatibility with Windows `.exe` packaging.

---

## 🛠️ Usage

1. Select any text typed with the wrong keyboard layout.
2. Press the configured hotkey.
3. KeyFix instantly replaces it with the corrected text.

---

## 🔮 Roadmap

* [ ] Configurable hotkeys
* [ ] System tray icon for enabling/disabling
* [ ] External config (JSON/YAML) for custom language mappings
* [ ] Extend support for additional languages (Russian, Arabic, etc.)

---

## 📜 License

MIT License. See `LICENSE` file for details.

```

---

This README:  
- Explains the **project clearly**.  
- Documents **install + usage**.  
- Includes a **Why venv** section with comparisons to Docker, Conda, uv.  
- Professional and GitHub-ready.  

---

Do you want me to also include a **diagram** (ASCII or mermaid) showing the workflow: *User → Hotkey → KeyFix Core → Clipboard → Corrected Text*?
```
