---
title: Turto skolinimas
description: Šioje temoje aprašoma, kaip modulyje Turto valdymas užregistruoti skolinamą turtą.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a365fb5b1e0126b9de56bcc84a14f2352208d4f
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571719"
---
# <a name="asset-loans"></a>Turto skolinimas

[!include [banner](../../includes/banner.md)]

 

Jei jūsų įmonė vykdo iš vidinių vietų ar klientų gauto turto remonto darbus ar priežiūros užduotis, ir jei jūs laikinai skolinate turtą šioms vietoms ar klientams, modulyje Turto valdymas galima sekti ir turto skolinimą.

## <a name="register-asset-loans-on-a-maintenance-request"></a>Turto skolinimo registravimas pagal priežiūros užklausą

1. Pasirinkite**Turto valdymas** \> **Bendra** \> **Priežiūros užklausos** \> **Visos priežiūros užklausos** arba **Aktyvios priežiūros užklausos**.
2. Pasirinkite priežiūros užklausą, kad užregistruotumėte skolinamą turtą, tada pasirinkite **Redaguoti**.
3. Puslapyje **Užklausa** pasirinkite **Siųsti skolinamą turtą**.
4. Pasirinkite turtą ir įveskite numatomą grąžinimo datą.
5. Pasirinkite **Gerai**.

> [!NOTE]
> - Skolinamą turtą galite siųsti tik tuo atveju, jei pasiekiamas to paties tipo turtas.
> - Jūsų skolinamas turtas turi turėti turto ciklo būseną, kuri leidžia jį naudoti kaip skolinamą turtą, kaip pvz., **InStorage**. Kai užregistruojamas skolinamas turtas, turto ciklo būsena automatiškai atnaujinama, kaip pvz., **OnLoan**.

Norėdami peržiūrėti visą turto, kurį paskolinote kitoms vietoms ar klientams, sąrašą, pasirinkite **Turto valdymas** \> **Bendra** \> **Paskola su įkeistu turtu** \> **Visos paskolos su įkeistu turtu**. Jei prie turto pažymėtas žymės langelis **Baigta**, turtas buvo užregistruotas kaip grąžintas jūsų įmonei.

![Priežiūros užklausų valdymas](media/06-manage-maintenance-requests.png)

Puslapyje **Aktyvusis turto skolinimas** galite peržiūrėti visą paskolinto turto, kuris dar nebuvo grąžintas jūsų įmonei, sąrašą.

## <a name="register-loan-assets-as-returned"></a>Skolinto turto grąžinimo registravimas

1. Pasirinkite **Turto valdymas** \> **Bendra** \> **Paskola su įkeistu turtu** \> **Aktyvios paskolos su įkeistu turtu**.
2. Pasirinkite paskolintą turtą, kurią norite užregistruoti kaip grąžintą, tada pasirinkite **Grąžinti paskolintą turtą**.
3. Laukelyje **Grąžinta** nustatykite datą ir laiką.
4. Pasirinkite **Gerai**.
5. Atnaujinkite sąrašo puslapį **Aktyvusis turto skolinimas** ir pamatysite, kad paskolintas turtas nebėra rodomas sąraše.
