---
title: Dvigubo rašymo sąranka iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį tarp naujos Finance and Operations aplinkos ir naujos Common Data Service aplinkos iš „Microsoft Dynamics Lifecycle Services“ (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 75765c0cc03c64030fac6bc656f57a143828b85b
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112487"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Dvigubo rašymo sąranka iš „Lifecycle Services“

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį tarp naujos Finance and Operations aplinkos ir naujos Common Data Service aplinkos iš „Microsoft Dynamics Lifecycle Services“ (LCS).

## <a name="prerequisites"></a>Būtinieji komponentai

Norėdami nustatyti dvigubo rašymo ryšį, turite turėti administratoriaus statusą.

+ Turite turėti prieigos prie nuomotojo teisę.
+ Turite būti administratorius tiek Finance and Operations, tiek Common Data Service aplinkose.

## <a name="set-up-a-dual-write-connection"></a>Dvigubo rašymo ryšio nustatymas

Norėdami nustatyti dvigubo rašymo ryšį, atlikite toliau nurodytus veiksmus.

1. Nueikite į savo projektą, esantį LCS.
2. Pasirinkite **Konfigūruoti**, kad įdiegtumėte naują aplinką.
3. Pasirinkite versiją. 
4. Pasirinkite topologiją. Jei galima tik viena topologija, ji pasirenkama automatiškai.
5. Atlikite pirmuosius veiksmus vedlyje **Diegimo parametrai**.
6. Skirtuke **Common Data Service** atlikite vieną iš toliau nurodytų veiksmų:

    - Jei Common Data Service aplinka jau parengta jūsų nuomininkui, ją galite pasirinkti.

        1. Parinktį **Konfigūruoti Common Data Service** nustatykite į **Taip**.
        2. Lauke **Galimos aplinkos** pasirinkite aplinką, į kurią norite integruoti savo Finance and Operations duomenis. Į sąrašą įeina visos aplinkos, kuriose turite administratoriaus privilegijas.
        3. Norėdami nurodyti, kad sutinkate su pateiktomis sąlygomis, pasirinkite žymės langelį **Sutinku**.

        ![Skirtukas Common Data Service, kai aplinka Common Data Service parengta jūsų nuomotojui](../dual-write/media/lcs_setup_1.png)

    - Jei jūsų nuomotojas dar neturi Common Data Service aplinkos, bus parengta nauja aplinka.

        1. Parinktį **Konfigūruoti Common Data Service** nustatykite į **Taip**.
        2. Įveskite Common Data Service aplinkos pavadinimą.
        3. Pasirinkite regioną, kuriame norite įdiegti aplinką.
        4. Pasirinkite numatytąją aplinkos kalbą ir valiutą.

            > [!NOTE]
            > Vėliau pakeisti kalbos ir valiutos negalite.

        5. Norėdami nurodyti, kad sutinkate su pateiktomis sąlygomis, pasirinkite žymės langelį **Sutinku**.

        ![Skirtukas Common Data Service, kai jūsų nuomotojas dar neturi Common Data Service aplinkos](../dual-write/media/lcs_setup_2.png)

7. Atlikite likusius veiksmus vedlyje **Diegimo parametrai**.
8. Kai aplinka įgyja statusą **Įdiegta**, atidarykite aplinkos išsamios informacijos puslapį. Skyriuje **Common Data Service aplinkos informacija** pateikiami susietų Finance and Operations ir Common Data Service aplinkų pavadinimai.

    ![Common Data Service aplinkos informacijos skyrius](../dual-write/media/lcs_setup_3.png)

9. Finance and Operations aplinkos administratorius turi prisijungti prie LCS ir pasirinkti **Programėlių CDS saitas**, kad susiejimas būtų užbaigtas. Aplinkos informacijos puslapyje pateikiama administratoriaus kontaktinė informacija.

    Susiejimą užbaigus, būsena atnaujinama į **Aplinkos siejimas sėkmingai užbaigtas**.

10. Norėdami atidaryti aplinkoje Finance and Operations esančią darbo sritį **Duomenų integravimas** ir valdyti pasiekiamus šablonus, pasirinkite **Programėlių CDS saitas**.

    ![Mygtukas „Programėlių CDS saitas“, esantis Common Data Service aplinkos informacijos sekcijoje](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Negalite atsieti aplinkos naudodami LCS. Norėdami atsieti aplinką, aplinkoje Finance and Operations atidarykite darbo sritį **Duomenų integravimas** ir pasirinkite **Atsieti**.
