---
title: Užsakymų įvedimo terminai
description: Šiame straipsnyje pateikiama informacija apie užsakymų įvedimo terminus. Užsakymų įvedimo terminas yra nutraukimo laikas, kuriuo nustatoma, ar kliento užsakymas apdorojamas (ir įvykdomas) taip, lyg jis būtų buvęs gautas dabartinę dieną ar kitą dieną.
author: omulvad
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOrderEntryDeadlineGroup, InventOrderEntryDeadlineParameters, InventOrderEntryDeadlineTable, MCRAutoTaxRules
audience: Application User
ms.reviewer: kamaybac
ms.custom: 7151
ms.assetid: bbc4f9a2-df4b-4d92-9f18-25282a85541f
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b04155bf9c5e282e97eba4fc0a6290c771d7ba3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977668"
---
# <a name="order-entry-deadlines"></a>Užsakymų įvedimo terminai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie užsakymų įvedimo terminus. Užsakymų įvedimo terminas yra nutraukimo laikas, kuriuo nustatoma, ar kliento užsakymas apdorojamas (ir įvykdomas) taip, lyg jis būtų buvęs gautas dabartinę dieną ar kitą dieną.

Daugelyje įmonių tik tie pardavimo užsakymai, kurie yra gauti iki tam tikro dienos meto, laikomi gauti tą dieną. Laikoma, kad visi po nurodyto laiko gauti užsakymai yra gauti kitą darbo dieną. Ši užsakymų nutraukimo data vadinama užsakymo įvedimo terminu.  

Užsakymo įvedimo terminai yra naudojami įvedant numatomas užsakymo datas. Jie padeda valdyti kliento lūkesčius dėl užsakymų pristatymo. Pvz., klientai gali matyti, kad, jei jie pateikia jums užsakymą prieš tam tikrą laiką, jūs įsipareigojate prekes išsiųsti tą pačią dieną. Tačiau jei jie nespėja užsakymo pateikti per tam tikrą laiką, siuntinys gali būti išsiunčiamas tik kitą darbo dieną. Užsakymo įvedimo terminai nustatomi pagal jūsų sandėlio galimybes ir siuntinio vežėjo grafiką.  

Puslapyje **Užsakymo įvedimo terminai** nustatote visoms savaitės dienoms taikomus užsakymo įvedimo terminus. Visi užsakymai, gauti po nustatyto laiko, laikomi gautais kitą darbo dieną. Pagal numatytuosius nustatymus šis laikas yra 23.59 val. (t. y., atitinkamos dienos pabaiga, be vienos minutės vidurnaktis). Numatytuosius laikus galite pakeisti, kad jie sutaptų su faktiniu siuntimo ar gavimo laiku.  

Konkrečioms klientų grupėms galite taikyti specifinius užsakymo įvedimo terminus. Pvz., galbūt norėsite tam tikros grupės klientams nustatyti vėlesnius užsakymo įvedimo terminus, nei kitiems klientams. Šiuo atveju puslapyje **Užsakymo įvedimo terminų grupės** pirmiausia reikia nurodyti grupes, kurioms bus taikomi užsakymo įvedimo terminai. Tada puslapyje **Klientai** turite priskirti grupes klientams.  

Jei jūsų įmonė veikia keliose teritorijose, užsakymo įvedimo terminus galite nustatyti pagal teritoriją. Jei teritorijos išsidėstę skirtingose laiko zonose, užsakymo įvedimo terminai nustatomi pagal kiekvienos teritorijos laiko zoną. Tačiau jei dirbama su pardavimo užsakymais ir pardavimo pasiūlymais, užsakymo įvedimo terminas konvertuojamas į jūsų laiko zoną puslapyje **Galimos siuntimo ir gavimo datos**.  

Puslapyje **Aktyvinti užsakymo įvedimo terminų kombinacijas** galite nurodyti leistinas teritorijų ir užsakymo įvedimo terminų grupių kombinacijas.

## <a name="example-order-entry-deadline"></a>Pavyzdys. Užsakymo įvedimo terminas
Nustatytas užsakymo įvedimo terminas antradieniais – 16.00 val. Konkretų antradienį, 17.00 val., bandote nustatyti esamą datą kaip siuntimo datą. (Atkreipkite dėmesį, kad nenurodomas šio pavyzdžio vykdymo laikas.) Jei pažymėtas žymės langelis **Pristatymo datos valdymas**, gausite įspėjamąjį pranešimą, kuriame bus nurodyta, kad data yra netinkama. Šis įspėjamasis pranešimas bus rodomas puslapyje **Galimos siuntimo ir gavimo datos**, kuriame galite pasirinkti kitas datas.

## <a name="example-different-order-entry-deadlines-per-site"></a>Pavyzdys. Skirtingi užsakymo įvedimo terminai pagal teritoriją
Jūsų įmonė veikia dviejose teritorijose. Teritorijos išsidėsčiusios skirtingose laiko juostose, kaip parodyta pateiktoje lentelėje.

| A teritorija                      | B teritorija                      |
|-----------------------------|-----------------------------|
| Kalifornija                  | Florida                     |
| PST (Ramiojo vandenyno standartinis laikas) | EST (Rytų standartinis laikas) |

A ir B teritorijoms nustatyti šie užsakymo įvedimo terminai.

| Savaitės diena             | A: Užsakymų įvedimo terminai (PST) | B: Užsakymų įvedimo terminai (EST) |
|-----------------------------|--------------------------------|--------------------------------|
| Pirmadienis                      | 13.00                          | 14.00                          |
| Antradienis                     | 13.00                          | 14.00                          |
| Trečiadienis                   | 13.00                          | 14.00                          |
| Ketvirtadienis                    | 13.00                          | 14.00                          |
| Penktadienis                      | 13.00                          | 14.00                          |

Jūs esate atsakingi už užsakymų apdorojimą ir esate Jutoje, kur laiko zona yra MST (Kalnų standartinis laikas). Tai reiškia, kad jei užsakymus skirstysite A teritorijai iki MST 14.00 val., o B teritorijai iki MST 12.00 val., jūs nepažeisite nė vienos teritorijos užsakymo įvedimo terminų.  

Toliau pateikiamoje lentelėje rasite A ir B teritorijų užsakymo įvedimo terminus, konvertuotus į MST laiką.

| A teritorija: (PST)         | A teritorija: (MST)        | B teritorija: (EST)           | B teritorija: (MST)        |
|---------------------|--------------------|-----------------------|--------------------|
| 13.00               | 14.00              | 14.00                 | 12.00              |

**Pastaba.** Jei naudojamas vasaros laikas, atitinkamai koreguojami užsakymo įvedimo terminai.

## <a name="example-same-order-entry-deadline-per-site"></a>Pavyzdys. Vienodi užsakymo įvedimo terminai pagal teritoriją
Jūsų įmonė veikia dviejose teritorijose. Teritorijos išsidėsčiusios skirtingose laiko juostose, kaip parodyta pateiktoje lentelėje.

| A teritorija                      | B teritorija                      |
|-----------------------------|-----------------------------|
| Kalifornija                  | Florida                     |
| PST (Ramiojo vandenyno standartinis laikas) | EST (Rytų standartinis laikas) |

A ir B teritorijoms nustatyti šie užsakymo įvedimo terminai.

| Savaitės diena | PST ir EST |
|-----------------|-------------|
| Pirmadienis          | 13.00       |
| Antradienis         | 13.00       |
| Trečiadienis       | 13.00       |
| Ketvirtadienis        | 13.00       |
| Penktadienis          | 13.00       |

Jūs esate atsakingi už užsakymų apdorojimą ir esate Jutoje, kur laiko zona yra MST. Tai reiškia, kad jei užsakymus skirstysite A teritorijai iki MST 14.00 val., o B teritorijai iki MST 11.00 val., jūs nepažeisite nė vienos teritorijos užsakymo įvedimo terminų. 

Toliau pateikiamoje lentelėje rasite A ir B teritorijų užsakymo įvedimo terminus, konvertuotus į MST laiką.

| A teritorija: (PST)         | A teritorija: (MST)        | B teritorija: (EST)           | B teritorija: (MST)        |
|---------------------|--------------------|-----------------------|--------------------|
| 13.00               | 14.00              | 13.00                 | 11.00              |

**Pastaba.** Jei naudojamas vasaros laikas, atitinkamai koreguojami užsakymo įvedimo terminai.

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Pristatymo grafikai](delivery-schedules.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]