---
title: Nustatyti kliento mokėjimo mokesčius
description: Sukurkite mokėjimų klientams mokesčius.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f18b88cfdeef2e66003cd4411ace4b4c49e42f6f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834444"
---
# <a name="establish-customer-payment-fees"></a>Nustatyti kliento mokėjimo mokesčius

[!include [task guide banner](../../includes/task-guide-banner.md)]

Sukurkite mokėjimų klientams mokesčius.

Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pasirinkite Gautinos sumos > Mokėjimų sąranka > Mokėjimo mokestis.
2. Spustelėkite Naujas.
3. Lauke Mokesčio ID įveskite mokesčio ID.
    * Mokesčio ID rodomas mokėjimų žurnaluose, todėl nurodykite jį aprašomąjį, kad suprastumėte, koks mokestis nustatomas.  
4. Lauke Pavadinimas įveskite mokesčio pavadinimą.
5. Lauke Mokesčio aprašas įveskite mokesčio aprašą.
6. Pasirinkite, ar mokestis bus taikomas klientui, ar DK sąskaitai.
    * Jei mokesčiu apmokestinamas klientas, pasirinkite Klientas. Jei mokesčiu, kaip išlaidomis, bus apmokestinta jūsų organizacija, pasirinkite Didžioji knyga. Šiai užduočiai atlikti pasirinkite Klientas.  
7. Pasirinkite žurnalo, kuris gali naudoti šį mokėjimo mokestį, tipą.
    * Jei šie mokesčiai naudojami klientų mokėjimams, žurnalo tipas greičiausiai bus Kliento mokėjimas.  
8. Spustelėkite Įrašyti.
9. Spustelėkite Mokėjimo mokesčio sąranka.
    * Mokėjimo mokesčio sąranka naudojama apibrėžti kriterijams, kada mokėjimo mokesčiu bus apmokestinama.  Pavyzdžiui, galite apibrėžti, kad mokestis bus skaičiuojamas, jei banko sąskaita bus USMF OPER, o mokėjimo būdas bus čekis.  
10. Pasirinkite Lentelė, Grupė arba Visos, kad apibrėžtumėte, kurioms banko sąskaitoms bus taikomas šis mokestis.
    * Jei pasirenkate Visos, šiuo mokesčiu galėtų būti apmokestintos visos banko sąskaitos.  Jei pasirenkate Lentelė, šiuo mokesčiu gali būti apmokestinta tik jūsų pasirinkta banko sąskaita. Jei pasirenkate Grupė, šiuo mokesčiu gali būti apmokestintos tik pasirinktos bankų grupės sąskaitos.  
11. Pasirinkite banko grupę arba banko sąskaitą.
    * Jei pasirinkote Lentelė, peržvalgoje bus rodomos banko sąskaitos. Jei pasirinkote Grupė, peržvalgoje bus rodomos bankų grupės.  
12. Sąraše spustelėkite saitą pasirinktoje eilutėje.
13. Pasirinkite mokėjimo būdą, kuriam šis mokestis bus taikomas.
    * Pavyzdžiui., mokesčiu galite apmokestinti savo klientus, jei jie mokėjimus siunčia kaip čekį, o ne kaip elektroninį mokėjimą.  
14. Sąraše raskite ir pasirinkite norimą įrašą.
15. Jei tai aktualu, įveskite mokėjimo valiutą.
    * Mokėjimo valiuta naudojama kaip papildomas kriterijus nustatyti, ar bus taikomas mokestis.  Pavyzdžiui, jūsų bankas gali taikyti papildomą mokestį už mokėjimus, gautus JAV doleriais, nes jie paprastai operuoja tik eurais.  
16. Pasirinkite, ar mokestis bus procentas, suma, ar intervalas.
17. Įveskite mokesčio procentą arba sumą.
    * Jei laukas Procentas / suma yra Procentas, tada čia įvesta reikšmė bus procentas. Jei laukas Procentas / suma yra Suma, tada čia jūsų įvesta reikšmė bus suma. Jei laukas Procentas / suma yra intervalas, naudokite skirtuką Intervalas, kad apibrėžtumėte pakopas.  
18. Lauke Mokesčio valiuta pasirinkite mokesčio valiutą.
    * Tai valiuta, kuria bus sukurta mokestis.  
19. Spustelėkite Įrašyti.

