---
title: Atnaujintų ER konfigūracijų versijų naujinimas
description: Šiame straipsnyje paaiškinama, kaip importuoti atnaujintas elektroninių ataskaitų (ER) konfigūracijų versijas iš konfigūracijos tarnybos visuotinės saugyklos.
author: kfend
ms.date: 06/09/2020
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
ms.openlocfilehash: 0eef9c9a112fd58a43f6c3a85163ccf44bea3d61
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292653"
---
# <a name="import-updated-versions-of-er-configurations"></a>Atnaujintų ER konfigūracijų versijų naujinimas

[!include [banner](../includes/banner.md)]

Elektroninių ataskaitų (ER) [saugyklos ](general-electronic-reporting.md#Repository) naudojamos norint bendrinti [ER konfigūracijas](general-electronic-reporting.md#Configuration). Galite importuoti [ER](download-electronic-reporting-configuration-lcs.md) konfigūracijas iš skirtingų saugyklų į savo Microsoft Dynamics 365 finansų egzempliorių. Importuojant ER konfigūracijas, konfigūracijos teikėjai [gali](general-electronic-reporting.md#Provider) publikuoti naujas versijų saugyklas, kad galėtų būti bendrai naudojamos.

Šiame straipsnyje paaiškinama, kaip importuoti atnaujintas ER konfigūracijų versijas iš konfigūracijos tarnybos visuotinės saugyklos. Daugiau informacijos rasite [Microsoft Dynamics 365 Finansų – reguliavimo tarnybos, Konfigūracijos tarnyba](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration).

## <a name="review-the-available-updated-versions"></a>Galimų atnaujintų versijų peržiūra

1. Prisijunkite prie „Finance“ naudodami vieną iš tolesnių vaidmenų:

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Importuoti konfigūracijų versijų naujinimus**.

    ![Lokalizavimo konfigūravimo puslapis.](./media/er-download-updated-versions-global-repo1.png)

4. Dialogo lange **Importuoti elektroninių ataskaitų konfigūracijos versijų naujinimus** **Leidimo režimas** pasirinkite **Rodyti tik galimus naujinimus**. Tada pasirinkite **Gerai**. 

    ![Vykdymo režimo laukas nustatytas į „Rodyti tik galimus naujinimus”.](./media/er-download-updated-versions-global-repo2.png)

5. Peržiūrėti gaunamus pranešimus. Šiuose pranešimuose pateikiama toliau nurodyta informacija apie ER konfigūracijas dabartinėje „Finance” programoje ir kuo jos panašios į bendros saugyklos turinį:

    - Bendras ER konfigūracijų skaičius
    - ER konfigūracijos, kurių nėra bendroje saugykloje
    - ER konfigūracijos, kurių naujausia versija jau prieinama dabartinėje „Finance” programoje (Norėdami peržiūrėti išsamų ER konfigūracijų sąrašą, pasirinkite **Pranešimų išsami informacija** .)

        ![„Naujausios šių konfigūracijų versijos jau importuotos” pranešimas ir pranešimų išsami informacija](./media/er-download-updated-versions-global-repo3.png)

    - ER konfigūracijos, kurių naujausia versija jau prieinama Bendroje saugykloje, kuri gali būti importuota dabartinėje „Finance” programoje (Norėdami peržiūrėti išsamų ER konfigūracijų sąrašą, pasirinkite **Pranešimų išsami informacija** saitą.)

        ![„Galimi naujinimai” pranešimas ir pranešimų išsami informacija](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>Importuokite galimas atnaujintas versijas

1. Prisijunkite prie „Finance“ naudodami vieną iš tolesnių vaidmenų:

    - Elektroninės ataskaitos kūrėjas
    - Elektroninės ataskaitos funkcijų konsultantas
    - Sistemos administratorius

2. Eikite į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos**.
3. **Lokalizavimo konfigūracijos** puslapyje **Susiję saitai** skyriuje pasirinkite **Importuoti konfigūracijų versijų naujinimus**.
4. Dialogo lange **Importuoti elektroninių ataskaitų konfigūracijos versijų naujinimus** **Vykdymo režimas** pasirinkite **Importuoti naujausius naujinimus**, kad būtų importuotos naujausios ER konfigūracijos iš Bendrosios saugyklos į dabartinę „Finance” programą.
5. Norėdami suplanuoti, kad būtų importuojama paketinė užduotis, **Paleisti fone** „FastTab” skirtuke nustatykite **Paketo apdorojimas** pasirinktį į **Taip**. Jei norite periodiškai kartoti importavimą, konfigūruokite reikiamą pasikartojimą.

    ![Vykdymo režimo laukas nustatytas į „Importuoti naujausius naujinimus”.](./media/er-download-updated-versions-global-repo5.png)

6. Pasirinkite **Gerai**.
7. Norėdami sužinoti, kokios konfigūracijų versijos importuotos, atlikite vieną iš šių veiksmų:

    - Jei importuosite interaktyviai, o ne naudodami paketinę užduotį, peržiūrėkite gaunamų pranešimų informaciją.

        ![Pranešimai, gaunami interaktyviojo importavimo vykdymo metu.](./media/er-download-updated-versions-global-repo6.png)

    - Jei paleidote importavimą paketo režimu, atlikite šiuos veiksmus:

        1. Eikite į **Bendra** \> **Užklausos** \> **Paketinės užduotys** \> **Mano paketinės užduotys**.
        2. Ieškokite ir pasirinkite **Importuoti elektroninės ataskaitos konfigūracijų versijos naujinimus** užduotį, o tada Veiksmų srityje **Paketinė užduotis** skirtuke pasirinkite **Paketinės užduoties istorija**, kad peržiūrėtumėte užduoties istoriją.
        3. **Paketinės užduoties istorija** puslapyje pasirinkite **Žurnalas**. Tada gautame pranešime pasirinkite **Pranešimų išsami informacija** saitą, kad peržiūrėtumėte užduoties žurnalą.

        ![Užduoties žurnalas.](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Nerekomenduojame, kad suplanuotumėte pasikartojančią paketinę užduotį, kad importuotumėte atnaujintas ER konfigūracijos versijas tiesiogiai iš Bendrosios saugyklos į gamybos aplinką, nes importuotas versijas bus galima iš karto naudoti. Užuot tai naudoję, naudokite šį metodą diegti ER konfigūracijų versijas į smėlio dėžės aplinką. Tada jos gali būti vertinamos smėlio dėžės aplinkoje prieš jas įdiegiant gamybos aplinkoje.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)
- [ER konfigūracijų atsisiuntimas iš konfigūravimo tarnybos bendrosios saugyklos](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
