---
title: Siunčiamo darbo krūvio vizualizavimas
description: Šioje temoje pateikta informacija apie siunčiamos darbo apkrovos vizualizaciją. Ši funkcija leidžia sandėlio vadovams ir prižiūrėtojams sukurti tinkintus darbo krūvio grafikus, kurie gali būti naudojami siekiant stebėti esamo darbo progresą ir jo turimą kiekį. Sandėlio vadovai gali sukurti keletą rodinių ir nustatyti automatinį paleidimą iš naujo, kaip būtina.
author: Mirzaab
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-08-28
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6b7512ea6ad2e97db388bac6750482f7ed967140
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225936"
---
# <a name="outbound-workload-visualization"></a>Siunčiamo darbo krūvio vizualizavimas

[!include [banner](../includes/banner.md)]

Papildomos nustatymų galimybės prieinamos iš **Siunčiamo darbo krūvio vizualizavimo** puslapio leidžia sandėlio vadovams ir prižiūrėtojams sukurti tinkintus darbo krūvių grafikus, kuriuos galima naudoti siekiant stebėti esamo darbo progresą ir likusį jo kiekį. Sandėlio vadovai gali sukurti keletą rodinių ir nustatyti automatinį paleidimą iš naujo, kaip būtina. Siunčiamo darbo krūvio vizualizavijos yra tinkamas siekiant rodyti sandėlio vykdymo puslapius.

Šią funkciją galima naudoti siekiant sekti paėmimo darbo progresą. Funkcija yra integruojama su darbo valdymu ir jei jis yra nustatytas, siunčiamos darbo krūvio vizualizacijos gali rodyti valandų skaičių apskaičiavimą, kuris liko rodomam darbo paėmimui (filtruojamam).

## <a name="turn-on-the-outbound-workload-visualization-feature"></a>Įjungti siunčiamą darbo krūvio vizualizacijos funkciją

Kad galėtumėte naudoti šią funkciją, ji turi būti įjungta jūsų sistemoje. Adminsitratoriai gali naudoti [Funkcijos valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) nustatymus tam, kad patikrintų funkcijos būseną ir ją įjungtų. Darbo srityje **Funkcijų valdymas** ši funkcija yra nurodyta toliau pateikiamu būdu.

- **Modulis:** *Sandėlio valdymas*
- **Funkcijos pavadinimas:** *Siunčiama darbo krūvio vizualizacija*

## <a name="set-up-outbound-workload-visualizations"></a>Nustatyti siunčiamas darbo krūvio vizualizacijas

Norėdami nustatyti vizualizacijas, sukuriate filtrų kolekciją (rodinius) ir nustatote kiekvieną filtrą taip, kad jis rodytų kitą analizės tipą. Naudojate **Konfigūruoti filtrus** puslapį, kad nustatytumėte filtrus.

Norėdami nustatyti siunčiamo darbo krūvio vizualzaciją, atlikite šiuos žingsnius.

1. Eikite į **Sandėlio valdymas \> Sandėlio stebėjimo ataskaitas \> Siunčiamo darbo krūvio vizualizacija**.

    Rodomas puslapis **Siunčiamo darbo krūvio vizualizacija**. Jum sukūrus keletą filtrų, šis puslapis rodys jūsų vizualizaciją. Galite sukurti tiek filtrų, kiek norite. Visi jūsų sukurti filtrai įrašomi į vartotojo paskyrą taip, kad galėtumėte vėliau juos naudoti. Kitaip tariant, kiekvienas vartotojas turės jo sukurtą filtrų rinkinį. Tie filtrai nebus bendrinti su kitais vartotojais.

1. Puslapyje **Siunčiama darbo krūvio vizualizacija**, veiksmų juostoje skirtukte **Filtrai** rinkitės **Konfigūruoti filtrus**.
1. Puslapyje **Konfigūruoti filtrus** veiksmų juostoje rinkitės **Naujas** , kad įtrauktumėte filtrą ir tada nustatykite tolesnius laukelius jam:

    - **X-ašės grupės lentelė** – Pasirinkite lentelę, kurioje yra laukelis naudotinas grupei X-ašies vertės.
    - **X-ašies grupės laukelis** – Iš lentelės laukelių, kurią pasirinkote  **X-ašies grupės lentelės** laukelio pasirinkite laukelį, kuris turi būti naudojamas grupei X-ašies vertės.
    - **X-ašės vertės lentelė** – Pasirinkite lentelę, kurioje yra laukelis naudotinas tolesnei grupės analizei.
    - **X-ašies vertės laukelis** – Iš lentelės laukelių, kurią pasirinkote  **X-ašies vertės lentelės** laukelio pasirinkite laukelį, kuriame pateikiamos vertės, analizuotinos šiai grupei.
    - **Automatinis paleidimas iš naujo** – Pasirinkite, ar vizualizacija turi būti paleista iš naujo automatiškai.
    - **Paleidimo iš naujo intervalas (minutės)** – Įveskite minučių skaičių tarp automatinių paleidimų iš naujo.
    - **Rodymo lygis** – Pasirinkite, ar grafikas turi rodyti atviras eilutes ar atvirus antraščių skaičius.
    - **Paėmimo tipas** – Jei nustatote **Rodymo lygis** flaukelį t _Atviros eilutės_, pasirinkite, ar atvirų darbo eilučių skaičius grafike turi apimti pradinius paėmimus, suplanuotus ar tiek pradinius, tiek suplanuotus.
    - **Saitas** – Pasirinkite saitą, kad įkeltumėte jam grafiką.
    - **Sandėlis** – Pasirinkite sandėlį, kad įkeltumėte jam grafiką.
    - **Apimamos dienos** – Įveskite dienų skaičių praeityje, kurioms turi būti sukurtas grafikas.
    - **Darbo užsakymo tipas** – Pasirinkite siunčiamo filtruojamųo darbo užsakymo tipus.

    ![Konfigūruoti filtrų puslapį](media/work-viz-filters-1.png "Konfigūruoti filtrų puslapį")

1. Užverkite **Konfigūruoti filtrus** puslapį ir grįžkite į **Siunčiamos darbo apkrovos vizualizacijos** puslapį.

    Puslapis **Siunčiamos darbo apkrovos vizualizacijos** puslapis nerodo jokių duomenų pagal jūsų naujus filtro nustatymus. Jūsų naujas filtras dabar yra prieinamas ir pasirinktas **Filtro** laukelyje. Tolesni laukeliai yra prieinami grafiko viršuje:

    - **Filtras** – Šis laukelis apima visus jūsų sukurtus filtrus iki dabar. Pasirinkite filtrą, kad peržiūrėtumėte jo duomenis grafike.
    - **Naujinta paskutiniu metu** – Šis laukelis rodo datą ir laiką, kai informacija grafike buvo naujinta paskutinį kartą.
    - **Apskaičiuotas/realus laikas** – Jei darbo standartai yra nustatyti jūsų sistemoje, nustatykite parinktį į *Taip* tam, kad ji rodytų apskaičiuotą paėmimo laiką kiekvieno grafiko stulpelio viršuje. Jei nenaudojate darbo standartu, ši parinktis yra neprieinama.

    ![Vizualizacijos pavyzdys](media/work-viz-chart.png "Vizualizacijos pavyzdys")

1. Rinkitės bet kurią juosta grafike, kad peržiūrėtumėte susietą darbo eilutės išsamią informaciją.

    ![Darbo eilutės informacija](media/work-viz-work-details.png "Darbo eilutės informacija")

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
- **Rodomas lygis** – Rinkitės _Atviros eilutės_, nes norite peržiūrėti kiekvienos eilutės informaciją, o ner kiekvienos darbo antraštės.

Tolesnis paveikslėlis rodo esančio grafiko pavyzdį.

![Zona prieš darbo būsenos vizualizacija](media/work-viz-chart.png "Zona prieš darbo būsenos vizualizacija")

Šis grafikas rodo dvi zonos, kurių pavadinimas **AUKŠTAS** ir **BENDRI**, taip pat zoną pavadinimu **Tuščia**. **Tuščia** zona rodo visas darbo eilutes, kurios nėra jokios zonos narės. Grafikas visada rodo visus nesusijusius filtruotus duomenis, tokius kaip **Tušti**, tam, kad pateiktų kiek įmanoma daugiau vaizdo. Zonoje **AUKŠTAS** grafikas rodo tris užvertas eilutes ir keturias atvertas. Zonoje **BENDRI** grafikas rodo keturias užvertas eilutes ir vieną atvertą ir 24 atšauktų. Galiausiai, grafikas rodo aštuonias užvertas eilutes, kurios nėra jokios zonos dalis ir dėl to išvardytos kaip **Tuščios**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]