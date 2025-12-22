| ID     | Název testu                                      | Kroky                                                                                           | Očekávaný výsledek |
|--------|--------------------------------------------------|--------------------------------------------------------------------------------------------------|--------------------|
| CH01   | Vyplnění osobních údajů – validní data           | 1. Otevřít checkout. 2. Vyplnit jméno, příjmení, e‑mail, telefon.                               | Formulář přijme data, žádná chyba |
| CH02   | Vyplnění osobních údajů – nevalidní e‑mail       | 1. Vyplnit e‑mail „test@“. 2. Pokusit se pokračovat.                                            | Zobrazí se validace „Neplatný e‑mail“ |
| CH03   | Povinná pole – prázdné                           | 1. Nevyplnit jméno/příjmení/e‑mail. 2. Kliknout „Pokračovat“.                                   | Zobrazí se validace u povinných polí |
| CH04   | Vyplnění adresy – validní data                   | 1. Vyplnit ulici, číslo domu, město, PSČ.                                                       | Formulář přijme data |
| CH05   | Vyplnění adresy – nevalidní PSČ                  | 1. Vyplnit PSČ „123“. 2. Pokusit se pokračovat.                                                 | Zobrazí se validace „Neplatné PSČ“ |
| CH06   | Výběr dopravy                                    | 1. Vybrat kurýra. 2. Zkontrolovat cenu dopravy.                                                 | Cena dopravy se přičte k celkové částce |
| CH07   | Změna dopravy                                    | 1. Vybrat kurýra. 2. Změnit na Zásilkovnu.                                                      | Cena se aktualizuje podle nové metody |
| CH08   | Výběr platební metody – karta                    | 1. Vybrat platbu kartou. 2. Pokračovat na další krok.                                           | Metoda se uloží, bez chyb |
| CH09   | Výběr platební metody – dobírka                  | 1. Vybrat dobírku. 2. Zkontrolovat přičtení poplatku.                                           | Poplatek se přičte k celkové ceně |
| CH10   | Rekapitulace – kontrola produktů                 | 1. Přidat produkty do košíku. 2. Otevřít checkout. 3. Přejít na rekapitulaci.                   | Zobrazí se všechny položky s cenami |
| CH11   | Odeslání objednávky – validní data               | 1. Vyplnit vše správně. 2. Kliknout „Dokončit objednávku“.                                      | Objednávka se odešle, zobrazí se potvrzení |
| CH12   | Odeslání objednávky – chybějící souhlas          | 1. Nezaškrtnout GDPR/obchodní podmínky. 2. Kliknout „Dokončit objednávku“.                      | Zobrazí se validace, nelze pokračovat |
| CH13   | Zadání velmi dlouhého jména                      | 1. Vyplnit jméno 100+ znaky.                                                                    | Zobrazí se chyba nebo se text ořízne |
| CH14   | Zadání textu do pole telefon                     | 1. Do telefonu zadat „abcd“.                                                                    | Pole odmítne vstup |
| CH15   | Zadání extrémně dlouhé adresy                    | 1. Vyplnit ulici 200+ znaky.                                                                    | Zobrazí se validace nebo oříznutí |
| CH16   | Nevyplněné město                                 | 1. Nechat město prázdné. 2. Pokusit se pokračovat.                                              | Zobrazí se validace |
| CH17   | Výběr výdejního místa                            | 1. Vybrat Zásilkovnu. 2. Otevřít seznam míst. 3. Vybrat místo.                                  | Místo se uloží |
| CH18   | Pokus o pokračování bez výběru výdejního místa   | 1. Vybrat Zásilkovnu. 2. Nepotvrdit výdejní místo.                                              | Zobrazí se validace |
| CH19   | Platba kartou – nevalidní číslo                  | 1. Vyplnit číslo karty „1111 1111 1111 1111“.                                                   | Zobrazí se chyba |
| CH20   | Platba kartou – expirovaná karta                 | 1. Vyplnit expirované datum.                                                                    | Platba odmítnuta |
| CH21   | 3D Secure – úspěšné ověření                      | 1. Vybrat platbu kartou. 2. Projít 3DS.                                                         | Platba úspěšná |
| CH22   | 3D Secure – neúspěšné ověření                    | 1. Vybrat platbu kartou. 2. Ověření zamítnuto.                                                  | Zobrazí se chyba |
| CH23   | Chyba platební brány                             | 1. Vybrat platbu kartou. 2. Simulovat chybu brány.                                              | Zobrazí se chybová hláška |
| CH24   | Opakování platby                                 | 1. Po chybě kliknout „Zkusit znovu“.                                                            | Platba se znovu odešle |
| CH25   | Timeout při odeslání objednávky                  | 1. Kliknout „Dokončit objednávku“. 2. Simulovat pomalý server.                                  | Zobrazí se chyba nebo retry |
| CH26   | Změna košíku v jiném okně                        | 1. Otevřít checkout. 2. V jiném okně změnit košík.                                              | Checkout se aktualizuje nebo zobrazí upozornění |
| CH27   | Expirace session                                 | 1. Nechat checkout otevřený 30+ minut.                                                          | Session vyprší, zobrazí se upozornění |
| CH28   | Přístupnost – ovládání klávesnicí                | 1. Navigovat checkout pomocí Tab/Enter.                                                         | Všechny prvky dostupné |
| CH29   | Přístupnost – screen reader                      | 1. Zapnout screen reader. 2. Projít formulář.                                                   | Správné popisky a čitelnost |
| CH30   | Analytics – události checkoutu                   | 1. Zahájit checkout. 2. Vyplnit adresu. 3. Vybrat platbu. 4. Dokončit objednávku.              | Odešlou se události: begin_checkout, add_shipping_info, add_payment_info, purchase |