---
title: Duomenų integravimo projekto kūrimas
description: Šioje temoje paaiškinama, kaip sukurti duomenų integravimo projektą.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 956524e3778eed9898374952466f70c37c99163f
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968942"
---
# <a name="create-a-data-integration-project"></a>Duomenų integravimo projekto kūrimas

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip sukurti duomenų integravimo projektą.

1. Prisijunkite prie „Microsoft Dynamics 365 Finance“.
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

    1. Kurkite tolesnių šablonų duomenų integravimo projektus, naudodami ką tik sukurtą ryšio rinkinį.

        - Kliento mokėjimų žinių žinių rezultatai (CDS į Fin ir Ops 10.0.17+)
        - Grynųjų pinigų srautų laiko serijos rezultatai (CDS į „Fin and Ops“)
        - Biudžeto laiko serijos rezultatai (CDS į „Fin and Ops“)

    2. Nustatykite tinkamą kiekvieno projekto planavimą.

> [!NOTE]
> Jei nematote reikiamų objektų CDS, eikite į **Kreditas ir surinkimas > Sąranka > „Finance Insights” > „Finance Insights” parametrai**, įjunkite funkciją Kliento mokėjimo prognozės ir spustelėkite mygtuką **Sukurti prognozavimo modelį**. Kai DI modelio diegimas baigtas (sėkmingas arba jo nepavyko atlikti), CDS objektai, kurių reikia kuriant integraciją, bus įdiegti į CDS.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
