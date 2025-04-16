# Návod k použití aplikace pro správu PDF dokumentů s využitím OCR technologie

Tento návod popisuje základní funkce aplikace pro správu PDF dokumentů a práci s rozpoznaným textem pomocí technologie OCR. Aplikace umožňuje správu souborů, vyhledávání v dokumentech a export výsledků.

---

### Přidávání souborů
<img width="1280" alt="dms" src="https://github.com/user-attachments/assets/c9cb39f4-56c4-49d8-88ef-3f52385cd1b5" />

Nové soubory lze do systému přidat pomocí tlačítka **„Nahrát soubor“** umístěného v uživatelském rozhraní modulu pro správu dokumentů (DMS). Po kliknutí se otevře dialog pro výběr souboru z počítače. Vybraný soubor je následně zkopírován do zvolené složky v rámci aplikace a ihned se zobrazí v seznamu.

---

### Kopírování souborů
<img width="1280" alt="CRUD" src="https://github.com/user-attachments/assets/f8cb3bf8-8191-42db-a1db-514ff0757938" />

Kopírování souboru nebo složky se provádí kliknutím pravým tlačítkem myši na požadovanou položku v seznamu a výběrem možnosti **„Kopírovat“** z kontextové nabídky. Poté lze přejít do jiné složky, kliknout pravým tlačítkem a zvolit **„Vložit“**, čímž se zkopírovaná položka vloží do nové lokace.

---

### Vyjmutí souborů
<img width="1280" alt="CRUD" src="https://github.com/user-attachments/assets/214483f0-3e8b-464f-a70a-8a1e37c0b4f7" />

Pro přesunutí souboru nebo složky slouží možnost **„Vyjmout“** v kontextové nabídce. Po zvolení této možnosti a přechodu do cílové složky lze položku vložit pomocí příkazu **„Vložit“**. Tím dojde k přesunutí položky bez jejího duplikování.

---

### Smazání souborů
<img width="1280" alt="CRUD" src="https://github.com/user-attachments/assets/ba73ea79-ef52-452a-abde-3c0120ae22d2" />

Smazání souboru nebo složky se provádí přes kontextovou nabídku po kliknutí pravým tlačítkem. Po výběru možnosti **„Smazat“** je uživatel vyzván k potvrzení akce. Po potvrzení je položka nevratně odstraněna z disku.

---

### Přejmenování souborů
<img width="1280" alt="CRUD" src="https://github.com/user-attachments/assets/58dad38d-4437-463b-833c-7fe481e1f798" />

Přejmenování se provádí opět prostřednictvím kontextové nabídky. Po výběru možnosti **„Přejmenovat“** lze zadat nový název, který bude použit bez změny přípony. Změna se aplikuje ihned po potvrzení.

---

### Vyhledávání v jednom dokumentu
<img width="1280" alt="Vyhledávání v souboru" src="https://github.com/user-attachments/assets/75049a01-9c98-4606-b474-0c7f3d8a311c" />

V pravém horním rohu modulu pro zobrazení dokumentu (PdfDisplay) se nachází tlačítko **„Hledat“**, které otevře panel pro vyhledávání. Uživatel zadá hledaný výraz a může pomocí tlačítek **„Hledat“**, **„Další“** a **„Předchozí“** procházet výskyty fráze. Výsledky jsou zvýrazněny přímo v OCR vrstvě dokumentu.

---

### Vyhledávání ve všech dokumentech
<img width="541" alt="Vyhledávání" src="https://github.com/user-attachments/assets/ddb672bb-3577-4eaa-8313-3c811132e19d" />

Tlačítko pro globální vyhledávání otevře samostatné vyhledávací okno. Do vstupního pole se zadá hledaný výraz a kliknutím na **„Hledat“** se spustí prohledávání všech OCR výstupů uložených v JSON souborech. Výsledky se zobrazují v seznamu spolu s počtem výskytů v jednotlivých dokumentech. Výběrem jednoho výsledku se daný dokument otevře s předvyplněným hledaným výrazem.

---

### Export výsledků vyhledávání do Excel tabulky
<img width="541" alt="Vyhledávání" src="https://github.com/user-attachments/assets/3a51f0f0-d664-4f48-9f35-db899daf1457" />

V globálním vyhledávacím okně lze kliknutím na tlačítko **„Export“** uložit výsledky do XLSX souboru. Exportovaný soubor obsahuje seznam všech dokumentů, kde se hledaný výraz vyskytuje, spolu s počtem výskytů v každém dokumentu. Tento soubor lze použít pro další zpracování nebo archivaci.

<img width="730" alt="Export" src="https://github.com/user-attachments/assets/05f60301-93be-46a6-a491-4d593699ff7b" />

---

## Administrátorský návod: Zprovoznění backendového API

Pro správné spuštění API s podporou OCR funkcionality je nutné mít k dispozici službu **Azure Document Intelligence**. Tato služba poskytuje OCR analýzu dokumentů a je nezbytnou součástí systému.

### Postup zprovoznění

1. **Získání přístupových údajů**
   - V Azure portálu si vytvořte (nebo použijte existující) službu Azure Document Intelligence.
   - Získané přihlašovací údaje obsahují:
     - `URL` služby
     - `KEY` pro autentizaci

2. **Nastavení konfiguračního souboru**
   - V repozitáři se **nenachází** soubor `appsettings.json`, protože je uveden v `.gitignore`.
   - Místo toho je k dispozici šablona `appsettings.json.template`, která obsahuje kompletní strukturu očekávaného konfiguračního souboru.
   - Pro nastavení postupujte následovně:
     1. Zkopírujte soubor `appsettings.json.template`.
     2. Přejmenujte kopii na `appsettings.json`.
     3. Vyplňte hodnoty `URL` a `KEY` ve vhodné sekci souboru.

3. **Příklad struktury souboru `appsettings.json`:**
  <img width="380" alt="image" src="https://github.com/user-attachments/assets/53b322d9-4048-4be7-a342-5230c8c5fe82" />


