---
title: Nustatyti Algalapį su Adyen Dynamics 365 Commerce
description: Šiame straipsnyje aprašoma, kaip nustatyti Algaus mokėjimo su Adyen in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 11/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: 0949b9d7a4b181605d43956932b4fc095940bd64
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780206"
---
# <a name="set-up-apple-pay-with-adyen-in-dynamics-365-commerce"></a>Nustatyti Algalapį su Adyen Dynamics 365 Commerce

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Šiame straipsnyje aprašoma, kaip nustatyti Algaus mokėjimo su Adyen in Microsoft Dynamics 365 Commerce.

## <a name="key-terms"></a>Pagrindiniai terminai

| Semestras | Aprašymas |
|---|---|
| Algalapių mokėjimas | Taip pat vadinamas Mygtuku Vlad pay, Alga pay yra mokėjimo būdas, kurį palaiko Adyen jungtis. Tai įgalina klientų patirtį ir integravimą, kuriuos palaiko Microsoft Dynamics 365 Algalapių jungtis. |
| Piniginė | Mokėjimo tipas, į kurį nėra įtrauktos tradicinės mokėjimo charakteristikos, pvz., banko identifikavimo numerio (TALPYKLOS) diapazonas ir galiojimo data, naudojami kredito ir debeto kortelių tipams atskirti. |

Dynamics 365 Commerce siūlo papildomą integravimą į Lauką Mokėti, kai naudojama Adyen mokėjimo šliuzo paslauga. "Arba Pay" yra skaitmeninis mokėjimo būdas, kuris naudoja "Vz.Pay" prekybininko sąskaitą pagal Adyen mokėjimų tarnybą. Sukonfigūrus šį mygtuką, reikia nustatyti norimą mokėjimo būdą, kuris yra interneto parduotuvės užsakymų tikrinimo puslapio dalis. Mygtukas Algalapis pateikiamas kaip mokėjimo pasirinktis tik palaikomuose "Vz." mokėjimo įrenginiuose. Kai vartotojai palaikomoje **naršyklėje** ar įrenginyje pasirenka Algalapio mokėjimą, jie nukreipiami į Algalapio mokėjimo tarnybą, kad jie tiesiogiai užbaigtų mokėjimą. Tada jie grąžinti į interneto parduotuvės iš anksto, kad būtų baigti užsakymui.

"Dynamics 365" mokėjimo jungtis, skirta "Alga Pay" jungties nuorodai, naudojama kartu su "Dynamics 365" mokėjimo jungtimi Adyen, kad būtų galima įjungti Algaus mokėjimo ir kredito kortelių mokėjimus svetainėje. "Blok" mokėjimą taip pat galima sukonfigūruoti naudoti parduotuvėse, kuriuose yra "Adyen" mokėjimo terminalai, kurie naudoja "Dynamics 365" mokėjimo jungtį Adyen su "Commerce point of sale ( EKA). Šiuo atveju "Dynamics 365" mokėjimo jungtis, skirta Adyen, apdoroja "Susie" mokėjimo įrenginį tarp mokėjimo terminalo.

## <a name="prerequisites"></a>Būtinieji komponentai

Norint naudotis "Alga Pay su Adyen" komercijos portale, reikalinga merchant account. Informacijos apie tai, kaip nustatyti Algau užmokestį jūsų tikrinimo kliento srityje, ieškokite [Algalapių mokėjimo inintegraciją](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#set-up-apple-pay). Informacijos apie tai, ką reikia daryti, kai būsite pasiruošę vykti į savo gamybos aplinką, ieškokite Live [Live](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).

Jūsų Adyen sąskaitoje taip pat turi būti integruotas Arba mokėjimo būdas. Adyen gali padėti nustatyti mokėjimo būdą ir taip pat gali padėti užtikrinti, kad domenai, kuriuose turėsite naudoti sertifikatą, būtų priskirti naudoti su sertifikatu.

Norėdami įjungti patobulintą "Commerce Headquarters" priemonių vėliavėlę, **eikite į darbo sričių funkcijų valdymą \>** ir ieškokite funkcijos Išplėstinis išplėstinis **palaikymas ir mokėjimo patobulinimas**. Pasirinkite funkciją ir tada pasirinkite **Įgalinti**. Įgalinę funkciją paleiskite **1110 paskirstymo grafiką**, kad pakeitimas būtų prieinamas visuose kanaluose.

## <a name="map-the-apple-pay-payment-method"></a>Susieti algalapių mokėjimo metodą

Kvit Pay yra skaitmeninis mokėjimo būdas. Informacijos apie tai, kaip nustatyti "Vz." mokėjimo susiejimo nustatymą, žr. [Paslaugos mokėjimų palaikymą](../wallets.md).

Norėdami susieti "Commerce Headquarters", su šiuo mokėjimu susieti "Commerce Headquarters", atlikite šiuos veiksmus.

1. Eikite į **"Retail" ir "Commerce \> Channel" \> mokėjimo būdų \> kortelių tipus**.
1. Pasirinkite **Nauja**, jei norite pridėti Eilutės Lauką Mokėti ir nustatykite šias vertes:

    - **ID:** Turi būti iš anksto sumokamas
    - **Elektroninio mokėjimo pavadinimas:** Algalapis mokėjimas
    - **Tipas: atmesta**
    - **Išdavėjas: kredito kortelės išdavėjas**

1. Pasirinkite Procesoriaus **susiejimas**, kad atidarytumėte **procesoriaus mokėjimo susiejimo** metodų dialogo langą. Nesusietų **procesoriaus mokėjimo metodų** stulpelyje išvardyti palaikomi kiekvienos galimos jungties (Adyen, PayPal ir Alga) mokėjimo būdai.
1. **Susiekite norimus palaikomus mokėjimo būdus ir "Dynamics 365" mokėjimo jungtis, skirtas Adyen** jungčiai (naudojama EKA) **ir "Dynamics 365" mokėjimo jungtis, skirta "Alga Pay**" jungtis (interneto kanalui).
1. Kiekvienos susiejimo eilutės stulpelyje Nesusieti **procesoriaus mokėjimo būdai pasirinkite eilutę, kad ji būtų palaikyti,** **o tada pasirinkite Įtraukti,** kad perkeltumėte pasirinkimus **į stulpelį Susieti procesoriaus mokėjimo** būdai.
1. Pasirinkite **Gerai**, tada puslapyje Kortelių **tipai** pasirinkite **Įrašyti**.

## <a name="set-up-the-apple-pay-certificate-for-your-site"></a>Jūsų svetainei nustatyti "Yra pay" sertifikatą

Kiekvienoje svetainėje turite įkelti domeno susiejimo rinkmeną (taip pat vadinamą Išdavimo mokėjimo sertifikatu), [kaip aprašyta Adyen Turimos mokėjimo dokumentacijoje](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live). Galite naudoti "Commerce" svetainės generatorių domeno susiejimo failui įkelti į savo svetainės laikmenų biblioteką.

Norėdami nustatyti "Vz.Pay" sertifikatą svetainės generatoriuje, atlikite šiuos veiksmus.

1. Atsisiųskite sertifikatą (domeno susiejimo failas) iš [Adyen](https://docs.adyen.com/payment-methods/apple-pay/web-drop-in#going-live).
1. Įtraukite .txt plėtinį į domeno susiejimo failą.
1. Svetainės generatoriuje įkelkite [domeno](../upload-serve-static-files.md) susiejimo failą į savo svetainės laikmenų biblioteką.
1. Eikite **į URL**.
1. Pasirinkite **Naujas \> Naujas URL**.
1. Dialogo lange **Naujas URL** pasirinkite laikmenų bibliotekos **turtą**.
1. URL maršruto **lauke** įveskite URL maršrutą (jei jis dar neįvedė). Po domeno pagrindinio URL įveskite šią reikiamą Už tam tikrą eilutę:`<domain>/.well-known/apple-developer-merchantid-domain-association.txt`.
1. Pasirinkite **Toliau**. Laikmenų biblioteka rodo visą dokumento (.txt) tipo **įkeltą** medijų turtą.
1. Pasirinkite domeno susiejimo failą, kuris turi būti naudojamas anksčiau nustatytame URL užklausoms.
1. Pasirinkite **Kurti**.

Dabar URL, kurį sukūrėte yra šablono būsenoje. Norėdami užbaigti procesą publikuokite URL. Failas, į kurį veda URL, nebebus grąžinamas iki jums publikuojant URL.

## <a name="configure-a-commerce-online-store-for-apple-pay"></a>Konfigūruoti "Commerce" internetinę saugyklą, kad būtų galima naudoti "Algalapių"

Norėdami konfigūruoti "Commerce Online Store", kad būtų galima naudoti Algalapį, atlikite šiuos veiksmus.

1. "Commerce Headquarters" eikite į mažmeninės **prekybos ir komercijos \> kanalų \> interneto parduotuves**.
1. Pasirinkite savo **svetainės interneto parduotuvės kanalo mažmeninės prekybos kanalo ID** vertę.
1. **Jei** dar nėra nustatyta mokėjimo sąskaitų "FastTab", **pridėkite "Dynamics 365" mokėjimo jungtį, skirta "Adyen**" jungtį, [vykdykite "Dynamics 365" mokėjimo jungties Adyen nurodymuose](adyen-connector-setup.md).
1. Sukonfigūrę Adyen **jungtį**, pasirinkite Įtraukti, **kad pridėtumėte "Dynamics 365" mokėjimo jungtį, kuri bus skirta "Smtp" mokėjimo jungčiai**.
1. Įveskite jungties prekybininko ypatybės vertes.

    | Ypatybė               | Aprašymas | Būtinas | Automatiškai nustatyti | Pavyzdžio vertė |
    | ---------------------- | ----------- | -------- | ----------------- | ------------ |
    | Rinkinio pavadinimas          | "Dynamics 365" mokėjimo jungties rinkinio, skirtoVz., Pay, pavadinimas. | Taip | Taip | Dvejetainis pavadinimas |
    | Tarnybos abonemento ID     | Unikalus prekybininko ypatybės nustatymo identifikatorius. Šis identifikatorius yra antspauduotas mokėjimo operacijose ir identifikuoja prekybininko ypatybes, kurias turi naudoti proceso pabaigos procesai (pvz., SF išrašymas). | Taip | Taip | Guid |
    | Prekybininko sąskaitos ID    | Įveskite unikalų Adyen prekybininko identifikatorių. Ši vertė pateikiama, kai prisiregistruojate Adyen, kaip [aprašyta Registruotis Adyen](adyen-connector-setup.md#sign-up-with-adyen). | Taip | Ne | MerchantIdentifier |
    | Debesies API raktas          | Įvesti Adyen debesies API raktą. Šį raktą galite gauti pagal instrukcijas, kaip [gauti API raktą](https://docs.adyen.com/developers/user-management/how-to-get-the-api-key). | Taip | Ne | abcdefg |
    | Šliuzo aplinka    | Įveskite Adyen šliuzo aplinką, su iš kurios norite susieti. Galimos vertės yra Bandymas **ir** Tiesioginis **·**. Šį lauką turėtumėte nustatyti tik gamybos **įrenginiams** ir operacijoms tiesiogiai naudoti. | Taip | Taip | Aktyvus |
    | Palaikomos valiutos   | Įveskite valiutas, kurias turėtų apdoroti jungtis. Dabartiniuose kortelių scenarijuose Adyen gali palaikyti papildomas [valiutas](https://www.adyen.com/pos-payments/dynamic-currency-conversion), per dinaminį valiutos konvertavimą po to, kai operacijos užklausa siunčiama į mokėjimo terminalą. Susisiekite su Adyen palaikyme, kad gautumėte palaikomų valiutų sąrašą. | Taip | Taip | USD; Eur |
    | Palaikomi mokėjimo priemonių tipai | Įveskite mokėjimo priemonių tipus, kuriuos turėtų apdoroti jungtis. | Taip | Taip | Galimas sąs. |

1. Kai prekybininko informacija įvesta, vykdykite **1070 kanalo konfigūravimo** paskirstymo grafiko užduotį.

## <a name="configure-commerce-pos-for-apple-pay"></a>Konfigūruoti "Commerce POS", kad būtų galima naudoti "Algalapių" užmokestį

EKA konfigūracija naudoja **aparatūros šablono EFT** paslaugos lauko, skirto "Dynamics 365" mokėjimo jungtis, skirta Adyen, konfigūraciją. Programoje "Commerce Headquarters" sukonfigūruokite "Dynamics 365" mokėjimo jungties EFT jungtį Adyen [, kaip aprašyta skyriuje Nustatyti "Dynamics 365 POS" aparatūros šabloną](adyen-connector-setup.md#set-up-a-dynamics-365-pos-hardware-profile).

Įsitikinkite, kad įtraukiate **Į mokėjimo** priemonių tipų sąrašą palaikomų mokėjimo **priemonių tipų** lauke. Naudoti kabliataškius (;), jei norite sąraše atskirti mokėjimo priemonių tipus.

"Adyen" jungties procesoriaus susiejimas fiksuoja kortelės tipus, kuriuos "Alga Pay" naudoja EKA terminale.

### <a name="configure-content-security-policies-in-site-builder"></a>Konfigūruoti turinio saugos strategijas svetainės generatoriuje

Prieš konfigūrdami savo fragmentus ar puslapius taip, kad jie būtų naudojami, turite užtikrinti, kad jūsų turinio saugos strategijos (CSPs) yra sukonfigūruotos jūsų svetainės "Commerce" svetainės generatoriuje.

Norėdami konfigūruoti turinio saugos strategijas svetainės generatoriuje, atlikite šiuos veiksmus.

1. Eikite į **Saito nustatymai \> Plėtiniai**.
1. **Skirtuke** Turinio saugos strategija pasirinkite Įtraukti, kad būtų eilutė, **·**`https://applepay.cdn-apple.com/jsapi/v1/apple-pay-sdk.js`**kuri turi antrinius src**, **connect-src** **, rėmus,** **img-src**, **scenarijaus src** **ir stiliaus src** skyrius.
1. Baigę pasirinkite Įrašyti ir paskelbti **, kad** užfiksuotumėte pakeitimus.

### <a name="set-up-apple-pay-as-a-checkout-payment-option"></a>Nustatyti Algalapių kaip mokėjimo išregistravimas pasirinktį

Norėdami Jūsų svetainės (ne skubus) čekio puslapyje nustatyti Yra mokėjimo čekiu pasirinktis, atlikite šiuos veiksmus.

1. Svetainės generatoriuje eikite **į** fragmentus ir pasirinkite svetainės tikrinimo fragmentą.
1. Pasirinkite **Redaguoti**.
1. **Tikrinimo skyriaus konteinerio atminties** dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite Modulį **Algalapių** mokėjimas, tada pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte fragmentą, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Modulyje **"Cb pay** " parametrai yra sukurti ir sujungti su sukonfigūruota "Dynamics 365" mokėjimo jungtis, skirta "Alga Pay" jungčiai, kuri nustatyta "Commerce Headquarters" interneto kanalui.

### <a name="apple-pay-payment-behavior"></a>Mokėjimo už mokėjimą veikimo būdas

Kvito **mokėjimo mygtukas** rodomas tik palaikomuose "Alga Pay" įrenginiuose ("iPhones", "iPhones" ir "Alga" naršyklėse, kurios palaiko Algalapį). Jei vartotojas nenaudoja vieno iš šių įrenginių, " **Forget Pay" mokėjimo** mygtukas nero naudojamas rodinyje.

Kai vartotojas pasirenka "Algalapio **mokėjimo** " mygtuką, pasirodo **dialogo langas** Pasirinktys. Ten vartotojas gali autentifikuoti savo Pagal jūsų "Ar" Pay įrenginį arba naršyklę. Dialogo **lange Skirtukas** mokėti rodoma užsakymo sumos ir mokėjimo būdo, kurį vartotojas sukonfigūravo pagal savo Patamską, suvestinė. Vartotojas gali peržiūrėti šią informaciją ir tada pasirinkti Mokėti **,** kad užbaigtų mokėjimą. Kai mokėjimas baigtas, vartotojas nukreipiamas į užsakymo užbaigto **svetainės** puslapį, kuriame pateikiama išsami užbaigtos operacijos užsakymo suvestinė.

## <a name="additional-resources"></a>Papildomi ištekliai

[DUK apie mokėjimus](payments-retail.md)

[Pirkimo užbaigimo modulis](../add-checkout-module.md)

[Mokėjimo modulis](../payment-module.md)
