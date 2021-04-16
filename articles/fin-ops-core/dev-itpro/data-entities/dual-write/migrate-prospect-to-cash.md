---
title: Perkelti Potencialus klientas į grynuosius pinigus duomenis iš duomenų integratoriaus į dvigubą rašymą
description: Šioje temoje aprašoma, kaip perkelti Potencialus klientas į grynuosius pinigus duomenis iš duomenų integratoriaus į dvigubą rašymą.
author: RamaKrishnamoorthy
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: f6758fe366c2ea59dc75be2f1070650eb5c2f9fc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750865"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Perkelti Potencialus klientas į grynuosius pinigus duomenis iš duomenų integratoriaus į dvigubą rašymą

[!include [banner](../../includes/banner.md)]

Norėdami perkelti Potencialus klientas į grynuosius pinigus duomenis iš duomenų integratoriaus į dvigubą rašymą, atlikite šiuos veiksmus.

1. Paleiskite Potencialus klientas į grynuosius pinigus duomenis integratoriaus užduotis vienam pilnam sinchronizavimui atlikti. Tokiu būdu užtikrinate, kad abi sistemos („Finance and Operations” ir „Customer Engagement” programos) turi visus duomenis.
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
5. Sukurkite dvigubo rašymo ryšį tarp „Finance and Operations” ir tarp „Customer Engagement” programų vienam ar daugiau juridinių subjektų.
6. Įgalinkite dvigubo rašymo lentelės schemas ir paleiskite pradinį reikalingų nuorodos duomenų sinchronizavimą. (Daugiau informacijos žiūrėkite [Pradinio sinchronizavimo svarstymai](initial-sync-guidance.md).) Reikalingų duomenų pavyzdžiai apima klientų grupės, mokėjimo sąlygas ir grafikus. Neįgalinkite dvigubo rašymo schemų lentelėms, kurioms reikia inicijavimo, pavyzdžiui, paskyros, pasiūlymo, pasiūlymo eilutės, užsakymo ir užsakymo eilučių lentelėms.
7. „Customer Engagement” programoje eikite į **Išplėstiniai parametrai \> Sistemos parametrai \> Duomenų valdymas \> Dublikatų aptikimo taisykles** ir išjunkite visas taisykles.
8. Inicijuokite 2 veiksme išvardytas lenteles. Instrukcijas rasite likusiuose šios temos skyriuose.
9. Atidarykite „Finance and Operations” programą ir įgalinkite lentelių schemas, pavyzdžiui, paskyros, pasiūlymo, pasiūlymo eilutės, užsakymo ir užsakymo eilutės lentelių schemas. Tada vykdykite pirminį sinchronizavimą. (Daugiau informacijos žiūrėkite [Pradinio sinchronizavimo svarstymai](initial-sync-guidance.md).) Šio proceso metu bus sinchronizuojama papildoma informacija iš „Finance and Operations” programos, pavyzdžiui, apdorojimo būsena, siuntimo ir sąskaitų siuntimo adresai, svetainės ir sandėliai.

## <a name="account-table"></a>Paskyros lentelė

1. Stulpelyje **Įmonė** įveskite įmonės pavadinimą, pavyzdžiui, **„USMF”**.
2. Stulpelyje **Ryšio tipas** įveskite **Klientas** kaip statinę reikšmę. Galbūt savo verslo logikoje nenorėsite klasifikuoti kiekvieno paskyros įrašo kaip kliento.
3. Stulpelyje **Klientų grupės ID** įveskite klientų grupės numerį iš „Finance and Operations” programos. Numatytoji reikšmė iš Potencialus klientas į grynuosius pinigus sprendimo **yra 10**.
4. Jei naudojate Potencialus klientas į grynuosius pinigus sprendimą be jokio tinkinimo **Paskyros numeriui**, įveskite reikšmę **Paskyros numeris** į **Šalies numeris** stulpelį. Jei yra tinkinimų ir nežinote šalies numerio, šią informaciją sužinokite iš „Finance and Operations” programos.

## <a name="contact-table"></a>Kontakto lentelė

1. Stulpelyje **Įmonė** įveskite įmonės pavadinimą, pavyzdžiui, **„USMF”**.
2. Remiantis **Ar klientas aktyvus** reikšme CSV faile nustatykite šiuos stulpelius:

    - Jei **Ar klientas aktyvus** nustatyta į **Taip** CSV faile, nustatykite stulpelį **Parduotinas** į **Taip**. Stulpelyje **Klientų grupės ID** įveskite klientų grupės numerį iš „Finance and Operations” programos. Numatytoji reikšmė iš Potencialus klientas į grynuosius pinigus sprendimo **yra 10**.
    - Jei **Ar klientas aktyvus** nustatyta į **Ne** CSV faile, nustatykite stulpelį **Parduotinas** į **Ne**, o stulpelį **Kontaktas, skirtas** į **Klientui**.

3. Jei naudojate Potencialus klientas į grynuosius pinigus sprendimą be jokio tinkinimo **Kontakto numeriui**, nustatykite šiuos stulpelius:

    - Perkelkite kontakto numerį iš CSV failo (**„msdynce”\_„contactnumber”**) į kontakto numerį **Kontaktas** lentelėje (**„msdyn”\_„contactnumber”**).
    - Naudokite reikšmes iš **Kontakto numerio** lentelės, esančios **Šalies numerio** stulpelyje.
    - Naudokite reikšmes iš **Kontakto numerio** lentelės, esančios **Paskyros numerio/Kontaktinio asmens ID** stulpelyje.

## <a name="invoice-table"></a>Sąskaitos faktūros lentelė

Kadangi lentelės **Sąskaita faktūra** duomenis yra skirti vienpusiam srautui, iš „Finance and Operations” į „Customer Engagement” programą, inicijavimas nėra būtinas. Vykdykite pradinį sinchronizavimą perkelti visiems reikalingiems duomenis iš „Finance and Operations” į „Customer Engagement” programą. Daugiau informacijos rasite [Pradinio sinchronizavimo svarstymai](initial-sync-guidance.md).

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

Kadangi lentelės **Produktai** duomenis yra skirti vienpusiam srautui, iš „Finance and Operations” į „Customer Engagement” programą, inicijavimas nėra būtinas. Vykdykite pradinį sinchronizavimą perkelti visiems reikalingiems duomenis iš „Finance and Operations” į „Customer Engagement” programą. Daugiau informacijos rasite [Pradinio sinchronizavimo svarstymai](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Pasiūlymo ir pasiūlymo produktų lentelės

Lentelei **Pasiūlymas** vadovaukitės instrukcijomis, pateiktomis ankstesniame šios temos skyriuje [Užsakymo lentelė](#order-table). Lentelei **Pasiūlymo produktas** vadovaukitės instrukcijomis, pateiktomis [Užsakymo produktų lentelė](#order-products-table) skyriuje.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]