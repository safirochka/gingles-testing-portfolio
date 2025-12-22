## Checkout – Funkční checklist

| Oblast | Co testovat | Očekávaný výsledek |
|--------|-------------|--------------------|
| Osobní údaje | Vyplnění jména, příjmení | Pole přijímá text, validace funguje |
| Osobní údaje | Vyplnění e‑mailu | Validní e‑mail je přijat, nevalidní odmítnut |
| Osobní údaje | Vyplnění telefonu | Přijímá jen čísla, validace formátu |
| Adresa | Vyplnění ulice, čísla domu | Pole přijímá text, validace povinných polí |
| Adresa | PSČ | Přijímá jen validní formát (např. 123 45) |
| Adresa | Město | Povinné pole, validace |
| Doprava | Výběr dopravy (kurýr, Zásilkovna, osobní odběr) | Cena dopravy se správně přičte |
| Doprava | Změna dopravy | Cena se aktualizuje podle výběru |
| Platba | Výběr platební metody (karta, převod, dobírka) | Metoda se uloží a zobrazí |
| Platba | Neúspěšná platba | Zobrazí se chybová hláška |
| Platba | Úspěšná platba | Pokračuje na potvrzení objednávky |
| Rekapitulace | Zobrazení produktů | Všechny položky z košíku jsou viditelné |
| Rekapitulace | Kontrola cen | Součty odpovídají košíku |
| Rekapitulace | Aplikace kuponu | Sleva se správně projeví |
| Souhlas | Zaškrtnutí GDPR / obchodních podmínek | Bez souhlasu nelze pokračovat |
| Odeslání | Kliknutí na „Dokončit objednávku“ | Objednávka se odešle |
| Potvrzení | Zobrazení potvrzovací stránky | Obsahuje číslo objednávky |
| E‑mail | Odeslání potvrzovacího e‑mailu | E‑mail dorazí s detaily objednávky |