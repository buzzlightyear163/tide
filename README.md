# TIDE ($TIDE): trade the tide

Sajten är en enda fil, `index.html`. All CSS och JS är inbakad. Lägg `og.png` och `fav.png` bredvid den.

## 1. Fyll i CONFIG
Öppna `index.html` och sök efter `const CONFIG`:

```js
const CONFIG = { ca: "", x: "https://x.com/", site: "", ... }
```
- `ca`: kontraktsadressen efter launch. Är den tom står det "posted here and on X at launch" och köpknappen är avstängd.
- `x`: länken till coinens X-konto.
- `site`: sajtens adress, t.ex. `https://tide.fun`. Den kommer med i delningsinlägget på X.

## 2. Deploy
GitHub-repo → Vercel → Import → Framework Preset **Other**, inget build-kommando, ingen output-mapp.

## 3. Kolla efter deploy
- **Typsnitt:** JetBrains Mono ska laddas (monospace överallt).
- **X-förhandsvisning:** klistra in länken i ett utkast på X. Då ska `og.png` visas.
- **Live-data:** uppe till höger ska det stå "live · 6 tides" med grön prick. Statusraden längst ner i heron ska säga "index levels: live" och "launch radar: live".

## Vad som är live och vad som är paper
| Del | Källa | Status |
|---|---|---|
| Indexkurser (6 tides + egna) | DexScreener + GeckoTerminal, gratis och utan nyckel | live, uppdateras var 45:e sekund |
| Bygg eget index ("type a narrative") | samma | live |
| Launch-radarn | pump.fun-strömmen (PumpPortal) | live |
| Long/short 1x–5x | sparas i besökarens webbläsare | paper beta, inga SOL flyttas |

Når sajten inte datakällorna visas exempeldata märkt **preview**, aldrig som om den vore riktig.

## Regler för ett index (står även i FAQ:n)
- Solana-coins vars namn eller ticker matchar narrativet
- minst 1 dag gamla, minst $8k likviditet (eller $15k mcap på pump.fun-kurvan), minst $5k volym och 50 trades på 24h
- topp 20 efter volym, lika vikt, varje coins rörelse räknas max ±50 %
- minst 5 coins för att handla. Varje index startar på 1 000.

Default-indexen (ai, gta6, cats, dogs, frogs, politics) ändrar du i `DEFAULTS` i index.html.
