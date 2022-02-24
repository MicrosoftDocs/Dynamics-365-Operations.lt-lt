---
title: ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos
description: Šioje temoje paaiškinama, kaip atsisiųsti elektroninių ataskaitų (ER) konfigūracijas iš konfigūravimo tarnybos bendrosios saugyklos.
author: NickSelin
manager: AnnBe
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a96e78a64fe0559ae5f3bfddabf3fe1cad8a3dcb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679563"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip atsisiųsti [elektroninių ataskaitų (ER) konfigūracijas](general-electronic-reporting.md#Configuration) iš konfigūravimo tarnybos bendrosios saugyklos. Norėdami gauti daugiau informacijos, žr. [„Microsoft Dynamics 365 for Finance and Operations“ – „Regulatory Services“, konfigūravimo tarnybą](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>Atidarykite konfigūracijų saugyklą

1. Prisijunkite prie „Dynamics 365 Finance“ programos naudodami vieną iš tolesnių vaidmenų.

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

2. Pasirinkite **Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos**.
3. Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **Microsoft**.
3. Plytelėje **Microsoft** pasirinkite **Saugyklos**.

    ![Elektroninių ataskaitų darbo sritis](./media/er-download-configurations-global-repo-er-workspace.png)

4. Puslapio **Konfigūracijų saugyklos** tinklelyje pasirinkite esamą saugyklą, kurios tipas **Bendroji**. Jei ši saugykla tinklelyje nerodoma, atlikite tolesnius veiksmus.

    1. Pasirinkite **Įtraukti**, kad įtrauktumėte naują saugyklą.
    2. Pasirinkite saugyklos tipą **Bendroji** ir pasirinkite **Kurti saugyklą**.
    3. Paraginti vykdykite autorizavimo instrukcijas.
    4. Įveskite saugyklos pavadinimą bei aprašą ir pasirinkite **Gerai**, kad patvirtintumėte naują saugyklos įrašą.
    5. Tinklelyje pasirinkite naują tipo **Bendroji** saugyklą.

5. Pasirinkite **Atidaryti**, norėdami peržiūrėti pasirinktos saugyklos ER konfigūracijų sąrašą.

    ![Konfigūracijų saugyklų puslapis](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Vienos konfigūracijos importavimas

1. Puslapyje **Konfigūracijų saugyklos**, esančiame konfigūracijos medyje, pasirinkite norimą ER konfigūraciją.
2. „FastTab“ **Versijos** pasirinkite reikiamą pasirinktos ER konfigūracijos versiją.
3. Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš bendrosios saugyklos į dabartinį „Finance“ egzempliorių.

    > [!NOTE]
    > Mygtuko **Importuoti** negalima naudoti ER konfigūracijų versijose, kurios jau yra dabartiniame „Finance“ egzemplioriuje.

    ![Konfigūracijos saugyklos puslapis](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Filtruotų konfigūracijų importavimas

1. Puslapyje **Konfigūracijų saugykla**, esančiame konfigūracijos medyje, išplėskite „FastTab“ **Filtras**.
2. Tinklelyje **Žymos** pridėkite visas reikiamas žymas.
3. Lauke **Šalies / regiono taikomumas** pasirinkite reikiamus šalies / regiono kodus ir pasirinkite **Taikyti filtrą**.

    > [!NOTE]
    > „FastTab“ **Konfigūracijos** rodomos visos konfigūracijos, kurios atitinka nurodytas pasirinkimo sąlygas.

4. „FastTab“ **Konfigūracijos** pasirinkite **Importuoti**, kad atsisiųstumėte filtruotas konfigūracijas iš bendrosios saugyklos į dabartinį egzempliorių.
5. „FastTab“ **Konfigūracijos** pasirinkite **Iš naujo nustatyti filtrą**, kad būtų išvalytos nurodytos pasirinkimo sąlygos.

    ![Konfigūracijos saugyklos puslapis](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> Atsižvelgiant į ER parametrus, konfigūracijos patikrinamos po importavimo. Galite būti informuoti apie rastas nenuoseklumo problemas. Prieš naudodami importuotą konfigūracijos versiją, turite išspręsti problemas. Daugiau informacijos ieškokite su šia tema susijusių išteklių sąraše.

> [!NOTE]
> ER konfigūracijos gali būti sukonfigūruotos kaip priklausomos nuo kitų konfigūracijų. Todėl kartu su pasirinkta konfigūracija gali būti importuotos ir kitos konfigūracijos. Norėdami gauti daugiau informacijos apie konfigūracijos priklausomybes, žr. [ER konfigūracijų priklausomybės nuo kitų komponentų apibrėžimas](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)
