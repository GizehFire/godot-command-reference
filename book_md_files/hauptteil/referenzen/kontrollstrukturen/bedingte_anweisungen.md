# Bedingte Anweisungen

---

**In GDScript steuerst du den Programmfluss, indem du Bedingungen prüfst und abhängig vom Ergebnis verschiedene Blöcke ausführst. Die wichtigsten Schlüsselwörter sind `if`, `elif`, `else` und `match`.**

---

## `if`

Führt einen Block **nur dann** aus, wenn die angegebene Bedingung *wahr* ist.

## `elif`

Erweitert eine `if`‑Prüfung um zusätzliche Bedingungen, die in der Reihenfolge ihres Auftretens ausgewertet werden.

## `else`

Greift, wenn alle vorherigen Bedingungen *falsch* waren, und stellt damit den „Standard‑Fall“ dar.

## `match`  *(ab Godot 4)*

Vergleicht einen Ausdruck mit mehreren Mustern; ähnlich einem `switch` und besonders nützlich bei vielen möglichen Ausprägungen.

---

###  _1. Beispiel:_

```gdscript
if coins > 0:
    buy_item()
else:
    show_message("Not enough coins")
```

### _2. Beispiel:_

```gdscript
if score >= 1000:
    rank = "Gold"
elif score >= 500:
    rank = "Silver"
else:
    rank = "Bronze"
```

### Wichtige Hinweise

* **Tab‑Einrückung Pflicht:** Ab Godot 4.4 müssen Blöcke mit einem Tabulator eingerückt sein; Leerzeichen werden nicht akzeptiert.
* Bedingungen werden **von oben nach unten** geprüft; die erste zutreffende Bedingung entscheidet, welcher Block ausgeführt wird.

---

| Schlüsselwort | Zweck                | Kurzform           |
| ------------- | -------------------- | ------------------ |
| `if`          | prüft eine Bedingung | „falls“            |
| `elif`        | weitere Bedingung    | „ansonsten, falls“ |
| `else`        | Standard‑Fall        | „ansonsten“        |
| `match`       | Muster­vergleich     | „switch“           |
