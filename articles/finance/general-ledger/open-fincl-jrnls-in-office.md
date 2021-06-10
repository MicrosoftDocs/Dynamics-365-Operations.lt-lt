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
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089462"
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
