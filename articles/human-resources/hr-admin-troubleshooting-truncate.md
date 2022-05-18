---
title: Kaip išvengti pareigų hierarchijos teksto trumpinimo ir ją eksportuoti į „Visio“
description: Šioje temoje paaiškinama, kaip išspręsti asmenų vardų problemą bei pareigų pavadinimų trumpinimo problemą, kai klientai peržiūri „Microsoft Dynamics 365 Human Resources“ pareigų hierarchiją.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20331b3a06301d10177fd0d5734f6e33994ef123
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693954"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Kaip išvengti pareigų hierarchijos teksto trumpinimo ir ją eksportuoti į „Visio“


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Išduoti**

Kai klientas peržiūri „Microsoft Dynamics 365 Human Resources“ pareigų hierarchiją, asmenų vardai ir (arba) pavardės bei pareigų pavadinimai sutrumpinami. Todėl gali būti sudėtinga užfiksuoti ekrano kopiją arba išspausdinti ir paskirstyti hierarchiją.

![Pareigybių hierarchija.](media/position-h.png)

**Priežastis**

Toks veikimo būdas yra numatytas.

**Sprendimas**

Deja, vartotojai negali lengvai keisti teksto dydį. Tačiau galite eksportuoti pareigų hierarchiją iš „Human Resources“ ir importuoti ją į „Microsoft Visio“. Nors šis straipsnis buvo parašytas „Microsoft Dynamics AX 2012“, procesas vis dar taikomas „Human Resources“: [Pareigų hierarchijos eksportavimas į „Microsoft Visio“](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Norėdami eksportuoti į „Visio“, atlikite šiuos veiksmus.

1. Programoje „Human Resources“ atidarykite sąrašo puslapį **Pareigos**.

    Norėdami įtraukti daugiau informacijos į organizacijos struktūros diagramą, įtraukite laukus į sąrašą **Pareigos** kad jie būtų prieinami, kai vėliau šioje procedūroje naudosite **Organizacijos schemos vedlį**.

2. Veiksmų srityje pasirinkite mygtuką **Atidaryti naudojant „Microsoft Office“**, tada dalyje **Eksportuoti į „Excel“** pasirinkite **Pareigos**. Arba paspauskite Ctrl+T.

    ![Eksportuoti pareigų sąrašo puslapį į „Excel“.](media/org-admin.png)

3. Įrašykite eksportuotą „Excel“ failą.

    ![Eksportuoti į „Excel“ dialogo langą.](media/export-excel.png)

4. Programoje „Visio“ pasirinkite **„Visio“ – kurti naują**, tada pasirinkite šablono kategoriją **Įmonės**.

    ![Nauja diagrama.](media/new.png)

5. Pasirinkite **Organizacijos struktūros diagramų vediklis**, tada pasirinkite **Kurti**.

    ![Organizacijos struktūros diagramų vediklio dialogo langas.](media/orgchart-wizard.png)

6. Pasirinkite **Informacija, kuri jau saugoma faile arba duomenų bazėje**, tada pasirinkite **Pirmyn**.

    ![1 organizacijos struktūros diagramų vedlys.](media/orgchart-wizard7.png)

7. Pasirinkite **Tekstas, „Org Plus“ (\*.txt) arba „Excel“ failas**, tada pasirinkite **Pirmyn**.

    ![2 organizacijos struktūros diagramų vedlys.](media/orgchart-wizard3.png)

8. Naršykite, kad pasirinktumėte eksportuotą „Excel“ failą, kuriame yra pareigų hierarchija, tada pasirinkite **Pirmyn**.

    ![3 organizacijos struktūros diagramų vedlys.](media/orgchart-wizard2.png)

9. Lauką **Pavadinimas / vardas ir (arba) pavardė** nustatykite į **Pareigos**, lauką **Teikia ataskaitas** – į **Teikia ataskaitas pareigų atstovui**, tada pasirinkite **Pirmyn**.

    ![4 organizacijos struktūros diagramų vedlys.](media/orgchart-wizard1.png)

10. Pasirinkite laukus, kurie turi būti rodomi kiekviename mazge, tada pasirinkite **Pirmyn**.

    ![5 organizacijos struktūros diagramų vedlys.](media/orgchart-wizard5.png)

11. Įtraukite stulpelį **Pareigos** į sąrašą **Duomenų laukų formavimas**, tada pasirinkite **Pirmyn**.

    ![6 organizacijos struktūros diagramų vedlys.](media/orgchart-wizard6.png)

12. Šiuo metu paveikslėlių nėra. Todėl kitame puslapyje pasirinkite **Pirmyn**.
13. Pasirinkite **Noriu, kad vediklis automatiškai visuose puslapiuose suskaidytų mano organizacijos diagramą**.

    ![7 organizacijos struktūros diagramų vedlys.](media/orgchart-wizard4.png)

14. Pasirinkite **Baigti**.

    Jei yra pareigų, nesančių struktūroje, bus paprašyta įtraukti jas į diagramą.

„Visio“ sugeneruota diagrama kiekvieną vadybininką rodo atskirame darbalapyje.

Pagal laukus, kuriuos pasirinkote įtraukti į diagramą, sugeneravus „Visio“ failą, kiekvienas mazgas rodo atitinkamą informaciją.

![Hierarchijos diagrama.](media/hierarchy.png)

**Papildoma parinktis**

Programoje „Human Resources“ taip pat galėsite naudoti darbo sritį **Žmonės**, norėdami peržiūrėti tam tikrą su hierarchija susijusią informaciją.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
