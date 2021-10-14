---
title: Koreguoti atsargų lygius sandėlyje (pagrindinis sandėliavimas)
description: Ši procedūra padės kurti ir registruoti atsargų koregavimo žurnalą, norint pakoreguoti produktų atsargų lygius sandėlyje.
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 02458d588c9925a1f4cb9afeada793dfc55a2071
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573830"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Koreguoti atsargų lygius sandėlyje (pagrindinis sandėliavimas)

[!include [banner](../../includes/banner.md)]

Ši procedūra padės kurti ir registruoti atsargų koregavimo žurnalą, norint pakoreguoti produktų atsargų lygius sandėlyje. Prieš pradedant atsargų koregavimus, reikia turėti atsargų žurnalo pavadinimo nustatymą. Šią procedūrą galite atlikti naudodami demonstracinių duomenų įmonę USMF arba savo duomenis. Šias užduotis paprastai turėtų atlikti sandėlio darbuotojas.


## <a name="create-an-inventory-adjustment-journal"></a>Atsargų koregavimo žurnalo kūrimas
1. Pasirinkite Atsargų valdymas > Žurnalo įrašai > Prekės > Atsargų koregavimas.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
4. Sąraše spustelėkite atsargų koregavimo žurnalo pavadinimą, kurį norite naudoti.
    * Kai kurie kiti laukai bus užpildyti atsižvelgiant į pasirinkto atsargų koregavimo žurnalo pavadinimo nustatymą.  
5. Spustelėkite GERAI.

## <a name="create-journal-lines"></a>Žurnalo eilučių kūrimas
1. Spustelėkite Naujas.
2. Sąraše pažymėkite prekės numerio lauką.
3. Lauke Prekės numeris pasirinkite prekę. Jei naudojate demonstracinių duomenų įmonės USMF, įveskite „D0001“.
4. Lauke Teritorija spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
5. Sąraše pasirinkite vietą.
6. Lauke Sandėlis spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
7. Sąraše pasirinkite sandėlį.
    * Jei pasirinkote prekę, kurios privaloma dimensija Vieta, čia turėtumėte nurodyti vietą.  
8. Lauke Kiekis įveskite skaičių.
    * Savikainos lauke nurodoma vieneto kaina, skirta atsargų gavimams. Jei prekės numerio savikaina nenurodyta arba, jei norėjote ją pakeisti neautomatiniu būdu, padarykite tai čia.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Atsargų koregavimo žurnalo tikrinimas ir registravimas
1. Spustelėkite Tikrinti.
2. Spustelėkite GERAI.
3. Spustelėkite Registruoti.
    * Registruojant tokį žurnalą, užregistruojamas atsargų gavimas arba išdavimas, pakeičiamas atsargų lygis ir vertė bei sugeneruojamos DK operacijos.  
4. Spustelėkite GERAI.
5. Uždarykite formą.
6. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]