---
title: Tęstinumo programos naudojimas
description: Šioje procedūroje parodoma, kaip parduoti tęstinumo programą ir apdoroti susijusius pardavimo užsakymus.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
ms.openlocfilehash: 3736984a336b35b23b7060b2d98770912cc9ec6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267410"
---
# <a name="using-continuity-program"></a>Tęstinumo programos naudojimas

[!include [banner](../includes/banner.md)]

Šioje procedūroje parodoma, kaip parduoti tęstinumo programą ir apdoroti susijusius pardavimo užsakymus. Norint atlikti šią procedūrą, vartotojas turi būti nustatytas kaip skambučių centro vartotojas. Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT.

1. Eikite į Mažmeninė prekyba ir prekyba > Klientai > Klientų aptarnavimas.
2. Lauke Ieškos tekstas įveskite Karen ir paspauskite klavišą TAB.
    * Turėtų pasirodyti išplėstinės ieškos dialogo langas. Jei jis nepasirodo, spustelėkite parinktį Ieškoti, esančią dešinėje šio lauko pusėje.  
3. Sąraše pažymėkite pasirinktą eilutę.
    * Tik vienoje eilutėje turi būti rodoma Karen Berg. Pasirinkite eilutę spustelėdami žymės langelio stulpelyje tolimojoje kairėje tinklelio pusėje.  
4. Spustelėkite Pažymėti.
5. Spustelėkite Naujas pardavimo užsakymas.
    * Neblogai būtų įsidėmėti pardavimo užsakymo numerį. Jo prireiks vėliau šios procedūros metu.  
6. Lauke Prekės numeris įveskite 88000 ir paspauskite klavišą TAB.
    * Tai yra tęstinė prekė demonstracinių duomenų įmonėje USRT.  
7. Spustelėkite Baigti.
8. Lauke Mokėjimo būdas įveskite Visa.
9. Spustelėkite Įtraukti kredito kortelę.
    * Įveskite reikiamą kredito kortelės informaciją šiame puslapį.  
10. Spustelėkite GERAI.
11. Išplėskite skyrių „Mokėjimas“.
    * Norint pateikti skambučių centro užsakymą, turi būti įvesti užsakymo mokėjimai.  
12. Spustelėkite GERAI.
13. Spustelėkite Pateikti.
    * Sukūrėte naują tęstinumo užsakymą. Dabar reikia atlikti du paketinius procesus, kurie yra naudojami tęstinumo užsakymams apdoroti.  
14. Uždarykite puslapį.
15. Eikite į Mažmeninė prekyba ir prekyba > Tęstinumas > Apdoroti tęstinius mokėjimus.
16. Lauke Tęstinė prekė įveskite 88000 ir paspauskite klavišą TAB.
17. Spustelėkite Gerai.
18. Eikite į Mažmeninė prekyba ir prekyba > Tęstinumas > Tęstinių antrinių užsakymų kūrimas.
    * Šiuo procesu bus sukurti nauji pardavimo užsakymai pagal tęstinumo programos parametrus.  
19. Lauke Tęstinė prekė įveskite 88000 ir paspauskite klavišą TAB.
    * Prekė 88000 yra tęstinė prekė demonstracinių duomenų įmonėje USRT.  
20. Lauke Pardavimo užsakymas įveskite arba pasirinkite reikšmę.
    * Įveskite pardavimo užsakymo numerį, kurį įsidėmėjote šios procedūros metu anksčiau. Tokiu būdu šios procedūros metu apdorojimo laikas bus kiek įmanoma trumpesnis. Laukas Pardavimo užsakymo nėra būtinas – galite apdoroti visus bet kurios vienos programos užsakymus.  
21. Spustelėkite GERAI.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
