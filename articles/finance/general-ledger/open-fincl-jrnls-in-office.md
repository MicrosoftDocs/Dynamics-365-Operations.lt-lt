---
title: Finansinių žurnalų šablonų atidarymas „Office“
description: Šioje temoje aprašomos problemos, kurios gali kilti kuriant pasirinktinius finansinius žurnalus naudojant „Microsoft Excel“ šabloną.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8c0c8d8e2e9b1978523bea378f4e231d9ebe3d1e8ccdc11ad8578eac16b067cf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753533"
---
# <a name="open-financial-journal-templates-in-office"></a>Finansinių žurnalų šablonų atidarymas „Office“

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos problemos, kurios gali kilti kuriant pasirinktinius finansinius žurnalus naudojant „Microsoft Excel“ šabloną.

## <a name="symptom"></a>Požymis

Sukūrėte pasirinktinį finansinių žurnalų „Excel“ šabloną, bet jis nerodomas meniu **Atidaryti eilutes programoje „Excel“**. Arba jis rodomas meniu, tačiau jį pasirinkus atidaromas kitas šablonas.

## <a name="resolution"></a>Sprendimas

Numatytoji atidarymo programoje „Excel“ funkcija naudoja dabartinio puslapio šakninį duomenų šaltinį (lentelę) nustatyti, kurie „Office“ šablonai ar duomenų objektai rodomi kaip parinktys meniu **Atidaryti programoje „Excel“**. Tai nėra geriausias finansinių žurnalų veikimo būdas, nes finansiniai žurnalai naudoja tas pačias lenteles (LedgerJournalTable ir LedgerJournalTrans) kaip daugelio kitų žurnalų tipų šakninį duomenų šaltinį.

Finansinių žurnalų funkcija Atidaryti eilutes programoje „Excel“ skirta šablonams, sukurtiems žurnalui, su kuriuo šiuo metu dirbate, pavyzdžiui, bendrajam žurnalui arba mokėjimų žurnalui, rodyti. Pavyzdžiui, šablonas, kurį norite naudoti su tiekėjo mokėjimų žurnalu, bus sukurtas jūsų pirminei sąskaitai kaip tiekėjo sąskaitai vykdyti.

Jei norite paaukštinti šabloną, kad jis būtų prieinamas meniu **Atidaryti eilutes programoje „Excel“** ir **Atidaryti programoje „Excel“**, kūrėjai paprasčiausia gali įdiegti sąsają **LedgerIJournalExcelTemplate** ir išplėsti klasę **DocuTemplateRegistrationBase**. Sistemoje įdiegta daug šio metodo pavyzdžių. Vienas pavyzdys, kurį galima naudoti kaip nuorodą, yra sąsaja **LedgerDailyJournalExcelTemplate**, kuri buvo sukurta bendrajam žurnalui (arba kasdieniam žurnalui).

Kai sąsaja **LedgerIJournalExcelTemplate** įdiegta jūsų šablonui, meniu **Atidaryti eilutes programoje „Excel“** išfiltruos šablonus pagal jūsų žurnalo tipą ir rodys tik tam žurnalui galimus šablonus. Sąsaja taip pat pateikia tikrinimo metodą, kuris užtikrina, kad žurnalo šablono negalima atidaryti, jei jis neatitinka sąskaitos tipo reikalavimų. Pavyzdžiui, galite nurodyti, kad sąskaitos tipas turi būti **Tiekėjas** arba **Didžioji knyga**.

Daugiau informacijos apie šią funkciją žr. [Šablonų įtraukimas į meniu Atidaryti eilutes programoje „Excel“](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).
