---
title: Verslo dokumento šablono struktūros atnaujinimas
description: Šioje temoje paaiškinama, kaip atnaujinti verslo dokumento šablono struktūrą naudojantis funkcija Verslo dokumentų valdymas.
author: NickSelin
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: fd279b28c43e22bec6bf814845fe97828bc96d81
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681333"
---
# <a name="update-the-structure-of-a-business-document-template"></a>Verslo dokumento šablono struktūros atnaujinimas 

[!include[banner](../includes/banner.md)]

Funkcijos [Verslo dokumentų valdymas](er-business-document-management.md) šablonų rengyklės srityje **Šablono struktūra** galite modifikuoti verslo dokumento šabloną, [įtraukdami naujų laukų](er-bdm-add-field-to-excel-template.md) į „Microsoft Excel“ šabloną. Šablono struktūra tada automatiškai atnaujinama programoje „Dynamics 365 Finance“, kad atspindėtų keitimus, atliktus srityje **Šablono struktūra**.

Taip pat galite modifikuoti šabloną naudodami „Office 365“ internetinę funkciją. Pavyzdžiui, į redaguojamą darbalapį galite įtraukti naują pavadintą elementą, pvz., paveikslėlį ar figūrą. Šiuo atveju šablono struktūra nėra automatiškai atnaujinama programoje „Finance“, o jūsų įtrauktas elementas nerodomas srityje **Šablono struktūra**. Programoje „Finance“ šablono struktūrą atnaujinkite neautomatiniu būdu, pasirinkdami **Atnaujinti struktūrą** šablonų rengyklės puslapyje.

Norėdami gauti daugiau informacijos apie šią funkciją, atlikite toliau pateiktą pavyzdį.

## <a name="example-update-the-structure-of-a-business-document-template"></a>Pavyzdys: verslo dokumento šablono struktūros atnaujinimas

Šiame pavyzdyje rodoma, kaip sistemos administratorius gali atnaujinti verslo dokumento šablono struktūrą programoje „Finance“, kai šablonas modifikuojamas programoje „Office Online“. Tolesniuose skyriuose aprašomi susiję veiksmai.

### <a name="prepare-a-business-document-template-for-editing"></a>Verslo dokumento šablono paruošimas redaguoti

Atlikite tolesnes procedūras, nurodytas temoje [Funkcijos Verslo dokumentų valdymas apžvalga](er-business-document-management.md).

1. [ER parametrų konfigūravimas](er-business-document-management.md#configure-er-parameters)
2. [ER sprendimų importavimas](er-business-document-management.md#import-er-solutions)
3. [Verslo dokumentų valdymo įjungimas](er-business-document-management.md#enable-business-document-management)
4. [Parametrų konfigūravimas](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a>Verslo dokumento šablono redagavimas

1. Darbo srityje **Verslo dokumentų valdymas** pasirinkite **Naujas dokumentas**.
2. Puslapyje **Naujo šablono sukūrimas** pasirinkite šabloną **Laisvos formos sąskaita faktūra (ER pavyzdys) („Excel“)**.
3. Pasirinkite **Kurti dokumentą**.
4. Lauke **Pavadinimas** įveskite **FTI pavyzdys „Litware“**.
5. Pasirinkite **Gerai**, kad sukurtumėte naują šabloną.

    > [!NOTE]
    > Jei dar neprisijungėte prie „Office Online“, būsite [nukreipti į „Office 365“ prisijungimo puslapį](er-business-document-management.md#i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-microsoft-365-web-page). Norėdami grįžti į savo „Finance“ aplinką, naršyklėje pasirinkite mygtuką **Atgal**.

    Naujas šablonas atidaromas redaguoti „Excel Online“ įdėtajame valdiklyje, esančiame šablonų rengyklės puslapyje.

[![Funkcijos Verslo dokumentų valdymas darbo srities naudojimas norint pradėti redaguoti verslo dokumento šabloną](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)

### <a name="review-the-current-structure-of-the-editable-template"></a>Dabartinės redaguojamojo šablono struktūros peržiūra

1. „Excel Online“ juostelės skirtuko **Rodinys** grupėje **Rodyti** pasirinkite **Tinklelio eilutės**.
2. Redaguojamame šablone pasirinkite stačiakampį, esantį virš šablono pavadinimo. Šis stačiakampis yra paveikslėlis, pavadintas **rptHeaderCompLogo**.
3. Jei sritis **Šablono struktūra** paslėpta, pasirinkite **Rodyti struktūrą**.
4. Srityje **Šablono struktūra** išplėskite **Ataskaita \> Sąskaita faktūra \> rptHeader \> rptHeaderPart1**.
5. Atkreipkite dėmesį, kad „Finance“ šablono struktūroje elementas **rptHeaderCompLogo** pateikiamas kaip antrinis **Ataskaita \> Sąskaita faktūra \> rptHeader \> rptHeaderPart1** elementas.

[![Funkcijos Verslo dokumentų valdymas darbo srities naudojimas norint peržiūrėti dabartinę redaguojamojo šablono struktūrą](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a>Verslo dokumento šablono struktūros atnaujinimas panaikinant paveikslėlį

1. „Excel Online“ redaguojamame šablone pasirinkite paveikslėlį **rptHeaderCompLogo**.
2. Atlikite vieną iš tolesnių veiksmų, kad panaikintumėte pažymėtą paveikslėlį redaguojamame šablone,

    - Pasirinkite klaviatūros klavišą **Naikinti**.
    - Pasirinkite ir palaikykite (arba dešiniuoju pelės mygtuku spustelėkite) paveikslėlį ir pasirinkite **Iškirpti**.

    > [!NOTE]
    > Elementas **rptHeaderCompLogo** šiuo metu vis dar yra „Finance“ šablono struktūroje, net jei paveikslėlis nebėra įtrauktas į „Excel“ šabloną.

3. Pasirinkite **Atnaujinti struktūrą**, kad sinchronizuotumėte redaguojamojo šablono struktūrą programose „Excel“ ir „Finance“.
4. Srityje **Šablono struktūra** išplėskite **Ataskaita \> Sąskaita faktūra \> rptHeader \> rptHeaderPart1**.
5. Atkreipkite dėmesį, kad elementas **rptHeaderCompLogo** nebėra įtrauktas į „Finance“ šablono struktūrą.

[![Funkcijos Verslo dokumentų valdymas darbo srities naudojimas norint panaikinti paveikslėlį verslo dokumento šablone](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a>Verslo dokumento šablono struktūros atnaujinimas įtraukiant paveikslėlį

1. „Excel Online“ juostelės skirtuko **Įterpti** grupėje **Iliustracijos** pasirinkite **Paveikslėlis**.
2. Pasirinkite **Pasirinkti failą**, naršydami pasirinkite vaizdą, kurį norite įtraukti, ir pasirinkite **Gerai**.
3. Pasirinkite **Įterpti**.
4. Perkelkite naują paveikslėlį į tinkamą vietą. Numatyta, kad „Excel“ paveikslėlį pavadina. Pavyzdžiui, ji gali paveikslėlį pavadinti **2 paveikslėlis**.
5. Pasirinkite **Atnaujinti struktūrą**, kad sinchronizuotumėte redaguojamojo šablono struktūrą programose „Excel“ ir „Finance“.
6. Srityje **Šablono struktūra** išplėskite **Ataskaita \> Sąskaita faktūra \> rptHeader \> rptHeaderPart1**.
7. Atkreipkite dėmesį, kad naujas paveikslėlis dabar kaip elementas įtrauktas į „Finance“ šablono struktūrą.

[![Funkcijos Verslo dokumentų valdymas darbo srities naudojimas norint įtraukti paveikslėlį į verslo dokumento šabloną](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)

## <a name="related-links"></a>Susiję saitai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[Verslo dokumentų valdymo apžvalga](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]