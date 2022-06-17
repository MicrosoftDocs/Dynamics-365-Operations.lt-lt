---
title: „Excel“ darbaknygės kūrimas norint redaguoti mažmeninės prekybos operacijas
description: Šiame straipsnyje aprašoma, kaip sukurti „Excel“ darbaknygę, kad galėtumėte redaguoti mažmeninės prekybos operacijas „Microsoft Dynamics 365 Commerce“.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: da3c2eb19491b37decaf29d13f675271ae7a3698
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873092"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a>„Excel“ darbaknygės kūrimas norint redaguoti mažmeninės prekybos operacijas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip sukurti „Excel“ darbaknygę, kad galėtumėte redaguoti mažmeninės prekybos operacijas „Microsoft Dynamics 365 Commerce“.

## <a name="overview"></a>Apžvalga

Yra iš anksto nustatytas „Excel“ šablonas, kurį klientai gali pasiekti iš skirtingų sistemos dalių ir naudoti mažmeninės prekybos operacijoms redaguoti ir tikrinti. Tačiau klientai taip pat gali sukurti pasirinktinę „Excel“ darbaknygę šiam tikslui.

## <a name="create-and-configure-an-excel-workbook"></a>„Excel“ darbaknygės kūrimas ir konfigūravimas

Norėdami sukurti ir konfigūruoti „Excel“ darbaknygę, kad galėtumėte redaguoti mažmeninės prekybos operacijas, atlikite nurodytus veiksmus.

1. Atidarykite „Excel“ ir sukurkite tuščią darbaknygę.
1. Skirtuke **Įterpti** pasirinkite **Mano papildiniai**.
1. Dešiniojoje srityje pasirinkite saitą **Įtraukti serverio informaciją**.
1. Įveskite serverio URL ir pasirinkite **Gerai**.
1. Jei gaunate klaidos pranešimą „Nerasta jokių programėlės registracijų“, atlikite šiuos veiksmus, kad išspręstumėte problemą:

    1. „Commerce“ eikite į **Sistemos administravimas \> Sąranka \> „Office“ programos parametrai**.
    1. „FastTab“ **Programos parametrai** pasirinkite **Inicijuoti programos parametrus**.
    1. Patvirtinimo pranešimo lauke pasirinkite **Gerai**.
    1. „FastTab“ **Užregistruotos programėlės** pasirinkite **Inicijuoti programėlės registraciją**.
    1. Kaip reikalaujama, pakartokite tris ankstesnius veiksmus.

1. Pasirinkite **Dizainas** ir tada pasirinkite **Įtraukti lentelę**.
1. Remdamiesi modifikuotinais duomenimis, pasirinkite objektus, kuriuos reikia įtraukti į „Excel“ darbaknygę ir redaguoti. Naudokite toliau pateikiamą lentelę kaip nuorodą.

    | Operacijos tipas | Naudotini duomenų objektai |
    |------------------|----------------------|
    | Atsiskaitymo grynaisiais operacijos, internetiniai užsakymai, asinchroniniai kliento užsakymai, asinchroniniai kliento pasiūlymai | Operacija (patikrinama), pardavimo operacija (patikrinama), mokėjimo operacijos (patikrinamos), mokesčių operacijos (patikrinamos), nuolaidų operacijos (patikrinamos), išlaidų operacijos (patikrinamos) |
    | Inkasavimas | Operacija (patikrinama), bankinio mokėjimo priemonių operacijos (patikrinamos) |
    | Pinigų įnešimas į kasą | Operacija (patikrinama), kasos mokėjimo priemonių operacijos (patikrinamos) |
    | Mokėjimo priemonių deklaravimas | Operacija (patikrinama), mokėjimo priemonių deklaravimo operacijos (patikrinamos) |
    | Pajamos, išlaidos | Operacija (patikrinama), pajamų / išlaidų operacijos (patikrinamos), mokėjimo operacijos (patikrinamos) |
    | Deklaruoti pradžios sumą, mokėjimo priemonės šalinimas, srauto įrašas, mokėjimo priemonės grąža, sąskaitos faktūros apmokėjimas, kliento depozitas | Operacija (patikrinama), mokėjimo operacijos (patikrinamos) |

    > [!NOTE]
    > Svarbu, kad į kiekvieną „Excel“ darbaknygę įtrauktumėte tik vieną duomenų objektą. Be to, visi laukai, pažymėti rakto simboliu, turi būti įtraukti į atitinkamą darbaknygę.

1. Sukonfigūravę darbaknygę, pritaikykite reikalingus filtrus. Nepamirškite tų pačių filtrų pritaikyti visuose failo darbalapiuose. Į „Excel“ failą neįkelkite labai didelio duomenų kiekio. Kitu atveju tai gali turėti įtakos našumui ir „Excel“ bei jūsų sistema gali veikti lėčiau. Rekomenduojame visada naudoti filtrus „Įmonė“ ir „Išrašo numeris“ arba „Operacijos numeris“ kaip filtrus, skirtus jūsų failui.
1. Sukonfigūravę filtrus, pasirinkite **Atnaujinti**, kad įkeltumėte duomenis.
1. Redaguokite reikalingus duomenis ir tada publikuokite juos. Jei mygtukas **Publikuoti** neprieinamas, tikriausiai kai kurie pagrindiniai laukai nebuvo įtraukti į „Excel“ darbaknygę.

## <a name="additional-resources"></a>Papildomi ištekliai

[Atsiskaitymo grynaisiais ir grynųjų pinigų valdymo operacijų redagavimas ir tikrinimas](edit-cash-trans.md)

[Internetinio užsakymo ir asinchroninio kliento užsakymo operacijų redagavimas ir tikrinimas](edit-order-trans.md)

[Mažmeninės prekybos operacijų finansinių dimensijų redagavimas](edit-financial-dim.md)

[Laukų įtraukimas į „Excel“ darbaknygę norint redaguoti mažmeninės prekybos operacijas](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]