---
title: Suplanuotų darbo užsakymų pajėgumo skaičiavimas
description: Šioje temoje aiškinama, kaip skaičiuoti suplanuotų darbo užsakymų pajėgumą turto valdyme.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7b7e4a20ed56b1eac29d16d527693d6e455cdc37
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021659"
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

![1 pav.](media/08-work-order-scheduling.png)

[!NOTE]
Jei skaičiavimui pasirinkote pajėgumo tipus **Pajėgumas** arba **Likutis**, jei pasirinktu laikotarpiu nebuvo rezervuota išteklių, bus rodomas tas pats rezultatas.

Informacijos apie tai, kaip skaičiuoti priežiūros grafiko eilučių ir nesuplanuotų darbo užsakymų pajėgumą, žr. [Pajėgumo skaičiavimas](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]