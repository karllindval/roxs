# Robot Rush

En spelbar webbprototyp av regelutkastet *ROBOT RUSH v0.1*, med banan från whiteboard-skissen.

- `index.html`: 3D-mobilspelet i förstapersonsvy (three.js r128 från cdnjs). Fungerar stående och liggande på mobil, och med tangentbord och mus på dator.
- `classic-2d.html`: den första 2D-prototypen för dator.

Öppna filen i en webbläsare. Inget byggsteg behövs.

## Banan

- Lagen startar längst bak på var sin kortsida och kör mot motståndarens sida.
- Zonerna är speglade: **3 · 2 · 1 · mitten · 1 · 2 · 3**. Ett lag får poäng i zonerna på den sida det anfaller.
- Omgången blåses av när den första hunden når 3-zonen, när alla hundar är utslagna eller står i 3-zonen, eller efter 60 s. Då får varje hund poängen för zonen den står i.
- Varje omgång startar om från början: hundarna ställs längst bak, på motsatt sida mot förra omgången. Träffar, reboots och sköldar nollställs, och skyttarna flyttar till U:et på lagets nya startsida.
- Hindren i mitten följer samma blocklayout som i den första prototypen: långa väggar, lådor, låga balkar och ett mittblock, spegelvänt runt mitten.
- Skyttarna står på upphöjda U-formade plattformar som omsluter varje kortsida. Armarna går längs långsidorna över zon 2 och 1. Nät bakom och utanför plattformarna fångar missade skott.

## Roller

Välj roll i menyn:

- **Hund:** du styr en robothund genom dess kamera, eller med en kamera bakom hunden. Dina tre skyttar sköts av datorn. Byt hund med hundkorten.
- **Skytt:** du står på den blå plattformen i förstapersonsvy och kan gå runt på hela U:et. Dina hundar och de andra två skyttarna sköts av datorn.

Varje skytt, även datorns, har **60 skott per magasin** och laddar om på 2,5 s. Kulorna följer en riktig kastbana med gravitation. En ring på banan visar var nästa kula landar.

## Kontroller

| Mobil | Dator | Vad det gör |
|---|---|---|
| Dra med vänster tumme | W A S D | Gå/kör |
| Dra med höger tumme | Mus (klicka för att låsa) / piltangenter | Titta och svänga |
| Håll SKJUT (och dra för att sikta) | Klick / mellanslag | Skjut |
| LADDA | R | Ladda om |
| ZOOM | Z / högerklick | Zooma |
| Hundkorten | 1 2 3 / Tab | Byt hund (hundrollen) |
| Vy | V | Hundkamera eller kamera bakom |
| Knappar i rutan | Q / E | Välj Fart eller Sköld |
| II | P / Esc | Paus |

## Övriga regler

- Omgångar på 60 s. Man spelar till 21 eller 11 poäng.
- 28 träffar slår ut en hund i 4 s. Varje hund har **en reboot per omgång**: slås den ut en andra gång är den ute resten av omgången. Den står kvar som hinder och får poängen för zonen där den stannade. Vådaskott räknas.
- Hundarna går i 75 % fart. Fartboost ger 100 % i 5 s.

## Husregler för de öppna frågorna

1. **Zoner:** 3 · 2 · 1 · mitten · 1 · 2 · 3. Laget får poäng på den sida det anfaller, och 3-zonen blåser av omgången.
2. **Offline:** 4 s. Hit-räknaren nollställs efter offline. Bara en reboot per hund och omgång.
3. **Sköld:** 12 extra träffar per hund. Skölden gäller tills den går sönder.
4. **Kontakt:** Knuffar och blockeringar är tillåtna. Det går inte att välta en hund.
5. **Power-ups:** två per omgång, när det är 45 s och 22 s kvar. Varje lag får en egen måltavla på sidan av banan med 10 träffpoäng. Laget som skjuter ner sin först väljer power-up.
6. **Säkerhet:** nät bakom och utanför plattformarna.
7. **Tiebreak:** om båda lagen passerar målet i samma omgång vinner högst summa. Vid lika poäng körs en förlängningsomgång.
8. **Plattformar:** skyttarna byter plattform med sina hundar varje omgång. Hundar startar alltid på samma sida som sina egna skyttar, aldrig på motståndarnas sida.
