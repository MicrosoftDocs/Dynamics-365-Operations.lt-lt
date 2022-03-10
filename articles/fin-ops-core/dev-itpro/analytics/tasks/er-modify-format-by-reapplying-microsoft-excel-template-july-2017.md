---
title: Formatų modifikavimas iš naujo pritaikant „Excel‟ šablonus
description: Norėdami užbaigti veiksmus šioje procedūroje, pirmiausia turite užbaigti procedūrą „ER – kurkite konfigūraciją ataskaitoms generuoti OPENXML formatu“.
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e66a2e24d3b1e77d5c790d2f3b7cfdce98fc4cca6e3734ad8b87ac7714192853
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749661"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a>Formatų modifikavimas iš naujo pritaikant „Excel‟ šablonus

[!include [banner](../../includes/banner.md)]

Norėdami užbaigti veiksmus šioje procedūroje, pirmiausia turite užbaigti procedūrą „ER – kurkite konfigūraciją ataskaitoms generuoti OPENXML formatu“.

Šia procedūra paaiškinama, kaip keisti elektroninių ataskaitų teikimo (ER) formato konfigūraciją, iš naujo taikant „Microsoft Excel“ šabloną, kuris buvo pakeistas. Šios procedūros metu importuosite modifikuotą „Excel“ šabloną į ER formato konfigūracijas, sukurtas pavyzdinei įmonei „Litware, Inc.“, ir tada generuokite elektroninius dokumentus. Ši procedūra skirta vartotojams, kuriems priskirtas sistemos administratoriaus arba elektroninių ataskaitų teikimo programuotojo vaidmuo. Šiuos veiksmus galima atlikti naudojant GBSI duomenų rinkinį. Prieš pradėdami atsisiųskite ir įrašykite failą SampleVendPaymWsReport2.xlsx, kuris nurodytas žinyno temoje „Elektroninių ataskaitų formato modifikavimas iš naujo pritaikant „Excel“ šabloną“ (modify-electronic-reporting-format-reapply-excel-template/).

1. Pasirinkite Organizacijos administravimas > Darbo sritys > Elektroninės ataskaitos.
    * Įsitikinkite, kad pavyzdinės įmonės „Litware, Inc.” konfigūracijos teikėjas yra prieinamas ir pažymėtas kaip aktyvus. Jei nematote šio konfigūracijos teikėjo, atlikite procedūros Kurkite konfigūracijos teikėją ir pažymėkite kaip aktyvų veiksmus.  

## <a name="select-the-er-format"></a>Pasirinkite ER formatą
1. Spustelėkite Ataskaitų konfigūracijos.
2. Medyje išplėskite „Mokėjimo modelis‟.
3. Medyje pasirinkite Mokėjimo modelis\Darbalapio ataskaitos pavyzdys.
4. Spustelėkite Priedai.
    * Atkreipkite dėmesį, kad SampleVendPaymWsReport.xlsx „Excel“ failas šiuo metu naudojamas kaip šablonas mokėjimo žurnalo apdorojimui.   
5. Spustelėkite Atidaryti.
    * Spustelėkite Atidaryti, kad ištirtumėte „Excel“ šablono išdėstymą.  
    * Peržiūrėkite šabloną. Žinokite, kad į ją dabar įeina šie kiekvienos mokėjimo eilutės duomenys: tiekėjo sąskaitos numeris, tiekėjo pavadinimas, bankas, kodas, sąskaitos numeris, debetas, kreditas ir valiuta. Šiam pavyzdžiui mes norime pratęsti šį sąrašą, pridėdami informacijos apie mokėjimo datą.   
6. Uždarykite puslapį.

## <a name="reapply-a-new-excel-template-to-er-format"></a>Iš naujo taikykite naują „Excel“ šabloną į ER formatui
1. Spustelėkite Konstruktorius.
    * Atidarykite pasirinkto ER formato juodraščio versiją redagavimui.  
2. Veiksmų srityje spustelėkite Importuoti.
3. Spustelėkite Naujinti iš „Excel‟.
    * Spustelėkite „Naujinti šabloną“ ir pasirinkite failą SampleVendPaymWsReport2.xlsx.  
    * Spustelėkite Atnaujinti šabloną ir naršykite, kad gautumėte anksčiau atsisiųstą SampleVendPaymWsReport2.xlsx failą.  
4. Spustelėkite GERAI.
    * Pritaikytas SampleVendPaymWsReport2.xlsx šablonas. ER formato struktūra sinchronizuojama su šablono, kurio elementai pridėti prie ER formato, turiniu. Bet kokie ER formate esantys elementai, kurie neįtraukti į šabloną, pašalinami iš formato apibrėžties.  
5. Medyje pasirinkite „Excel“.
    * Atkreipkite dėmesį, kad šablono lauke dabar yra nuoroda į naują šabloną.   
6. Spustelėkite Priedai.
7. Spustelėkite Atidaryti.
    * Spustelėkite Atidaryti, kad ištirtumėte pakeisto „Excel“ šablono išdėstymą.  
    * Peržiūrėkite šabloną. Atkreipkite dėmesį, kad jame dabar yra eilutė mokėjimo datai.   
8. Uždarykite puslapį.
9. Medyje išplėskite „Excel“.
10. Medyje išplėskite „Excel \ PaymLines”.
11. Medyje pasirinkite „Excel\PaymLines\PaymDate“.
    * Atkreipkite dėmesį, kad ER formate dabar yra dar vienas elementas. Langelis PaymDate pridėtas prie „Excel“ šablono.  
12. Spustelėkite skirtuką „Susiejimas“.
13. Medyje išplėskite „modelis‟.
14. Medyje išplėskite „modelis \ Mokėjimai‟.
15. Medyje pasirinkite „modelis \ Mokėjimai \ Operacijos data (TransactionDate)“.
16. Spustelėkite Susieti.
    * Nurodykite, kokie duomenys pridedami prie naujo langelio veikiant.  
17. Spustelėkite Įrašyti.
18. Uždarykite puslapį.

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a>Įgalinkite pakeistą ER formato juodraščio versiją naudoti mokėjimų žurnalo apdorojimui
1. Veiksmų srityje spustelėkite Konfigūracijos.
2. Spustelėkite Vartotojo parametrai.
3. Lauke Paleisti parametrus pasirinkite Taip.
4. Spustelėkite GERAI.
5. Spustelėkite Redaguoti.
6. Lauke Paleisti juodraštį pasirinkite Taip.

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a>Naudokite pakeistą ER formato juodraščio versiją naudoti mokėjimų žurnalo apdorojimui

Peržiūrėkite sukurtą darbalapį, įskaitant naują mokėjimo eilučių informaciją – mokėjimo data.  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]