### Konfigurace backend API
*Klíčová slova: `konfigurace`, `nastavení`, `backend`, `api`, `azure`, `document intelligence`, `appsettings.json`, `key`*

Před spuštěním aplikace je nutné nakonfigurovat backend API tak, aby mělo přístup ke službě Azure Document Intelligence a mohlo správně obsluhovat OCR požadavky.

#### 1. Získání přístupových údajů z Azure
- Přihlaste se do Azure portálu.
- Vytvořte (nebo znovu použijte) instanci služby **Azure Document Intelligence**.
- Z portálu získejte:
  - **URL endpoint** služby (např. `https://<název>.cognitiveservices.azure.com/`)
  - **API klíč (Key)** — slouží pro autentizaci.

#### 2. Konfigurace souboru `appsettings.json`
- V kořenovém adresáři backendové aplikace se nenachází soubor `appsettings.json`, protože je uveden v `.gitignore`.
- Místo něj je k dispozici soubor `appsettings.json.template`, který obsahuje očekávanou strukturu.
- Postup:
  1. Zkopírujte soubor `appsettings.json.template`.
  2. Přejmenujte jej na `appsettings.json`.
  3. Otevřete nově vytvořený soubor a doplňte hodnoty v sekci `Api`.

#### 3. Příklad výsledného `appsettings.json`:
```json
{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft.AspNetCore": "Warning"
    }
  },
  "AllowedHosts": "*",
  "Api": {
    "Url": "https://<vaše-služba>.cognitiveservices.azure.com/",
    "Key": "<váš-api-klíč>"
  }
} 
```

---

[⬅️ Zpět na hlavní stránku manuálu](../README.md)
