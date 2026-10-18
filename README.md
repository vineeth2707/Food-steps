# Food Steps

A simple phone app for tracking what you eat. You don't log meals as you eat them. When you get a minute, or in the evening, tick off the foods you had. The app adds up **calories, protein, carbs and fat** and shows how much is left against your daily targets.

**Use it now:** https://vineeth2707.github.io/Food-steps/

Anyone can open this link and use the app. Each person's data stays in their own phone's browser. Nothing is uploaded and nobody sees anyone else's log.

## Features

- Tick a food to mark it as eaten. Use **− / +** to change servings in half steps.
- A totals panel stays at the bottom of the screen. It shows calories eaten out of your target and how much is left, plus protein, carbs and fat.
- Your **daily targets** can be edited (⚙︎). "Suggest targets" gives a rough starting point from your weight and goal.
- **Any day:** use ‹ › to move between days, tap the date to pick from a calendar, and tap **Today** to jump back. You can look back at past days or plan ahead.
- About 55 common foods are built in (South Indian breakfasts, rice, dal, curries, eggs, paneer, fruit, drinks and more):
  - **＋** adds your own food.
  - **✎** lets you edit or delete any food, including the built-in ones.
  - Deleted foods can be restored in ⚙︎ settings, and edits to built-in foods can be undone there.
- Search, category filters and an **Eaten** filter that shows that day's list.
- Works offline. You can install it on your home screen (PWA), and it follows your phone's dark mode.
- Export and import a backup file (in ⚙︎ settings).

Nutrition values are approximate, per serving. Edit them to match what you actually eat.

## Install on your phone

Open the link above, then:

- **Android (Chrome):** menu ⋮ → **Add to Home screen / Install app**
- **iPhone (Safari):** Share → **Add to Home Screen**

It then opens full screen from its own icon, like a normal app.

## Get your own copy of the code

The app is plain HTML, CSS and JavaScript with no build step and nothing to install.

**Download it to your computer**

```sh
git clone https://github.com/vineeth2707/Food-steps.git
cd Food-steps
python3 -m http.server 8000
# then open http://localhost:8000 in your browser
```

No git? Click the green **Code** button on the repo page, choose **Download ZIP**, and unzip it. Opening `index.html` directly also works, but offline mode needs it served over `http://` as shown above.

**Host your own version (free)**

1. Click **Fork** at the top of the repo page to copy it to your GitHub account.
2. In your fork, go to **Settings → Pages**, choose **Deploy from a branch**, pick `main` and `/ (root)`, then **Save**.
3. A minute later your copy is live at `https://<your-username>.github.io/Food-steps/`.

## Files

| File | What it does |
|---|---|
| `index.html` | The whole app: screens, food list and calculations |
| `manifest.webmanifest` | Lets phones install it as an app |
| `sw.js` | Makes it work offline |
| `icon.svg` | App icon |

To change the built-in food list, edit `BASE_FOODS` near the top of the script in `index.html`. Each row is `[id, name, serving, category, kcal, protein, carbs, fat]`.

## License

MIT. Free to use, copy and change. See [LICENSE](LICENSE).
