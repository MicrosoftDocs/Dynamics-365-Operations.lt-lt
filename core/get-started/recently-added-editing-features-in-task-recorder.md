---
title: "Neseniai pridėti redagavimo funkcijų, užduočių rašytuvas"
description: "Jei naudodami užduočių rašytuvą kurti užduotis vadovus, galite redaguoti failus daugiau efektyviai naudojant funkciją, aprašytą šiame wiki."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core
ms.custom: 266464
ms.assetid: b4640e67-4b92-4855-8041-1bfc71aadc47
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: c4f9ac515eab6ed8b194fc8985f6d3fae40ced38
ms.lasthandoff: 03/31/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Neseniai pridėti redagavimo funkcijų, užduočių rašytuvas

Jei naudodami užduočių rašytuvą kurti užduotis vadovus, galite redaguoti failus daugiau efektyviai naudojant funkciją, aprašytą šiame wiki.

Šias funkcijas galima rasti, **parametrai &gt;užduočių rašytuvą &gt;redaguoti įrašą** meniu.

-   Įterpti veiksmus be perrašymą visą failą.
-   Perkelti veiksmus pagal subrangos užduotis be perrašymą visą failą.
-   Sutraukti įrašymo laukuose pavadinimas ir aprašas.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Įterpti veiksmus be rerecording visą failą
Dabar galite pridėti žingsnis visur užduoties vadovas be Groti arba perrašymo visą failą.

1.  Pasirinkite veiksmą, po kurios norite įterpti naują žingsnį. Įsitikinkite, kad žingsnis yra paryškinta.

Kad įterpti žingsnis užduočių rašytuvą, turite atidaryti teisingame puslapyje. Teisingas puslapis yra puslapis, kuriame kyla naujas žingsnis. Užduočių rašytuvas yra mechanizmas, kuris nustato, kas puslapių yra, o bus išjungti funkciją, jei teisingas puslapis nėra atidarytas. 

[![1tg](./media/tg1.png)](./media/tg1.png) 


Kai esate teisingame puslapyje, **įterpti žingsnis** tampa prieinama.

[![2TG](./media/tg2-231x300.png)](./media/tg2.png)

2. Spustelėkite **įterpti žingsnis**.

Kai spustelite **įterpti žingsnis**, užduočių rašytuvą persijungia į įrašymo režimu. Kokių veiksmų buvo imtasi vartotojo sąsaja dabar fiksuojamos ir papildomas vietoje veiksmus.

3. Spustelėkite **sustabdyti**.

Galite pakartoti šį procesą, įtraukti kuo daugiau priemonių arba perkelti kuo daugiau subrangos užduotis pagal poreikį (žr. toliau į pietus užduotis).

4. Baigę redaguoti užduoties vadovas, spustelėkite **atlikti redagavimo**, ir tada pasirinkite parinktį įrašyti arba paskelbti užduoties vadovas.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Perkelti antrinės veiksmus, be rerecording visą failą
Galite perkelti veiksmus pagal subrangos užduotis be Groti arba perrašymo visą failą. Taip pat galite perkelti subrangos užduotis žingsnis arba pabaigos subrangos užduotis žingsnis, jei norite grupuoti esamas blokas, veiksmus.

1.  Pasirinkite veiksmą arba subrangos užduotis veiksmą, kurį norite perkelti. Įsitikinkite, kad žingsnis yra paryškinta.
2.  Spustelėkite elipsę, tada spustelėkite **pereiti žingsnis po**.

[![TG3](./media/tg3.png)](./media/tg3.png)

3. Pasirinkite veiksmą arba subrangos užduotis veiksmą, kurį norite perkelti veiksmą arba subrangos užduotis žingsnis po. Užduočių rašytuvas pereis prie veiksmo.

4. Perkelti pabaigos subrangos užduotis veiksmas, pažymėkite jį, spustelėkite elipsę, spustelėkite **pereiti žingsnis po**, ir tada pasirinkite žingsnis, po kurio norite pabaigos subrangos užduotis žingsnis, kad būtų.

Jei norite, kad užduočių vadovą pagal subrangos užduotis, pirmiausia, sukurti subrangos užduotis žingsnis būtų antrasis etapas ir perkelkite pirmasis žingsnis į jį. Galite įtraukti arba perkelti kuo daugiau priemonių arba subrangos užduotis, kiek reikia.

5. Baigę redaguoti užduoties vadovas, spustelėkite **atlikti redagavimo**, ir tada pasirinkite parinktį įrašyti arba paskelbti užduoties vadovas.

## <a name="collapse-recording-name-and-description"></a>Sutraukti įrašo pavadinimą ir aprašą
Jūs galite išplėsti arba sutraukti į **įrašo pavadinimas** ir **įrašymo Aprašymas** laukus. Jei šiose srityse yra sutraukti, daugiau veiksmų bus rodomas užduočių rašytuvą redagavimo srityje. 

[![TG4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Kurkite dokumentus ar mokymus naudodami Užduočių įrašus](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Užduočių rašytuvas greitos nuorodos](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)


