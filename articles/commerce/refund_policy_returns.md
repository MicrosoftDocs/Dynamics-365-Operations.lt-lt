---
title: Kanalo prekių ir pinigų grąžinimų strategijos kūrimas ir naujinimas
description: Šiame straipsnyje paaiškinama, kaip nustatyti kanalo grąžinimo ir grąžinimo strategiją.
author: ShalabhjainMSFT
ms.date: 07/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.custom: ''
ms.search.industry: Retail
ms.openlocfilehash: d01ad490301dd2f4103b8bd3f702db12b93a45a8
ms.sourcegitcommit: bd7b1ffe90b25eb4c68d6aaebd063bf33e09d9cd
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/05/2022
ms.locfileid: "9627502"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Kanalo prekių ir pinigų grąžinimų strategijos kūrimas ir naujinimas

[!include [banner](includes/banner.md)]

Kanalo grąžinimo politika, esanti „Dynamics 365 Commerce“, suteikia galimybę mažmenininkams nustatyti vykdymo principus, pagal kuriuos gali būti leidžiama priimti grąžinimus elektroninio kasos aparato (EKA) įrenginyje.  

Šiame straipsnyje aprašomi kanalo grąžinimo ir grąžinimo strategijos nustatyti veiksmai.

Politikos taikymo sritis šiuo metu apsiriboja mokėjimo būdų, kurias galima leisti kanalui, nustatymu. „Leidžiamų“ mokėjimo būdų sąrašas yra pagrįstas mokėjimo būdais, naudojamais įsigyjant prekes. Pavyzdys:

- Jei už prekes buvo sumokėta naudojant dovanų kortelę, parduotuvės politika yra grąžinti pinigus į naują dovanų kortelę arba išrašyti sąskaitą. 
- Jei už prekes buvo sumokėta grynaisiais pinigais, galima grąžinti grynuosius pinigus, grąžinti pinigus į dovanų kortelę arba į kliento sąskaitą, bet ne į kredito kortelę. 

## <a name="enable-return-policy"></a>Grąžinimo politikos įgalinimas

Ši funkcija išjungta pagal nutylėjimą. Galite jį rasti funkcijų valdymo darbo **srityje** funkcijų pavadinimų **sąraše ieškodami Įgalinti** kanalo grąžinimo strategijas.


## <a name="configure-return-policy"></a>Grąžinimo politikos sukonfigūravimas

Norėdami sukonfigūruoti mažmeninės parduotuvės ar internetinės mažmeninės prekybos parduotuvės kanalo grąžinimo politiką, atlikite toliau nurodytus veiksmus.

1. Eikite į **„Retail and Commerce“** \> **Kanalo sąranka** \> **Grąžinimai** \> **Kanalo grąžinimo politika**.

1. Norėdami sukurti naują grąžinimo politikos šabloną, pasirinkite **Naujas**. Norėdami naudoti esamą šabloną, pasirinkite šabloną kairiojoje srityje. Jei norite kurti naujus šablonus, pridėkite pavadinimą ir aprašą, kurie padės nustatyti politiką, kai ji taikoma kanalui.

   ![Pridėti naują grąžinimo politiką.](media/Return-policy-page1.png)
     
   
1. Skyriuje **„Leistini grąžinimo įmokos būdai“** apibrėžkite **Leistini** grąžinimo įmokų mokėjimo priemones, būdingas kiekvienam mokėjimo būdui.
   ![Leidžiamų mokėjimo būdų nustatymas kiekvienam mokėjimo tipui.](media/Return-policy-page2.png)
   
    > [!IMPORTANT]
    > - Mokėjimo būdai sukuriami iš organizacijai nustatytų mokėjimo būdų.
    > - Pridėję leistiną grąžinimo mokėjimo būdo tipą kiekvienam nurodytam mokėjimo būdui, užtikrinsite, kad bus galima grąžinti leidžiamu grąžinimo būdu.
    
1. Susiekite grąžinimo politikos šabloną su parduotuvėmis, kuriose jis bus naudojamas. Skirtuke **Mažmeninės prekybos kanalai** pasirinkite **Pridėti** ir susiekite galimus kanalus. 

    - Dialogo lange **Pasirinkti organizacijos mazgus** pasirinkite parduotuves, regionus ir organizacijas, su kuriomis turėtų būti susietas šablonas.
    - Su kiekviena parduotuve galima susieti tik vieną grąžinimo politikos šabloną.
    - Pasirinkite parduotuves, regionus ar organizacijas naudodami rodyklių mygtukus.
    - Politikos įsigaliojimo data bus ta diena, kai politika bus taikoma kanalams ir bus vykdomos kanalo užduotys. 

    ![Pasirinkti organizacijos mazgų dialogo langą.](media/Return-policy-page3.png)

1. Puslapyje **Pasiskirstymo grafikas** paleiskite **1070** užduotį, kad kanalo grąžinimo politika būtų prieinama EKA.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Peržiūrėkite kanalo grąžinimo politiką, esančią EKA

Jei norite pamatyti leistinus grąžinimo mokėjimo būdus, esančius EKA, atlikite veiksmus, pateiktus bet kuriame iš toliau nurodytų pavyzdžių.

1. Prisijunkite prie EKA kaip kasininkas ar vadovas.
1. Skyriuje **Pamaina ir stalčius** pasirinkite **Rodyti žurnalą**.
1. Pasirinkite operaciją, kuri yra grąžinimo dalis. 
1. Pasirinkite prekes, kurias norite grąžinti, ir pasirinkite mokėjimo būdą.  
    - Jei pasirinktas mokėjimo būdas yra leidžiamų grąžinti būdų tipų sąraše, kasininkas gali atlikti grąžinimą.
    - Jei pasirinktas mokėjimo būdas neleidžiamas, rodomas klaidos pranešimas.
    - Pasirinkite **Atlikti mokėjimą**, kad būtų parodytas visų leidžiamų grąžinimo būdų tipų sąrašas.

Arba

1. Prisijunkite prie EKA kaip kasininkas ar vadovas.
1. Pasirinkite **Grąžinimas** ir įveskite kvito ID, nuskaitydami brūkšninį kodą arba įvesdami jį rankiniu būdu. 
1. Pasirinkite operaciją, kuri yra grąžinimo dalis. 
1. Pasirinkite prekes, kurias norite grąžinti, ir pasirinkite mokėjimo būdą.  
    - Jei pasirinktas mokėjimo būdas yra leidžiamų grąžinti būdų tipų sąraše, kasininkas gali atlikti grąžinimą.
    - Jei pasirinktas mokėjimo būdas neleidžiamas, rodomas klaidos pranešimas.
    - Pasirinkite **Atlikti mokėjimą**, kad būtų parodytas visų leidžiamų grąžinimo būdų tipų sąrašas.

![Blogas grąžinimo tipas.](media/Return-policy-page6.png)



![Galimi grąžinimo tipai.](media/Return-policy-page5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
