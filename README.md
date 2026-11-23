# Robot Rush

En spelbar webbprototyp av regelutkastet *ROBOT RUSH v0.1*. Två lag kör robothundar över samma hinderbana medan skyttarna på plattformarna skjuter gel mot motståndarens hundar.

Öppna `index.html` i en webbläsare. Spelet kräver tangentbord och mus och har inget byggsteg.

## Kontroller

| Tangent | Vad den gör |
|---|---|
| W A S D / piltangenter | Styr vald hund |
| 1 2 3 / Tab | Byt hund. De andra två kör själva. |
| Mus (håll inne) | Sikta och skjut från mitten av den blå plattformen |
| Q / E | Välj Fart eller Sköld när ditt lag har vunnit en power-up |
| P / Esc | Paus |
| M | Ljud av/på |

## Regler i prototypen

- Varje lag har 3 hundar och 3 skyttar. Du är blått lag och spelar mot CPU (Lätt, Normal eller Svår).
- Omgångar på 60 s. Man spelar till 21 eller 11 poäng.
- Banan har 6 zoner värda **0 · 1 · 1 · 2 · 3 · 4** i färdriktningen. När klockan når noll får varje hund värdet på zonen den står i.
- Nästa omgång körs åt andra hållet, med start där hundarna står. Ingen reset.
- 28 träffar slår ut en hund i 4 s. Vådaskott räknas.
- Hundarna går i 75 % fart. Fartboost ger 100 % i 5 s.
- Skotten går i båge från den upphöjda plattformen och kan bara träffa på andra halvan av sträckan mot siktet. Skydden stoppar dem.

## Svar på de öppna frågorna (husregler i den här versionen)

1. **Zoner:** 6 zoner värda 0, 1, 1, 2, 3, 4. Max 12 poäng per lag och omgång.
2. **Offline:** 4 s. Hit-räknaren nollställs efter offline.
3. **Sköld:** 12 extra träffar per hund. Skölden gäller tills den går sönder.
4. **Kontakt:** Knuffar och blockeringar är tillåtna. Det går inte att välta en hund.
5. **Power-ups:** två per omgång, när det är 45 s och 22 s kvar. Varje lag får en egen måltavla med 10 träffpoäng. Laget som skjuter ner sin först väljer power-up och båda måltavlorna släcks.
6. **Säkerhet:** nät bakom banans kortsidor fångar skott som lämnar banan.
7. **Tiebreak:** om båda lagen passerar målet i samma omgång vinner högst summa. Vid lika poäng körs en förlängningsomgång.
8. **Plattformar:** lagen byter inte plattform.
