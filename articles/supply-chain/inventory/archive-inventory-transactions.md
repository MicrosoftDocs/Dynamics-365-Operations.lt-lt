---
title: Archyvuoti atsargų operacijas
description: Šioje temoje aprašoma, kaip archyvuoti atsargų operacijų duomenis, kad būtų pagerintas sistemos našumas.
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: bacc27c1a9066892c51110d28ba9a2ad26bebe77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839300"
---
# <a name="archive-inventory-transactions"></a>Archyvuoti atsargų operacijas

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Laikui bėgant atsargų operacijų lentelė (`InventTrans`) toliau plečiasi ir sunaudoja daugiau duomenų bazės vietos. Todėl dėl lentelės pateiktos užklausos palaipsniui veiks lėčiau. Šioje temoje aprašoma, kaip galima naudoti atsargų operacijų archyvo priemonę *duomenims apie atsargų operacijas archyvuoti* siekiant pagerinti sistemos našumą.

> [!NOTE]
> Tik finansiškai atnaujintas atsargų operacijas galima suarchyvuoti pasirinktu uždarytu DK laikotarpiu. Norint suarchyvuoti, finansiškai atnaujintų siunčiamų atsargų operacijų išdavimo būsena turi būti *Parduota*, o gavimo atsargų operacijų gavimo būsena turi būti *Nupirkta*.

Archyvuojant atsargų operacijas, visos susijusios operacijos perkeliamos į lentelę `InventTransArchive`. Atsargų išdavimo ir atsargų gavimo operacijos archyvuojamos atskirai, remiantis prekės ID (`itemId`) ir atsargų dimensijos ID (`inventDimId`) kombinacija, o tada jos pateikiamos į išdavimo ir gavimo operacijų suvestinę.

Jei `itemId` ir `inventDimId` kombinacijoje yra tik viena gavimo arba išdavimo operacija, operacija nebus archyvuota.

## <a name="turn-on-the-feature-in-your-system"></a>Funkcijos įjungimas sistemoje

Jei jūsų sistemoje dar nėra funkcijų, aprašytų šioje temoje, eikite į [Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ir įjunkite funkciją *Atsargų operacijų archyvas*.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Dalykai, į kuriuos reikia atsižvelgti archyvuojant atsargų operacijas

Prieš archyvuojant atsargų operacijas reikia atsižvelgti į šiuos verslo scenarijus, nes juos paveiks operacija:

- Kai audituojate atsargų operacijas iš susijusių dokumentų, pvz., pirkimo užsakymo eilučių, jos bus rodomos kaip suarchyvuotos. Norėdami peržiūrėti suarchyvuotas operacijas, turite eiti į **Atsargų valdymas\>Periodinės užduotys \>Valyti \> Atsargų operacijų archyvas**.
- Negalima atšaukti suarchyvuotų laikotarpių atsargų uždarymo. Prieš atšaukdami atsargų uždarymą, turite atšaukti atitinkamo laikotarpio atsargų operacijų archyvą.
- Suarchyvuotų laikotarpių standartinių išlaidų konvertuoti negalima. Prieš atlikdami standartinį savikainos konvertavimą, turite atšaukti atitinkamo laikotarpio atsargų operacijų archyvą.
- Atsargų ataskaitos, išgaunamos iš atsargų operacijų, bus paveiktos archyvuojant atsargų operacijas. Šios ataskaitos apima atsargų skirstymo ataskaitą ir atsargų vertės ataskaitas.
- Atsargų prognozės gali būti paveiktos, jei jos paleidžiamos archyvuotų laikotarpių laikotarpiu.

## <a name="prerequisites"></a>Būtinieji komponentai

Atsargų operacijos gali būti suarchyvuotos tik per laikotarpius, kai tenkinamos šios sąlygos:

- DK laikotarpis turi būti uždarytas.
- Atsargų uždarymas turi būti vykdomas archyvo dieną arba laikotarpiu po jos.
- Laikotarpis turi būti bent metus prieš archyvo pradžios laikotarpio datą.
- Neturi būti jokių esamų atsargų perskaičiavimų.

## <a name="archive-inventory-transactions"></a>Archyvuoti atsargų operacijas

Norėdami archyvuoti atsargų operacijas, atlikite toliau nurodytus veiksmus.

1. Eikite į **Atsargų valdymas** \> **Periodinės užduotys** \> **Valymas** \> **Atsargų operacijų archyvų**.

    Rodomas puslapis **Atsargų operacijų archyvas** bei archyvuotų proceso įrašų sąrašas.

    ![Atsargų operacijų archyvo puslapis](media/archive-inventory-empty.png "Atsargų operacijų archyvo puslapis")

1. Veiksmų srityje pasirinkite **Atsargų operacijų archyvas**, kad sukurtumėte atsargų operacijų archyvas.
1. Dialogo lange **Atsargų operacijų archyvas** „FastTab“ skirtuke **Parametrai** nustatykite šiuos laukelius:

    - **Nuo uždarymo DK laikotarpio pradžios datos** – pasirinkite anksčiausią operacijos datą, kuri bus įtraukta į archyvą.
    - **Iki uždarymo DK laikotarpio pradžios datos** – pasirinkite vėliausią operacijos datą, kuri bus įtraukta į archyvą.

    ![Atsargų operacijų archyvo dialogo langas](media/archive-inventory-dates.png "Atsargų operacijų archyvo dialogo langas")

    > [!NOTE]
    > Bus galima pasirinkti tik laikotarpius, kurie atitinka [būtinas sąlygas](#prerequisites).

1. Prireikus, „FastTab“ skirtuke **Vykdyti fone** nustatykite paketinio vykdymo informaciją. Atlikite įprastus „Microsoft Dynamics 365 Supply Chain Management“ paketinių užduočių veiksmus.
1. Pasirinkite **Gerai**.
1. Gaunate pranešimą, kuriuo prašoma patvirtinti, kad norite tęsti. Atidžiai perskaitykite pranešimą ir pasirinkite **Taip**, jei norite tęsti.

    Gaunate pranešimą, kuriame teigiama, kad jūsų atsargų operacijų archyvo užduotis buvo įtraukta į paketinių užduočių eilę. Dabar užduotis pradės archyvuoti atsargų operacijas nuo pasirinkto laikotarpio.

## <a name="view-archived-inventory-transactions"></a>Peržiūrėti archyvuotas atsargų operacijas

Puslapyje **Atsargų operacijų archyvas** rodoma visa archyvavimo retrospektyva. Kiekvienoje tinklelio eilutėje rodoma tokia informacija kaip archyvo sukūrimo data, jį sukūręs naudotojas ir jo būsena.

![Atsargų operacijų archyvavimo retrospektyvos puslapis](media/archive-inventory-full.png "Atsargų operacijų archyvavimo retrospektyvos puslapis")

Norėdami filtruoti tinklelyje rodomus archyvus, puslapio viršuje pateiktame išskleidžiamajame sąraše pasirinkite vieną iš nurodytų verčių:

- **Aktyvūs** – rodyti tik aktyvius archyvus, bet ne atšauktus archyvus.
- **Visi** – rodyti visus archyvus – tiek aktyvius, tiek atšaukus.

Kiekvienam tinklelio archyvui pateikiama ši informacija:

- **Aktyvus** – varnelė rodo, kad archyvas yra aktyvus.
- **Pradžios data** – seniausios operacijos, kurią galima įtraukti į archyvą, data.
- **Pabaigos data** – naujausios operacijos, kurią galima įtraukti į archyvą, data.
- **Suplanuota** – naudotojo, sukūrusio archyvą, paskyra.
- **Įvykdyta** – archyvo sukūrimo data.
- **Atšauktas** – varnelė rodo, kad archyvas buvo atšauktas.
- **Stabdyti dabartinį atnaujinimą** – varnelė rodo, kad archyvavimas vyksta, bet buvo pristabdytas.
- **Būsena** – archyvo apdorojimo būsena. Galimos vertės: *Laukiama*, *Vykdoma* ir *Baigta*.

Įrankių juostoje virš tinklelio yra šie mygtukai, kuriuos galima naudoti darbui su pasirinktu archyvu:

- **Archyvuotos operacijos** – visos pasirinkto archyvo informacijos peržiūra. Rodomame puslapyje **Archyvuotos operacijos** rodomos visos archyvo operacijos.

    ![Archyvuotų operacijų puslapis](media/archive-inventory-transactions.png "Archyvuotų operacijų puslapis")

    Norėdami peržiūrėti daugiau informacijos apie konkrečias operacijas puslapyje **Archyvuotos operacijos**, pasirinkite tinklelį, o tada, veiksmų srityje pasirinkite **Archyvuotos operacijos duomenys**. Rodomame puslapyje **Archyvuotos operacijos duomenys** rodoma tokia informacija kaip DK registravimas, susijusios papildomos DK nuorodos ir finansinės dimensijos.

- **Archyvavimo pristabdymas** – šiuo metu apdorojamo pasirinkto archyvavimo pristabdymas. Pristabdymas vykdomas tik sugeneravus archyvavimo užduotį. Todėl prieš įsigaliojant pauzei galimas nedidelis uždelsimas. Pristabdžius archyvavimą laukelyje **Stabdyti dabartinį atnaujinimą** pasirodo varnelė.
- **Archyvavimo tęsimas** – šiuo metu apdorojamo pasirinkto archyvavimo vykdymo tęsimas.
- **Atšaukti** – pasirinkto archyvavimo atšaukimas. Archyvavimą galima atšaukti tik jei jo laukelis **Būsena** nustatytas kaip *Baigta*. Atšaukus archyvavimą laukelyje **Atšaukti** pasirodo varnelė.
