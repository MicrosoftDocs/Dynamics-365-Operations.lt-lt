---
title: Nustatyti tiekėjo mokėjimo mokesčius
description: Nustatykite tiekėjų mokėjimų mokesčius.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e9e723ec54b6f34082c422ce4c8e48bf52d2e3e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189458"
---
# <a name="define-vendor-payment-fees"></a>Nustatyti tiekėjo mokėjimo mokesčius

[!include [task guide banner](../../includes/task-guide-banner.md)]

Nustatykite tiekėjų mokėjimų mokesčius. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pasirinkite Mokėtinos sumos > Mokėjimų sąranka > Mokėjimo mokestis.
2. Spustelėkite Naujas.
3. Lauke Mokesčio ID surinkite reikšmę.
    * Mokesčio ID turėtų apibūdinti, kada šis mokestis bus naudojamas, pvz., „EFT_mokestis‟.  
4. Lauke Pavadinimas surinkite reikšmę.
5. Lauke Mokesčio aprašas surinkite reikšmę.
    * Pridėkite aprašą, kad suteiktumėte daugiau informacijos apie tai, kada mokestis taikomas.  
6. Lauke Mokestis pasirinkite Tiekėjas arba Didžioji knyga.
    * DK yra naudojama, kai mokestis priskiriamas organizacijai.  Tiekėjas naudojamas, kai mokestis taikomas tiekėjui.  
7. Įveskite pagrindinę sąskaitą, kuriai mokestis bus priskiriamas.
    * Ši parinktis galima tik tada, kai kaip parinktis Mokestis pasirenkama Didžioji knyga.  
8. Pasirinkite žurnalą, kuriame šis mokestis gali būti naudojamas. 
    * Tiekėjo mokėjimo mokesčiui reikėtų pasirinkti žurnalą „Išmoka tiekėjui‟.  
9. Spustelėkite Įrašyti.
10. Spustelėkite Mokėjimo mokesčio sąranka.
    * Pereikite prie mokėjimo mokesčio sąrankos, kad apibrėžtumėte, kada mokestis turėtų pagal numatytąsias nuostatas būti taikomas jūsų pasirinktam žurnalui.  
11. Pasirinkite Lentelė, Grupė arba Visi.
    * Lentelė naudojama norint pasirinkti vieną banko sąskaitą, Grupė naudojama norint pasirinkti bankų grupę, o Visi – šią mokesčio sąranką naudoti visoms banko sąskaitoms.  
12. Pasirinkite banko grupę arba banko sąskaitą.
    * Peržvalga rodys bankų grupę, jei pasirinkote Grupė, ir – banko sąskaitas, jei pasirinkote Lentelė.  
13. Pasirinkite mokėjimo būdą, kada šis mokestis bus taikomas.
14. Pasirinkite pasirinkto mokėjimo būdo mokėjimo specifikaciją.
    * Mokėjimo specifikacija naudojama su elektroniniais mokėjimo lėšų pervedimo būdais.  
15. Pasirinkite, ar mokestis yra procentas, suma, ar intervalas.
16. Įveskite mokesčio procentą arba sumą.
    * Jei mokestis yra procentas, įveskite tą procentą. Jei mokestis yra suma, įveskite mokesčio sumą. Jei mokestis yra intervalas, naudokite skirtuką Intervalas, kad apibrėžtumėte pakopinius mokesčius.  
17. Lauke Mokesčio valiuta pasirinkite valiutą, kuria mokestis bus taikomas.
    * Tai – mokesčio valiuta. Mokėjimo valiuta naudojama apibrėžti, kada mokesčių taisyklė turėtų būti taikoma pagal mokėjimo valiutą. Pvz., bankas gali taikyti mokestį, kai mokėjimas atliekamas eurais, tačiau visiems kitiems mokėjimams mokestis netaikomas.  
18. Spustelėkite Įrašyti.
