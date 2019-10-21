---
title: Atšaukimo registravimas žurnale
description: Šioje temoje aprašomos galimybės, leidžiančios atšaukti kvitus iš kvitų operacijų sąrašo arba iš finansinių žurnalų.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248590"
---
# <a name="reverse-journal-posting"></a>Atšaukimo registravimas žurnale

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos „Microsoft“ „Dynamics 365 Finance“ galimybės, leidžiančios atšaukti visą žurnalą arba atšaukti vieną ar keletą kvitų iš kvitų operacijų sąrašo, neatsižvelgiant į jų kilmę. 

## <a name="reversing-journals"></a>Žurnalų atšaukimas

Galite atšaukti atskiras žurnalo eilutes. Registruodami atšaukimą žurnale, taip pat galite atšaukti visą finansinį žurnalą. Atšaukite žurnalą, atlikę toliau pateikiamus veiksmus. 
- Atidarykite finansinį žurnalą ir filtruokite užregistruotus žurnalus
- Spustelėkite puslapio viršuje esantį meniu Atšaukti
- Matysite bendrą kvitų ir kvitų eilučių skaičių, taip pat bendrą atšaukiamų eilučių sumą
- Pasirinkite Taip, jei norite, kad būtų naudojamos esamos operacijų datos, arba Ne, kad įvestumėte naują. Kai kuriais atvejais pradinės operacijos laikotarpis gali būti uždarytas, o jūs norite įvesti naują atšaukimo operacijos datą.
- Jei pasirinkote Ne, įveskite atšaukimo operacijos datą. 
- Įveskite komentarą, kurį norite įtraukti į atšaukimo operaciją
- Spustelėkite mygtuką Atšaukti

Operacijos bus atšauktos. 

Jei kvitų eilučių skaičius viršija 100 eilučių, atšaukimo procesas bus vykdomas naudojant paketinį procesą. Galite peržiūrėti atšaukimo rezultatus peržiūrėję įvykdytos paketinės užduoties komentarus. Visos klaidos bus įtrauktos į paketinių užduočių retrospektyvą.

Jei kvitų eilučių skaičius neviršija 100 eilučių, atšaukimo procesas bus vykdomas nedelsiant. Rezultatai bus pateikti dialogo lange, kuriame rodomi visi kvitai, kurių nepavyko atšaukti, ir priežastys, dėl kurių nepavyko atšaukti. Spustelėję Gerai, užverkite dialogo langą.

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>Kvitų atšaukimas kvitų operacijų sąraše. 

Kvitus taip pat galite atšaukti **Kvitų operacijų sąraše** visose papildomose knygose. Be to, vienu metu galite atšaukti keletą kvitų. 

Norėdami atšaukti vieną ar daugiau kvitų, atlikite toliau pateikiamus veiksmus. 
- Spustelėkite puslapio viršuje esantį meniu Atšaukti
- Matysite bendrą kvitų ir kvitų eilučių skaičių, taip pat bendrą atšaukiamų eilučių sumą
- Pasirinkite Taip, jei norite, kad būtų naudojamos esamos operacijų datos, arba Ne, kad įvestumėte naują. Kai kuriais atvejais pradinės operacijos laikotarpis gali būti uždarytas, o jūs norite įvesti naują atšaukimo operacijos datą.
- Jei pasirinkote Ne, įveskite atšaukimo operacijos datą. 
- Įveskite komentarą, kurį norite įtraukti į atšaukimo operaciją
- Spustelėkite mygtuką Atšaukti

Operacijos bus atšauktos. 

Jei kvitų eilučių skaičius viršija 100 eilučių, atšaukimo procesas bus vykdomas naudojant paketinį procesą. Galite peržiūrėti atšaukimo rezultatus peržiūrėję įvykdytos paketinės užduoties komentarus. Visos klaidos bus įtrauktos į paketinių užduočių retrospektyvą.

Jei kvitų eilučių skaičius neviršija 100 eilučių, atšaukimo procesas bus vykdomas nedelsiant. Rezultatai bus pateikti dialogo lange, kuriame rodomi visi kvitai, kurių nepavyko atšaukti, ir priežastys, dėl kurių nepavyko atšaukti. Spustelėję Gerai, užverkite dialogo langą.

