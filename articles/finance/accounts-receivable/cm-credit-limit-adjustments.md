---
title: Kredito limito koregavimai
description: Šioje temoje paaiškinama, kaip nustatyti ir įtraukti kredito limito koregavimus.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 31d83e2083806a518928dc2079c31fab6f95872c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254532"
---
# <a name="credit-limit-adjustments"></a>Kredito limito koregavimai 

[!include [banner](../includes/banner.md)]

Kredito limito koregavimai leidžia kreditų vadovams naujinti vieno kliento, klientų grupės arba visų klientų kreditų limitus ir galiojimo datas naudojant registravimo procesą. Galite įtraukti kredito limito koregavimo įrašus, kad atnaujintumėte klientus ir klientų kredito grupes, arba galite juos naudoti norėdami automatiškai apskaičiuoti kredito limitus. Po to įrašai gali būti peržiūrimi, siunčiami tvirtinimui naudojant darbo eigą ir registruojami kliento sąskaitoje.

## <a name="set-up-credit-limit-adjustments"></a>Kredito limito koregavimų nustatymas

Galite kurti įrašus kredito limitų koregavimų žurnale puslapyje **Kredito limito koregavimas** (**Kredito valdymas \> Kredito limito koregavimai \> Kredito limito koregavimai**).

1. Pasirinkite **Naujas**. Sukuriama nauja įrašų grupė, turinti kredito limito koregavimo numerį.
2. Pasirinkite kredito limito koregavimo tipą:

    - Pasirinkite **Kredito limitas**, kad pakeistumėte kliento kredito limitą.
    - Pasirinkite **Laikinas kredito limitas**, kad sukurtumėte laikiną kredito limitą užuot keitę esamą kliento kredito limitą. Laikinas kredito limitas perrašo kliento kredito limitą apibrėžtam laikotarpiui. Pasibaigus šiam laikotarpiui, kliento kredito limitas vėl naudojamas.
3. Įvesti aprašymą. 

Jei pasirinktas žymės langelis **Užregistruota**, kredito limitai yra pritaikyti. Lauke **Patvirtinimo būsenos** rodoma žurnalo darbo eigos būsena. Darbo eiga yra pasirinktinė.

### <a name="add-credit-limit-adjustments"></a>Kredito limito koregavimų įtraukimas

Norėdami rankiniu būdu įtraukti kredito limito koregavimus, pasirinkite **Eilutės** ir atlikite toliau nurodytus veiksmus.

1. Norėdami įtraukti kliento kredito limito koregavimą, naudokite meniu **Kliento koregavimai**. Norėdami įtraukti kredito limitą į klientų kredito grupę, pasirinkite **Klientų kredito grupės koregavimai**.
2. Įveskite kliento sąskaitą, skirtą SF kliento sąskaitai, kurią reikia atnaujinti į naują kredito limitą. Jei pirmame veiksme pasirenkate **Klientų kredito grupės koregavimai**, įveskite klientų kredito grupę. Toje pačioje žurnalo eilutėje negalite įvesti ir kliento sąskaitos, ir klientų kredito grupės ID.

    Rodomas dabartinis kredito limitas; pavadinimas atsiranda automatiškai.

3. Įveskite naują kredito limitą, kuris turėtų pakeisti dabartinį kredito limitą, kai užregistruojamas kredito limito įrašas.
4. Įveskite datą, kad apibrėžtumėte naują kliento kredito limito galiojimo datą. Kurdami kredito limito koregavimą, turite įvesti kredito limito galiojimo datą.

Lauke **Patvirtinimo būsenos** rodoma žurnalo eilutės darbo eigos būsena.

Jei norite, kad būtų automatiškai sugeneruoti kredito limito koregavimai, veiksmų srityje galite naudoti meniu **Generuoti**.
 
### <a name="add-temporary-credit-limit-adjustments"></a>Laikinų kredito limito koregavimų įtraukimas

Norėdami rankiniu būdu įtraukti laikinus kredito limito koregavimus, atlikite toliau nurodytus žurnalo eilučių veiksmus.

1. Norėdami įtraukti kliento kredito limito koregavimą, naudokite meniu **Kliento koregavimai**. Norėdami įtraukti kredito limitą į klientų kredito grupę, pasirinkite **Klientų kredito grupės koregavimai**.
2. Įveskite kliento sąskaitą, skirtą SF kliento sąskaitai, kurią reikia atnaujinti į naują kredito limitą. Jei pirmame veiksme pasirenkate **Klientų kredito grupės koregavimai**, įveskite klientų kredito grupę. Toje pačioje žurnalo eilutėje negalite įvesti ir kliento sąskaitos, ir klientų kredito grupės ID.

    Jei jau yra aktyvus arba būsimas laikinas kredito limitas, kiekvienam laikinam kredito limitui atsiranda dabartinis laikinas kredito limitas ir datos intervalas. Pavadinimas rodomas automatiškai.

3. Įveskite naują kredito limitą, kuris turėtų pakeisti dabartinį kredito limitą.
4. Laukuose **Naujas pradžios datos** ir **Naujas iki pabaigos datos** nurodykite laikotarpį, kada galioja išplėstinis kredito limitas. Kurdami kredito limito koregavimų žurnalą, turite įvesti kredito limito galiojimo datas.

Lauke **Patvirtinimo būsenos** rodoma žurnalo eilutės darbo eigos būsena.

## <a name="generate-credit-limit-adjustments"></a>Kredito limito koregavimų generavimas

Kredito limitai taip pat gali būti koreguojami automatiškai. Veiksmų srityje pasirinkite **Generuoti**, tada pasirinkite vieną iš toliau nurodytų parinkčių.

- Iš esamo kliento
- Iš esamos klientų kredito grupės
- Automatiniai kredito limitai

### <a name="from-existing-customer"></a>Iš esamo kliento

Galite kurti žurnalo eilutes iš esamų klientų. Kai pasirenkate **Generuoti \> Iš esamos kliento**, atsiranda dialogo langas, kuriame galite pateikti klientų pasirinkimo ir naujų limitų skaičiavimo kriterijus.

1. Įveskite koregavimo reikšmę, kad galėtumėte pridėti arba atimti sumą prie kredito limito. Įveskite neigiamą reikšmė, kad sumažintumėte dabartinį kredito limitą arba teigiamą reikšmę, kad padidintumėte.
2. Lauke **Reikšmės tipas** pasirinkite, kaip reikšmė, kurią įvedėte 1 veiksme, turi būti naudojama apskaičiuojant naują kredito limitą.

    - Pasirinkite **Fiksuota reikšmė**, jei norite pakeisti kredito limitą pagal sumą.
    - Pasirinkite **Procentai**, jei norite pakeisti kredito limitą pagal procentus.

3. Įveskite reikšmę, naudojamą apskaičiuotam kredito limitui apvalinti. Pavyzdžiui, įveskite **10,00**, norėdami apvalinti kredito limitą iki artimiausio 10,00 valiutos vieneto.
4. Nustatykite lauką **Apvalinimo formos**, kad galėtumėte nurodyti, ar likutį apvalinti į didžiąją ar į mažąją pusę.
5. Pasirinkite datų koregavimo metodą.

    - Jei pasirinksite **Absoliutus**, galite įvesti datas, apibrėžiančias kredito limitų datų intervalą.
    - Jei pasirinksite **Santykinis**, galite įvesti intervalo poslinkio datas. Dabartinis kredito limito datos intervalas bus koreguojamas pagal poslinkį.

6. Naudokite „FastTab“ **Įtrauktini įrašai**, kad galėtumėte filtruoti įtrauktus klientus. Jei neįtraukite filtrų, kredito limito įrašai bus sugeneruojami visiems klientams.
7. Pasirinkite **Gerai**, jei norite sukurti kredito limito koregavimo įrašus.

### <a name="from-existing-customer-credit-group"></a>Iš esamos klientų kredito grupės

Galite kurti žurnalo eilutes iš esamų klientų kredito grupių. Kai pasirenkate **Generuoti \> Iš esamos klientų kredito grupės**, atsiranda dialogo langas, kuriame galite pateikti klientų kredito grupių pasirinkimo ir naujų limitų skaičiavimo kriterijus. Kriterijai yra tie patys kriterijai, kurie naudojami kuriant žurnalo eilutes iš esamų klientų. Žiūrėkite veiksmus ankstesniame skyriuje.

### <a name="automatic-credit-limits"></a>Automatiniai kredito limitai

Galite sukurti automatinius kreditų limitus, kad nustatytumėte ir atnaujintumėte klientų kredito limitus. Automatiniai kredito limitai yra sukurti rizikos grupei ir jie yra pagrįsti konkrečiomis reikšmėmis, kurios naudojamos vertinimo grupėse. Galite naudoti šiuos automatinius kreditų limitus kredito limito įrašams generuoti. Jei klientas priskirtas konkrečiai rizikos grupei, o kliento kredito informacija sutampa su automatinio kredito limito kriterijais, sukuriamas kredito limito koregavimo įrašas.

#### <a name="create-automatic-credit-limits"></a>Automatinių kredito limitų kūrimas

Galite sukurti automatinius kredito limitus naudodami kredito limito koregavimus. Kai pasirenkate **Generuoti \> Automatiniai kredito limitai**, atsiranda dialogo langas, kuriame galite nustatyti naujų kredito limitų, kurie bus sukurti pagal rizikos grupes, kurioms priskirti klientai, galiojimo datą. Kai baigsite, pasirinkite **Gerai**, kad sukurtumėte kredito limito koregavimų eilutes.

### <a name="post-adjustments"></a>Registravimo koregavimai

Sukūrę kredito limito koregavimų eilutes, veiksmų srityje galite naudoti mygtuką **Registruoti**, kad užregistruotumėte įrašus ir atnaujintumėte kliento kredito limitus. Tačiau, jei nustatėte darbo eigą, veiksmų srityje turite pasirinkti **Darbo eiga \> Pateikti**, kad tvirtinimui pateiktumėte žurnalą.

### <a name="credit-limit-adjustments-workflows"></a>Kredito limito koregavimų darbo eigos

Darbo eigos **Kredito limito koregavimai** gali būti naudojamos norint siųsti kredito limito koregavimus naudojant darbo eigos patvirtinimo procesą. Puslapyje **Kredito valdymo darbo eigos** galite sukurti dvi darbo eigas (**Kreditų valdymas \> Sąranka \> Kreditų valdymo darbo eigos**):

- **Kredito limito koregavimai** – ši darbo eiga gali būti naudojama įrašams tvirtinti antraštės lygiu.
- **Kredito limito koregavimų eilutė** – ši darbo eiga gali būti naudojama koregavimo įrašams tvirtinti, kad įrašus galėtų patvirtinti skirtingi asmenys, remdamiesi darbo eigos kriterijais.

> [!NOTE]
> Sukūrę darbo eigą **Kredito limito koregavimai**, galite nustatyti ją taip, kad koregavimai būtų registruojami automatiškai po to, kai eilutės patvirtinamos. Tiesiog užduotį **Automatiškai registruoti žurnalą** įtraukite į darbo eigą.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]