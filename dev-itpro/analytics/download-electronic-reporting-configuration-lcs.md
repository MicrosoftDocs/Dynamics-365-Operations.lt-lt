---
title: "Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“"
description: "Šioje temoje paaiškinama, kaip parsisiųsti Elektroninė duomenų perdavimo (ER) konfigūracijos iš Microsoft Dynamics gyvavimo ciklo paslaugų (LCS)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektroninių ataskaitų konfigūracijų atsisiuntimas iš „Lifecycle Services“

Šioje temoje paaiškinama, kaip parsisiųsti Elektroninė duomenų perdavimo (ER) konfigūracijos iš Microsoft Dynamics gyvavimo ciklo paslaugų (LCS).

Ši mokymo programa padės jums atsisiųsti naujausias elektroninio ataskaitų (ER) konfigūracijas iš „Microsoft Dynamics Lifecycle Services“ (LCS).

1.  Prisijunkite prie „Dynamics 365 for Operations“ naudodami vieną iš tolesnių vaidmenų.
    -   Elektroninės ataskaitos kūrėjas
    -   Elektroninės ataskaitos funkcijų konsultantas
    -   Sistemos administratorius

2.  Eikite į **organizacijos administracijos**&gt;**elektroniniai pranešimai**.
3.  Dalyje **Konfigūracijų teikėjai** pasirinkite plytelę **Microsoft**.
4.  Plytelėje **Microsoft** spustelėkite **Saugyklos**. [![Update-er-from-LCS-for-MS-Open-MS-Repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  Puslapio **Konfigūracijų saugyklos** tinklelyje pasirinkite esamą tipo **LCS** saugyklą. Jei ši saugykla tinklelyje nerodoma, atlikite tolesnius veiksmus.
    1.  Spustelėdami **Įtraukti** įtraukite naują saugyklą.
    2.  Pasirinkite **LCS** kaip saugyklos tipą.
    3.  Spustelėkite **Kurti saugyklą**.
    4.  Įveskite saugyklos pavadinimą ir aprašymą.
    5.  Spustelėkite **Gerai**, kad patvirtintumėte naują saugyklos įrašą.
    6.  Tinklelyje pasirinkite naują tipo **LCS** saugyklą.

6.  Spustelėkite **Atidaryti**, norėdami peržiūrėti pasirinktos saugyklos ER konfigūracijų sąrašą. [![Update-er-from-LCS-for-MS-Make-LCS-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Kairiojoje srityje esančiame konfigūracijų medyje pasirinkite reikiamą ER konfigūraciją.
8.  „FastTab“ **Versijos** pasirinkite reikiamą pasirinktos ER konfigūracijos versiją.
9.  Spustelėkite **Importuoti**, kad pasirinktą versiją atsisiųstumėte iš LCS į dabartinį „Dynamics 365 for Operations“ egzempliorių. **Pastaba.** Mygtuko **Importuoti** negalima naudoti ER konfigūracijų versijose, kurios jau yra dabartiniame „Dynamics 365 for Operations“ egzemplioriuje. [![Update-er-from-LCS-for-MS-Download-Configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Pastaba.** Atsižvelgiant į ER parametrus, konfigūracijos patikrinamos po importavimo. Galite būti informuoti apie rastas nenuoseklumo problemas. Prieš naudodami importuotą konfigūracijos versiją, turite išspręsti šias problemas. Daugiau informacijos ieškokite šioje temoje susijusių straipsnių sąrašas.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)


