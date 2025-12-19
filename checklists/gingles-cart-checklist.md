## Košík – detailní checklist

| Oblast testu        | Scénář / krok                                                                 | Očekávaný výsledek |
|----------------------|-------------------------------------------------------------------------------|--------------------|
| Přidání produktu     | Přidání jednoho produktu do prázdného košíku                                  | Produkt se zobrazí v košíku, cena se přičte |
| Přidání více kusů    | Přidání 5 kusů stejného produktu                                              | Košík ukáže správné množství, celková cena = jednotková × 5 |
| Odstranění produktu  | Odstranění jednoho produktu                                                   | Produkt zmizí, celková cena se sníží |
| Vyprázdnění košíku   | Kliknutí na „Vyprázdnit košík“                                                | Košík je prázdný, celková cena = 0 |
| Úprava množství      | Změna množství na 0                                                           | Produkt se odstraní z košíku |
| Úprava množství      | Změna množství na záporné číslo                                               | Systém zobrazí chybu, množství se nezmění |
| Cenová logika        | Přidání produktu se slevou                                                    | Sleva se správně aplikuje, cena odpovídá |
| Kupony               | Aplikace platného kuponu                                                      | Cena se sníží podle kuponu |
| Kupony               | Aplikace neplatného kuponu                                                    | Zobrazí se chybová hláška |
| DPH                  | Přidání produktu s DPH                                                        | Celková cena obsahuje správně vypočtené DPH |
| Doprava              | Přidání dopravy (např. kurýr)                                                 | Cena dopravy se přičte k celkové částce |
| Uložení stavu        | Refresh stránky                                                               | Košík zůstane nezměněný |
| Uložení stavu        | Odhlášení a opětovné přihlášení                                               | Košík se zachová |
| Edge case            | Přidání produktu, který není skladem                                          | Zobrazí se hláška „Není skladem“ |
| Edge case            | Přidání extrémně velkého množství (např. 9999 kusů)                           | Systém zobrazí chybu nebo limit |
| UX / přístupnost     | Ovládání košíku pouze klávesnicí                                              | Všechny funkce dostupné |
| UX / přístupnost     | Čtení košíku screen readerem                                                  | Informace jsou srozumitelné |
| Analytics            | Přidání produktu → událost v Google Analytics                                 | Událost se správně loguje |