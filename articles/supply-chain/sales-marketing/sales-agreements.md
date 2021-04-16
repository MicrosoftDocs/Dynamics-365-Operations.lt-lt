---
title: Pardavimo sutarčių apžvalga
description: Šioje temoje pateikiama informacija apie pardavimo sutartis. Pardavimo sutartis yra sutartis, kuri įpareigoja klientą pirkti tam tikrą produktų kiekį per tam tikrą laiką už specialias kainas ir taikant specialias nuolaidas.
author: omulvad
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesAgreementListPage, SalesAgreementInvoiceJournal, SalesAgreementInvoicePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: 9554
ms.assetid: c5d55c8d-99f2-44f9-a897-5b0dee85fc81
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47e8dc0c3244f07d3648c10ad26a92a923d3db77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817802"
---
# <a name="sales-agreements-overview"></a>Pardavimo sutarčių apžvalga

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie pardavimo sutartis. Pardavimo sutartis yra sutartis, kuri įpareigoja klientą pirkti tam tikrą produktų kiekį per tam tikrą laiką už specialias kainas ir taikant specialias nuolaidas.

Pardavimo sutartis yra sutartis, kuri įpareigoja klientą pirkti tam tikrą produkto kiekį per tam tikrą laiką už specialias kainas ir taikant specialias nuolaidas bei kitas specialias sąlygas, pvz., mokėjimo ir pristatymo. Pardavimo sutarties kainos ir nuolaidos turi pirmenybę prieš kainas ir nuolaidas, kurios nurodytos bet kuriose esamose prekybos sutartyse.  

Pardavimo sutarties galiojimo laikotarpis apibrėžiamas sutarties laukuose **Įsigaliojimo data** ir **Galiojimo pabaigos data**. Kliento pardavimo užsakymas atitinka sutarties sąlygas, jei pageidaujama užsakymo siuntimo data atitinka galiojimo laikotarpį. Visos pardavimo užsakymo eilutės, kurios susietos su pardavimo sutartimi, prisideda prie tos pardavimo sutarties vykdymo.  

Galite sukurti pardavimo užsakymą tiesiogiai iš pardavimo sutarties naudodami veiksmą **Išleisti užsakymą**. Arba galite pasirinkti galiojančią pardavimo sutartį atlikdami užsakymus (žr. šio straipsnio skyrių „Pardavimo sutarčių taikymas užsakymo procese“).  

> [Pastaba!] Ankstesnėse versijose pardavimo sutartys buvo vadinamos bendrais pardavimo užsakymais.

## <a name="commitment-types"></a>Įsipareigojimo tipai
Kiekviena pardavimo sutarties eilutė įpareigoja ką nors parduoti. Iš esmės yra dvi įsipareigojimų kategorijos:

-   **Vertės įsipareigojimas**– klientas įsipareigoja nupirkti produktų už tam tikrą sumą.
-   **Kiekio įsipareigojimas**– klientas įsipareigoja nupirkti tam tikrą produktų kiekį.

Be to, pagal sutartį klientas gali būti įpareigotas pirkti konkretų produktą ar produktus tam tiktoje produktų kategorijoje. Derinant šiuos du veiksnius (vertės ir kiekio bei konkrečių produktų ir produktų kategorijų), gaunami keturių tipų įsipareigojimai:

-   **Produkto kiekio įsipareigojimas**– klientas įsipareigoja nupirkti tam tikrą produktų kiekį. Eilutes, kuriose naudojamas šis įsipareigojimo tipas, apibrėžia prekės numeris ir sutartas kiekis bei vienetas. Laukas **Suma** negalimas.
-   **Produkto vertės įsipareigojimas**– klientas įsipareigoja nupirkti tam tikrų produktų už tam tikrą sumą. Eilutes, kuriose naudojamas šis įsipareigojimo tipas, apibrėžia prekės numeris ir sutarta suma. Laukai **Kiekis** ir **Vienetas** negalimi.
-   **Produkto kategorijos vertės įsipareigojimas**– klientas įsipareigoja nupirkti tam tikros pardavimo kategorijos produktų už tam tikrą sumą. Eilutes, kuriose naudojamas šis įsipareigojimo tipas, apibrėžia pardavimo kategorijų hierarchijos pardavimo kategorija ir suma. Laukai **Kiekis** ir **Vienetas** negalimi.
-   **Vertės įsipareigojimas** – klientas įsipareigoja nupirkti bet kokį produktą ar produktų iš bet kurios įsigijimo kategorijos už tam tikrą sumą. Laukai **Kiekis** ir **Vienetas** negalimi.

Tos pačios pardavimo sutarties eilutėse gali būti naudojami skirtingų tipų įsipareigojimai.

## <a name="pricing-terms-for-sales-agreements"></a>Pardavimo sutarčių kainodaros sąlygos
Kainodaros sąlygos gali skirtis, atsižvelgiant į įsipareigojimo tipą. Pardavimo užsakymo, kuris susietas su pardavimo sutartimi, kainodaros sąlygos, numatytos toje sutartyje, turi pirmenybę prieš kitas kainodaros sąlygas, kurios nurodytos prekybos sutartyse. Toliau pateikiamoje lentelėje aprašomi kainos laukai, kuriuos paveikia kiekvienas įsipareigojimo tipas. „Taip“ reiškia, kad laukas gali būti atnaujintas užsakymo eilutėje.

| Įsipareigojimo tipas                   | Vnt. kaina | Kainos vienetas | Nuolaidos procentas | Mokėjimo nuolaidos suma |
|-----------------------------------|------------|------------|------------------|----------------------|
| Produkto kiekio įsipareigojimas       | Taip        | Taip        | Taip              | Taip                  |
| Produkto vertės įsipareigojimas          |            |            | Taip              |                      |
| Produkto kategorijos vertės įsipareigojimas |            |            | Taip              |                      |
| Vertės įsipareigojimas                  |            |            | Taip              |                      |

## <a name="policies-for-sales-agreements"></a>Pardavimo sutarčių strategijos
Šios strategijos turi įtakos tam, kaip veikia ryšys tarp įsipareigojimo pardavimo sutartimi ir atitinkamos pardavimo užsakymo eilutės:

-   **Maksimaliai vykdoma**– bendras kiekis arba visų užsakymo eilučių suma negali viršyti susijusiame įsipareigojime nurodyto kiekio arba sumos.
-   **Kaina ir nuolaida fiksuotos** – užsakymo eilutės kaina ir susijusio įsipareigojimo kaina turi būti tokia pati. Jei kaina užsakymo eilutėje pakeičiama, nutraukiama sąsaja su įsipareigojimu. Jei sąsaja su įsipareigojimu nutraukiama, užsakymo eilutė nebeprisideda prie įsipareigojimo vykdymo.
-   **Minimali išduodama suma** ir **Maksimali išduodama suma** – jei suma nurodyta, atlikus bet kokius pakeitimus užsakymo eilutėje, dėl kurių užsakymo eilutė nebesutampa su susijusiu įsipareigojimu, rodomas pranešimas.

## <a name="fulfillment-calculations-for-sales-agreements"></a>Pardavimo sutarčių įvykdymo skaičiavimas
Įvykdymo kiekiai ir sumos rodomi skirtuke **Įvykdymas**, esančiame „FastTab‟ dalyje **Eilučių informacija**, puslapyje **Pardavimo sutartys**.  

Srityje **Įvykdymas** galite peržiūrėti bendrus visų su konkrečia pardavimo sutartimi susijusių užsakymo eilučių kiekius ir sumas. Taip pat galite peržiūrėti likusią sumą ar kiekį, kurio reikia įsipareigojimo įvykdymui.  

Srityje **Sutartis** galite peržiūrėti nurodytos pardavimo sutarties kiekius ir sumas. Šie kiekiai ir sumos yra bendri kiekiai ir sumos, kurioms buvo įsipareigota.

## <a name="confirmations-and-version-history-for-sales-agreements"></a>Pardavimo sutarčių tvirtinimas ir versijų retrospektyva
Patvirtinus pardavimo sutartį esama pardavimo sutarties versija yra saugoma retrospektyvos lentelėje. Jei pakeisite pardavimo sutartį, galite ją patvirtinti dar kartą, norėdami saugoti kitą pardavimo sutarties versiją retrospektyvoje.  

Jei pardavimo sutarties nepatvirtinote, vis tiek galite ją naudoti, norėdami kurti pardavimo užsakymus. Tačiau pardavimo sutarties retrospektyvos informacija nesaugoma.  

Galite peržiūrėti arba spausdinti visas patvirtinimų revizijas. Pakeitimus galite bendrinti su klientu, norėdami gauti patvirtinimą.

## <a name="applying-sales-agreements-during-the-ordering-process"></a>Pardavimo sutarčių taikymas užsakymo procese
Jei nepaleisite pardavimo užsakymų tiesiogiai iš pardavimo sutarties, dar galite susieti pardavimo sutartį su užsakymu jo įvedimo proceso metu. Kai kuriate naują pardavimo užsakymą ir pasirenkate pardavimo sutartį, šios sutarties sąlygos, pvz., mokėjimo sąlygas, pristatymo sąlygos ir pristatymo adresas, taikomos užsakymo antraštėje ir sukuriamas saitas tarp sutarties ir užsakymo. Tada užsakymo eilutėse pasirinkus produktus ir kategorijas, kurie nurodyti pardavimo sutartyje, kainos ir nuolaidos bus nukopijuotos iš tos sutarties. Tame pačiame pardavimo užsakyme gali būti eilučių, kurios nesusijusios su pardavimo sutartimi ir eilučių, kurios susijusios su pardavimo sutarties įsipareigojimu.

## <a name="modifying-sales-orders-that-are-linked-to-sales-agreements"></a>Pardavimo užsakymų, susietų su pardavimo sutartimis, keitimas
Jei sukūrėte (paleidote) pardavimo užsakymą pagal pardavimo sutartį, kai kuriuos laukus pardavimo tose užsakymo eilutėse galima keisti tik tada, jei pašalinate saitą į susijusios pardavimo sutarties eilutes. Toliau pateikiamoje lentelėje aprašomi kai kurie iš šių laukų.

| Laukas                                                             | Prekės/Paslaugos pavadinimas                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pageidaujama siuntimo data                                               | Jei pakeisite pageidaujamą siuntimo datą į datą, kuri yra ankstesnė už pardavimo sutarties eilutėje nurodytą vertę **Įsigaliojimo data**, turite pašalinti saitą į pardavimo sutarties eilutę prieš įrašydami pakeistą siuntimo datą. Jei pakeisite pageidaujamą siuntimo datą į datą, kuri yra vėlesnė už pardavimo sutarties eilutėje nurodytą vertę **Galiojimo pabaigos data**, turite pašalinti saitą į pardavimo sutarties eilutę prieš įrašydami pakeistą siuntimo datą. |
| CurrencyDiscount, percentDiscountUnit, pricePrice, unitNet suma | Jei pakeisite bet kurio iš šių laukų vertę, kai susijusios pardavimo sutarties eilutėje pažymėtas žymės langelis **Fiksuotos kainos ir nuolaidos**, pranešimo langas paragins jus įrašyti pakeitimą. Spustelėkite **Taip**, kad pašalintumėte saitą į pardavimo sutarties eilutę ir perskaičiuotumėte kainą. Spustelėkite **Ne**, kad pašalintumėte saitą į pardavimo sutarties eilutę neperskaičiavę kainos.                                                                   |
| Grynoji suma                                                        | Jei nurodote sumą, kuri viršija sumą, nurodytą pardavimo sutarties eilutėje, kurioje pažymėtas žymės langelis **Maksimaliai vykdoma**, pranešimų langas paragins jus įrašyti pakeistą sumą. Spustelėkite **Taip**, kad pašalintumėte saitą į pardavimo sutarties eilutę ir perskaičiuotumėte kainą. Spustelėkite **Ne**, kad pašalintumėte saitą į pardavimo sutarties eilutę neperskaičiavę kainos.                                                                 |
| Kiekis                                                          | Jei nurodote kiekį, kuris viršija kiekį, nurodytą pardavimo sutarties eilutėje, kurioje pažymėtas žymės langelis **Maksimaliai vykdoma**, pranešimų langas paragins jus įrašyti pakeistą kiekį. Spustelėkite **Taip**, kad pašalintumėte saitą į pardavimo sutarties eilutę ir perskaičiuotumėte kainą. Spustelėkite **Ne**, kad pašalintumėte saitą į pardavimo sutarties eilutę neperskaičiavę kainos.                                                            |

## <a name="returning-an-item-that-was-ordered-from-a-sales-agreement"></a>Prekės, užakytos iš pardavimo sutarties, grąžinimas
Kai klientas grąžina produktą, kuris buvo užsakytas pagal pardavimo sutartį, Tiekimo grandinės valdymas gali rasti ir automatiškai atnaujinti susijusį pardavimo sutarties įsipareigojimą, kad jis atspindėtų kiekio arba sumos pokytį. Kurdami grąžinimo užsakymą pagal pradinį pardavimo užsakymą, kuris susietas su pardavimo sutartimi, sukuriate ryšį tarp pardavimo sutarties įsipareigojimo, pardavimo užsakymo eilutės ir grąžinimo užsakymo SF.  

Jei nenorite atimti grąžintos prekės kiekio iš pardavimo sutarties įsipareigojimo, galite naudoti valdiklį **Pašalinti saitą** puslapyje **Grąžinimo užsakymas** ir pašalinti saitą tarp grąžinimo užsakymo ir pardavimo sutarties įsipareigojimo. Jei vėliau prireiktų atkurti saitą, spustelėkite **Kurti saitą**.  

**Pastaba.** Grąžinimo užsakymas gali būti susietas tik su viena pardavimo sutartimi. jei klientas grąžina keletą produktų, kurie buvo užsakyti pagal keletą pardavimo sutarčių, turite sukurti naują kiekvieno produkto grąžinimo užsakymą ir sukurti saitą su atitinkama pardavimo sutartimi.

## <a name="automatic-search-for-sales-agreements"></a>Automatinė pardavimo sutarčių paieška
Kai kuriais atvejais, kai pardavimo užsakymai kuriami netiesiogiai, pvz., kai kuriate kredito pažymą arba vidinės įmonės pardavimo užsakymus, galite kontroliuoti, ar sistema automatiškai ieškos taikytinų pardavimo sutarčių.

## <a name="financial-dimensions-on-sales-agreements"></a>Pardavimo sutarčių pardavimo dimensijos
Galite nukopijuoti finansines dimensijas į dokumento antraštes arba į atskiras pardavimo sutarties eilutes. Sutarties antraštėje arba sutarties eilutėje dimensijas galite keisti bet kuriuo metu. Dimensijos tada automatiškai kopijuojamos į paleidimo užsakymų leidimo antraštę arba leidimo eilutę.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]