---
title: Mokėti kliento mokėjimus
description: Deponuokite kliento mokėjimus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445986"
---
# <a name="deposit-customer-payments"></a>Mokėti kliento mokėjimus

[!include [banner](../../includes/banner.md)]

Deponuokite kliento mokėjimus. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Eikite į **Naršymo sritis > Moduliai > Gautinos sumos > Mokėjimai > Mokėjimo žurnalas**.
2. Pasirinkite **Naujas**.
3. Lauke **Pavadinimas** pasirinkite **CustPay** išplečiamajame meniu.
4. Pasirinkite **Eilutės**.
5. Lauke **Klientas** pasirinkite klientą, kuriam išrašote mokėjimą.
6. Lauke **Kreditas** įveskite mokėjimo sumą. Pasirinkdami SF, kurios buvo sumokėtos, galite sumą palikti tuščią, kad ją apskaičiuotų sistema.  
7. Lauke **Mokėjimo nuoroda** įveskite reikšmę. Mokėjimo nuoroda galėtų būti įvedamas mokėjimo čekio numeris. Mokėjimo nuorodos reikia tam, kad mokėjimą būtų galima įtraukti į depozito kvitą,  
8. Pažymėkite langelį Naudoti depozito kvitą. Jei mokėjimas turėtų būti įtrauktas į depozitą, šią nuostatą pakeiskite į Taip.  
9. Pasirinkite **Naujas**.
10. Lauke **Klientas** pasirinkite klientą kitam mokėjimui.
11. Lauke **Kreditas** įveskite mokėjimo sumą.
12. Lauke **Mokėjimo nuoroda** įveskite reikšmę.
13. Pažymėkite langelį **Naudoti depozito kvitą**.
14. Pasirinkite **Registruoti**. Prieš generuojant depozito kvitą, reikia registruoti mokėjimus. Tuo siekiama užtikrinti, kad, sugeneravus depozito kvitą, nepasikeistų mokėjimai.  
15. Pasirinkite **Funkcijos**.
16. Pasirinkite **Depozito kvitas**.
17. Pasirinkite **Gerai**. Pirmasis puslapis naudojamas kurti depozito kvitui.  
18. Pasirinkite **Gerai**. Antrasis veiksmas yra spausdinti depozito kvitą, tačiau šis veiksmas nebūtinas.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]