---
title: Kaip išvengti pareigų hierarchijos teksto trumpinimo ir ją eksportuoti į „Visio“
description: Šioje temoje paaiškinama, kaip išspręsti asmenų vardų ir (arba) pavardžių bei pareigų pavadinimų trumpinimo problemą, kai klientai peržiūri „Microsoft Dynamics 365 Talent“ pareigų hierarchiją. Dėl teksto trumpinimo gali būti sudėtinga užfiksuoti ekrano kopiją arba išspausdinti hierarchiją.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e151818f29ac37ff449daaf1dc02e44b8fb317c3
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008505"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Kaip išvengti pareigų hierarchijos teksto trumpinimo ir ją eksportuoti į „Visio“

[!include [banner](includes/banner.md)]

**Išduoti**

Kai klientas peržiūri „Microsoft Dynamics 365 Talent“ pareigų hierarchiją, asmenų vardai ir (arba) pavardės bei pareigų pavadinimai sutrumpinami. Todėl gali būti sudėtinga užfiksuoti ekrano kopiją arba išspausdinti ir paskirstyti hierarchiją.

![Darbo vietų hierarchija](media/position-h.png)

**Priežastis**

Toks veikimo būdas yra numatytas.

**Skiriamoji geba**

Deja, vartotojai negali lengvai keisti teksto dydį. Tačiau galite eksportuoti pareigų hierarchiją iš „Talent“ ir importuoti ją į „Microsoft Visio“. Nors šis straipsnis buvo parašytas „Microsoft Dynamics AX 2012“, procesas vis dar taikomas „Talent“: [Pareigų hierarchijos eksportavimas į „Microsoft Visio“](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Norėdami eksportuoti į „Visio“, atlikite šiuos veiksmus.

1. Programoje „Talent“ atidarykite sąrašo puslapį **Pareigos**.

    Norėdami įtraukti daugiau informacijos į organizacijos struktūros diagramą, įtraukite laukus į sąrašą **Pareigos**, kad jie būtų prieinami, kai vėliau šioje procedūroje naudosite vediklį.

2. Veiksmų srityje pasirinkite mygtuką **Atidaryti naudojant „Microsoft Office“**, tada dalyje **Eksportuoti į „Excel“** pasirinkite **Pareigos**. Arba paspauskite Ctrl+T.

    ![Eksportuoti pareigų sąrašo puslapį į „Excel“](media/org-admin.png)

3. Įrašykite eksportuotą „Excel“ failą.

    ![Eksportuoti į „Excel“ dialogo langą](media/export-excel.png)

4. Programoje „Visio“ pasirinkite **„Visio“ – kurti naują**, tada pasirinkite šablono kategoriją **Įmonės**.

    ![Nauja diagrama](media/new.png)

5. Pasirinkite**Organizacijos struktūros diagramų vediklis**, tada pasirinkite **Kurti**.

    ![Organizacijos struktūros diagramų vediklio dialogo langas](media/orgchart-wizard.png)

6. Pasirinkite **Informacija, kuri jau saugoma faile arba duomenų bazėje**, tada pasirinkite **Pirmyn**.

    ![1 organizacijos struktūros diagramų vediklis](media/orgchart-wizard7.png)

7. Pasirinkite **Tekstas, „Org Plus“ (\*.txt) arba „Excel“ failas**, tada pasirinkite **Pirmyn**.

    ![2 organizacijos struktūros diagramų vediklis](media/orgchart-wizard3.png)

8. Naršykite, kad pasirinktumėte eksportuotą „Excel“ failą, kuriame yra pareigų hierarchija, tada pasirinkite **Pirmyn**.

    ![3 organizacijos struktūros diagramų vediklis](media/orgchart-wizard2.png)

9. Lauką **Pavadinimas / vardas ir (arba) pavardė** nustatykite į **Pareigos**, lauką **Teikia ataskaitas** – į **Teikia ataskaitas pareigų atstovui**, tada pasirinkite **Pirmyn**.

    ![4 organizacijos struktūros diagramų vediklis](media/orgchart-wizard1.png)

10. Pasirinkite laukus, kurie turi būti rodomi kiekviename mazge, tada pasirinkite **Pirmyn**.

    ![5 organizacijos struktūros diagramų vediklis](media/orgchart-wizard5.png)

11. Įtraukite stulpelį **Pareigos** į sąrašą **Duomenų laukų formavimas**, tada pasirinkite **Pirmyn**.

    ![6 organizacijos struktūros diagramų vediklis](media/orgchart-wizard6.png)

12. Šiuo metu paveikslėlių nėra. Todėl kitame puslapyje pasirinkite **Pirmyn**.
13. Pasirinkite **Noriu, kad vediklis automatiškai visuose puslapiuose suskaidytų mano organizacijos diagramą**.

    ![7 organizacijos struktūros diagramų vediklis](media/orgchart-wizard4.png)

14. Pasirinkite **Baigti**.

    Jei yra pareigų, nesančių struktūroje, bus paprašyta įtraukti jas į diagramą.

„Visio“ sugeneruota diagrama kiekvieną vadybininką rodo atskirame darbalapyje.

Pagal laukus, kuriuos pasirinkote įtraukti į diagramą, sugeneravus „Visio“ failą, kiekvienas mazgas rodo atitinkamą informaciją.

![Hierarchijos diagrama](media/hierarchy.png)

**Papildoma parinktis**

Programoje „Talent“ taip pat galėsite naudoti darbo sritį **Žmonės**, norėdami peržiūrėti tam tikrą su hierarchija susijusią informaciją.
