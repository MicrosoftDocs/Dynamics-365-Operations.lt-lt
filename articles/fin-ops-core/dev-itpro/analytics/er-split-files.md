---
title: Sugeneruotų XML failų skaidymas pagal failo dydį ir turinio kiekį
description: Šiame straipsnyje pateikiama informacija apie tai, kaip skaidyti sugeneruotus failus pagal failo dydį ir turinio elementų kiekį.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 5347d4e85198893dd94f14508176db93ccd47c22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280102"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>Sugeneruotų XML failų skaidymas pagal failo dydį ir turinio kiekį

[!include[banner](../includes/banner.md)]

Galite sukurti elektroninių ataskaitų (ER) formatus, skirtus generuoti siunčiamus dokumentus XLS formatu. Kartais šie dokumentai gali būti priimti tik tada, kai atitinka konkrečius kriterijus, pvz., maksimalus failo dydis arba didžiausias kai kurių XML mazgų skaičius. Galite kurti ER formatus, skirtus generuoti elektroninius dokumentus, kurie atitiktų šių dokumentų gavėjų nurodytus reikalavimus.

- FAILO formato elementui, galite nustatyti failo dydžio ribą kaip ER išraišką. Viršijus nustatytą ribą generuojant ER ataskaitą, ER baigia kurti dabartinį failą ir tada pereina į kito failo kūrimą.
- Bet kuriam formatui XML ELEMENTAS galite nustatyti elementų skaičiaus ribą kaip ER išraišką. Sugeneruotame faile viršijus nustatytą XML mazgų ribą vykdant ER ataskaitą, ER baigia kurti dabartinį failą ir tada pereina į kito failo kūrimą.
- Bet kuriam formato XML SEKA elementui galite nustatyti antrinių elementų skaičiaus ribą kaip ER išraišką. Sugeneruotame faile viršijus nustatytą formato elemento įdėtųjų XML mazgų ribą vykdant ER ataskaitą, ER baigia kurti dabartinį failą ir tada pereina į kito failo kūrimą.
- Galite pažymėti bet kurį XML ELEMENTAS formato elementą kaip neperkeliamąjį. Tokiu būdu galite išlaikyti įdėtuosius XML mazgų elementus, sugeneruotus pagal formato elementą, viename sugeneruotame faile.

Be to, be formato elementų XML ELEMENTAS ir XML SEKA, XML mazgams įtraukti į sugeneruotą failą galite naudoti formato elementą NEAPDOROTAS XML. Tačiau mazgų, kuriuos įtrauksite naudodami formato elementą NEAPDOROTAS XML, nėra paisoma skaičiuojant mazgus, siekiant įvertinti elementų skaičiaus ribas.

Jei sukonfigūravote formato elemento FAILAS failų paskirties vietas, kuris sukonfigūruotas skaidyti sugeneruotą išvestį, kai viršijamos konkrečios ribos, kiekviena sugeneruotos išvesties dalis siunčiama į sukonfigūruotą failo paskirties vietą kaip atskiras failas. Norėdami unikaliai pavadinti failus, kurie sukuriami suskaidžius išvestį, turite sukonfigūruoti formato elemento FAILAS ER išraišką. Jei norite įtraukti NUMERACIJA tipo ER duomenų šaltinį, numeracija bus didinama su kiekviena suskaidytos išvesties dalimi.

Norėdami daugiau sužinoti apie šią funkciją, leiskite užduočių vedlį **ER XML failai, suskaidyti atsižvelgiant į failo dydį arba turinio elementų kiekį**, kuris yra **7.5.4.3 Įsigyti / sukurti IT paslaugų ir sprendimų komponentų (10677)** verslo proceso dalis ir gali būti atsisiųstas iš [„Microsoft“ atsisiuntimo centras](https://go.microsoft.com/fwlink/?linkid=874684). Šis užduočių vedlys padės ER formato konfigūravimo proceso metu, norint skaidyti sugeneruotus failus atsižvelgiant į failo dydžio ir turinio elementų kiekio ribas. Norėdami užbaigti užduočių vedlį, turite atsisiųsti šiuos failus:

- [ER modelio konfigūracija – XmlFilesSplittingModel.xml](https://download.microsoft.com/download/e/a/f/eaffe96a-22ec-4a32-898a-f4328c91c387/XmlFilesSplittingModel.xml)
- [ER formato konfigūracija – XmlFilesSplittingFormat.xml](https://download.microsoft.com/download/e/9/c/e9c5849b-8254-4cdf-bb00-4c2ebc72ddec/XmlFilesSplittingFormat.xml)

## <a name="additional-resources"></a>Papildomi ištekliai
[Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)

[Elektroninių ataskaitų (ER) formulių kūrimo įrankis](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
