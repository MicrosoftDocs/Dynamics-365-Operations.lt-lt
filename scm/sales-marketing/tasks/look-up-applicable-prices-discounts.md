--- 
title: "Peržiūrėti taikytinas kainas ir nuolaidas"
description: "Ši procedūra nurodo, kaip rasti produkto kainą ir (arba) nuolaidą, kuri šiuo metu taikoma konkrečiam klientui, nesukuriant pardavimo užsakymo."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ecfe2ad4dbba74cb067628b63abaf780bcf0680e
ms.contentlocale: lt-lt
ms.lasthandoff: 07/27/2017

---
# <a name="look-up-applicable-prices-and-discounts"></a>Peržiūrėti taikytinas kainas ir nuolaidas

[!include[task guide banner](../../includes/task-guide-banner.md)]

Ši procedūra nurodo, kaip rasti produkto kainą ir (arba) nuolaidą, kuri šiuo metu taikoma konkrečiam klientui, nesukuriant pardavimo užsakymo. Procedūra žingsnis po žingsnio apžvelgia konkretų pavyzdį, kuriuo jums reikės vadovautis naudojant demonstracinę įmonę USMF, kad pasirinktumėte būtinas reikšmes.


## <a name="find-the-applicable-price"></a>Rasti taikomą kainą
1. Eikite į Pardavimas ir rinkodara > Kainos ir nuolaidos > Rasti kainas.
2. Lauke Kliento sąskaita spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
3. Sąraše raskite ir pasirinkite klientą US-001.
4. Sąraše spustelėkite saitą pasirinktoje eilutėje.
5. Lauke „Prekės numeris“ įveskite „T0004“.
    * Numatyta, kad lauko „Kiekis“ reikšmė yra 1. Tačiau, jei žinote kliento ketinamo pateikti susijusių produktų užsakymo dydį, tada įveskite šią reikšmę. Ši informacija aktuali, jei su klientu sudarytose prekybos sutartyse numatytos kiekių ribos, t. y., produkto kaina priklauso nuo mažiausio perkamo kiekio.  
6. Lauke „Data“ įveskite datą, kada klientas tikisi pateikti užsakymą. 
    * Data gali būti šiandiena arba bet kuri kita data ateityje.  
    * Dabar sistema nurodys kainą, kuri galioja pasirinktam produktui, kai jį perka pasirinktas klientas, pasirinktą dieną pagal nurodytą kiekį. Šiame pavyzdyje, jei klientas US-001 šiandien perka 1 produkto T0004 vienetą, turėtų sumokėti 350 CAD už vienetą. Ši kaina nustatoma pagal esamą ir galiojančią prekybos sutartį su klientu.      Kituose puslapio laukuose pateikiama daugiau informacijos apie produkto kainą, produkto savikainą (jei nustatyta bendrajame produkte) ir apskaičiuotą pelningumą.  
    * Jei pasirinkta „Rodyti susijusius produkto variantus“, tai reiškia, kad yra papildomų prekybos sutarčių dėl produkto variantų.  
7. Pažymėkite žymės langelį „Rodyti susijusius produkto variantus“.
    * Rodomas produkto variantų sąrašas su informacija apie jų dimensijas.  
8. Sąraše pažymėkite baltą spalvą reprezentuojančią eilutę.
    * Atkreipkite dėmesį, kad produkto kaina dabar skiriasi nuo anksčiau rodytos, kai ji nebuvo apskaičiuota pagal dimensiją.  
9. Spustelėkite „Peržiūrėti pardavimo kainas“.
    * Puslapyje „Kaina (pardavimai)“ rodomos visos produktui, įskaitant jo variantus, taikomos prekybos sutartys.  
10. Uždarykite puslapį.

## <a name="find-the-applicable-discount"></a>Rasti taikomą nuolaidą
    * Įsitikinkite, kad lauke „Kliento sąskaita“ yra kliento numeris US-001    
1. Lauke „Prekės numeris“ įveskite „T0012“.
    * Įsitikinkite, kad lauko „Kiekis“ reikšmė yra 1.  
    * Tokie produktui T0012 taikomi įkainiai nustatyti pagal vieną ar daugiau prekybos sutarčių: vieneto kaina yra 1000 CAD, o nuolaidos procentas yra 5.  
2. Nustatykite kiekį – 20.
    * Dėl didesnio užsakymo kiekio eilutei taikoma nuolaida – klientui bus pasiūlyta ją padidinti nuo 5 iki 7 procentų.  
    * Grynoji suma apskaičiuojama pagal vieneto kainą, nuolaidą ir bendrą kiekį.  
3. Spustelėkite „Peržiūrėti eilutės nuolaidą“.
    * Yra dvi eilutės nuolaidos sutartys produktui T0012, nurodančios 5 proc. nuolaidą užsakymo eilutės kiekiui nuo 1 iki 10 ir 7 proc. nuolaidą užsakymams, viršijantiems 10. Atkreipkite dėmesį, kad šiame pavyzdyje nuolaidos taikomos produktų grupei (grupės kodas 01), kurios narys yra T0012 produktas.  
4. Uždarykite puslapį.


