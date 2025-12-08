# Project Outcomes

## 🔖 Stav projektu
Projekt LED Piano Trainer je v stave plne funkčného prototypu.  
Hardvérová časť je kompletná – 3D tlačená LED nadstavba pre 2 oktávy, úspešne prispôsobená LED pásu s rôznym rozstupom, a 3D tlačená krabička pre Raspberry Pi Pico a kabeláž.  
Softvérová pipeline je funkčná v základnej podobe: program dokáže detegovať MIDI zariadenie, pracovať s transkripciou skladieb a pripravuje dáta pre LED sekvencie.

---

## 🧩 Výstupy podľa SDLC / V-modelu

### 1. Business požiadavky  
- Uľahčiť učenie hry na klavíri pomocou vizuálnych LED indikátorov.  
- Vytvoriť fyzickú nadstavbu, ktorá funguje na bežnom MIDI keyboarde bez zásahu do kláves.  
- Dodať riešenie, ktoré môžu používať úplní začiatočníci a deti.  

### 2. Top Level Architecture  
- **Hardware Layer:**  
  - AKAI LPK25 MIDI keyboard  
  - 3D tlačená LED nadstavba pre 25 kľúčov  
  - WS2812B adresovateľný LED pás  
  - Raspberry Pi Pico (MicroPython)  
- **Software Layer:**  
  - PC aplikácia pre transkripciu a odosielanie dát  
  - Firmware na Pico pre riadenie LED sekvencií  

### 3. Solution Architecture  
- PC aplikačná vrstva generuje MIDI alebo konvertuje YouTube → MIDI.  
- Prenos MIDI udalostí cez USB do Raspberry Pico.  
- Pico mapuje noty na LED indexy a spúšťa farebné sekvencie.  
- 3D nadstavba zabezpečuje fyzickú izoláciu svetla pre každý kláves.

### 4. Analysis  
- LED pás má odlišné rozostupy ako klávesy → nutné ohýbanie.  
- Čierne klávesy spôsobujú nerovnomerné rozloženie → použitie jednotných boxov.  
- Potreba samostatného boxu pre posledný kláves (chyba v prvom návrhu).  

### 5. Design  
- Testovanie rôznych hrúbok priečok medzi LED boxmi.  
- Výber šírky, ktorá poskytuje najlepšiu svetelnú difúziu.  
- Modulárna nadstavba umožňujúca tlač po častiach.  
- 3D box pre Raspberry na estetické a bezpečné usporiadanie káblov.

### 6. Implementation  
- Ohýbanie LED pásu tak, aby každý pixel sedel presne pod jedným boxom.  
- Tlač finálnej dvojoktávovej lišty + doplnkový box pre posledný kláves.  
- Tlač krabičky pre Raspberry + káble.  
- Prvé verzie firmvéru a testovanie sekvencií.

### 7. Verification & Testing  
- Test rovnomernosti svetla medzi boxmi.  
- Kontrola správnej pozície LED pre každý kláves.  
- Testovanie prevádzky s MIDI keyboardom.  
- Kontrola PC aplikácie na detekciu zariadení a odosielanie dát.

### 8. Operation  
- Prototyp je schopný interpretovať jednoduché LED sekvencie podľa zadaných MIDI udalostí.  
- Je možné rozšíriť ho o režim učenia, tempo kontrolu a ďalšie funkcionality.

---

## 🏆 Finálny produkt

### 🔧 Hardvérový výsledok
Po sérii experimentov s hrúbkou priečok a ohýbaním LED pásu vznikla plne funkčná svetelná nadstavba, ktorá rovnomerne osvetľuje jednotlivé klávesy.

#### Prvá verzia (chybná – chýbajúci posledný box)
![LED bar v prvej verzii](./images/ledbar_v1.png)

#### Opravená finálna verzia s doplneným boxom
![LED bar final](./images/ledbar_final.png)

#### 3D tlačená krabička pre Raspberry + káble
![Raspberry box](./images/raspberry_box.png)

### 💻 Softvérový výsledok
Finálna verzia PC aplikácie obsahuje:
- MIDI detekciu  
- prepojenie s Pico  
- generovanie LED sekvencií z MIDI alebo automatickej transkripcie  

![Piano Trainer App](./images/piano_trainer_app.png)

### 🎬 Demo video
*(bude doplnené)*  
> YouTube demonštrácia LED reakcií na prehrávané tóny.

### 📦 Celkový dodaný produkt
- 3D tlačená LED nadstavba → **kompletne funkčná**  
- Krabička pre Raspberry → **hotová**  
- Prepojenie keyboard → PC → Pico → LED → **funguje**  
- PC aplikácia → **funkčný prototyp (demo-ready)**  
- Firmware pre Pico → **stabilný základ**  

Repozitár: *(bude doplnené)*

---

## 🧭 Porovnanie s Project Summary

### 🔹 Čo sme plánovali
- Vytvoriť LED nadstavbu pre 2 oktávy  
- Implementovať mapovanie not → LED  
- Spraviť prototyp PC aplikácie  
- Vyrobiť krabičku pre Raspberry  
- Mať demo video  

### 🔹 Čo sme skutočne dodali
| Plán | Realita |
|------|---------|
| LED nadstavba pre 2 oktávy | ✔️ Dodané (vylepšené po chybnej prvej verzii) |
| Mapovanie not → LED | ✔️ Funkčné základné sekvencie |
| PC aplikácia | ✔️ GUI + MIDI detekcia + pipeline |
| Krabička pre Raspberry | ✔️ Vytlačená a funkčná |
| Demo video | 🔄 Pripravuje sa |

🟣 **Výsledok:** Projekt prekročil pôvodné očakávania v kvalite hardvéru a estetickom prevedení. Softvér existuje ako funkčný prototyp pripravený na ďalší rozvoj.

---

## Navigácia
- [↩️ Späť](../index.md)
