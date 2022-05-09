---
title: Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams
description: Šioje temoje aprašoma, kaip konfigūruoti kliento sąskaitos mokėjimo metodą programoje Microsoft Dynamics 365 Commerce. Jame taip pat aprašoma, kaip kredito limitai veikia sąskaitų mokėjimų fiksavimą verslo verslui (B2B) elektroninės prekybos svetainėse.
author: josaw1
ms.date: 04/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a8fdeb109204557f0e44457e23a60224e662474f
ms.sourcegitcommit: 96e2fb26efd2cd07bbf97518b5c115e17b77a0a8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/20/2022
ms.locfileid: "8616837"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip konfigūruoti kliento sąskaitos mokėjimo metodą programoje Microsoft Dynamics 365 Commerce. Jame taip pat aprašoma, kaip kredito limitai veikia sąskaitų mokėjimų fiksavimą verslo verslui (B2B) elektroninės prekybos svetainėse.

Mažmeniniai prekybininkai gali priimti įvairius mokėjimo tipus vietoje produktų ir paslaugų, kuriuos jie parduoda el. komercijos kanale. Nustačius sistemą, „Dynamics 365 Commerce“ reikia sukonfigūruoti kiekvieną mokėjimo tipą, kurį pardavėjas priima. Kliento sąskaitos (arba "laisvos formos sąskaitos") mokėjimo metodas turi būti palaikomas B2B el. prekybos svetainėse. 

## <a name="prerequisites"></a>Būtinieji komponentai

1. Įtraukite kliento sąskaitos mokėjimo metodą į „Commerce“ būstinę.
2. Susiekite kliento sąskaitos mokėjimo metodą su el. komercijos kanalu.
3. Įsitikinkite, kad **ypatybė Leisti naudoti sąskaitą** įgalinta klientui mažmeninės **prekybos ir prekybos \> klientams \> Visi klientai \> Mokėjimai numatytieji "** Commerce" būstinėje.

    > [!NOTE]
    > Jei visiems klientams turėtų būti leidžiama įjungti laisvos formos sąskaitos mokėjimo metodą, galite nustatyti **su B2B svetaine susieto kanalo ypatybę Leisti sąskaitoje** į **Taip**. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Įjunkite kliento sąskaitos mokėjimo metodą „Commerce“ vietos kūrimo įrankyje 

Norėdami įjungti kliento sąskaitos mokėjimo metodą „Commerce“ saito kūrimo įrankyje, vadovaukitės šiais žingsniais.

1. Eikite į **Saito nustatymai \> Plėtiniai**.
1. Nustatykite **Įjungti kliento sąskaitos mokėjimus** ypatybę į **Įjungti B2B klientams**. 
1. Pasirinkite **Įrašyti ir publikuoti**.

> [!NOTE]
> Nauji saito nustatymai įsigalioja tik atnaujinus app.settings.json failą. Dėl daugiau informacijos, žr. [SDK ir modulio bibliotekos naujinimai](../e-commerce-extensibility/sdk-updates.md).

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>Įjunkite kliento sąskaitos mokėjimo metodą išsiregistravimo puslapyje B2B el. komercijos saite

Norėdami įjungti kliento sąskaitos mokėjimo metodą išsiregistravimo puslapyje B2B el. komercijos saite, atlikite šiuos žingsnius.

1. „Commerce“ saito kūrimo įrankyje, suraskite ir redaguokite išsiregistravimo puslapį ar fragmentą, kuriame yra išsiregistravimo modulis B2B el. komercijos saite.
1. Vietoje **Išsiregistravimo sektoriaus konteineris** rinkitės **Įtraukti modulį** ir tuomet įtraukite **Kliento sąskaitos mokėjimas** modulį.
1. Padėkite **Kliento sąskaitos mokėjimas** modulį pasirinkę daugtaškį (**...**) ir tuomet pasirinkę **Eiti aukštyn** ar **Eiti žemyn** kaip būtina.
1. Pasirinkite **Išsaugoti**, tada – **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Patvirtinkite, kad kliento sąskaitos sumokėjimo metodas buvo įjungtas ir publikuotas

Norėdami patvirtinti, kad kliento sąskaitos sumokėjimo metodas buvo įjungtas ir publikuotas, atlikite šiuos veiksmus.

1. Prisijunkite prie el. komercijos saito.
1. Įtraukite prekę į vežimėlį.
1. Eikite į išsiregistravimo puslapį. Turėtumėte matyti naują **Kliento sąskaitos** mokėjimo metodą.

## <a name="work-with-credit-limits"></a>Darbas su kredito limitais

Kai B2B svetainėje įgalinamos kliento sąskaitų mokėjimų galimybės, organizacijos paprastai nori rodyti informaciją apie kredito limitus ir kredito limito likučius užsakymų fiksavimo proceso metu. Kliento kredito limitas apibrėžiamas **pagal turtą Kredito limitas**, esantį **"Commerce" būstinėje** esančio kliento įrašo FastTab Kreditas ir rinkiniai. Tačiau B2B scenarijuose užsakymui, kurį klientas pateikia, dažnai turėtų būti išrašyta SF į organizacijos, kuriai priklauso klientas, sąskaitą. Todėl pirkėjo įrašo FastTab SF ir pristatymas **ypatybę** **turite** nustatyti organizacijos pirkėjo sąskaitos ID į organizacijos pirkėjo sąskaitos ID. Tada, kai klientas pateikia užsakymą B2B svetainėje, užsakymui bus išrašyta SF organizacijai. B2B svetainėje taip pat bus naudojamas organizacijos kredito limitas, o ne kliento įraše nurodytas kredito limitas.

Kredito limito skaičiavimas ir likutis, rodomas B2B svetainėje, priklauso nuo kredito limito **tipo** turto nustatymo "Commerce" būstinėje. Šios ypatybės vieta skiriasi, atsižvelgiant į tai, ar **kredito valdymo** funkcija įgalinta **darbo srityje Funkcijų valdymas**:

- **Jei kredito valdymo** funkcija įgalinta, ypatybė yra **FastTab Kredito limitai**, esančiame Kredito **ir rinkinių nustatymo \> kredito ir rinkinių \> parametruose \> Kreditas**. 
- **Jei kredito valdymo** funkcija išjungta, turtas yra dalyje **Gautinų sumų nustatymo gautinų sumų** parametrų **\> kredito reitingas \>\>**.

Reikšmės, kurias **palaiko ypatybė Kredito limito tipas**, yra **Nėra**, **Likutis**, **Likutis + važtaraštis arba produkto gavimo kvitas** ir **Likutis + Visi**. Daugiau informacijos apie šias vertes ieškokite [Credit limit type values](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> Rekomenduojame nustatyti ypatybę Kredito limito **tipas** kaip **Likutis + pakuotės lapas arba produkto kvitas**, kad atviri pardavimo užsakymai neprisidėtų prie balanso skaičiavimo. Tada, jei jūsų klientai pateikia būsimus užsakymus, jiems nereikia nerimauti, kad šie užsakymai paveiks jų dabartinį balansą.

Kita ypatybė, turinti įtakos laisvos formos sąskaitos užsakymui, yra **ypatybė Privalomas kredito limitas**, esanti **kliento įrašo FastTab Kreditas ir rinkiniai**. Nustatydami šią ypatybę į **Taip** konkretiems klientams, galite priversti sistemą patikrinti jų kredito limitą, net jei **kredito limito tipo** ypatybė buvo nustatyta kaip **Nėra**, kad būtų nurodyta, jog kredito limito negalima tikrinti nė vienam klientui.

Šiuo metu klientas, naudojantis laisvos formos sąskaitos mokėjimo metodą, negali sumokėti daugiau nei likęs užsakymo kredito likutis. Pavyzdžiui, jei likęs kliento kredito likutis yra $1,000, bet užsakymo vertė yra $1,200, klientas gali sumokėti $1,000 tik naudodamas laisvos formos sąskaitos metodą. Tada klientas turi naudoti kitą mokėjimo būdą, kad sumokėtų likutį. Būsimame leidime "Commerce" konfigūracija leis vartotojams išleisti daugiau nei jų kredito limitas pateikiant užsakymus.

Kredito **ir kolekcijų modulis** turi naujas kredito valdymo galimybes. Norėdami įjungti šias galimybes, įgalinkite **kredito valdymo** funkciją **darbo srityje Funkcijų valdymas**. Viena iš naujų galimybių leidžia sustabdyti pardavimo užsakymus pagal blokavimo taisykles. Tada kredito valdytojo asmuo gali paleisti arba atmesti užsakymus po tolesnės analizės. Tačiau galimybė sulaikyti pardavimo užsakymus netaikoma "Commerce" užsakymams, nes pardavimo užsakymuose dažnai yra išankstinis apmokėjimas, o **kredito valdymo** funkcija nevisiškai palaiko išankstinio apmokėjimo scenarijus. 

Neatsižvelgiant į tai, ar **įgalinta kredito valdymo** funkcija, jei įvykdymo metu kliento balansas viršija kredito limitą, pardavimo užsakymai nebus sulaikyti. Todėl Commerce generuos įspėjimo pranešimą arba klaidos pranešimą, atsižvelgiant į pranešimo vertę, **kai viršysite kredito limito** **lauką kredito limito** lauką "FastTab".

Neįtraukti **į kredito valdymo ypatybę**, kuri neleidžia sulaikdyti "Commerce" pardavimo užsakymų, yra pardavimo užsakymo antraštėje (**Mažmeninės prekybos ir komercijos \>\> klientai visi pardavimo užsakymai**). Jei ši ypatybė yra nustatyta į **Taip** (numatytąją vertę) "Commerce" pardavimo užsakymams, užsakymai nebus įtraukti į sulaikytą kredito valdymo darbo eigą. Nors ypatybės pavadinimas Yra Neįtraukti **į kredito valdymą**, nustatytas kredito limitas vis tiek bus naudojamas užsakymo įvykdymo metu. Užsakymai, kurie tik nebus sulaikyti.

Galimybės sulaikyti "Commerce" pardavimo užsakymus, remiantis blokavimo taisyklėmis, suplanuotos būsimiems "Commerce" paleidimams. Kol jis nepalaikomas, jei turite priversti " Commerce" pardavimo užsakymus pereiti per naujus kredito valdymo srautus, savo sprendimas gali pritaikyti šiuos XML Visual Studio failus. Failuose modifikuokite logiką, kad **CredManExcludeSalesOrder vėliavėlė** būtų nustatyta kaip **Ne**. Tokiu būdu "**Commerce" pardavimo užsakymų ypatybė** Neįtraukti į kredito **valdymą** bus nustatyta kaip Ne.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

**Jei nustatyta credManExcludeSalesOrder** **vėliavėlė Ne**, o B2B klientas gali pirkti iš parduotuvių naudodamas kasos aparato (EKA) programą, gali nepavykti registruoti grynųjų pinigų ir atlikti operacijų. Pavyzdžiui, mokėjimo grynaisiais tipui taikoma blokavimo taisyklė, o B2B klientas parduotuvėje nusipirko keletą prekių naudodamas grynuosius pinigus. Šiuo atveju gautam pardavimo užsakymui nebus sėkmingai išrašyta SF, nes jis bus sulaikytas. Todėl registruoti nepavyks. Dėl šios priežasties rekomenduojame, kad po šio pritaikymo pritaikymo, atbaigtumėte testą.

## <a name="additional-resources"></a>Papildomi ištekliai

[B2B el. prekybos svetainės nustatymas](set-up-b2b-site.md)

[B2B verslo partnerių valdymas naudojant klientų hierarchijas](partners-customer-hierarchies.md)

[Verslo partnerio vartotojų valdymas B2B el. prekybos svetainėse](manage-b2b-users.md)

[Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams](quantity-limits.md)

[SDK ir Modulio bibliotekos naujinimai](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
