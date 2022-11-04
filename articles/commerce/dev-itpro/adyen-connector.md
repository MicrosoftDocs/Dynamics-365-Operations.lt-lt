---
title: „Dynamics 365 Payment Connector“, skirto sprendimui „Adyen“, apžvalga
description: Šiame straipsnyje pateikta Adyen Microsoft Dynamics 365 mokėjimo jungties apžvalga.
author: rassadi
ms.date: 10/27/2022
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 931fc69cda8daa2e06b6f1155fbf0369fd2bca55
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728297"
---
# <a name="dynamics-365-payment-connector-for-adyen-overview"></a>„Dynamics 365 Payment Connector“, skirto sprendimui „Adyen“, apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama Adyen Microsoft Dynamics 365 mokėjimo jungties apžvalga ir išsamus palaikomų funkcijų ir funkcijų sąrašas. Susiję straipsniai apima "Adyen" prisijungimą, jungties konfigūraciją, dažnai užduodamus klausimus ir kai kurių bendrųjų problemų trikčių šalinimo gaires.

## <a name="key-terms"></a>Pagrindiniai terminai

| Semestras | Aprašymas |
|---|---|
| Mokėjimo jungtis | Plėtinys, kuris palengvina ryšį Microsoft Dynamics 365 Commerce tarp (ir susijusių komponentų) ir mokėjimo tarnybos. Šiame straipsnyje aprašyta jungtis įdiegta naudojant standartinių mokėjimų programinės įrangos kūrimo rinkinį (SDK). |
| Kortelė yra | Nurodo mokėjimo operacijas, kai pateikiama faktinė kortelė ir naudojama mokėjimo terminalo jungtyje su "Dynamics 365" pardavimo tašku. |
| Kortelės nėra | Nurodo mokėjimo operacijas, kuriose nėra faktinės kortelės, pvz., el. komercijos arba skambučių centro scenarijus. Šiuose scenarijuose su mokėjimu susijusi informacija įvedama rankiniu būdu arba el. komercijos svetainėje, skambučių centro sraute, elektroninį kasos kodą ar mokėjimo terminale. |

## <a name="supported-features-functionality-versions-and-terminals"></a>Palaikomos funkcijos, funkcijos, versijos ir terminalai

"Dynamics 365" mokėjimo jungtis, skirta Adyen, naudoja standartinį mokėjimų SDK. Todėl jis neturi specialių galimybių, kurių negalima naudoti ir kitoms mokėjimo jungtims.

### <a name="supported-versions"></a>Palaikomos versijos

#### <a name="microsoft-dynamics-365-supported-versions"></a>Microsoft Dynamics 365 palaikomos versijos
Pirmos šalies "Dynamics 365" mokėjimo jungtis, skirta Adyen Microsoft Dynamics, palaikoma 365 finansų versijoje 8.1.3 (2019 m. sausio mėn.) arba vėlesnėje versijoje, Microsoft Dynamics 365 Retail 8.1.3 arba vėlesnėje versijoje. Tačiau trečiosios šalys vis dar gali kurti kitas 365 versijų Adyen Microsoft Dynamics mokėjimo jungtis.

#### <a name="supported-adyen-firmware-versions"></a>Palaikomos Adyen failo versijos

Toliau pateiktame sąraše aprašomos minimalios ir maksimalios Adyen versijos, kurias palaiko kiekviena EKA Microsoft Dynamics 365 Retail versija.

---

# <a name="10025"></a>[10.0.25](#tab/10-0-25)
### <a name="dynamics-365-retail-pos-version-10025"></a>Dynamics 365 Retail EKA versija 10.0.25
| Minimali AdyenŲ versija | Maksimali Adyen Maksimalaus versija |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_73p6 |

# <a name="10026"></a>[10.0.26](#tab/10-0-26)
### <a name="dynamics-365-retail-pos-version-10026"></a>Dynamics 365 Retail EKA versija 10.0.26
| Minimali AdyenŲ versija | Maksimali Adyen Maksimalaus versija |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10027"></a>[10.0.27](#tab/10-0-27)
### <a name="dynamics-365-retail-pos-version-10027"></a>Dynamics 365 Retail EKA versija 10.0.27
| Minimali AdyenŲ versija | Maksimali Adyen Maksimalaus versija |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p13 |

# <a name="10028"></a>[10.0.28](#tab/10-0-28)
### <a name="dynamics-365-retail-pos-version-10028"></a>Dynamics 365 Retail EKA versija 10.0.28
| Minimali AdyenŲ versija | Maksimali Adyen Maksimalaus versija |
| --- | --- |
| adyen_v1_73p6 | adyen_v1_75p22 |

# <a name="10029"></a>[10.0.29](#tab/10-0-29)
### <a name="dynamics-365-retail-pos-version-10029"></a>Dynamics 365 Retail EKA versija 10.0.29
| Minimali AdyenŲ versija | Maksimali Adyen Maksimalaus versija |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

# <a name="10030"></a>[10.0.30](#tab/10-0-30)
### <a name="dynamics-365-retail-pos-version-10030"></a>Dynamics 365 Retail EKA versija 10.0.30
| Minimali AdyenŲ versija | Maksimali Adyen Maksimalaus versija |
| --- | --- |
| adyen_v1_71p16 | adyen_v1_78p6 |

---

> [!NOTE]
> Adyen gali išleisti smulkų versijos naujinimą po to, kai Microsoft išbandė pagrindinę versiją. Jei palaikoma pagrindinė versija, galima gerai turėti smulkius tos pačios pagrindinės versijos versijos atnaujinimus. Paprastai šie atnaujinimai yra labai tikslinės pataisos ir neatitinka viso pakartotinio tikinimo juostos, kol anksčiau buvo patikrinta ta pati pagrindinė programos versija. Atnaujinimai neturi viršyti maksimalios dokumentacijoje nurodytos Adyen uždavimo versijos. 
>
> Norint pereiti iš Adyen versijos, ankstesnės nei 53 versijos, į 53 versiją, reikia EKA **4577957**, kad būtų galima kas mėnesį atnaujinti "Commerce", nuo 10.0.11 iki 10.0.14 versijas. Jei viena iš šių versijų naudojama ir neapima karštųjų pataisų, atnaujinus mokėjimo terminalą mokėjimai bus leidžiami tik per NFC. Pritaikius karštąją pataisą EKA išsprendžia šią problemą. Jei EKA versija senesnė nei 10.0.11 versija, patkite palaikymo užklausą, kad kb **4577957** reikalinga ne tarnybos MPOS pataisa.
> 
> Adyen 59p7–62p9 versijoms iš dovanų kortelės išgryninimo operacija pageidauja PIN įrašo du kartus scenarijuose, **kuriuose** dovanų kortelė įvedama rankiniu būdu. Nu perbraukus dovanų kortelę ši problema dar kartą nepateikiama. Adyen tyrinėti. 

### <a name="supported-payment-terminals"></a>Palaikomi mokėjimo terminalai
"Dynamics 365" mokėjimo jungtis, skirta Adyen, pasinaudoti įrenginio agnostinio [Adyen mokėjimo terminalo API privalumais](https://www.adyen.com/blog/introducing-the-terminal-api). Jis palaiko visus mokėjimo terminalus, kuriuos palaiko ši programos programavimo sąsaja (API). Norėdami pasiekti visą palaikomų mokėjimo terminalų sąrašą, apsilankykite " [Adyen POS" terminalų](https://www.adyen.com/pos-payments/terminals) puslapyje.

### <a name="supported-payment-instruments"></a>Palaikomi mokėjimo instrumentai

#### <a name="supported-debit-and-credit-cards"></a>Palaikomos debeto ir kredito kortelės

| Rūšis | Variantas | Kortelė yra | El. prekyba | Skambučių centras |
|---|---|:-:|:-:|:-:|
| MasterCard | Kreditas | ✔ | ✔ | ✔ |
| MasterCard | Debetas | ✔ | ✔ | ✔ |
| MasterCard | Raidinė banko premija | ✔ | ✔ | ✔ |
| MasterCard | Algalapių mokėjimas | ✔ |  |  |
| MasterCard | Algalapių mokėjimas | ✔ |  |  |
| MasterCard | Maestro | ✔ | ✔ | ✔ |
| MasterCard | Algalapių mokėjimas | ✔ |  |  |
| MasterCard | Arba UK | ✔ | ✔ | ✔ |
| VIZOS | Kreditas | ✔ | ✔ | ✔ |
| VIZOS | Debetas | ✔ | ✔ | ✔ |
| VIZOS | Raidinė banko premija | ✔ | ✔ | ✔ |
| VIZOS | Android Mokėti | ✔ |  |  |
| VIZOS | Algalapių mokėjimas | ✔ |  |  |
| VIZOS | Algalapių mokėjimas | ✔ |  |  |
| VIZOS | VIZOS IŠREGISTRAVIMAS | ✔ | ✔ | ✔ |
| VIZOS | VISA Dankort | ✔ | ✔ | ✔ |
| VIZOS | Visa Javsaario | ✔ | ✔ | ✔ |
| VIZOS | VISA Ar turi kortelė | ✔ | ✔ | ✔ |
| AMEX | Kreditas | ✔ | ✔ | ✔ |
| AMEX | Debetas | ✔ | ✔ | ✔ |
| AMEX | Android Mokėti | ✔ |  |  |
| AMEX | Algalapių mokėjimas | ✔ |  |  |
| AMEX | Algalapių mokėjimas | ✔ |  |  |
| AMEX | AMEX komercinė veikla | ✔ | ✔ | ✔ |
| AMEX | AMEX vartotojas | ✔ | ✔ | ✔ |
| AMEX | AMEX įmonės | ✔ | ✔ | ✔ |
| AMEX | AMEX smulkusis verslas | ✔ | ✔ | ✔ |
| Aptikti | Standartinis | ✔ | ✔ | ✔ |
| Aptikti | Android Mokėti | ✔ |  |  |
| Aptikti | Algalapių mokėjimas | ✔ |  |  |
| Aptikti | Algalapių mokėjimas | ✔ |  |  |
| Diners   | Standartinis | ✔ | ✔ | ✔ |
| Dineromail | Standartinis | ✔ | ✔ | ✔ |
| Jcb | Standartinis | ✔ | ✔ | ✔ |
| "Union Pay"\* | Standartinis | ✔ |  |  |
| Tarpinis debetas\* | Standartinis | ✔ |  |  |

\* Adyen pateikia ne "Interac" ir "Union Pay" pasikartojančių kortelių atpažinimo ženklų, todėl jų negalima naudoti kortelėms pateikti operacijų.

#### <a name="supported-gift-cards"></a>Palaikomos dovanų kortelės
| Schema | Kortelė yra | Kortelės nėra |
|---|:-:|---|
| Atiduoti | ✔ | ✔ |
| SVS | ✔ | ✔ |

Norėdami palaikyti šias išorines dovanų kortelių schemas naudodami "Dynamics 365" mokėjimo jungtį Adyen, turite atlikti papildomus veiksmus. Daugiau informacijos ieškokite išorinių [dovanų kortelių palaikymas](/dynamics365/unified-operations/retail/dev-itpro/gift-card).

#### <a name="supported-wallets"></a>Palaikomi užd.

| Schema | Kortelė yra | Kortelės nėra |
|---|---|---|
| Alipay | Palaikymas bus įtrauktas į būsimą leidimą. | Ne |
| Wechat | Palaikymas bus įtrauktas į būsimą leidimą. | Ne |

#### <a name="supported-card-present-input-methods"></a>Palaikomos kortelės įvesties metodai
| Įvesties metodas | Palaikoma | Pastabos |
|---|:-:|---|
| Dip | ✔ | |
| Perbraukti | ✔ | |
| Bakstelėkite | ✔ | |
| Rankiniu būdu įvesti naudojant EKA UI. |  | Šiuo metu nepalaikoma |
| Įvesti neautomatiniu būdu per mokėjimo terminalą. | ✔ | Palaiko neautomatinį kredito, debeto ir dovanų kortelių į įvestis su pin įrašu. | 


#### <a name="supported-card-present-countries"></a>Palaikomos kortelės pateikia šalis

Šiose šalyse yra "Commerce" komponentų ir kortelė pateikia Adyen palaikymą. Jei norite gauti šiuo metu pasiekiamumą tarptautiniu mastu, apsilankykite tarptautinių [paslaugų puslapyje](/dynamics365/get-started/availability).

| Šalis | Palaikoma |
| --- | :-: |
| Australija | ✔ |
| Austrija | ✔ |
| Belgija | ✔ |
| Kanada | ✔ |
| Čekijos Respublika | ✔ |
| Danija | ✔ |
| Estija | ✔ |
| Suomija | ✔ |
| Prancūzija | ✔ |
| Vokietija | ✔ |
| YAKR Honkongas | ✔ |
| Vengrija | ✔ |
| Islandija | ✔ |
| Airija | ✔ |
| Italija | ✔ |
| Japonija | Būsimas paleidimas |
| Latvija | ✔ |
| Lietuva | ✔ |
| Malaizija | ✔ |
| Nyderlandai | ✔ |
| Naujoji Zelandija | ✔ |
| Norvegija | ✔ |
| Lenkija | ✔ |
| Singapūras | ✔ |
| Šveicarija | ✔ |
| Ispanija | ✔ |
| Švedija | ✔ |
| Šveicarija | ✔ |
| Jungtinė Karalystė | ✔ |
| Jungtinės Valstijos | ✔ |
| Brazilija | Būsimas paleidimas |

#### <a name="supported-card-not-present-countries"></a>Palaikomos kortelės nėra šalyse

Adyen palaiko šias šalis, kurios neturi operacijų su kortele. [Norėdami gauti išsamesnės informacijos apie konkrečios šalies palaikymą, susisiekite su Adyen](https://www.adyen.com/contact/sales). Jei norite gauti šiuo metu pasiekiamumą tarptautiniu mastu, apsilankykite tarptautinių [paslaugų puslapyje](/dynamics365/get-started/availability).

| Šalis | 
| --- |
| Argentina |
| Armėnija |
| Australija |
| Austrija |
| Bahreinas |
| Belgija |
| Brazilija |
| Bulgarija |
| Kanada |
| Čilė |
| Kinija |
| Kolumbija |
| Kroatija |
| Kipras |
| Čekijos Respublika  |
| Danija |
| Egiptas |
| Estija |
| Suomija |
| Prancūzija |
| Gruzija |
| Vokietija |
| Gibraltaras |
| Graikija |
| Gernsis |
| YAKR Honkongas |
| Vengrija |
| Islandija |
| Indija |
| Indonezija |
| Airija |
| Meno Sala |
| Izraelis |
| Italija |
| Japonija |
| Džersis |
| Korėja |
| Kuveitas |
| Latvija |
| Lietuva |
| Liuksemburgas |
| Malaizija |
| Malta |
| Meksika |
| Marokas |
| Nyderlandai |
| Naujoji Zelandija |
| Norvegija |
| Peru |
| Lenkija |
| Portugalija |
| Kataras |
| Rumunija |
| Saudo Arabija |
| Serbija |
| Singapūras |
| Slovakija |
| Slovėnija |
| Pietų Afrika |
| Ispanija |
| Švedija |
| Šveicarija |
| Taivanas |
| Tanzanija |
| Tailandas |
| Turkija |
| Jungtiniai Arabų Emyratai (JAE) |
| Jungtinė Karalystė |
| Jungtinės Amerikos Valstijos, įskaitant Puerto Riką  |

#### <a name="supported-dynamics-365-payment-features"></a>Palaikomos "Dynamics 365" mokėjimo funkcijos

Šioje lentelėje parodytas funkcijų, kurias palaiko "Dynamics 365" mokėjimo jungtis Adyen, rinkinys. Šios funkcijos naudoja patobulinimus, kurie buvo įdiegti mokėjimų SDK, ir kai kuriuos komponentus 2018 m. gruodžio mėn. Jie nėra išskirtiniai Adyen "Dynamics 365" mokėjimo jungtis. Daugiau informacijos apie tai, kaip naudoti šiuos patobulinimus skirtingoms mokėjimo jungti, [ieškokite sukurkite mokėjimo terminalo galutinio mokėjimo integravimą](/dynamics365/unified-operations/retail/dev-itpro/end-to-end-payment-extension).

| Schema | Kortelė yra | Kortelės nėra |
|---|:-:|:-:|
| [Iš grynųjų pinigų išeiti dovanų kortelės likutis](/dynamics365/unified-operations/retail/dev-itpro/gift-card-cash-out) | ✔ | |
| [Dubliuoti mokėjimų apsaugą](/dynamics365/unified-operations/retail/duplicate-payment-protection) | ✔ | |
| Tamsos kanalo atpažinimo ženklų išdavimas | ✔ | ✔ |
| Susieti grąžinimai | ✔<br>(Prasideda 10.0.1) | ✔<br>(Prasideda 10.0.1) |
| [Įrašyti mokėjimus tinkle](../dev-itpro/adyen-connector-listPI.md) | | ✔<br>(Prasideda 10.0.2) | 
| [Išorinės dovanų kortelės, skirti skambučių centrui ir el. prekybai](./gift-card.md) | ✔<br>(Prasideda 10.0.10) | 
| [SCA mokėjimo nukreipimas](../adyen_redirect.md) | | ✔<br>(Prasideda 10.0.12) |
| [Paskirtieji mokėjimo terminalai ir raginimai spausdintuvui ir kasos stalčiui](../pos-multi-hws.md) | ✔<br>(Prasideda 10.0.12) | |
| [SDK lygio patarimo palaikymas naudojant "Adyen" jungtį](tipping.md) | ✔<br>(Prasideda 10.0.14) | |
| [Papildantysis užsakymų sąskaitų faktūrų išrašymo įrašymas](incremental-capture.md) |  | ✔<br>(Prasideda 10.0.18) |
| [Esa mokėjimus](../wallets.md) |  | ✔<br>(Prasideda 10.0.20) |
| [Algalapių mokėjimas su Adyen](google-pay-adyen.md) |  | ✔<br>(Prasideda 10.0.27) |

## <a name="next-steps"></a>Kiti veiksmai

Daugiau informacijos apie "Dynamics 365 Payment Connector" Adyen pasirašymą ir konfigūravimą ieškokite ["Dynamics 365" mokėjimo jungtyje, skirtoje Adyen nustatymui](adyen-connector-setup.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Payment Connector“, skirto sprendimui „Adyen“, nustatymas](adyen-connector-setup.md)

[DUK apie „Dynamics 365 Payment Connector“, skirto sprendimui „Adyen“](adyen-connector-faq.md)

[„Dynamics 365 Payment Connector“, skirtos sprendimui „Adyen“, trikčių šalinimas](adyen-connector-troubleshoot.md)

[DUK apie mokėjimus](/dynamics365/unified-operations/retail/dev-itpro/payments-retail)

[!INCLUDE [footer-include](../../includes/footer-banner.md)]
