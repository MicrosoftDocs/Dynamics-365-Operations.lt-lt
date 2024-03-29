---
title: ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos
description: Šiame straipsnyje paaiškinama, kaip atsisiųsti elektroninių ataskaitų (ER) konfigūracijas iš visuotinės konfigūracijos tarnybos saugyklos.
author: kfend
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
ms.openlocfilehash: 3bbc341d1668e54fcb4034263a7e142166a94b05
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273315"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip atsisiųsti elektroninių [ataskaitų (ER) konfigūracijas](general-electronic-reporting.md#Configuration) iš visuotinės konfigūracijos tarnybos saugyklos. Daugiau informacijos rasite [Microsoft Dynamics 365 Finansų – reguliavimo tarnybos, Konfigūracijos tarnyba](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="open-configurations-repository"></a>Atidarykite konfigūracijų saugyklą

1. Prisiregistruokite prie "Dynamics 365" finansinės programos, naudodami vieną iš šių vaidmenų:

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

2. Pasirinkite **Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos**.
3. Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **Microsoft**.
3. Plytelėje **Microsoft** pasirinkite **Saugyklos**.

    ![Elektroninių ataskaitų darbo sritis.](./media/er-download-configurations-global-repo-er-workspace.png)

4. Puslapio **Konfigūracijų saugyklos** tinklelyje pasirinkite esamą saugyklą, kurios tipas **Bendroji**. Jei ši saugykla tinklelyje nerodoma, atlikite tolesnius veiksmus.

    1. Pasirinkite **Įtraukti**, kad įtrauktumėte naują saugyklą.
    2. Pasirinkite saugyklos tipą **Bendroji** ir pasirinkite **Kurti saugyklą**.
    3. Paraginti vykdykite autorizavimo instrukcijas.
    4. Įveskite saugyklos pavadinimą bei aprašą ir pasirinkite **Gerai**, kad patvirtintumėte naują saugyklos įrašą.
    5. Tinklelyje pasirinkite naują tipo **Bendroji** saugyklą.

5. Pasirinkite **Atidaryti**, norėdami peržiūrėti pasirinktos saugyklos ER konfigūracijų sąrašą.

    ![Konfigūracijų saugyklų puslapis.](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Vienos konfigūracijos importavimas

1. Puslapyje **Konfigūracijų saugyklos**, esančiame konfigūracijos medyje, pasirinkite norimą ER konfigūraciją.
2. „FastTab“ **Versijos** pasirinkite reikiamą pasirinktos ER konfigūracijos versiją.
3. Pasirinkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš bendrosios saugyklos į dabartinį „Finance“ egzempliorių.

    > [!NOTE]
    > Mygtuko **Importuoti** negalima naudoti ER konfigūracijų versijose, kurios jau yra dabartiniame „Finance“ egzemplioriuje.

    ![Konfigūracijos saugyklos puslapis, Konfigūracijos "FastTab".](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Filtruotų konfigūracijų importavimas

1. Puslapyje **Konfigūracijų saugykla**, esančiame konfigūracijos medyje, išplėskite „FastTab“ **Filtras**.
2. Tinklelyje **Žymos** pridėkite visas reikiamas žymas.
3. Lauke **Šalies / regiono taikomumas** pasirinkite reikiamus šalies / regiono kodus ir pasirinkite **Taikyti filtrą**.

    > [!NOTE]
    > „FastTab“ **Konfigūracijos** rodomos visos konfigūracijos, kurios atitinka nurodytas pasirinkimo sąlygas.

4. „FastTab“ **Konfigūracijos** pasirinkite **Importuoti**, kad atsisiųstumėte filtruotas konfigūracijas iš bendrosios saugyklos į dabartinį egzempliorių.
5. „FastTab“ **Konfigūracijos** pasirinkite **Iš naujo nustatyti filtrą**, kad būtų išvalytos nurodytos pasirinkimo sąlygos.

    ![Konfigūracijos saugyklos puslapis, Versijos "FastTab", Importavimo mygtukas.](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> Atsižvelgiant į ER parametrus, konfigūracijos patikrinamos po importavimo. Galite būti informuoti apie rastas nenuoseklumo problemas. Prieš naudodami importuotą konfigūracijos versiją, turite išspręsti problemas. Norėdami gauti daugiau informacijos, peržiūrėkite šio straipsnio susijusių išteklių sąrašą.

> [!NOTE]
> ER konfigūracijos gali būti sukonfigūruotos kaip priklausomos nuo kitų konfigūracijų. Todėl kartu su pasirinkta konfigūracija gali būti importuotos ir kitos konfigūracijos. Norėdami gauti daugiau informacijos apie konfigūracijos priklausomybes, žr. [ER konfigūracijų priklausomybės nuo kitų komponentų apibrėžimas](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

