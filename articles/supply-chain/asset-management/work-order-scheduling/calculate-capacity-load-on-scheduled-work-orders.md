---
title: Suplanuotų darbo užsakymų pajėgumo skaičiavimas
description: Šioje temoje aiškinama, kaip skaičiuoti suplanuotų darbo užsakymų pajėgumą turto valdyme.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0c0dd1e306c54d3f99b86ad6f1816d5acabe6c18
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887164"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Suplanuotų darbo užsakymų pajėgumo skaičiavimas

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Galite skaičiuoti suplanuotų darbo užsakymų pajėgumą, kad peržiūrėtumėte išteklių darbo pajėgumą konkrečiu laikotarpiu. Galima atlikti šių išteklių skaičiavimą: priežiūros darbuotojai, darbuotojų grupės, įrankiai ir turtas.

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Grafikas** > **Pajėgumas**.

2. Dialogo lango **Skaičiuoti konkretų pajėgumą** lauke **Rodyti** pažymėkite, kurį pajėgumo tipą norite skaičiuoti: Pajėgumas, Rezervuota arba Likutis.

3. Perjungimo mygtuke **Praleisti nulį** pažymėkite taip, jei nenorite, kad būtų rodomi nuliniai rezultatai.

4. Pasirinkite išteklių tipus, kurių pajėgumą norite skaičiuoti, atitinkamuose perjungimo mygtukuose – **Darbuotojas**, **Priežiūros darbuotojų grupė**, **Įrankis** ir **Turtas** – pažymėdami Taip.

5. Lauke **Pradžios data** pažymėkite skaičiavimo pradžios datą.

6. Lauke **Intervalo tipas** pažymėkite skaičiavimo intervalą: Diena, Savaitė, Mėnuo arba Ketvirtis.

7. Lauke **Laikotarpio dažnumas** įveskite intervalų, kuriuos norite skaičiuoti, skaičių. Pavyzdžiui, jei kaip intervalo tipą pasirinkote Diena ir lauke įvedėte skaičių 5, bus atliktas penkių dienų nuo pradžios datos skaičiavimas.

8. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

Paveiksle toliau pateikiamas trijų savaičių pajėgumo tipo Rezervuota skaičiavimas.

![1 pav.](media/08-work-order-scheduling.png)

>[!NOTE]
>Jei skaičiavimui pasirenkate Pajėgumas arba Likutis pajėgumo tipus, bus rodomas tas pats rezultatas, jei pasirinktu laikotarpiu nebuvo rezervuota išteklių.

Daugiau informacijos, kaip skaičiuoti priežiūros grafiko eilučių ir nesuplanuotų darbo užsakymų pajėgumą, žr. [Pajėgumo skaičiavimas](../capacity-planning/calculate-capacity-load.md).

