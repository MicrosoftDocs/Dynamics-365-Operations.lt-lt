---
title: Žurnalų ir eilučių parametrų atšaukimas
description: Šioje temoje nagrinėjama, kodėl bendrajame žurnale įvestas atšaukimo įrašas gali būti neįtrauktas į užregistruotą operaciją.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028576"
---
# <a name="reverse-settings-on-journals-and-lines"></a>Žurnalų ir eilučių parametrų atšaukimas

[!include [banner](../includes/banner.md)]

Šioje temoje nagrinėjama, kodėl bendrajame žurnale įvestas atšaukimo įrašas gali būti neįtrauktas į užregistruotą operaciją.  

## <a name="symptom"></a>Požymis

Bendrajame žurnale yra žurnalo atšaukimo įrašas ir atšaukimo data. Kai registruojate žurnalą, joks kvitas nėra atšauktas. Kodėl taip atsitinka?

## <a name="resolution"></a>Sprendimas

Užregistravus žurnalą, vykdant atšaukimo procesą atsižvelgiama tik į parametrus **Atšaukimo įrašas** ir **Atšaukimo data** kvito skyriuje **Eilutės**. Šis metodas leidžia žurnalui įtraukti kai kuriuos kvitus, kurie yra pažymėti atšaukti, ir kitus, kurie nėra pažymėti.

Žurnalo reikšmės naudojamos tik kaip numatytosios, kai įtraukiama *naujų* eilučių. Reikšmių keitimas žurnale neturi įtakos esamoms eilutėms. Šiame pavyzdyje pirmiausia buvo įtrauktos kvito eilutės. Kai įvedate eilutės informaciją prieš nurodydami žurnalą kaip atšaukiamą, nurodymas kaip atšaukimo įrašas ir data nebus taikomas esančioms eilutėms.

Keičiant esamos eilutės atšaukimo įrašą arba atšaukimo datą keitimas atliekamas ir kitose to paties kvito eilutėse. Siekiant optimizuoti našumą, tinklelis neatnaujinamas atlikus keitimus kitose eilutėse. Atnaujintos reikšmės gali būti rodomos atnaujintus tinklelį.


