---
title: Priežiūros užklausos
description: Šioje temoje apžvelgiama, kaip valdyti priežiūros užklausas modulyje Turto valdymas.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d81fed34c1eb9ff0347c67086ceb08c038d8eb08
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253379"
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

## <a name="view-maintenance-requests"></a>Priežiūros užklausų peržiūra

Norėdami peržiūrėti priežiūros užklausas, pasirinkite **Turto valdymas** \> **Dažnas** \> **Techninės priežiūros prašymai** \> **Visos priežiūros užklausos**, **Aktyvios priežiūros užklausos** arba **Mano funkcinės vietos priežiūros užklausos**. Kiekviename sąrašo puslapyje pateikiama dalis informacijos, susijusios su priežiūros užklausa.

![Peržiūrėti priežiūros užklausas](media/01-manage-maintenance-requests.png)

> [!NOTE]
> Sąrašo puslapyje **Mano funkcinės vietos priežiūros užklausos** galite peržiūrėti priežiūros užklausų, kuriose yra funkcinių vietų, su kuriomis esate susijęs kaip darbuotojas, arba turto, įdiegto funkcinėse vietose, su kuriomis esate susijęs kaip darbuotojas, sąrašą. (Informacijos apie tai, kaip nustatyti funkcines vietas priežiūros darbuotojams, rasite skyriuje [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).)
> 
> Nors kliento abonemento informacija pasiekiama Turto tarnybos valdyme (išorinė priežiūra), ji nepasiekiama modulyje Turto valdymas (vidinė priežiūra).

Norėdami atidaryti įrašo išsamios informacijos rodinį, sąrašo puslapio **Visos priežiūros užklausos** tinklelio rodinyje pasirinkite saitą stulpelyje **Priežiūros užklausa**.

![Peržiūrėti priežiūros užklausos informaciją](media/02-manage-maintenance-requests.png)

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