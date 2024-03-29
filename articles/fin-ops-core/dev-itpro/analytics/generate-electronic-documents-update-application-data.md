---
title: Elektroninių dokumentų generavimas ir prašymų duomenų naujinimas naudojant ER
description: Galite kurti elektroninių ataskaitų (ER) formatus, kuriuos galima naudoti programoje norint generuoti siunčiamus elektroninius dokumentus.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 1be618d16be2ce9e50c2a43864040dfd23a8ff69
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269668"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Elektroninių dokumentų generavimas ir prašymų duomenų naujinimas naudojant ER

[!include [banner](../includes/banner.md)]

Galite kurti elektroninių ataskaitų (ER) formatus, kuriuos galima naudoti programoje norint generuoti siunčiamus elektroninius dokumentus. Taip pat galite kurti ER formatus, kurie analizuoja gaunamus elektroninius dokumentus ir naudoja šių dokumentų turinį programos duomenims atnaujinti.

Naudojant šią funkciją, vieną ER formatą galima naudoti siunčiamiems elektroniniams dokumentams generuoti ir tada programos duomenims atnaujinti. Šią funkciją galima naudoti esant toliau nurodytiems scenarijams.

- Norėdami išvengti pakartotinio programos naudojimo paskesniuose procesuose, programos duomenis galite pažymėti iš karto po to, kai jie panaudojami elektroniniams dokumentams generuoti. Pavyzdžiui, mokėjimo operacijas galite pažymėti kaip jau apdorotas iš karto po to, kai jos buvo įtrauktos į sugeneruotą mokėjimo pranešimą.
- Saugoti elektroninių dokumentų, kurie buvo sugeneruoti naudojant ER logiką, apdorojimo informaciją. Pavyzdžiui, unikalią mokėjimo pranešimo identifikaciją, sukurtą naudojant ER išraišką. Išraiška grindžiama informacija, kuri įvesta į ER dialogo langą paleidus ER formatą dokumentams generuoti.

Norėdami sužinoti daugiau apie šią funkciją, paleiskite užduočių vedlių rinkinį ER: dokumentų su programos duomenų atnaujinimu generavimas (Verslo proceso 7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677) dalis), kuriame pateikta informacija apie Intrastat ataskaitų teikimą ir archyvavimą. Šiuose užduočių vedliuose nurodyti failai turi atlikti tam tikrus veiksmus. Atsisiųskite ir įrašykite šiuos failus į savo vietinį kompiuterį.

- [ER duomenų modelio konfigūracija: Intrastat (modelis)](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [ER modelio susiejimo konfigūracija: Intrastat (susiejimas)](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [ER formato konfigūracija: Intrastat (formatas)](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
