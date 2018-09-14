--- 
title: "Kurti priminimo laiškų seką"
description: "Naudodami šį užduočių vadovą, sukurkite priminimo laiškų seką."
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6331c3680169b305c4bfbfada4ba106b619be092
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-collection-letter-sequence"></a>Kurti priminimo laiškų seką

[!include [task guide banner](../../includes/task-guide-banner.md)]

Naudodami šį užduočių vadovą, sukurkite priminimo laiškų seką. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pasirinkite Kreditas ir rinkiniai > Sąranka > Nustatyti priminimo laiškų seką.
2. Spustelėkite Naujas.
3. Lauke Priminimo laiškų seka įveskite sekos ID, kuris atitinka seką. Jis bus naudojamas, kai nustatinėsite registravimo šabloną.
4. Lauke Aprašas įveskite reikšmę.
    * Mokėjimo sąlygos nėra privalomos. Jei reikšmę įvesite čia, priminimo laiško mokesčio SF bus naudojamos šios mokėjimo sąlygos, o ne mokėjimo sąlygos, saugomos su klientu.  
5. Priminimo laiško kodo lauke pasirinkite pirmojo priminimo laiško, kurį norite siųsti, kodą.
    * Sukuriamas pirmasis priminimo laiškas pagal SF nurodytą terminą, atidėjimo vertę, kurią įvedate šios eilutės lauke Dienos, ir kitą informaciją, kurią įvedate šioje eilutėje.  
6. Lauke Aprašas įveskite reikšmę.
    * Mokesčio valiuta pagal numatytąsias nuostatas naudojama ir kaip kliento valiuta. Šis valiutos kodas gali skirtis nuo SF valiutos.  
7. Spustelėkite Pridėti, kad pridėtumėte kitą priminimo laišką, kuris bus siunčiamas sekoje
    * Daugeliu atvejų pirmasis priminimo laiškas yra tik perspėjimas. Jei reikia, galite pridėti mokesčių.  
8. Priminimo laiško kodo lauke pasirinkite kitą priminimo laišką, kuris bus siunčiamas sekoje.
9. Lauke Aprašas surinkite reikšmę.
10. Pagrindinės sąskaitos lauke pasirinkite įplaukų sąskaitą, kuri bus naudojama mokesčiams.
11. Įveskite mokestį, kuris bus taikomas registruojant šį priminimo laišką.
12. Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
    * Jei reikia apskaičiuoti mokesčio PVM, pasirinkite prekių PVM grupę.  
13. Sąraše spustelėkite saitą pasirinktoje eilutėje.
14. Įveskite mažiausią pradelstą balansą, kurio reikia prieš siunčiant priminimo laišką.
15. Įveskite leistinų atidėjimo dienų skaičių.
    * Tai yra dienų skaičius po termino, iki kurio galima generuoti priminimo laišką. Terminas, naudojamas skaičiuojant, priklauso nuo priminimo laiško padėties priminimo laiškų sekoje: ⦁ 1 priminimo laiško atidėjimo laikotarpis yra susijęs su terminu SF.  ⦁ 2 ir tolesnių priminimo laiškų atidėjimo laikotarpis yra susijęs su data, kada registruotas ar išspausdintas ankstesnis priminimo laiškas, atsižvelgiant į pasirinktį puslapio Gautinų sumų parametrai lauke Atnaujinti priminimo laiško kodą.  
16. Spustelėkite Pridėti, kad pridėtumėte paskutinį priminimo laišką sekoje.
    * Galite pridėti iki penkių priminimo laiškų sekos priminimo laiškų.  
17. Priminimo laiško kodo lauke pasirinkite kitą priminimo laišką, kuris bus siunčiamas sekoje.
18. Lauke Aprašas surinkite reikšmę.
19. Lauke Pagrindinė sąskaita nustatykite norimas reikšmes.
20. Lauke Mokestis valiuta įveskite skaičių.
21. Lauke Prekių PVM grupė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
22. Sąraše spustelėkite saitą pasirinktoje eilutėje.
23. Lauke Mažiausias pradelstas balansas įveskite skaičių.
24. Lauke Dienos įveskite skaičių.
25. Pažymėkite šį žymės langelį, kad klientas daugiau negalėtų pristatyti ir išrašyti SF.
    * Norėdami atblokuoti sąskaitą, puslapio Klientai lauke SF išrašymo ir pristatymo sulaikymas pasirinkite Ne.  
26. Išplėskite „FastTab“ Pastabos.
27. Įveskite tekstą, kuris bus rodomas pasirinkto priminimo laiško kodo priminimo laiške.
    * Naudodami meniu Vertimai, esantį virš pastabų langelio, šį tekstą galite išversti į kelias kalbas.  


