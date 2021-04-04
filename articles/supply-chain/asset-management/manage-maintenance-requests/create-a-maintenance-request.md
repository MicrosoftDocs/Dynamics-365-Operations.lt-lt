---
title: Priežiūros užklausos kūrimas
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas sukurti priežiūros užklausą.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a85125853b3b69d33f07249e0d2aa7592de1cc8a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253427"
---
# <a name="create-maintenance-requests"></a>Priežiūros užklausos kūrimas

[!include [banner](../../includes/banner.md)]

 

Priežiūros užklausas galima kurti tada, kai techninės priežiūros darbuotojai arba gamybos darbuotojai nustato, kad įrangą reikia taisyti, tačiau remonto atlikti iš karto negalima.

**Pavyzdžiui:** Pavyzdžiui, techninės priežiūros darbuotojas atlieka remonto darbus ir pamato, kad reikia sutaisyti toje pačioje vietoje esančią detalę. Tačiau techninės priežiūros darbuotojas neturi laiko ar reikalingų atsarginių dalių, kad atliktų remonto darbus. Todėl techninės priežiūros darbuotojas sukuria priežiūros užklausą ir trumpai aprašo problemą.

Srities **Susijusi informacija**, esančios dešinėje puslapio **Visas turtas** arba **Aktyvus turtas** pusėje (**Turto valdymas**\>**Bendra**\>**Turtas**\>**Visas turtas** arba **Aktyvus turtas**), skyriuje **Aktyvios priežiūros užklausos** rodomos aktyviosios priežiūros užklausos, kurios pridėtos prie pasirinkto turto.

1. Pasirinkite **Turto valdymas** \> **Bendra** \> **Priežiūros užklausos** \> **Visos priežiūros užklausos** arba **Aktyvios priežiūros užklausos**.
2. Pasirinkite **Naujas**.
3. Dialogo lange **Kurti užklausą**, lauke **Priežiūros užklausos tipas** pasirinkite priežiūros užklausos tipą. Rekomenduojamas numatytasis tipas.
4. Lauke **Aprašas** įrašykite užklausos pavadinimą, kuris apibūdintų priežiūros užklausą.
5. Laukuose **Funkcinė vietovė** ir **Turtas** pasirinkite funkcinę vietovę, turtą arba funkcinės vietovės ir turto derinį. Galite sukurti priežiūros užklausą nepasirinkdami turto, nes jį galimą pridėti prie priežiūros užklausos vėliau. Jei prisijungęs priežiūros darbuotojas yra susijęs su ištekliais, kurie susiję su turtu, laukas **Turtas** nustatomas automatiškai.

    Jei priežiūros užklausa jau pridėta prie pasirinkto turto, dialogo lango **Kurti užklausą** viršuje pasirodo pranešimo juosta, kuri nurodo esamos priežiūros užklausos ID. Pranešimo juosta taip pat įspėja apie garantijos sutartį.

6. Lauke **Aptarnavimo lygis** pasirinkite aptarnavimo lygį, nurodantį užklausos skubumą.
7. Jei turtą pasirinkote 5 veiksme, gedimo registravimą galite sukurti naudodami laukus **Gedimo požymis**, **Gedimo sritis** ir **Gedimo tipas**.
8. Jei vykdant priežiūros užklausą atsirado techninės priežiūros prastova, įveskite prastovos pradžios datą ir laiką.

    Lauke **Pradėta** automatiškai atsiranda jūsų vardas.

10. **Faktinis pradžios laikas** laukas automatiškai nustatomas į dabartinę datą. Tačiau šio lauko reikšmę galite keisti.
11. Lauke **Pastabos** įveskite papildomas pastabas.
12. Pasirinkite **Gerai**.

![Kurti priežiūros užklausą](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a>Vėlesnis priežiūros užklausų apdorojimas

Sukūrus priežiūros užklausą, joje reikia atnaujinti tam tikrą informaciją, tačiau tai reikia atlikti prieš sukonvertuojant užklausą į darbo užsakymą. Paprastai šią užduotį atlieka planuotojas arba administratorius.

- Puslapyje **Visos priežiūros užklausos** arba **Aktyviosios priežiūros užklausos** pasirinkite norimą užklausą, tada pasirinkite **Redaguoti**.

Išsamios informacijos rodinyje galite atnaujinti įvairią informaciją. Štai keletas pavyzdžių:

- Pasirinkite ir patvirtinkite turtą. Jei vėliau norite pasirinkti kitą turtą, galite nustatyti parinktį **Turtas patvirtintas** į **Ne**.
- Pasirinkite atsakingą darbuotojų grupę ir (arba) atsakingą priežiūros darbuotoją. Daugiau informacijos apie būtiną konfigūraciją rasite [Už priežiūrą atsakingi darbininkai](../setup-for-maintenance-requests/responsible-workers.md).
- Pasirinkite priežiūros užduoties tipą ir, jei reikia, atitinkamą priežiūros užduoties variantą ir prekybą.
- Laukuose **Platuma** ir **Ilguma** įveskite geografines koordinates. Visos į priežiūros užklausą įtrauktos koordinatės automatiškai perkeliamos į atitinkamą darbo užsakymą. 

![Priežiūros užklausos atnaujinimas](media/04-manage-maintenance-requests.png)

> [!NOTE]
> Jei kurdami priežiūros užklausą pasirenkate turtą, prie jo galite pridėti vieną gedimą. Sukūrę priežiūros užklausą, pagal poreikius galite pridėti ir daugiau gedimų. Norėdami pridėti daugiau gedimų, puslapyje **Visos priežiūros užklausos** pasirinkite **Turto gedimas**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]