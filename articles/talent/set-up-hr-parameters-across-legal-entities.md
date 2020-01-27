---
title: Personalo (HR) parametrų nustatymas visiems juridiniams subjektams
description: Turite nustatyti bendrai keliose įmonėse naudojamus įrašus, pvz., įrašus Pareigos. Šiame straipsnyje paaiškinama, kaip keliuose juridiniuose subjektuose nustatyti modulio Personalas parametrus.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 5bd9684b8d5a5847ac212f2ff5214a6bcc3326fd
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897055"
---
# <a name="set-up-human-resources-hr-parameters-across-legal-entities"></a>Personalo (HR) parametrų nustatymas visiems juridiniams subjektams

Turite nustatyti bendrai keliose įmonėse naudojamus įrašus, pvz., įrašus Pareigos. Šiame straipsnyje paaiškinama, kaip keliuose juridiniuose subjektuose nustatyti modulio Personalas parametrus.

Kai kurių tipų įrašai, pvz., pareigų įrašai, yra bendrai naudojami keliose įmonėse. Šiems įrašams reikia nustatyti bendrai naudojamus parametrus. Pavyzdžiui, galite naudoti puslapį **Bendrai naudojami personalo parametrai** kelių juridinių subjektų personalo parametrams nustatyti. 

Puslapyje **Bendrai naudojami personalo parametrai** parametrai sugrupuoti į sritis pagal jų funkcijas. 

### <a name="previously-released-functionality"></a>Anksčiau išleistos funkcijos
Skirtuke **Identifikacija** turite pasirinkti identifikavimo tipus, kurie atitinka identifikavimo numerius, išvardytus puslapyje. Turite nustatyti identifikavimo tipus prieš įvesdami darbuotojų identifikavimo informaciją. Informacija apie socialinio draudimo numerį, asmens kodą ir pašalinio vartotojo ID numerį yra saugoma puslapyje **Identifikavimo tipas**. Norėdami nustatyti naują identifikavimo tipą arba peržiūrėti esamų tipų sąrašą, spustelėkite **Personalo valdymas** &gt; **skirtuką Saitai** &gt; **Sąranka** &gt; **Identifikavimo tipai**. Galite įvesti paprastą kodą ir aprašymą. 

### <a name="if-youre-using-dynamics-365-talent"></a>Jei naudojate „Dynamics 365 Talent“
Skirtuke **Identifikacija** turite pasirinkti identifikavimo tipus, kurie atitinka identifikavimo numerius, išvardytus puslapyje. Turite nustatyti identifikavimo tipus prieš įvesdami darbuotojų identifikavimo informaciją. Informacija apie socialinio draudimo numerį, asmens kodą ir pašalinio vartotojo ID numerį yra saugoma puslapyje **Identifikavimo tipas**. Norėdami nustatyti naują identifikavimo tipą arba peržiūrėti esamų tipų sąrašą, spustelėkite **Personalas** &gt; **Sąranka** &gt; **Identifikavimo tipai**. Galite įvesti paprastą kodą ir aprašymą. 

Skirtuke **Numeracijos** galite pasirinkti numeracijas, naudojamas šiuose įrašuose: darbuotojo numeryje, pareigose, vartotojo užklausos ID, I-9 dokumente, pretendente, diskusijoje, išmokos ID ir personalo veiksme (jei šis įrašo tipas suaktyvintas). Norėdami tvarkyti numeravimo nuorodas ir kodus, naudokite sąrašo puslapį **Numeracijos**. Norėdami rasti šį puslapį, naudokite puslapio ieškos funkciją. 

Skirtuke **Pareigos** nurodykite, ar pagal numatytuosius nustatymus naujas pareigas galima priskirti.

-   **Visada** – galima priskirti darbuotojus naujoms pareigoms kuriant pareigas. Sukūrus pareigas **Galima priskirti** data ir laikas bus automatiškai nustatyti į sukūrimo datą ir laiką skirtuke **Bendra**, esančiame puslapyje **Pareigos**.
-   **Niekada** – negalima priskirti darbuotojų naujoms pareigoms kuriant pareigas. Pasirinkus šią pasirinktį, reikės atidaryti puslapį **Pareigos** apdorojant kiekvienas naujas pareigas, kai jas bus galima naudoti, ir tada skirtuke **Bendra** įvesti **Galima priskirti** datą , kad būtų suaktyvintas darbuotojo priskyrimas.


<a name="additional-resources"></a>Papildomi ištekliai
--------

[Konkrečios įmonės personalo (HR) parametrų nustatymas](set-up-company-specific-hr-parameters.md)



