---
title: Darbo užsakymų įvadas
description: Šiame straipsnyje pateikta turto valdymo darbo užsakymų apžvalga.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderLineNote, EntAssetWorkOrderTable, EntAssetWorkOrderActive, EntAssetWorkOrderHoursInfoPart, EntAssetWorkOrderLineListPage, EntAssetWorkOrderAddObjectBOMItem, EntAssetWorkOrderTablePoolAdd, EntAssetWorkOrderPurchReqListPagePreviewPane, EntAssetWorkOrderPoolReferenceAdd, EntAssetWorkOrderWorkspace, EntAssetWorkOrderTableAdjust, EntAssetWorkOrderGantt, EntAssetWorkOrderNotes, EntAssetWorkOrderActivePart, EntAssetWorkOrderTableInfoPart, EntAssetWorkOrderLineListPagePreviewPane, EntAssetWorkOrderTool, EntAssetMobileWorkOrderLineDetails, EntAssetMobileWorkOrderLineList, EntAssetMobileWorkOrderDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5eb911ec4ba9655c4ecaea3bf9a4f8736fa036c2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016716"
---
# <a name="introduction-to-work-orders"></a>Darbo užsakymų įvadas

[!include [banner](../../includes/banner.md)]



Darbo užsakymai naudojami priežiūros užduotims tvarkyti, pateikti joms būtiną informaciją ir jų suvartojimui registruoti. Kiekviename darbo užsakyme gali būti viena arba keletas darbo užsakymo užduočių; su kiekvienu darbo užsakymu galima susieti vieną arba daugiau turto vienetų. Kiekvienoje darbo užsakymo užduotyje apibrėžiama turtui suplanuota priežiūros užduotis.

Darbo užsakymai gali būti kuriami toliau nurodytais būdais.

- Automatiškai jie kuriami naudojant formą [Priežiūros planų planavimas](../preventive-and-reactive-maintenance/schedule-maintenance-plans.md), kai pagal kalendorių vykdomuose priežiūros planuose nustatyta „Automatinis kūrimas“.

- Automatiškai jie kuriami naudojant formą [Priežiūros ciklų planavimas](../preventive-and-reactive-maintenance/maintenance-rounds.md), kai priežiūros cikluose nustatyta „Automatinis kūrimas“.

- Prevencinės priežiūros užduotys arba priežiūros užklausos kuriamos naudojant formą [Priežiūros grafikas](../preventive-and-reactive-maintenance/maintenance-schedule.md).

- Rankiniu būdu

- Puslapyje **Visos priežiūros užklausos**, **Aktyviosios priežiūros užklausos** arba **Mano funkcinės vietos priežiūros užklausos**.

>[!NOTE]
>Darbo užsakymų užduotys, susijusios su tuo pačiu turtu, yra susijusios su tuo pačiu projekto ID.

## <a name="all-work-orders"></a>Visi darbo užsakymai

Pasirinkite **Turto valdymo darbo** > **užsakymai Visi** > **darbo užsakymai, kad** atidarytumėte **visų darbo užsakymų** sąrašo puslapį. Šiame puslapyje pateikiamos visi darbo užsakymai ir dalis informacijos apie juos.

Toliau pateiktame paveikslėlyje parodytas sąrašo puslapio **Visi darbo užsakymai** pavyzdys.

![1 iliustracija.](media/01-work-orders.png)

Norėdami peržiūrėti tik aktyvių darbo užsakymų sąrašą, pasirinkite Turto **valdymo darbo** > **užsakymai Aktyvūs** > **darbo užsakymai**. 

Norėdami peržiūrėti darbo užsakymo užduočių, kuriose yra funkcinėse vietose, su kurias susiję su darbuotoju, sąrašą, **·** > **·** > **pasirinkite Turto valdymo darbo užsakymai Mano funkcinės vietos darbo užsakymo priežiūros užduotys.** (Darbuotojų ir funkcinių vietų ryšys nustatomas puslapyje **Darbuotojai**.) Daugiau informacijos žr. [Priežiūros darbuotojai ir darbuotojų grupės](../setup-for-objects/workers-and-worker-groups.md).)

Toliau pateikiami keli būdai, kaip naudoti puslapį **Visi darbo užsakymai**.

- Tinklelio rodinyje pasirinkite saitą, esantį stulpelyje **Darbo užsakymas**, kad būtų parodytas pasirinkto įrašo informacijos rodinys. Tada galite pasirinkti **Redaguoti**, kad įrašas būtų atidarytas redagavimo režimu.

- Informacijos rodinyje galite peržiūrėti išsamią informaciją apie darbo užsakymą.  

- Informacijos rodinyje pasirinkite skirtuką **Eilutės**, kad peržiūrėtumėte išsamią informaciją apie darbo užsakymo užduotį, arba pasirinkite skirtuką **Antraštė**, kad peržiūrėtumėte išsamią informaciją apie darbo užsakymą.  

- Norėdami peržiūrėti papildomą informaciją, susijusią su pasirinktu darbo užsakymu, puslapio dešinėje pusėje išplėskite **susijusios informacijos** sritį.

Toliau pateiktame paveikslėlyje parodytas informacijos rodinio **Visi darbo užsakymai** pavyzdys.

![2 iliustracija.](media/02-work-orders.png)


Mygtukai, esantys veiksmų srityje, tvarkomi skirtukuose. Toliau pateikiamoje lentelėje trumpai aprašyti mygtukai, susiję su turto valdymu.



| Mygtuko pavadinimas                     | Aprašymas                                                                                                                                                                                                                                                             |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Redagavimas                            | Pasirinkto darbo užsakymo redagavimas.                                                                                                                                                                                                                                           |
| Naujos                             | Naujo darbo užsakymo kūrimas.                                                                                                                                                                                                                                                  |
| „Delete“                          | Pasirinkto darbo užsakymo naikinimas.                                                                                                                                                                                                                                         |
| Darbo užsakymų telkinys                 | Pasirinkto darbo užsakymo įtraukimas į darbo užsakymų telkinį arba jo pašalinimas iš darbo užsakymų telkinio.                                                                                                                                                                                           |
| Koreguoti                          | Informacijos apie pasirinktų darbo užsakymų numatomą pradžią ir pabaigą, aptarnavimo lygį, atsakingą priežiūros darbuotoją arba atsakingą priežiūros darbuotojų grupę koregavimas.                                                                                                                                     |
| Susijęs darbo užsakymas              | Naujo darbo užsakymo, susijusio su pasirinkta darbo užsakymo užduotimi, kūrimas. Naudinga, jei norite registruoti pirminius ir antrinius darbo užsakymus.                                                                                                                              |
| Kopijuoti darbo užsakymą                 | Naujo darbo užsakymo kūrimas pagal esamą darbo užsakymą.                                                                                                                                                                                                               |
| Įvykių retrospektyva                   | Darbo užsakymo registravimo retrospektyvos peržiūra.                                                                                                                                                                                                                |
| Darbo užsakymo priežiūros darbo pastabos                           | Darbo užsakymo aprašo arba pastabų kūrimas. Pirmiausia pasirinkite **Įtraukti lako žymą**, kad į pastabą įtrauktumėte savo vartotojo vardą ir laiko žymą. Pastabos rodomos skirtuke **Aprašas**, esančiame puslapio **Darbo užsakymas** „FastTab” **Eilutės informacija**.         |
| Įrankiai                           | Būtinų darbo užsakymo įrankių kūrimas. Įrankiai pateikiami kaip ištekliai, pasirinkus **Organizacijos administravimas** > **Ištekliai** > **Ištekliai**.                                                                                                      |
| Prižiūrimo turto kontrolinis sąrašas           | Su darbo užsakymu susijusio turto kontrolinio sąrašo peržiūra.                                                                                                                                                                                                              |
| Turto gedimas                     | Turto gedimo informacijos peržiūra arba registravimas. Ši informacija naudojama gedimų valdyme.                                                                                                                                                                                      |
| Prižiūrimo turto prastova            | Darbo užsakymo prižiūrimo turto prastovos nurodymas.                                                                                                                                                                                                                               |
| Sąlygos įvertinimas            | Darbo užsakymo sąlygos įvertinimo matmenų registravimas.                                                                                                                                                                                                             |
| Turto skaitikliai                 | Turto skaitiklio registracijų kūrimas arba peržiūra.                                                                                                                                                                                                                     |
| Prognozė                        | Darbo užsakymo prognozių kūrimas arba peržiūra.                                                                                                                                                                                                                               |
| Žurnalai                        | Darbo užsakymo žurnalų kūrimas arba peržiūra. Žurnalo eilutes galimo nukopijuoti iš prognozių.                                                                                                                                                                                         |
| Projekto operacijos            | Visų su turto darbo užsakymais susijusių užregistruotų operacijų peržiūra.                                                                                                                                                                                             |
| Darbo užsakymo būsenos naujinimas           | Darbo užsakymo ciklo būsenos naujinimas.                                                                                                                                                                                                                                                |
| Ciklo būsenos žurnalas                      | Pateikiamas žurnalas, kuriame registruojamos pasirinkto darbo užsakymo ciklo būsenos.                                                                                                                                                                                                                   |
| Turto dokumentai                | Su darbo užsakymu susijusio turto dokumentų sąrašo peržiūra. Šie dokumentai pateikiami pasirinkus **Turto valdymas** > **Sąranka** > **Turto dokumentai**.                                                                                                 |
| Grafikas                        | Pasirinktų darbo užsakymų planavimas.                                                                                                                                                                                                                                      |
| Išsiųsti            | Pasirinkto darbo užsakymo planavimas vienam darbuotojui.                                                                                                                                                                                                                        |
| Naikinti grafiką                 | Pasirinkto darbo užsakymo grafiko naikinimas.                                                                                                                                                                                                                          |
| Suplanuotos darbo užsakymo priežiūros užduotys             | Sąrašo puslapio **Suplanuotos darbo užsakymo priežiūros užduotys** atidarymas.                                                                                                                                                                                                                             |
| Darbo užsakymo pirkimo paraiška | Sąrašo puslapio **Darbo užsakymo pirkimo paraiška** atidarymas.                                                                                                                                                                                                                 |
| Darbo užsakymo pirkimas             | Sąrašo puslapio **Darbo užsakymo pirkimas** atidarymas.                                                                                                                                                                                                                             |
| Išlaidų kontrolė                    | Darbo užsakymo biudžeto išlaidų ir faktinių išlaidų palyginimas.                                                                                                                                                                                                                |
| Valandų kontrolė                    | Darbo užsakymo prognozuotų valandų ir faktinių valandų palyginimas.                                                                                                                                                                                                                |
| Darbo užsakymo ataskaita               | Darbo užsakymo ataskaitos spausdinimas.                                                                                                                                                                                                                                                |
| Darbo užsakymo suvartojimas          | Suvartojimo ataskaitos spausdinimas.                                                                                                                                                                                                                                               |


Mygtukai veiksmų srities skirtuko **Darbo užsakymas** grupėje **Projektas** yra susiję su modulio **Projektų valdymas ir apskaita** funkcija, susijusia su prognozėmis, žurnalais ir sąskaitų išrašymu.

>[!NOTE]
>Sukurtas darbo užsakymo prognozes galima įtraukti, vykdant bendrąjį planavimą ir naudojant prognozės modelį, pasirinktą puslapyje **Turto valdymo parametrai**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]