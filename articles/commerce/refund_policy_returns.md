---
title: Kanalo grąžinimo politikos kūrimas ir atnaujinimas
description: Šioje temoje pateikiama informacija apie tai, kaip sukonfigūruoti kanalo grąžinimo politiką.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Retail 10.0.9 update
ms.openlocfilehash: c2a9325f09ffe43c3436b7e0ca2ab511e1f57f83
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414447"
---
# <a name="create-and-update-a-returns-and-refunds-policy-for-a-channel"></a>Kanalo grąžinimo politikos kūrimas ir atnaujinimas

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Peržiūrėti

Kanalo grąžinimo politika, esanti „Dynamics 365 Commerce“, suteikia galimybę mažmenininkams nustatyti vykdymo principus, pagal kuriuos gali būti leidžiama priimti grąžinimus elektroninio kasos aparato (EKA) įrenginyje.  

Šioje temoje aprašomi kanalo grąžinimo politikos sukonfigūravimo veiksmai.

Politikos taikymo sritis šiuo metu apsiriboja mokėjimo būdų, kurias galima leisti kanalui, nustatymu. „Leidžiamų“ mokėjimo būdų sąrašas yra pagrįstas mokėjimo būdais, naudojamais įsigyjant prekes. Pavyzdys:

- Jei už prekes buvo sumokėta naudojant dovanų kortelę, parduotuvės politika yra grąžinti pinigus į naują dovanų kortelę arba išrašyti sąskaitą. 
- Jei už prekes buvo sumokėta grynaisiais pinigais, galima grąžinti grynuosius pinigus, grąžinti pinigus į dovanų kortelę arba į kliento sąskaitą, bet ne į kredito kortelę. 


## <a name="enable-return-policy"></a>Grąžinimo politikos įgalinimas

Norėdami įjungti kanalo grąžinimo politikos funkciją, atlikite toliau nurodytus veiksmus.

1. Eikite į darbo sritį **Funkcijų valdymas**, esančią „Dynamics 365 Commerce“.
2. Funkcijų pavadinimų sąraše ieškokite **Įgalinti kanalų grąžinimo politiką**.
3. Pasirinkite **Įjungti dabar**. 

## <a name="configure-return-policy"></a>Grąžinimo politikos sukonfigūravimas

Norėdami sukonfigūruoti mažmeninės parduotuvės ar internetinės mažmeninės prekybos parduotuvės kanalo grąžinimo politiką, atlikite toliau nurodytus veiksmus.

1. Eikite į **„Retail and Commerce“** \> **Kanalo sąranka** \> **Grąžinimai** \> **Kanalo grąžinimo politika**.

2. Norėdami sukurti naują grąžinimo politikos šabloną, pasirinkite **Naujas**. Norėdami naudoti esamą šabloną, pasirinkite šabloną kairiojoje srityje. Jei norite kurti naujus šablonus, pridėkite pavadinimą ir aprašą, kurie padės nustatyti politiką, kai ji taikoma kanalui.

   ![Pridėti naują grąžinimo politiką](media/Return-policy-page1.png "Pridėti naują grąžinimo politiką")
     
   
3. Skyriuje **„Leistini grąžinimo įmokos būdai“** apibrėžkite **Leistini** grąžinimo įmokų mokėjimo priemones, būdingas kiekvienam mokėjimo būdui.
   ![Pridėti mokėjimo būdą](media/Return-policy-page2.PNG "Leidžiamų mokėjimo būdų nustatymas kiekvienam mokėjimo tipui")
   
    > [!IMPORTANT]
    > - Mokėjimo būdai sukuriami iš organizacijai nustatytų mokėjimo būdų.
    > - Pridėję leistiną grąžinimo mokėjimo būdo tipą kiekvienam nurodytam mokėjimo būdui, užtikrinsite, kad bus galima grąžinti leidžiamu grąžinimo būdu.
    
4. Susiekite grąžinimo politikos šabloną su parduotuvėmis, kuriose jis bus naudojamas. Skirtuke **Mažmeninės prekybos kanalai** pasirinkite **Pridėti** ir susiekite galimus kanalus. 

    - Dialogo lange **Pasirinkti organizacijos mazgus** pasirinkite parduotuves, regionus ir organizacijas, su kuriomis turėtų būti susietas šablonas.
    - Su kiekviena parduotuve galima susieti tik vieną grąžinimo politikos šabloną.
    - Pasirinkite parduotuves, regionus ar organizacijas naudodami rodyklių mygtukus.
    - Politikos įsigaliojimo data bus ta diena, kai politika bus taikoma kanalams ir bus vykdomos kanalo užduotys. 

    ![Pasirinkti organizacijos mazgų dialogo langą](media/Return-policy-page3.PNG "Pasirinkti organizacijos mazgų dialogo langą")

5. Puslapyje **Pasiskirstymo grafikas** paleiskite **1070** užduotį, kad kanalo grąžinimo politika būtų prieinama EKA.

## <a name="preview-the-channel-return-policy-in-the-pos"></a>Peržiūrėkite kanalo grąžinimo politiką, esančią EKA

Jei norite pamatyti leistinus grąžinimo mokėjimo būdus, esančius EKA, atlikite veiksmus, pateiktus bet kuriame iš toliau nurodytų pavyzdžių.

1. Prisijunkite prie EKA kaip kasininkas ar vadovas.
2. Skyriuje **Pamaina ir stalčius** pasirinkite **Rodyti žurnalą**.
3. Pasirinkite operaciją, kuri yra grąžinimo dalis. 
4. Pasirinkite prekes, kurias norite grąžinti, ir pasirinkite mokėjimo būdą.  
- Jei pasirinktas mokėjimo būdas yra leidžiamų grąžinti būdų tipų sąraše, kasininkas gali atlikti grąžinimą.
- Jei pasirinktas mokėjimo būdas neleidžiamas, rodomas klaidos pranešimas.
- Pasirinkite **Atlikti mokėjimą**, kad būtų parodytas visų leidžiamų grąžinimo būdų tipų sąrašas.

Arba

1. Prisijunkite prie EKA kaip kasininkas ar vadovas.
2. Pasirinkite **Grąžinimas** ir įveskite kvito ID, nuskaitydami brūkšninį kodą arba įvesdami jį rankiniu būdu. 
3. Pasirinkite operaciją, kuri yra grąžinimo dalis. 
4. Pasirinkite prekes, kurias norite grąžinti, ir pasirinkite mokėjimo būdą.  
- Jei pasirinktas mokėjimo būdas yra leidžiamų grąžinti būdų tipų sąraše, kasininkas gali atlikti grąžinimą.
- Jei pasirinktas mokėjimo būdas neleidžiamas, rodomas klaidos pranešimas.
- Pasirinkite **Atlikti mokėjimą**, kad būtų parodytas visų leidžiamų grąžinimo būdų tipų sąrašas.

![Grąžinti negalima](media/Return-policy-page6.png "Blogas grąžinimo tipas")



![Mokėjimo būdų sąrašas](media/Return-policy-page5.PNG "Galimi grąžinimo tipai")


[!INCLUDE[footer-include](../includes/footer-banner.md)]