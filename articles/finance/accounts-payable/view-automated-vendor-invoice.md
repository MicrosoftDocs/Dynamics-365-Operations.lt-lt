---
title: Tiekėjo sąskaitos faktūros automatizavimo rezultatų peržiūra (peržiūros versija)
description: Šioje temoje paaiškinama, kaip peržiūrėti tiekėjo sąskaitų faktūrų, kurios yra įtrauktos į automatizuoto pateikimo į darbo eigą procesą, būseną.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: baa2f1f55dfb9bb93b4f27c45db563e39850dd37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969731"
---
# <a name="view-vendor-invoice-automation-results"></a>Tiekėjo SF automatizavimo rezultatų peržiūra

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip peržiūrėti tiekėjo sąskaitų faktūrų, kurios yra įtrauktos į automatizuoto pateikimo į darbo eigą procesą, būseną. Saugoma kiekvienos importuotos tiekėjo sąskaitos automatizavimo retrospektyvos informacija. Atsižvelgiant į automatizuotus verslo procesus, puslapyje **Laukiančios tiekėjo SF** rodomos **Automatizuoto kvito gretinimo būsena** ir **Automatizuoto pateikimo į darbo eigą būsena** vertės. Galite peržiūrėti išsamią informaciją ir susidaryti planą, skirtą sąskaitų faktūrų, kurių automatizavimo veiksmas buvo nesėkmingas, apdorojimui. Tada, kai išspręsite problemą, galėsite tęsti importuotų sąskaitų faktūrų automatizuotą procesą.

Tam, kad galėtumėte redaguoti pateiktą sąskaitą faktūrą, turite sustabdyti automatizuotą apdorojimą. Jei sąskaita automatizuotame pateikimo į darbo eigos procese turi būti sustabdyta, nustatykite lauko **Įtraukti į automatizuotą apdorojimą**, esančio puslapyje **Tiekėjo sąskaitos faktūros** reikšmę **Ne**. Tada automatizavimas nebus vykdomas, kol nenustatysite lauko **Įtraukti į automatizuotą apdorojimą** reikšmės **Taip**. Sąskaitos faktūros tolesnis automatizavimas gali būti sustabdytas, jei ji dar nėra darbo eigos sistemoje ir nėra naudojama automatizuoto proceso.

Jei importuota sąskaita faktūra yra įtraukta į pateikimo į darbo eigą procesą, jos **Automatizavimo būsena** vertę galite matyti puslapyje **Tiekėjo sąskaitos faktūros**. Skiriamos šios būsenos:

- **Įtraukta** – automatizuoti procesai, apibrėžti puslapyje **Mokėtinų sumų parametrai**, veikia tinkamai, tačiau dar nebaigė darbo.
- **Pristabdyta** – automatizuoti procesai, apibrėžti puslapyje **Mokėtinų sumų parametrai** buvo paleisti, tačiau ne mažiau nei vienas veiksmas buvo nesėkmingas. Būsena **Pristabdyta** taip pat taikoma, jei nustatyta lauko **Įtraukti į automatizuotą apdorojimą** reikšmė yra **Ne**. Klaidas galite peržiūrėti pasirinkę **Peržiūrėti naujausius rezultatus**.
- **Darbo eigoje** – importuota sąskaita faktūra buvo pateikta darbo eigos sistemai naudojant automatizuotą pateikimo į darbo eigą procesą arba rankiniu būdu.
- **Darbo eiga baigta** – importuotos sąskaitos faktūros darbo eigos procesas yra baigtas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]