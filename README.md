# Food Steps

A simple phone app for tracking what you eat. You don't log meals as you eat them. When you get a minute, or in the evening, tick off the foods you had. The app adds up **calories, protein, carbs and fat** and shows how much is left against your daily targets.

## Features

- Tick a food to mark it as eaten. Use **− / +** to change servings in half steps.
- A totals panel stays at the bottom of the screen. It shows calories eaten out of your target and how much is left, plus protein, carbs and fat.
- Your **daily targets** can be edited. "Suggest targets" gives a rough starting point from your weight and goal.
- About 55 common foods are built in (South Indian breakfasts, rice, dal, curries, eggs, paneer, fruit, drinks and more). Use **＋** to add your own.
- Each day is saved separately. Use ‹ › to look back at earlier days.
- Search, category filters and an **Eaten** filter that shows today's list.
- Works offline. You can install it on your home screen (PWA), and it follows your phone's dark mode.
- Export and import a backup file (in ⚙︎ settings).

Nutrition values are approximate, per serving. Change them or add your own foods to match what you actually eat.

## Put it on your phone

The app is plain HTML, CSS and JS with no build step. Host it with GitHub Pages:

1. On GitHub, open the repo, then **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**. Pick the branch with this code and the `/ (root)` folder, then **Save**.
3. After a minute or so the app is live at `https://<your-username>.github.io/food-steps/`.
4. Open that link on your phone:
   - **Android (Chrome):** menu ⋮ → **Add to Home screen / Install app**
   - **iPhone (Safari):** Share → **Add to Home Screen**

Your data is stored on your phone in the browser's local storage. Nothing is uploaded. Use **Export** now and then to keep a backup.

## Run locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```
