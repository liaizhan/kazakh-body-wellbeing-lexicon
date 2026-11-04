# Kazakh body and well-being lexicon

A small parallel lexicon in **Kazakh, Russian and English**: 83 everyday
health topics women search for (body parts, symptoms, common conditions),
the words people actually type when they look for them, a short life theme
for each topic, and the WHO-5 Well-Being Index wording in all three languages.

Kazakh texts about the body and psychosomatics are rare online. This set is
meant for people who build search, chat assistants, keyword tools or
classifiers that should understand Kazakh users, including the common habit
of mixing Kazakh and Russian words in one query.

## What is inside

| File | Rows | What it holds |
| --- | --- | --- |
| `data/terms.csv` | 83 | Topic name and life theme in kk, ru, en, plus the source page in each language |
| `data/terms.jsonl` | 83 | The same topics with keyword lists, one JSON object per line |
| `data/keywords.csv` | 1,913 | Long format: `slug, lang, keyword` (kk 636, ru 587, en 690) |
| `data/who5.kk.json`, `who5.ru.json`, `who5.en.json` | 3 | WHO-5 questions, answer labels and result messages |

Example row (`terms.jsonl`, shortened):

```json
{"slug":"shchitovidnaya-zheleza",
 "name":{"kk":"Қалқанша без","ru":"Щитовидная железа","en":"Thyroid gland"},
 "theme":{"kk":"Өмір қарқыны және «үлгермеймін» сезімі","ru":"Темп жизни и чувство «я не успеваю»","en":"The pace of life and the feeling “I can't keep up”"},
 "keywords":{"kk":["қалқанша без","жемсау","қалқанша без түйіні","тиреоидит","..."],"ru":["щитовидка","зоб","..."],"en":["thyroid","goiter","..."]},
 "source":{"kk":"https://108psy.com/kk/psihosomatika/shchitovidnaya-zheleza","ru":"...","en":"..."}}
```

## How it was made

Every topic comes from a published page of the section on women's
psychosomatics at [108psy.com](https://108psy.com/psihosomatika), which
exists in Russian, Kazakh and English. The Russian page is the original.
The Kazakh and English pages are translations. Each row links to all three
pages, so you can check the context of any word.

Keywords are search phrases written for those pages. Kazakh keyword lists
deliberately contain some Russian words (for example `щитовидка`), because
many Kazakh speakers search that way. If you need pure Kazakh, filter by
the Kazakh letters ә ғ қ ң ө ұ ү һ і or review the list by hand.

## Limits, please read

- **Not a medical resource.** Topic names are plain words, not diagnoses.
  The life themes are questions for reflection from the Ladder method by
  Aizhan Li. They do not describe causes of any illness.
- **Translation quality.** The Kazakh texts were reviewed by the author
  before publication on the site. They were not checked by a professional
  translator or a linguist. Corrections are welcome as issues or pull requests.
- **WHO-5 wording.** The WHO-5 Well-Being Index was developed by the WHO
  Regional Office for Europe (1998) and is free to use, see
  [who-5.org](https://www.who-5.org). The Kazakh and Russian wordings here
  are working translations, not official validated versions. Do not use
  them for clinical research without validation.
- **Women's topics.** The source section is written for women, so the topic
  list leans toward gynecology and women's health.

## Қысқаша (kk)

Қазақ, орыс және ағылшын тілдеріндегі 83 тақырып: дене мүшелері, белгілер,
жиі кездесетін жағдайлар, адамдар іздейтін сөздер және ДДҰ-5 сауалнамасы.
Бұл дәрігерлік анықтама емес. Қазақ мәтінін автор тексерген, кәсіби аудармашы
тексермеген. Түзетулерді issue немесе pull request арқылы жіберіңіз.

## Кратко (ru)

83 темы на казахском, русском и английском: части тела, признаки, частые
состояния, слова, которыми их ищут, и опросник ВОЗ-5. Это не медицинский
справочник. Казахский текст проверен автором, профессиональный переводчик
его не проверял. Исправления присылайте через issue или pull request.

## Related

- [ladder-who5](https://github.com/liaizhan/ladder-who5): WHO-5 scoring and
  Ladder method question templates, with a browser demo.
- [chatgpt-plugin-one-tool](https://github.com/liaizhan/chatgpt-plugin-one-tool):
  a minimal MCP server with one WHO-5 tool and notes on the OpenAI review.

## License and citation

Data: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
Attribution: "Aizhan Li, author of the Ladder method, 108psy.com".
See `CITATION.cff` for a citation entry.
