# Gingles.co — Funkční checklist celého webu

**Projekt:** Gingles.co  
**Typ dokumentu:** Funkční checklist  
**Autor:** Iryna Aleksandrova  
**Datum vytvoření:** 16.12.2025  
**Verze:** 1.0  
**Cíl:** Základní kontrola klíčové funkčnosti webu Gingles.co (katalog, filtrování, košík, objednávka, účet, navigace).

---

## Legenda

- **Priorita:**  
  - High — kritická funkčnost (objednávka, platba, dostupnost webu)  
  - Medium — důležitá funkčnost (pohodlí, konverze)  
  - Low — doplňková funkčnost  

- **Status:**  
  - Netestováno  
  - OK  
  - Chyba  
  - N/A  

---

## Navigace a dostupnost

| ID     | Sekce       | Kontrolní bod                                              | Priorita | Status      | Poznámky |
|--------|-------------|------------------------------------------------------------|----------|-------------|----------|
| NAV-01 | Navigace    | Domovská stránka se načítá bez chyb (HTTP 200)             | High     | Netestováno |          |
| NAV-02 | Navigace    | Hlavní menu je viditelné na všech klíčových stránkách      | High     | Netestováno |          |
| NAV-03 | Navigace    | Logo vede zpět na domovskou stránku                        | Medium   | Netestováno |          |
| NAV-04 | Navigace    | Interní odkazy nevedou na 404 / prázdné stránky            | High     | Netestováno |          |
| NAV-05 | Navigace    | Web se správně otevírá v Chrome, Firefox, Edge             | High     | Netestováno |          |


| ID     | Sekce       | Kontrolní bod                                                   | Priorita | Status      | Poznámky |
|--------|-------------|-----------------------------------------------------------------|----------|-------------|----------|
| CAT-01 | Katalog     | Stránka katalogu se načítá bez chyb                             | High     | Netestováno |          |
| CAT-02 | Katalog     | Produkty mají název, cenu a obrázek                             | High     | Netestováno |          |
| CAT-03 | Katalog     | Kliknutí na produkt vede na detail produktu                     | High     | Netestováno |          |
| CAT-04 | Katalog     | Počet produktů odpovídá očekávání (paginace / infinite scroll)  | Medium   | Netestováno |          |
| CAT-05 | Katalog     | Při prázdném katalogu se zobrazí jasná zpráva                   | Medium   | Netestováno |          |



## Filtrování a řazení

| ID     | Sekce       | Kontrolní bod                                              | Priorita | Status      | Poznámky |
|--------|-------------|------------------------------------------------------------|----------|-------------|----------|
| FLT-01 | Filtrování  | Filtrovací prvky jsou viditelné a klikatelné               | High     | Netestováno |          |
| FLT-02 | Filtrování  | Aplikace filtru aktualizuje seznam produktů                | High     | Netestováno |          |
| FLT-03 | Filtrování  | Reset filtrů vrátí kompletní seznam produktů               | Medium   | Netestováno |          |
| FLT-04 | Řazení      | Řazení podle ceny (vzestupně/sestupně) funguje správně     | Medium   | Netestováno |          |
| FLT-05 | Řazení      | Řazení podle popularity/novinek funguje správně            | Low      | Netestováno |          |

---

## Detail produktu

| ID     | Sekce         | Kontrolní bod                                              | Priorita | Status      | Poznámky |
|--------|---------------|------------------------------------------------------------|----------|-------------|----------|
| PDP-01 | Detail        | Stránka produktu se načítá z katalogu i přímým odkazem     | High     | Netestováno |          |
| PDP-02 | Detail        | Zobrazuje se název, cena a popis produktu                  | High     | Netestováno |          |
| PDP-03 | Detail        | Zobrazuje se hlavní obrázek produktu                       | High     | Netestováno |          |
| PDP-04 | Detail        | Tlačítko „Přidat do košíku“ je viditelné a funkční         | High     | Netestováno |          |
| PDP-05 | Detail        | Po přidání do košíku se zobrazí potvrzení / změna stavu    | High     | Netestováno |          |

---

## Košík

| ID       | Sekce | Kontrolní bod                                               | Priorita | Status      | Poznámky |
|----------|-------|-------------------------------------------------------------|----------|-------------|----------|
| CART-01  | Košík | Stránka košíku je dostupná z hlavičky/menu                  | High     | Netestováno |          |
| CART-02  | Košík | Přidané produkty se zobrazují správně                       | High     | Netestováno |          |
| CART-03  | Košík | Lze změnit množství produktu                                | High     | Netestováno |          |
| CART-04  | Košík | Lze odstranit produkt z košíku                              | High     | Netestováno |          |
| CART-05  | Košík | Celková cena se přepočítá po změně množství/odstranění      | High     | Netestováno |          |

---

## Objednávka (Checkout)

| ID      | Sekce     | Kontrolní bod                                              | Priorita | Status      | Poznámky |
|---------|-----------|------------------------------------------------------------|----------|-------------|----------|
| CHK-01  | Checkout  | Přechod z košíku na objednávku funguje                     | High     | Netestováno |          |
| CHK-02  | Checkout  | Povinná pole jsou označena a validována                    | High     | Netestováno |          |
| CHK-03  | Checkout  | Chyby se zobrazují při nevyplněných povinných polích       | High     | Netestováno |          |
| CHK-04  | Checkout  | Výběr dopravy funguje správně                              | High     | Netestováno |          |
| CHK-05  | Checkout  | Výběr platby funguje správně                               | High     | Netestováno |          |
| CHK-06  | Checkout  | Úspěšná objednávka vede na potvrzovací stránku             | High     | Netestováno |          |

---

## Vyhledávání

| ID       | Sekce      | Kontrolní bod                                             | Priorita | Status      | Poznámky |
|----------|------------|-----------------------------------------------------------|----------|-------------|----------|
| SRCH-01  | Vyhledávání| Vyhledávací pole je viditelné a aktivní                   | Medium   | Netestováno |          |
| SRCH-02  | Vyhledávání| Vyhledání existujícího produktu vrací relevantní výsledky | Medium   | Netestováno |          |
| SRCH-03  | Vyhledávání| Neexistující dotaz zobrazí informaci „nic nenalezeno“     | Low      | Netestováno |          |

---

## Uživatelský účet (pokud existuje)

| ID      | Sekce   | Kontrolní bod                                               | Priorita | Status      | Poznámky |
|---------|---------|-------------------------------------------------------------|----------|-------------|----------|
| ACC-01  | Účet    | Stránka přihlášení je dostupná                              | Medium   | Netestováno |          |
| ACC-02  | Účet    | Přihlášení s platnými údaji je úspěšné                      | High     | Netestováno |          |
| ACC-03  | Účet    | Chyba při neplatných údajích se zobrazí správně             | High     | Netestováno |          |
| ACC-04  | Účet    | Odhlášení funguje správně                                   | Medium   | Netestováno |          |

---

## Statické stránky

| ID      | Sekce     | Kontrolní bod                                              | Priorita | Status      | Poznámky |
|---------|-----------|------------------------------------------------------------|----------|-------------|----------|
| CNT-01  | Obsah     | Stránka „O nás“ je dostupná                                | Low      | Netestováno |          |
| CNT-02  | Obsah     | Stránka „Kontakt“ je dostupná                              | Low      | Netestováno |          |
| CNT-03  | Obsah     | Stránky GDPR / obchodní podmínky jsou dostupné             | Low      | Netestováno |          |

---

## Technické kontroly

| ID       | Sekce   | Kontrolní bod                                               | Priorita | Status      | Poznámky |
|----------|---------|-------------------------------------------------------------|----------|-------------|----------|
| TECH-01  | Technické | Web běží přes HTTPS (pokud je podporováno)                | High     | Netestováno |          |
| TECH-02  | Technické | V konzoli nejsou kritické JavaScript chyby                | Medium   | Netestováno |          |
| TECH-03  | Technické | Stránky se načítají v rozumném čase                       | Medium   | Netestováno |          |