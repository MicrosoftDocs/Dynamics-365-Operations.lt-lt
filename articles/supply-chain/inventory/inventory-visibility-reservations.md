---
title: Atsargų matomumo rezervavimai
description: Šioje temoje aprašoma, kaip nustatyti rezervavimo priemonę, kad būtų galima kurti rezervavimus, naudoti rezervavimus ir (arba) nerealizuoti nurodytų atsargų kiekių naudojant atsargų matomumą.
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
ms.openlocfilehash: 4a85520c0911bb7eed5842b3fd5bd706009351e5
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500360"
---
# <a name="inventory-visibility-reservations"></a>Atsargų matomumo rezervavimai

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Šioje temoje aprašoma, kaip nustatyti rezervavimo priemonę, kad būtų galima kurti rezervavimus, naudoti rezervavimus ir (arba) nerealizuoti nurodytų atsargų kiekių naudojant atsargų matomumą.

Rezervavimai pažymi atsargų kiekį, kuris bus naudojamas ateityje. Kai sukuriate rezervavimą, sistema neleidžia kitiems užsakymams rezervuoti ar naudoti rezervuotų prekių, kol rezervavimas suvartojamas arba nerealizuojamas. Rezervavimai kuriami, naudojami ir atšaukiami naudojant API iškvietimus į atsargų matomumo tarnybą.

Galite pasirinktinai nustatyti „Microsoft Dynamics 365 Supply Chain Management“ (ir kitas trečiųjų šalių sistemas) siekiant automatiškai padengti kiekį, rezervuotą naudojant atsargų matomumą. Korespondentinis kiekis panaikinamas iš rezervavimo įrašų atsargų matomumo lauke.

Kai įjungsite rezervavimo funkciją, „Supply Chain Management“ automatiškai taps parengtu korespondentiniu rezervavimu, kuris atliktas naudojant atsargų matomumą.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Įjungti ir nustatyti rezervavimo funkciją

Norėdami įjungti šią rezervacijos funkciją, atlikite toliau nurodytus veiksmus.

1. „Power Apps“ prisiregistruoti ir atidaryti **atsargų matomumą**.
1. Atidarykite **Konfigūravimo** puslapį.
1. **Funkcijų valdymo** skirtuke įjunkite funkciją *OnHandReservation*.
1. Prisijunkite prie „Supply Chain Management“.
1. Eikite į **[funkcijų valdymą](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** darbo sritį ir įjunkite *atsargų matomumo integravimą su rezervavimo kompensavimą* funkciją (reikalinga 10.0.22 ar vėlesnė versija).
1. Eikite į **Atsargų valdymo \> nustatymo \> atsargų matomumo integravimo parametrus**, atidarykite **Rezervavimo kompensavimas** skirtuką ir atlikite šiuos parametrus:
    - **Įgalinti rezervavimo korespondentinę sąskaitą** – nustatykite kaip *Taip*, norėdami įgalinti šią funkciją.
    - **Rezervavimo korespondentinis modifikatorius** – pasirinkite atsargų operacijos būseną, kuri koresponduos rezervavimus, atliktas atsargų matomumo metu. Šis parametras nustato užsakymo apdorojimo etapą, kuris suaktyvina kompensavimus. Etapą seka užsakymo atsargų operacijos būsena. Pasirinkite vieną iš šių parinkčių:
        - *Užsakyta* – kai operacijos būsena Yra, sukūrus užsakymą, *užsakymas* atsiųs korespondentinę užklausą. Korespondentinis kiekis bus sukurto užsakymo kiekis.
        - *Rezervas* – kai *operacijos būsena Rezervuota,* Užsakytas užsakymas siųs korespondentinę užklausą, kai ji rezervuota, paimta, užregistruotas važtaraštis arba išrašyta SF. Užklausa bus suaktyvinta tik vieną kartą, pirmojo žingsnio atveju, kai bus įvyksta nurodytas procesas. Korespondentinis kiekis bus kiekis, kai atsargų operacijos būsena atitinkamoje užsakymo eilutėje pasikeičia iš *Užsakyta* į *Rezervuota* (arba vėlesnė būsena).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Naudoti rezervacijos funkciją atsargų matomume

Kai iškiesite rezervavimo API, sistema pažymi nurodytų prekių ir kiekių rezervavimą. Turite apibrėžti rezervavimo hierarchiją ir užregistruoti užklausas, kurios atitinka tą rezervavimo hierarchiją. Tada rezervavimai gali būti atliekami tiesiogiai iškvievieuojant rezervavimo API.

### <a name="configure-the-reservation-hierarchy"></a>Konfigūruoti rezervavimo hierarchiją

Rezervavimo hierarchija aprašo dimensijų seką, kurią reikia nurodyti rezervuojant. Tai veikia tuo pačiu būdu, kaip indeksų hierarchija veikia turimose užklausose.

Rezervavimo hierarchija gali skirtis nuo indeksų hierarchijos. Šis nepriklausomumas leidžia įgyvendinti kategorijų valdymą, kur vartotojai gali suskaidyti dimensijas į išsamią informaciją, kad nustatytų tikslesnių rezervavimų reikalavimus.

Norėdami konfigūruoti soft rezervavimo hierarchiją „Power Apps“, atidarykite **konfigūracijos** puslapį ir tada **Švelniai rezervavimo hiearchija** nustatykite rezervavimo hierarchiją pridėdami ir (arba) modifikuodami dimensijas ir jų hierarchijos lygius.

Jūsų soft rezervavimo hierarchijoje turi `SiteId` būti komponentai ir kaip `LocationId` komponentai, nes jie sudaro skaidinio konfigūraciją.

Daugiau informacijos apie tai, kaip konfigūruoti rezervavimus, žr. [Rezervavimo konfigūravimas](inventory-visibility-configuration.md#reservation-configuration).

### <a name="call-the-reservation-api"></a>Iškviesti rezervavimo API

Rezervavimai atliekami atsargų matomumo paslaugoje, pateikiant post užklausą paslaugos URL, pvz., `/api/environment/{environment-ID}/onhand/reserve`.

Rezervuojant užklausos dokumentuose turi būti organizacijos ID, produkto ID, rezervuoti kiekiai ir dimensijos. Užklausa sugeneruoja unikalų rezervavimo ID kiekvienam rezervavimo įrašui. Rezervavimo įraše yra unikalus produkto ID ir dimensijų derinys.

Kai iškiesite rezervavimo API, galite valdyti rezervavimo tikrinimą nurodydami parametrą Boolean `ifCheckAvailForReserv` užklausos body. Vertė, `True` kuri reiškia, kad būtinas tikrinimas, o `False` vertė reiškia, kad tikrinimas nebūtinas. Numatytoji vertė yra `True`.

Jei norite atšaukti rezervavimą ar nereservuoti nurodytų atsargų kiekių, nustatykite neigiamą kiekio vertę ir nustatykite parametrą praleisti `ifCheckAvailForReserv` ir `False` tikrinimą.

Čia pateikiamas nuorodos užklausos tekstas.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "Red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "SoftReservOrdered",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

## <a name="offset-reservations-in-supply-chain-management"></a>Kompensavimo rezervacijos „Supply Chain Management“

Atsargų operacijų būsenose, kurios apima nurodytą rezervo korespondentinį modifikatorių, operacijos atnaujinimas su koresponduos atitinkamą rezervavimo įrašą, kai bus įvykdytos visos šios sąlygos:

- Atsargų operacijos rezervavimo ID sutampa su rezervavimo įrašo rezervavimo ID atsargų matomumo paslaugoje.
- Atsargų operacijos dimensijos sutampa su dimensijomis įrašo rezervavimo atsargų matomumo paslaugoje.
- Atsargų operacijos būsenos pakeitimai suaktyvina rezervavimų kompensavimus, kai atsargų operacijos būsena atspindi faktą, kad užsakymo procesas buvo baigtas arba praleistas.

Korespondentinis kiekis yra toks pat kaip atsargų kiekis, nurodytas atsargų operacijose. Korespondentinė sąskaita neveikia, jei atsargų matomumo paslaugoje nelieka jokio rezervuotų kiekio.

### <a name="set-up-the-reservation-offset-modifier"></a>Nustatyti rezervo korespondentinės modifikatorių

Jei to dar nepadarėte, nustatykite rezervavimo modifikatorių, kaip aprašyta [Įjungti ir nustatykite rezervavimo funkciją](#turn-on).

### <a name="set-up-reservation-ids"></a>Rezervavimo ID nustatymas

Rezervavimo ID unikaliai pažymi rezervavimo įrašą atsargų matomumo lauke. „Supply Chain Management“ srityje vartotojai rezervuos užsakymo eilutes, kad žymėti atitinkamo rezervavimo įrašo korespondentinę sąskaitą.

Norėdami „Supply Chain Management“ dalyje nustatyti rezervavimo ID, atlikite šiuos veiksmus.

1. Atidaryti pardavimo užsakymą (pvz., **Visi pardavimo užsakymai** puslapyje).
1. „FastTab“ **Pardavimo užsakymo eilutės** pasirinkite užsakymo eilutę.
1. „FastTab" **Pardavimo užsakymo eilučių**, įrankių juostoje, pasirinkite **Atnaujinti eilutę \> Atsargos \> Atsargų matomumo integravimas**.
1. Įveskite atitinkamus rezervavimo ID.

Atsargų būsenos pakeitimas sutampa su korespondentinio modifikatoriaus nustatymu.
