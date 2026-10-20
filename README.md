# 🍱 Bento Balance · ميزان البنتو

**EN** — A 2D physics game that turns your meal into Tetris-like blocks. Block size follows calories, color follows the dominant macro (protein / carbs / fat / veg). Arrange them on a plate balanced on a pivot: too many calories, uneven load, or a bad macro ratio and the plate falls.

**AR** — لعبة فيزياء ثنائية الأبعاد تحوّل مكونات وجبتك إلى قطع تيتريس. حجم القطعة يتبع السعرات ولونها يتبع العنصر الغذائي الغالب. رتّبها على طبق متوازن على محور؛ إذا زادت السعرات أو اختلّ التوزيع أو النسب الغذائية يسقط الطبق.

## How it works · كيف تعمل

| Rule | القاعدة |
|---|---|
| Block cells = kcal ÷ 70 (1–8) | عدد خلايا القطعة = السعرات ÷ 70 |
| Tilt = Σ(kcal × distance from pivot) ÷ budget | الميلان = مجموع (السعرات × البعد عن المحور) ÷ الميزانية |
| Falls if kcal > 115% budget, tilt > 15°, or macros extreme | يسقط إذا تجاوزت السعرات 115% أو الميلان 15° أو اختلت النسب |
| Ideal: protein 20–35%, carbs 40–55%, fat 20–35% | النسب المثالية: بروتين 20–35%، كربوهيدرات 40–55%، دهون 20–35% |

Nutrition values are approximate per 100 g. This is a game, not medical advice · القيم تقريبية واللعبة ليست نصيحة طبية.

## Run · التشغيل

No build step. Open `index.html`, or deploy on GitHub Pages:

1. Push `index.html` and `README.md` to a repo.
2. **Settings → Pages → Deploy from a branch → `main` / root**.
3. Your site is live at `https://<user>.github.io/<repo>/`.

## Roadmap · الخطوات القادمة

- Free-text ingredients → macros through an LLM API (use a small serverless proxy; never ship an API key in client code).
- Custom foods, saved meals, daily challenge.
- Real physics engine (Matter.js) for collapsing blocks.

## License

MIT
