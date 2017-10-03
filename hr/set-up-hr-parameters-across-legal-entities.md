---
title: "Kelių juridinių subjektų personalo parametrų nustatymas"
description: "Turite nustatyti bendrai keliose įmonėse naudojamus įrašus, pvz., įrašus Pareigos. Šiame straipsnyje paaiškinama, kaip keliuose juridiniuose subjektuose nustatyti modulio Personalas parametrus."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: f83bc127f7bf3cdceb39a79c1e69f4f7e96f6462
ms.openlocfilehash: 1a23ec184538510527573de8dd334603dc973ae6
ms.contentlocale: lt-lt
ms.lasthandoff: 06/19/2017


---

# <a name="set-up-hr-parameters-across-legal-entities"></a>Kelių juridinių subjektų personalo parametrų nustatymas

[!include[banner](includes/banner.md)]


Turite nustatyti bendrai keliose įmonėse naudojamus įrašus, pvz., įrašus Pareigos. Šiame straipsnyje paaiškinama, kaip keliuose juridiniuose subjektuose nustatyti modulio Personalas parametrus.

Kai kurių tipų įrašai, pvz., pareigų įrašai, yra bendrai naudojami keliose įmonėse. Šiems įrašams reikia nustatyti bendrai naudojamus parametrus. Pavyzdžiui, galite naudoti puslapį **Bendrai naudojami personalo parametrai** kelių juridinių subjektų personalo parametrams nustatyti. 

Puslapyje **Bendrai naudojami personalo parametrai** parametrai sugrupuoti į sritis pagal jų funkcijas. 

### <a name="previously-released-functionality"></a>Anksčiau išleistos funkcijos
Skirtuke **Identifikacija** turite pasirinkti identifikavimo tipus, kurie atitinka identifikavimo numerius, išvardytus puslapyje. Turite nustatyti identifikavimo tipus prieš įvesdami darbuotojų identifikavimo informaciją. Informacija apie socialinio draudimo numerį, asmens kodą ir pašalinio vartotojo ID numerį yra saugoma puslapyje **Identifikavimo tipas**. Norėdami nustatyti naują identifikavimo tipą arba peržiūrėti esamų tipų sąrašą, spustelėkite **Personalo valdymas** &gt; **skirtuką Saitai** &gt; **Sąranka** &gt; **Identifikavimo tipai**. Galite įvesti paprastą kodą ir aprašymą. 

### <a name="if-youre-using-dynamics-365-for-talent"></a>Jei naudojate „Dynamics 365 for Talent‟
Skirtuke **Identifikacija** turite pasirinkti identifikavimo tipus, kurie atitinka identifikavimo numerius, išvardytus puslapyje. Turite nustatyti identifikavimo tipus prieš įvesdami darbuotojų identifikavimo informaciją. Informacija apie socialinio draudimo numerį, asmens kodą ir pašalinio vartotojo ID numerį yra saugoma puslapyje **Identifikavimo tipas**. Norėdami nustatyti naują identifikavimo tipą arba peržiūrėti esamų tipų sąrašą, spustelėkite **Personalas** &gt; **Sąranka** &gt; **Identifikavimo tipai**. Galite įvesti paprastą kodą ir aprašymą. 

Skirtuke **Numeracijos** galite pasirinkti numeracijas, naudojamas šiuose įrašuose: darbuotojo numeryje, pareigose, vartotojo užklausos ID, I-9 dokumente, pretendente, diskusijoje, išmokos ID ir personalo veiksme (jei šis įrašo tipas suaktyvintas). Norėdami tvarkyti numeravimo nuorodas ir kodus, naudokite sąrašo puslapį **Numeracijos**. Norėdami rasti šį puslapį, naudokite puslapio ieškos funkciją. 

Skirtuke **Pareigos** nurodykite, ar pagal numatytuosius nustatymus naujas pareigas galima priskirti.

-   **Visada** – galima priskirti darbuotojus naujoms pareigoms kuriant pareigas. Sukūrus pareigas **Galima priskirti** data ir laikas bus automatiškai nustatyti į sukūrimo datą ir laiką skirtuke **Bendra**, esančiame puslapyje **Pareigos**.
-   **Niekada** – negalima priskirti darbuotojų naujoms pareigoms kuriant pareigas. Pasirinkus šią pasirinktį, reikės atidaryti puslapį **Pareigos** apdorojant kiekvienas naujas pareigas, kai jas bus galima naudoti, ir tada skirtuke **Bendra** įvesti **Galima priskirti** datą , kad būtų suaktyvintas darbuotojo priskyrimas.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Konkrečios įmonės personalo parametrų nustatymas](set-up-company-specific-hr-parameters.md)




