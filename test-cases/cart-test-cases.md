## Test Cases – Košík

| ID   | Název testu                   | Kroky                                                                 | Očekávaný výsledek |
|------|-------------------------------|----------------------------------------------------------------------|--------------------|
| TC01 | Přidání jednoho produktu      | 1. Otevřít produkt. 2. Kliknout „Přidat do košíku“.                  | Produkt se zobrazí v košíku |
| TC02 | Přidání více kusů             | 1. Přidat produkt. 2. Nastavit množství = 5.                         | Košík ukáže 5 kusů, cena odpovídá |
| TC03 | Odstranění produktu           | 1. Přidat produkt. 2. Kliknout „Odstranit“.                          | Produkt zmizí, cena se sníží |
| TC04 | Vyprázdnění košíku            | 1. Přidat více produktů. 2. Kliknout „Vyprázdnit košík“.             | Košík je prázdný |
| TC05 | Aplikace platného kuponu      | 1. Přidat produkt. 2. Vložit kupon „SALE10“.                         | Cena se sníží o 10 % |
| TC06 | Aplikace neplatného kuponu    | 1. Přidat produkt. 2. Vložit kupon „XYZ“.                            | Zobrazí se chybová hláška |
| TC07 | Refresh stránky               | 1. Přidat produkt. 2. Refreshnout stránku.                           | Produkt zůstane v košíku |
| TC08 | Přidání produktu mimo sklad   | 1. Otevřít produkt „Není skladem“. 2. Kliknout „Přidat do košíku“.   | Zobrazí se hláška „Není skladem“ |