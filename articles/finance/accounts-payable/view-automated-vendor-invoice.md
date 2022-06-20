---
title: Tiekėjo sąskaitos faktūros automatizavimo rezultatų peržiūra (peržiūros versija)
description: Šiame straipsnyje paaiškinama, kaip peržiūrėti tiekėjo SF, kurios yra automatizuoto pateikimo darbo eigos procese, būseną.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd9b74d2ed34399aff455563504c296a5a25a874
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895173"
---
# <a name="view-vendor-invoice-automation-results"></a>Tiekėjo SF automatizavimo rezultatų peržiūra

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip peržiūrėti tiekėjo SF, kurios yra automatizuoto pateikimo darbo eigos procese, būseną. Saugoma kiekvienos importuotos tiekėjo sąskaitos automatizavimo retrospektyvos informacija. Atsižvelgiant į automatizuotus verslo procesus, puslapyje **Laukiančios tiekėjo SF** rodomos **Automatizuoto kvito gretinimo būsena** ir **Automatizuoto pateikimo į darbo eigą būsena** vertės. Galite peržiūrėti išsamią informaciją ir susidaryti planą, skirtą sąskaitų faktūrų, kurių automatizavimo veiksmas buvo nesėkmingas, apdorojimui. Tada, kai išspręsite problemą, galėsite tęsti importuotų sąskaitų faktūrų automatizuotą procesą.

Tam, kad galėtumėte redaguoti pateiktą sąskaitą faktūrą, turite sustabdyti automatizuotą apdorojimą. Jei sąskaita automatizuotame pateikimo į darbo eigos procese turi būti sustabdyta, nustatykite lauko **Įtraukti į automatizuotą apdorojimą**, esančio puslapyje **Tiekėjo sąskaitos faktūros** reikšmę **Ne**. Tada automatizavimas nebus vykdomas, kol nenustatysite lauko **Įtraukti į automatizuotą apdorojimą** reikšmės **Taip**. Sąskaitos faktūros tolesnis automatizavimas gali būti sustabdytas, jei ji dar nėra darbo eigos sistemoje ir nėra naudojama automatizuoto proceso.

Jei importuota sąskaita faktūra yra įtraukta į pateikimo į darbo eigą procesą, jos **Automatizavimo būsena** vertę galite matyti puslapyje **Tiekėjo sąskaitos faktūros**. Skiriamos šios būsenos:

- **Įtraukta** – automatizuoti procesai, apibrėžti puslapyje **Mokėtinų sumų parametrai**, veikia tinkamai, tačiau dar nebaigė darbo.
- **Pristabdyta** – automatizuoti procesai, apibrėžti puslapyje **Mokėtinų sumų parametrai** buvo paleisti, tačiau ne mažiau nei vienas veiksmas buvo nesėkmingas. Būsena **Pristabdyta** taip pat taikoma, jei nustatyta lauko **Įtraukti į automatizuotą apdorojimą** reikšmė yra **Ne**. Klaidas galite peržiūrėti pasirinkę **Peržiūrėti naujausius rezultatus**.
- **Darbo eigoje** – importuota sąskaita faktūra buvo pateikta darbo eigos sistemai naudojant automatizuotą pateikimo į darbo eigą procesą arba rankiniu būdu.
- **Darbo eiga baigta** – importuotos sąskaitos faktūros darbo eigos procesas yra baigtas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
