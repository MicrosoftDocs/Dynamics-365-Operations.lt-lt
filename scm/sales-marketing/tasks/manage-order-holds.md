--- 
title: "Valdyti užsakymų sulaikymą"
description: "Šioje procedūroje parodoma, kaip sulaikyti kliento pardavimo užsakymus, kaip dirbti su užsakymo sulaikymo išregistravimu ir kaip pašalinti užsakymų sulaikymą."
author: omulvad
manager: AnnBe
ms.date: 01/09/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 6a9487567620b7b7d6d15015f7f0b7675e227c8a
ms.contentlocale: lt-lt
ms.lasthandoff: 07/28/2017

---
# <a name="manage-order-holds"></a>Valdyti užsakymų sulaikymą

[!include[task guide banner](../../includes/task-guide-banner.md)]

Šioje procedūroje parodoma, kaip sulaikyti kliento pardavimo užsakymus, kaip dirbti su užsakymo sulaikymo išregistravimu ir kaip pašalinti užsakymų sulaikymą. Užsakymas gali būti sulaikytas dėl įvairių priežasčių. Pavyzdžiui, galima sulaikyti užsakymą, kol bus patikrintas kliento adresas ar mokėjimo būdas arba kol vadybininkas peržiūrės kliento kredito limitą. Kai užsakymas sulaikytas, negalima apdoroti siųstinų prekių. 

Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.


## <a name="set-up-order-holds"></a>Nustatyti užsakymų sulaikymą
1. Pasirinkite Pardavimas ir rinkodara > Sąranka > Pardavimo užsakymai > Užsakymo sulaikymo kodai.
2. Spustelėkite Naujas.
3. Lauke Sulaikymo kodas surinkite reikšmę.
    * Pavyzdžiui, surinkite Perskambinti.  
4. Lauke Aprašas įveskite reikšmę.
    * Pavyzdžiui, užsakymas sulaikomas, nes laukiama kliento perskambinimo.  
    * Norėdami iš užsakymo pašalinti visus faktinius rezervavimus, kai pridėtas šis sulaikymo kodas, pasirinktinai pažymėkite žymės langelį Pašalinti rezervavimus.  
5. Spustelėkite Įrašyti.

## <a name="place-order-on-hold"></a>Sulaikyti užsakymą
1. Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
4. Spustelėkite Gerai.
5. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
6. Lauke Kiekis įveskite skaičių.
7. Veiksmų srityje spustelėkite Pardavimo užsakymas.
8. Spustelėkite Užsakymų sulaikymas.
9. Spustelėkite Naujas.
10. Lauke Sulaikymo kodas pasirinkite kodą, kurį sukūrėte ankstesnėje papildomoje užduotyje.
11. Spustelėkite Įrašyti.
12. Uždarykite puslapį.
13. Eikite į Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai.
14. Sąraše pažymėkite pasirinktą eilutę.
    * Šiuo metu sulaikytų užsakymų laukai „Neapdoroti” ir „Sulaikyta” yra pažymėti.    
15. Veiksmų srityje spustelėkite Paimti ir pakuoti.

## <a name="manage-order-holds"></a>Valdyti užsakymų sulaikymą
1. Pasirinkite Pardavimas ir rinkodara > Pardavimo užsakymai > Atviri užsakymai > Užsakymų sulaikymas.
    * Užsakymų sulaikymo puslapis veikia kaip darbastalis, kuriame galima peržiūrėti ir tvarkyti visus dabartinius ir apdorotus sulaikymus bei susijusius pardavimo užsakymus.      
2. Sąraše pažymėkite pasirinktą eilutę.
3. Veiksmų srityje spustelėkite Sulaikyti pirkimo užbaigimą.
4. Spustelėkite Išregistruoti.
5. Sąraše atžymėkite pasirinktą eilutę.
    * Išregistravimo lauke dabar rodomas jūsų vartotojo ID.   
6. Spustelėkite Valyti išregistravimą.
7. Veiksmų srityje spustelėkite Išvalyti sulaikymą.
    * Turite išvalyti sulaikymą, kai būsite pasirengę jį pašalinti ir leisite tęsti kitą užsakymo vykdymo veiksmą. Jei užsakymui nereikia jokių pakeitimų, galite vykdyti veiksmą Išvalyti sulaikymą. Tačiau galite naudoti veiksmą Valyti ir modifikuoti, jei išvalius sulaikymą reikia atnaujinti užsakymą.      
    * Veiksmas Valyti ir pateikti taikomas tik naudojant skambučių centro funkcijas.  
8. Spustelėkite Išvalyti sulaikymą.
    * Sulaikymas dabar išvalytas iš užsakymo ir pašalintas iš aktyvių sulaikymų sąrašo. Norėdami peržiūrėti visus sulaikymus arba jų subrinkinį pagal konkrečią būseną, pakeiskite lauko Rodyti reikšmę.     


