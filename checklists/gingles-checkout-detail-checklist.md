## Checkout – detailní checklist

### 1. Osobní údaje

| Scénář | Co ověřit | Očekávaný výsledek |
|--------|-----------|--------------------|
| Vyplnění jména | Zadání běžného jména | Pole přijímá text |
| Vyplnění jména | Zadání velmi dlouhého jména (100+ znaků) | Zobrazí se chyba nebo se text ořízne |
| Vyplnění příjmení | Zadání běžného příjmení | Validní vstup |
| Vyplnění e‑mailu | Formát `test@example.com` | Přijato |
| Vyplnění e‑mailu | Formát bez @ | Odmítnuto |
| Vyplnění e‑mailu | Formát s mezerou | Odmítnuto |
| Vyplnění telefonu | Zadání pouze číslic | Přijato |
| Vyplnění telefonu | Zadání textu | Odmítnuto |
| Povinná pole | Odeslání bez vyplnění | Zobrazí se validace |

---

### 2. Adresa

| Scénář | Co ověřit | Očekávaný výsledek |
|--------|-----------|--------------------|
| Ulice | Zadání běžné adresy | Přijato |
| Ulice | Zadání prázdného pole | Validace „Povinné pole“ |
| Číslo domu | Zadání čísla | Přijato |
| Číslo domu | Zadání textu | Odmítnuto |
| PSČ | Formát `123 45` | Přijato |
| PSČ | Nevalidní formát | Odmítnuto |
| Město | Povinné pole | Validace při prázdném vstupu |
| Země | Správné předvyplnění | Odpovídá výchozí zemi e‑shopu |

---

### 3. Doprava

| Scénář | Co ověřit | Očekávaný výsledek |
|--------|-----------|--------------------|
| Výběr dopravy | Kurýr / Zásilkovna / Osobní odběr | Cena se aktualizuje |
| Změna dopravy | Přepnutí mezi metodami | Cena se přepočítá |
| Doprava zdarma | Aplikace podmínky (např. nad 1500 Kč) | Cena dopravy = 0 |
| Výběr výdejního místa | Zobrazení mapy / seznamu | Uživatel může vybrat místo |
| Nevybrané výdejní místo | Pokus o pokračování | Zobrazí se validace |

---

### 4. Platba

| Scénář | Co ověřit | Očekávaný výsledek |
|--------|-----------|--------------------|
| Výběr platební metody | Karta / převod / dobírka | Metoda se uloží |
| Platba kartou | Zadání validních údajů | Platba proběhne |
| Platba kartou | Nevalidní číslo karty | Zobrazí se chyba |
| Platba kartou | Expired karta | Odmítnuto |
| 3D Secure | Přesměrování na ověření | Ověření proběhne |
| Neúspěšná platba | Chyba platební brány | Zobrazí se chybová hláška |
| Opakování platby | Kliknutí na „Zkusit znovu“ | Platba se znovu odešle |
| Dobírka | Zobrazení poplatku | Cena se přičte |

---

### 5. Rekapitulace

| Scénář | Co ověřit | Očekávaný výsledek |
|--------|-----------|--------------------|
| Zobrazení produktů | Všechny položky z košíku | Správné množství a ceny |
| Mezisoučty | Cena × množství | Správný výpočet |
| Celková cena | Součet všech položek + doprava | Správný výsledek |
| Sleva | Aplikace kuponu | Sleva se projeví |
| DPH | Zobrazení DPH | Správná sazba |

---

### 6. Souhlasy a podmínky

| Scénář | Co ověřit | Očekávaný výsledek |
|--------|-----------|--------------------|
| GDPR | Zaškrtnutí | Bez zaškrtnutí nelze pokračovat |
| Obchodní podmínky | Povinný souhlas | Validace při chybě |
| Newsletter | Nepovinné | Lze odeslat i bez |

---

### 7. Odeslání objednávky

| Scénář | Co ověřit | Očekávaný výsledek |
|--------|-----------|--------------------|
| Kliknutí na „Dokončit objednávku“ | Všechna data validní | Objednávka se odešle |
| Chybějící údaje | Neúplný formulář | Zobrazí se validace |
| Dvojklik | Odeslání dvakrát | Systém zabrání duplicitě |
| Pomalá odezva serveru | Timeout | Zobrazí se chyba nebo retry |

---

### 8. Potvrzení objednávky

| Scénář | Co ověřit | Očekávaný výsledek |
|--------|-----------|--------------------|
| Zobrazení potvrzení | Stránka „Děkujeme za objednávku“ | Obsahuje číslo objednávky |
| Rekapitulace | Zobrazení všech položek | Správné ceny |
| E‑mail | Odeslání potvrzení | E‑mail dorazí |

---

### 9. Edge cases

| Scénář | Co ověřit | Očekávaný výsledek |
|--------|-----------|--------------------|
| Ztráta připojení | Odeslání bez internetu | Zobrazí se chyba |
| Expirace session | Checkout po 30+ minutách | Session vyprší, košík se obnoví |
| Změna košíku v jiném okně | Otevřený checkout + změna košíku | Checkout se aktualizuje nebo zobrazí upozornění |
| Přepnutí měny | CZK → EUR | Ceny se přepočítají |

---

### 10. Přístupnost (A11y)

| Scénář | Co ověřit | Očekávaný výsledek |
|--------|-----------|--------------------|
| Ovládání klávesnicí | Tab/Enter | Všechny prvky dostupné |
| Screen reader | Čtení polí | Správné popisky |
| Kontrast | Text vs pozadí | Splňuje WCAG |

---

### 11. Analytics

| Scénář | Událost | Očekávaný výsledek |
|--------|---------|--------------------|
| Zahájení checkoutu | `begin_checkout` | Událost se odešle |
| Vyplnění adresy | `add_shipping_info` | Událost se odešle |
| Výběr platby | `add_payment_info` | Událost se odešle |
| Dokončení objednávky | `purchase` | Událost obsahuje ID objednávky |