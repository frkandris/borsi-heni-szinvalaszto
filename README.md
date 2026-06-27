# Borsi & Heni Színválasztó

Egyszerű, egyetlen fájlból álló (`index.html`) webalkalmazás színpárok böngészéséhez és kedvenc-választó játékhoz. Nincs build, nincs külső függőség — bárhol megnyitható, és GitHub Pages szolgálja ki.

🔗 **Élő oldal:** https://frkandris.github.io/borsi-heni-szinvalaszto/

## Funkciók

A főoldalon két mód közül lehet választani:

### 📋 Lista megtekintése
Az összes színpár rácsos nézetben. Minden színpárt egy kör mutat, aminek bal fele az egyik, jobb fele a másik szín. Alatta a színek neve és hex kódja.

### 🎮 Játék
Osztott képernyő: **Borsi** és **Heni** egyszerre, egymás mellett játszik. Mindkét oldalon két színpár jelenik meg, és négyféleképpen lehet dönteni:

- **bal kör** → az nyer, a másik veszít
- **jobb kör** → az nyer, a másik veszít
- **👍 Mindkettő tetszik** → mindkét színpár nyer
- **👎 Egyik sem** → mindkét színpár veszít

A program először az adott játékos által még nem értékelt párokat ajánlja fel; ha elfogytak, véletlenszerűen választ.

### Állapot-lista
A játék alatt mindkét játékos teljes állapota látszik:

- ✅ **Nyert** · ❌ **Vesztett** · ⬜ **Nem értékelte még**
- 💖 **Mindkettőnknek tetszik** — azok a párok, amiket Borsi és Heni is megnyertnek jelölt

A nyert/vesztett elemeknél egy **↩** gombbal bármelyik színpárt vissza lehet küldeni „nem értékelte még" állapotba.

## Tárolás

Minden szavazat a böngésző `localStorage`-ában tárolódik (`szinvalaszto-votes-v1` kulcs), így az adatok megmaradnak az oldal újratöltése után is. Az adatok az adott böngészőhöz/eszközhöz kötöttek.

## Fejlesztés

Nincs telepítés. Szerkeszd az `index.html`-t, és nyisd meg böngészőben:

```sh
open index.html
```

A `main` ágra pusholt változások 1–2 percen belül automatikusan megjelennek a GitHub Pages oldalon.
