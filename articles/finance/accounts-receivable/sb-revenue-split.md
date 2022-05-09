---
title: Įplaukų skaidymo šablonai abonemento sąskaitose
description: Šioje temoje paaiškinama, kaip nustatyti prekių, parduodamų kaip grupavimai, įplaukų skaidymo šablonus.
author: JodiChristiansen
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 5c2eb6c8e18770eb149c445f662ab7a90aad81a7
ms.sourcegitcommit: 367e323bfcfe41976e5d8aa5f5e24a279909d8ac
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/29/2022
ms.locfileid: "8660517"
---
# <a name="revenue-split-templates-in-subscription-billing"></a>Įplaukų skaidymo šablonai abonemento sąskaitose

Norėdami nustatyti įplaukų **skaidymo šablonus**, naudokite puslapį Įplaukų skaidymo šablonas. Įplaukų skaidymo susideda iš pirminės prekės, kuri turi antrinių prekių. Šis prekių tipas dažnai parduodamas klientams kaip viena prekė ar grupavimas.

Pavyzdžiui, kompiuterio elementas gali būti sukurtas tokiu būdu:

- **Pirminė prekė: abonemento sidabro**
- **Eilutės (antriniai) elementai:**

    - Palaikymas
    - Priežiūra
    - Licencija

Kurdami pirminę prekę atmeskite šiuos apribojimus:

- Prekę galima nurodyti kaip pirminę prekę tik vieną kartą.
- Pirminė prekė gali būti pasirinkta kaip antrinis elementas tame pačiame šablone.
- Tinkamame šablone turi būti bent vienas antrinis elementas.
- Prekė gali būti nurodyta kaip antrinis daugiau nei vienos sugrupuotos prekės elementas.
- Kiekvienas pirminis ir antrinis ryšys turi būti unikalus.

## <a name="create-a-parent-item-that-has-child-items"></a>Pirminės prekės, kuri turi antrinių prekių, kūrimas

Norėdami sukurti pirminę prekę, turi šiandienos prekes, atlikite šiuos veiksmus.

1. Įplaukų **skaidymo šablono** puslapyje pasirinkite **Naujas**.
1. **Lauke Pirminė prekė** pasirinkite pirminę prekę. Varianto **numerio** laukas atnaujinamas automatiškai. Jei reikia, vertę galite pakeisti.
1. **Lauke Paskirstymo metodas** pasirinkite paskirstymo metodą.
1. Sąraše Komponento **elementai** pasirinkite Įtraukti, kad **įtraukumėte** antrinius elementus.
1. Jei lauke Paskirstymo **metodas** pasirinkote **Procentas**, lauke Procentai nurodykite **procentus**.

    - Jei lauke Paskirstymo **metodas pasirinkote** **Lygi suma**, laukas **Procentai** automatiškai atnaujinamas, kad kiekviena prekė turėtų vienodą procentą.
    - Jei pasirinkote **Kintama** suma, **·** **·** **Nulinė** pirminė suma arba Nulinė suma paskirstymo metodo lauke, **·** **lauko Procentai vertė lieka 0** (nulis), todėl jos keisti negalima.

1. Pasirinkite **Įrašyti**.

## <a name="fields"></a>Laukai

Puslapyje **Įplaukų skaidymo** šablonas yra šie laukai.

| Laukas | Aprašymas |
|-------|-------------|
| Pirminė prekė | Pasirinkite prekės numerį. Ši prekė tampa jūsų sukurta pirmine grupės prekės preke. |
| Produkto pavadinimas | Produkto pavadinimas. |
| Paskirstymo metodas | <p>Pasirinkite paskirstymo metodą:</p><ul><li>**Lygi suma** – paskirstymo procentai apskaičiuojami automatiškai ir vienodai padalijami visoms šablono prekėms.</li><li>**Procentas** – galite nurodyti paskirstymo procentinę sumą. Visų procentų suma turi būti lygi 100.</li><li>**Kintama** suma – antrinių prekių, kurios pridėtos, grynoji suma yra 0 (nulis). Antrinių prekių kaina turi būti nurodyta operacijos lygiu.</li><li>**Nulinė** suma – pirminė prekė išlaiko vieneto kainą ir grynąją sumą. Visų antrinių prekių grynoji suma yra 0 (nulis).</li><li>**Nulinė pirminės sumos** – pirminės prekės fiksuota grynoji suma lygi 0 (nuliui). Visos antriniai prekės yra laikomos standartinėmis prekėmis. Nėra tikrinama, norint patikrinti, ar antrinių prekių sumų suma lygi pirminės prekės sumai.</li></ul> |
| **Komponento prekės** | |
| Komponento prekė | Pasirinkite prekės numerį. Ši prekė yra antrinis elementas. |
| Varianto numeris | Pasirinkite prekės varianto numerį. |
| Produkto pavadinimas | Produkto pavadinimas. |
| Procentai | <p>Rodyklės paskirstymo procentas:</p><ul><li>Jei lauke **Paskirstymo** metodas nustatyta procentinė **išraiška**, galite nurodyti procentą.</li><li>Jei lauke **Paskirstymo metodas** nustatyta Lygi **suma**, procentas automatiškai skaičiuojamas taip, kad kiekvienam šablono elementui būtų taikomas vienodas procentas.</li><li>Jei lauke **Paskirstymo metodas** nustatyta **kintama** suma, **·** **Nulinė** pirminė suma arba Nulinė suma, procentas yra 0 (nulis), jo negalima redaguoti.</li></ul><p>Šio lauko vertė gali būti bet koks teigiamas skaičius nuo 0 (nulio) iki 100. Visų procentų suma turi būti lygi 100.</p> |
| Bendrasis procentas | <p>Verčių suma stulpelyje **Procentai**.</p><ul><li>Jei lauke **Paskirstymo metodas** nustatyta Lygi **suma arba Procentas** **·**, visų procentų suma turi būti lygi 100.</li><li>Jei lauke **Paskirstymo metodas nustatyta** Kintama **suma**, Nulinė **pirminė** **suma arba Nulinė suma**, bendroji procentinė dalis lygi 0 (nuliui).</li></ul> |

## <a name="revenue-split-on-a-sales-order"></a>Įplaukos, suskaidytos į pardavimo užsakymą

Norėdami sukurti pardavimo užsakymą, kuriame yra prekė, nustatyta įplaukoms išskaidyti, atlikite šiuos veiksmus.

1. **Pardavimo užsakymo puslapyje**, sukurkite pardavimo užsakymą.
2. Kiekvienos nustatytos įplaukų skaidyti prekės eilutėje pažymėkite žymės langelį Įplaukų **skaidymo**. Ta prekė tampa pirmine preke. Jei šablonas jau nustatytas, antriniai elementai automatiškai pasirodo sąraše.
3. Norėdami pridėti daugiau antrinių prekių, **pasirinkite Įtraukti įplaukų išskaidytus** antrinius elementus ir pasirinkite norimą įtraukti iš naujo prekę.
4. Įrašykite užsakymą.

## <a name="revenue-split-with-billing-schedules"></a>Įplaukų skaidymo su atsiskaitymo grafikais

Norėdami sukurti sąskaitų pateikimo grafiką, kuriame yra prekė, nustatyta įplaukų skaidimui, atlikite šiuos veiksmus.

1. Puslapyje Viskas **/Aktyvus atsiskaitymo grafikas** sukurkite atsiskaitymo grafiką.
2. Kiekvienos nustatytos įplaukų skaidyti prekės eilutėje pažymėkite žymės langelį Įplaukų **skaidymo**. Ta prekė tampa pirmine preke. Jei šablonas jau nustatytas, antriniai elementai automatiškai pasirodo sąraše.
3. Norėdami pridėti daugiau antrinių prekių, **pasirinkite Įtraukti įplaukų išskaidytus** antrinius elementus ir pasirinkite norimą įtraukti iš naujo prekę.
4. Toliau atlikite darbo su atsiskaitymo grafiku veiksmus.

> [!NOTE]
> Jei parinktis **Automatiškai kurti įplaukų** skaidymo parinktį **nustatyta kaip Taip** pasikartojančių **sutarčių atsiskaitymo parametrų** puslapyje, įvyksta šie veiksmai:
>
> - Jei eilutės elementas yra nustatytas kaip pirminė prekė įplaukų skaidymo šablone, Įplaukų **skaidymo** žymės langelis yra pažymėtas automatiškai.
> - Antriniai elementai automatiškai įvedami į pardavimo užsakymą arba atsiskaitymo grafiko eilutę.
>
> Jei parinktis **Automatiškai kurti įplaukų** skaidymo pasirinktį nustatyta kaip **Ne**, veikimo būdas pateikiamas taip, kaip paaiškinta anksčiau.
