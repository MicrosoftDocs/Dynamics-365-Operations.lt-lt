---
title: Dvigubo rašymo sąranka iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį tarp naujos Finance and Operations aplinkos ir naujos Dataverse aplinkos iš „Microsoft Dynamics Lifecycle Services“ (LCS).
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 25db9c58c3d09e44dcf11b48cae1a9eda4241c35
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683530"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Dvigubo rašymo sąranka iš „Lifecycle Services“

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje paaiškinama, kaip nustatyti dvigubo rašymo ryšį tarp naujos Finance and Operations aplinkos ir naujos Dataverse aplinkos iš „Microsoft Dynamics Lifecycle Services“ (LCS).

## <a name="prerequisites"></a>Būtinieji komponentai

Norėdami nustatyti dvigubo rašymo ryšį, turite turėti administratoriaus statusą.

+ Turite turėti prieigos prie nuomotojo teisę.
+ Turite būti administratorius tiek Finance and Operations, tiek Dataverse aplinkose.

## <a name="set-up-a-dual-write-connection"></a>Dvigubo rašymo ryšio nustatymas

Norėdami nustatyti dvigubo rašymo ryšį, atlikite toliau nurodytus veiksmus.

1. Nueikite į savo projektą, esantį LCS.
2. Pasirinkite **Konfigūruoti**, kad įdiegtumėte naują aplinką.
3. Pasirinkite versiją. 
4. Pasirinkite topologiją. Jei galima tik viena topologija, ji pasirenkama automatiškai.
5. Atlikite pirmuosius veiksmus vedlyje **Diegimo parametrai**.
6. Skirtuke **Dataverse** atlikite vieną iš toliau nurodytų veiksmų:

    - Jei Dataverse aplinka jau parengta jūsų nuomininkui, ją galite pasirinkti.

        1. Parinktį **Konfigūruoti Dataverse** nustatykite į **Taip**.
        2. Lauke **Galimos aplinkos** pasirinkite aplinką, į kurią norite integruoti savo Finance and Operations duomenis. Į sąrašą įeina visos aplinkos, kuriose turite administratoriaus privilegijas.
        3. Norėdami nurodyti, kad sutinkate su pateiktomis sąlygomis, pasirinkite žymės langelį **Sutinku**.

        ![Skirtukas Dataverse, kai aplinka Dataverse parengta jūsų nuomotojui](../dual-write/media/lcs_setup_1.png)

    - Jei jūsų nuomotojas dar neturi Dataverse aplinkos, bus parengta nauja aplinka.

        1. Parinktį **Konfigūruoti Dataverse** nustatykite į **Taip**.
        2. Įveskite Dataverse aplinkos pavadinimą.
        3. Pasirinkite regioną, kuriame norite įdiegti aplinką.
        4. Pasirinkite numatytąją aplinkos kalbą ir valiutą.

            > [!NOTE]
            > Vėliau pakeisti kalbos ir valiutos negalite.

        5. Norėdami nurodyti, kad sutinkate su pateiktomis sąlygomis, pasirinkite žymės langelį **Sutinku**.

        ![Skirtukas Dataverse, kai jūsų nuomotojas dar neturi Dataverse aplinkos](../dual-write/media/lcs_setup_2.png)

7. Atlikite likusius veiksmus vedlyje **Diegimo parametrai**.
8. Kai aplinka įgyja statusą **Įdiegta**, atidarykite aplinkos išsamios informacijos puslapį. Skyriuje **Dataverse aplinkos informacija** pateikiami susietų Finance and Operations ir Dataverse aplinkų pavadinimai.

    ![Dataverse aplinkos informacijos skyrius](../dual-write/media/lcs_setup_3.png)

9. Finance and Operations aplinkos administratorius turi prisijungti prie LCS ir pasirinkti **Programėlių CDS saitas**, kad susiejimas būtų užbaigtas. Aplinkos informacijos puslapyje pateikiama administratoriaus kontaktinė informacija.

    Susiejimą užbaigus, būsena atnaujinama į **Aplinkos siejimas sėkmingai užbaigtas**.

10. Norėdami atidaryti aplinkoje Finance and Operations esančią darbo sritį **Duomenų integravimas** ir valdyti pasiekiamus šablonus, pasirinkite **Programėlių CDS saitas**.

    ![Mygtukas „Programėlių CDS saitas“, esantis Dataverse aplinkos informacijos sekcijoje](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Negalite atsieti aplinkos naudodami LCS. Norėdami atsieti aplinką, aplinkoje Finance and Operations atidarykite darbo sritį **Duomenų integravimas** ir pasirinkite **Atsieti**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]