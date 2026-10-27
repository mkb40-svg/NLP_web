# Алгоритмы NLP · NLP algoritmlari

Виртуальные лаборатории и практикумы по курсу «Алгоритмы NLP» на двух языках: русском и узбекском.
«NLP algoritmlari» kursi boʻyicha virtual laboratoriyalar va amaliy mashgʻulotlar, ikki tilda: rus va oʻzbek.

```
index.html            выбор языка / tilni tanlash
config.js             настройка кнопок Colab (см. ниже) / Colab tugmalari sozlamasi
ru/index.html         оглавление на русском
ru/labs/              18 лабораторий (HTML, работают без интернета)
ru/notebooks/         18 практикумов для Google Colab (.ipynb)
uz/index.html         oʻzbekcha mundarija
uz/labs/              18 ta laboratoriya
uz/notebooks/         18 ta amaliy mashgʻulot
.nojekyll             служебный файл для GitHub Pages
```

## Публикация на GitHub Pages

1. Распакуйте архив на компьютере. Загружать в репозиторий нужно **содержимое** папки `nlp-labs`
   (index.html, config.js, папки ru и uz), а не сам zip-файл: GitHub не распаковывает архивы.
   Проще всего это сделать через GitHub Desktop или командой `git push`; через сайт папки загружаются
   перетаскиванием в окно «Upload files» в Chrome или Edge.
2. В репозитории: Settings → Pages → Source: Deploy from a branch → main → / (root) → Save.
3. Через 1–2 минуты сайт откроется по адресу `https://<пользователь>.github.io/<репозиторий>/`.
4. Репозиторий должен быть публичным (Public), иначе Colab не сможет открыть практикумы.

Курс можно положить и подпапкой в уже существующий репозиторий (например, рядом с лабораториями по
кластеризации): адрес будет `https://<пользователь>.github.io/<репозиторий>/<папка>/`, кнопки Colab найдут
папку сами.

Кнопки «Практикум в Colab» на GitHub Pages настраиваются сами. Если сайт размещён в другом месте (Vercel,
Netlify, сервер университета), откройте `config.js` и впишите, где на GitHub лежат ноутбуки:
`window.NLP_LABS = { repo: "пользователь/репозиторий", branch: "main", folder: "" };`
(`folder` — подпапка курса внутри репозитория, если она есть).

Без интернета: откройте `index.html` двойным щелчком. Лаборатории работают полностью, а вместо кнопки Colab
будет ссылка на скачивание .ipynb (его можно загрузить в Colab через «Файл → Загрузить блокнот»).

## Vercel (по желанию)

vercel.com → войти через GitHub → Add New → Project → выбрать репозиторий → Framework Preset: Other,
Build Command и Output Directory оставить пустыми → Deploy. После этого заполните `config.js`, как описано выше.

## Практикумы

Каждый практикум запускается в Google Colab без установки. Ячейки, помеченные тегом `colab-only`, скачивают
настоящие модели с Hugging Face (размер указан в ячейке). Им нужен интернет, и они работают только в Colab.
Остальные ячейки выполняются за 1–2 минуты.

---

## GitHub Pages’da eʼlon qilish

1. Arxivni kompyuterda oching. Repozitoriyaga zip-faylning oʻzini emas, `nlp-labs` papkasining **ichidagilarini**
   (index.html, config.js, ru va uz papkalari) yuklash kerak: GitHub arxivlarni ochmaydi.
2. Repozitoriyada: Settings → Pages → Source: Deploy from a branch → main → / (root) → Save.
3. 1–2 daqiqadan keyin sayt `https://<foydalanuvchi>.github.io/<repozitoriya>/` manzilida ochiladi.
4. Repozitoriya ochiq (Public) boʻlishi kerak, aks holda Colab amaliy mashgʻulotlarni ocha olmaydi.

Kursni mavjud repozitoriyaning ichki papkasiga ham joylash mumkin: Colab tugmalari papkani oʻzi topadi.

GitHub Pages’da «Colab» tugmalari oʻzi sozlanadi. Sayt boshqa joyda boʻlsa (Vercel, universitet serveri),
`config.js` faylida repozitoriya manzilini yozing:
`window.NLP_LABS = { repo: "foydalanuvchi/repozitoriya", branch: "main", folder: "" };`

## Amaliy mashgʻulotlar

Har bir mashgʻulot Google Colabʼda oʻrnatishsiz ishga tushadi. `colab-only` tegi qoʻyilgan kataklar Hugging Face’dan
haqiqiy modellarni yuklab oladi (hajmi katakda koʻrsatilgan); ularga internet kerak va ular faqat Colabʼda ishlaydi.
Qolgan kataklar 1–2 daqiqada bajariladi.

Internetsiz: `index.html` faylini oching. Laboratoriyalar toʻliq ishlaydi, Colab tugmasi oʻrniga .ipynb faylini
yuklab olish havolasi chiqadi.
