---
title: Kliento mokėjimo prognozių įjungimas (peržiūros versija)
description: Šioje temoje paaiškinama, kaip įjungti ir konfigūruoti modulio Finansinės įžvalgos funkciją Kliento mokėjimo prognozės.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 584c1af5f9252a4b8c88a8866a64184bd0595b2e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009423"
---
# <a name="enable-customer-payment-predictions-preview"></a>Kliento mokėjimo prognozių įjungimas (peržiūros versija)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip įjungti ir konfigūruoti modulio Finansinės įžvalgos funkciją Kliento mokėjimo prognozės. Galite įjungti funkciją darbo srityje **Funkcijų valdymas**, o konfigūracijos parametrus įvesti puslapyje **Modulio Finansinės įžvalgos parametrai**. Šioje temoje taip pat pateikiama informacija, kuri gali padėti veiksmingai naudoti funkciją.

> [!NOTE]
> Prieš atlikdami šiuos veiksmus, būtinai atlikite būtinuosius veiksmus, aprašytus temoje [Konfigūravimas moduliui Finansinės įžvalgos](configure-for-fin-insites.md).

1. Naudokite informaciją iš aplinkos puslapio portale „Microsoft Dynamics Lifecycle Services“ (LCS), kad prisijungtumėte prie pirminio „Azure SQL“ tos aplinkos egzemplioriaus. Norėdami įjungti smėlio dėžės aplinkos testus, vykdykite tolesnę Transact-SQL (T-SQL) komandą. (Gali reikėti įjungti prieigą prie savo IP adreso portale LCS, kad galėtumėte nuotoliniu būdu prisijungti prie programos objektų serverio \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > Jei jūsų „Microsoft Dynamics 365 Finance“ įdiegtis yra „Service Fabric“ įdiegtis, galite praleisti šį veiksmą. Modulio Finansinės įžvalgos komanda jums jau turėjo įjungti testą. Jei nematote funkcijos darbo srityje **Funkcijų valdymas** arba jei kyla problemų bandant ją įjungti, kreipkitės adresu <fiap@microsoft.com>.

2. Funkcijos Kliento mokėjimo įžvalgos įjungimas

    1. Eikite į **Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**.
    2. Rasti funkciją, pavadintą **Kliento mokėjimo įžvalgos (peržiūros versija)**.
    3. Pasirinkite **Įjungti dabar**.

    Funkcija Kliento mokėjimo įžvalgos dabar yra įjungta ir parengta konfigūruoti.

3. Funkcijos Kliento mokėjimo įžvalgos konfigūravimas

    1. Nueikite į **Kreditas ir surinkimas \> Sąranka \> Finansinės įžvalgos \> Modulio Finansinės įžvalgos parametrai**.

        [![Puslapis Modulio Finansinės įžvalgos parametrai prieš funkciją konfigūruojant](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. Puslapio **Modulio Finansinės įžvalgos parametrai** skirtuke **Kliento mokėjimo įžvalgos** pasirinkite saitą **Peržiūrėti duomenų laukus, naudojamus prognozavimo modelyje**, kad atidarytumėte puslapį **Prognozavimo modelio duomenų laukai**. Čia galite peržiūrėti numatytąjį laukų, kurie naudojami kuriant kliento mokėjimo prognozių dirbtinio intelekto (DI) prognozavimo modelį, sąrašą.

        Norėdami naudoti numatytąjį laukų sąrašą, kad būtų galima sukurti prognozavimo modelį, uždarykite puslapį **Prognozavimo modelio duomenų laukai**, tada puslapyje **Modulio Finansinės įžvalgos parametrai** nustatykite parinktį **Įjungti funkciją** kaip **Taip**.

    3. Nurodykite „labai pavėluotą“ operacijos laikotarpį, kad nustatytumėte, ką jūsų įmonei reiškia prognozavimo talpykla **Labai vėluoja**.

        Kiekvienoje atidarytoje SF sistema prognozuoja mokėjimo tikimybę pagal tris talpyklas: **Laiku**, **Vėluoja** ir **Labai vėluoja**.

        - **Laiku** – ši talpykla apima mokėjimus, kurie, kaip prognozuojama, bus sumokėti operacijos termino dieną arba anksčiau.
        - **Vėluoja** – ši talpykla apima mokėjimus, kurie, kaip prognozuojama, bus sumokėti po operacijos termino dienos, bet prieš „labai vėluojančio“ operacijos laikotarpio pradžią.
        - **Labai vėluoja** – ši talpykla apima mokėjimus, kurie, kaip prognozuojama, bus sumokėti prasidėjus „labai vėluojančiam“ operacijos laikotarpiui.

        > [!NOTE]
        > Pakeitus „labai vėluojantį“ operacijos laikotarpį ir pasirinkus **Pakeisti vėlavimo ribinę reikšmę** po to, kai buvo sukurtas kliento mokėjimų DI prognozavimo modelis, esamas prognozavimo modelis panaikinamas ir sukuriamas naujas modelis. Naujas prognozavimo modelis perkels operacijas į „labai vėluojantį“ laikotarpį, atsižvelgdamas į parametrus, įvestus jam nustatyti.

    4. Kai baigsite apibrėžti „labai vėluojantį“ operacijos laikotarpį, pasirinkite **Kurti prognozavimo modelį**, kad sukurtumėte prognozavimo modelį. Puslapio **Modulio Finansinės įžvalgos parametrai** skyriuje **Prognozavimo modelis** rodoma prognozavimo modelio būsena.

        > [!NOTE]
        > Bet kuriuo metu kurdami prognozavimo modelį, galite pasirinkti **Iš naujo nustatyti modelio kūrimą**, kad procesas būtų paleistas iš naujo.

    Funkcija jau sukonfigūruota ir yra parengta naudoti.

Kai funkcija įjungta ir sukonfigūruota, o prognozavimo modelis sukurtas ir veikia, puslapio **Modulio Finansinės įžvalgos parametrai** skyriuje **Prognozavimo modelis** rodomas modelio tikslumas, kaip parodyta šioje iliustracijoje.

[![Prognozavimo modelio tikslumas puslapyje Modulio Finansinės įžvalgos parametrai](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>Išleidimo informacija

Bandomąją modulio Finansinės įžvalgos viešosios peržiūros versiją galima įdiegti Jungtinėse Amerikos Valstijose, Europoje ir Jungtinėje Karalystėje. „Microsoft“ palaipsniui į palaikomų regionų sąrašą įtraukia daugiau regionų.

Viešosios peržiūros versijos funkcijos gali ir turi būti įjungtos tik 2 pakopos smėlio dėžės aplinkose. Sąrankos ir DI modelių, sukurtų smėlio dėžės aplinkoje, negalima perkelti į gamybos aplinką. Norėdami gauti daugiau informacijos, žr. [„Microsoft Dynamics 365“ peržiūros versijų papildomos naudojimo sąlygos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Privatumo pranešimas

Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]