---
title: Kurti priminimo laiškų seką
description: Naudodami šį užduočių vadovą, sukurkite priminimo laiškų seką.
author: mikefalkner
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d8aa4963026ad55ed3dfccb28b6cc68a872f326
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445887"
---
# <a name="create-a-collection-letter-sequence"></a>Kurti priminimo laiškų seką

[!include [banner](../../includes/banner.md)]

Naudodami šį užduočių vadovą, sukurkite priminimo laiškų seką. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Valdymo skiltyje pasirinkite **Moduliai > Kreditas ir rinkiniai > Sąranka > Nustatyti priminimo laiškų seką**.
2. Spustelėkite **Naujas**.
3. Lauke **Priminimo laiškų seka** įveskite sekos ID, kuris atitinka seką. Jis bus naudojamas, kai nustatinėsite registravimo šabloną.
4. Lauke **Aprašymas įveskite** surinkite reikšmę.  Mokėjimo sąlygos nėra privalomos. Jei reikšmę įvesite čia, priminimo laiško mokesčio SF bus naudojamos šios mokėjimo sąlygos, o ne mokėjimo sąlygos, saugomos su klientu.  
5. Lauke **Priminimo laiško kodas** pasirinkite pirmojo priminimo laiško, kurį norite siųsti, kodą. Sukuriamas pirmasis priminimo laiškas pagal SF nurodytą terminą, atidėjimo vertę, kurią įvedate šios eilutės lauke Dienos, ir kitą informaciją, kurią įvedate šioje eilutėje.  
6. Lauke **Aprašymas įveskite** surinkite reikšmę. Mokesčio valiuta pagal numatytąsias nuostatas naudojama ir kaip kliento valiuta. Šis valiutos kodas gali skirtis nuo SF valiutos.  
7. Spustelėkite **Pridėti**, kad pridėtumėte kitą priminimo laišką, kuris bus siunčiamas sekoje Daugeliu atvejų pirmasis priminimo laiškas yra tik perspėjimas. Jei reikia, galite pridėti mokesčių.  
8. Priminimo laiško kodo lauke pasirinkite kitą priminimo laišką, kuris bus siunčiamas sekoje.
9. Lauke **Aprašymas įveskite** surinkite reikšmę.
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
25. Pažymėkite žymės langelį **Blokuoti**, kad klientas daugiau negalėtų pristatyti ir išrašyti SF. Norėdami atblokuoti sąskaitą, puslapio Klientai lauke SF išrašymo ir pristatymo sulaikymas pasirinkite **Ne**.  
26. Išplėskite „FastTab“ **Pastaba**.
27. Įveskite tekstą, kuris bus rodomas pasirinkto priminimo laiško kodo priminimo laiške. Naudodami meniu Vertimai, esantį virš pastabų langelio, šį tekstą galite išversti į kelias kalbas.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]