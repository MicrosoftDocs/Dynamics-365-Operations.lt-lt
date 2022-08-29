---
title: "\"Commerce pricing\" API"
description: Šiame straipsnyje aprašomos įvairios kainodaros API, kurias teikia kainodaros Microsoft Dynamics 365 Commerce variklis.
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2022
ms.locfileid: "9293654"
---
# <a name="commerce-pricing-apis"></a>"Commerce pricing" API

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomos įvairios kainodaros API, kurias teikia kainodaros Microsoft Dynamics 365 Commerce variklis.

Kainų Dynamics 365 Commerce nustatymo variklis pateikia tokius "Retail Server" API, kuriuos išorinės programos gali suvartoti, kad palaiky galėtų palaikyti įvairius kainodaros scenarijus:

- **GetActivePrices** – ši API gauna apskaičiuotą produkto kainą, įskaitant paprastas nuolaidas.
- **CalculateSalesDocument** – ši API apskaičiuoja kartu perkamų produktų kainas ir nuolaidas duotais kiekiais.
- **GetAvailablePromotions** – ši API gauna taikomas nuolaidas produktams krepšelyje. 
- **AddCoupons** – ši API įtraukia kuponus į krepšelį.
- **RemoveCoupons** – ši API pašalina kuponus iš krepšelio.

Norėdami gauti daugiau informacijos apie tai, kaip išorinėse programose naudoti "Retail Server" API, žr [. "Retail Server" API naudojimas išorinėse programose](dev-itpro/consume-retail-server-api.md).

## <a name="getactiveprices"></a>GetActivePrices

GetActivePrices *API* buvo įtraukta į "Commerce" 10.0.4 versiją. API gauna apskaičiuotą produkto kainą, įskaitant paprastas nuolaidas. Jis neskaičiuoja kelių eilučių nuolaidų, ir daro prielaidą, kad kiekvieno API užklausos produkto kiekis yra 1. API taip pat gali pateikti produktų sąrašą kaip įvestį ir pateikti užklausą dėl atskirų produktų kainos masiškai.

GetActivePrices *API* palaiko darbuotojo **, kliento**, **anoniminio** **ir** programos **komercijos** vaidmenis.

Pagrindinis getActivePrices *API* naudojimo atvejis yra informacijos apie produktą puslapis (PDP), kur mažmenininkai nori parodyti geriausią produkto kainą, įskaitant visas efektyvias nuolaidas.

Šioje lentelėje rodomi *GETActivePrices API įvesties* parametrai.

| Vardas                                    | Antrinis pavadinimas | Tipas | Būtina / pasirinktinai | Aprašymas |
|-----------------------------------------|----------|------|-------------------|-------------|
| Projekto domenas                           | | Projekcijos domenas | Būtinas | |
|                                         | Kanalo ID | Ilgas | Būtinas | |
|                                         | Katalogo ID | Ilgas | Būtinas | |
| Produkto ID                              | | IEnumerable\<long\> | Būtinas | Produktų, kurių kainas reikia apskaičiuoti, sąrašas. |
| activeDate                              | | DateTimeOffset | Būtinas | Kainų apskaičiavimo data. |
| Kliento ID                              | | eilutė | Pasirinktina | Kliento sąskaitos numeris. |
| affiliationLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | Pasirinktina | Priskyrimo ir lojalumo pakopos. |
|                                         | Priskyrimo Id | Ilgas | Būtinas | Priskyrimo ID. |
|                                         | LoyaltyTierId | Ilgas | Pasirinktina | Lojalumo pakopos ID. |
| apimaImpleDiscountsInContextualPrice | | "bo bo" | Pasirinktina | Nustatykite šį parametrą **kaip teisinga**, jei skaičiuojant kainą reikia įtraukti paprastas nuolaidas. Numatytoji reikšmė yra **klaidinga**. |
| includeVariantPriceRange                | | "bo bo" | Pasirinktina | Nustatykite šį parametrą **kaip** teisingą, jei norite gauti mažiausią ir didžiausią kainą iš visų bendrojo produkto variantų. Numatytoji reikšmė yra **klaidinga**. |
| includeAttainablePricesAndDiscounts     | | "bo bo" | Pasirinktina | Norėdami gauti apmokestinamas kainas **ir** nuolaidas, nustatykite šį parametrą kaip teisingą. Numatytoji reikšmė yra **klaidinga**. |

**Pavyzdžio užklausos tekstas**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**Atsakymo į pavyzdžio tekstas**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>CalculateSalesDocument

API *buvo įtraukta į "Commerce* " 10.0.25 versiją. API apskaičiuoja produktų kainas ir nuolaidas duotais kiekiais, jei jie perkami kartu užsakyme. Skaičiuojant kainą po *CalculateSalesDocument* API atsižvelgiama į vienos eilutės nuolaidas ir kelių eilučių nuolaidas.

Pagrindinis naudojimo atvejis *CalculateSalesDocument* API yra kainų skaičiavimas scenarijuose, kuriuose neišlieka visas krepšelio kontekstas (pvz., pardavimo pasiūlymai). Scenarijams, esantims "Point of sale" (EKA) ir "Commerce e-commerce", taip pat gali būti naudingas šis naudojimo atvejis. Mažesnė bendra kaina, kai krepšelio prekės skaičiuojamos kaip rinkinys (pvz., nerekomenduojamas grupavimas, susieti ar rekomenduojami produktai arba produktai, jau įtraukti į krepšelį) gali padėti klientams į krepšelį įtraukti produktų.

Duomenų modelis, skirtas ir Užklausai, ir *CalculateSalesDocument API atsakymui yra* Krepšelis **·**. Tačiau šios API kontekste duomenų modelis pavadintas **SalesDocument**. Kadangi daugelis ypatybės yra pasirenkamos ir tik kai kurios iš jų daro įtaką kainos skaičiavimui, šioje lentelėje rodomi tik su kainodara susiję laukai. Mes nerekomenduojame į API užklausą įtraukti jokių kitų laukų.

*CalculateSalesDocument API apimtis* yra tik kainų ir nuolaidų skaičiavimas. Į mokesčius ir išlaidas neįeis.

Šioje lentelėje rodomi įvesties parametrai objekte, kuris pavadintas **salesDocument**.

| Vardas             | Antrinis pavadinimas | Tipas | Būtina / pasirinktinai | Aprašymas |
|------------------|----------|------|-------------------|-------------|
| ID               | | eilutė | Būtinas | Pardavimo dokumento identifikatorius. |
| Krepšelio linijos        | | I sąrašas\<CartLine\> | Pasirinktina | Eilučių, kurių kainas ir nuolaidas reikia apskaičiuoti, sąrašas. |
|                  | Produkto ID | Ilgas | Būtina krepšelio srityje | Produkto įrašo ID. |
|                  | ItemId | eilutė | Pasirinktina | Prekės identifikatorius. Jei pateikta reikšmė, ji turi sutapti su parametro **ProductId** reikšme. |
|                  | InventoryDimensionId | eilutė | Pasirinktina | Atsargų dimensijos identifikatorius. Jei pateikta reikšmė, verčių **ItemId** **ir InventoryDimensionId** derinys turi atitikti parametro **ProductId** reikšmę. |
|                  | Kiekis | Dešimtainis | Būtina krepšelio srityje | Produkto kiekis. |
|                  | UnitOfMeasureSymbol | eilutė | Pasirinktina | Produkto vienetas. Pagal numatytuosius nustatymus, jei vertė nėra pateikta, API naudoja produkto pardavimo vienetą. |
| Kliento ID       | | eilutė | Pasirinktina | Kliento sąskaitos numeris. |
| Lojalumo kortelės ID    | | eilutė | Pasirinktina | Lojalumo kortelės identifikatorius. Bet kuri kliento sąskaita, susieta su lojalumo kortele, turi **atitikti parametro CustomerId** vertę (jei ji pateikta). Lojalumo kortelės neįlaikoma, jei ji nerasta arba jos būsena **užblokuota**. |
| AffiliationLines | | I sąrašas\<AffiliationLoyaltyTier\> | Pasirinktina | Priskyrimo lojalumo pakopos eilutės. Jei **pateiktos CustomerId** ir (**arba) LoyaltyCardId** vertės, **atitinkamos priskyrimo lojalumo pakopos eilutės bus sulietos su eilutėmis, kurios pateiktos affiliationLines** vertėje. |
|                  | Priskyrimo Id | Ilgas | Būtina AffiliationLoyaltyTier aprėptis | Priskyrimo įrašo ID. |
|                  | LoyaltyTierId | Ilgas | Būtina AffiliationLoyaltyTier aprėptis | Lojalumo pakopos įrašo ID. |
|                  | AffiliationTypeValue | Int | Būtina AffiliationLoyaltyTier aprėptis | Vertė, nurodanti, ar priskyrimo eilutės **tipas** yra Bendrasis (**0**), **ar lojalumo** tipas (**1**). Jei šis parametras nustatytas **kaip 0**, API **kaip identifikatorių paima priskyrimoId** vertę ir nepaiso LoyaltyTierId **vertės**. Jei nustatyta **1, API** kaip identifikatorių paima LoyaltyTierId **vertę** ir nepaiso AffiliationId **vertės**. |
|                  | Priežasties kodo juostos | Kolekcija\<ReasonCodeLine\> | Būtina AffiliationLoyaltyTier aprėptis | Priežasties kodo eilutės. Šis parametras neturi įtakos kainos skaičiavimui, bet jis būtinas **kaip objekto AffiliationLoyaltyTier** dalis. |
|                  | Kliento ID | eilutė | Būtina AffiliationLoyaltyTier aprėptis | Kliento sąskaitos numeris. |
| Kuponai          | | I sąrašas\<Coupon\> | Pasirinktina | Skaičiuojant kainą negalima atsižvelgti į kuponus, kurie nėra taikomi (neaktyvūs, nebegalioja arba nelaikomi). |
|                  | Kodas | eilutė | Būtina kupono apimtis | Kupono kodas. |
|                  | Kodo ID | eilutė | Pasirinktina | Kupono kodo identifikatorius. Jei pateikta vertė, ji turi sutapti su parametro Kodas **verte**. |
|                  | DiscountOfferId | eilutė | Pasirinktina | Nuolaidos identifikatorius. Jei pateikta vertė, ji turi sutapti su parametro Kodas **verte**. |

**Pavyzdžio užklausos tekstas**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

Visas krepšelio objektas grąžinamas kaip atsakymo tekstas. Norėdami tikrinti kainas ir nuolaidas, turite sutelkti dėmesį į šios lentelės laukus.

| Vardas           | Antrinis pavadinimas | Tipas | Aprašymas |
|----------------|----------|------|--------------|
| Grynoji vertė       | | Dešimtainis | Grynoji viso pardavimo dokumento kaina prieš pradedant taikyti nuolaidas. |
| Nuolaidos suma | | Dešimtainis | Bendra viso pardavimo dokumento nuolaidos suma. |
| TotalAmount    | | Dešimtainis | Bendra viso pardavimo dokumento suma. |
| Krepšelio linijos      | | I sąrašas\<CartLine\> | Suskaičiuotas eilutes, kuriose įtraukta kainų ir nuolaidų informacija. |
|                | Kaina | Dešimtainis | Produkto vieneto kaina. |
|                | Grynoji vertė | Dešimtainis | Grynoji eilutės kaina prieš pradedant taikyti nuolaidas (= *kainos*&times;*kiekis).* |
|                | Nuolaidos suma | Dešimtainis | Nuolaidos suma. |
|                | TotalAmount | Dešimtainis | Galutinis eilutės bendrosios kainos rezultatas. |
|                | PriceLines | I sąrašas\<PriceLine\> | Išsami kainos informacija, įskaitant kainos šaltinį (bazinę kainą, kainos koregavimą ar prekybos sutartį) ir sumą. |
|                | Nuolaidos eilutės | I sąrašas\<DiscountLine\> | Nuolaidos informacija. |

## <a name="getavailablepromotions"></a>GautiAvailablePromotions 

Atsižvelgiant į krepšelį, kuriame yra kelios krepšelio eilutės, *GetAvailablePromotions* API grąžina visas krepšelio eilutėms taikomas nuolaidas. 

Pagrindinis naudojimo " *GetAvailablePromotions* " API atvejis yra krepšelio puslapis, kuriame mažmenininkai nori parodyti pritaikytas nuolaidas arba turimus dabartinio krepšelio kuponus.

Šioje lentelėje rodomi GETAvailablePromotions *API įvesties* parametrai.

| Vardas        | Tipas | Būtina / pasirinktinai | Aprašymas |
|-------------|------|-------------------|-------------|
| raktas         | eilutė | Būtinas | Krepšelio ID. |
| cartLineIds | IEnumerable\<string\> | Pasirinktina | Nustatyti šį parametrą, norint grąžinti tik pasirinktų krepšelio eilučių nuolaidas. |

**Atsakymo į pavyzdžio tekstas**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>Pridėticoupons

AddCoupons *API* palaiko kuponų sąrašo į krepšelį įtraukimą. Įdus kuponus, grąžinamas krepšelio objektas.

Šioje lentelėje rodomi AddCoupons *API įvesties* parametrai.

| Vardas                 | Tipas | Būtina / pasirinktinai | Aprašymas |
|----------------------|------|-------------------|-------------|
| raktas                  | eilutė | Būtinas | Krepšelio ID. |
| Kuponų kodai          | IEnumerable\<string\> | Būtinas | Kupono kodai, kuriuos reikia įtraukti į krepšelį. |
| isLegacyDiscountCode | "bo bo" | Pasirinktina | Norėdami nurodyti, kad kuponas **yra** senesnė už nuolaidos kodą, nustatykite šį parametrą kaip teisingą. Numatytoji reikšmė yra **klaidinga**. |

## <a name="removecoupons"></a>Pašalinticoupons

RemoveCoupons *API* palaiko kuponų iš krepšelio sąrašo pašalinimą. Nuėmus kuponus, jis grąžina krepšelio objektą.

Toliau esančioje lentelėje pateikiami *RemoveCoupons API įvesties* parametrai.

| Vardas        | Tipas | Būtina / pasirinktinai | Aprašymas |
|-------------|------|-------------------|-------------|
| raktas         | eilutė | Būtinas | Krepšelio ID. |
| Kuponų kodai | IEnumerable\<string\> | Būtinas | Kupono kodai, kuriuos reikia pašalinti iš krepšelio. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
