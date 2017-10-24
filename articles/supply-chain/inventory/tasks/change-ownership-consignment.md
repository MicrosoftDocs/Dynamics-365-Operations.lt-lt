---
title: "Konsignacinių atsargų nuosavybės pakeitimas pagal gamybos poreikį"
description: "Šioje procedūroje parodoma, kaip pakeisti konsignacijos atsargų savininką iš tiekėjo į savo juridinį subjektą esant gaminamų atsargų poreikiui."
author: perlynne
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5925f5423d596adc4326dfff4734de2afd80b5a8
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Konsignacinių atsargų nuosavybės pakeitimas pagal gamybos poreikį

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip pakeisti konsignacijos atsargų savininką iš tiekėjo į savo juridinį subjektą esant gaminamų atsargų poreikiui. Šis nuosavybės pakeitimas atliekamas kuriant ir registruojant atsargų nuosavybės pakeitimo žurnalą. Nuosavybės pakeitimo žurnalo eilutes galima kurti neautomatiniu būdu arba, kaip parodyta šiame įraše, pagal esamą gamybos poreikį. Paprastai šią užduotį atlieka darbo laiko prižiūrėtojas. Šią procedūrą galite atlikti demonstracinių duomenų įmonėje USMF arba su savo duomenimis. Jei naudojate savo duomenis, įsitikinkite, kad tenkinamos šios sąlygos: nustatytas atsargų nuosavybės pakeitimo žurnalo pavadinimas, tiekėjui priklausiančios turimos prekės fiziškai įrašytos ir yra viena arba daugiau medžiagos gamybos užsakymo eilučių. Ši procedūra yra skirta funkcijai, įtrauktai į „Dynamics 365 for Operations“ 1611 versiją.


## <a name="create-an-inventory-ownership-journal"></a>Atsargų nuosavybės žurnalo kūrimas
1. Eikite į Atsargų valdymas > Žurnalo įrašai > Prekės > Atsargų nuosavybės pakeitimas.
2. Spustelėkite Naujas.
    * Atsargų nuosavybės pakeitimo žurnalas naudojamas norint keisti konsignacijos atsargų savininką iš tiekėjo į dabartinį juridinį subjektą. Šis nuosavybės pakeitimas atliekamas išleidžiant turimas atsargas, kurios priklauso tiekėjui, ir tada gaunant tas atsargas dabartiniame juridiniame subjekte.  
3. Lauke Pavadinimas įveskite arba pasirinkite reikšmę.
    * Galite pasirinkti tik atsargų žurnalų pavadinimus, kurių žurnalo tipas yra Nuosavybės pakeitimas.  
4. Spustelėkite GERAI.
5. Spustelėkite Funkcijos.
6. Spustelėkite Kurti žurnalo eilutes iš gamybos užsakymų.
    * Galite pradėti nuosavybės pakeitimo procesą, pateikdami užklausą dėl visų gamybos eilučių, kuriose yra žaliavų sunaudojimo poreikis.  
7. Lauke Įtrauktinos atsargų išdavimo būsenos pasirinkite parinktį.
    * Ši parinktis leidžia filtruoti pagal atsargų operacijų išdavimo būseną. Pavyzdžiui, galite kurti žurnalo eilutes, skirtas atsargoms, kurių būsena yra Paimta arba Rezervuota faktiškai.  
8. Išplėskite dalį Įtrauktini įrašai.
    * Šis skyrius suteikia galimybę taikyti papildomus filtrus. Pavyzdžiui, galite pasirinkti konkrečią žaliavų datą.  
9. Spustelėkite GERAI.

## <a name="post-the-inventory-ownership-change-journal"></a>Atsargų nuosavybės pakeitimo žurnalo registravimas
1. Spustelėkite Registruoti.
    * Kai žurnalas užregistruojamas, tiekėjui priklausančios atsargos yra išleidžiamos naudojant nuorodą Nuosavybės pakeitimas. Tada atsargos yra gaunamos kaip turimas kiekis naudojant atsargų operaciją, kuri yra atnaujinama pirkimo užsakymo gavimo dokumentu. Atkreipkite dėmesį, kad kuriamos tik operacijos, susijusios su užregistruotu žurnalu. Numatomų atsargų operacijos nekuriamos.  
2. Spustelėkite GERAI.
3. Uždarykite puslapį.

