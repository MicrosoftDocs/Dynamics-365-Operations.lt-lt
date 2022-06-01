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
ms.openlocfilehash: 73dbc2242639a54d687506e7c325fec4b9a95d12
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770160"
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

## <a name="additional-revenue-split-information"></a>Papildoma įplaukų skaidymo informacija

Kai pridedate prekę, kuri yra įplaukų skaidymo dalis, pasižymėkite šią informaciją: 

- Pirminės sumos atidėti negalima.
- Antrinių prekių pradžios data, pabaigos data, kiekis, vienetas, vieta ir sandėlio vertės pagrįstos pirmine preke. Šių antrinių prekių verčių keisti negalima. Visi pirminės prekės keitimai turi būti atlikti. 
- Kainodaros metodas yra **Butas** ir jo pakeisti negalima.
- Antriniai elementai gali būti pridėti arba pašalinti.
- Pirminės ir tarpinių prekių turi būti naudojama ta pati prekių grupė. 
- Antriniai elementai gali būti vieno iš šių nustatymų:

    - Nustatyta **pirminės prekės** atsiskaitymo **dažnumo** ir atsiskaitymo intervalų laukų reikšmė tokia pati. 
    - Atsiskaitymo **dažnumo** laukas nustatytas kaip **Vienkartinis**. Tokiu atveju laukas Atsiskaitymo **intervalai** automatiškai nustatomas kaip **1**. 

- Antrinių prekių grynųjų sumų suma lygi pirminėms sumoms. Jei paskirstymo metodas yra nulinės **sumos**, ir antrinių prekių sumų suma, ir pirminė suma yra 0 (nulis). 

    > [!NOTE]
    > Jei paskirstymo metodas yra nulinė **pirminė** suma, antrinių prekių (ne nulinė) suma nėra lygi pirminė sumai, kuri lygi 0 (nuliui). Šis paskirstymo metodas naudojamas vidiniams tikslams, kad darbuotojai galėtų matyti ant jų esančių prekių. Tačiau klientai gali matyti tik pirminę prekę.

- Jei pardavimo užsakymo kelių elementų išdėstymo (MEA) **tipas** yra Vienas, įtraukiama atitinkama kelių elementų įplaukų paskirstymo operacijos eilutė sukuriama, kai papildomos pirminės ir antriniai prekės. 
- Jei įplaukų skaidymo paskirstymo metodas yra **vienodos sumos** ir pakeičiama pirminė suma, sumos perskaičiuojamos visose antriniuose eilutėse. 
- Įplaukoms išskaidyti, kai paskirstymo metodas **yra kintama** suma, įvyksta šis veikimo būdas:

    - Pirminės prekės grynoji suma pasirodo stulpelyje **Pirminė** suma. Šią vertę galima redaguoti. Tačiau vieneto kaina, grynoji suma ir nuolaida yra 0 (nulis), todėl jos redaguoti negalima.
    - Antrinių prekių vieneto kaina yra 0 (nulis). Galite redaguoti vieneto kainą arba grynąją sumą. Redaguojant vieną vertę, kita vertė atnaujinama automatiškai.

- Įplaukoms išskaidytos tada, kai paskirstymo metodas **yra** procentinis dydis, įvyksta šis veikimo būdas:

    - Pirminės prekės grynoji suma pasirodo stulpelyje **Pirminė** suma. Šią vertę galima redaguoti. Tačiau vieneto kaina, grynoji suma ir nuolaida yra 0 (nulis), todėl jos redaguoti negalima. 
    - Grynoji antrinių prekių suma apskaičiuojama kaip pirminė *procentinė*&times;*suma.*

- Įplaukoms išskaidyti, kai paskirstymo metodas **yra lygus** kiekiui, įvyksta šis veikimo būdas:

    - Pirminės prekės grynoji suma pasirodo stulpelyje **Pirminė** suma. Šią vertę galima redaguoti. Tačiau vieneto kaina, grynoji suma ir nuolaida yra 0 (nulis), todėl jos redaguoti negalima. 
    - Grynoji antrinių prekių suma apskaičiuojama padalinant pirminę sumą po lygiai iš visų antrinių prekių. 
    - Jei antriniai elementai pašalinami arba pridedami, grynoji suma ir vieneto kainos perskaičiuojamos, kad visų antrinių eilučių sumos būtų vienodos. 
    - Jei pirminės sumos vienodai padalyti negalima, paskutinio antrinio elemento grynoji suma ir vieneto kaina gali būti šiek tiek didesnė už kitų antrinių prekių grynąją sumą ir vieneto kainą. 

- Įplaukoms išskaidyti, kai paskirstymo metodas yra **nulinė** suma, įvyksta šis veikimo būdas:

    - Vieneto kainą, grynąją sumą ir nuolaidą galima redaguoti. Pirminė suma yra 0 (nulis), todėl jos redaguoti negalima. 
    - Antrinių prekių kiekis, vienetas, vieta ir sandėlio vertės paremtos pirmine preke. Negalima keisti šių antrinių prekių verčių. Visi pirminės prekės keitimai turi būti atlikti. 
    - Antrinių prekių vieneto kaina ir grynoji kaina yra 0 (nulis), todėl jos redaguoti negalima. 

- Įplaukoms išskaidyti, kai paskirstymo metodas yra **nulinė pirminė** suma, įvyksta šis veikimo būdas:

    - Pirminės prekės vieneto kaina, pirminė suma ir grynoji suma yra 0 (nulis).
    - Atsiskaitymo grafike antriniai eilutės pasirodo taip tarsi būtų įtraukti rankiniu būdu, o visos vertės atnaujinamos pagal pasirinktą atsiskaitymo grafiko grupę. Šias vertes galima redaguoti. Antrinių prekių **perskyrimo** **·** **ir** nuolaidos bei išplėstinės kainos parinktis galite pasiekti naudodami laukus Įvestas kiekis, **Vieneto** kaina, **·** **Nuolaida ir Grynoji** **suma**. 
    - Pardavimo užsakyme antrinių eilučių nuolaida ir nuolaidos procentas yra 0 (nulis). 
    - Pirminių ir antrinių elementų atsiskaitymo dažnumas gali būti pakeistas, o kiekvienos eilutės dažnumas gali skirtis. Tačiau pirminė prekė automatiškai atnaujinama taip, kad tarp antrinių eilučių ji turėtų trumpiausią dažnumą. Pavyzdžiui, įplaukų skaidymo metu yra du antriniai elementai, **·** **iš kurių vienas naudoja mėnesinį atsiskaitymo dažnumą, ir kitą kartą per metus sąskaitų pateikimo** dažnumą. Šiuo atveju pirminės prekės atsiskaitymo dažnumas atnaujinamas į Kas **mėnesį**.
