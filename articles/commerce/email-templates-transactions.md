---
title: El. laiškų šablonų, skirtų operacijų įvykiams, kūrimas
description: Šioje temoje aprašoma, kaip kurti, įkelti ir konfigūruoti operacijų įvykių el. laiškų šablonus „Microsoft Dynamics 365 Commerce”.
author: bicyclingfool
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 69ba8821cde6788d6e0accb37288f92acdfc776c
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713802"
---
# <a name="create-email-templates-for-transactional-events"></a>El. laiškų šablonų, skirtų operacijų įvykiams, kūrimas

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šioje temoje aprašoma, kaip kurti, įkelti ir konfigūruoti operacijų įvykių el. laiškų šablonus „Microsoft Dynamics 365 Commerce”.

„Dynamics 365 Commerce“ teikia siunčiamų el. laiškų, kuriuos klientai įspėjami apie operacijų įvykius, siunčiamų siunčiamų pranešimų siuntimo nestandartinį sprendimą. Pavyzdžiui, el. laiškai gali būti siunčiami, kai užsakymas yra pateiktas, paruoštas paimti arba išsiųstas. Šioje temoje aprašomi veiksmai, skirti kurti, įkelti ir konfigūruoti el. laiškų šablonus, naudojamus siunčiant operacijų el. laiškus.

## <a name="notification-types"></a>Pranešimo tipai

Galima konfigūruoti pranešimus, kad jie informuotų klientus el. paštu, kai užsakymo ir kliento ciklo metu įvyksta konkretūs įvykiai. Norėdami konfigūruoti pranešimus, sukurdami komercijos el. paštu siunčiamų pranešimų šabloną, turite susieti el. laiško šabloną su pranešimo tipu. Informacijos, kaip nustatyti el. paštu siunčiamų pranešimų šablonus, ieškokite [El. paštu siunčiamo pranešimo šablono nustatykite](email-notification-profiles.md).

„Dynamics 365 Commerce“ palaiko šiuos pranešimų tipus.

### <a name="order-created"></a>Užsakymas sukurtas

Užsakymo *sukurtas pranešimo* tipas suaktyvinamas, kai „Commerce Headquarters" sukuriamas naujas pardavimo užsakymas.

> [!NOTE]
> Sukurtas užsakymo pranešimo tipas nėra suaktyvintas grynųjų pinigų ir carry operacijų, kurios įvyksta kasos aparato (EKA) terminale, atveju. Šiuo atveju generuojamas el. paštu išsiųstas ir (arba) išspausdintas kvitas. Daugiau informacijos rasite [siųsti el. paštu kvitus iš „Modern POS" (MPOS)](email-receipts.md).

### <a name="order-confirmed"></a>Užsakymas patvirtintas

Užsakymo *patvirtintas pranešimo* tipas suaktyvinamas, kai iš „Commerce Headquarters" sugeneruojamas pardavimo užsakymo patvirtinimo dokumentas „Commerce headquarters“.

### <a name="picking-completed"></a>Paėmimas baigtas

Išrinkimo *pranešimo tipas* suaktyvinamas, kai užsakymo išrinkimo dokumento „Commerce Headquarters" pažymėta kaip baigta.

> [!NOTE]
> Išrinkimo baigto pranešimo tipas nėra suaktyvintas, kai prekė pažymėta kaip paimta EKA terminale.

### <a name="packing-completed"></a>Pakavimas baigtas

Išrinkimo *pakavimo tipas* suaktyvinamas, kai užsakymo važtaraščio dokumentas sukuriamas „Commerce Headquarters" pažymėta EKA terminale.

Baigtas pakavimo pranešimo tipas palaiko šiuos papildomus el. pašto vietos rezervavimo ženklus, kad būtų lengviau "paruošti paimti užsakymą" ir užsakymų peržvalgos funkcijos pagal operacijų el. laiškus.

| Vietos rezervavimo ženklo pavadinimas    | Paskirtis |
| ------------------- | ------- |
| `pickupstorename`     | Parduotuvės, kurioje galima paimti užsakymą, pavadinimas. |
| `pickupstoreaddress`  | Adresas parduotuvės, kurioje galima paimti užsakymą, pavadinimas. |
| `pickupstorehourfrom` | Paėmimo parduotuvės atidarymo valanda. |
| `pickupstorehourto`   | Paėmimo parduotuvės uždarymo valanda. |
| `pickupchannelid`     | Paėmimo parduotuvės kanalo ID. |
| `packingslipid`      | Užsakymo, kuris bus paimtas, važtaraščio ID. |
| `confirmationid`      | Užsakymo patvirtinimo, kuris bus paimtas, važtaraščio ID. (Šis ID kartais vadinamas kanalo nuorodos ID.) |

Daugiau informacijos apie kliento įregistravimo ir užsakymų peržvalgos funkcijas žr. [Nustatyti geografinio aptikimo ir nukreipimo nustatymą](geo-detection-redirection.md) ir [Įjungti užsakymo paieškos svečio išregistravimus](order-lookup-guest.md).

### <a name="order-ready-for-pickup"></a>Užsakymas paruoštas atsiimti

*Užsakymas, paruoštas paėmimo* pranešimo tipui, suaktyvinamas, kai užsakymas pažymėtas kaip supakuotas, o pristatymo būdas nustatytas kaip **Kliento paėmimas** vienoje ar daugiau užsakymo eilučių.

> [!NOTE]
> Paruoštas paimti užsakymo pranešimo tipas pagal pakavimo baigtą pranešimo tipą yra pasenusi. Šis pranešimo tipas tinkinimas pagal pristatymo būdą.

### <a name="order-shipped"></a>Užsakymas išsiųstas

*Užsakymo siuntimo* pranešimo tipas suaktyvinamas, kai išrašoma užsakymo, kuris neturi parduotuvės paėmimo rėžimo SF.

> [!NOTE]
> Paruoštas siųsti užsakymo pranešimo tipas pagal pakavimo baigtą sąskaitoje įtrauktą užsakymą tipą yra pasenusi. Šis pranešimo tipas tinkinimas pagal pristatymo būdą.

### <a name="order-invoiced"></a>Užsakymo sąskaita faktūra išrašyta

Užsakymo *sąskaitoje įtrauktas užsakymas* tipas suaktyvinamas, kai EKA ar „Commerce Headquarters" sukuriamas naujas pardavimo užsakymas.

### <a name="issue-gift-card"></a>Išduoti dovanų kortelę

Išdavimo *išduoti dovanų kortelę* pranešimo tipas suaktyvinamas, kai pardavimo užsakymas, kuriame yra dovanų kortelės tipo produktas, išrašomą SF.

> [!NOTE]
> Išdavimo dovanų kortelės pranešimo el. laiškas išsiųstas dovanų kortelės gavėjui. Dovanų kortelės gavėjas nurodytas „Commerce Headquarters", atskiros pardavimo užsakymo eilutės skirtuko **Važtaraštis** dalyje **Eilutės informacija**. Gali būti nurodyta rankiniu arba programiniu būdu.

Dovanų kortelės išdavimo pranešimo tipas palaiko šiuos papildomus vietos rezervavimo ženklus.

| Vietos rezervavimo ženklo pavadinimas      | Paskirtis |
| --------------------- | ------- |
| `giftcardnumber`        | Dovanų kortelės tipo produktų dovanų kortelės numeris. |
| `giftcardbalance`       | Dovanų kortelės tipo produktų dovanų kortelės balansas. |
| `giftcardmessage`       | Dovanų kortelės tipo produktų dovanų kortelės pranešimas. |
| `giftcardpin`         | Dovanų kortelės tipo produktų dovanų kortelės asmeninis identifikavimo numeris (PIN). (Šis vietos rezervavimo ženklas būdingas išorinėms dovanų kortelėms.) |
| `giftcardexpiration`    | Dovanų kortelės tipo produktų dovanų kortelės galiojimo data. (Šis vietos rezervavimo ženklas būdingas išorinėms dovanų kortelėms.) |
| `giftcardrecipientname` | Dovanų kortelės tipo produktų dovanų kortelės gavėjo vardas. |
| `giftcardbuyername`     | Dovanų kortelės tipo produktų dovanų kortelės pirkėjo vardas. |

Daugiau informacijos apie dovanų korteles žr. [„E-commerce" skaitmeninių dovanų kortelių](digital-gift-cards.md) ir [Išorinių dovanų kortelių palaikymo svetainėje](dev-itpro/gift-card.md).

### <a name="order-cancellation"></a>Užsakymo atšaukimas

Užsakymo *užsakymo atšaukimas* tipas suaktyvinamas, kai užsakymas yra atšauktas „Commerce Headquarters".

### <a name="customer-created"></a>Klientas sukurtas

Užsakymo *sukurtas klientas* tipas suaktyvinamas, kai „Commerce Headquarters" sukuriamas naujas kliento objektas.

### <a name="b2b-prospect-approved"></a>B2B potencialus klientas patvirtintas

Pranešimo tipas *B2B potencialaus kliento* pranešimo tipas suaktyvinamas, kai potencialaus kliento parengimo užklausa patvirtinama "Commerce Headquarters". Daugiau informacijos apie tai, kaip patvirtinti arba atmesti B2B potencialius klientus, ieškokite [Naujo verslo partnerio vartotojo administratoriaus nustatykite](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

B2B perspektyvos patvirtinimo pranešimo tipas palaiko šiuos papildomus vietos rezervavimo ženklus.

| Vietos rezervavimo ženklo pavadinimas | Paskirtis                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`       | Į programą įvedamos B2B potencialaus kliento vardas. |
| `lastname`         | Į programą įvedamos B2B potencialaus kliento pavardė. |
| `company`          | Į programą įvedamos pareiškėjo įmonės potencialaus kliento vardas. |
| `email`            | Į programą el. pašto adresas įvedamas potencialaus kliento pavardė.   |
| `zipcode`          | Asmens pagrindinio adreso pašto kodas. |
| `comments`         | Komentaras, kurį potencialus klientas įvedė į programą. |
| `storename`        | Skalės vieneto kanalas, kuriame buvo sukurtas įrašas. |
| `storeurl`         | Tuščia pagal numatytąjį nustatymą. Norint naudoti šį vietos rezervavimo ženklą, turi būti sukurtas pasirinktinis plėtinys. |

### <a name="b2b-prospect-approved"></a>B2B potencialus klientas patvirtintas

Pranešimo tipas *B2B atmestas klientas* pranešimo tipas suaktyvinamas, kai potencialaus kliento parengimo užklausa patvirtinama „Commerce Headquarters". Daugiau informacijos apie tai, kaip patvirtinti arba atmesti B2B potencialius klientus, ieškokite [Naujo verslo partnerio vartotojo administratoriaus nustatykite](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

B2B perspektyvos nepatvirtinto pranešimo tipas palaiko šiuos papildomus vietos rezervavimo ženklus.

| Vietos rezervavimo ženklo pavadinimas | Paskirtis                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`        | Į programą įvedamos B2B potencialaus kliento vardas. |
| `lastname`         | Į programą įvedamos B2B potencialaus kliento pavardė. |
| `company`          | Į programą įvedamos pareiškėjo įmonės potencialaus kliento vardas. |

## <a name="create-an-email-template"></a>El. laiško šablono kūrimas

Kad galėtumėte susieti konkretų operacijų įvykį su el. laiško šablonu, turite sukurti šabloną.

Norėdami sukurti el. pašto šabloną, atlikite toliau nurodytus veiksmus.

1. „Commerce“ valdymo srityje eikite į **Mažmeninė prekyba ir komercija \> Valdymo srities sąranka \> Įmonės el. laiškų šablonai** arba **Įmonės administravimas\> Sąranka \> Įmonės el. laiškų šablonai**.
1. Pasirinkite **Naujas**.
1. Dalyje **Bendra** nustatykite tolesnius laukus.

    - **El. laiško ID** – el. pašto ID yra unikalus šablono identifikatorius. Tai vertė, rodoma, kai pasirenkate šabloną, kurį norite susieti su įvykiu.
    - **El. pašto aprašas** – šį pasirinktinį lauką galite naudoti norėdami pateikti šablono aprašymą. Įvesta reikšmė rodoma tik „Commerce“ pagrindiniame komponente.
    - **Siuntėjo vardas** – vardas, kurį įvedate, rodomas daugelio el. pašto klientų lauke „Nuo”.
    - **Siuntėjo el. paštas** – įveskite el. pašto adresą, kuris turėtų būti naudojamas el. laiškams, siunčiamiems naudojant šį šabloną.
    - **Numatytasis kalbos kodas** – šis laukas nurodo pagal numatytuosius nustatymus siunčiamo el. laiško lokalizuotą versiją, jei kanalas, iškviečiantis šį šabloną, nepateikia kalbos.

1. Dalyje **El. laiško turinys** pasirinkite **Naujas**.
1. Lauke **Kalba** įveskite el. laiško šablono kalbą. Galite įtraukti daugiau kalbų ir lokalizuotų šablonų vėliau.
1. Lauke **Tema** įveskite el. laiško temą, kuri turėtų būti rodoma el. laiško temos lauke.
1. Pasirinkite **Redaguoti**, kad įkeltumėte el. laiško šabloną.

## <a name="create-an-email-message-body-by-using-html"></a>El. laiško teksto kūrimas naudojant HTML

El. laiško tekstas sudarytas HTML formatu. Galite naudoti bet kurį maketą, stilių ir prekės ženklus, kuriuos leidžia HTML ir įdėtieji pakopinio stiliaus aprašai (CSS). Taip pat galite naudoti vaizdus, jei juos laikote viešai pasiekiamame tinklo galiniame punkte. Norėdami įtraukti vaizdą, įveskite vaizdo URL HTML žymės **&lt;img&gt;** atribute **src**.

> [!NOTE]
> El. pašto klientai įveda maketo ir stiliaus apribojimus, dėl kurių gali reikėti atlikti HTML ir CSS, naudojamų pranešimo tekste, koregavimus. Rekomenduojame susipažinti su geriausia HTML kūrimo praktika, kurią palaikys populiariausi el. pašto klientai.

## <a name="add-placeholders-to-the-email-message-body"></a>Vietos rezervavimo ženklų įtraukimas į el. laiško tekstą

El. laiške gali būti vietos rezervavimo ženklų, kurie pakeičiami konkretaus kliento ir konkrečių operacijų reikšmėmis, kai el. laiškas sugeneruojamas. Vietos rezervavimo ženklai abiejose jų pusėse visada yra procento ženklai (%) įterpiami tiesiai į HTML dokumentą.

Toliau pateikiamas pavyzdys.

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Užsakymo vietos rezervavimo ženklai (pardavimo užsakymo lygiu)

Tolesni vietos rezervavimo ženklai nuskaito ir rodo duomenis, nurodytus pardavimo užsakymo lygiu (o ne pardavimo eilutės lygiu).

| Vietos rezervavimo ženklo pavadinimas     | Paskirtis                                                      |
| -------------------- | ------------------------------------------------------------ |
| `customername`         | Kliento, kuris pateikė užsakymą, vardas.               |
| `customeraddress`      | Kliento adresas.                                 |
| `customeremailaddress` | El. pašto adresas, kurį klientas įvedė išsiregistruodamas.     |
| `salesid`              | Užsakymo pardavimo ID.                                   |
| `orderconfirmationid`  | Kuriant užsakymą sugeneruotas kryžminio kanalo ID.   |
| `channelid`            | Mažmeninės prekybos arba interneto kanalo, per kurį buvo pateiktas užsakymas, ID. |
| `deliveryname`         | Pristatymo adresui nurodytas pavadinimas.         |
| `deliveryaddress`      | Išsiųstų užsakymų pristatymo adresas.                     |
| `deliverydate`         | Pristatymo data.                                           |
| `shipdate`             | Siuntimo data.                                               |
| `modeofdelivery`       | Užsakymo pristatymo būdas.                              |
| `ordernetamount`       | Bendroji užsakymo suma, atėmus bendrą mokesčių sumą.         |
| `discount`            | Bendra užsakymo nuolaida.                            |
| `charges`              | Bendros užsakymo išlaidos.                             |
| `tax`                  | Bendra užsakymo mokesčių suma.                                 |
| `total`                | Bendroji užsakymo suma.                              |
| `storename`            | Parduotuvės, kurioje buvo pateiktas užsakymas, pavadinimas.            |
| `storeaddress`         | Parduotuvės, pateikusios užsakymą, adresas.              |
| `storeopenfrom`        | Parduotuvės, pateikusios užsakymą, atidarymo laikas.         |
| `storeopento`          | Parduotuvės, pateikusios užsakymą, uždarymo laikas.         |
| `pickupstorename`      | Parduotuvės, kurioje bus paimtas užsakymas, pavadinimas.\*   |
| `pickupstoreaddress`   | Parduotuvės, kurioje bus paimtas užsakymas, adresas.\* |
| `pickupopenstorefrom`  | Parduotuvės, kurioje bus paimtas užsakymas, atidarymo laikas.\* |
| `pickupopenstoreto`    | Parduotuvės, kurioje bus paimtas užsakymas, uždarymo laikas.\* |
| `pickupchannelid`     | Parduotuvės kanalo ID, nurodytas pristatymo paėmimo režimui.\* |
| `packingslipid`        | Važtaraščio, kuris buvo sugeneruotas pakuojant užsakymo eilutes, ID.\* |

\*Šie vietos rezervavimo ženklai grąžina duomenis tik tada, kai jie naudojami **užsakymui paruoštame paėmimo** pranešimo tipui. 

### <a name="order-line-placeholders-sales-line-level"></a>Užsakymo eilučių vietos rezervavimo ženklai (pardavimo eilutės lygiu)

Tolesni vietos rezervavimo ženklai nuskaito ir rodo atskirų produktų (eilučių) duomenis pardavimo užsakyme.

| Vietos rezervavimo ženklo pavadinimas               | Paskirtis |
|--------------------------------|-------------------|
| `productid`                      | <p>Produkto ID. Šios variantų ID sąskaitos.</p><p><strong>Pastaba:</strong> šis vietos rezervavimo ženklas buvo pasenusi `lineproductrecid` už eilutėje.</p> |
| `lineproductrecid`               | Produkto ID. Šios variantų ID sąskaitos. Ji unikaliai identifikuoja prekę varianto lygiu. |
| `lineitemid`                     | Produkto lygio produkto ID. (Šis ID neskaičiuoja variantų.) |
| `lineproductvariantid`           | Produkto varianto ID. |
| `lineproductname`                | Produkto pavadinimas. |
| `lineproductdescription`         | Produkto aprašymas. |
| `linequantity`                   | Užsakytų eilutės vienetų skaičius ir matavimo vienetas (pvz., **ea** arba **pora**). |
| `lineunit`                       | Eilutės matavimo vienetas. |
| `linequantity_withoutunit`       | Užsakytų eilutės vienetų skaičius be matavimo vieneto. |
| `linequantitypicked`             | Kai naudojamas įvykis **PickOrder**, tai paimtų vienetų skaičius. Kitu atveju tai **0** (nulis). |
| `linequantitypicked_withoutunit` | Kai naudojamas įvykis **PickOrder**, tai paimtų vienetų skaičius be matavimo vieneto. Kitu atveju tai **0** (nulis). |
| `linequantitypacked`             | Kai naudojami įvykiai **PackOrder** ir **Užsakymas paruoštas paėmimui**, tai supakuotų vienetų skaičius. Kitu atveju tai **0** (nulis). |
| `linequantitypacked_withoutuom`  | Kai naudojami įvykiai **PackOrder** ir **Užsakymas paruoštas paėmimui**, tai supakuotų vienetų skaičius be matavimo vieneto. Kitu atveju tai **0** (nulis). |
| `linequantityshipped`            | Visada **0**, išskyrus atvejus, kai naudojami konkretūs įvykiai, kaip aprašyta tolesnėje eilutėje. |
| `linequantityshipped_withoutuom` | Kai naudojamas įvykis **ShipOrder**, tai paimtų vienetų skaičius be matavimo vieneto. Kitu atveju tai **0** (nulis). |
| `lineprice`                      | Atskiro vieneto kaina. |
| `linenetamount`                  | Eilutės kaina po vienetų skaičiaus ir nuolaidos taikymo. |
| `linediscount`                   | Nuolaida atskiram vienetui. |
| `lineshipdate`                   | Eilutės siuntimo data. |
| `linedeliverydate`               | Eilutės pristatymo data. |
| `linedeliverymode`               | Eilutės pristatymo būdas. |
| `linedeliveryaddress`            | Eilutės pristatymo adresas. |
| `linepickupdate`                 | Kliento nurodyta paėmimo data užsakymams, kurie naudoja pristatymo paėmimo režimą. |
| `linepickuptimeslot`             | Kliento nurodytas paėmimo laikas užsakymams, kurie naudoja pristatymo paėmimo režimą. |
| `giftcardnumber`                 | Dovanų kortelės tipo produktų dovanų kortelės numeris. |
| `giftcardbalance`                | Dovanų kortelės tipo produktų dovanų kortelės balansas. |
| `giftcardmessage`                | Dovanų kortelės tipo produktų dovanų kortelės pranešimas. |
| `giftcardpin`                    | Dovanų kortelės PIN produktų dovanų kortelės balansas. (Šis vietos rezervavimo ženklas būdingas išorinėms dovanų kortelėms.) |
| `giftcardexpiration`             | Dovanų kortelės tipo produktų dovanų kortelės galiojimo data. (Šis vietos rezervavimo ženklas būdingas išorinėms dovanų kortelėms.) |
| `giftcardrecipientname`          | Dovanų kortelės tipo produktų dovanų kortelės gavėjo vardas. |
| `giftcardbuyername`              | Dovanų kortelės tipo produktų dovanų kortelės pirkėjo vardas. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Užsakymo eilučių vietos rezervavimo ženklų formatas el. laiško tekste

Kurdami atskirų užsakymo eilučių el. laiško tekste HTML, apsupkite pasikartojantį HTML bloką ir eilučių vietos rezervavimo ženklus tolesniais vietos rezervavimo ženklais, pateikiamais HTML komentarų žymėse. Atkreipkite dėmesį, kad vietos rezervavimo ženklai yra HTML komentarų žymių viduje.

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

Toliau pateikiamas pavyzdys.

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>El. paštu siunčiamų kvitų šablono kūrimas

Kvitus galima siųsti el. paštu klientams, perkantiems mažmeninės prekybos elektroniniame kasos aparate (EKA). Paprastai veiksmai, skirti el. paštu siunčiamų kvitų šablonui kurti, yra tokie patys kaip veiksmai, skirti kitų operacijų įvykių šablonams kurti. Tačiau būtini tolesni keitimai.

- **%message%** tarpas yra naudojamas įteprti tekstą į gavėjo į el. laišką. Kad užtikrintumėte, jog kvito tekstas tinkamai atvaizduotas, apsupkite **%message%** rezervavimo ženklą HTML žymėmis **&lt;pre&gt;** ir **&lt;/pre&gt;**.
- Rezervavimo ženklą **%receiptid%** galima naudoti QR kodui arba brūkšniniam kodui, nurodančiam gavimo ID, rodyti. (QR kodus ir brūkšninius kodus dinamiškai generuoja ir pristato trečiosios šalies tarnyba.) Norėdami gauti daugiau informacijos apie tai, kaip rodyti QR kodą arba brūkšninį kodą el. paštu siunčiamame kvite, žr. skyrių [QR kodo arba brūkšninio kodo pridėjimas prie sandorių ir gavimo el. laiškų](add-qr-code-barcode-email.md).

## <a name="upload-the-email-html"></a>El. laiško HTML nusiuntimas

Sukūrę ir išbandę jūsų laiško teksto HTML, turite jį nusiųsti į „Commerce“ pagrindinį komponentą. Šiuo metu negalima eksportuoti el. laiškų HTML. Todėl turite tvarkyti jūsų HTML pagrindinę kopiją ne „Commerce“ pagrindiniame komponente.

Norėdami nusiųsti naują ar redaguotą el. laiško šablono HTML, atlikite tolesnius veiksmus.

1. „Commerce“ pagrindiniame komponente eikite į **Mažmeninė prekyba ir prekyba \> Pagrindinio komponento sąranka \> Organizacijos el. laiškų šablonai**.
1. Pasirinkite kalbos, kuriai norite įtraukti arba pakeisti HTML, eilutę. Taip pat galite pasirinkti **Naujas**, kad sukurtumėte naujos kalbos eilutę.
1. Pasirinkite **Redaguoti**.
1. Pasirodžiusiame dialogo lange pasirinkite **Naršyti**. Eikite į HTML dokumentą, kurį norite įkelti, pasirinkite jį ir pasirinkite **Atidaryti**.
1. Pasirinkite **Nusiųsti**.
1. Po to, kai jūsų el. pašto HTML pasirodys peržiūros lange, pasirinkite **Gerai**.
1. Įsitikinkite, kad pažymėtas eilutės žymės langelis **Yra teksto**.

Jeigu jau sukonfigūravote „Commerce” pagrindinį komponentą, kad galėtumėte siųsti el. laiškus, naujas arba atnaujintas el. laiškas bus išsiųstas visiems klientams, vykdantiems operaciją, iškviečiančią su šablonu susietą įvykį.

Daugiau informacijos apie tai, kaip konfigūruoti el. laiškus „Dynamics 365 Commerce”, žr. [El. laiškų konfigūravimas ir siuntimas](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Papildomi ištekliai 

[El. paštu siunčiamo pranešimo šablono nustatymas](email-notification-profiles.md)

[El. pašto konfigūravimas ir siuntimas](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[El. paštu siunčiamų kvitų nustatymas](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Kvitų iš „Modern POS“ siuntimas el. paštu](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
