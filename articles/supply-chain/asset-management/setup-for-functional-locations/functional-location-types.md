---
title: Funkcinės vietos tipai
description: Šiame straipsnyje aprašoma, kaip kurti funkcinių vietų tipus turto valdymo modulyje.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c44e503900bd157d7f0159cdf2b2d0c1fb3393f
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015789"
---
# <a name="functional-location-types"></a>Funkcinės vietos tipai

[!include [banner](../../includes/banner.md)]

 

Šiame straipsnyje aprašoma, kaip kurti funkcinių vietų tipus turto valdymo modulyje. Funkcinių vietų tipai naudojami siekiant tvarkyti funkcinių vietų reikalavimus, įskaitant tai, kaip turtas diegiamas funkcinėje vietoje. Galima nustatyti turto tipus, priežiūros planus, funkcinių vietų atributus ir turto atributų reikalavimus, kurie bus naudojami funkcinėje vietoje, naudojančioje konkretų funkcinės vietos tipą. Kuriant funkcinę vietą būtina nustatyti funkcinės vietos tipą.

>[!NOTE] 
>Norėdami dirbti su funkcinėmis vietomis, turite sukurti numatytąją funkcinę vietą, kuri bus naudojama tik kuriant naują turtą. Numatytai funkcinei vietai būtina sukurti numatytąjį funkcinės vietos tipą, kas yra visai paprasta ir leidžia numatytoje funkcinėje vietoje įdiegti kelis turtus. Daugiau informacijos apie funkcinių vietų nustatymą žr. [Funkcinių vietų kūrimas](../functional-locations/create-functional-locations.md).

## <a name="create-a-default-functional-location-type"></a>Numatytojo funkcinės vietos tipo kūrimas

Ši procedūra nurodo, kaip kurti numatytąjį funkcinės vietos tipą, naudojamą numatytajai funkcinei vietai.

1. Pasirinkite **Turto valdymas** > **Sąranka** > **Funkcinės vietos** > **Funkcinės vietos tipai**.
2. Pasirinkite **Naujas**, kad sukurtumėte funkcinės vietos tipą.
3. Lauke **Funkcinės vietos tipas** įterpkite funkcinės vietos tipo ID, pvz., „Numatytasis“, ir pavadinimą lauke **Pavadinimas**.
4. Lauke **Funkcinės vietos ciklo modelis** pasirinkite ciklo modelį.
5. Perjungimo mygtuke **Keli turto objektai** pasirinkite „Taip“, kad funkcinėje vietoje leistumėte diegti daugiau turto objektų (numatytoji funkcinė vieta) naudojant šį tipą.

Sukuriamas numatytasis funkcinės vietos tipas, kuris bus naudojamas tik kuriamai numatytai funkcinei vietai. Neturėtumėte įtraukti jokių šio numatytojo funkcinės vietos tipo reikalavimų ar apribojimų.


## <a name="create-functional-location-types"></a>Funkcinės vietos tipų kūrimas

1. Pasirinkite **Turto valdymas** > **Sąranka** > **Funkcinės vietos** > **Funkcinės vietos tipai**.
2. Pasirinkite **Naujas**, kad sukurtumėte funkcinės vietos tipą.
3. Lauke **Funkcinės vietos tipas** įterpkite funkcinės vietos tipo ID ir pavadinimą lauke **Pavadinimas**.
4. Lauke **Funkcinės vietos ciklo modelis** pasirinkite ciklo modelį. Daugiau informacijos apie funkcinės vietos ciklo būsenas ir ciklo modelius žr. [Funkcinės vietos ciklo būsenos](../setup-for-functional-locations/functional-location-stages.md).
5. Perjungimo mygtuke **Keli turto objektai** pasirinkite „Taip“, jeigu turi būti įmanoma diegti kelis turto objektus funkcinėje vietoje naudojant šį funkcinės vietos tipą. Jei pasirinksite „Ne“, funkcinėje vietoje naudodami šį funkcinės vietos tipą bus galima įdiegti tik *vieną* turto objektą.
6. Perjungimo mygtuke **Naujinti turto dimensiją** pasirinkite „Taip“, jeigu norite, kad turto objektai būtų diegiami šio tipo funkcinėje vietoje siekiant automatiškai naudoti su funkcine vieta susijusias finansines dimensijas. Tai reiškia, kad, jei pakeisite finansinių matmenų [Funkcinių vietų kūrimas](../functional-locations/create-functional-locations.md) formą, o funkcinė vieta naudoja funkcinės vietos tipą su perjungimo mygtuku, nustatytų į „Taip“, automatiškai atnaujinami viso turto, įdiegto toje funkcinėje vietoje, finansiniai matmenys.
7. Laukas **Turto tipas** naudojamas tuo atveju, jei norite funkcinei vietai sukurti *vieną* turto objektą su tuo pačiu ID ir pavadinimu, kaip kuriama funkcinė vieta. Pavyzdžiui, tai gali būti aktualu, jei kuriate statinę funkcinę vietą, pvz., pastatą ar vamzdyną. Tokiu atveju pasirinkite turto tipą, kurį norite naudoti automatiškai kuriamam turtui. Atminkite, kad atlikus pasirinkimą šiame lauke, perjungimo mygtukas **Keli turto objektai** turi būti nustatytas į „Ne“.
8. „FastTab“ **Turto tipai** pasirinkite turto tipus, kurie turėtų būti susieti su funkcinės vietos tipu. Pasirinkite **Įtraukti eilutę**, tada pasirinkite turto tipus. Jei čia įtraukiate turto tipų, funkcinėje vietoje naudojant šį funkcinės vietos tipą gali būti diegiami tik tie turto objektai, kurie naudoja šiuos turto tipus. Jei „FastTab“ **Turto tipai** nepasirenkami jokie turto tipai, galima diegti visų tipų turtą.
9. „FastTab“ **Priežiūros planai** pasirinkite priežiūros planus, kurie turėtų būti automatiškai nustatomi naujose funkcinėse vietose naudojant šį funkcinės vietos tipą. Pasirinkite **Įtraukti eilutę**, tada pasirinkite priežiūros planus. Jei čia įtrauksite priežiūros planus, funkcinėse vietose naudojant šį funkcinės vietos tipą bus galima naudoti tik šiuos planus.
10. „FastTab“ **Turto atributų reikalavimai** nustatykite turto atributus, kurie turėtų būti automatiškai nustatomi naujose funkcinėse vietose naudojant šį funkcinės vietos tipą. Pasirinkite **Įtraukti eilutę**, tada pasirinkite atributą. Šie atributo reikalavimai naudojami kaip gairės. Jos nėra patikrintos pagal turtui nustatytus atributus (**·** > **·** > **Turto** valdymo turtas Visas turtas> turtą galite pasirinkti sąrašo puslapyje > Mygtukas **Bendra** > **atributai).** Atributo reikalavimai rodomi įdiegus turtą funkcinėse vietose.
11. „FastTab“ **Leistini tipai** pasirinkite funkcinių vietų tipus, kurie turėtų tikti antrinių funkcinių vietų tipams, susijusiems su pagrindiniu funkcinės vietos tipu, kuriam naudojamas pasirinktas funkcinės vietos tipas.
12. „FastTab“ **Atributai** pasirinkite funkcinės vietos atributus, kurie turėtų būti automatiškai nustatomi funkcinėse vietose naudojant šį funkcinės vietos tipą. Pasirinkite **Įtraukti eilutę**, tada pasirinkite atributą.


>[!NOTE] 
>„FastTab“ **Bendra** galima peržiūrėti funkcinės vietos tipui nustatytų turto tipų, priežiūros planų, turto atributų reikalavimų, leistinų tipų, atributų ir funkcinių vietų apžvalgą. Lauke **Funkcinės vietos** rodomos kelios funkcinės vietos, kurios naudoja funkcinės vietos tipą. Naudojant mygtuką **Kopijuoti** galima nukopijuoti parametrus iš funkcinės vietos tipo į pasirinktą funkcinės vietos tipą.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]