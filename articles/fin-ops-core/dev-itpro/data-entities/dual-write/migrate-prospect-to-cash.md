---
title: Perkelti Potencialus klientas į grynuosius pinigus duomenis iš duomenų integratoriaus į dvigubą rašymą
description: Šiame straipsnyje aprašoma, kaip perkelti potencialų klientą į grynųjų pinigų duomenis iš duomenų integratoriaus į dvigubo rašymo.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: 91cc0e59405bc085e09f01f05ef02e4a0260481e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111901"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Perkelti Potencialus klientas į grynuosius pinigus duomenis iš duomenų integratoriaus į dvigubą rašymą

[!include [banner](../../includes/banner.md)]

Galimas duomenų integratoriaus potencialus kliento grynųjų pinigų sprendimas nesuderinamas su dvigubo rašymo programa. To priežastis yra tas msdynce_AccountNumber lentelės, kurią gavote kaip potencialaus kliento į grynųjų pinigų sprendimą dalis, indeksas. Jei yra šis indeksas, to paties kliento sąskaitos numerio negalima sukurti dviejuose skirtinguose juridiniuose subjektuose. Galite pasirinkti pradėti naują su dvigubo rašymo būdu, pereidami potencialų klientą į grynųjų pinigų duomenis iš duomenų integratoriaus į dvigubo rašymo įrašą, arba galite įdiegti paskutinę potencialaus kliento "dorman" versiją į grynųjų pinigų sprendimą. Šiame straipsnyje aprašomas abu šie būdai.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Įdiegti paskutinę Duomenų integratoriaus potencialaus kliento versiją į grynųjų pinigų sprendimą

**P2C 15.0.0.2** yra laikoma paskutine duomenų integratoriaus potencialaus kliento į grynųjų pinigų sprendimą "dorman" versija. Galite atsisiųsti jį iš [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Turite jį įdiegti rankiniu būdu. Įdiegus viskas lieka lygiai taip pat, išskyrus msdynce_AccountNumber indeksas pašalinamas.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Veiksmai, norint perkelti potencialų klientą į grynųjų pinigų duomenis iš duomenų integratoriaus į dvigubo rašymo

Norėdami perkelti Potencialus klientas į grynuosius pinigus duomenis iš duomenų integratoriaus į dvigubą rašymą, atlikite šiuos veiksmus.

1. Paleiskite Potencialus klientas į grynuosius pinigus duomenis integratoriaus užduotis vienam pilnam sinchronizavimui atlikti. Tokiu būdu užtikrinate, kad tiek sistemose (finansų, tiek operacijų programėles ir klientų įsipareigojimo programėles) bus visi duomenys.
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
5. Kurkite dvigubo rašymo ryšį tarp finansų ir operacijų programos ir klientų įsipareigojimo programos vienam ar daugiau juridinių subjektų.
6. Įgalinkite dvigubo rašymo lentelės schemas ir paleiskite pradinį reikalingų nuorodos duomenų sinchronizavimą. (Daugiau informacijos žiūrėkite [Pradinio sinchronizavimo svarstymai](initial-sync-guidance.md).) Reikalingų duomenų pavyzdžiai apima klientų grupės, mokėjimo sąlygas ir grafikus. Neįgalinkite dvigubo rašymo schemų lentelėms, kurioms reikia inicijavimo, pavyzdžiui, paskyros, pasiūlymo, pasiūlymo eilutės, užsakymo ir užsakymo eilučių lentelėms.
7. „Customer Engagement” programoje eikite į **Išplėstiniai parametrai \> Sistemos parametrai \> Duomenų valdymas \> Dublikatų aptikimo taisykles** ir išjunkite visas taisykles.
8. Inicijuokite 2 veiksme išvardytas lenteles. Instrukcijų ieškokite likusiuose šio straipsnio skyriuose.
9. Atidarykite finansų ir operacijų programą ir įgalinkite lentelių schemas, pvz., sąskaitos, pasiūlymo, pasiūlymo eilutės, užsakymo ir užsakymo eilučių lentelių schemos. Tada vykdykite pirminį sinchronizavimą. (Daugiau informacijos žr. [Pradinio sinchronizavimo aplinkybės](initial-sync-guidance.md).) Šio proceso metu bus sinchronizuojama papildoma informacija iš finansų ir operacijų programos, pvz., apdorojimo būsena, siuntimo ir sąskaitų siuntimo adresai, svetainės ir sandėliai.

## <a name="account-table"></a>Paskyros lentelė

1. Stulpelyje **Įmonė** įveskite įmonės pavadinimą, pavyzdžiui, **„USMF”**.
2. Stulpelyje **Ryšio tipas** įveskite **Klientas** kaip statinę reikšmę. Galbūt savo verslo logikoje nenorėsite klasifikuoti kiekvieno paskyros įrašo kaip kliento.
3. Stulpelyje **Klientų grupės ID** įveskite klientų grupės numerį iš finansų ir operacijų programos. Numatytoji reikšmė iš Potencialus klientas į grynuosius pinigus sprendimo **yra 10**.
4. Jei naudojate Potencialus klientas į grynuosius pinigus sprendimą be jokio tinkinimo **Paskyros numeriui**, įveskite reikšmę **Paskyros numeris** į **Šalies numeris** stulpelį. Jei yra pritaikymų ir nežinote šalies numerio, traukite šią informaciją iš finansų ir operacijų programos.

## <a name="contact-table"></a>Kontakto lentelė

1. Stulpelyje **Įmonė** įveskite įmonės pavadinimą, pavyzdžiui, **„USMF”**.
2. Remiantis **Ar klientas aktyvus** reikšme CSV faile nustatykite šiuos stulpelius:

    - Jei **Ar klientas aktyvus** nustatyta į **Taip** CSV faile, nustatykite stulpelį **Parduotinas** į **Taip**. Stulpelyje **Klientų grupės ID** įveskite klientų grupės numerį iš finansų ir operacijų programos. Numatytoji reikšmė iš Potencialus klientas į grynuosius pinigus sprendimo **yra 10**.
    - Jei **Ar klientas aktyvus** nustatyta į **Ne** CSV faile, nustatykite stulpelį **Parduotinas** į **Ne**, o stulpelį **Kontaktas, skirtas** į **Klientui**.

3. Jei naudojate Potencialus klientas į grynuosius pinigus sprendimą be jokio tinkinimo **Kontakto numeriui**, nustatykite šiuos stulpelius:

    - Perkelkite kontakto numerį iš CSV failo (**„msdynce”\_„contactnumber”**) į kontakto numerį **Kontaktas** lentelėje (**„msdyn”\_„contactnumber”**).
    - Naudokite reikšmes iš **Kontakto numerio** lentelės, esančios **Šalies numerio** stulpelyje.
    - Naudokite reikšmes iš **Kontakto numerio** lentelės, esančios **Paskyros numerio/Kontaktinio asmens ID** stulpelyje.

## <a name="invoice-table"></a>Sąskaitos faktūros lentelė

SF lentelės duomenys **sukurti** rodyti vienu būdu, todėl iš finansų ir operacijų programos į kliento įsipareigojimo programą inicijuoti nebūtina. Vykdykite pradinę sinchronizaciją, norėdami perkelti visus reikiamus duomenis iš finansų ir operacijų programos į klientų įsipareigojimo programą. Daugiau informacijos rasite [Pradinio sinchronizavimo svarstymai](initial-sync-guidance.md).

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

Kadangi duomenys iš **produktų lentelės** sukurti taip, kad iš finansų ir operacijų programų į kliento įsipareigojimų programą būtų pateikti vienu būdu, inicijavimas nebūtinas. Vykdykite pradinę sinchronizaciją, norėdami perkelti visus reikiamus duomenis iš finansų ir operacijų programos į klientų įsipareigojimo programą. Daugiau informacijos rasite [Pradinio sinchronizavimo svarstymai](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Pasiūlymo ir pasiūlymo produktų lentelės

Jei norite **naudoti** lentelę Pasiūlymas, vadovaukitės anksčiau šiame straipsnyje [skyriuje](#order-table) Užsakymų lentelė pateiktomis instrukcijomis. Lentelei **Pasiūlymo produktas** vadovaukitės instrukcijomis, pateiktomis [Užsakymo produktų lentelė](#order-products-table) skyriuje.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

