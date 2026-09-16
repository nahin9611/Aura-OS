# Aura OS

An interactive, web-based desktop environment that simulates the look, feel, and functionality of a traditional operating system inside the browser. Aura OS translates modular web components into a cohesive, multitasking workspace.

---

## 🚀 Features

* **Window Management**: Dynamic $z\text{-index}$ layering, window lifecycle controls (minimize, maximize, close), and smooth drag-and-drop repositioning.
* **Desktop Shell & Taskbar**: Central hub managing open processes, dynamic taskbar icons, system widgets, launcher menu, and a live clock.
* **Modular App Engine**: Plug-and-play architecture for mounting isolated sub-applications (File Explorer, Terminal, Code Editor, custom tools).
* **State Persistence**: Automatic syncing of desktop layouts, active themes, wallpaper, and user data using browser storage (`localStorage` / `IndexedDB`).
* **Global Event Bus**: Centralized event handling for keyboard shortcuts, window focus switching, background tasks, and context menus.

---

## ⚙️ How It Works

### 1. Window Layering & Physics
Window positioning updates real-time positional coordinates $(x, y)$ on the viewport grid. Active windows are automatically brought to the foreground by re-indexing depth values upon user interaction.

### 2. Process Lifecycle
* **Initiation**: Launching an app via the desktop shortcut or start menu emits a trigger to the process manager.
* **Mounting**: The system instantiates an isolated app component wrapped inside a dynamic window container.
* **Execution**: Global state tracks active process IDs, instantly syncing open applications with the taskbar.
* **Persistence**: System configuration changes write directly to local cache to preserve workspace state across page reloads.

---

## 🛠️ Tech Stack

* **Frontend Framework**: JavaScript (ES6+) / React / HTML5 / CSS3
* **State & Storage**: Web Storage API (`localStorage`, `IndexedDB`)
* **Icons & Styling**: Tailwind CSS / Custom Web Components

---

## 📦 Getting Started

### Prerequisites
* Node.js (v18.0.0 or higher)
* npm or yarn

### Installation

1. **Clone the repository**
   ```bash
   git clone [https://github.com/your-username/aura-os.git](https://github.com/your-username/aura-os.git)
   cd aura-os
