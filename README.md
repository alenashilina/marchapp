# ✨ Подниматель настроения (Mood Lifter)

A cozy web app for Russian-speaking women that displays attractive men and cute animals with personalized compliments. Built with pure HTML, CSS, and JavaScript - no frameworks needed!
Note: the app is fully vibecoded with Claude and GLM

## 🌟 Features

- **Two modes**: Men (Мужчины) and Animals (Животные)
- **Smart filtering** for men:
  - Vibe (brutal/pretty)
  - Age (young/mature)
  - Beard (yes/no/stubble)
  - Glasses (yes/no)
  - 🔥 Special filter (appears at certain times...)
- **Animal types**: Cats, dogs, horses, parrots
- **Time-aware content**
- **Responsive design**: Works great on phones and desktop

## 📁 Project Structure

```
marchapp/
├── index.html              # Main app
├── celebrities.json        # Celebrity data with tags
├── names-map.json          # English → Russian names
├── phrases.json            # Compliments & phrases
├── phrases_animals.json    # Animal-specific phrases
├── animals.json            # Animal image lists
├── images/                 # Celebrity photos
└── animals/                # Animal photos
    ├── kittens/
    ├── puppies/
    ├── horses/
    └── parrots/
```

## 🚀 How to Run Locally

Since the app uses `fetch()` to load JSON files, you need a local server:

```bash
# Option 1: Python
python -m http.server 8000

# Option 2: Node.js
npx serve

# Option 3: PHP
php -S localhost:8000
```

Then open `http://localhost:8000` in your browser.

## 🌐 Deploy to GitHub Pages

1. Create a new repository on GitHub
2. Upload all files and folders
3. Go to **Settings** → **Pages**
4. Select **main** branch as source
5. Your app will be live at `https://yourusername.github.io/repo-name`

## ➕ Adding New Content

### Adding Celebrity Images

1. **Add images** to the `images/` folder
2. **Open `tagger.html`** in your browser (works with local server)
3. **Fill in the info** for each image:
   - Select the celebrity name from the list
   - Choose an emoji
   - Set the tags (vibe, age, beard, glasses, hot)
4. **Click "Export JSON"** when done
5. **Copy the output** and paste it into `celebrities.json`
6. **Add the name to `names-map.json`** if it's a new celebrity (format: `"English Name": "Русское Имя"`)

### Adding Animal Images

1. **Add images** to the appropriate folder: `animals/kittens/`, `animals/puppies/`, `animals/horses/`, or `animals/parrots/`
2. **Open `animals.json`** and add the filename to the corresponding array:

```json
{
  "cat": ["existing.jpg", "your-new-image.jpg"],
  "dog": ["puppy.jpg"],
  "horse": ["horse.jpg"],
  "parrot": ["parrot.jpg"]
}
```

### Adding New Phrases

- **Compliments with names**: Edit `phrases.json` → `compliments` → morning/afternoon/evening/night
- **Standalone silly/deep phrases**: Edit `phrases.json` → `silly` or `deep`
- **Animal phrases**: Edit `phrases_animals.json` → `animals` → animal type → time of day

## ⏰ Time-Based Features

| Time | Period |
|------|--------|
| 06:00 - 12:00 | Morning |
| 12:00 - 18:00 | Afternoon |
| 18:00 - 22:00 | Evening |
| 22:00 - 06:00 | Night |

## 🎨 Tech Stack

- Pure HTML5
- CSS3 (no frameworks)
- Vanilla JavaScript
- Google Fonts (Unbounded, Cormorant Garamond)

## 📝 License

Feel free to use and modify for personal use!

---

Made with 💖 for mood lifting
