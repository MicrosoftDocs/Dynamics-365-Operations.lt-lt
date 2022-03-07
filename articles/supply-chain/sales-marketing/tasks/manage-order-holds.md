---
title: Valdyti užsakymų sulaikymą
description: Šioje procedūroje parodoma, kaip sulaikyti kliento pardavimo užsakymus, kaip dirbti su užsakymo sulaikymo išregistravimu ir kaip pašalinti užsakymų sulaikymą.
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0a6acbc55a69f854463e72391fb0fff4dfb459c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817730"
---
# <a name="manage-order-holds"></a>Valdyti užsakymų sulaikymą

[!include [banner](../../includes/banner.md)]

Šioje procedūroje parodoma, kaip sulaikyti kliento pardavimo užsakymus, kaip dirbti su užsakymo sulaikymo išregistravimu ir kaip pašalinti užsakymų sulaikymą. Užsakymas gali būti sulaikytas dėl įvairių priežasčių. Pavyzdžiui, galima sulaikyti užsakymą, kol bus patikrintas kliento adresas ar mokėjimo būdas arba kol vadybininkas peržiūrės kliento kredito limitą. Kai užsakymas sulaikytas, negalima apdoroti siųstinų prekių. 

Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.


## <a name="set-up-order-holds"></a>Nustatyti užsakymų sulaikymą
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Sąranka > Pardavimo užsakymai > Užsakymo sulaikymo kodai**.
2. Spustelėkite **Naujas**.
3. Lauke **Sulaikymo kodas** įveskite reikšmę. Pavyzdžiui, įveskite „Perskambinti“.  
4. Lauke **Aprašo laukas** surinkite reikšmę.
    - Pavyzdžiui, užsakymas sulaikomas, nes laukiama kliento perskambinimo.  
    - Norėdami iš užsakymo pašalinti visus faktinius rezervavimus, kai pridėtas šis sulaikymo kodas, pasirinktinai pažymėkite žymės langelį **Pašalinti rezervavimus**.  
5. Spustelėkite **Įrašyti**.

## <a name="place-order-on-hold"></a>Sulaikyti užsakymą
1. Eikite į **Naršymo sritis > Moduliai > Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai**.
2. Spustelėkite **Naujas**.
3. Lauke **Kliento sąskaita** įveskite arba pasirinkite reikšmę.
4. Spustelėkite **Gerai**.
5. Lauke **Prekės numeris** įveskite arba pasirinkite reikšmę.
6. Lauke **Kiekis** įveskite skaičių.
7. **Veiksmų srityje** spustelėkite **Pardavimo užsakymas**.
8. Spustelėkite **Užsakymų sulaikymas**.
9. Spustelėkite **Naujas**.
10. Lauke **Sulaikymo kodas** pasirinkite kodą, kurį sukūrėte ankstesnėje papildomoje užduotyje.
11. Spustelėkite **Įrašyti**.
12. Uždarykite puslapį.
13. Eikite į **Pardavimas ir rinkodara > Pardavimo užsakymai > Visi pardavimo užsakymai**.
14. Sąraše pažymėkite pasirinktą eilutę. Šiuo metu sulaikytų užsakymų laukai „Neapdoroti” ir „Sulaikyta” yra pažymėti.
15. Veiksmų srityje spustelėkite **Paimti ir pakuoti**.

## <a name="manage-order-holds"></a>Valdyti užsakymų sulaikymą
1. Eikite į **Pardavimas ir rinkodara > Pardavimo užsakymai > Atviri užsakymai > Užsakymų sulaikymas**. Puslapis **Užsakymų sulaikymas** veikia kaip darbastalis, kuriame galima peržiūrėti ir tvarkyti visus dabartinius ir apdorotus sulaikymus bei susijusius pardavimo užsakymus.     
2. Sąraše pažymėkite pasirinktą eilutę.
3. **Veiksmų srityje** spustelėkite **Sulaikyti pirkimo užbaigimą**.
4. Spustelėkite **Išregistruoti**.
5. Sąraše atžymėkite pasirinktą eilutę. Lauke **Išregistruoti** dabar rodomas jūsų vartotojo ID.   
6. Spustelėkite **Valyti išregistravimą**.
7. **Veiksmų srityje** spustelėkite **Išvalyti sulaikymą**.
    - Turite išvalyti sulaikymą, kai būsite pasirengę jį pašalinti ir leisite tęsti kitą užsakymo vykdymo veiksmą. Jei užsakymui nereikia jokių pakeitimų, galite vykdyti veiksmą Išvalyti sulaikymą. Tačiau galite naudoti veiksmą Valyti ir modifikuoti, jei išvalius sulaikymą reikia atnaujinti užsakymą.      
    - Veiksmas **Valyti ir pateikti** taikomas tik naudojant skambučių centro funkcijas.  
8. Spustelėkite **Išvalyti sulaikymą**. Sulaikymas dabar išvalytas iš užsakymo ir pašalintas iš aktyvių sulaikymų sąrašo. Norėdami peržiūrėti visus sulaikymus arba jų subrinkinį pagal konkrečią būseną, pakeiskite lauko Rodyti reikšmę.     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]