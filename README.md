# PDO semestrální práce
# Aplikace pro správu PDF dokumentů s využitím OCR technologie

# use cases


## Přidání dokumentu
**Aktér:** Uživatel  

### Hlavní scénář:
1. Uživatel nahraje dokument do systému.
2. Systém automaticky spustí OCR (Optical Character Recognition) pro extrakci textu.
3. Rozpoznaný text je uložen spolu s dokumentem.

### Alternativní scénáře:
- Pokud OCR selže, systém upozorní uživatele a nabídne možnost opětovného nahrání.

## Nahrání dokumentu
**Aktér:** Uživatel  

### Hlavní scénář:
1. Uživatel vybere dokument z lokálního úložiště.
2. Systém ověří formát a velikost dokumentu.
3. Dokument je uložen do databáze.

### Související use case:
- **Správa dokumentů (CRUD operace):**  
  - **Vytvoření:** Uložení nového dokumentu.  
  - **Čtení:** Zobrazení seznamu dokumentů.  
  - **Aktualizace:** Úprava metadat dokumentu.  
  - **Smazání:** Odstranění dokumentu z databáze.  

## Dotaz s hledanou frází v dokumentu
**Aktér:** Uživatel  

### Hlavní scénář:
1. Uživatel zadá hledanou frázi.
2. Uživatel zvolí, zda chce vyhledávat v jednom nebo více dokumentech.
3. Systém prohledá texty dokumentů a vrátí výsledky.
4. Výsledky jsou zvýrazněny v dokumentech.

### Poduse case:
- **Vyhledávání v jednom dokumentu:** Uživatel vybere konkrétní dokument.
- **Vyhledávání ve více dokumentech:** Systém prohledá všechny dostupné dokumenty.
- **Export výsledků:** Výsledky jsou uloženy do Excelové tabulky (včetně počtu výskytů a odkazů na stránky).

## Správa dokumentů (CRUD operace)
**Aktér:** Administrátor/Uživatel s oprávněním  

### Scénáře:
- **Vytvoření dokumentu:** Nahrání nového souboru.
- **Čtení dokumentu:** Prohlížení obsahu nebo metadat.
- **Aktualizace dokumentu:** Změna názvu, kategorie nebo dalších atributů.
- **Smazání dokumentu:** Trvalé odstranění z databáze.

## Export výsledků do Excelu
**Aktér:** Uživatel  

### Hlavní scénář:
1. Po vyhledání fráze uživatel zvolí možnost „Exportovat výsledky“.
2. Systém vygeneruje Excelovou tabulku s:
   - Názvy dokumentů obsahujících frázi.
   - Počtem výskytů v každém dokumentu.
   - Odkazy na konkrétní stránky/oddíly.
3. Soubor je stažen do zařízení uživatele.
