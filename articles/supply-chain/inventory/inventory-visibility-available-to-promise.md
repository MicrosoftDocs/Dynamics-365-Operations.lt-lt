---
title: Turimų atsargų matomumo grafikai ir prieinamos atsargos
description: Šioje temoje aprašoma, kaip planuoti būsimus turimos atsargos pakeitimus ir apskaičiuoti prieinamų atsargų (ATP) kiekius.
author: yufeihuang
ms.date: 05/11/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-04
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 7456f87bede7bd0073223fa4762f96f919799e06
ms.sourcegitcommit: 38d97efafb66de298c3f504b83a5c9b822f5a62a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/17/2022
ms.locfileid: "8763259"
---
# <a name="inventory-visibility-on-hand-change-schedules-and-available-to-promise"></a>Turimų atsargų matomumo grafikai ir prieinamos atsargos

[!include [banner](../includes/banner.md)]

Šioje temoje *aprašoma*, kaip nustatyti turimos atsargose pakeitimo grafiko priemonę, kad būtų galima suplanuoti būsimus turimos atsargos pakeitimus ir apskaičiuoti prieinamų atsargų (ATP) kiekius. ATP – tai turimos prekės kiekis, kurį galima žadėti klientui kitą laikotarpį. Naudojant šį skaičiavimą gali labai padidėti užsakymo įvykdymo galimybės.

Daugeliui gamintojų, mažmenininkų ar pagal ką nors daugiau sužinoti, kas šiuo metu yra, nepakanka. Jos turi būti visiškai matomos ateityje. Šis pasiekiamumas turi atsižvelgti į būsimą tiekimą, būsimą poreikį ir ATP.

## <a name="enable-and-set-up-the-features"></a><a name="setup"></a> Įjungti ir nustatyti funkcijas

Prieš naudodami ATP turite nustatyti vieną ar daugiau apskaičiuotų priemonių ATP kiekiams apskaičiuoti. Taip pat turite įjungti funkciją ir konfigūruoti ATP parametrus Microsoft Power Apps.

### <a name="set-up-calculated-measures-for-atp-quantities"></a>Nustatyti APSKAIČIUOtus ATP kiekių priemones

*ATP apskaičiuotas matas* yra iš anksto nustatytas apskaičiuotas matas, kuris paprastai naudojamas dabar turimas kiekiui rasti. Tiekimo *kiekis* *yra* kiekių suma, skirta tiems faktiniams priemonėms, kurių modifikatoriaus tipas yra Pridėjimo tipas, o poreikio kiekis yra šių fizinių priemonių, kurių modifikatoriaus *tipas yra Atimtis,* *kiekių suma.*

Norėdami apskaičiuoti kelis ATP kiekius, galite pridėti keletą apskaičiuotų priemonių. Tačiau bendras atskirų fizinių priemonių skaičius visose ATP apskaičiuotose priemonėse turi būti mažesnis nei devyni.

> [!IMPORTANT]
> Apskaičiuotas matas yra faktinių matų struktūra. Jos formulė gali apimti tik faktinius priemones be dublikatų, o ne apskaičiuotus išrašus.

Pvz., nustatote tokį apskaičiuotą matą:

**Turimos turimos prekės** = (*PhysicalInvent* + *OnHand* + *·* + *neužfiksuotas QualityInspection* + *Inbound*) – (*ReservPhysical* + *SoftReservePhysical* + *Outbound*)

Suma (PhysicalInvent *OnHand* + *atlaisvintas QualityInspection* + *Gavimas* + *) rodo tiekimą, o suma (* + *ReservPhysical* *SoftReservePhysical* + *Outbound* + *·*) atitinka poreikį. Todėl apskaičiuotą matą galima suprasti taip:

**Turimas tiekimas** = *–* *poreikis*

Norėdami apskaičiuoti turimo faktinio **ATP kiekį, galite pridėti kitą apskaičiuotą** matą.

**Turimos turimos prekės** = (*PhysicalInvent* + *OnHand* + *neapidaręs* + *QualityInspection Inbound* + *·*) – (*Siunčiama*)

Tarp šių dviejų ATP apskaičiuotų priemonių yra aštuoni skirtingi faktiniai priemonės: PhysicalInvent, OnHand *,* Unrestricted *,* QualityInspection *,* Inbound *,* ReservPhysical *,* SoftReservePhysical *ir* Outbound *.* *·*

Daugiau informacijos apie apskaičiuotus matus ieškokite Apskaičiuoti [matai](inventory-visibility-configuration.md#calculated-measures).

### <a name="turn-on-the-on-hand-change-schedule-feature-and-configure-atp-settings"></a>Įjungti turimos informacijos pakeitimo grafiko funkciją ir konfigūruoti ATP parametrus

Norėdami įjungti ir konfigūruoti *ATP parametrus, atlikite šiuos* veiksmus, norėdami įjungti Power Apps turimos informacijos pakeitimo grafiko funkciją.

1. Prisiregistruokite Power Apps ir atidarykite Atsargų matomumas.
1. Atidarykite **Konfigūravimo** puslapį.
1. Funkcijų valdymo **skirtuke** įjunkite funkciją *OnhandChangeSchedule*.
1. **Pasirinkite ATP parametrų skirtuką**.
1. Kai užklausiate atsargų matomumo, ji pateikia rezultatą, kuriame yra kiekvienas ČIA įtraukiamas ATP apskaičiuotas matas. Pasirinkite **Įtraukti**, norėdami įtraukti naują apskaičiuotą ATP matą.
1. Užpildykite toliau nurodytus laukus:

    - **Duomenų šaltinis** – pasirinkite duomenų šaltinį, susietą su apskaičiuotu matu.
    - **Apskaičiuotas matas** – pasirinkite apskaičiuotą matą, susietą su pasirinktu duomenų šaltiniu ir kurį norite naudoti turimam kiekiui rasti.
    - **Planuoti laikotarpį** – įveskite dienų skaičių, per kurį vartotojai gali peržiūrėti ir pateikti suplanuotus turimos vertės pakeitimus, kai naudojamas pasirinktas apskaičiuotas matas. Vartotojai, kurie užklausą dėl atsargų informacijos gaus turimo kiekio, suplanuotus turimo kiekio pakeitimus ir ATP kiekvienai šio laikotarpio dienai, pradedant dabartine data. Pasirinkite 1–7 skaičių.

    > [!IMPORTANT]
    > Į grafiko laikotarpį įtraukta dabartinė data. Todėl vartotojai gali suplanuoti, kad turimos atsargų pakeitimai įvyktų bet kuriuo metu nuo esamos datos (pakeitimo pateikimo) iki (grafiko laikotarpis – 1) dienų ateityje.

1. Pasirinkite **Įrašyti**.
1. Kartokite 5–7 veiksmus, kol pridėsite visus apskaičiuotus veiksmus, kurių reikia ATP.
1. Baigę konfigūruoti visus reikiamus parametrus, pasirinkite Naujinti **konfigūraciją**.

Daugiau informacijos rasite Atlikta [ir atnaujinti konfigūraciją](inventory-visibility-configuration.md).

## <a name="how-the-on-hand-change-schedule-and-atp-calculations-work"></a>Kaip veikia turimos atsargų pakeitimo grafikas ir ATP skaičiavimai

Turimos *atsargų pakeitimo grafike nustatomos* numatytos datos ir suplanuotų bei turimų atsargų pakeitimų kiekiai. Galite pateikti turimų atsargų keitimo grafiką į atsargų matomumą, jei datos yra to laikotarpio, **kuris** apibrėžtas grafiko laikotarpio nustatyme ([žr](#setup). skyrių Įgalinti ir nustatyti funkcijas). Vartotojai, kurie užklausą dėl atsargų informacijos gaus turimo kiekio, suplanuotus turimo kiekio pakeitimus ir ATP kiekvienai to laikotarpio dienai.

Suplanuoti pakeitimai iš pradžių yra neįvesti ir todėl neturi įtakos jūsų faktiniams turimi sistemos kiekiams. Norėdami fiksuoti pakeitimus, turite pateikti turimo *kiekio pakeitimo įvykį*, kuris atnaujina faktinį turimo kiekio kiekį. Tada turite grąžinti suplanuotą pakeitimą pateikdami turimo kiekio keitimo grafiką, turimo neigiamam kiekiui.

Pavyzdžiui, jūs negalite pristatyti 10 užsakymo pagal ką ir tikitės, kad jis bus pristatytas rytojaus metu. Todėl jūs pateikiate turimo pakeitimo grafiką, kurio gaunamas kiekis yra 10 ir kurio data rytojui. Kai užsakymas atvyksta kitą dieną, pridedate pereidami prie faktinių turimų atsargų. Tada turite užfiksuoti sistemos pakeitimą, kad būtų galima atnaujinti faktinį turimo kiekio kiekį. Norėdami fiksuoti pakeitimą, pateikiate turimo pakeitimo įvykį, kurio gaunamas kiekis yra 10. Tada, pateikdami turimo kiekio keitimo grafiką, kurio gaunamas kiekis -10, turite grąžinti suplanuotą pakeitimą.

Užklaususi apie turimų atsargų matomumą ir ATP kiekius, pateikia šią kiekvienos grafiko laikotarpio dienos informaciją:

- **Data** – data, taikoma rezultatui. Laiko juosta yra universalusis laikas (UTC).
- **Turimo kiekio** – faktinis kiekis nurodytą datą. Šis skaičiavimas apskaičiuojamas pagal ATP apskaičiuotą matą, kuris sukonfigūruotas atsargų matomumui nustatyti.
- **Suplanuotas** tiekimas – visų suplanuotų gaunamų kiekių, kurie iki nurodytos datos nebuvo faktiškai galimi skubiam suvartojimui arba siuntimui, suma.
- **Suplanuotas** poreikis – visų suplanuotų siunčiamų kiekių, kurie nebuvo suvartoti arba išsiųsti nurodytą datą, suma.
- **ATP kiekis** – minimalus planuotas turimas kiekis, galimas nuo nurodytos datos iki grafiko laikotarpio pabaigos. Šis kiekis apima visus suplanuoto kiekio koregavimus. Didžiausias kiekis, kurį galima žadėti dabartine pristatymo ar suvartojimo data tą dieną.

Pavyzdžiui, jei šiandien yra 2022 m. vasario 1 d., o grafiko laikotarpis yra 7, vartotojai gali pateikti suplanuotus turimos informacijos pakeitimus, kurie numatomi atlikti nuo 2022 m. vasario 1 d. iki vasario 7 d. Šiuo atveju, vasario 3 d. ATP kiekis, pavyzdžiui, skaičiuojamas pagal tos dienos turimą kiekį ir suplanuotus kiekius nuo vasario 3 d. iki vasario 7 d.

## <a name="example"></a>Pavyzdys

Toliau pateikiamas pavyzdys rodo, kaip suplanuoto kiekio pakeitimų serija daro įtaką turimo kiekio ir ATP kiekiams, kurie nurodyti atsargų matomumo ataskaitose. Taip pat rodoma, kaip atlikti suplanuotą pakeitimą, kaip fiksuoto grafiko pakeitimas veikia rezultatus ir kas gali įvykti, jei neatimsite suplanuoto pakeitimo.

Šiame pavyzdyje pateikti rezultatai rodo *, kuri turi būti, turimos* vertės projektą. Ši vertė įtraukia visus suplanuotus atnaujinimus, kad būtų galima naudoti pavyzdį, bet iš tikrųjų ji nėra pateikiama užklausoje Atsargų matomumas.

1. AtP parametrų puslapyje jūsų **sistemai sukonfigūruoti šie** parametrai Power Apps:

    - **ATP apskaičiuotas matas** – turite apskaičiuotą matą, kuris vadinamas *Turimose išlaidose*. Jis apskaičiuotas kaip Turimos *= Tiekimas – Poreikis*. Tą matą pasirenkate čia.
    - **Planuoti laikotarpį** – pasirenkate *7*.

1. Taip pat taikomos šios sąlygos:

    - Esama data yra 2022 m. vasario 1 d.
    - Dabar turimos prekės kiekis yra 20.

1. Šią dieną (2022 m. vasario 1 d.) pateikiate suplanuotą 3 poreikio kiekį į atsargų matomumą. Todėl minimalus turimo kiekio kiekis yra 17. Toliau pateikiamoje lentelėje rodomas rezultatas.

    | Data | Turimos atsargos | Suplanuotas tiekimas | Suplanuota paklausa | Projekto turimos išlaidos | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | | | 17 | 17 |
    | 2022-02-04 | 20 | | | 17 | 17 |
    | 2022-02-05 | 20 | | | 17 | 17 |
    | 2022-02-06 | 20 | | | 17 | 17 |
    | 2022-02-07 | 20 | | | 17 | 17 |

1. Šią dieną (2022 m. vasario 1 d.) pateikiate 2022 m. vasario 3 d. suplanuotą tiekimo kiekį, kuris yra 10. Toliau pateikiamoje lentelėje rodomas rezultatas.

    | Data | Turimos atsargos | Suplanuotas tiekimas | Suplanuota paklausa | Projekto turimos išlaidos | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 17 |
    | 2022-02-02 | 20 | | | 17 | 17 |
    | 2022-02-03 | 20 | 10 | | 27 | 27 |
    | 2022-02-04 | 20 | | | 27 | 27 |
    | 2022-02-05 | 20 | | | 27 | 27 |
    | 2022-02-06 | 20 | | | 27 | 27 |
    | 2022-02-07 | 20 | | | 27 | 27 |

1. Šią dieną (2022 m. vasario 1 d.) pateikiate šiuos suplanuoto kiekio pakeitimus:

    - 2022 m. vasario 4 d. poreikio kiekis – 15
    - 2022 m. vasario 5 d. 1 tiekimo kiekis
    - 2022 m. vasario 6 d. 3 tiekimo kiekis

    Toliau pateikiamoje lentelėje rodomas rezultatas.

    | Data | Turimos atsargos | Suplanuotas tiekimas | Suplanuota paklausa | Projekto turimos išlaidos | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 20 | | 3 | 17 | 12 |
    | 2022-02-02 | 20 | | | 17 | 12 |
    | 2022-02-03 | 20 | 10 | | 27 | 12 |
    | 2022-02-04 | 20 | | 15 | 12 | 12 |
    | 2022-02-05 | 20 | 1 | | 13 | 13 |
    | 2022-02-06 | 20 | 3 | | 16 | 16 |
    | 2022-02-07 | 20 | | | 16 | 16 |

1. Šią dieną (2022 m. vasario 1 d.) nuųsite suplanuotą 3 poreikio kiekį. Todėl šį pakeitimą turite padaryti taip, kad jis atspindėtų faktinį turimo kiekio kiekį. Norėdami fiksuoti pakeitimą, pateikiate turimo pakeitimo įvykį, kurio siunčiamas kiekis yra 3. Tada, pateikdami turimo kiekio keitimo grafiką, kurio siuntimo kiekis - 3, turite grąžinti suplanuotą pakeitimą. Toliau pateikiamoje lentelėje rodomas rezultatas.

    | Data | Turimos atsargos | Suplanuotas tiekimas | Suplanuota paklausa | Projekto turimos išlaidos | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-01 | 17 | | 0 | 17 | 12 |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | 15 | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |

1. Kitą dieną (2022 m. vasario 2 d.) grafiko laikotarpis pasislinks viena diena į priekį. Toliau pateikiamoje lentelėje rodomas rezultatas.

    | Data | Turimos atsargos | Suplanuotas tiekimas | Suplanuota paklausa | Projekto turimos išlaidos | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-02 | 17 | | | 17 | 12 |
    | 2022-02-03 | 17 | 10 | | 27 | 12 |
    | 2022-02-04 | 17 | | 15 | 12 | 12 |
    | 2022-02-05 | 17 | 1 | | 13 | 13 |
    | 2022-02-06 | 17 | 3 | | 16 | 16 |
    | 2022-02-07 | 17 | | | 16 | 16 |
    | 2022-02-08 | 17 | | | 16 | 16 |

1. Tačiau, po dviejų dienų (2022 m. vasario 4 d.), tiekimo kiekis 10, kuris buvo suplanuotas vasario 3 d., dar nėra pristatytas. Toliau pateikiamoje lentelėje rodomas rezultatas.

    | Data | Turimos atsargos | Suplanuotas tiekimas | Suplanuota paklausa | Projekto turimos išlaidos | ATP |
    | --- | --- | --- | --- | --- | --- |
    | 2022-02-04 | 17 | | 15 | 2 | 2 |
    | 2022-02-05 | 17 | 1 | | 3 | 3 |
    | 2022-02-06 | 17 | 3 | | 6 | 6 |
    | 2022-02-07 | 17 | | | 6 | 6 |
    | 2022-02-08 | 17 | | | 6 | 6 |
    | 2022-02-09 | 17 | | | 6 | 6 |
    | 2022-02-10 | 17 | | | 6 | 6 |

    Kaip matote, suplanuoti (bet ne fiksuoti) turimi pakeitimai neturi įtakos faktiniam turimo kiekio kiekiui.

## <a name="submit-change-schedules-change-events-and-atp-queries-through-the-api"></a><a name="api-urls"></a> Pateikti keitimo grafikus, keisti įvykius ir ATP užklausas naudojant API

Norėdami pateikti turimos informacijos keitimo grafikus, keisti įvykius ir užklausas, galite naudoti šiuos programos programavimo sąsajos (API) URL.

| Kelias | Metodas | Aprašymas |
| --- | --- | --- |
| `/api/environment/{environmentId}/onhand/changeschedule` | `POST` | Kurti vieną suplanuotą turimos dalies pakeitimą. |
| `/api/environment/{environmentId}/onhand/changeschedule/bulk` | `POST` | Kurti kelis suplanuotus turimos informacijos pakeitimus. |
| `/api/environment/{environmentId}/onhand` | `POST` | Sukurti vieną turimos informacijos pakeitimo įvykį. |
| `/api/environment/{environmentId}/onhand/bulk` | `POST` | Kurti kelis pakeitimo įvykius. |
| `/api/environment/{environmentId}/onhand/indexquery` | `POST` | Užklausa naudojant `POST` metodą. |
| `/api/environment/{environmentId}/onhand` | `GET` | Užklausa naudojant `GET` metodą. |

Norėdami gauti daugiau informacijos, žr. [atsargų matomumo viešas API](inventory-visibility-api.md).

### <a name="create-one-on-hand-change-schedule"></a>Kurti vieną turimos informacijos pakeitimo grafiką

Turimų atsargų pakeitimo `POST` grafikas sukuriamas pateikiant užklausą atitinkamiems atsargų matomumo paslaugos URL ([žr. keitimo grafikų, keitimo įvykių ir ATP užklausas API](#api-urls) skyriuje). Taip pat galite pateikti masinių užklausų.

Turimos informacijos pakeitimo grafiką galima sukurti tik tada, jei suplanuota data yra tarp dabartinės datos ir dabartinio grafiko laikotarpio pabaigos. Datetime formatas turi būti *metai (pvz* ., **2022-02-01**). Laiko formatas turi būti tikslus tik dienai.

API sukuria vieną turimos informacijos pakeitimo grafiką.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        id: string,
        organizationId: string,
        productId: string,
        dimensionDataSource: string, # optional
        dimensions: {
            [key:string]: string,
        },
        quantitiesByDate: {
            [datetime:datetime]: {
                [dataSourceName:string]: {
                    [key:string]: number,
                },
            },
        },
    }
```

Šiame pavyzdyje rodomas turinio pavyzdžio turinys `dimensionDataSource`.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId&quot;: &quot;Small"
    },
    "quantitiesByDate":
    {
        "2022-02-01": // today
        {
            "pos":{
                "inbound": 10
            }
        }
    }
}
```

### <a name="create-multiple-on-hand-change-schedules"></a>Kurti kelių turimos informacijos keitimo grafikus

API gali kurti kelis įrašus vienu metu. Vienintelis skirtumas tarp šios API ir vieno įvykio API yra ir `Path``Body` vertės. Šiai API `Body` pateikiamas įrašų masyvas. Maksimalus įrašų skaičius yra 512. Todėl turimos atsargų pakeitimo grafiko buferinės API gali palaikyti iki 512 suplanuotų pakeitimų.

```txt
Path:
    /api/environment/{environmentId}/onhand/changeschedule/bulk
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    [
        {
            id: string,
            organizationId: string,
            productId: string,
            dimensionDataSource: string,
            dimensions: {
                [key:string]: string,
            },
            quantityDataSource: string, # optional
            quantitiesByDate: {
                [datetime:datetime]: {
                    [dataSourceName:string]: {
                        [key:string]: number,
                    },
                },
            },
        },
        ...
    ]
```

Šiame pavyzdyje rodomas turinio pavyzdžio turinys.

```json
[
    {
        "id": "id-bike-0001",
        "organizationId": "usmf",
        "productId": "Bike",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-01": // today
            {
                "pos":{
                    "inbound": 10
                }
            }
        }
    },
    {
        "id": "id-car-0002",
        "organizationId": "usmf",
        "productId": "Car",
        "dimensions": {
            "SiteId": "1",
            "LocationId": "11",
            "ColorId": "Red",
            "SizeId&quot;: &quot;Small"
        },
        "quantitiesByDate":
        {
            "2022-02-05":
            {
                "pos":{
                    "outbound": 10
                }
            }
        }
    }
]
```

### <a name="create-on-hand-change-events"></a>Kurti vieną turimos informacijos pakeitimo įvykius

Turimų atsargų pakeitimo `POST` įvykiai atliekami pateikiant užklausą atitinkamiems atsargų matomumo paslaugos URL ([žr. keitimo grafikų, keitimo įvykių ir ATP užklausas API](#api-urls) skyriuje). Taip pat galite pateikti masinių užklausų.

> [!NOTE]
> Turimų atsargų pakeitimo įvykiai nėra unikalūs ATP funkcijoms, bet yra standartinių atsargų matomumo API dalis. Šis pavyzdys įtrauktas, nes įvykiai yra svarbūs, kai dirbate su ATP. Turimos informacijos pakeitimo įvykiai yra panašūs į turimos informacijos keitimo rezervavimus, tačiau įvykių pranešimus reikia siųsti į kitą API URL ir įvykius, `quantities``quantityByDate` kurie naudojami vietoje pranešimo teksto. Daugiau informacijos apie turimų atsargų pakeitimo įvykius ir kitas atsargų matomumo API funkcijas ieškokite [atsargų matomumo viešuose API](inventory-visibility-api.md#create-one-onhand-change-event).

Toliau pateikiamas pavyzdys rodo užklausos instituciją, kurioje yra vienas turimos informacijos keitimo įvykis.

```json
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "SizeId": "Big",
        "ColorId": "Red"
    },
    "quantities": {
        "pos": {
            "inbound": 10.0
        }
    }
}
```

## <a name="query-the-scheduled-on-hand-changes-and-atp-results"></a>Pateikti užklausą dėl suplanuotų turimos informacijos keitimų ir ATP rezultatų

Galite pateikti suplanuotų turimos informacijos pakeitimų ir ATP rezultatų užklausą pateikdami užklausą arba užklausą atitinkamas API URL (`POST` žr. pakeitimo grafikų pateikimą, keitimų įvykius ir ATP `GET`[užklausas api](#api-urls) skyriuje).

Savo užklausoje nustatykite `QueryATP` kaip *teisingas*, jei norite pateikti užklausą dėl suplanuotų turimos informacijos keitimų ir ATP rezultatų.

- Jei pateikiate užklausą naudodami metodą `GET`, nustatykite šį parametrą URL lauke.
- Jei užklausą pateikiate naudodami šį metodą `POST`, nustatykite šį parametrą užklausos body.

> [!NOTE]
> Neatsižvelgiant į tai, `returnNegative`*·* *ar* parametras užklausos sąstate nustatytas kaip teisingas ar klaidingas, rezultatuose bus neigiamos vertės, kai užklausoje bus nustatyti suplanuoti turimo atsargų pakeitimai ir ATP rezultatai. Šios neigiamos vertės bus įtrauktos, nes, jei suplanuoti tik poreikio užsakymai, arba jei tiekimo kiekiai yra mažesni nei poreikio kiekiai, suplanuoti turimi pakeisti kiekiai bus neigiami. Jei neigiamos vertės nebuvo įtrauktos, rezultatai bus priinioti. Norėdami gauti daugiau informacijos apie šią pasirinktį ir kaip ji veikia kitų tipų užklausoms, žr [. atsargų matomumo viešąsias API](inventory-visibility-api.md#query-with-post-method).

```txt
Path:
    /api/environment/{environmentId}/onhand/indexquery
Method:
    Post
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Body:
    {
        dimensionDataSource: string, # Optional
        filters: {
            organizationId: string[],
            productId: string[],
            siteId: string[],
            locationId: string[],
            [dimensionKey:string]: string[],
        },
        groupByValues: string[],
        returnNegative: boolean,
    }
```

Toliau pateikiamas pavyzdys rodo, kaip sukurti užklausos instituciją, kurią galima pateikti atsargų matomumui naudojant `POST` metodą.

```json
{
    "filters": {
        "organizationId": ["usmf"],
        "productId": ["Bike"],
        "siteId": ["1"],
        "LocationId": ["11"]
    },
    "groupByValues": ["ColorId", "SizeId"],
    "returnNegative": true,
    "QueryATP":true
}
```

### <a name="get-method-example"></a>GET metodo pavyzdys

```txt
Path:
    /api/environment/{environmentId}/onhand
Method:
    Get
Headers:
    Api-Version="1.0"
    Authorization="Bearer $access_token"
ContentType:
    application/json
Query(Url Parameters):
    groupBy
    returnNegative
    [Filters]
```

Toliau pateikiamas pavyzdys, kaip sukurti užklausos URL kaip užklausą`GET`.

```txt
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand?organizationId=usmf&productId=Bike&SiteId=1&LocationId=11&groupBy=ColorId,SizeId&returnNegative=true&QueryATP=true
```

Šios užklausos rezultatas `GET` yra lygiai toks pat kaip ir ankstesnio `POST` pavyzdžio užklausos rezultatas.

### <a name="query-result-example"></a>Užklausos rezultatų pavyzdys

Abu ankstesni užklausų pavyzdžiai gali pateikti tokį atsakymą. Pavyzdžiui, sistema konfigūruota naudojant šiuos parametrus:

- **ATP apskaičiuotas matas:** *iv.onhand = eka atvežimo – eka.siuntimo*
- **Grafiko laikotarpis:** *7*

Čia yra atsakymo tekstas.

```json
[
    {
        "quantitiesByDate": {
            "2022-02-02T00:00:00": {
                "pos": {
                    "outbound": 5,
                    "inbound": 0,
                },
                "iv": {
                    "onhand": -5,
                },
            },
            "2022-02-06T00:00:00": {
                "pos": {
                    "inbound": 7,
                    "outbound": 0,
                },
                "iv": {
                    "onhand": 7,
                },
            }
        },
        "atpQuantities": {
            "2022-02-01T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-02T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-03T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-04T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-05T00:00:00Z": {
                "iv": {
                    "onhand": 5.0
                }
            },
            "2022-02-06T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            },
            "2022-02-07T00:00:00Z": {
                "iv": {
                    "onhand": 12.0
                }
            }
        },
        "productId": "Bike ",
        "dimensions": {
            "ColorId": "Red",
            "SizeId": "Big",
            "siteid": "1",
            "locationid": "11"
        },
        "quantities": {
            "pos": {
                "inbound": 10.0,
                "outbound": 0,
            },
            "iv": {
                "onhand": 10.0,
            }
        }
    }
]
```
