---
title: Perkelti Potencialus klientas į grynuosius pinigus duomenis iš duomenų integratoriaus į dvigubą rašymą
description: Šioje temoje aprašoma, kaip perkelti Potencialus klientas į grynuosius pinigus duomenis iš duomenų integratoriaus į dvigubą rašymą.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: 82bfb768b0ecac04184f4b806527346d39584d64
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087273"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Perkelti Potencialus klientas į grynuosius pinigus duomenis iš duomenų integratoriaus į dvigubą rašymą

[!include [banner](../../includes/banner.md)]

„Prospect to cash“ sprendimas, skirtas „Data Integrator“, nesuderinamas su dvigubu rašymu. To priežastis yra sąskaitos lentelės indeksas msdynce_AccountNumber, kuris buvo pateiktas kaip „Prospect to cash“ sprendimo dalis. Jei šis indeksas yra, negalite sukurti to paties kliento sąskaitos numerio dviejuose skirtinguose juridiniuose subjektuose. Galite pasirinkti iš naujo pradėti nuo dvigubo rašymo, perkeldami potencialųjį klientą į grynųjų pinigų duomenis iš duomenų integratoriaus į dvigubą rašymą, arba galite įdiegti paskutinę „neaktyvią“ „Prospect“ į grynųjų pinigų sprendimo versiją. Ši tema apima abu šiuos metodus.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Įdiekite paskutinę „neaktyvią“ „Data Integrator Prospect“ į grynųjų pinigų sprendimą versiją

**P2C versija 15.0.0.2** yra laikoma paskutine „neaktyvia“ duomenų integratoriaus „Prospect to cash“ sprendimo versija. Jį galite atsisiųsti iš [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Turite jį įdiegti rankiniu būdu. Po įdiegimo viskas išlieka lygiai taip pat, išskyrus msdynce_AccountNumber indeksą, kuris pašalinamas.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Veiksmai, kaip perkelti „Prospect“ į grynųjų pinigų duomenis iš „Data Integrator“ į dvigubą rašymą

Norėdami perkelti Potencialus klientas į grynuosius pinigus duomenis iš duomenų integratoriaus į dvigubą rašymą, atlikite šiuos veiksmus.

1. Paleiskite Potencialus klientas į grynuosius pinigus duomenis integratoriaus užduotis vienam pilnam sinchronizavimui atlikti. Tokiu būdu užtikrinate, kad abi sistemos (programėlės „Finance and Operations“ ir „klientų įtraukimo programos“) turėtų visus duomenis.
2. Norėdami išvengti galimo duomenų praradimo, eksportuokite Potencialus klientas į grynuosius pinigus duomenis iš „Microsoft Dynamics 365 Sales” į „Excel” failą arba kableliais atskirtų verčių (CSV) failą. Eksportuokite duomenis iš šių objektų:

    - [Paskyra](#account-table)
    - [Kontaktas](#contact-table)
    - [PVM sąskaita faktūra](#invoice-table)
    - Išrašyti produktų sąskaitą faktūrą
    - [Užsakymas](#order-table)
    - [Užsakymo produktai](#order-products-table)
    - [Produktai](#products-table)
    - [Pasiūlymas](#quote-and-quote-product-tables)
    - [Pasiūlymo produktai](#quote-and-quote-product-tables)

3. Pašalinkite Potencialus klientas į grynuosius pinigus sprendimą iš „Sales” aplinkos. Šiuo veiksmu pašalinami stulpeliai ir atitinkami duomenys, kuriuos pateikė sprendimas Potencialus klientas į grynuosius pinigus.
4. Įdiekite dvigubo rašymo sprendimą.
5. Sukurkite dvigubo rašymo ryšį tarp programos „Finance and Operations“ ir klientų įtraukimo programos vienam ar keliems juridiniams asmenims.
6. Įgalinkite dvigubo rašymo lentelės schemas ir paleiskite pradinį reikalingų nuorodos duomenų sinchronizavimą. (Daugiau informacijos žiūrėkite [Pradinio sinchronizavimo svarstymai](initial-sync-guidance.md).) Reikalingų duomenų pavyzdžiai apima klientų grupės, mokėjimo sąlygas ir grafikus. Neįgalinkite dvigubo rašymo schemų lentelėms, kurioms reikia inicijavimo, pavyzdžiui, paskyros, pasiūlymo, pasiūlymo eilutės, užsakymo ir užsakymo eilučių lentelėms.
7. „Customer Engagement” programoje eikite į **Išplėstiniai parametrai \> Sistemos parametrai \> Duomenų valdymas \> Dublikatų aptikimo taisykles** ir išjunkite visas taisykles.
8. Inicijuokite 2 veiksme išvardytas lenteles. Instrukcijas rasite likusiuose šios temos skyriuose.
9. Atidarykite programą „Finance and Operations“ ir įgalinkite lentelės žemėlapius, pvz., sąskaitos, kainos pasiūlymo, pasiūlymo eilutės, užsakymo ir užsakymo eilutės lentelės žemėlapius. Tada vykdykite pirminį sinchronizavimą. (Daugiau informacijos žr [Pradinio sinchronizavimo svarstymai](initial-sync-guidance.md) .) Šis procesas sinchronizuos papildomą informaciją iš programos „Finance and Operations“, pvz., apdorojimo būseną, pristatymo ir atsiskaitymo adresus, svetaines ir sandėlius.

## <a name="account-table"></a>Paskyros lentelė

1. Stulpelyje **Įmonė** įveskite įmonės pavadinimą, pavyzdžiui, **„USMF”**.
2. Stulpelyje **Ryšio tipas** įveskite **Klientas** kaip statinę reikšmę. Galbūt savo verslo logikoje nenorėsite klasifikuoti kiekvieno paskyros įrašo kaip kliento.
3. Viduje konors **Klientų grupės ID** stulpelyje įveskite klientų grupės numerį iš programėlės „Finance and Operations“. Numatytoji reikšmė iš Potencialus klientas į grynuosius pinigus sprendimo **yra 10**.
4. Jei naudojate Potencialus klientas į grynuosius pinigus sprendimą be jokio tinkinimo **Paskyros numeriui**, įveskite reikšmę **Paskyros numeris** į **Šalies numeris** stulpelį. Jei yra tinkinimų ir nežinote šalies numerio, paimkite šią informaciją iš programos „Finance and Operations“.

## <a name="contact-table"></a>Kontakto lentelė

1. Stulpelyje **Įmonė** įveskite įmonės pavadinimą, pavyzdžiui, **„USMF”**.
2. Remiantis **Ar klientas aktyvus** reikšme CSV faile nustatykite šiuos stulpelius:

    - Jei **Ar klientas aktyvus** nustatyta į **Taip** CSV faile, nustatykite stulpelį **Parduotinas** į **Taip**. Viduje konors **Klientų grupės ID** stulpelyje įveskite klientų grupės numerį iš programėlės „Finance and Operations“. Numatytoji reikšmė iš Potencialus klientas į grynuosius pinigus sprendimo **yra 10**.
    - Jei **Ar klientas aktyvus** nustatyta į **Ne** CSV faile, nustatykite stulpelį **Parduotinas** į **Ne**, o stulpelį **Kontaktas, skirtas** į **Klientui**.

3. Jei naudojate Potencialus klientas į grynuosius pinigus sprendimą be jokio tinkinimo **Kontakto numeriui**, nustatykite šiuos stulpelius:

    - Perkelkite kontakto numerį iš CSV failo (**„msdynce”\_„contactnumber”**) į kontakto numerį **Kontaktas** lentelėje (**„msdyn”\_„contactnumber”**).
    - Naudokite reikšmes iš **Kontakto numerio** lentelės, esančios **Šalies numerio** stulpelyje.
    - Naudokite reikšmes iš **Kontakto numerio** lentelės, esančios **Paskyros numerio/Kontaktinio asmens ID** stulpelyje.

## <a name="invoice-table"></a>Sąskaitos faktūros lentelė

Kadangi duomenys iš **Sąskaita faktūra** lentelė sukurta taip, kad būtų vykdoma į vieną pusę – nuo programos „Finance and Operations“ iki kliento įtraukimo programos, inicijuoti nereikia. Vykdykite pradinį sinchronizavimą, kad perkeltumėte visus reikiamus duomenis iš programos „Finance and Operations“ į klientų įtraukimo programą. Daugiau informacijos rasite [Pradinio sinchronizavimo svarstymai](initial-sync-guidance.md).

## <a name="order-table"></a>Užsakymų lentelė

1. Stulpelyje **Įmonė** įveskite įmonės pavadinimą, pavyzdžiui, **„USMF”**.
2. Nukopijuokite **Užsakymo ID** stulpelio reikšmę CSV faile į **Pardavimo užsakymo numerio** stulpelį.
3. Nukopijuokite **Kliento** stulpelio reikšmę CSV faile į **Sąskaitos faktūros kliento numerio** stulpelį.
4. Nukopijuokite stulpelio **Gabenti į šalį/regioną** reikšmę CSV faile į **Gabenti į šalį/regioną** stulpelį. Šios reikšmės pavyzdžiai yra **JAV** ir **Jungtinės Valstijos**.
5. Nustatykite **Pageidaujama gavimo data** stulpelį. Jei nenaudojate gavimo datos, naudokite stulpelius **Pageidaujama pristatymo data**, **Vykdymo data** ir **Pateikimo data** CSV faile. Šios reikšmės pavyzdys yra **„2020-03-27T00:00:00Z”**.
6. Nustatykite **Kalba** stulpelį. Šios reikšmės pavyzdys yra **„en-us”**.
7. Nustatykite stulpelį **Užsakymo tipas** naudodami **Pagal prekę** stulpelį.

## <a name="order-products-table"></a>Užsakymo produktų lentelė

- Stulpelyje **Įmonė** įveskite įmonės pavadinimą, pavyzdžiui, **„USMF”**.

## <a name="products-table"></a>Produktų lentelė

Kadangi duomenys iš **Produktai** lentelė sukurta taip, kad būtų vykdoma į vieną pusę – nuo programos „Finance and Operations“ iki kliento įtraukimo programos, inicijuoti nereikia. Vykdykite pradinį sinchronizavimą, kad perkeltumėte visus reikiamus duomenis iš programos „Finance and Operations“ į klientų įtraukimo programą. Daugiau informacijos rasite [Pradinio sinchronizavimo svarstymai](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Pasiūlymo ir pasiūlymo produktų lentelės

Lentelei **Pasiūlymas** vadovaukitės instrukcijomis, pateiktomis ankstesniame šios temos skyriuje [Užsakymo lentelė](#order-table). Lentelei **Pasiūlymo produktas** vadovaukitės instrukcijomis, pateiktomis [Užsakymo produktų lentelė](#order-products-table) skyriuje.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
