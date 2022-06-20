---
title: Siunčiamo darbo krūvio vizualizavimas
description: Šiame straipsnyje pateikiama informacija apie siunčiamo darbo krūvio vizualizavimą. Ši funkcija leidžia sandėlio vadovams ir prižiūrėtojams sukurti tinkintus darbo krūvio grafikus, kurie gali būti naudojami siekiant stebėti esamo darbo progresą ir jo turimą kiekį. Sandėlio vadovai gali sukurti keletą rodinių ir nustatyti automatinį paleidimą iš naujo, kaip būtina.
author: Mirzaab
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 0e5a2cd2aa458217ff212d45c0dd13c9d0623bd0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851339"
---
# <a name="outbound-workload-visualization"></a>Siunčiamo darbo krūvio vizualizavimas

[!include [banner](../includes/banner.md)]

Papildomos nustatymų galimybės prieinamos iš **Siunčiamo darbo krūvio vizualizavimo** puslapio leidžia sandėlio vadovams ir prižiūrėtojams sukurti tinkintus darbo krūvių grafikus, kuriuos galima naudoti siekiant stebėti esamo darbo progresą ir likusį jo kiekį. Sandėlio vadovai gali sukurti keletą rodinių ir nustatyti automatinį paleidimą iš naujo, kaip būtina. Siunčiamo darbo krūvio vizualizavimai yra tinkami siekiant rodyti sandėlio vykdymo puslapius.

Šią funkciją galima naudoti siekiant sekti paėmimo darbo progresą. Funkcija yra integruojama su darbo valdymu ir jei jis yra nustatytas, siunčiamos darbo krūvio vizualizacijos gali rodyti valandų skaičių apskaičiavimą, kuris liko rodomam darbo paėmimui (filtruojamam).

## <a name="turn-the-outbound-workload-visualization-feature-on-or-off"></a>Įjungti arba išjungti siunčiamo darbo krūvio vizualizacijos funkciją

Kaip ir tiekimo grandinės valdymo versija 10.0.25 ši funkcija įjungiama pagal numatytąjį nustatymą. Administratoriai šią funkciją gali įjungti arba išjungti funkcijų *valdymo* darbo srityje ieškodami siunčiamų darbo krūvio [vizualizavimo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) priemonių.

## <a name="set-up-outbound-workload-visualizations"></a>Nustatyti siunčiamas darbo krūvio vizualizacijas

Norėdami nustatyti vizualizacijas, sukuriate filtrų kolekciją (rodinius) ir nustatote kiekvieną filtrą taip, kad jis rodytų kitą analizės tipą. Naudojate **Konfigūruoti filtrus** puslapį, kad nustatytumėte filtrus.

Norėdami nustatyti siunčiamo darbo krūvio vizualizavimą, atlikite šiuos žingsnius.

1. Eikite į **Sandėlio valdymas \> Sandėlio stebėjimo ataskaitas \> Siunčiamo darbo krūvio vizualizacija**.

    Rodomas puslapis **Siunčiamo darbo krūvio vizualizacija**. Jums sukūrus keletą filtrų, šis puslapis rodys jūsų vizualizaciją. Galite sukurti tiek filtrų, kiek norite. Visi jūsų sukurti filtrai įrašomi į vartotojo paskyrą taip, kad galėtumėte vėliau juos naudoti. Kitaip tariant, kiekvienas vartotojas turės jo sukurtą filtrų rinkinį. Tie filtrai nebus bendrinti su kitais vartotojais.

1. Puslapyje **Siunčiama darbo krūvio vizualizavimas**, veiksmų juostos skirtuke **Filtrai** rinkitės **Konfigūruoti filtrus**.
1. Puslapyje **Konfigūruoti filtrus** veiksmų juostoje rinkitės **Naujas** , kad įtrauktumėte filtrą ir tada nustatykite tolesnius laukelius jam:

    - **X-ašies grupės lentelė** – Pasirinkite lentelę, kurioje yra laukelis naudotinas grupei X-ašies vertės.
    - **X-ašies grupės laukelis** – Iš lentelės laukelių, kurią pasirinkote  **X-ašies grupės lentelės** laukelio pasirinkite laukelį, kuris turi būti naudojamas grupei X-ašies vertės.
    - **X-ašies vertės lentelė** – Pasirinkite lentelę, kurioje yra laukelis naudotinas tolesnei grupės analizei.
    - **X-ašies vertės laukelis** – Iš lentelės laukelių, kurią pasirinkote  **X-ašies vertės lentelės** laukelio pasirinkite laukelį, kuriame pateikiamos vertės, analizuotinos šiai grupei.
    - **Automatinis paleidimas iš naujo** – Pasirinkite, ar vizualizacija turi būti paleista iš naujo automatiškai.
    - **Paleidimo iš naujo intervalas (minutės)** – Įveskite minučių skaičių tarp automatinių paleidimų iš naujo.
    - **Rodymo lygis** – Pasirinkite, ar grafikas turi rodyti atviras eilutes ar atvirus antraščių skaičius.
    - **Paėmimo tipas** – Jei nustatote **Rodymo lygis** laukelį t _Atviros eilutės_, pasirinkite, ar atvirų darbo eilučių skaičius grafike turi apimti pradinius paėmimus, suplanuotus ar tiek pradinius, tiek suplanuotus.
    - **Saitas** – Pasirinkite saitą, kad įkeltumėte jam grafiką.
    - **Sandėlis** – Pasirinkite sandėlį, kad įkeltumėte jam grafiką.
    - **Apimamos dienos** – Įveskite dienų skaičių praeityje, kurioms turi būti sukurtas grafikas.
    - **Darbo užsakymo tipas** – Pasirinkite siunčiamo filtruojamo darbo užsakymo tipus.

    ![Konfigūruoti filtrų puslapį.](media/work-viz-filters-1.png "Konfigūruoti filtrų puslapį")

1. Užverkite **Konfigūruoti filtrus** puslapį ir grįžkite į **Siunčiamos darbo apkrovos vizualizacijos** puslapį.

    Puslapis **Siunčiamos darbo apkrovos vizualizacijos** puslapis nerodo jokių duomenų pagal jūsų naujus filtro nustatymus. Jūsų naujas filtras dabar yra prieinamas ir pasirinktas **Filtro** laukelyje. Tolesni laukeliai yra prieinami grafiko viršuje:

    - **Filtras** – Šis laukelis apima visus jūsų sukurtus filtrus iki dabar. Pasirinkite filtrą, kad peržiūrėtumėte jo duomenis grafike.
    - **Naujinta paskutiniu metu** – Šis laukelis rodo datą ir laiką, kai informacija grafike buvo naujinta paskutinį kartą.
    - **Apskaičiuotas/realus laikas** – Jei darbo standartai yra nustatyti jūsų sistemoje, nustatykite parinktį į *Taip* tam, kad ji rodytų apskaičiuotą paėmimo laiką kiekvieno grafiko stulpelio viršuje. Jei nenaudojate darbo standartu, ši parinktis yra neprieinama.

    ![Vizualizacijos pavyzdys.](media/work-viz-chart.png "Vizualizacijos pavyzdys")

1. Rinkitės bet kurią juosta grafike, kad peržiūrėtumėte susietą darbo eilutės išsamią informaciją.

    ![Darbo eilutės informacija.](media/work-viz-work-details.png "Darbo eilutės informacija")

## <a name="example-outbound-workload-visualization-for-zones"></a>Pavyzdys: Siunčiamo darbo krūvio vizualizacija zonoms

Šiam pavyzdžiui, jums reikia nustatyti vizualizaciją, kuri rodo darbo eilutes kiekvienai zonai ir kiekvienos darbo eilutės būsenai (_Atverti_, _Uždaryta_, ar _Atšaukta_). Tokiu atveju, galite nustatyti filtrą, kuris turi tolesnius nustatymus:

- **Filtro pavadinimas** – Šiam filtrui įveskite pavadinimą (tokį kaip _Zona prieš darbo būseną_).
- **Aprašas** – Šiam filtrui įveskite trumpą aprašą (tokį kaip _Zona prieš darbo būseną_).
- **X-ašies grupės lentelė** – Rinkitės _Vietos._
- **X-ašies grupės lentelė** – Rinkitės _Zonos ID_.
- **X-ašies vertės lentelė** – Rinkitės _Darbas_, nes norite peržiūrėti kiekvienos zonos darbą.
- **X-ašies vertės laukelis** – Rinkitės _Darbo būsena_, nes norite peržiūrėti kiekvieną darbo būseną.
- **Automatinis paleidimas iš naujo** – Pasirinkite, ar vizualizacija turi būti paleista iš naujo automatiškai.
- **Paėmimo tipas** – Rinkitės _Pradiniai atsiėmimai ir suplanuoti atsiėmimai_, nes norite įtraukti tiek pradinius atsiėmimui, tiek iš suplanuotų vietų. Kitaip tariant, jūs iš esmės norite įtraukti visas turimas darbo eilutes.
- **Rodomas lygis** – Rinkitės _Atviros eilutės_, nes norite peržiūrėti kiekvienos eilutės informaciją, o ne kiekvienos darbo antraštės.

Tolesnis paveikslėlis rodo esančio grafiko pavyzdį.

![Zona prieš darbo būsenos vizualizacija.](media/work-viz-chart.png "Zona prieš darbo būsenos vizualizacija")

Šis grafikas rodo dvi zonos, kurių pavadinimas **AUKŠTAS** ir **BENDRI**, taip pat zoną pavadinimu **Tuščia**. **Tuščia** zona rodo visas darbo eilutes, kurios nėra jokios zonos narės. Grafikas visada rodo visus nesusijusius filtruotus duomenis, tokius kaip **Tušti**, tam, kad pateiktų kiek įmanoma daugiau vaizdo. Zonoje **AUKŠTAS** grafikas rodo tris užvertas eilutes ir keturias atvertas. Zonoje **BENDRI** grafikas rodo keturias užvertas eilutes ir vieną atvertą ir 24 atšauktų. Galiausiai, grafikas rodo aštuonias užvertas eilutes, kurios nėra jokios zonos dalis ir dėl to išvardytos kaip **Tuščios**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]