---
title: Duomenų integravimo projekto kūrimas
description: Šiame straipsnyje paaiškinama, kaip sukurti duomenų integravimo projektą.
author: ShivamPandey-msft
ms.date: 05/06/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4ff4f88c6c5d55d853aebd7d437bfb107292fb2f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876246"
---
# <a name="create-a-data-integration-project"></a>Duomenų integravimo projekto kūrimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip sukurti duomenų integravimo projektą.

1. Prisiregistruoti Microsoft Dynamics prie 365 finansų.
2. Eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite **Duomenų objektai**. Palaukite, kol visi duomenų objektai bus atnaujinti, prieš pereidami prie tolesnio veiksmo.
3. Atidarykite [„Power Apps“ portalą](https://make.powerapps.com/) ir atlikite tolesnius veiksmus.

    1. Pasirinkite tinkamą aplinką.
    2. Kairiojoje naršymo srityje pasirinkite **Dataverse\> Ryšiai**.
    3. Prisijunkite prie atitinkamų tolesnių elementų egzempliorių.

        - „Dynamics 365“
        - „Dynamics 365 for Fin & Ops“

4. Atidarykite [„Power Apps“ aplinkas](https://admin.powerapps.com/environments) ir atlikite tolesnius veiksmus.

    1. Pasirinkite **duomenų integravimą**.
    2. Pasirinkite **Ryšio rinkiniai**.
    3. Pasirinkite **Naujas ryšio rinkinys**.
    4. Įveskite ryšio pavadinimą.
    5. Pasirinkite atitinkamus tolesnių elementų ryšius.

        - „Dynamics 365“
        - „Dynamics 365 for Fin & Ops“

    6. Pasirinkite tinkamą organizacijos susiejimą.
    7. Pasirinkite **Kurti**.

5. Atidarykite [„Power Apps“ aplinkas](https://admin.powerapps.com/environments) ir atlikite tolesnius veiksmus.  

    1. Sukurkite vieną duomenų integravimo projektą kiekvienam iš šių šablonų naudodami ką tik sukurtą ryšio rinkinį:

        - Kliento mokėjimų žinių žinių rezultatai (CDS į Fin ir Ops 10.0.17+)
        - Grynųjų pinigų srautų laiko serijos rezultatai (CDS į „Fin and Ops“)
        - Biudžeto laiko serijos rezultatai (CDS į „Fin and Ops“)

      > [!NOTE]
      > Kuriant kelis kiekvieno šablono duomenų integravimo projektus gali kilti klaidų, kurios užblokuos naujinimus.

    2. Nustatykite tinkamą kiekvieno projekto planavimą.

> [!NOTE]
> Jei nematote Dataverse reikalingų objektų, **·** > **·** > **·** > **eikite** į Kreditų ir rinkinių nustatymas Finansų žinių rinkimo parametrai, įgalinkite funkciją, **Kliento mokėjimo numatymes**, **tada pasirinkite Sukurti numatymą modelį.** Kai AI modelio diegimas baigtas, bus įdiegti Dataverse objektai, kurių reikia integravimui sukurti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
