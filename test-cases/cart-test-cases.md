## Test Cases – Košík

## Pokročilé test cases – Košík (část 2)

| ID    | Název testu                                   | Kroky                                                                                     | Očekávaný výsledek |
|-------|------------------------------------------------|--------------------------------------------------------------------------------------------|--------------------|
| TC09  | Změna množství pomocí tlačítek + / –           | 1. Přidat produkt. 2. Kliknout na „+“. 3. Kliknout na „–“.                                 | Množství se mění o 1 kus správným směrem |
| TC10  | Ruční zadání množství                          | 1. Přidat produkt. 2. Do pole množství zadat „3“.                                          | Množství = 3, cena odpovídá |
| TC11  | Zadání nečíselné hodnoty                       | 1. Přidat produkt. 2. Do pole množství zadat „abc“.                                        | Zobrazí se chyba, množství se nezmění |
| TC12  | Zadání extrémně vysoké hodnoty                 | 1. Přidat produkt. 2. Zadání množství „9999“.                                              | Systém zobrazí limit nebo chybu |
| TC13  | Přidání více různých produktů                  | 1. Přidat 3 různé produkty.                                                                | Všechny produkty se zobrazí v košíku |
| TC14  | Kontrola mezisoučtu                             | 1. Přidat 2 produkty. 2. Ověřit mezisoučet každého produktu.                               | Mezisoučet = cena × množství |
| TC15  | Kontrola celkové ceny                           | 1. Přidat více produktů. 2. Ověřit celkovou cenu.                                          | Celková cena = součet mezisoučtů |
| TC16  | Aplikace dopravy                                | 1. Přidat produkt. 2. Vybrat dopravu (např. kurýr).                                        | Cena dopravy se přičte k celkové částce |
| TC17  | Změna dopravy                                   | 1. Vybrat dopravu A. 2. Změnit na dopravu B.                                               | Cena se aktualizuje podle nové dopravy |
| TC18  | Aplikace dárkového balení                       | 1. Přidat produkt. 2. Vybrat „Dárkové balení“.                                             | Cena balení se přičte |
| TC19  | Odstranění dárkového balení                     | 1. Aktivovat balení. 2. Zrušit balení.                                                     | Cena balení se odečte |
| TC20  | Aplikace více kuponů                            | 1. Přidat produkt. 2. Aplikovat kupon A. 3. Aplikovat kupon B.                             | Systém povolí pouze jeden kupon nebo zobrazí chybu |
| TC21  | Expired kupon                                   | 1. Přidat produkt. 2. Vložit expirovaný kupon.                                             | Zobrazí se hláška „Kupon je neplatný“ |
| TC22  | Košík po odhlášení a přihlášení                 | 1. Přidat produkt. 2. Odhlásit se. 3. Přihlásit se.                                         | Košík zůstane zachovaný |
| TC23  | Košík po vypršení session                       | 1. Přidat produkt. 2. Nechat session vypršet.                                              | Košík se zachová nebo se vymaže podle specifikace |
| TC24  | Refresh stránky                                 | 1. Přidat produkt. 2. Refreshnout stránku.                                                 | Košík zůstane nezměněný |
| TC25  | Košík na mobilním zařízení                       | 1. Otevřít košík v mobilním viewportu.                                                     | Rozložení je responzivní a funkční |
| TC26  | Košík na tabletu                                | 1. Otevřít košík v tablet viewportu.                                                       | Rozložení je responzivní |
| TC27  | Přístupnost – ovládání klávesnicí               | 1. Navigovat košík pomocí Tab/Enter.                                                       | Všechny prvky jsou dostupné |
| TC28  | Přístupnost – screen reader                     | 1. Zapnout screen reader. 2. Projít košík.                                                 | Popisy jsou srozumitelné |
| TC29  | Analytics – přidání produktu                    | 1. Přidat produkt.                                                                          | Odešle se událost „add_to_cart“ |
| TC30  | Analytics – odstranění produktu                 | 1. Odstranit produkt.                                                                       | Odešle se událost „remove_from_cart“ |