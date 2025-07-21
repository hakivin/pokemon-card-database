# 📦 Pokémon Card Database

This repository provides **JSON datasets of Pokémon TCG cards**.
Currently supports **Indonesia (id)**, and will be extended to support **other languages/regions** in the future.

---

## 📂 Folder Structure

```
/data
├── /id # Bahasa Indonesia datasets
│   ├── cards_SV7s.json
│   ├── cards_SV8s.json
│   ├── cards_SVI.json
│   ├── cards_SV11s.json
│   └── ... (other expansions)
├── /<other-language> # Planned soon
└── README.md
```

Each `.json` file contains cards from **one expansion**.

---

## 🔗 Example Usage (Download Raw JSON)

```
https://raw.githubusercontent.com/<your-username>/pokemon-card-database/main/data/id/cards_SV7s.json
```

In your app, fetch the file like this:

```dart
final url = 'https://raw.githubusercontent.com/hakivin/pokemon-card-database/main/data/id/cards_SV7s.json';
final response = await http.get(Uri.parse(url));
if (response.statusCode == 200) {
  final data = jsonDecode(response.body);
  print(data);
}
```

---

## 🚀 Purpose

* For use in apps to show Pokémon TCG card data.
* For hobby projects like deck builders, search engines, or collection managers.

---

## ⚠️ Disclaimer

These datasets are scraped **for educational & personal use only**.
Not affiliated with **The Pokémon Company** or **Creatures Inc.**

---

## 🛠️ Future Ideas

* Support `th`, `zh`, `ko`, etc. folders
* Search API
* Versioning system
