---
title: Priežiūros užklausos kūrimas
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas sukurti priežiūros užklausą.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 147388d5052bd14851bbddfbb7fe25297a43f104
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102979"
---
# <a name="create-maintenance-requests"></a>Priežiūros užklausos kūrimas

[!include [banner](../../includes/banner.md)]

 

Priežiūros užklausas galima kurti tada, kai techninės priežiūros darbuotojai arba gamybos darbuotojai nustato, kad įrangą reikia taisyti, tačiau remonto atlikti iš karto negalima.

**Pavyzdys:** Atlikdamas remonto darbus, techninės priežiūros darbuotojas pastebi, kad reikia sutaisyti kitą detalę, esančią toje pačioje vietoje. Tačiau techninės priežiūros darbuotojas neturi laiko ar reikalingų atsarginių dalių, kad atliktų remonto darbus. Todėl jis sukuria detalės priežiūros užklausą ir trumpai aprašo problemą.

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