# 🗺️ U.S. States Quiz Game

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Turtle](https://img.shields.io/badge/Turtle-Graphics-green)
![Pandas](https://img.shields.io/badge/pandas-latest-blue)
![Licensz](https://img.shields.io/badge/license-MIT-green)

*Teszteld tudásod az Egyesült Államok földrajzáról ebben a szórakoztató játékban!* 🎮

</div>

## 🎯 A Játék Célja

Ebben az interaktív földrajzi kvízjátékban a játékosnak meg kell neveznie az összes amerikai államot. A program egy üres USA térképet mutat, és a játékos feladata, hogy beírja az államok neveit. Minden helyes találat esetén az állam neve megjelenik a térképen a megfelelő helyen.

## 🎮 Játékmenet

- A játék egy üres USA térképpel indul
- A játékos beírja az államok neveit egyenként
- Helyes találat esetén az állam neve megjelenik a térképen
- A játék folyamatosan számolja a helyes találatokat
- A játék addig tart, amíg:
  - Mind az 50 államot kitaláltuk, vagy
  - A játékos beírja az "Exit" szót

## 📋 Funkciók

- 🎯 Valós idejű pontszámkövetés
- 🗺️ Vizuális visszajelzés a térképen
- 💾 Automatikus mentés a még nem kitalált államokról
- ⌨️ Egyszerű szöveges bevitel
- 🏆 Haladás követése (X/50 formátumban)

## ⚙️ Technikai Követelmények

| Követelmény | Verzió    |
|-------------|-----------|
| Python      | 3.x+      |
| turtle      | beépített |
| pandas      | latest    |

## 📁 Projekt Struktúra

```
us_states_game/
│
├── main.py                # Fő játék script
├── blank_states_img.gif   # Térkép háttér
├── 50_states.csv          # Államok koordinátái
└── states_to_learn.csv    # Generált tanulólista
```

## 🚀 Telepítés és Indítás

1. **Környezet Előkészítése**
```bash
# Függőségek telepítése
pip install pandas
```

2. **Játék Indítása**
```bash
python main.py
```

## 💻 Kód Részlet

```python
# Játék állapot inicializálása
screen = turtle.Screen()
screen.title("U.S. States Game")
image = "blank_states_img.gif"
screen.addshape(image)
turtle.shape(image)

# Államok betöltése
data = pandas.read_csv("50_states.csv")
all_states = data.state.to_list()
guessed_states = []
```

## 📊 Adatstruktúra

### 50_states.csv Formátum

| Oszlop | Típus    | Leírás                           |
|--------|----------|----------------------------------|
| state  | string   | Állam neve                       |
| x      | integer  | X koordináta a térképen          |
| y      | integer  | Y koordináta a térképen          |

## 🎯 Játék Tulajdonságok

- **Maximális Pontszám:** 50 pont (államonként 1 pont)
- **Időkorlát:** Nincs
- **Mentés:** Automatikus a kilépéskor
- **Nehézségi Szint:** Közepes

## 💡 Tippek a Játékhoz

1. Kezdd a parti államokkal
2. Használd a fővárosok tudásod
3. Gondolkozz régiónként
4. A nehezebb államokat hagyd későbbre

## 🤝 Közreműködés

Szívesen fogadjuk a fejlesztési javaslatokat! Ehhez:

1. Fork-old a repository-t
2. Hozz létre egy új branch-et (`git checkout -b feature/ujfunkcio`)
3. Commit-old a változtatásokat (`git commit -m 'Új funkció hozzáadása'`)
4. Push-old a branch-et (`git push origin feature/ujfunkcio`)
5. Nyiss egy Pull Request-et

## ✨ Szerző

[Az Ön Neve]

## 📝 Licensz

Ez a projekt [MIT](LICENSE) licensz alatt áll.

---

<div align="center">
Készült 🌎 és 🧠 segítségével

[Hibajelentés](https://github.com/namezor90/repo/issues) · [Funkció Kérése](https://github.com/namezor90/repo/issues)
</div>
