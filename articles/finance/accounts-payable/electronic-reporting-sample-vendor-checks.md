---
title: Elektroninės ataskaitos tiekėjo čekių pavyzdžiai
description: Šiame straipsnyje pateikiama bendroji informacija apie tai, kaip naudoti elektroninių ataskaitų pavyzdžio čekių formatus.
author: mrolecki
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6863acaa264cfb8f15c34e85811a94afc67bec5e
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715217"
---
# <a name="electronic-reporting-sample-vendor-checks"></a>Elektroninės ataskaitos tiekėjo čekių pavyzdžiai

[!include [banner](../includes/banner.md)]

Norėdami formatuoti tiekėjo čekius, galite naudoti elektronines ataskaitas (ER). Rinkoje siūloma daug bankui skirtų ir čekio tiekėjui skirtų čekio formatų. Čekių formatų pavyzdžiai įtraukti į elektroninių ataskaitų rengimo įrankio saugyklos mokėjimo čekio modelį. Šie čekių pavyzdžiai pažymėti **Tikrinti viduryje (JAV)** ir **Tikrinti žemiau pateiktoje viršutinėje šaknelėje (JAV)**.

## <a name="what-check-formats-are-currently-supported"></a>Kokie čekio formatai šiuo metu palaikomi?

Visada turite eiti į bendrai naudojamo turto biblioteką „Microsoft Dynamics Lifecycle Services“ (LCS) ir peržiūrėti dabartinį prieinamų failų, kurių turto tipas yra **GER konfigūracija**, sąrašą. Kitame skyriuje "Ką reikia nustatyti?" yra saitas į straipsnį, kuriame paaiškinama, kaip sukurti LCS saugyklą, kad būtų galima peržiūrėti galimas konfigūracijas ir importuoti pasirinktas konfigūracijas.

Microsoft Dynamics 365 Finansai apima pavyzdinį formatą, kuriame ant viršaus yra čekis, ir du pavedimo skyriai. Taip pat pateikiamas formato, kai čekis yra viduryje, tarp dviejų pavedimo dalių, pavyzdys. Šių formatų pavyzdžiai atitinka „Deluxe“ verslo čekių formatus.

## <a name="what-do-i-have-to-set-up"></a>Ką turiu nustatyti?

- Prieš spausdinant čekius naudojant ER (elektronines ataskaitas) į ER (elektroninių ataskaitų) konfigūracijas būtina importuoti bent vieną aktyvią čekio konfigūraciją. Instrukcijų ieškokite [Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
- Kai konfigūruojate banko sąskaitos grynųjų pinigų ir banko valdymo čekius, pažymėkite žymės langelį **Bendrasis eksporto elektroniniu būdu formatas**, o po to pasirinkite atitinkamą čekio formatą kaip eksportavimo formato konfigūraciją.
- Taip pat turite nurodyti pavedime spausdinamų važtaraščio eilučių skaičių. Skaičiuodami šį skaičių būtinai įtraukite antraštės eilutes. Rekomenduojamas šių dviejų čekio formatų pavyzdžių kvito eilučių skaičius yra 17. Tačiau, atsižvelgiant į jūsų čekius ir jūsų spausdintuvo tvarkykles, šis skaičius skirsis.
- Mes rekomenduojame atsispausdinti bandomąjį čekį ir patikrinti čekio maketą. Norėdami atsispausdinti bandomąjį čekį, pažymėkite parinktį **Bandomasis spausdinimas**. Čekio formatų pavyzdžius geriausiai naudoti tada, kai nustatyta išplėstinių „Microsoft Excel“ spausdintuvo ypatybių dalies **Paraštės** parinktis **Nėra**. Sugeneravę bandomąjį čekį įjunkite „Excel“ išvesties redagavimą ir sukonfigūruokite puslapio išdėstymą taip, kad būtų nustatyta visų paraščių parinktis **0** (nulis). Palyginkite bandomąją čekių kopiją su jūsų turimais čekiais ir koreguokite parametrus tol, kol nustatysite norimą lygiuotę.
- Kai mokėjimo žurnale generuojate sukonfigūruotos banko sąskaitos mokėjimus, čekiai bus spausdinami naudojant nurodytą formatą.

Daugiau informacijos rasite [Elektroninių ataskaitų formato modifikavimas](../../fin-ops-core/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
