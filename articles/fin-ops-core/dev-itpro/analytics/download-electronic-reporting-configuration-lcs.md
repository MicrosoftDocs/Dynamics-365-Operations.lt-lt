---
title: Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“
description: Šioje temoje paaiškinama, kaip atsisiųsti elektroninių ataskaitų (ER) konfigūracijas iš „Microsoft Dynamics Lifecycle Services“ (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8aaa3be426c0321da7e72d6acc18918d8b0ecee2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570375"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip atsisiųsti naujausią [elektroninių ataskaitų (ER) konfigūracijų](general-electronic-reporting.md#Configuration) versiją iš [bendrai naudojamo turto bibliotekos](../lifecycle-services/asset-library.md), esančios „Microsoft Dynamics Lifecycle Services” (LCS).

1. Prisijunkite prie programos naudodami vieną iš tolesnių vaidmenų.

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

2. Eikite į **Organizacijos administravimas** &gt; **Darbo sritys** &gt; **Elektroninės ataskaitos**.
3. Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **Microsoft**.
4. Plytelėje **Microsoft** pasirinkite **Saugyklos**.

    [![Plytelė „Microsoft” puslapyje Lokalizavimo konfigūracijos](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Puslapio **Konfigūracijų saugyklos** tinklelyje pasirinkite esamą tipo **LCS** saugyklą. Jei ši saugykla tinklelyje nerodoma, atlikite tolesnius veiksmus.

    1. Pasirinkite **Įtraukti**, kad įtrauktumėte saugyklą.
    2. Pasirinkite **LCS** kaip saugyklos tipą.
    3. Pasirinkite **Kurti saugyklą**.
    4. Jei esate raginami pateikti autorizaciją, vykdykite ekrane pateikiamus nurodymus.
    5. Įveskite saugyklos pavadinimą ir aprašymą.
    6. Pasirinkite **Gerai**, kad patvirtintumėte naują saugyklos įrašą.
    7. Tinklelyje pasirinkite naują tipo **LCS** saugyklą.

6. Pasirinkite **Atidaryti**, norėdami peržiūrėti pasirinktos saugyklos ER konfigūracijų sąrašą.

    [![Konfigūracijų saugyklų puslapis](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Jei kyla problemų prisijungiant prie LCS saugyklos norint atsisiųsti konfigūracijas iš LCS bendrai naudojamo turto bibliotekos, galite atsisiųsti konfigūracijas iš [bendrosios saugyklos](er-download-configurations-global-repo.md).

7. Kairiojoje srityje esančiame konfigūracijų medyje pasirinkite reikiamą ER konfigūraciją.
8. „FastTab“ **Versijos** pasirinkite reikiamą pasirinktos ER konfigūracijos versiją.
9. Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš LCS į dabartinį egzempliorių.

    > [!NOTE]
    > Mygtuko **Importuoti** negalima naudoti ER konfigūracijų versijose, kurios jau yra dabartiniame egzemplioriuje.

    [![Konfigūracijos saugyklos puslapis](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Atsižvelgiant į ER parametrus, konfigūracijos patikrinamos po importavimo. Galite būti informuoti apie rastas nenuoseklumo problemas. Prieš naudodami importuotą konfigūracijos versiją, turite išspręsti šias problemas. Daugiau informacijos ieškokite šios temos susijusių temų sąraše.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]