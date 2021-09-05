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
ms.openlocfilehash: 6c87018cbfbe22fbbc441a1a23aee0ac44af9ddc
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345154"
---
# <a name="inventory-visibility-reservations"></a>Atsargų matomumo rezervavimai

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Šioje temoje aprašoma, kaip nustatyti rezervavimo priemonę, kad būtų galima kurti rezervavimus, naudoti rezervavimus ir (arba) nerealizuoti nurodytų atsargų kiekių naudojant atsargų matomumą.

Rezervavimai pažymi atsargų kiekį, kuris bus naudojamas ateityje. Kai sukuriate rezervavimą, sistema neleidžia kitiems užsakymams rezervuoti ar naudoti rezervuotų prekių, kol rezervavimas suvartojamas arba nerealizuojamas. Rezervavimai kuriami, naudojami ir atšaukiami naudojant API iškvietimus į atsargų matomumo tarnybą.

Galite pasirinktinai nustatyti „Microsoft Dynamics 365 Supply Chain Management“ (ir kitas trečiųjų šalių sistemas) siekiant automatiškai padengti kiekį, rezervuotą naudojant atsargų matomumą. Korespondentinis kiekis panaikinamas iš rezervavimo įrašų atsargų matomumo lauke.

Kai įjungsite rezervavimo funkciją, „Supply Chain Management“ automatiškai taps parengtu korespondentiniu rezervavimu, kuris atliktas naudojant atsargų matomumą.

> [!NOTE]
> Korespondentinei funkcijai reikia „Supply Chain Management“ versijos 10.0.22 ar vėlesnės versijos. Jei norite naudoti atsargų matomumo rezervavimus, rekomenduojame palaukti, kol „Supply Chain Management“ atnaujinsite į 10.0.22 arba vėlesnę versiją.

## <a name="turn-on-the-reservation-feature"></a>Įjungti rezervavimo funkciją

Norėdami įjungti šią rezervacijos funkciją, atlikite toliau nurodytus veiksmus.

1. „Power Apps“, atverkite **Atsargų matomumo**.
1. Atidarykite **Konfigūravimo** puslapį.
1. **Funkcijų valdymo** skirtuke įjunkite funkciją *OnHandReservation*.
1. Prisijunkite prie „Supply Chain Management“.
1. Eikite į **Atsargų valdymas \> Sąranka \> Atsargų ir sandėlio matomumo integravimo parametrai**.
1. Dalyje **Rezervavimo korespondentinė** sąskaita nustatykite **pasirinktį Įgalinti rezervavimo** korespondentinę sąskaitą kaip *Taip*.

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Naudoti rezervacijos funkciją atsargų matomume

Kai iškiesite rezervavimo API, sistema pažymi nurodytų prekių ir kiekių rezervavimą. Turite apibrėžti rezervavimo hierarchiją ir užregistruoti užklausas, kurios atitinka tą rezervavimo hierarchiją. Tada rezervavimai gali būti atliekami tiesiogiai iškvievieuojant rezervavimo API.

### <a name="configure-the-reservation-hierarchy"></a>Konfigūruoti rezervavimo hierarchiją

Rezervavimo hierarchija aprašo dimensijų seką, kurią reikia nurodyti rezervuojant. Tai veikia tuo pačiu būdu, kaip indeksų hierarchija veikia turimose užklausose.

Rezervavimo hierarchija gali skirtis nuo indeksų hierarchijos. Šis nepriklausomumas leidžia įgyvendinti kategorijų valdymą, kur vartotojai gali suskaidyti dimensijas į išsamią informaciją, kad nustatytų tikslesnių rezervavimų reikalavimus.

Norėdami konfigūruoti soft rezervavimo hierarchiją „Power Apps“, atidarykite **konfigūracijos** puslapį ir tada **Švelniai rezervavimo konvertavimas** nustatykite rezervavimo hierarchiją pridėdami ir (arba) modifikuodami dimensijas ir jų hierarchijos lygius.

### <a name="call-the-reservation-api"></a>Iškviesti rezervavimo API

Rezervavimai atliekami atsargų matomumo paslaugoje, pateikiant post užklausą paslaugos URL, pvz., `/api/environment/{environment-ID}/onhand/reserve`.

Rezervuojant užklausos dokumentuose turi būti organizacijos ID, produkto ID, rezervuoti kiekiai ir dimensijos. Užklausa sugeneruoja unikalų rezervavimo ID kiekvienam rezervavimo įrašui. Rezervavimo įraše yra unikalus produkto ID ir dimensijų derinys.

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

> [!NOTE]
> Galima naudoti 10.0.22 versijos korespondentinę funkciją

### <a name="set-up-the-reserve-offset-modifier"></a>Nustatyti rezervo korespondentinės sąskaitos modifikatorių

Rezervo korespondentinis modifikatorius nustato užsakymo apdorojimo etapą, kuris suaktyvina korespondavimo atvejus. Etapą seka užsakymo atsargų operacijos būsena. Norėdami rezervuoti kompensavimo keitimą, atlikite šiuos žingsnius.

1. Eikite į **Atsargų valdymas \> Sąranka \> Atsargų ir sandėlio matomumo integravimo parametrai \> Rezervavimo kompensavimas**.
1. Nustatyti **Rezervavimo kompensavimo keitiklį** laukelis turi būti nustatytas viena iš tolesnių verčių:

    - *Užsakyta* – kai operacijos būsena Yra, sukūrus užsakymą, *užsakymas* atsiųs korespondentinę užklausą.
    - *Rezervas* – kai *operacijos būsena Rezervuota,* Užsakytas užsakymas siųs korespondentinę užklausą, kai ji rezervuota, paimta, užregistruotas važtaraštis arba išrašyta SF. Užklausa bus suaktyvinta tik vieną kartą, pirmojo žingsnio atveju, kai bus įvyksta nurodytas procesas.

### <a name="set-up-reservation-ids"></a>Rezervavimo ID nustatymas

Rezervavimo ID unikaliai pažymi rezervavimo įrašą atsargų matomumo lauke. „Supply Chain Management“ srityje vartotojai rezervuos užsakymo eilutes, kad žymėti atitinkamo rezervavimo įrašo korespondentinę sąskaitą.

Norėdami „Supply Chain Management“ dalyje nustatyti rezervavimo ID, atlikite šiuos veiksmus.

1. Atidaryti pardavimo užsakymą (pvz., **Visi pardavimo užsakymai** puslapyje).
1. „FastTab“ **Pardavimo užsakymo eilutės** pasirinkite užsakymo eilutę.
1. „FastTab" **Pardavimo užsakymo eilučių**, įrankių juostoje, pasirinkite **Atnaujinti eilutę \> Atsargos \> Atsargų matomumo integravimas**.
1. Įveskite atitinkamus rezervavimo ID.

Atsargų būsenos pakeitimas sutampa su korespondentinio modifikatoriaus nustatymu.
