# GEMINI.md - Shopping List App Context

## Project Overview
This project is a simple, modern **Shopping List Application** designed for ease of use and persistence. It's a single-page application (SPA) that allows users to manage their shopping items entirely within the browser.

### Main Technologies
- **Frontend**: HTML5, Vanilla JavaScript.
- **Backend/DB**: [Supabase](https://supabase.com/) (PostgreSQL).
- **Styling**: [Tailwind CSS](https://tailwindcss.com/) (loaded via CDN).
- **Icons**: [Lucide Icons](https://lucide.dev/) (loaded via CDN).
- **Fonts**: [Pretendard](https://github.com/orioncactus/pretendard) (loaded via Google Fonts).
- **Persistence**: Supabase Database is used for real-time data storage.

### Key Features
- **Add Items**: Users can input items into the list (Stored in Supabase).
- **Check/Uncheck Items**: A toggle to mark items as completed (Updated in Supabase).
- **Remove Items**: Delete individual items from the list.
- **Remaining Count**: Dynamically updates the number of active items.
- **Empty State**: Visual feedback when the list is empty.
- **Cloud Persistence**: Data is saved to `shopping_items` table in Supabase.

---

## Directory Overview
The directory contains the application code and documentation of its states through screenshots.

### Key Files
- `index.html`: The core of the application, containing the structure, styling, and logic.
- `01_initial_state.png`, `02_item_added.png`, `03_item_checked.png`, `04_item_deleted.png`: Screenshots illustrating various app states, likely captured during testing or manual walkthroughs.
- `.playwright-mcp/`: Contains logs and state information for the Playwright MCP tool, indicating browser automation has been used on this project.

---

## Building and Running
As a static HTML project, no build step is required.

### How to Run
- Simply open `index.html` in any modern web browser.
- No local server is strictly necessary, though one can be used (e.g., `python -m http.server` or VS Code Live Server).

### Testing
- Visual validation is provided by the included `.png` screenshots.
- Automation: The presence of `.playwright-mcp` suggests that Playwright is used for browser-level testing or state capture.

---

## Development Conventions
- **Single File Architecture**: All HTML, CSS (Tailwind classes), and JS are contained in `index.html`.
- **Vanilla JS**: No frontend framework (like React or Vue) is used. DOM manipulation is handled directly.
- **Naming**: Use descriptive IDs and classes (e.g., `add-form`, `item-input`, `shopping-list`).
- **Persistence**: Always synchronize the `items` array with `localStorage` after any state change.
