---
title: "Pridėti rekomendacijas valdymo operacijų puslapio POS įrenginį"
description: "Šioje temoje aprašoma, kaip pridėti rekomendacijas valdymo operacijos ekrano dėl pardavimo (PV) įrenginį naudodami ekrano maketo konstruktorių Microsoft Dynamics 365 operacijoms."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>Pridėti rekomendacijas valdymo operacijų puslapio POS įrenginį

Šioje temoje aprašoma, kaip pridėti rekomendacijas valdymo operacijos ekrano dėl pardavimo (PV) įrenginį naudodami ekrano maketo konstruktorių Microsoft Dynamics 365 operacijoms.

Produktų rekomendacijos gali Rodyti POS įrenginyje, kai naudojate Microsoft Dynamics 365 operacijoms. *Rekomendacijos* daiktų, kad jūsų klientas gali būti domina pagal jų pirkimo istoriją, prekes į savo pageidavimų sąrašus ir daiktų, kad kitiems klientams įsigyti internetu ir plytų ir skiedinio parduotuvėse. Norėdami Rodyti produkto rekomendacijos, jums reikia pridėti valdymo operacijos ekrane, naudojant ekrano maketo konstruktorių.

## <a name="open-layout-designer"></a>Atidaryti maketo dizaineris
1.  Eikite į **mažmeninės prekybos ir prekybos**&gt;**kanalo nustatymas**&gt;**POS sąrankos**&gt;**POS**&gt;**ekrano išdėstymas**.
2.  Naudoti sparčiojo filtro rasti ekrano, kurį norite įtraukti į valdiklį. Pvz., filtruoti ir **ekrano išdėstymas ID** lauko naudoti vertė yra "F2CP16:9M".
3.  Sąraše raskite ir pasirinkite norimą įrašą. Pavyzdžiui, pasirinkite "pavadinimas: ekranas F2CP16:9M ID: F2CP16:9M".
4.  Spustelėkite **maketo dizaineris**.
5.  Vykdykite nurodymus, kad paleistumėte maketo konstruktorių. Kai būsite paraginti įvesti kredencialus, įvesti tuos pačius kredencialus, buvo naudojami kai maketo konstruktorių buvo pradėta nuo **ekrano išdėstymas** puslapis.
6.  Kai prisijungsite, pasirodys puslapis panašus į vieną žemiau. Išdėstymo skirsis priklausomai nuo to, visus tinkinimus, atliktus jūsų parduotuvės.

[![screenlayout-IPS-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) pasirinkti rodymo parinktį
-----------------------

Yra du konfigūracijų variantų. Pasirinkite variantą, kuris geriausiai tinka jūsų parduotuvės ir likusius nurodymus, kad baigtumėte konfigūruoti kontrolę. Yra du variantai:
-   Rekomendacijos visada yra matomas.
-   A **rekomendacijų** skirtukas tinklelio dešinėje pusėje ekrano.

#### <a name="to-make-recommendations-always-visible"></a>Pateikti rekomendacijas visada matomas

1.  Sumažinti operacijos eilutės informacijos srityje taip, kad jis yra tokio pat aukščio kaip klientas skydo kairėje. [](./media/pic-2.png)[![screenlayout-IPS-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)
2.  Iš meniu kairėje, vilkite ir upuść rekomendacijas valdiklį, kad tarp operacijos eilutės detales ir mygtukyno centras operacijos ekrano apačioje. Pakeiskite valdiklio dydį, kad jis telpa į tą erdvę. [](./media/pic-3.png)[![screenlayout-IPS-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)
3.  Spustelėkite į **X** išsaugoti ir išeiti iš maketo konstruktorių.
4.  Dynamics 365 operacijoms, eikite į **mažmeninės prekybos ir prekybos**&gt;**mažmeninės prekybos ji**&gt;**pasiskirstymo tvarkaraščių**.
5.  Sąraše, pasirinkite **1090 registrų**.
6.  Spustelėkite **surengę**.

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>Norėdami pridėti rekomendacijas skirtuką mygtukyno dešinėje pusėje ekrano

1.  Dešiniuoju pelės mygtuku spustelėkite tuščioje vietoje žemiau paskutinį skirtuką puslapio dešinėje pusėje mygtuką tinklelį.
2.  Spustelėkite **pritaikyti**. [![pic-5](./media/pic-5.png)](./media/pic-5.png)
3.  Spustelėkite **naujas skirtukas**.
4.  Raskite ką tik įtrauktą naują skirtuką. Jums gali reikėti slinkti žemyn.
5.  – Į **turinį** meniu, pasirinkite **rekomenduojama produktus**. [![IPS-6](./media/pic-6.png)](./media/pic-6.png)
6.  – Į **ženklo** lauke, įveskite pavadinimą skirtuką rekomendacijas. Pavyzdžiui, įveskite "Rekomenduotini produktai".
7.  – Į **vaizdo** pasirinkite vaizdas būtų rodomas skirtuke.
8.  Click **OK**. Skirtuke atsiranda mygtukynas.
9.  Spustelėkite į **X** išsaugoti ir išeiti iš maketo konstruktorių.
10. Dynamics 365 operacijoms, eikite į **mažmeninės prekybos ir prekybos**&gt;**mažmeninės prekybos ji**&gt;**pasiskirstymo tvarkaraščių**.
11. Sąraše, pasirinkite **1090 registrų**.
12. Spustelėkite **surengę**.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Asmeninį produktų rekomendacijų apžvalga](personalized-product-recommendations.md)


