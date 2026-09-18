
# Názov projektu
- **Názov projektu**: RC cars
- **Meno riešiteľa**: 

---

## Dôvod a okolnosti zavedenia riešenia
Projekt vznikol ako podklad na Stredoškolskú odbornú činnosť (SOČ) a praktickú časť maturitnej skúšky. Jeho cieľom je ukázať vedomosti, zručnosti a skúsenosti ktoré môže študent nadobudnúť počas 4 rokoch štúdia na škole. 

---

## Slovné zadanie, popis projektu od zákazníka
Cieľom projektu je navrhnúť, zostrojiť a naprogramovať autá na diaľkové ovládanie, ktoré budú ovládané pomocou buď aplikácie v mobile, alebo pomocou diaľkových ovládačov. Funkcionalita aplikácie bude zahŕňať nielen samotné ovládanie vozidla ale aj vytváranie profilov, zobrazovanie rebríčkov, meranie času a počítanie kôl.

---

## Seznam modulů projektu a jejich významných atributů
1. **Modul ovládanie vozidla**
   - Atribúty: smer, rýchlosť
   - Unikátna identifikácia objektov: ID vozidla

2. **Modul používateľských profilov**
   - Atribúty: meno, dosiahnuté výsledky
   - Unikátna identifikácia objektov: ID užívateľa

3. **Modul merania času a kôl**
   - Atribúty: čas kola, počet kôl
   - Unikátna identifikácia objektov: ID jazdy

4. **Modul rebríčkov**
   - Atribúty: používateľ, čas kola, umiestnenie
   - Unikátna identifikácia objektov: ID výsledku

---

## Systémové požiadavky FURPS
1. **Funkčnosť (Functionality - F)**
   - Ovládanie vozidla pomocou aplikácie alebo ovládača
   - Tvorba a správa používateľských profilov
   - Meranie času
   - Zobrazenie výsledkov

3. **Vhodnosť k použitiu (Usability - U)**
   - Jednoduché ovládanie vozidla
   - Jednoduché používateľské rozhranie

4. **Spoľahlivosť (Reliability - R)**
   - Mikrokontrolér ktoré komunikuje s aplikáciou
   - Správne zaznamenávanie času a počtu kôl

5. **Výkon (Performance - P)**
   - Aplikácia nebude náročná na hardvér
   - Ovládanie vozidla bude bez výrazného oneskorenia
   
7. **Schopnosť údržby (Supportability - S)**
   - Možnosť jednoducho pridať a upraviť vozidlá
   - Možnosť jednoducho upravovať a rozširovať aplikáciu 

---

## Kritické situácie
1. **Systémové**
   - Výpadok napájania: Vozidlo nebude schopné pohybu ani komunikácie
   - Zlyhanie hardware: Poškodenie senzorov alebo mikrokontroléra 

2. **Aplikačné**
   - Problémy s komunikáciou medzi mikrokontroléra a aplikáciou
   - Výpadok internetu by viedlo k strate aktuálnych údajov z rebríčka

---

## Tri situácie definujúce hranice systému
1. **Ideálny scenár**
   - Systém úspešne vykoná diagnostiku, zobrazuje chybové kódy a poskytuje potrebné informácie pre opravu vozidla.

2. **Hranične riešiteľný scenár**
   - Systém nedokáže identifikovať konkrétnu závadu, ale poskytne návrh na ďalšiu diagnostiku.

3. **Situácie, ktoré systém nezvládne**
   - Systém nie je schopný vykonať diagnostiku v prípade úplného zlyhania ECU alebo riadiacej jednotky.

---

## Kontext prostredia
Systém by mal byť použitý iba v interiéri, na uzavretých tratiach, ktoré budú zaevidované v aplikácii.

---

## Charakteristika aktérov a prostredia
- **Aktéri**: Používateľ, správca aplikácie, technik
- **Prostredie**: Interiéri, uzavretá trať

---

## Use Case diagram
<img width="1920" height="1080" alt="Use Case diagram" src="https://github.com/user-attachments/assets/97de3123-8d9a-431b-8604-cfac14a1a40f" />

---

## Scenáre - konkrétna implementácia Use Case

**1. Ovládanie vozidla**  
   - **Názov**: Ovládanie RC auta  
   - **Kontext**: Používateľ chce ovládať RC vozidlo  
   - **Level zanoření Use Case**: Hlavný scénar  
   - **Aktéri**: Používateľ, mikrokontrolér
   - **Vstupné podmienky**: Používateľ je prihlásený  
   - **Výstupné podmienky**: Vozidlo reaguje na príkazy používateľa  
   - **Minimálny výstup**: Používateľ ovláda vozidlo
   - **Ideálny výstup**: Používateľ ovláda vozidlo bez výrazného oneskorenia a reaguje na všetky príkazy

**Hlavný scénár**:  
1. Používateľ sa prihlási do aplikácie
2. Používateľ si vyberie vozidlo
3. Aplikácia odosiela príkazy mikrokontroléru
4. Mikrokontrolér spracuje prijaté príkazy
5. Vozidlo vykoná požadovaný pohyb


**Rozšírenie**:  
- Ak užívateľ nie je prihlásený tak ho aplikácia vyzve na prihlásenie
- Ak dôjde k strate signálu tak sa vozidlo zastaví

---

## Sekvenčný diagram
<img width="1920" height="1080" alt="Sekvenčný diagram" src="https://github.com/user-attachments/assets/ea253d4c-89a4-44bf-88bc-8029d835bf9e" />

---

## Triedny diagram
<img width="1449" height="1086" alt="Triedny Diagram" src="https://github.com/user-attachments/assets/19c2285c-a8f2-484e-b285-ee6ad38f4a79" />

---
