# Robot Rush

En spelbar webbprototyp av regelutkastet *ROBOT RUSH v0.1*. Två lag kör robothundar över samma hinderbana medan skyttarna på plattformarna skjuter gel mot motståndarens hundar.

- `index.html`: 3D-mobilspelet (three.js r128 från cdnjs). Fungerar stående och liggande på mobil, och med tangentbord och mus på dator.
- `classic-2d.html`: den första 2D-prototypen för dator.

Öppna filen i en webbläsare. Inget byggsteg behövs.

## Kontroller (3D)

| Mobil | Dator | Vad det gör |
|---|---|---|
| Dra nere till vänster | W A S D / piltangenter | Styr vald hund (virtuell joystick) |
| Tryck på hundkorten | 1 2 3 / Tab | Byt hund. De andra två kör själva. |
| Tryck och håll på banan | Mus (håll inne) | Sikta och skjut från mitten av den blå plattformen. Sikte nära en röd hund låser på den. |
| Knappar i rutan | Q / E | Välj Fart eller Sköld när ditt lag har vunnit en power-up |
| II | P / Esc | Paus |
| Vy | V | Växla mellan hela banan och en kamera som följer din hund |

Stående visar banan från den blå plattformen. Liggande visar den från sidan.

## Regler i prototypen

- Varje lag har 3 hundar och 3 skyttar. Du är blått lag och spelar mot CPU (Lätt, Normal eller Svår).
- Omgångar på 60 s. Man spelar till 21 eller 11 poäng.
- Banan har 6 zoner värda **0 · 1 · 1 · 2 · 3 · 4** i färdriktningen. När klockan når noll får varje hund värdet på zonen den står i.
- Nästa omgång körs åt andra hållet, med start där hundarna står. Ingen reset.
- 28 träffar slår ut en hund i 4 s. Vådaskott räknas.
- Hundarna går i 75 % fart. Fartboost ger 100 % i 5 s.
- Gelkulorna flyger i en båge från den upphöjda plattformen. En kula träffar bara det som den når i rätt höjd, så den passerar över hundar och skydd nära plattformen och kan stoppas av skydd nära målet.

## Svar på de öppna frågorna (husregler i den här versionen)

1. **Zoner:** 6 zoner värda 0, 1, 1, 2, 3, 4. Max 12 poäng per lag och omgång.
2. **Offline:** 4 s. Hit-räknaren nollställs efter offline.
3. **Sköld:** 12 extra träffar per hund. Skölden gäller tills den går sönder.
4. **Kontakt:** Knuffar och blockeringar är tillåtna. Det går inte att välta en hund.
5. **Power-ups:** två per omgång, när det är 45 s och 22 s kvar. Varje lag får en egen måltavla med 10 träffpoäng. Laget som skjuter ner sin först väljer power-up och båda måltavlorna släcks.
6. **Säkerhet:** nät bakom båda plattformarna fångar skott som missar.
7. **Tiebreak:** om båda lagen passerar målet i samma omgång vinner högst summa. Vid lika poäng körs en förlängningsomgång.
8. **Plattformar:** lagen byter inte plattform.
