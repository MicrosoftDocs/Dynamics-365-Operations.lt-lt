---
title: Priežiūros užklausos
description: Šiame straipsnyje pateikiama apžvalga apie priežiūros užklausų valdymą turto valdyme
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 488b6505aba246aa3a6ea69436514a274403bf49
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015644"
---
# <a name="maintenance-requests"></a>Priežiūros užklausos

[!include [banner](../../includes/banner.md)]

Priežiūros užklausos yra pranešimai arba deklaracijos, sukurtos siekiant pranešti vadovui arba planuotojui, kad gali prireikti atlikti turto priežiūros arba remonto užduotį, nesukuriant darbo užsakymo. Jei priežiūros užklausos turinys laikomas tinkamu, remiantis priežiūros užklausa galima sukurti darbo užsakymą.

Modulyje Turto valdymas galima kurti bet kurio turto priežiūros užklausas. Atsižvelgiant į tai, kaip jūsų įmonėje naudojamos priežiūros užklausos, galima kurti įvairių tipų priežiūros užklausas. Štai keletas pavyzdžių:

- Priežiūros užklausos
- Pastabos
- Taisymai arba patobulinimai
- Investicijos
- Sandėlio remontas (Šis tipas naudojamas, kai gaunate turtą iš kitos vietos, kad galėtumėte atlikti priežiūros arba remonto užduotį, ir paskui atlikę užduotį turtą grąžinate.)

## <a name="view-maintenance-requests"></a>Peržiūrėti priežiūros užklausas

Norėdami peržiūrėti priežiūros užklausas, **pasirinkite Turto** \> **valdymo priežiūros** \> **užklausos** Visos priežiūros užklausos, **Aktyvios priežiūros užklausos arba** Mano funkcinės **vietos priežiūros užklausos.** Kiekviename sąrašo puslapyje pateikiama dalis informacijos, susijusios su priežiūros užklausa.

![Peržiūrėti priežiūros užklausas.](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Sąrašo puslapyje **Mano funkcinės vietos priežiūros užklausos** galite peržiūrėti priežiūros užklausų, kuriose yra funkcinių vietų, su kuriomis esate susijęs kaip darbuotojas, arba turto, įdiegto funkcinėse vietose, su kuriomis esate susijęs kaip darbuotojas, sąrašą. (Informacijos apie tai, kaip nustatyti funkcines vietas priežiūros darbuotojams, rasite skyriuje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Nors kliento abonemento informacija pasiekiama Turto tarnybos valdyme (išorinė priežiūra), ji nepasiekiama modulyje Turto valdymas (vidinė priežiūra).

Norėdami atidaryti įrašo išsamios informacijos rodinį, sąrašo puslapio **Visos priežiūros užklausos** tinklelio rodinyje pasirinkite saitą stulpelyje **Priežiūros užklausa**.

![Peržiūrėti priežiūros užklausos informaciją.](media/02-manage-maintenance-requests.png)

Mygtukai, esantys veiksmų srityje, tvarkomi skirtukuose. Toliau pateikiamoje lentelėje trumpai aprašyti mygtukai, susiję su turto valdymu.

| Mygtuko pavadinimas                      | Aprašymas |
|----------------------------------|-------------|
| Redagavimas                             | Redaguojama pasirinkta priežiūros užklausa. |
| Naujos                              | Sukuriama nauja priežiūros užklausa. |
| Naikinti                           | Naikinama pasirinkta priežiūros užklausa. |
| Darbo užsakymų telkinys                  | Pasirinkta priežiūros užklausa prijungiama prie darbo užsakymų telkinio. |
| Darbo užsakymas                       | Darbo užsakymas sukuriamas pagal pasirinktą priežiūros užklausą. |
| Turto gedimas                      | Spustelėjus **Turto gedimai**, galima sukurti pasirinktos priežiūros užklausos gedimo registravimą. |
| Darbo užsakymai                      | Rodomas visų darbo užsakymų, kurie yra susiję su pasirinkta priežiūros užklausa, sąrašas. |
| Atnaujinti priežiūros užklausos būseną | Atnaujinama priežiūros užklausos būsena. |
| Ciklo būsenų žurnalas              | Pateikiamas žurnalas, kuriame registruojami pasirinktos priežiūros užklausos ciklo būsenos. |
| Išsami priežiūros užklausos informacija      | Spausdinama ataskaita, kurioje pateikiama išsami informacija apie pasirinktą priežiūros užklausą. |
| Siųsti skolintą turtą                  | Pasirenkamas skolintas turtas, kuris turėtų laikinai pakeisti turtą, pasirinktą pasirinktoje priežiūros užklausoje. |
| Grąžinti skolintą turtą                | Registruojamas skolinto turto grąžinimas. |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]