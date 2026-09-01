# Pult za pozive

Interaktivne kartice sa gotovim rečenicama za hladne pozive — alat za ljude
koji tek počinju da zovu firme i nude izradu sajta.

## Šta je unutra

Jedan fajl: `index.html`. Nema build, nema zavisnosti, nema servera.
Otvara se duplim klikom ili sa bilo kog hostinga.

- **41 kartica** u 7 kategorija: ko se javio, tok poziva, kaže DA, okleva,
  kaže NE, posle poziva, nikad ne govori.
- Klik na karticu je uveća; dugmad ispod rečenice vode na sledeću karticu
  prema tome šta je klijent odgovorio.
- Polja na vrhu (ime, firma, cena + podaci o trenutnom pozivu) automatski se
  ubacuju u sve rečenice. Pamte se u pregledaču, na tom računaru.
- Radi na telefonu, ima svetlu i tamnu temu, i može da se odštampa.

## Objavljivanje na GitHub Pages

Settings → Pages → Source: *Deploy from a branch* → branch `main`, folder `/ (root)`.
Za minut-dva sajt je na `https://KORISNIK.github.io/IME-REPOA/`.

## Izmene teksta

Sve rečenice su u nizu `CARDS` na dnu `index.html`. Svaka kartica ima:

| polje    | značenje                                            |
|----------|-----------------------------------------------------|
| `kad`    | naslov — situacija u kojoj si                        |
| `kaze`   | rečenica koja se izgovara                            |
| `note`   | savet ispod rečenice                                 |
| `react`  | dugmad: šta klijent odgovori i na koju karticu vodi  |
| `silent` | `true` za kartice iz „Nikad ne govori“               |

U tekstu se koriste zamene u uglastim zagradama: `[ime]`, `[firma]`, `[cena]`,
`[klijent]`, `[usluga]`, `[grad]`, `[konkurent]`, `[dan]`. Sve što nije u toj
listi (npr. `[link]`) ostaje istaknuto na stranici kao podsetnik da se popuni ručno.
