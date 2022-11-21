---
title: Vėlesnių čekių nustatymas
description: Šiame straipsnyje paaiškinama, kaip nurodyti, ar registruoti žurnalo įrašus postduotims čekiams ir kurie registravimo žurnalai bus naudojami tarpuskaitos įrašams ir tiekėjo mokėjimams.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e7172dd56113de23d841fe59ed9785471e90ed1f
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779615"
---
# <a name="set-up-postdated-checks"></a>Vėlesnių čekių nustatymas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nurodyti, ar registruoti žurnalo įrašus postduotims čekiams ir kurie registravimo žurnalai bus naudojami tarpuskaitos įrašams ir tiekėjo mokėjimams. Taip pat galite nurodyti išrašytų čekių, gautų čekių ir išskaitomo mokesčio tarpuskaitos sąskaitas. Vėlesni čekiai, išrašomi norint atlikti ir gauti mokėjimus ateityje. Galite nurodyti, ar čekis turi būti rodomas apskaitos knygose prieš mokėjimo termino datą.



Šios procedūros vaidmuo yra Iždininkas. Šioje procedūroje naudojama demonstracinė įmonė USMF.


## <a name="set-up-postdated-checks"></a>Vėlesnių čekių nustatymas
1. Pereikite į **grynųjų pinigų ir banko valdymo > nustatykite > grynųjų pinigų ir banko valdymo parametrus**.
2. Spustelėkite skirtuką **Užregistruoti čekiai**.
3. Pažymėkite arba išvalykite žymės **langelį Įgalinti pasenusius** čekius.
4. Pažymėkite arba išvalykite žymės **langelį Registruoti žurnalo įrašus užregistruoti užregistruoti čekius**.
5. Išrašytų **čekių tarpuskaitos sąskaitoje** nurodykite norimas vertes.
6. Lauke Gautų **čekių tarpuskaitos sąskaitoje** nurodykite norimas vertes.
7. Kliringo **įrašų lauke bendrajame** žurnale įveskite vertę.
8. Į šį **tiekėjo mokėjimų žurnalo lauką perkelti pasenusius čekius** įveskite vertę.
9. Lauke Išskaitomo **mokesčio tarpuskaitos sąskaita** nurodykite norimas vertes.
10. Spustelėkite **Įrašyti**.
11. Uždarykite puslapį.
12. Pereikite į **mokėtinų sumų > mokėjimo > metodus**.
13. Spustelėkite **Naujas**.
14. Lauke **Mokėjimo būdas** įveskite reikšmę.
15. Norėdami nurodyti **, kad čekio suma užregistruota** tarpuskaitos sąskaitoje, pasirinkite postduoto čekio tarpuskaitos registravimo pasirinktį.
16. Lauke Sąskaitos **tipas** pasirinkite **Bankas**.
    * Mokėjimo metodo korespondentinė sąskaita bus bankas.  
17. **Lauke Mokėjimo sąskaita** nurodykite norimas vertes.
    * Pasirinkite banko sąskaitą, naudojamą atskaityti SF sumai.  
18. Spustelėkite **Įrašyti**.
19. Uždarykite puslapį.
> [!NOTE]
> Norėdami banko sąskaitoje užregistruoti naują čekią, kai seanso data vėlesnė arba lygi mokėjimo termino datai, turite įgalinti mokėjimo žurnalo registravimo su vėlesnėmis čekiais į banko **sąskaitą priemonės mokėjimo termino datos tikrinimą**. Ši funkcija leidžia registruoti tiekėjų arba klientų mokėjimų žurnalus su vėlesnėis čekiais, kai seanso data yra vėlesnė negu mokėjimo termino data arba tokia pat.
> 
> Nustatydami mokėjimo **būdą** (mokėtinų **sumų > mokėjimo >** Mokėjimo būdai), **neužpildkite tarpinės sąskaitos**. Šiuo atveju, korespondentinė sąskaita užpildoma banko sąskaita, kuri nustatoma **mokėjimo metode**.
>  
> Įgalinus priemonę, o seanso data yra mažesnė nei mokėjimo termino data, registruojant mokėjimų žurnalą rodomas šis klaidos pranešimas, **pagal kurį mokėjimo termino data turi būti mažesnė už seanso datą arba tokia pat, jei korespondentinės sąskaitos tipas yra Bankas**. Jei priemonė neįgalinta, galite užregistruoti mokėjimo žurnalą su postduotu čekiu, kai seanso data yra mažesnė nei mokėjimo termino data.
> Ši funkcija pasiekiama 10.0.21 arba vėlesnėje versijoje.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
