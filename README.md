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
- Banan är 60 × 14 m med 20 hinder (väggar, lådor och låga balkar) spegelvänt runt mitten. Alla filer är minst cirka 2,4 m breda.
- Skyttarna står på upphöjda U-formade plattformar som omsluter varje kortsida. Armarna går längs långsidorna ända fram till mittlinjen, så båda lagens plattformar täcker halva banan var. Nät bakom och utanför plattformarna fångar missade skott.

## Roller

Den hund eller skytt du inte styr sköts alltid av datorn.

Välj roll i menyn:

- **Hund:** du styr en robothund genom dess kamera, eller med en kamera bakom hunden. Dina fyra skyttar sköts av datorn. Byt hund med hundkorten.
- **Skytt:** du står på lagets plattform i förstapersonsvy och kan gå runt på hela U:et. Dina hundar och de andra tre skyttarna sköts av datorn.

Skyttarna har en **Nerf Rival Nemesis**: cirka 30 m/s, 8 skott per sekund och en räckvidd på 15–20 m. Kulorna bromsas av luftmotstånd. Varje lag har **fyra skyttar**, två på varje arm av U:et. De rör sig fritt längs plattformen, och datorns skyttar går mot den hund de siktar på för att komma inom räckhåll. Varje skytt har **ett magasin på 100 kulor per omgång** och kan inte ladda om. En ring på banan visar var nästa kula landar. Banan räknas i meter (60 × 14 m).

## Grafik

Allt byggs i koden: robothundar i Spot-stil med traverande gång, skyttar med Nerf Rival Nemesis, ställningsplattformar med galler och räcken, plywoodbunkrar och betongbarriärer, gummigolv och en inomhushall med takbelysning.

## Kontroller

| Mobil | Dator | Vad det gör |
|---|---|---|
| Dra med vänster tumme | W A S D | Gå/kör |
| Dra med höger tumme | Mus (klicka för att låsa) / piltangenter | Titta och svänga |
| Håll SKJUT (och dra för att sikta) | Klick / mellanslag | Skjut |
| ZOOM | Z / högerklick | Zooma |
| Hundkorten | 1 2 3 / Tab | Byt hund (hundrollen) |
| Vy | V | Hundkamera eller kamera bakom |
| Knappar i rutan | Q / E | Välj Fart eller Sköld |
| II | P / Esc | Paus |

## Övriga regler

- Omgångar på 60 s. Man spelar till 21 eller 11 poäng.
- 10 träffar slår ut en hund i 4 s. Efter en reboot tål hunden inga träffar på 2 s, så att den hinner röra sig. Varje hund har **en reboot per omgång**: slås den ut en andra gång är den ute resten av omgången. Den står kvar som hinder och får poängen för zonen där den stannade. Vådaskott räknas.
- Hundarna springer i 75 % av 20 km/h (15 km/h). Fartboost ger 100 %, alltså 20 km/h, i 5 s.

## Husregler för de öppna frågorna

1. **Zoner:** 3 · 2 · 1 · mitten · 1 · 2 · 3. Laget får poäng på den sida det anfaller, och 3-zonen blåser av omgången.
2. **Offline:** 4 s. Hit-räknaren nollställs efter offline. Bara en reboot per hund och omgång.
3. **Sköld:** 5 extra träffar per hund. Skölden gäller tills den går sönder.
4. **Kontakt:** Knuffar och blockeringar är tillåtna. Det går inte att välta en hund.
5. **Power-ups:** två per omgång, när det är 45 s och 22 s kvar. Varje lag får en egen måltavla på sidan av banan med 10 träffpoäng. Laget som skjuter ner sin först väljer power-up.
6. **Säkerhet:** nät bakom och utanför plattformarna.
7. **Tiebreak:** om båda lagen passerar målet i samma omgång vinner högst summa. Vid lika poäng körs en förlängningsomgång.
8. **Plattformar:** skyttarna byter plattform med sina hundar varje omgång. Hundar startar alltid på samma sida som sina egna skyttar, aldrig på motståndarnas sida.
