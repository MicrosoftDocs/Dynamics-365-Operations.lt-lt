---
title: Mokėjimo būdai skambučių centruose
description: Šioje temoje aprašomi įvairūs mokėjimo būdai, kuriuos galite naudoti „Dynamics 365 Commerce“ skambučių centre.
author: josaw1
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: e7636f5c664634c680edf2ff9d8bae5ebb9035af
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414362"
---
# <a name="payment-methods-in-call-centers"></a>Mokėjimo būdai skambučių centruose

[!include [banner](includes/banner.md)]

„Dynamics 365 Commerce“ skambučių centro kanalo konfigūracija apima nustatymą, pavadintą **Įgalinti užsakymo baigimą**. Šis nustatymas padeda užtikrinti, kad būtų išleisti visi kanalo vartotojų sukurti užsakymai, kad būtų galima užsakyti apdorojimą tik tuo atveju, jeigu juose nurodytas iš anksto apmokėtas arba iš anksto įgaliotas mokėjimas, kurio sumos patvirtintų nuokrypių ribose. Jei nustatymas **Įgalinti užsakymo baigimą** įjungtas, naudodamiesi skambučių centro mokėjimo apdorojimo funkcijomis skambučių centro vartotojai gali įvesti klientų pardavimo užsakymų mokėjimus. Jei nustatymas išjungtas, skambučių centro vartotojai skambučių centro mokėjimo apdorojimo funkcijomis naudotis negali, tačiau naudodamiesi standartine funkcija Gautinos sumos jie vis tiek gali pardavimo užsakymams taikyti išankstinius mokėjimus.

Atlikdama kanalo konfigūraciją įmonė gali nurodyti leistinus skambučių centro kanalo mokėjimo būdus. Skambučių centro kanalas naudoja tuos pačius mokėjimo būdus, kurie nurodyti kaip tinkami parduotuvės kanalams.

Norėdami sukonfigūruoti skambučių centro kanalo mokėjimo būdus, eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalai** \> **Skambučių centrai** \> **Visi skambučių centrai**, po to meniu **Sąranka** pasirinkite parinktį **Mokėjimo būdai**.

Sukūrę mokėjimo būdą jam galite priskirti penkias mokėjimo būdo funkcijas.

| Funkcija            | aprašymas |
|---------------------|-------------|
| Įprastas              | Mokėjimo būdo funkciją **Įprastas** naudokite kaip mokėjimo būdą nurodydami atsiskaitymą grynaisiais arba kvitais. Kai šių tipų mokėjimai taikomi pardavimo užsakymui skambučių centre, pagal numatytuosius parametrus bus nustatyta žymės **Išankstinis mokėjimas** reikšmė **Taip**. Kliento sąskaitoje iš karto užregistruojamas išankstinio apmokėjimo kvitas, kai šis užsakymas pateikiamas. Jei reikia, vartotojai gali pakeisti žymės **Išankstinis mokėjimas** reikšmę į **Ne**, kad mokėjimo kvitas nebūtų kuriamas, kol neužregistruota sąskaita faktūra. Išankstinio mokėjimo kvitas užregistruojamas kliento operacijų retrospektyvoje, kur jis bus sistemingai padengtas pagal pardavimo užsakymo sąskaitą faktūrą. |
| Tikrinti               | Jei kaip mokėjimo formą nurodote atsiskaitymą banko čekiu, naudokite funkciją **Čekis**. Kai pardavimo užsakymui taikomas šis mokėjimo tipas, tam, kad būtų galima apdoroti taikomą mokėjimą, vartotojas turi įvesti kliento čekio numerį. Mokėjimai čekiais visada traktuojami kaip išankstiniai mokėjimai ir mokėjimo kvitai sukuriami iškart, kai pateikiamas užsakymas. Šie išankstinio mokėjimo kvitai sistemingai padengiami pagal sukurtas užsakymo sąskaitas faktūras. |
| Kortelės               | Mokėjimo kortele tipai atitinka bet kokio tipo mokėjimą, kai reikalaujama įvesti ant kliento mokėjimo kortelės nurodytą kortelės numerį. Pavyzdžiui, kai mokama kredito kortelėmis ir dovanų kortelėmis. Konfigūruodami šių tipų mokėjimus naudodamiesi meniu **Kortelės sąranka** turite būtinai nurodyti su šiuo mokėjimo būdu susietų kortelių ID. Įvesdami užsakymą naudodamiesi mokėjimo įvedimo puslapyje rodoma parinktimi **Išankstinis mokėjimas** vartotojai gali nurodyti, ar mokėjimas kortele bus išankstinis. Išskyrus tuos atvejus, kai reikalaujama išankstinių mokėjimų, įprastas atsiskaitymas kredito kortele yra dviejų veiksmų procesas, kai autorizacija suteikiama įvedant užsakymą, po to padengiamas mokėjimas ir išrašant sąskaitą faktūrą iš kliento kortelės nuskaitomi pinigai. Atsiskaitant dovanų kortelėmis rekomenduojamas išankstinis apmokėjimas, nes dovanų kortelės balansas turi sumažėti iš karto, kad klientas negalėtų taikyti tos pačios vertės kitur. |
| Klientas            | Naudojantis mokėjimo būdo funkcija **Klientas** mokėjimas taikomas kliento kredito limitui arba suma įrašoma „į sąskaitą“. Srities Prekyba klientui priskirtą kredito limitą galima patikrinti įvedant užsakymą. Kai atliekant mokėjimus naudojamasi su funkcija **Klientas** susietu mokėjimo būdu, sukuriamas kliento sąskaitos įsipareigojimas. Po to, kai išrašoma pardavimo užsakymo sąskaita faktūra, rodomas skolos likutis. Tokiais atvejais klientai paprastai atsiunčia mokėjimą pagal nurodytas sąlygas. Arba norint padengti likusią skolą gali būti naudojamasi pirmiau atidarytu kliento sąskaitos kredito kvitu. Atkreipkite dėmesį, kad net ir nurodžius šį mokėjimo būdą jis nerodomas tarp skambučių centro užsakymo įvedimo mokėjimo pasirinkimo parinkčių, išskyrus atvejus, kai nustatoma kliento, su kuriuo dirbate, įrašo žymė **Leisti pateikti užsakymą pagal laisvos formos sąskaitą**. Ši žymė matoma kliento įrašo skirtuke **Numatytieji mokėjimo nustatymai**. |
| Mokėjimo priemonės šalinimas / nefiksavimas | Skambučių centras funkcija **Mokėjimo priemonės šalinimas / nefiksavimas** nesinaudoja. Ji taikoma tik nurodžius elektroninio kasos aparato (EKA) programos parduotuvės kanale naudojamus mokėjimo būdus. |

Nurodžius mokėjimo būdus juos reikėtų susieti su didžiąja knyga arba banko sąskaita. Jei praleisite šį veiksmą, vartotojams bandant išsaugoti mokėjimo tipą bus rodomos klaidos.

## <a name="refund-payment-methods"></a>Grąžinimo mokėjimo būdai

Pagal grąžinimo apdorojimo scenarijus skambučių centras taip pat naudoja kai kuriuos srityje Gautinos sumos nurodytus mokėjimo būdus. Norėdami sukonfigūruoti šiuos mokėjimo būdus, eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalo sąranka** \> **Skambučių centro sąranka** \> **Skambučių centro grąžinimo būdai**. Norėdami apdoroti klientų grąžinimo čekius, turite užbaigti šią konfigūraciją. Pvz., jei klientas iš pradžių apmokėjo užsakymą grynaisiais arba čekiu, gali būti, kad srityje Gautinos sumos vartotojas norės išsiųsti klientui grąžinimo čekį. Tokiu atveju skambučių centro grynųjų pinigų ir čekio mokėjimo tipai turi būti susieti su tinkamu srities Gautinos sumos mokėjimo būdu, kad būtų galima užtikrinti tinkamą grąžinimo apdorojimą.

Be to, jei vartotojas grąžinimo užsakymą apdoroja kaip srities Prekyba skambučių centro vartotojas, bet negali susieti grąžinimo su pradiniu pardavimu, skambučių centro parametruose turi būti nurodomas mokėjimo būdas **Grąžinimas**. Eikite į **Mažmeninė prekyba ir prekyba** \> **Kanalo sąranka** \> **Skambučių centro sąranka** \> **Skambučių centro parametrai**, o po to įsitikinkite, kad lauko **Mokėjimo būdas** skirtuke **RMA / grąžinimas** nurodytas mokėjimo būdas. Mokėjimo būdas – tai grąžinimams taikomas mokėjimo būdas. Paprastai jis nurodomas kaip čekio būdas arba kliento sąskaitos būdas.
