# Návod k použití aplikace pro správu PDF dokumentů s využitím OCR technologie

Tento návod popisuje základní funkce aplikace pro správu PDF dokumentů a práci s rozpoznaným textem pomocí technologie OCR. Aplikace umožňuje správu souborů, vyhledávání v dokumentech a export výsledků.

---

### Přidávání souborů

Nové soubory lze do systému přidat pomocí tlačítka **„Nahrát soubor“** umístěného v uživatelském rozhraní modulu pro správu dokumentů (DMS). Po kliknutí se otevře dialog pro výběr souboru z počítače. Vybraný soubor je následně zkopírován do zvolené složky v rámci aplikace a ihned se zobrazí v seznamu.

---

### Kopírování souborů

Kopírování souboru nebo složky se provádí kliknutím pravým tlačítkem myši na požadovanou položku v seznamu a výběrem možnosti **„Kopírovat“** z kontextové nabídky. Poté lze přejít do jiné složky, kliknout pravým tlačítkem a zvolit **„Vložit“**, čímž se zkopírovaná položka vloží do nové lokace.

---

### Vyjmutí souborů

Pro přesunutí souboru nebo složky slouží možnost **„Vyjmout“** v kontextové nabídce. Po zvolení této možnosti a přechodu do cílové složky lze položku vložit pomocí příkazu **„Vložit“**. Tím dojde k přesunutí položky bez jejího duplikování.

---

### Smazání souborů

Smazání souboru nebo složky se provádí přes kontextovou nabídku po kliknutí pravým tlačítkem. Po výběru možnosti **„Smazat“** je uživatel vyzván k potvrzení akce. Po potvrzení je položka nevratně odstraněna z disku.

---

### Přejmenování souborů

Přejmenování se provádí opět prostřednictvím kontextové nabídky. Po výběru možnosti **„Přejmenovat“** lze zadat nový název, který bude použit bez změny přípony. Změna se aplikuje ihned po potvrzení.

---

### Vyhledávání v jednom dokumentu

V pravém horním rohu modulu pro zobrazení dokumentu (PdfDisplay) se nachází tlačítko **„Hledat“**, které otevře panel pro vyhledávání. Uživatel zadá hledaný výraz a může pomocí tlačítek **„Hledat“**, **„Další“** a **„Předchozí“** procházet výskyty fráze. Výsledky jsou zvýrazněny přímo v OCR vrstvě dokumentu.

---

### Vyhledávání ve všech dokumentech

Tlačítko pro globální vyhledávání otevře samostatné vyhledávací okno. Do vstupního pole se zadá hledaný výraz a kliknutím na **„Hledat“** se spustí prohledávání všech OCR výstupů uložených v JSON souborech. Výsledky se zobrazují v seznamu spolu s počtem výskytů v jednotlivých dokumentech. Výběrem jednoho výsledku se daný dokument otevře s předvyplněným hledaným výrazem.

---

### Export výsledků vyhledávání do Excel tabulky

V globálním vyhledávacím okně lze kliknutím na tlačítko **„Export“** uložit výsledky do XLSX souboru. Exportovaný soubor obsahuje seznam všech dokumentů, kde se hledaný výraz vyskytuje, spolu s počtem výskytů v každém dokumentu. Tento soubor lze použít pro další zpracování nebo archivaci.
