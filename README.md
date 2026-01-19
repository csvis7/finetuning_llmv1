**Finetuning 270M parameters model :**

(https://csvis-foodextract-v1.hf.space/)

%%writefile demos/FoodExtract/README.md

---
title: FoodExtract Fine-tuned LLM Structued Data Extractor
sdk: gradio
app_file: app.py
pinned: false
license: apache-2.0
---

"""
Fine-tuned Gemma 3 270M to extract food and drink items from raw text.

Input can be any form of real text and output will be a formatted string such as the following:

```
food_or_drink: 1
tags: fi, re
foods: tacos, milk, red apple, pineapple, cherries, fried chicken, steak, mayonnaise
drinks: iced latte, matcha latte
```

The tags map to the following items:

```
tags_dict = {'np': 'nutrition_panel',
 'il': 'ingredient list',
 'me': 'menu',
 're': 'recipe',
 'fi': 'food_items',
 'di': 'drink_items',
 'fa': 'food_advertistment',
 'fp': 'food_packaging'}
```
"""


%%writefile demos/FoodExtract/requirements.txt
```
transformers
gradio
torch
accelerate

```

**
