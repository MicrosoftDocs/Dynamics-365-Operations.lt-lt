---
title: Vėlesnių čekių nustatymas
description: Šioje temoje paaiškinama, kaip nurodyti, ar registruoti vėlesnių čekių žurnalo įrašus ir kuriuos registravimo žurnalus naudoti su tarpuskaitos įrašais bei tiekėjo mokėjimais.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 645b474b8b4bd13cd47bef404cda002e6b29a1ba
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724848"
---
# <a name="set-up-postdated-checks"></a>Vėlesnių čekių nustatymas

[!include [banner](../../includes/banner.md)]

Šioje temoje paaiškinama, kaip nurodyti, ar registruoti vėlesnių čekių žurnalo įrašus ir kuriuos registravimo žurnalus naudoti su tarpuskaitos įrašais bei tiekėjo mokėjimais. Taip pat galite nurodyti išrašytų čekių, gautų čekių ir išskaitomo mokesčio tarpuskaitos sąskaitas. Vėlesni čekiai, išrašomi norint atlikti ir gauti mokėjimus ateityje. Galite nurodyti, ar čekis turi būti rodomas apskaitos knygose prieš mokėjimo termino datą.



Šios procedūros vaidmuo yra Iždininkas. Šioje procedūroje naudojama demonstracinė įmonė USMF.


## <a name="set-up-postdated-checks"></a>Vėlesnių čekių nustatymas
1. Pasirinkite Grynųjų pinigų ir banko valdymas > Nustatymas > Grynųjų pinigų ir banko valdymo parametrai.
2. Spustelėkite skirtuką Vėlesni čekiai.
3. Pažymėkite arba išvalykite žymės langelį Įjungti vėlesnius čekius.
4. Pažymėkite arba išvalykite žymės langelį Registruoti vėlesnių čekių žurnalo įrašus.
5. Lauke Išrašytų čekių atsiskaitymo sąskaita nurodykite norimas vertes.
6. Lauke Gautų čekių atsiskaitymo sąskaita nurodykite norimas vertes.
7. Lauke Atsiskaitymo įrašų bendrasis žurnalas įveskite vertę.
8. Lauke Perkelti vėlesnius čekius į šio tiekėjo mokėjimų žurnalą įveskite vertę.
9. Lauke Išskaitomo mokesčio atsiskaitymo sąskaita nurodykite norimas vertes.
10. Spustelėkite Įrašyti.
11. Uždarykite puslapį.
12. Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo būdai.
13. Spustelėkite Naujas.
14. Lauke Mokėjimo būdas surinkite reikšmę.
15. Pažymėkite parinktį Vėlesnių čekių atsiskaitymo registravimas, jei norite nurodyti, kad čekio suma užregistruota atsiskaitymo sąskaitoje.
16. Lauke Kliento sąskaita pasirinkite „Bankas‟.
    * Mokėjimo metodo korespondentinė sąskaita bus bankas.  
17. Lauke Mokėjimo sąskaita nurodykite norimas reikšmes.
    * Pasirinkite banko sąskaitą, naudojamą atskaityti SF sumai.  
18. Spustelėkite Įrašyti.
19. Uždarykite puslapį.
> [!NOTE]
> Norėdami banko sąskaitoje užregistruoti naują čekią, kai seanso data vėlesnė arba lygi mokėjimo termino datai, turite įgalinti mokėjimo žurnalo registravimo su vėlesnėmis čekiais į banko **sąskaitą priemonės mokėjimo termino datos tikrinimą**. Ši funkcija leidžia registruoti tiekėjų arba klientų mokėjimų žurnalus su vėlesnėis čekiais, kai seanso data yra vėlesnė negu mokėjimo termino data arba tokia pat.
> 
> Nustatydami **mokėjimo būdą** (**Mokėtinos sumos > Mokėjimo nustatymas > Mokėjimo būdai**), tarpinės **sąskaitos užpildyti** nereikia. Šiuo atveju, korespondentinė sąskaita užpildoma banko sąskaita, kuri nustatoma **mokėjimo metode**.
>  
> Kai priemonė įgalinta, o seanso data yra mažesnė nei mokėjimo termino data, registruojant mokėjimų žurnalą rodomas šis klaidos pranešimas: "Mokėjimo termino data turi būti mažesnė už seanso datą arba tokia pat, jei korespondentinės sąskaitos tipas yra Bankas". Jei priemonė neįgalinta, galite užregistruoti mokėjimo žurnalą su postduotu čekiu, kai seanso data yra mažesnė nei mokėjimo termino data.
> Ši funkcija pasiekiama 10.0.21 arba vėlesnėje versijoje.    

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
