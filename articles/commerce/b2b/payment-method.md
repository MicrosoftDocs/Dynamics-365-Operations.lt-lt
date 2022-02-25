---
title: Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams
description: Šioje temoje aprašoma, kaip konfigūruoti kliento sąskaitos mokėjimo būdą Microsoft Dynamics 365 Commerce. Taip pat aprašoma, kaip kredito limitai daro įtaką mokėjimo pagal sąskaitą fiksavimui "verslas verslui" (B2B) el. komercijos svetainėse.
author: josaw1
ms.date: 02/16/2022
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
ms.openlocfilehash: 0366f7b51ac138cc7305f98d5607c554440e6d34
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323360"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip konfigūruoti kliento sąskaitos mokėjimo būdą Microsoft Dynamics 365 Commerce. Taip pat aprašoma, kaip kredito limitai daro įtaką mokėjimo pagal sąskaitą fiksavimui "verslas verslui" (B2B) el. komercijos svetainėse.

Mažmeniniai prekybininkai gali priimti įvairius mokėjimo tipus vietoje produktų ir paslaugų, kuriuos jie parduoda el. komercijos kanale. Nustačius sistemą, „Dynamics 365 Commerce“ reikia sukonfigūruoti kiekvieną mokėjimo tipą, kurį pardavėjas priima. Kliento sąskaitos (arba "pagal sąskaitą") mokėjimo būdas turi būti palaikomas B2B el. komercijos svetainėse. 

## <a name="prerequisites"></a>Būtinieji komponentai

1. Įtraukite kliento sąskaitos mokėjimo metodą į „Commerce“ būstinę.
2. Susiekite kliento sąskaitos mokėjimo metodą su el. komercijos kanalu.
3. Įsitikinkite, kad **"** **Commerce Headquarters" kliento ypatybė Leisti pagal sąskaitą yra įgalinta kaip numatytoji "Retail" ir "Commerce \> Customers \> All \> customers Payment**".

    > [!NOTE]
    > Jei visiems klientams turi būti įgalintas mokėjimo pagal sąskaitą būdas, **·** **galite** nustatyti ypatybę Leisti pagal sąskaitą kaip Taip, jei tai numatytasis kanalo klientas, susietas su B2B svetaine. 

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

Kai kliento sąskaitos mokėjimų galimybės įgalintos B2B svetainėje, organizacijos paprastai nori parodyti informaciją apie kredito limitus ir kredito limitų balansus užsakymo fiksavimo proceso metu. Kliento kredito limitą nustato **"Commerce Headquarters**" kliento įrašo "FastTab" Kredito ir mokėjimų priežiūros ypatybė Kredito **limitas**. Tačiau B2B scenarijuose užsakymas, kuriam klientas dažnai turėtų būti išrašomas pagal organizacijos, kuriai priklauso klientas, sąskaitą. Todėl kliento įrašo **SF** **ir** pristatymo "FastTab" ypatybę SF kodas turite nustatyti kaip organizacijos kliento sąskaitos ID. Tada, kai klientas surašo užsakymą B2B svetainėje, organizacijai bus išrašyta užsakymo SF. B2B teritorijoje taip pat bus naudojamas organizacijos kredito limitas, o ne kredito limitas, nustatytas kliento įraše.

Kredito limito skaičiavimas ir balansas, rodomi B2B **svetainėje, priklauso nuo "Commerce Headquarters" ypatybės Kredito limito** tipo nustatymo. Šios ypatybės vieta skiriasi atsižvelgiant į tai, ar **funkcijų** valdymo darbo srityje įgalinta kredito **valdymo** funkcija:

- Jei įgalinta **kredito valdymo** funkcija, ypatybė yra kredito limitų "FastTab **·**",**\> kuris yra Kreditas ir rinkiniai Nustatymo \> kreditas ir mokėjimų priežiūros parametrai Kreditas \>**. 
- Jei kredito **valdymo funkcija** išjungta, ypatybė yra gautinų sumų **vertinimo** **dalyje Gautinų sumų nustatymas \> Gautinų \> sumų parametrai Kredito \> vertinimas**.

Vertės, kurias palaiko **ypatybė Kredito limito tipas** **, yra Nėra**, **Balansas**, **Balansas + Važtaraštis arba Produkto gavimo kvitas**, Balansas **+ Visi**. Daugiau informacijos apie šias vertes ieškokite kredito limito [tipo vertėse](/dynamics365/supply-chain/sales-marketing/credit-limits-customers).

> [!NOTE]
> Rekomenduojame nustatyti ypatybę Kredito **limito tipas** **kaip Balansas +** Važtaraštis arba Produkto važtaraštis, kad atviri pardavimo užsakymai neprisidarytų skaičiuojant balansą. Tada, jei jūsų klientai įteikite būsimus užsakymus, jiems nereikia pranešti, kad tie užsakymai turės įtakos jų dabartiniam balansui.

Kita ypatybė, veikiantis užsakymo pagal sąskaitą, yra **privalomo kredito limito** ypatybė, **kuri** yra kliento įrašo FastTab Kreditas ir rinkiniai. Nustatydami šią **ypatybę** kaip Taip konkretiems klientams, galite priversti sistemą patikrinti jų kredito limitą, **net jei kredito limito** **tipo ypatybė buvo nustatyta kaip Nėra**, kad būtų nurodyta, jog neturi būti tikrinamas nė vienas klientas kredito limitas.

Šiuo metu B2B svetainės, kuriose įgalinta **privalomo kredito limito** ypatybė, turi papildomų funkcijų. Jei kliento įraše įgalinta ypatybė, kai klientas pateikite užsakymą, B2B svetainė neleidžia jiems naudoti mokėjimo pagal sąskaitą metodo, kad būtų mokama daugiau nei likęs kredito balansas. Pavyzdžiui, jei likęs kliento kredito balansas yra $1,000, bet užsakymas yra vertas $1,200, klientas gali sumokėti tik $1,000 naudodamas kreditinės sąskaitos metodą. Jie turi naudoti kurį nors kitą mokėjimo būdą balansui sumokėti. Jei kliento **įraše išjungta** privalomo kredito limito ypatybė, klientas gali mokėti bet kokią sumą, naudodamas mokėjimo pagal sąskaitą būdą. Tačiau, net jei klientas gali pateikti užsakymus, sistema neleis įvykdyti šių užsakymų, jei jie viršija kredito limitą. Jei turite patikrinti visų klientų, kurie turi teisę gauti mokėjimą pagal sąskaitą, kredito limitą, **·** **rekomenduojame nustatyti ypatybės Kredito limito tipas balanso +** **pakavimo kvitas arba produkto kvitas ir privalomo kredito limito** ypatybę kaip **Ne.**

Kreditų **ir rinkinių** modulyje yra naujų kredito valdymo galimybių. Norėdami įjungti šias galimybes, funkcijų valdymo **darbo srityje** įgalinkite kredito **valdymo** funkciją. Viena iš naujų galimybių leidžia sulaikyti pardavimo užsakymus remiantis blokavimo taisyklėmis. Tada kredito vadybininko asmuo vėliau gali išleisti arba atmesti užsakymus. Tačiau galimybė sulaikyti pardavimo užsakymus netaikoma "Commerce" užsakymams, nes pardavimo užsakymuose dažnai yra išankstinis apmokėjimas, **o** kredito valdymo funkcija ne visiškai palaiko išankstinio apmokėjimo scenarijus. 

Nepaisant to, ar **kredito valdymo** funkcija įgalinta, jei kliento balansas vykdant užsakymą viršija kredito limitą, pardavimo užsakymai nebus sulaikyti. Todėl Commerce generuos įspėjimo pranešimą arba klaidos pranešimą, atsižvelgiant į pranešimo vertę, **kai viršysite kredito limito** **lauką kredito limito** lauką "FastTab".

Neįtraukti **į kredito valdymo ypatybę**, kuri neleidžia sulaikdyti "Commerce" pardavimo užsakymų, yra pardavimo užsakymo antraštėje (**Mažmeninės prekybos ir komercijos \>\> klientai visi pardavimo užsakymai**). Jei ši ypatybė yra nustatyta į **Taip** (numatytąją vertę) "Commerce" pardavimo užsakymams, užsakymai nebus įtraukti į sulaikytą kredito valdymo darbo eigą. Įsidėmėkite, kad nors ypatybės **pavadinimas Yra Neįtraukti į kredito** valdymą, nurodytas kredito limitas vis tiek bus naudojamas vykdant užsakymą. Užsakymai, kurie tik nebus sulaikyti.

Galimybės sulaikyti "Commerce" pardavimo užsakymus, remiantis blokavimo taisyklėmis, suplanuotos būsimiems "Commerce" paleidimams. Kol jis nepalaikomas, jei turite priversti " Commerce" pardavimo užsakymus pereiti per naujus kredito valdymo srautus, savo sprendimas gali pritaikyti šiuos XML Visual Studio failus. Failuose modifikuokite logiką, kad **CredManExcludeSalesOrder vėliavėlė** būtų nustatyta kaip **Ne**. Tokiu būdu "**Commerce" pardavimo užsakymų ypatybė** Neįtraukti į kredito **valdymą** bus nustatyta kaip Ne.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

Atkreipkite dėmesį, **kad jei credManExcludeSalesOrder** **vėliavėlė nustatyta kaip Ne**, o B2B klientas gali pirkti iš parduotuvių naudodamas kasos aparato (EKA) programą, grynųjų pinigų registravimas ir operacijų gali nepavykti registruoti. Pavyzdžiui, mokėjimo grynaisiais pinigais tipui taikoma blokavimo taisyklė, o B2B klientas parduotuvėje nusipirko keletą prekių naudodamas grynuosius pinigus. Šiuo atveju gautam pardavimo užsakymui nebus sėkmingai išrašyta SF, nes jis bus sulaikytas. Todėl registruoti nepavyks. Dėl šios priežasties rekomenduojame, kad po šio pritaikymo pritaikymo, atbaigtumėte testą.

## <a name="additional-resources"></a>Papildomi ištekliai

[B2B el. prekybos svetainės nustatymas](set-up-b2b-site.md)

[Valdyti B2B verslo partnerius naudojant klientų hierarchijas](partners-customer-hierarchies.md)

[Verslo partnerio vartotojų valdymas B2B el. prekybos svetainėse](manage-b2b-users.md)

[Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams](quantity-limits.md)

[SDK ir Modulio bibliotekos naujinimai](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
