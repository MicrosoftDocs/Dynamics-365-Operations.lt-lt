---
title: Suplanuotų darbo užsakymų pajėgumo skaičiavimas
description: Šioje temoje aiškinama, kaip skaičiuoti suplanuotų darbo užsakymų pajėgumą turto valdyme.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ff244e51151a1cc0485cae25873566fa97253171516d48449fed75f070146431
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766223"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Suplanuotų darbo užsakymų pajėgumo skaičiavimas

[!include [banner](../../includes/banner.md)]

 

Galite skaičiuoti suplanuotų darbo užsakymų pajėgumą, kad peržiūrėtumėte išteklių darbo pajėgumą konkrečiu laikotarpiu. Galima atlikti šių išteklių skaičiavimą: priežiūros darbuotojai, darbuotojų grupės, įrankiai ir turtas.

1. Spustelėkite **Turto valdymas** > **Užklausos** > **Grafikas** > **Pajėgumas**.

2. Dialogo lango **Skaičiuoti pajėgumą** > lauke **Rodyti** pasirinkite, kurį pajėgumo tipą norite skaičiuoti: **Pajėgumas**, **Rezervuota** arba **Likutis**.

3. Perjungimo mygtuke **Praleisti nulį** pasirinkite **Taip**, jei nenorite, kad būtų rodomi nuliniai rezultatai.

4. Pasirinkite išteklių tipus, kurių pajėgumą norite skaičiuoti, atitinkamuose perjungimo mygtukuose **Darbuotojas**, **Priežiūros darbuotojų grupė**, **Įrankis** ir **Turtas** pasirinkdami **Taip**.

5. Lauke **Pradžios data** pažymėkite skaičiavimo pradžios datą.

6. Lauke **Intervalo tipas** pasirinkite skaičiavimo intervalą: **Diena**, **Savaitė**, **Mėnuo** arba **Ketvirtis**.

7. Lauke **Laikotarpio dažnumas** įveskite intervalų, kuriuos norite skaičiuoti, skaičių. Pavyzdžiui, jei kaip intervalo tipą pasirinkote **Diena** ir lauke įvedėte skaičių „5“, bus atliktas penkių dienų nuo pradžios datos skaičiavimas.

8. Norėdami pradėti skaičiavimą, spustelėkite **Gerai**.

Toliau esančiame paveikslėlyje pateiktas trijų savaičių pajėgumo tipo **Rezervuota** skaičiavimas.

![1 iliustracija.](media/08-work-order-scheduling.png)

[!NOTE]
Jei skaičiavimui pasirinkote pajėgumo tipus **Pajėgumas** arba **Likutis**, jei pasirinktu laikotarpiu nebuvo rezervuota išteklių, bus rodomas tas pats rezultatas.

Informacijos apie tai, kaip skaičiuoti priežiūros grafiko eilučių ir nesuplanuotų darbo užsakymų pajėgumą, žr. [Pajėgumo skaičiavimas](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]