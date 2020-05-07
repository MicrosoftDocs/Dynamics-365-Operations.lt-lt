---
title: Išplėstinių atsiskaitymo pagal eigą sutarčių kūrimas
description: Šioje temoje paaiškinama, kaip kurti projekto sutartis, kad būtų galima generuoti klientų SF, atsižvelgiant į užbaigto darbo procentinę dalį.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282839"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Išplėstinių atsiskaitymo pagal eigą sutarčių kūrimas
[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip kurti projekto sutartis, kad būtų galima kurti klientų SF, atsižvelgiant į užbaigto darbo procentinę dalį. Automatiškai apskaičiuojamos projekte nustatyto darbo biudžeto kategorijų SF sumos. SF išrašymo laikas nustatomas derinant projekto sutartį su klientu.

Naudokite šioje temoje aprašytas procedūras, norėdami nustatyti sutartį, susijusį projektą ir atsiskaitymo taisykles, apskaičiuojančias projekte numatyto darbo biudžeto kategorijų SF sumas.

Sukūrę sutartį ir projektą, galite nustatyti išsamią projekto informaciją. Pvz., galite nustatyti veiklą ir priskirti darbuotojus projektui.

## <a name="example"></a>Pavyzdys

Jūsų organizacija yra programinę įrangą kurianti įmonė. Jūs sutinkate klientui sukurti darbo užmokesčio apskaitos paketą už 20 000 JAV dolerių (USD). Jūsų organizacija susitaria išrašyti klientui SF, kai bus atlikta tam tikra projekto dalis. Galite nustatyti tolesnes darbo projekto kategorijas, kad galėtumėte jas naudoti atsiskaitymo procese.

- Konsultavimas
- Dizainas
- Diegimas

Taip pat galite nustatyti atsiskaitymo taisykles, kad SF sumos būtų automatiškai apskaičiuojamos pagal tai, kiek atlikta kiekvienos kategorijos projekto darbo.

Biudžeto vadybininkas sukuria biudžetą pagal projekto kategorijas. Atlikto darbo kiekis automatiškai apskaičiuojamas procentais pagal faktinio darbo kiekį, palyginti su biudžeto sumomis.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš kurdami projektą, naudojantį atsiskaitymo taisykles, turite nustatyti atsiskaitymo taisyklių numeracijas ir mokesčių žurnalą, naudojamą registruoti sąskaitų pateikimo eigą.

1. Eikite į **Projektų valdymas ir apskaita** \> **Nustatymas** \> **Projektų valdymo ir apskaitos parametrai**.
2. Puslapyje **Projekto valdymo ir apskaitos parametrai**, skirtuke **Numeracijos**, nustatykite numeraciją, kurią norite naudoti, kai kuriamos atsiskaitymo taisyklės.
3. Eikite į **Projektų valdymas ir apskaita** \> **Žurnalai** \> **Mokestis**.
4. Puslapyje **Mokesčių žurnalas** pasirinkite **Naujas** ir įveskite žurnalo pavadinimą.

## <a name="create-a-contract-for-progress-billings"></a>Sukurkite sutartį dėl sąskaitų pateikimo eigos.

Naudodami šią procedūrą sukurkite projekto sutartį, skirtą fiksuotos kainos projektui. Galite sukurti projekto SF, kai įvykdyta nurodyta dalis projekto darbų (procentais).

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Projekto sutartys**.
2. Puslapyje **Projekto sutartys** pasirinkite **Naujas**.
3. Dialogo lange **Nauja projekto sutartis** nustatykite tolesnius laukus.

    - **Vardas ir (arba) pavardė**
    - **Lėšų skyrimo tipas**
    - **Lėšų skyrimo šaltinis**
    - **Pardavimo valiuta** – pagal numatytuosius parametrus ši valiuta naudojama kliento SF, kurios susietos si projekto sutartimi. Tačiau galite keisti konkrečios kliento SF pardavimo valiutą.

4. Pasirinkite **Gerai**. Informacija nukopijuojama į puslapio **Projekto sutartys** antraštę.
5. Puslapyje **Projekto sutartys** įveskite likusią reikiamą projekto informaciją.

## <a name="create-a-project-for-progress-billings"></a>Sąskaitų pateikimo eigos projekto kūrimas

Atlikite šiuos veiksmus kurdami projektą ir visus subprojektus, susietus su projekto sutartimi.

1. Pasirinkite **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**.
2. Puslapyje **Visi projektai** pasirinkite **Nauja**.
3. Dialogo lango **Naujas projektas** lauke **Projekto tipas** pasirinkite **Laikas ir medžiagos**.
4. Pasirinkite projektų grupę. Projektų grupė nustato grupei priskirtų projektų registravimo informaciją.
5. Pasirinkite **Kurti projektą**.
6. Sukūrę projektą, nustatykite projekto etapą **Vykdoma**.

## <a name="create-a-budget-for-a-project"></a>Projekto biudžeto kūrimas

Biudžeto kategorijos naudojamos siekiant automatiškai apskaičiuoti SF sumas pagal tai, kiek atlikta kiekvienos kategorijos darbų. Atlikite tolesnius veiksmus, norėdami sukurti įvertintų savikainų biudžeto kategorijas.

1. Pasirinkite **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**.
2. Puslapyje **Visi projektai** pasirinkite ir atidarykite norimą projektą.
3. Puslapio **Projektai** veiksmų srityje, skirtuke **Planuoti**, grupėje **Biudžetas**, pasirinkite **Projekto biudžetas**.
4. Puslapyje **Projekto biudžetas** įveskite kiekvienos projekto kategorijos įvertintą savikainą.

## <a name="create-billing-rules-for-progress-billings"></a>Sąskaitų pateikimo eigai skirtų atsiskaitymo taisyklių kūrimas

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Projekto sutartys**.
2. Puslapyje **Projekto sutartys** pasirinkite ir atidarykite projekto sutartį.
3. Projekto sutarties puslapyje, „FastTab” **Atsiskaitymo taisyklės**, pasirinkite **Įtraukti**.
4. Puslapyje **Atsiskaitymo taisyklė**, lauke **Eilutės tipas**, pasirinkite **Eiga**.
5. „FastTab” **Atsiskaitymo taisyklės eilutės informacija**, lauke **Sutarties vertė**, įveskite bendrąją sutarties vertę.
6. Lauke **Kategorija** pasirinkite kategoriją, kurioje turi būti užregistruota mokesčio operacija.
7. Lauke **Projektas** pasirinkite projektą arba užduotį, kurioje naudojama ši atsiskaitymo taisyklė.
8. Pasirinktinai: atsiskaitymo taisyklę priskirkite papildomiems projektams. „FastTab” **Projektas** skyriuje **Galimi projektai** pasirinkite projektą, tada pasirinkite rodyklės dešinėn mygtuką, kad įtrauktumėte projektą į skyrių **Pasirinkti projektai**.
9. Pasirinktinai: apskaičiuokite procentinę sumą, kuri klientui išskaitoma iš mokėjimų sąskaitoje-faktūroje. „FastTab” **Mokėjimo užlaikymo sąlygos** pasirinkite lėšų skyrimo šaltinį, tada lauke **Užlaikymo procentinis dydis** įveskite užlaikymo procentą.
10. Kartokite šiuos veiksmus norėdami sukurti papildomas projekto sutarties atsiskaitymo taisykles.
