--- 
title: "Nustatyti kliento mokėjimo būdą"
description: "Sukurkite mokėjimų klientams būdą."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabcfe83ac83a8210ce4e0d46a08acdc48f4bf3b
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-method-of-payment"></a>Nustatyti kliento mokėjimo būdą

[!include [task guide banner](../../includes/task-guide-banner.md)]

Sukurkite mokėjimų klientams būdą. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pasirinkite Gautinos sumos > Mokėjimų sąranka > Mokėjimo būdai.
2. Spustelėkite Naujas.
3. Lauke Mokėjimo būdas įveskite mokėjimo būdo ID.
    * Mokėjimo būdo ID rodomas SF ir mokėjimuose, todėl nurodykite jį pakankamai aprašomąjį, kad suprastumėte, kokio tipo mokėjimas registruojamas, ir kokios banko sąskaitos.  
4. Lauke Aprašas įveskite aprašą.
5. Pasirinkite, kokios reikia mokėjimo būsenos, kad būtų galima registruoti mokėjimus.
    * Kuriant kliento mokėjimą, jį registruoti galima tik kai mokėjimo būsena atitinka čia jūsų apibrėžtą mokėjimo būseną.  
6. Pasirinkite, kaip turėtų būti kuriami klientų mokėjimai už SF.
    * Ši parinktis naudojama tik vykdant mokėjimo pasiūlymą. Klientų mokėjimams mokėjimo pasiūlymas galėtų būti naudojamas atliekant tiesioginį debetą ir išimant lėšas iš klientų bankų sąskaitų.  
7. Pasirinkite mokėjimo tipą.
    * Mokėjimo tipas padės nustatyti, ar bus atliekamas koks nors mokėjimo tikrinimas, ar ne.  
8. Pasirinkite, į kokio tipo sąskaitą bus registruojami mokėjimai.
    * Paprastai šiai parinkčiai būtų pasirinkta Bankas.  
9. Pasirinkite banko sąskaitą, į kurią bus įrašytas šis mokėjimas.
10. Įveskite banko operacijų tipą, kad identifikuotumėte jūsų banko naudojamą mokėjimo tipą.
    * Bankų operacijos tipas naudojamas bankų derinimo proceso metu ir gali derinimą palengvinti.  
11. Pasirinkite, ar šis mokėjimas bus laikinai registruojamas tarpinėje sąskaitoje.
    * Jei norite išbandyti mokėjimo srauto laiką, kad jį patvirtintų bankas, naudokite funkciją Tarpin. Mokėjimas bus laikinai registruojamas DK sąskaitoje tol, kol jį patvirtins bankas, o tada mokėjimas bus perkeltas į banko sąskaitą, kurią apibrėžėte čia.  
12. Įveskite pagrindinę sąskaitą, naudojamą registruoti tarpiškai.
    * Tai yra pagrindinė sąskaita, kurioje, jei naudojama tarpinė funkcija, bus laikinai registruojamas mokėjimas.  
13. Naudokite skirtuką Failo formatas, kad apibrėžtumėte elektroninių mokėjimų nuostatą.
14. Naudokite skirtuką Mokėjimo kontrolė, kad apibrėžtumėte privalomus laukus.
    * Pavyzdžiui, jei reikia pervesti visus šiuo būdu atliktus mokėjimus, tokią parinktį galite pasirinkti šiame skirtuke.  
15. Naudokite skirtuką Mokėjimo atributai, kad apibrėžtumėte, kuriuos šio mokėjimo būdo atributus norite naudoti.
16. Spustelėkite Įrašyti.


