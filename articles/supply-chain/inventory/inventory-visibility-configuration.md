---
title: „Inventory Visibility“ konfigūravimas
description: Šiame straipsnyje aprašoma, kaip konfigūruoti atsargų matomumą.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 915382c14cc9ba89b9d543cfd668a94cecbc0a55
ms.sourcegitcommit: 4f987aad3ff65fe021057ac9d7d6922fb74f980e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/14/2022
ms.locfileid: "9764869"
---
# <a name="configure-inventory-visibility"></a>„Inventory Visibility“ konfigūravimas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip konfigūruoti atsargų matomumą naudojant programą Atsargų matomumas Power Apps.

## <a name="introduction"></a><a name="introduction"></a>Įžanga

Prieš pradėdami dirbti su atsargų matomumu, turite užbaigti šią konfigūraciją, kaip aprašyta šiame straipsnyje:

- [Duomenų šaltinio konfigūravimas](#data-source-configuration)
- [Skaidinio konfigūracija](#partition-configuration)
- [Produkto indeksų hierarchijos konfigūracija](#index-configuration)
- [Rezervavimo konfigūracija (pasirinktinai)](#reservation-configuration)
- [Numatytosios konfigūracijos pavyzdys](#default-configuration-sample)

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami, įdiekite ir nustatykite atsargų matomumo priedą, kaip aprašyta [įdiegti ir nustatyti atsargų matomumą](inventory-visibility-setup.md).

## <a name="the-configuration-page-of-the-inventory-visibility-app"></a><a name="configuration"></a>Atsargų matomumo programos konfigūracijos puslapis

„Power Apps“, puslapyje **Konfigūracijos** [Atsargų matomumo programa](inventory-visibility-power-platform.md) padeda nustatyti turimos konfigūracijos ir soft reservation konfigūraciją. Įdiegus papildinį, numatytoji konfigūracija įtraukia „Microsoft Dynamics 365 Supply Chain Management“ (duomenų `fno` šaltinio vertę). Galite peržiūrėti numatytuosius nustatymus. Be to, atsižvelgdami į savo verslo poreikius ir išorinės sistemos atsargų registravimo reikalavimus, galite modifikuoti konfigūraciją, kad būtų galima standartizuoti būdą, kuriuo atsargų pakeitimai gali būti registruojami, tvarkomi keliose sistemose ir jų bus užklausta. Likusiuose šio straipsnio skyriuose paaiškinama, kaip naudoti kiekvieną konfigūracijos puslapio **dalį**.

Baigę konfigūruoti programoje pasirinkite **Naujinti konfigūraciją** programoje.

## <a name="enable-inventory-visibility-features-in-power-apps-feature-management"></a><a name="feature-switch"></a>Įjungti atsargų matomumo funkcijas „Power Apps“ funkcijų valdymo srityje

Atsargų matomumo priedas prie jūsų diegimo prideda keletą naujų „Power Apps“ funkcijų. Pagal numatytuosius nustatymus šios funkcijos yra išjungtos. Norėdami juos naudoti, atidarykite **konfigūravimo** puslapį ir tada skirtuke **Funkcijų** valdymas įjunkite toliau nurodytas funkcijas, jei reikia.

| Priemonių valdymo pavadinimas | Aprašymas |
|---|---|
| *OnHandReservation* | Ši funkcija leidžia kurti rezervavimus, naudoti rezervavimus ir (arba) nereservuoti nurodytų atsargų kiekių naudojant atsargų matomumą. Dėl daugiau informacijos, žr. [Inventoriaus matomumo rezervavimas](inventory-visibility-reservations.md). |
| *OnHandMostSpecificBackgroundService* | Ši priemonė pateikia produktų atsargų suvestinę kartu su visomis dimensijomis. Atsargų suvestinės duomenys bus periodiškai sinchronizuojami pagal atsargų matomumą. Numatytasis sinchronizavimo dažnumas yra vienas po 15 minučių ir gali būti nustatytas kaip didelis kas 5 minutes. Daugiau informacijos ieškokite Atsargų [suvestinė](inventory-visibility-power-platform.md#inventory-summary). |
| *onHandIndexQueryPreloadBackgroundService* | Ši funkcija leidžia iš anksto įkelti turimų atsargų matomumo užklausas, kad būtų galima surinkti turimų atsargų sąrašus su iš anksto pasirinktomis dimensijomis. Numatytasis sinchronizavimo dažnumas yra kas 15 minučių. Norėdami gauti daugiau informacijos, žr. užklausą [Iš anksto įkelkite supaprastintą turimos informacijos užklausą](inventory-visibility-power-platform.md#preload-streamlined-onhand-query). |
| *OnhandChangeSchedule* | Ši pasirinktinė priemonė įgalina turimo atsargų pakeitimo grafiką ir prieinamų atsargų (ATP) priemones. Daugiau informacijos rasite atsargų matomumo [turimų atsargų keitimo grafike ir prieinamose atsargose](inventory-visibility-available-to-promise.md). |
| *Paskirstymas* | Ši pasirinktinė funkcija leidžia atsargų matomumui apsaugoti (žiedinis skambutis) ir valdyti perrašant. Daugiau informacijos rasite atsargų [matomumo atsargų paskirstyme](inventory-visibility-allocation.md). |
| *Įgalinti sandėlio prekes atsargų matomumo skiltyje* | Ši pasirinktinė funkcija įgalina atsargų matomumą palaikyti prekes, kurios įgalintos sandėlio valdymo procesuose (WMS). Daugiau informacijos ieškokite WMS [prekių atsargų matomumo palaikymas](inventory-visibility-whs-support.md). |

## <a name="find-the-service-endpoint"></a><a name="get-service-endpoint"></a>Paslaugos galinio punkto radimas

Jei nežinote tinkamo atsargų matomumo paslaugos galinio punkto, **·** Power Apps **viršutiniame** dešiniajame kampe atidarykite konfigūracijos puslapį ir pasirinkite Rodyti paslaugos informaciją. Puslapyje bus rodomas tinkamas tarnybos galinis punktas. Taip pat galite rasti galinį punktą ciklo Microsoft Dynamics tarnybose, kaip aprašyta [skyriuje Rasti galinį punktą pagal savo ciklo tarnybų aplinką](inventory-visibility-api.md#endpoint-lcs).

> [!NOTE]
> Netinkamo galinio punkto naudojimas gali sukelti nepavykusį atsargų matomumo diegimą ir klaidas, kai tiekimo grandinės valdymas sinchronizuojamas su atsargų matomumu. Jei nesate tikri, kas yra jūsų galinis punktas, kreipkitės į sistemos administratorių. Galinio punkto URL naudoja tokį formatą:
>
> `https://inventoryservice.<RegionShortName>-il<IsLandNumber>.gateway.prod.island.powerapps.com`

## <a name="data-source-configuration"></a><a name="data-source-configuration"></a>Duomenų šaltinio konfigūravimas

Kiekvienas duomenų šaltinis rodo sistemą, iš kurios gauti jūsų duomenys. Duomenų šaltinių pavadinimai gali būti `fno` (atitinka tiekimo grandinės valdymą) ir `pos` (tai reiškia "point of sale"). Pagal numatytuosius nustatymus „Supply Chain Management“ nustatomas kaip numatytasis duomenų šaltinis (`fno`) atsargų matomumo atveju.

> [!NOTE]
> Duomenų `fno` šaltinis rezervuotas tiekimo grandinės valdymui. Jei jūsų atsargų matomumo priedas yra integruotas `fno` tiekimo grandinės valdymo aplinkoje, rekomenduojame nenaiknti konfigūracijų, susijusių su duomenų šaltiniu.

Norėdami įtraukti duomenų šaltinį, atlikite nurodytus veiksmus.

1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **Konfigūravimo** puslapį.
1. Norėdami įtraukti **duomenų šaltinį**, skirtuke **Duomenų šaltinis** pasirinkite Naujas duomenų šaltinis (pvz., `ecommerce` ar kitą prasmingą duomenų šaltinio ID).

> [!NOTE]
> Kai pridedate duomenų šaltinį, prieš atnaujindami atsargų matomumo tarnybos konfigūraciją būtinai patikrinkite duomenų šaltinio pavadinimą, faktinius matus ir dimensijų susiejimus. Pasirinkę Naujinti konfigūraciją šių parametrų **modifikuoti negalėsite**.

Duomenų šaltinio konfigūraciją sudaro toliau nurodytos dalys:

- Dimensijos (dimensijos susiejimas)
- Fizinis matas
- Apskaičiuoti matai

### <a name="dimensions-dimension-mapping"></a><a name="data-source-configuration-dimension"></a>Dimensijos (dimensijos susiejimas)

Nurodymo konfigūravimo tikslas yra standartizuoti daugelio sistemų integravimą užklausai, įvykių publikavimas pagal dimensijų kombinacijas. Atsargų matomumas pateikia bazinių dimensijų, kurias galima susieti pagal jūsų duomenų šaltinio dimensijas, sąrašą. Per daug tris dimensijas galima susieti.

- Jei tiekimo grandinės valdymą naudojate kaip vieną iš savo duomenų šaltinių, pagal numatytuosius nustatymus 13 dimensijų jau susietos su tiekimo grandinės valdymo standartinėmis dimensijomis. Kitos 12 dimensijų (`inventDimension1` iki `inventDimension12`) taip pat susietos su pasirinktomis tiekimo grandinės valdymo dimensijomis. Likusios aštuonios dimensijos (`ExtendedDimension1` per `ExtendedDimension8`) yra išplėstinės dimensijos, kurias galite susieti su išoriniais duomenų šaltiniais.
- Jei negalite naudoti „Supply Chain Management“ kaip vieno iš savo duomenų šaltinių, galite laisvai susieti dimensijas. Šioje lentelėje rodomas visas galimų dimensijų sąrašas.

> [!NOTE]
> Jei naudojate tiekimo grandinės valdymą ir keičiate numatytuosius tiekimo grandinės valdymo ir atsargų matomumo dimensijų susiejimus, pakeista dimensija nesinchronizuoja duomenų. Todėl jei jūsų dimensija nėra numatytajame dimensijų sąraše ir naudojate išorinį duomenų šaltinį, `ExtendedDimension1``ExtendedDimension8` rekomenduojame naudoti susiejimui atlikti.

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
| Plėtinys | `ExtendedDimension1` per `ExtendedDimension8` |
| System | `Empty` |

> [!NOTE]
> Dimensijų tipai, pateikti ankstesnėje lentelėje, skirti tik jūsų nuorodai. Nereikia jų nustatyti atsargų matomumo dalyje.
>
> Atsargų (pasirinktinės) dimensijos gali būti rezervuotos tiekimo grandinės valdymui. Tokiu atveju naudokite išplėsties dimensijas.

Išorinės sistemos gali pasiekti atsargų matomumą per savo RESTful API. Integravimui atsargų matomumas leidžia konfigūruoti *išorinį duomenų šaltin* ir išorinių dimensijų  *susiejimą su* su  *bazinėmis dimensijomis*. Čia yra dimensijų susiejimo lentelės pavyzdys.

| Išorinė dimensija | Pagrindinė dimensija |
|---|---|
| `MyColorId` | `ColorId` |
| `MySizeId` | `SizeId` |
| `MyStyleId` | `StyleId` |
| `MyDimension1` | `ExtendedDimension1` |
| `MyDimension2` | `ExtendedDimension2` |

Konfigūruodami dimensijų konvertavimą, išorines dimensijas galite siųsti tiesiogiai į atsargų matomumą. Tada atsargų matomumas automatiškai konvertuos išorines dimensijas į bazines dimensijas.

Norėdami dimensijų žemėlapius, atlikite nurodytus veiksmus.

1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **Konfigūravimo** puslapį.
1. Skirtuke **Duomenų šaltinis** pasirinkite duomenų šaltinį, kuriame norite atlikti dimensijos konvertavimą. Tada skyriuje Dimensijų susiejimai **pasirinkite** Įtraukti, kad **būtų** įtraukti dimensijų susiejimai.

    ![Dimensijų žemėlapių įtraukimas](media/inventory-visibility-dimension-mapping.png "Dimensijų žemėlapių įtraukimas")

1. Lauke **Dimensijos pavadinimas** nurodykite šaltinio dimensiją.
1. Lauke **Į bazinę dimensiją** pasirinkite dimensiją iš Atsargų matomumo, kurį norite susieti.
1. Pasirinkite **Įrašyti**.

Pavyzdžiui, jūs jau sukūrėte duomenų šaltinį, pavadintą `ecommerce`, ir jame yra produkto spalvos dimensija. Tokiu atveju, norėdami atlikti susiejimą, `ProductColor`**·**`ecommerce``ColorId` pirmiausia galite įtraukti dimensijos pavadinimą į duomenų šaltinio lauką, o tada pasirinkti lauke **Į pagrindinę dimensiją.**

### <a name="physical-measures"></a><a name="data-source-configuration-physical-measures"></a>Fizinis matas

Kai duomenų šaltinis užregistruoja atsargų pakeitimą į Atsargų matomumą, jis užregistruoja jį naudodamas *faktinius duomenis*. Faktinės priemonės modifikuoja kiekį ir atspindi atsargų būseną. Galite apibrėžti savo fizinius priemones pagal savo poreikius. Užklausos gali būti pagrįstos faktiniais išmes taisyme.

Atsargų matomumas pateikia numatytųjų faktinių priemonių, kurios susietos su tiekimo grandinės valdymu (duomenų `fno` šaltiniu), sąrašą. Šie numatytieji faktiniai duomenys imami iš atsargų operacijų būsenų, esančių tiekimo grandinės valdymo sąrašo puslapyje **Turimos atsargos** puslapyje „Supply Chain Management“ (**Atsargų valdymas \> Užklausos ir ataskaita \> Turimas sąrašas**). Šioje lentelėje pateikiamas faktinių priemonių pavyzdys.

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

Jei jūsų duomenų šaltinis yra Tiekimo grandinės valdymas, nereikia iš naujo kurti numatytųjų faktinių priemonių. Tačiau šiems išoriniams duomenų šaltiniams galite sukurti naujus fizinius veiksmus.

1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **Konfigūravimo** puslapį.
1. Skirtuke **Duomenų šaltinis** pasirinkite duomenų šaltinį, į kuriuos norite įtraukti faktinius duomenis (pvz., duomenų `ecommerce` šaltinį). Tada skyriuje Faktiniai **matai** **pasirinkite** Įtraukti ir nurodykite mato pavadinimą (pvz., `Returned` jei norite įrašyti grąžintus kiekius šiame duomenų šaltinyje į Atsargų matomumas). Įrašykite pakeitimus.

### <a name="calculated-measures"></a>Apskaičiuoti matai

Atsargų matomumo užklausą galite naudoti ir atsargų faktiniams priemonėms, ir *pasirinktiniams apskaičiuoties priemonėms*. Skaičiuojami reiškia pritaikytą skaičiavimo formulę, kurią sudaro fizinių priemonių derinys. Ši funkcija paprasčiausiai leidžia jums nustatyti priemonės rinkinį, kuris bus įtrauktas ir (arba) nustatys priemones išimtas siekiant suformuoti tinkintą priemonę.

> [!IMPORTANT]
> Apskaičiuotas matas yra faktinių matų struktūra. Jos formulė gali apimti tik faktinius priemones be dublikatų, o ne apskaičiuotus išrašus.

Konfigūracija leidžia apibrėžti apskaičiuotų matų formulių rinkinį, kuriame yra priedo arba atimties modifikatoriai, kad būtų gauti bendras suvestinis išeigos kiekis.

Norėdami nustatyti tinkinto skaičiavimo matmenį, atlikite tokius veiksmus.

1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **Konfigūravimo** puslapį.
1. Skirtuke **Apskaičiuotas matas** pasirinkite **Naujas skaičiavimo matas,** kad pridėtumėte apskaičiuotą matą.
1. Nustatykite šiuos naujo apskaičiuoto matavimo laukus:

    - **Naujo apskaičiuoto mato** pavadinimas – įveskite apskaičiuoto matavimo pavadinimą.
    - **Duomenų šaltinis** – pasirinkite duomenų šaltinį, į jį įtraukite naują apskaičiuotą matą. Užklausų sistema yra duomenų šaltinis.

1. Norėdami **prie** naujo apskaičiuoto mato pridėti modifikatorių, pasirinkite Įtraukti.
1. Nustatykite šiuos naujo modifikatoriaus laukus:

    - **Modifikatorius** – pasirinkite modifikatoriaus tipą (*pridėjimas* arba *atimtis*).
    - **Duomenų šaltinis** – pasirinkite duomenų šaltinį, kuriame bus galima rasti modifikatoriaus vertę teikiaį matą.
    - **Matas** – pasirinkite matavimo pavadinimą (iš pasirinkto duomenų šaltinio), kuris teikia modifikatoriaus vertę.

1. Kartokite 5–6 veiksmus, kol įdėsite visus reikalingus modifikatorius ir įbaigsite apskaičiuoto matavimo formulę.
1. Pasirinkite **Įrašyti**.

Pavyzdžiui, madingos prekės įmonė veikia tarp trijų duomenų šaltinių:

- `pos`– atitinka parduotuvės kanalą.
- `fno`– atitinka tiekimo grandinės valdymą.
- `ecommerce`– atitinka jūsų interneto kanalą.

Jei užklausi apie produktą D0002 (Kabinetas) pateikiate užklausą dėl produkto D0002 (kabinetas), 1 teritorijoje, 11 sandėlyje ir dimensijos vertės, `ColorID``Red` galite gauti tokį užklausos rezultatą, kuris rodo atsargų kiekius pagal kiekvieną iš anksto sukonfigūruotą fizinį matą. Tačiau jūs negalite matyti visų jūsų duomenų šaltinių rezervavimo kiekių.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
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
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `inbound` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `pos` | `outbound` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `received` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `scheduled` | `Addition` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `issued` | `Subtraction` |
| `CrossChannel` | `MyCustomAvailableforReservation` | `ecommerce` | `reserved` | `Subtraction` |

Kai naudojama ši skaičiavimo formulė, naujuose užklausos rezultatuose bus pritaikytas matavimas.

```json
[
    {
        "productId": "D0002",
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
            "ecommerce": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CrossChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

Išvestis `MyCustomAvailableforReservation` paremta apskaičiavimo nustatymais tinkintuose matavimuose, yra 100 + 50 – 10 + 80 – 20 + 90 + 30 – 60 – 40 = 220.

## <a name="partition-configuration"></a><a name="partition-configuration"></a>Skaidinio konfigūracija

Šiuo metu skaidinio konfigūraciją sudaro dvi pagrindinės dimensijos (`SiteId` ir `LocationId`) kurios nurodo, kaip paskirstomi duomenys. To paties skaidinio operacijos gali padidinti našumą už mažesnes išlaidas. Toliau pateikiamoje lentelėje rodoma numatytoji skaidinio konfigūracija, kurią teikia atsargų matomumo priedas.

| Pagrindinė dimensija | Hierarchija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |

Sprendimas apima šio skaidinio konfigūraciją pagal numatytuosius nustatymus. *Todėl jums nereikia jų patiems nurodyti*.

> [!IMPORTANT]
> Nepritaikykite numatytosios skaidinio konfigūracijos. Jei jį panaikinsite arba pakeisite, tikėtina, kad įvyko netikėta klaida.

## <a name="product-index-hierarchy-configuration"></a><a name="index-configuration"></a>Produkto indeksų hierarchijos konfigūracija

Dažniausiai turimų atsargų užklausa nebus tik aukščiausias "bendras" lygis. Vietoje to jūs galite norėti matyti rezultatus, kurie yra sujungti pagal atsargų dimensijas.

Atsargų matomumas suteikia lankstumo, leisdamas *jums* nustatyti indeksus, kad jūsų užklausos būtų našumui pagerinti. Šie indeksai remiasi dimensija arba dimensijų kombinacija. Indeksą sudaro *rinkinio numeris*, *dimensija* ir *hierarchija*, kaip nurodyta šioje lentelėje.

| Pavadinimas / vardas ir (arba) pavardė | Aprašas |
|---|---|
| Nustatyti numerį | Dimensijos, priklausančios tam pačiam rinkinio (indeksui), bus sugrupuotos ir joms bus priskirtas tas pats rinkinio numeris. |
| Dimensija | Pagrindinės dimensijos, pagal kurias sujungiamas užklausos rezultatas. |
| Hierarchija | Hierarchija leidžia padidinti konkrečių dimensijų kombinacijų našumą, kai naudojama užklausos parametruose filtruoti ir grupuoti pagal užklausas. Pavyzdžiui, jei nustatote dimensijų `(ColorId, SizeId, StyleId)` rinkinį su hierarchijos seka, sistema gali apdoroti užklausas, susijusias su keturiomis dimensijų kombinacijomis, greičiau. Pirmasis derinys yra tuščias, antrasis `(ColorId)`, trečiasis yra `(ColorId, SizeId)`, o ketvirtasis yra `(ColorId, SizeId, StyleId)`. Kitos kombinacijos nebus dar nesusiduotos. Filtrai ribojami pagal užsakymą, bet turi būti šių dimensijų viduje, jei norite pagerinti jų našumą. Daugiau informacijos ieškokite šiame pavyzdyje. |

Norėdami nustatyti savo produkto hierarchijos indeksą, atlikite šiuos žingsnius.

1. Prisiregistruokite savo „Power Apps“ aplinkoje ir atidarykite **Atsargų matomumas**.
1. Atidarykite **Konfigūravimo** puslapį.
1. Skirtuko **Produkto hierarchijos indeksas** skyriuje **Dimensijų susiejimai** pasirinkite **Įtraukti** įtraukumėte dimensijų susiejimus.
1. Numatyta, kad pateikiamas indeksų sąrašas. Norėdami modifikuoti esamą indeksą, atitinkamo **Redaguoti** ar **Įtraukti** skyriuje pasirinkite Redaguoti arba Įtraukti. Norėdami sukurti naują indeksų rinkinį, pasirinkite **Naujas indeksų rinkinys**. Kiekvienai eilutei iš kiekvieno indeksų rinkinio **dimensijos** lauke pasirinkite iš pagrindinės dimensijos sąrašo. Automatiškai generuojamos šių laukų vertės:

    - **Nustatyti numerį** – Dimensijos, priklausančios tam pačiam grupės (indeksui), bus sugrupuotos ir joms bus priskirtas tas pats rinkinio numeris.
    - **Hierarchija** – hierarchija padidina konkrečių dimensijų kombinacijų našumą, kai naudojama filtruoti ir grupuoti pagal užklausos parametrus.

> [!TIP]
> Nustatydami indeksų hierarchiją atmeskite keletą patarimų:
>
> - Pagrindinės dimensijos, kurios nustatytos skaidinio konfigūracijoje, neturi būti apibrėžtos indekso konfigūracijose. Jei pagrindinė dimensija iš naujo nustatoma indekso konfigūracijoje, pagal šį indeksą užklausos negalėsite pateikti.
> - Jei jums reikia pateikti užklausą apie atsargas, kurios sujungiamos pagal visus dimensijų derinius, tada nustatykite vieną indeksą, kuriame yra pagrindinė dimensija `Empty`.

### <a name="example"></a>Pavyzdys

Šiame skyriuje pateikiamas pavyzdys, kuriame parodyta, kaip veikia hierarchija.

Šioje lentelėje šiame pavyzdyje pateikiamas galimų atsargų sąrašas.

| Elementas | ColorId | SizeId | StyleId | Kiekis |
|---|---|---|---|---|
| D0002 | Juoda | Mažas | Plati | 1 |
| D0002 | Juoda | Mažas | Reguliarus | 2 |
| D0002 | Juoda | Didelis | Plati | 3 |
| D0002 | Juoda | Didelis | Reguliarus | 4 |
| D0002 | Raudona | Mažas | Plati | 5 |
| D0002 | Raudona | Mažas | Reguliarus | 6 |
| D0002 | Raudona | Didelis | Reguliarus | 7 |

Tolesnėje lentelėje parodyta, kaip nustatoma indekso hierarchijos grupė.

| Nustatyti numerį | Dimensija | Hierarchija |
|---|---|---|
| 1 | `ColorId` | 1 |
| 1 | `SizeId` | 2 |
| 1 | `StyleId` | 3 |

Indeksas leidžia pateikti užklausą apie turimų atsargų informaciją šiais būdais:

- `()`– sugrupuota pagal visus

    - D0002, 28

- `(ColorId)` – Sugrupuota pagal `ColorId`

    - D0002, juoda, 10
    - D0002, Raudona, 18

- `(ColorId, SizeId)`– grupuojamas pagal kombinaciją `ColorId` ir `SizeId`

    - D0002, juoda, mažas, 3
    - D0002, juoda, didelis, 7
    - D0002, raudona, mažas, 11
    - D0002, raudona, didelis, 7

- `(ColorId, SizeId, StyleId)` – grupuojamas pagal kombinaciją `ColorId`, `SizeId`, ir `StyleId`

    - D0002, juoda, mažas, platus, 1
    - D0002, juoda, mažas, reguliarus, 2
    - D0002, juoda, didelis, platus, 3
    - D0002, juoda, didelis, reguliarus, 4
    - D0002, raudona, mažas, platus, 5
    - D0002, raudona, mažas, reguliarus, 6
    - D0002, raudona, didelis, reguliarus, 7

## <a name="reservation-configuration-optional"></a><a name="reservation-configuration"></a>Rezervavimo konfigūracija (pasirinktinai)

Jei norite naudoti funkciją Švelniai rezervavimas, reikia rezervavimo konfigūracijos. Konfigūraciją sudaro dvi pagrindinės dalys:

- Švelniai rezervavimo susiejimas
- Švelni rezervavimo hierarchija

### <a name="soft-reservation-mapping"></a>Švelniai rezervavimo susiejimas

Kai rezervate, galite norėti žinoti, ar šiuo metu turimas atsargas galima rezervuoti. Tikrinimas yra susietas su apskaičiuotu matu, kuris nurodo faktinių matų derinio skaičiavimo formulę.

Nustatydami faktinio mato susiejimą su apskaičiuotu matu įgalinate atsargų matomumo tarnybą, kad remiantis faktiniu matu būtų automatiškai tikrinamas rezervavimas.

Prieš pradedant nustatyti šį susiejimą konfigūracijos puslapio skirtukuose Duomenų šaltinis ir Apskaičiuotas **matas** **turi būti nurodyti faktiniai matai,** **·** Power Apps apskaičiuoti matai ir jų šaltiniai (kaip aprašyta anksčiau šiame straipsnyje).

Norėdami nustatyti švelniai rezervavimo susiejimą, atlikite šiuos veiksmus.

1. Nurodyti fizinį matą, kuris naudojamas kaip švelniai rezervavimo matas (pvz., `SoftReservPhysical`).
1. Puslapio skirtuke **Apskaičiuotas matas** nustatykite **Konfigūracija** ir *prieinamą rezervuoti*, kuriame yra AFR skaičiavimo formulė, kurią norite susieti su faktini matu. Pavyzdžiui, galite nustatyti (galima rezervuoti), kad jis būtų susietas su `AvailableToReserve` anksčiau apibrėžtu `SoftReservPhysical` faktiniu matais. Tokiu būdu galite rasti, kuriuos kiekius, kurių `SoftReservPhysical` atsargų būsena yra galima rezervuoti. Toliau pateikiamoje lentelėje rodoma AFR skaičiavimo formulė.

    | Skaičiavimo tipas | Duomenų šaltinis | Fizinis matas |
    |---|---|---|
    | Priedas | `fno` | `AvailPhysical` |
    | Priedas | `pos` | `Inbound` |
    | Atimtis | `pos` | `Outbound` |
    | Atimtis | `iv` | `SoftReservPhysical` |

    Rekomenduojame nustatyti apskaičiuotą matą, kad jame būtų faktinis matas, pagal kurį būtų pagrįstas rezervavimo matas. Tokiu būdu apskaičiuotas matų kiekis bus paveiktas rezervavimo matų kiekio. Todėl šiame pavyzdyje apskaičiuotas `AvailableToReserve` duomenų šaltinio `iv` matas kaip `SoftReservPhysical` komponentas turi turėti `iv` fizinį matą.

1. Atidarykite **Konfigūravimo** puslapį.
1. Skirtuke **Švelnus rezervavimo susiejimas** nustatykite susiejimą su fiziniu matmeniu siekiant apskaičiuoti matą. Ankstesniame pavyzdyje galite naudoti šiuos parametrus, norėdami susieti su `AvailableToReserve` anksčiau apibrėžtu `SoftReservPhysical` fiziniu matais.

    | Faktinio matavimo duomenų šaltinis | Fizinis matas | Galimas rezervavimo duomenų šaltinis | Galimas rezervuoti apskaičiuotas matas |
    |---|---|---|---|
    | `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

    > [!NOTE]
    > Jei negalite redaguoti skirtuko **Švelniai rezervavimas** turite įjungti funkciją *OnHandReservation* skirtuke **Funkcijų valdymas**.

Dabar, kai rezervavimui atlikti, atsargų matomumas automatiškai surasti ir su rezervavimo patvirtinimu susijusi `SoftReservPhysical` skaičiavimo `AvailableToReserve` formulė.

Pavyzdžiui, turite šias turimų atsargų matomumo atsargas.

```json
{
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red"
    },
    "quantities": {
        "iv": {
            "SoftReservPhysical": 90
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

`AvailableToReserve` = `fno.availphysical` + `pos.inbound`– – `pos.outbound``iv.SoftReservPhysical`  
= 70 + 50 – 20 – 90  
= 10

Todėl jei bandysite rezervuoti `iv.SoftReservPhysical` ir `AvailableToReserve` kiekis bus mažesnis arba lygus (10), prašymas rezervuoti bus sėkmingas.

> [!NOTE]
> Kai iškiesite rezervavimo API, galite valdyti rezervavimo tikrinimą nurodydami parametrą Boolean `ifCheckAvailForReserv` užklausos body. Vertė reiškia `True`, kad būtinas tikrinimas, `False` o tikrinimo vertė – nebūtinas tikrinimas (`AvailableToReserve` nors galite baigti neigiamą kiekį, sistema vis tiek jums leis rezervuoti švelniai). Numatytoji vertė yra `True`.

### <a name="soft-reservation-hierarchy"></a>Švelni rezervavimo hierarchija

Rezervavimo hierarchija aprašo dimensijų seką, kurią reikia nurodyti rezervuojant. Tai veikia tuo pačiu būdu, kaip produkto hierarchija veikia turimose užklausose.

Rezervavimo hierarchija nepriklauso nuo produkto indeksų hierarchijos. Šis nepriklausomumas leidžia įgyvendinti kategorijų valdymą, kur vartotojai gali suskaidyti dimensijas į išsamią informaciją, kad nustatytų tikslesnių rezervavimų reikalavimus. Jūsų soft rezervavimo hierarchijoje turi `SiteId` būti komponentai ir kaip `LocationId` komponentai, nes jie sudaro skaidinio konfigūraciją. Rezervuojant reikia nurodyti produkto skaidinį.

Tai – soft reservation hierarchijos pavyzdys.

| Pagrindinė dimensija | Hierarchija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |
| `StyleId` | 5 |

Šiame pavyzdyje galite rezervuoti šias dimensijų sekas. Rezervuojant turite nurodyti produkto skaidinį. Todėl pagrindinė hierarchija, kurią galite naudoti, yra `(SiteId, LocationId)`.

- `(SiteId, LocationId)`
- `(SiteId, LocationId, ColorId)`
- `(SiteId, LocationId, ColorId, SizeId)`
- `(SiteId, LocationId, ColorId, SizeId, StyleId)`

Tinkama dimensijų seka turi griežtai laikytis rezervavimo hierarchijos – dimensijos pagal dimensiją. Pavyzdžiui, hierarchijos `(SiteId, LocationId, SizeId)` seka netinkama, nes `ColorId` trūksta.

## <a name="available-to-promise-configuration-optional"></a>Prieinamų atsargos konfigūracijų (pasirinktinai)

Galite nustatyti atsargų matomumą, kad leisite planuoti būsimus turimų atsargų pakeitimus ir apskaičiuoti prieinamų atsargų (ATP) kiekius. ATP – tai turimos prekės kiekis, kurį galima žadėti klientui kitą laikotarpį. Naudojant šį skaičiavimą gali labai padidėti užsakymo įvykdymo galimybės. Norėdami naudoti šią funkciją, turite ją įgalinti skirtuke **Funkcijų** valdymas ir nustatyti ATP parametrų **skirtuke**. Daugiau informacijos ieškokite turimų [atsargų matomumo grafikuose ir prieinamose atsargose](inventory-visibility-available-to-promise.md).

## <a name="complete-and-update-the-configuration"></a>Baigti ir atnaujinti konfigūraciją

Baigę konfigūruoti turite įvykdyti visus atsargų matomumo keitimus. Norėdami fiksuoti pakeitimus, atlikite šiuos veiksmus.

1. Konfigūracijos Power Apps puslapyje, **viršutiniame** dešiniajame **kampe**, pasirinkite Naujinti konfigūraciją. 
1. Sistema reikalauja prisijungimo kredencialų. Įveskite šias vertes:

    - **Kliento ID** – „Azure" programos ID, kurį sukūrėte atsargų matomumui.
    - **Nuomininko ID** – jūsų „Azure" nuomininko ID.
    - **Kliento raktas** – „Azure" programos raktą, kurį sukūrėte atsargų matomumui.

    Norėdami gauti daugiau informacijos apie šiuos kredencialus ir kaip juos rasti, žr [. Įdiekite ir nustatykite atsargų matomumą](inventory-visibility-setup.md).

    > [!IMPORTANT]
    > Prieš atnaujindami konfigūraciją būtinai patikrinkite duomenų šaltinio pavadinimą, faktinius matus ir dimensijų susiejimus. Atnaujinę šiuos parametrus negalėsite modifikuoti.

1. Prisiregistrę dar kartą pasirinkite **Naujinti konfigūraciją**. Sistema taiko jūsų parametrus ir parodo, kas pasikeitė.

## <a name="default-configuration-sample"></a><a name="default-configuration-sample"></a>Numatytosios konfigūracijos pavyzdys

Inicijavimo etapu atsargų matomumas nustato numatytąją konfigūraciją, kuri aprašyta čia. Jei reikia, konfigūraciją galima modifikuoti.

### <a name="data-source-configuration"></a>Duomenų šaltinio konfigūravimas

#### <a name="configuration-of-the-iv-data-source"></a>Iv duomenų šaltinio konfigūravimas

Šiame skyriuje aprašoma, `iv` kaip konfigūruoti duomenų šaltinį.

##### <a name="physical-measures-configured-for-the-iv-data-source"></a>Sukonfigūruoti "iv" duomenų šaltinio faktiniai duomenys

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
| Pridėjimas | `fno` | `ReservPhysical` |
| Pridėjimas | `fno` | `ReservOrdered` |
| Pridėjimas | `iv` | `ReservPhysical` |
| Pridėjimas | `iv` | `ReservOrdered` |

#### <a name="configuration-of-the-fno-data-source"></a>"fno" duomenų šaltinio konfigūracija

Šiame skyriuje aprašoma, `fno` kaip konfigūruoti duomenų šaltinį.

##### <a name="dimension-mappings-for-the-fno-data-source"></a>"fno" duomenų šaltinio dimensijos susiejimai

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

##### <a name="physical-measures-configured-for-the-fno-data-source"></a>Sukonfigūruoti "fno" duomenų šaltinio faktiniai matai

Sukonfigūruoti šie duomenų šaltinio `fno` faktiniai duomenys:

- `Arrived`
- `PhysicalInvent`
- `ReservPhysical`
- `onorder`
- `notspecified`
- `availordered`
- `availphysical`
- `picked`
- `postedqty`
- `quotationreceipt`
- `received`
- `ordered`
- `ReservOrdered`

#### <a name="configuration-of-the-pos-data-source"></a>EKA duomenų šaltinio konfigūracija

Šiame skyriuje aprašoma, `pos` kaip konfigūruoti duomenų šaltinį.

##### <a name="physical-measures-for-the-pos-data-source"></a>EKA duomenų šaltinio faktiniai duomenys

Sukonfigūruoti šie duomenų šaltinio `pos` faktiniai duomenys:

- `PosInbound`
- `PosOutbound`

##### <a name="availquantity-calculated-measure"></a>Prieinamas kiekis apskaičiuotas matas

Tada `AvailQuantity` konfigūruojate matmenį, kuris apskaičiuotas `pos` duomenų šaltiniui, kaip parodyta šioje lentelėje.

| Skaičiavimo tipas | Duomenų šaltinis | Fizinė priemonė |
|---|---|---|
| Pridėjimas | `fno` | `AvailPhysical` |
| Pridėjimas | `pos` | `PosInbound` |
| Atimtis | `pos` | `PosOutbound` |

#### <a name="configuration-of-the-iom-data-source"></a>"iom" duomenų šaltinio konfigūracija

Sukonfigūruoti šie duomenų šaltinio `iom` (protingo užsakymo valdymo) faktiniai duomenys:

- `OnOrder`
- `OnHand`

#### <a name="configuration-of-the-erp-data-source"></a>"erp" duomenų šaltinio konfigūracija

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

Šioje lentelėje rodoma numatytoji rezervavimo konfigūracija.

| Faktinio matavimo duomenų šaltinis | Fizinis matas | Galimas rezervavimo duomenų šaltinis | Galimas rezervuoti apskaičiuotas matas |
|---|---|---|---|
| `iv` | `SoftReservPhysical` | `iv` | `AvailableToReserve` |

#### <a name="reservation-hierarchy"></a>Rezervavimo hierarchija

Šioje lentelėje rodoma numatytoji rezervavimo hierarchija.

| Pagrindinė dimensija | Hierarchija |
|---|---|
| `SiteId` | 1 |
| `LocationId` | 2 |
| `ColorId` | 3 |
| `SizeId` | 4 |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
