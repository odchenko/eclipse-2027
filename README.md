# Total solar eclipse of 2 August 2027, built by Fable 5.2

Live: https://odchenko.github.io/eclipse-2027/

`index.html` is the file the model wrote, unedited. One prompt, one try.

## The prompt

> Build the total solar eclipse of 2 August 2027 in a single HTML file with Three.js: the Earth turning under the Moon's shadow, the umbra racing across the ground, and a view from the spot of the longest totality with the corona. Compute the Sun and Moon positions yourself from orbital mechanics for that date; don't hardcode the path, the times or the place of greatest eclipse. Show on screen where your model puts greatest eclipse and how long totality lasts there. Make it beautiful. Don't ask me anything.

## The run

- Fable 5.2 on high effort in Claude Code, file tools only: no web, no terminal. It never opened the page in a browser.
- 9 steps, 41 minutes.
- Tokens: 389,765 cache read, 134,157 cache write (1 h), 243,561 output (208,716 of it thinking).
- $11.97 at API list prices ($8 / $40 per million, 1 h cache write $16, cache read $0.20).

## Against NASA

| | This page | NASA |
|---|---|---|
| Greatest eclipse, time | 10:06:37.8 UT | 10:06:37.7 UT |
| Greatest eclipse, place | 25.4994°N 33.1796°E | 25°30.3'N 33°11.0'E |
| Totality there | 6m 24.7s | 6m 22.6s |
| Longest totality, place | 26.8145°N 31.1237°E | 26°49'N 31°08'E |

Greatest eclipse lands 0.73 km from NASA's point, the longest-totality point about 1 km. The page uses ΔT = 69.2 s, NASA 71.7 s.

NASA path table (F. Espenak, NASA GSFC): https://eclipse.gsfc.nasa.gov/SEpath/SEpath2001/SE2027Aug02Tpath.html

## Notes

- Known glitch: about a minute before totality, stripes show on the Moon's disk.
- The Earth texture is loaded from the three.js / three-globe example files on public CDNs. The model did not make it.
