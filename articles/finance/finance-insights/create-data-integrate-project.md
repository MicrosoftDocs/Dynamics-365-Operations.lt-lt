---
title: Duomenų integratoriaus projekto kūrimas (peržiūros versija)
description: Šioje temoje paaiškinama, kaip sukurti duomenų integratoriaus projektą.
author: ShivamPandey-msft
ms.date: 07/24/2020
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
ms.openlocfilehash: 9ecf6ef7b7f052ebbb1201dcd04a7431f5b72ce5
ms.sourcegitcommit: b64c52d85aa6f110f3b1959a5521637dd8631b5b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867452"
---
# <a name="create-a-data-integrator-project-preview"></a>Duomenų integratoriaus projekto kūrimas (peržiūros versija)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip sukurti duomenų integratoriaus projektą.

1. Prisijunkite prie „Microsoft Dynamics 365 Finance“.
2. Eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite **Duomenų objektai**. Palaukite, kol visi duomenų objektai bus atnaujinti, prieš pereidami prie tolesnio veiksmo.
3. Atidarykite [„Power Apps“ portalą](https://make.powerapps.com/) ir atlikite tolesnius veiksmus.

    1. Pasirinkite tinkamą aplinką.
    2. Kairiojoje naršymo srityje pasirinkite **Duomenys \> Ryšiai**.
    3. Prisijunkite prie atitinkamų tolesnių elementų egzempliorių.

        - „Dynamics 365“
        - „Dynamics 365 for Fin & Ops“

4. Atidarykite [„Power Apps“ aplinkas](https://admin.powerapps.com/environments) ir atlikite tolesnius veiksmus.

    1. Pasirinkite **Duomenų integratorius**.
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

        - Kliento mokėjimo įžvalgų rezultatai (CDS į „Fin and Ops“)
            - Jei naudojate 10.0.17 ar vėlesnę versiją, turite naudoti šabloną, pavadinimu Kliento mokėjimo įžvalgų rezultatai (CDS į Fin ir Ops 10.0.17+).
        - Grynųjų pinigų srautų laiko serijos rezultatai (CDS į „Fin and Ops“)
        - Biudžeto laiko serijos rezultatai (CDS į „Fin and Ops“)

    2. Nustatykite tinkamą kiekvieno projekto planavimą.

> [!NOTE]
> Jei nematote reikiamų objektų CDS, eikite į **Kreditas ir surinkimas > Sąranka > „Finance Insights” > „Finance Insights” parametrai**, įjunkite funkciją Kliento mokėjimo prognozės ir spustelėkite mygtuką **Sukurti prognozavimo modelį**. Kai DI modelio diegimas baigtas (sėkmingas arba jo nepavyko atlikti), CDS objektai, kurių reikia kuriant integraciją, bus įdiegti į CDS.

## <a name="privacy-notice"></a>Privatumo pranešimas

Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
