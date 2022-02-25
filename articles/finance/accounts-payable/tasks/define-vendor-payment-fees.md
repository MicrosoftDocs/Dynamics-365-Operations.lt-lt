---
title: Nustatyti tiekėjo mokėjimo mokesčius
description: Nustatykite tiekėjų mokėjimų mokesčius.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c490bb4d15fa03742b12f337046f26976ab70d29
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109836"
---
# <a name="define-vendor-payment-fees"></a>Nustatyti tiekėjo mokėjimo mokesčius

[!include [banner](../../includes/banner.md)]

Nustatykite tiekėjų mokėjimų mokesčius. Šioje užduotyje naudojama demonstracinė įmonė USMF.

1. Pereikite į **mokėtinų sumų > mokėjimo nustatymą > mokestį**.
2. Spustelėkite **Naujas**.
3. **Mokesčio ID lauke** įveskite vertę.
    * Mokesčio **ID turi** aprašyti, kada šis mokestis bus naudojamas, pvz., "EFT_Fee".  
4. Lauke **Pavadinimas** įveskite reikšmę.
5. **Mokesčio aprašymo** lauke įveskite vertę.
    * Pridėkite aprašą, kad suteiktumėte daugiau informacijos apie tai, kada mokestis taikomas.  
6. Lauke Mokestis **pasirinkite** Tiekėjas **arba** **DK**.
    * **DK** naudojama, kai mokestis bus išlaidų jūsų organizacijai. **Tiekėjas** naudojamas, kai mokestis bus vertinamas tiekėjui.  
7. Įveskite pagrindinę sąskaitą, kuriai mokestis bus priskiriamas.
    * Ši pasirinktis galima tik pasirinkus **DK** kaip parinktį **Mokestis**.  
8. Pasirinkite žurnalą, kuriame šis mokestis gali būti naudojamas. 
    * Tiekėjo mokėjimo mokesčiui reikėtų pasirinkti žurnalą „Išmoka tiekėjui‟.  
9. Spustelėkite "Save **"**.
10. Spustelėkite **Mokėjimo mokesčio sąranka**.
    * Pereikite prie mokėjimo mokesčio **nustatymo, kad** nurodytumėte, kada mokestis turi būti numatytasis jūsų pasirinktame žurnale.  
11. Pasirinkite **Lentelė**, **Grupė** arba **Viskas**.
    * **Lentelė** naudojama norint pasirinkti vieną banko sąskaitą, **grupė** naudojama bankų grupei pasirinkti, **o** visi – visoms banko sąskaitoms naudoti šį mokesčio nustatymą.  
12. Pasirinkite banko grupę arba banko sąskaitą.
    * Peržvalgoje bus rodoma banko grupė, jei pasirinkote **Grupė**, o jei pasirinkote Lentelė, bus rodomi banko **sąskaitos**.  
13. Pasirinkite mokėjimo būdą, kada šis mokestis bus taikomas.
14. **Pasirinkti pasirinkto** mokėjimo būdo mokėjimo specifikaciją.
    * Mokėjimo **specifikacija naudojama** su elektroninio lėšų pervedimo mokėjimo metodais.  
15. Pasirinkite, ar mokestis yra procentas, suma, ar intervalas.
16. Įveskite mokesčio procentą arba sumą.
    * Jei mokestis **yra** procentinė išraiška, įveskite procentus. **Jei mokestis** yra suma, įveskite mokesčio sumą. Jei mokestis **yra** intervalas, pakopiniai mokesčiai **nustatomi** naudojant skirtuką Intervalas.  
17. **Lauke Mokesčio valiuta** pasirinkite valiutą, kuria bus vertinamas mokestis.
    * Tai – mokesčio valiuta. Mokėjimo valiuta naudojama apibrėžti, kada mokesčių taisyklė turėtų būti taikoma pagal mokėjimo valiutą. Pvz., bankas gali taikyti mokestį, kai mokėjimas atliekamas eurais, tačiau visiems kitiems mokėjimams mokestis netaikomas.  
18. Spustelėkite **Įrašyti**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
