---
title: Kliento mokėjimo būdo nustatymas
description: Šiame straipsnyje paaiškinama, kaip sukurti mokėjimo klientams būdą.
author: ShivamPandey-msft
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3843ce596d054263b69ccc577f3885970fe49d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861508"
---
# <a name="establish-customer-method-of-payment"></a>Kliento mokėjimo būdo nustatymas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip sukurti mokėjimo klientams būdą. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Naršymo srityje eikite į **Moduliai > Gautinos sumos > Mokėjimų sąranką > Mokėjimo būdai**.
2. Pasirinkite **Naujas**.
3. Lauke **Mokėjimo būdas** įveskite mokėjimo būdo ID. Mokėjimo būdo ID rodomas SF ir mokėjimuose, todėl nurodykite jį pakankamai aprašomąjį, kad suprastumėte, kokio tipo mokėjimas registruojamas, ir kokios banko sąskaitos.  
4. Lauke **Aprašas** įveskite aprašą.
5. Pasirinkite, kokios reikia mokėjimo būsenos, kad būtų galima registruoti mokėjimus. Kuriant kliento mokėjimą, jį registruoti galima tik kai mokėjimo būsena atitinka čia jūsų apibrėžtą mokėjimo būseną.  
6. Pasirinkite, kaip turėtų būti kuriami klientų mokėjimai už SF. Ši parinktis naudojama tik vykdant mokėjimo pasiūlymą. Klientų mokėjimams mokėjimo pasiūlymas galėtų būti naudojamas atliekant tiesioginį debetą ir išimant lėšas iš klientų bankų sąskaitų.  
7. Pasirinkite mokėjimo tipą. Mokėjimo tipas padės nustatyti, ar bus atliekamas koks nors mokėjimo tikrinimas, ar ne.  
8. Pasirinkite, į kokio tipo sąskaitą bus registruojami mokėjimai. Paprastai šiai parinkčiai būtų pasirinkta Bankas.  
9. Pasirinkite banko sąskaitą, į kurią bus įrašytas šis mokėjimas.
10. Įveskite banko operacijų tipą, kad identifikuotumėte jūsų banko naudojamą mokėjimo tipą. Bankų operacijos tipas naudojamas bankų derinimo proceso metu ir gali derinimą palengvinti.  
11. Pasirinkite, ar šis mokėjimas bus laikinai registruojamas tarpinėje sąskaitoje. Jei norite išbandyti mokėjimo srauto laiką, kad jį patvirtintų bankas, naudokite funkciją Tarpin. Mokėjimas bus laikinai registruojamas DK sąskaitoje tol, kol jį patvirtins bankas, o tada mokėjimas bus perkeltas į banko sąskaitą, kurią apibrėžėte čia.  
12. Įveskite pagrindinę sąskaitą, naudojamą registruoti tarpiškai. Tai yra pagrindinė sąskaita, kurioje, jei naudojama tarpinė funkcija, bus laikinai registruojamas mokėjimas.  
13. Norėdami apibrėžti elektroninių mokėjimų parametrą, naudokite skirtuką **Failo formatas**.
14. Norėdami apibrėžti privalomus laukus, naudokite skirtuką **Mokėjimų kontrolė**. Pavyzdžiui, jei reikia pervesti visus šiuo būdu atliktus mokėjimus, tokią parinktį galite pasirinkti šiame skirtuke.  
15. Naudokite skirtuką **Mokėjimo atributai**, kad apibrėžtumėte, kuriuos šio mokėjimo būdo atributus norite naudoti.
16. Pasirinkite **Įrašyti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
