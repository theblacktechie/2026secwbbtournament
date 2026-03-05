# 2026 SEC Women's Basketball Tournament Bracket

An interactive, mobile-first tournament bracket for the 2026 SEC Women's Basketball Tournament held at Bon Secours Wellness Arena in Greenville, SC.

Designed in the style of The Athletic and Sportico : warm off-white editorial base with SEC navy/gold branding and school color accents throughout.

---

## Features

- 📱 **Mobile-first** : swipe left/right to navigate rounds, fully responsive
- 🏀 **Live bracket** : tap any team to advance them as the winner
- 🎨 **School color theming** : each team's card glows in their official colors
- 📊 **Game stat cards** : quarter scores, team rebounds & assists, top scorer, and game notes
- 🏆 **Full tournament flow** : First Round through Championship, all 15 games

---

## How to Deploy

No build step. No npm. Just two files:

1. Upload `index.html` to your GitHub repo
2. Upload `README.md`
3. Enable GitHub Pages in repo **Settings → Pages → main branch**

Live at `https://YOUR_USERNAME.github.io/REPO_NAME/`

---

## Adding Game Stats

All stats live in the `STATS` object near the top of `index.html`. To add a completed game, add an entry:

```js
g4: {
  score1:"72", score2:"68",
  q1_1:"18", q2_1:"20", q3_1:"16", q4_1:"18",
  q1_2:"14", q2_2:"22", q3_2:"18", q4_2:"14",
  reb1:"38", ast1:"14", reb2:"32", ast2:"11",
  star1:"Player Name", starSt1:"24 pts · 6 reb",
  star2:"Player Name", starSt2:"18 pts · 4 ast",
  notes:"Game narrative here.",
},
```

To advance a winner in the bracket, update the `initBracket` function:

```js
b.r1[3].winner = "Alabama";
b.r2[3].t1 = "Alabama";
```

---

## Tech

- React 18 via CDN : no build step required
- Babel standalone for in-browser JSX transpiling
- [Inter](https://fonts.google.com/specimen/Inter) via Google Fonts
- Pure inline styles : zero dependencies

---

## Credits

- Tournament data: [SEC Sports](https://www.secsports.com)
- Design inspiration: The Athletic, Sportico
- Font: [Inter by Rasmus Andersson](https://fonts.google.com/specimen/Inter)
