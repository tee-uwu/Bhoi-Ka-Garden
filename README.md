# BHOI KA GARDEN 🦋

> An interactive, collaborative web canvas where users can draw, plant, and arrange custom flowers in a shared virtual garden.

## ✨ Features
* **Custom Drawing Pad:** Design your own flowers using a built-in canvas with adjustable brush sizes, custom color swatches, and an eraser.
* **Interactive Garden:** Plant your drawn flowers directly into the garden. Drag and drop them to find the perfect spot, and "lock" them in place[cite: 1].
* **Real-time Collaboration:** Powered by Supabase, watch other users plant and move flowers in the garden in real-time[cite: 1].
* **Gallery View:** Browse all planted flowers in a dedicated modal gallery and remove your own creations[cite: 1].
* **Dark/Light Mode:** Toggle between distinct visual themes to suit your viewing preference[cite: 1].

## 🛠️ Tech Stack
* **Frontend:** HTML5, CSS3, Vanilla JavaScript[cite: 1].
* **Backend / Database:** Supabase (PostgreSQL) for data persistence and real-time WebSocket syncing[cite: 1].
* **Fonts:** Google Fonts ('Patrick Hand' and 'Fredoka')[cite: 1].

## 🚀 Getting Started

### Prerequisites
You will need a [Supabase](https://supabase.com/) account to host the database.

### Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/bhoi-ka-garden.git](https://github.com/yourusername/bhoi-ka-garden.git)
   cd bhoi-ka-garden

# Set up your database:
Create a new project in Supabase Go to the SQL Editor in your Supabase dashboard and run the setup.sq Enable "Realtime" for the flowers table in your Database settings.

### Configure your API Keys:
1.Open index.html.
2.Locate the Supabase configuration section:
const supabaseUrl = "YOUR_SUPABASE_URL_HERE";
const supabaseKey = "YOUR_SUPABASE_ANON_KEY_HERE";
3.Run the project:
Simply open index.html in any modern web browser, or use a tool like Live Server in VS Code.

⚠️ A Note on Your API Keys
In the provided code, your Supabase URL and sb_publishable API key are hardcoded directly into the HTML[cite: 1]. While Supabase "anon/publishable" keys are generally safe to expose in front-end code (as long as you have Row Level Security configured properly in your database), it is best practice to eventually move them to a .env file if you ever convert this static HTML site into a Node.js/React/Vite project.
