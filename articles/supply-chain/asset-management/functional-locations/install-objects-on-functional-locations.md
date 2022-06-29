---
title: Turto diegimas funkcinėse vietose
description: Šiame straipsnyje paaiškinama, kaip įdiegti turtą funkcinėse turto valdymo vietose.
author: johanhoffmann
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationObjectChange, EntAssetFunctionalLocationObjectInstall, EntAssetFunctionalLocationObject
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ae571f4ad7210b31d212b0472610b36dc5c488b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016078"
---
# <a name="install-assets-on-functional-locations"></a>Turto diegimas funkcinėse vietose

[!include [banner](../../includes/banner.md)]

 

Sukūrus funkcinės vietos struktūras, kitas žingsnis yra įdiegti turtą atitinkamose funkcinėse vietose. Šiame straipsnyje paaiškinama, kaip įdiegti turtą tose funkcinėse turto valdymo vietose. Daugiau informacijos apie turto kūrimą žr. [Turto pristatymas](../objects/introduction-to-objects.md).

Jei sukūrėte turto struktūrą, visa turto struktūra turi būti įdiegta funkcinėje vietoje. Todėl funkcinėje vietoje galima pasirinkti tik pagrindinį turtą (aukščiausio lygio turtą, kuris neturi pagrindinio turto). Funkcinėje vietoje taip pat bus įdiegtas visas susijęs antrinis turtas (antrinis turtas). Diegiant turtą funkcinėje vietoje, į jas gali būti automatiškai perkeltos funkcinės vietos finansinės dimensijos, atsižvelgiant į funkcinei vietai parinkto funkcinės vietos tipo nustatymą. Daugiau informacijos apie funkcinės vietos tipų nustatymą žr. [Funkcinių vietų tipai](../setup-for-functional-locations/functional-location-types.md).

> [!NOTE]
> Galite nustatyti turto tipus funkcinės vietos tipui, kuris naudojamas funkcinėje vietoje. Tokiu atveju, diegiant turtą funkcinėje vietoje, turto, kurį galima diegti funkcinėje vietoje, sąrašuose rodomas tik pagrindinis turtas, turintis tą patį turto tipą.

Įdiegus turtą funkcinėje vietoje galima pagal poreikius pakeisti pagrindinį turtą arba turto struktūrą. Įdiegus turtą pasirenkamas pagrindinis turtas, kurį norite pakeisti. Taip pat bus pakeistas visas susijęs antrinis turtas. 


## <a name="install-an-asset-structure-on-a-functional-location"></a>Turto struktūros diegimas funkcinėje vietoje

1. Pasirinkite **turto valdymo funkcines** \> **vietas** \> **visose funkcinėse vietose** arba aktyviose **funkcinėse vietose.**
2. Pasirinkite funkcinę vietą, kurioje bus diegiamas turtas.
3. Pasirinkite **Diegti turtą**.

    Dalyje **Atributai** rodomas turto atributų reikalavimų, nustatytų funkcinės vietos tipui, pasirinktam funkcinei vietai, sąrašas. Atributai skirti tik informacijai. Sistema netikrina atributų pagal turto atributus, kurie nustatyti diegiamam turtui. Šį tikrinimą būtina atlikti pasirinkus turtą lauke **Turtas.**

4. Lauke **Turtas** pasirinkite norimą diegti pagrindinį turtą. Visas susijęs antrinis turtas automatiškai įtraukiamas į diegimą.

    Dalyje **Turto atributai** turto sąrašo dešinėje rodomi turto atributai, susiję su pasirinktu turtu.

5. Lauke **Efektyvus** pasirinkite turto diegimo tinkamumo datą ir laiką. Po šios datos ir laiko išlaidos turtui ir susijusiam antriniam turtui bus susietos su funkcine vieta.

    > [!NOTE]
    > Turto atributai, nustatyti turtui, įtraukiami į dalį **Atributai.** Pavyzdžiui, atributo **Svoris** reikalavimas įtrauktas kaip reikalavimas į turtą ir į funkcinę vietą. Jei turtui priskirti to paties tipo kaip funkcinė vieta atributo reikalavimai, turto atributo reikalavimų reikšmės įvedamos laukuose **Reikšmė**. Todėl galima patikrinti turto reikšmes pagal atributo reikalavimus, kurie nustatyti funkcinei vietai. Funkcinei vietai nustatyti atributo reikalavimai pažymėti varnele.

6. Pasirinkite **Gerai**.

    > [!NOTE]
    > Jei norite pakeisti turto diegimą diegdami jį naujoje funkcinėje vietoje, atlikite šios procedūros 1–6 veiksmus. Diegiant turtą naujoje funkcinėje vietoje, turtas automatiškai pašalinamas iš ankstesnės funkcinės vietos. Visos aktyvios priežiūros užklausos arba darbo užsakymai, kurie buvo sukurti turtui prieš jį diegiant naujoje funkcinėje vietoje, **nėra** automatiškai perkeliami į naują funkcinę vietą. Jei šios priežiūros užklausos ir darbo užsakymai vis tiek būtini turtui, turite rankiniu būdu juos iš naujo sukurti, kai turtas bus įdiegtas naujoje vietoje.

7. Norėdami peržiūrėti funkcinėje vietoje įdiegto viso turto, įskaitant antrinį turtą, sąrašą, puslapyje **Visos funkcinės vietos** pasirinkite funkcinę vietą, tada pasirinkite **Turtas**.
8. Norėdami peržiūrėti su funkcinėje vietoje įdiegtu turtu susijusių aktyvių priežiūros užklausų, aktyvių darbo užsakymų ar klaidingų registracijų sąrašą, puslapyje **Visos funkcinės vietos** pasirinkite funkcinę vietą, tada pasirinkite **Užklausos**, **Darbo užsakymai** arba **Gedimai**.

> [!NOTE]
> Pakeitus su turtu susijusius duomenis jie automatiškai atnaujinami funkcinėje vietoje, kurioje įdiegtas turtas. Šis automatinis naujinimas susijęs su priežiūros užklausų, darbo užsakymų, turto gedimų registravimų, prižiūrimo turto prastovų registracijų ir turto matų registracijų pakeitimais.

## <a name="automatically-create-one-asset-on-a-functional-location"></a>Automatinis vieno turto kūrimas funkcinėje vietoje

Galima nustatyti funkcinės vietos etapus ir funkcinės vietos tipus, kad funkcinėje vietoje būtų tvarkomas automatinis *vieno* turto kūrimas. Turtui skiriamas tas pats ID ir pavadinimas, kaip ir funkcinei vietai. Ši funkcija gali būti naudinga, kai tvarkote didelio, statinio turto, pvz., pastato, priežiūrą.

Prieš tai, kai bus galima automatiškai kurti turtą funkcinėje vietoje, turi būti pasiekiami tolesni nustatymų duomenys:

- Sukurkite funkcinės vietos tipą, kad būtų galima tvarkyti automatinį turto kūrimą. Lauke **Turto tipas** pasirinkite turto tipą. Daugiau informacijos žr. [Funkcinių vietų tipai](../setup-for-functional-locations/functional-location-types.md).
- Sukurkite funkcinės vietos ciklo būseną, kad būtų galima tvarkyti automatinį turto kūrimą. Parinktį **Kurti turtą** nustatykite į **Taip**. Daugiau informacijos žr. [Funkcinių vietų ciklo būsenos](../setup-for-functional-locations/functional-location-stages.md).

Kai pasiekiami nustatymų duomenys, būsite pasirengę kurti turtą.

1. Puslapyje **Visos funkcinės vietos** įsitikinkite, kad funkcinėje vietoje, kurioje norite automatiškai kurti turtą, naudojamas funkcinės vietos tipas, kurį sukūrėte šiam tikslui.
2. Sąraše pasirinkite funkcinę vietą.
3. Pasirinkite **Naujinti funkcinės vietos būseną**, tada pasirinkite ciklo būseną, kurią sukūrėte šiuo tikslu. Vienas turtas dabar automatiškai įdiegiamas funkcinėje vietoje. Turtas turi tokį patį pavadinimą, kaip funkcinė vieta.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]