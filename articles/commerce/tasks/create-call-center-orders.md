---
title: Skambučių centro užsakymų kūrimas
description: Šis straipsnis rodo pavyzdį, kaip skambučių centro vartotojas ieško kliento, sukuria naują užsakymą, ieško produkto ir renka mokėjimą iš kliento Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16d483896ce131e9a7bc60ab5ea7b8fa01a3bea8
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228516"
---
# <a name="create-call-center-orders"></a>Skambučių centro užsakymų kūrimas

[!include [banner](../includes/banner.md)]

Šis straipsnis rodo pavyzdį, kaip skambučių centro vartotojas ieško kliento, sukuria naują užsakymą, ieško produkto ir renka mokėjimą iš kliento Microsoft Dynamics 365 Commerce. Procedūros metu naudojama US YRA demonstracinių duomenų įmonė ir ji skirta pardavimo užsakymo klerkas. 

## <a name="prerequisites"></a>Būtinieji komponentai

Procedūrą pabaigęs vartotojas turi būti nustatytas kaip skambučių centro vartotojas. Pasirinktinai Fabrikam pusmetinį katalogą galima publikuoti su bent vienu šaltinio kodu.

### <a name="add-yourself-as-a-call-center-user"></a>Pridėti save kaip skambučių centro vartotoją

Norėdami save pridėti kaip skambučių centro vartotoją, atlikite šiuos veiksmus.

1. "Commerce Headquarters" eikite į mažmeninės **prekybos ir komercijos \> kanalų \> skambučių \> centrus Visi skambučių centrai**.
1. Lauke Vartotojai **pasirinkite** Kanalo **vartotojai**.
1. Veiksmų srityje pasirinkite **Naujas**.
1. Lauke Vartotojo **ID** įveskite savo vartotojo ID.
1. **Lauke Pavadinimas** įveskite savo vartotojo vardą. Vartotojo vardas gali būti toks pat kaip vartotojo ID.
1. Veiksmų srityje pasirinkite **Įrašyti**.
1. Grįžkite į **mažmeninės prekybos ir komercijos \> kanalų \> skambučių centrus \> Visi skambučių centrai**.
1. Pasirinkite skambučių centro mažmeninės prekybos kanalo ID.
1. Patvirtinkite, kad **parinktis Įgalinti užsakymo** baigimą nustatyta kaip **Taip**. Jei pasirinktis nematoma, šį veiksmą galite praleisti.

## <a name="complete-the-example-call-center-procedure"></a>Užbaigti skambučių centro procedūros pavyzdį

Norėdami užbaigti skambučių centro procedūros pavyzdį, atlikite šiuos žingsnius.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Klientai \> Klientų aptarnavimas**.
1. Skirtuke **Kliento** ieška įveskite ieškos kriterijus, pagal kuriuos norite ieškoti kliento. Kaip pavyzdį įveskite **Karen**.
1. Pasirinkite **Ieškoti**. Atsiranda **kliento ieškos** dialogo langas ir pateikiami ieškos rezultatai.
1. Pasirinkite Kliento įrašą, kuriam **karen Turi** būti **2001** m. kliento kodas, tada pasirinkite **Pasirinkti**.
1. Veiksmų srityje pasirinkite Naujas **pardavimo užsakymas**.
1. Dešinėje pasirinkite skirtuką **Antraštė**.
1. Pristatymo "**FastTab**", pristatymo **būdo lauke**, pasirinkite **99 standartą**.

    ![Pristatymo būdo pasirinkimas.](../media/Select_Mode_of_Delivery.png)

1. Dešinėje pasirinkite skirtuką **Eilutės**.
1. Pardavimo užsakymo **eilučių** skyriuje, naujoje naujos pardavimo eilutės eilutėje, **lauke** Prekės numeris įveskite prekės, kurios norite ieškoti, numerį. Kaip šiame pavyzdyje procedūrą įveskite **81327**, tada išplečiamajame sąraše pasirinkite produktą, kad jį pridėtumėte prie pardavimo užsakymo.
1. **Lauke Kiekis** įveskite pardavimo kiekį.
1. **Lauke Šaltinio kodas** pasirinkite katalogo šaltinio kodą. Jei aktyvių šaltinio kodų nėra, šį veiksmą galite praleisti.
1. Veiksmų srityje pasirinkite Baigti **, kad būtų** fiksuojatas kliento mokėjimas. Šiuo veiksmu atidaromas **pardavimo užsakymo** suvestinės dialogo langas, kuriame rodoma bendra mokėtina suma. Veiksmas taip pat suaktyvina visų išlaidų, pvz., siuntimo ir tvarkymo, skaičiavimą ir rodo juos **pardavimo užsakymo suvestinės dialogo** lange.

    ![Užbaigti mygtuką.](../media/Complete_button.png)

1. Dialogo lango **Pardavimo užsakymo suvestinė** mokėjimų **·** "FastTab" pasirinkite Įtraukti **, kad būtų** fiksuojami mokėjimai.

    ![Pardavimo užsakymo suvestinės dialogo langas.](../media/order_summary.png)

1. **Lauke Mokėjimo būdas pasirinkite** mokėjimo būdą, kurį **rasite dialogo lange** Įvesti kliento mokėjimo informaciją. Šiame pavyzdyje atlikti pasirinkite Grynieji **pinigai**.
1. **Mokėjimo sumos lauke** įveskite mokėjimo sumą. Šiame pavyzdyje įveskite **120,00**, lygų užsakymo balansui, **kuris rodomas pardavimo užsakymo suvestinės** dialogo lange. Įvesdami šią sumą, galite užpildyti užsakymą kaip visiškai apmokėtą.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Pateikti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tinkinti perlaidų el. paštus pagal pristatymo būdą](../customize-email-delivery-mode.md)

[Pristatymo režimo keitimas EKA](../pos-change-delivery-mode.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
