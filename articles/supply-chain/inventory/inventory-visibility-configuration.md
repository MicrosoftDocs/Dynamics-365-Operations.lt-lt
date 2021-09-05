---
title: Atsargų matomumo konfigūravimas
description: Šioje temoje aprašoma, kaip konfigūruoti atsargų matomumą.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 92e42b22d424ab80303d771f760cfcf0599b9f4c
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345038"
---
# <a name="inventory-visibility-configuration"></a>Atsargų matomumo konfigūravimas

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Šioje temoje aprašoma, kaip konfigūruoti atsargų matomumą.

## <a name="introduction"></a><a name="introduction"></a>Įžanga

Prieš pradėdami dirbti su atsargų matomumu, turite užbaigti šią konfigūraciją, kaip aprašyta šioje temoje:

- [Duomenų šaltinio konfigūravimas](#data-source-configuration)
- [Skaidinio konfigūracija](#partition-configuration)
- [Produkto indeksų hierarchijos konfigūracija](#index-configuration)
- [Rezervavimo konfigūracija (pasirinktinai)](#reservation-configuration)
- [Numatytosios konfigūracijos pavyzdys](#default-configuration-sample)

> [!NOTE]
> Galite peržiūrėti ir redaguoti atsargų matomumo konfigūracijas [„Microsoft Power Apps“](./inventory-visibility-power-platform.md#configuration). Baigę konfigūruoti programoje pasirinkite **Naujinti konfigūraciją**.

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Duomenų šaltinio konfigūravimas

Duomenų šaltinis rodo sistemą, iš kurios gauti jūsų duomenys. Pavyzdžiai `fno` (tai reiškia „Dynamics 365 Finance and Operations "programėles") ir `pos` (tai reiškia "point of sale").

Duomenų šaltinio konfigūraciją sudaro toliau nurodytos dalys:

- Dimensija (dimensijos susiejimas)
- Fizinis matas
- Apskaičiuotas matas

> [!NOTE]
> Duomenų `fno`šaltinis rezervuotas „Dynamics 365 Supply Chain Management“.

### <a name="dimension-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensija (dimensijos susiejimas)

Nurodymo konfigūravimo tikslas yra standartizuoti daugelio sistemų integravimą užklausai, įvykių publikavimas pagal dimensijų kombinacijas.

Atsargų matomumas palaiko šias bendrąsias bazines dimensijas.

| Dimensijos tipas | Pagrindinė dimensija |
|---|---|
| Produktas | `ColorId` |
| Produktas | `SizeId` |
| Produktas | `StyleId` |
| Produktas | `ConfigId` |
| Sekimas | `BatchId` |
| Sekimas | `SerialId` |
| Buvimo vieta | `LocationId` |
| Buvimo vieta | `SiteId` |
| Atsargų būsena | `StatusId` |
| Sandėliui konkretus | `WMSLocationId` |
| Sandėliui konkretus | `WMSPalletId` |
| Sandėliui konkretus | `LicensePlateId` |
| Kita | `VersionId` |
| Atsargos (muitinės) | `InventDimension1` per `InventDimension12` |
| Papildomas telefonas | `ExtendedDimension1` per `ExtendedDimension8` |

> [!NOTE]
> Dimensijos tipai įrašyti ankstesnėje lentelėje tik nuorodų tikslais. Nereikia jų nustatyti atsargų matomumo dalyje.
>
> Atsargų (pasirinktinės) dimensijos gali būti rezervuotos „Supply Chain Management“. Tokiu atveju vietoj jo galite naudoti išplėsti dimensijas.

Išorinės sistemos gali pasiekti atsargų matomumą per savo RESTful API. Integravimui atsargų matomumas leidžia konfigūruoti _išorinį duomenų šaltin_ ir išorinių dimensijų  _susiejimą su_ su  _bazinėmis dimensijomis_. Čia pateikiamas statistinės dimensijos pavyzdys.

| Išorinė dimensija | Pagrindinė dimensija |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Konfigūruodami dimensijų konvertavimą, išorines dimensijas galite siųsti tiesiogiai į atsargų matomumą. Tada atsargų matomumas automatiškai konvertuos išorines dimensijas į bazines dimensijas.

### <a name="physical-measures"></a>Fizinis matas

Faktinės priemonės modifikuoja kiekį ir atspindi atsargų būseną. Atsižvelgdami į savo poreikius galite apibrėžti savo fizinius priemones.

Atsargų matomumas pateikia numatytųjų fizinių priemonių, susietų su „Supply Chain Management“ (duomenų `fno` šaltiniu), sąrašą. Šioje lentelėje pateikiamas faktinių priemonių pavyzdys.

| Fizinio mato pavadinimas | Aprašas |
|---|---|
| `NotSpecified` | Nenurodytas |
| `Arrived` | Pristatyta |
| `AvailOrdered` | Galimas užsakytas |
| `AvailPhysical` | Faktiškai turima |
| `Deducted` | Išskaičiuota |
| `OnOrder` | Užsakyta |
| `Ordered` | Užsakyta |
| `PhysicalInvent` | Faktinės atsargos |
| `Picked` | Paimta |
| `PostedQty` | Užregistruotas kiekis |
| `QuotationIssue` | Pasiūlyta išduoti |
| `QuotationReceipt` | Pasiūlymo gavimas |
| `Received` | Gauta |
| `Registered` | Užregistruota |
| `ReservOrdered` | Užsakyta rezervuotų |
| `ReservPhysical` | Faktiškai rezervuota |

### <a name="calculated-measures"></a><a name="data-source-configuration-calculated-measure"></a>Apskaičiuoti matai

Skaičiuojami reiškia pritaikytą skaičiavimo formulę, kurią sudaro fizinių priemonių derinys. Ši funkcija paprasčiausiai leidžia jums nustatyti priemonės rinkinį, kuris bus įtrauktas ir (arba) nustatys priemones išimtas siekiant suformuoti tinkintą priemonę.

Pavyzdžiui, turite šių pirkimo užsakymų rezultatas.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]
```

Tada konfigūruojate apskaičiuotą `MyCustomAvailableforReservation` matą, pavadintą, kaip parodyta pateiktoje lentelėje. Šį apskaičiuotą matą suvartoja suvartojimo sistema.

| Vartojimo sistema | Apskaičiuotas matas | Duomenų šaltinis | Fizinis matas | Skaičiavimo tipas |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `received` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `scheduled` | `Addition` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `issued` | `Subtraction` |
| `CustomChannel` | `MyCustomAvailableforReservation` | `externalchannel` | `reserved` | `Subtraction` |

Kai naudojama ši skaičiavimo formulė, naujuose užklausos rezultatuose bus pritaikytas matavimas.

```json
[
    {
        "productId": "T-shirt",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red"
        },
        "quantities": {
            "pos": {
                "inbound": 80.0,
                "outbound": 20.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "externalchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Išvestis `MyCustomAvailableforReservation` paremta apskaičiavimo nustatymais tinkintuose matavimuose, yra 100 + 50 + 80 + 90 + 30 – 10 – 20 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Skaidinio konfigūracija

Skaidinio konfigūraciją sudaro pagrindinės dimensijos derinys. Jis nurodo duomenų paskirstymo trafaretą. Duomenų operacijos tame pačiame skaidinyje palaiko aukštą našumą ir per daug nekainoti. Todėl tinkami skaidinio modeliai gali turėti didelės naudos.

Atsargų matomumas suteikia tokią numatytąją skaidinio konfigūraciją.

| Pagrindinė dimensija | Hierarchija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

> [!NOTE]
> Numatytoji skaidinio konfigūracija skirta tik nuorodai. Nereikia jų nustatyti atsargų matomumo dalyje. Šiuo metu skaidinio konfigūracijos naujinimas nepalaikomas.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Produkto indeksų hierarchijos konfigūracija

Dažniausiai turimų atsargų užklausa nebus tik aukščiausias "bendras" lygis. Vietoje to jūs galite norėti matyti rezultatus, kurie yra sujungti pagal atsargų dimensijas.

Atsargų matomumas suteikia lankstumo, informuodamas apie tai, kaip nustatote _indeksus_. Šie indeksai remiasi dimensija arba dimensijų kombinacija. Indeksą sudaro *rinkinio numeris*, *dimensija* ir *hierarchija*, kaip nurodyta šioje lentelėje.

| Pavadinimas / vardas ir (arba) pavardė | Aprašas |
|---|---|
| Nustatyti numerį | Dimensijos, priklausančios tam pačiam rinkinio (indeksui), bus sugrupuotos ir joms bus priskirtas tas pats rinkinio numeris. |
| Dimensija | Pagrindinės dimensijos, pagal kurias sujungiamas užklausos rezultatas. |
| Hierarchija | Hierarchija naudojama apibrėžti palaikomas dimensijų kombinacijas, kurių galima užklausti. Pvz., nustatote dimensijų rinkinį, kuriame yra hierarchijos seka `(ColorId, SizeId, StyleId)`. Šiuo atveju sistema palaiko užklausas apie keturias dimensijų kombinacijas. Pirmasis derinys yra tuščias, antrasis `(ColorId)`, trečiasis yra `(ColorId, SizeId)`, o ketvirtasis yra `(ColorId, SizeId, StyleId)`. Nepalaikomos kitos kombinacijos. Daugiau informacijos ieškokite šiame pavyzdyje. |

### <a name="example"></a>Pavyzdys

Šiame skyriuje pateikiamas pavyzdys, kuriame parodyta, kaip veikia hierarchija.

Savo atsargose yra šios prekės.

| Produktas | SpalvosID | DydžioID | StiliausID | Kiekis |
|---|---|---|---|---|
| Marškinėliai | Juoda | Mažas | Plati | 1 |
| Marškinėliai | Juoda | Mažas | Reguliarus | 2 |
| Marškinėliai | Juoda | Dideli | Plati | 3 |
| Marškinėliai | Juoda | Dideli | Reguliarus | 4 |
| Marškinėliai | Raudona | Mažas | Plati | 5 |
| Marškinėliai | Raudona | Mažas | Reguliarus | 6 |
| Marškinėliai | Raudona | Dideli | Reguliarus | 7 |

Toliau parodytas indeksas.

| Nustatyti numerį | Dimensija | Hierarchija |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Indeksas leidžia pateikti užklausą apie turimų atsargų informaciją šiais būdais:

- `()`– sugrupuota pagal visus

    - Marškinėliai, 28

- `(ColorId)` – Sugrupuota pagal `ColorId`

    - Marškinėlių, juoda, 10
    - Marškinėlių, raudona, 18

- `(ColorId, SizeId)`– grupuojamas pagal kombinaciją `ColorId` ir `SizeId`

    - Marškinėlių, juoda, mažas 3
    - Marškinėlių, juoda, didelis 7
    - Marškinėlių, raudonas, mažas 11
    - Marškinėlių, raudonas, didelis 7

- `(ColorId, SizeId, StyleId)` – grupuojamas pagal kombinaciją `ColorId`, `SizeId`, ir `StyleId`

    - Marškinėlių, juoda, platus 1
    - Marškinėlių, juoda, įprastas 2
    - Marškinėlių, didelis, platus 3
    - Marškinėlių, didelis, įprastas 4
    - Marškinėlių, raudonas, mažas, platus 5
    - Marškinėlių, raudonas, įprastas 6
    - Marškinėlių, raudonas, didelis, įprastas 7

> [!NOTE]
> Pagrindinės dimensijos, kurios nustatytos skaidinio konfigūracijoje, neturi būti apibrėžtos indekso konfigūracijose.

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Rezervavimo konfigūracija (pasirinktinai)

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Jei norite naudoti funkciją Švelniai rezervavimas, reikia rezervavimo konfigūracijos. Konfigūraciją sudaro dvi pagrindinės dalys:

- Švelniai rezervavimo susiejimas
- Švelni rezervavimo hierarchija

### <a name="soft-reservation-mapping"></a>Švelniai rezervavimo susiejimas

Kai rezervate, galite norėti žinoti, ar šiuo metu turimas atsargas galima rezervuoti. Tikrinimas yra susietas su apskaičiuotu matu, kuris nurodo faktinių matų derinio skaičiavimo formulę.

Pavyzdžiui, rezervavimo matas yra pagrįstas faktiniu `SoftReservOrdered` matais `iv` iš (atsargų matomumo) duomenų šaltinio. Šiuo atveju galite nustatyti apskaičiuotą duomenų `AvailableToReserve` šaltinio `iv` matą, kaip parodyta čia.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `fno` | `AvailPhysical` |
| Priedas | `pos` | `Inbound` |
| Atimtis | `pos` | `Outbound` |
| Atimtis | `iv` | `SoftReservOrdered` |

Tada nustatykite švelniai rezervavimo susiejimą, kad būtų galima pateikti susiejimą iš `SoftReservOrdered` rezervavimo matavimo į apskaičiuotą `AvailableToReserve` matą.

| Faktinio matavimo duomenų šaltinis | Fizinis matas | Galimas rezervavimo duomenų šaltinis | Galimas rezervuoti apskaičiuotas matas |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

Dabar, kai rezervavimui atlikti, atsargų matomumas automatiškai surasti ir su rezervavimo patvirtinimu susijusi `SoftReservOrdered` skaičiavimo `AvailableToReserve` formulė.

Pavyzdžiui, turite šias turimų atsargų matomumo atsargas.

```json
{
    "productId": "T-shirt",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservOrdered": 90
        },
        "fno": {
            "availphysical": 70.0,
        },
        "pos": {
            "inbound": 50.0,
            "outbound": 20.0
        }
    }
}
```

Šiuo atveju taikomas šis skaičiavimas:

`AvailableToReserve` = `fno.availphysical` + `pos.inbound` – `pos.outbound` – `iv.SoftReservOrdered`  
= 70 + 50 – 20 – 90  
= 10

Todėl jei bandysite rezervuoti ir kiekis bus mažesnis arba `iv.SoftReservOrdered` lygus `AvailableToReserve` (10), galėsite atlikti rezervavimą.

### <a name="soft-reservation-hierarchy"></a>Švelni rezervavimo hierarchija

Rezervavimo hierarchija aprašo dimensijų seką, kurią reikia nurodyti rezervuojant. Tai veikia tuo pačiu būdu, kaip produkto hierarchija veikia turimose užklausose.

Rezervavimo hierarchija nepriklauso nuo produkto indeksų hierarchijos. Šis nepriklausomumas leidžia įgyvendinti kategorijų valdymą, kur vartotojai gali suskaidyti dimensijas į išsamią informaciją, kad nustatytų tikslesnių rezervavimų reikalavimus.

Čia pateikiamas švelnios rezervacijos hierarchijos pavyzdys.

| Pagrindinė dimensija | Hierarchija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

Šiame pavyzdyje galite rezervuoti šias dimensijų sekas:

- `()`– nenurodyta jokia dimensija.
- `(SiteId)`
- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Tinkama dimensijų seka turi griežtai laikytis rezervavimo hierarchijos – dimensijos pagal dimensiją. Pavyzdžiui, hierarchijos `(SiteId, LocationId, SizeId)` seka netinkama, nes `ColorId` trūksta.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Numatytosios konfigūracijos pavyzdys

Inicijavimo etapu atsargų matomumas nustato numatytąją konfigūraciją. Jei reikia, konfigūraciją galima modifikuoti.

### <a name="data-source-configuration"></a>Duomenų šaltinio konfigūravimas

#### <a name="configuration-of-the-iv-data-source"></a>Iv duomenų šaltinio konfigūravimas

Šiame skyriuje aprašoma, `iv` kaip konfigūruoti duomenų šaltinį.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Iv duomenų šaltinio sukonfigūruoti faktiniai duomenys

Sukonfigūruoti šie duomenų šaltinio `iv` faktiniai duomenys:

- `Ordered`
- `SoftReservPhysical`
- `SoftReservOrdered`
- `ReservOrdered`
- `ReservPhysical`

##### <a name="orderedtotal-calculated-measure"></a>OrderedTotal apskaičiuotas matas

Tada `OrderedTotal` konfigūruojate matmenį, kuris apskaičiuotas `iv` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `fno` | `Ordered` |
| Priedas | `fno` | `Arrived` |
| Priedas | `iv` | `Ordered` |

##### <a name="onhand-calculated-measure"></a>Turimas apskaičiuotas matmuo

Tada `OnHand` konfigūruojate matmenį, kuris apskaičiuotas `iv` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `fno` | `PhysicalInvent` |
| Priedas | `iom` | `OnHand` |
| Priedas | `erp` | `Unrestricted` |
| Priedas | `erp` | `QualityInspection` |
| Priedas | `pos` | `PosInbound` |
| Atimtis | `pos` | `PosOutbound` |

##### <a name="reservedtotal-calculated-measure"></a>Rezervuota iš viso apskaičiuotas matas

Tada `ReservedTotal` konfigūruojate matmenį, kuris apskaičiuotas `iv` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `fno` | `ReservPhysical` |
| Priedas | `fno` | `ReservOrdered` |
| Priedas | `iv` | `SoftReservPhysical` |
| Priedas | `iv` | `SoftReservOrdered` |
| Priedas | `iv` | `ReservPhysical` |
| Priedas | `iv` | `ReservOrdered` |

##### <a name="softreserved-calculated-measure"></a>Švelniai rezervuota iš viso apskaičiuotas matas

Tada `SoftReserved` konfigūruojate matmenį, kuris apskaičiuotas `iv` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `iv` | `SoftReservPhysical` |
| Priedas | `iv` | `SoftReservOrdered` |

##### <a name="hardreserved-calculated-measure"></a>Stipriai rezervuota iš viso apskaičiuotas matas

Tada `HardReserved` konfigūruojate matmenį, kuris apskaičiuotas `iv` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `fno` | `ReservPhysical` |
| Priedas | `fno` | `ReservOrdered` |
| Priedas | `iv` | `ReservPhysical` |
| Priedas | `iv` | `ReservOrdered` |

##### <a name="openorder-calculated-measure"></a>Atviras užsakymo apskaičiuotas matas

Tada `OpenOrder` konfigūruojate matmenį, kuris apskaičiuotas `iv` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `fno` | `OnOrder` |
| Priedas | `iom` | `OnOrder` |

##### <a name="onhandavailable-calculated-measure"></a>Apskaičiuotas užsakytas matas

Tada `OnHandAvailable` konfigūruojate matmenį, kuris apskaičiuotas `iv` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `fno` | `PhysicalInvent` |
| Priedas | `iom` | `OnHand` |
| Priedas | `erp` | `Unrestricted` |
| Priedas | `erp` | `QualityInspection` |
| Priedas | `pos` | `PosInbound` |
| Atimtis | `fno` | `ReservPhysical` |
| Atimtis | `iv` | `SoftReservPhysical` |
| Atimtis | `pos` | `PosOutbound` |

##### <a name="availabletoreserve-calculated-measure"></a>Prieinamas rezervuoti užsakytas matas

Tada `AvailableToReserve` konfigūruojate matmenį, kuris apskaičiuotas `iv` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `fno` | `PhysicalInvent` |
| Priedas | `iom` | `OnHand` |
| Priedas | `erp` | `Unrestricted` |
| Priedas | `erp` | `QualityInspection` |
| Priedas | `pos` | `PosInbound` |
| Priedas | `fno` | `Ordered` |
| Priedas | `fno` | `Arrived` |
| Priedas | `iv` | `Ordered` |
| Atimtis | `fno` | `ReservPhysical` |
| Atimtis | `fno` | `ReservOrdered` |
| Atimtis | `iv` | `SoftReservPhysical` |
| Atimtis | `iv` | `SoftReservOrdered` |
| Atimtis | `iv` | `ReservPhysical` |
| Atimtis | `iv` | `ReservOrdered` |
| Atimtis | `pos` | `PosOutbound` |

##### <a name="inventorysupply-calculated-measure"></a>Apskaičiuotas Atsargų tiekimo matas

Tada `InventorySupply` konfigūruojate matmenį, kuris apskaičiuotas `iv` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `fno` | `Ordered` |
| Priedas | `fno` | `Arrived` |
| Priedas | `iv` | `Ordered` |
| Priedas | `fno` | `PhysicalInvent` |
| Priedas | `iom` | `OnHand` |
| Priedas | `erp` | `Unrestricted` |
| Priedas | `erp` | `QualityInspection` |
| Priedas | `pos` | `PosInbound` |
| Atimtis | `pos` | `PosOutbound` |

##### <a name="inventorydemand-calculated-measure"></a>Atsargų paklausos apskaičiuotas matas

Tada `InventoryDemand` konfigūruojate matmenį, kuris apskaičiuotas `iv` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `fno` | `OnOrder` |
| Priedas | `iom` | `OnOrder` |
| Priedas | `iv` | `SoftReservPhysical` |
| Priedas | `iv` | `SoftReservOrdered` |
| Priedas | `fno` | `ReservPhysical` |
| Priedas | `fno` | `ReservOrdered` |
| Priedas | `iv` | `ReservPhysical` |
| Priedas | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>Iv duomenų šaltinio fno konfigūravimas

Šiame skyriuje aprašoma, `fno` kaip konfigūruoti duomenų šaltinį.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>Fno duomenų šaltinio dimensijos susiejimai

Toliau pateiktoje lentelėje pateikti dimensijų susiejimai yra sukonfigūruoti duomenų `fno` šaltiniui.

| Išorinė dimensija | Pagrindinė dimensija |
|---|---|
| `InventBatchId` | `BatchId` |
| `InventColorId` | `ColorId` |
| `InventLocationId` | `LocationId` |
| `InventSerialId` | `SerialId` |
| `InventSiteId` | `SiteId` |
| `InventSizeId` | `SizeId` |
| `InventStatusId` | `StatusId` |
| `InventStyleId` | `StyleId` |
| `LicensePlateId` | `LicensePlateId` |
| `WMSLocationId` | `WMSLocationId` |
| `WMSPalletId` | `WMSPalletId` |
| `ConfigId` | `ConfigId` |
| `InventVersionId` | `VersionId` |
| `InventDimension1` | `CustomDimension1` |
| `InventDimension2` | `CustomDimension2` |
| `InventDimension3` | `CustomDimension3` |
| `InventDimension4` | `CustomDimension4` |
| `InventDimension5` | `CustomDimension5` |
| `InventDimension6` | `CustomDimension6` |
| `InventDimension7` | `CustomDimension7` |
| `InventDimension8` | `CustomDimension8` |
| `InventDimension9` | `CustomDimension9` |
| `InventDimension10` | `CustomDimension10` |
| `InventDimension11` | `CustomDimension11` |
| `InventDimension12` | `CustomDimension12` |

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Iv duomenų šaltinio sukonfigūruoti fno faktiniai duomenys

Sukonfigūruoti šie duomenų šaltinio `fno` faktiniai duomenys:

- `Ordered`
- `Arrived`
- `AvailPhysical`
- `PhysicalInvent`
- `ReservPhysical`
- `ReservOrdered`
- `OnOrder`

#### <a name="configuration-of-the-pos-data-source"></a>Iv duomenų šaltinio pos konfigūravimas

Šiame skyriuje aprašoma, `pos` kaip konfigūruoti duomenų šaltinį.

##### <a name="physical-measures-for-the-pos-data-source"></a>Pos duomenų šaltinio sukonfigūruoti faktiniai duomenys

Sukonfigūruoti šie duomenų šaltinio `pos` faktiniai duomenys:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>Prieinamas kiekis apskaičiuotas matas

Tada `AvailQuantity` konfigūruojate matmenį, kuris apskaičiuotas `pos` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
|---|---|---|
| Priedas | `fno` | `AvailPhysical` |
| Priedas | `pos` | `PosInbound` |
| Atimtis | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>iom duomenų šaltinio konfigūravimas

Sukonfigūruoti šie duomenų šaltinio `iom` (protingo užsakymo valdymo) faktiniai duomenys:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>Erp duomenų šaltinio konfigūravimas

Sukonfigūruoti šie duomenų šaltinio `erp` (įmonės šaltinio planavimo) faktiniai duomenys:

- `Unrestricted`
- `QualityInspection`

### <a name="partition-configuration"></a>Skaidinio konfigūracija

Šioje lentelėje rodoma numatytoji skaidinio konfigūracija.

| Pagrindinė dimensija | Hierarchija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

### <a name="index-configuration"></a>Indekso konfigūravimas

Šioje lentelėje rodoma numatytoji indekso konfigūracija.

| Nustatyti numerį | Dimensija | Hierarchija |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

### <a name="reservation-configuration"></a>Rezervavimo konfigūracija

Šiame skyriuje aprašoma numatytoji rezervavimo konfigūracija.

#### <a name="reservation-mapping"></a>Rezervavimo susiejimas

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Šioje lentelėje rodoma numatytoji rezervavimo konfigūracija.

| Faktinio matavimo duomenų šaltinis | Fizinis matas | Galimas rezervavimo duomenų šaltinis | Galimas rezervuoti apskaičiuotas matas |
|---|---|---|---|
| `iv` | `SoftReservOrdered` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Rezervavimo hierarchija

Šioje lentelėje rodoma numatytoji rezervavimo hierarchija.

| Pagrindinė dimensija | Hierarchija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |
| `BatchId` | 6 |
| `SerialId` | 7 |
| `StatusId` | 8 |
| `LicensePlateId` | 9 |
| `WMSLocationId` | 10 |
| `WMSPalletId` | 11 |
| `ConfigId` | 12 |
| `VersionId` | 13 |
| `CustomDimension1` | 14 |
| `CustomDimension2` | 15 |
| `CustomDimension3` | 16 |
| `CustomDimension4` | 17 |
| `CustomDimension5` | 18 |
| `CustomDimension6` | 19 |
| `CustomDimension7` | 20 |
| `CustomDimension8` | 21 |
| `CustomDimension9` | 22 |
| `CustomDimension10` | 23 |
| `CustomDimension11` | 24 |
| `CustomDimension12` | 25 |
| `ExtendedDimension1` | 26 |
| `ExtendedDimension2` | 27 |
| `ExtendedDimension3` | 28 |
| `ExtendedDimension4` | 29 |
| `ExtendedDimension5` | 30 |
| `ExtendedDimension6` | 31 |
| `ExtendedDimension7` | 32 |
| `ExtendedDimension8` | 33 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
