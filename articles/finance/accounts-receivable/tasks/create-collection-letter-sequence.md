---
title: Priminimo laiškų sekos kūrimas
description: Naudodami šią procedūrą, sukurkite priminimo laiškų seką.
author: JodiChristiansen
ms.date: 12/07/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af5d0a001fbe705834e116516933be67f2de8826
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734164"
---
# <a name="create-a-collection-letter-sequence"></a>Priminimo laiškų sekos kūrimas

[!include [banner](../../includes/banner.md)]

Naudodami šią procedūrą, sukurkite priminimo laiškų seką. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Eikite į **Kredito ir mokėjimų > nustatymas > laiškų seką**.
2. Spustelėkite **Naujas**.
3. Lauke **Priminimo laiškų seka** įveskite sekos ID, kuris atitinka seką. Jis bus naudojamas, kai nustatinėsite registravimo šabloną.
4. Lauke **Aprašymas įveskite** surinkite reikšmę. Mokėjimo sąlygos nėra privalomos. Jei reikšmę įvesite čia, priminimo laiško mokesčio SF bus naudojamos šios mokėjimo sąlygos, o ne mokėjimo sąlygos, saugomos su klientu.  
5. Lauke **Priminimo laiško kodas** pasirinkite pirmojo priminimo laiško, kurį norite siųsti, kodą. Sukuriamas pirmasis priminimo laiškas pagal SF nurodytą terminą, atidėjimo vertę, kurią įvedate šios eilutės lauke Dienos, ir kitą informaciją, kurią įvedate šioje eilutėje.  
6. Lauke **Aprašo laukas** surinkite reikšmę. 
7. Numatytoji mokesčio valiuta yra juridinio subjekto valiuta. Šis valiutos kodas gali skirtis nuo SF valiutos.   
8. Spustelėkite **Pridėti**, kad pridėtumėte kitą priminimo laišką, kuris bus siunčiamas sekoje Daugeliu atvejų pirmasis priminimo laiškas yra tik perspėjimas. Jei reikia, galite pridėti mokesčių.  
9. Lauke **Priminimo laiško kodas** pasirinkite kitą priminimo laišką, kuris bus siunčiamas sekoje.
10. Lauke **Pagrindinė sąskaita** pasirinkite įplaukų sąskaitą, kuri bus naudojama mokesčiams.
11. Įveskite mokestį, kuris bus taikomas registruojant šį priminimo laišką.
12. Lauke **Prekių PVM grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą. Jei reikia apskaičiuoti mokesčio PVM, pasirinkite prekių PVM grupę.  
13. Sąraše spustelėkite saitą pasirinktoje eilutėje.
14. Lauke **Minimalus pradelstas balansas** įveskite minimalų pradelstą balansą, reikalingą prieš išsiunčiant priminimo laišką.
15. Laukelyje **Dienos** įveskite leistinų atidėjimo dienų skaičių. Tai yra dienų skaičius po termino, iki kurio galima generuoti priminimo laišką. Terminas, naudojamas skaičiuojant, priklauso nuo priminimo laiško padėties priminimo laiškų sekoje:
    - 1 priminimo laiško atidėjimo laikotarpis yra susijęs su terminu SF.
    - 2 ir tolesnių priminimo laiškų atidėjimo laikotarpis yra susijęs su data, kada registruotas ar išspausdintas ankstesnis priminimo laiškas, atsižvelgiant į pasirinktį puslapio Gautinų sumų parametrai lauke Atnaujinti priminimo laiško kodą.  
16. Spustelėkite **Pridėti**, kad pridėtumėte paskutinį priminimo laišką sekoje. Galite pridėti iki penkių priminimo laiškų sekos priminimo laiškų.  
17. Lauke **Priminimo laiško kodas** pasirinkite kitą priminimo laišką, kuris bus siunčiamas sekoje.
18. Lauke **Aprašas** įveskite reikšmę.
19. Lauke **Pagrindinė sąskaita** nustatykite norimas reikšmes.
20. Lauke **Mokestis valiuta** įveskite skaičių.
21. Lauke **Prekių PVM grupė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
22. Sąraše spustelėkite saitą pasirinktoje eilutėje.
23. Lauke **Mažiausias pradelstas balansas** įveskite skaičių.
24. Lauke **Dienos** įveskite skaičių.
25. Pažymėkite žymės langelį **Blokuoti**, kad klientas daugiau negalėtų pristatyti ir išrašyti SF. Norėdami atblokuoti sąskaitą, klientų **·** **puslapyje pasirinkite Ne SF išrašymo** ir pristatymo sulaikymo **lauke**.  
26. Išplėskite „FastTab“ **Pastaba**.
27. Įveskite tekstą, kuris bus rodomas pasirinkto priminimo laiško kodo priminimo laiške. Naudodami virš pastabos lauko pateiktą meniu Vertimai šį tekstą **galite išversti** į kelias kalbas.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
