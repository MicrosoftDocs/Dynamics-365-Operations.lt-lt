---
title: FORMAT ER funkcija
description: Šioje temoje pateikiama informacija apie tai, kaip naudojama FORMAT elektroninių ataskaitų (ER) funkcija.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ae688ef6b24f8d90c0354c8c6449adba1588bfa
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041083"
---
# <a name="FORMAT">FORMAT ER funkcija</a>

[!include [banner](../includes/banner.md)]

`FORMAT` funkcija grąžina nurodytą eilutę kaip *Eilutės* reikšmę, suformatuotą pakeičiant visus **%N** pasikartojimus *N*-uoju argumentu.

## <a name="syntax"></a>Sintaksė

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Argumentai

`string`: *Eilutė*

Nuoroda į duomenų šaltinį, kuris yra formatuotinas *Eilutės* tipas. Šis argumentas yra būtinas.

`argument 1`: *Eilutė*

Pirmasis argumentas, kuris yra naudojamas pakeisti **%1** pasikartojimus. Šis argumentas yra būtinas.

`argument N`: *Eilutė*

*N*-tasis argumentas, kuris yra naudojamas pakeisti **%2**, **%3** ir kitus pasikartojimus. Šie papildomi argumentai yra pasirinktiniai.

## <a name="return-values"></a>Grįžties vertės

*Eilutė*

Gaunama tekstinė reikšmė.

## <a name="usage-notes"></a>Naudojimo pastabos

Jei nėra pateiktas parametro argumentas, parametras eilutėje pateikiamas kaip **„%N“**. *Realiojo skaičiaus* tipo reikšmių numatytosios eilutės konvertavimas apribotas dviem skaičiais po kablelio.

## <a name="example"></a>Pavyzdys

Tolesnėje iliustracijoje duomenų šaltinis **PaymentModel** grąžina klientų įrašų sąrašą naudodamas **kliento** komponentą. Jis grąžina apdorojimo datos reikšmę naudojant lauką **ProcessingDate**.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

Elektroninių ataskaitų (ER) formate, skirtame generuoti elektroninį failą pasirinktiems klientams, **PaymentModel** yra pasirinktas kaip duomenų šaltinis ir jis kontroliuoja proceso eigą. Pateikiama išimtis, informuojanti vartotoją, jei pasirinktas klientas sustabdomas ataskaitos apdorojimo dieną. Formulė, sukurta šio tipo apdorojimo kontrolei, gali naudoti tokius išteklius:

- Žymė SYS70894, kur nurodytas toks tekstas:

    - **LT kalba:** „Nėra ką spausdinti“
    - **DE kalba:** „Nichts zu drucken“

- Žymė SYS18389, kur nurodytas toks tekstas:

    - **EN-US kalba:** „Customer %1 is stopped for %2.“
    - **DE kalba:** „Debitor '%1' wird für %2 gesperrt.“

Tai yra išraiška, kurią galima sukurti.

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Jei 2015 m. gruodžio 17 d. apdorojama kliento **Litware Retail** kultūros **EN-US** ir kalbos **EN-US** ataskaita, ši formulė pateikia tokį tekstą, kuris vartotojui gali būti pateiktas kaip tolesnis išimties pranešimas.

*Nėra spausdinių. „Customer Litware Retail“ sustabdytas 2015-12-17.*

Jei ta pati ataskaita apdorojama **„Litware Retail“** klientui 2015 m. gruodžio 17 d. pagal **DE** kultūrą ir **DE** kalbą, ši formulė pateikia tokį tekstą, kuris naudoja toliau nurodytą kitokį datos formatą.

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> ER formulėse žymoms taikoma tokia sintaksė:
>
> - **„Microsoft Dynamics 365 Finance“ programos išteklių žymėms:** **\@X**, kai **X** yra žymės ID programos objektų medyje (AOT)
> - **ER konfigūracijose esančioms žymėms:** **@"GER_LABEL:X"**, kai **X** yra žymės ID ER konfigūracijoje

## <a name="additional-resources"></a>Papildomi ištekliai

[Tekstinės funkcijos](er-functions-category-text.md)
