---
title: EKA programos ir vartotojo kalbos parametrai
description: "Šioje temoje aprašoma, kaip pakeisti kalbos parametrai mažmeninės prekybos šiuolaikinės POS (MPOS) ir debesies POS."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>EKA programos ir vartotojo kalbos parametrai

Šioje temoje aprašoma, kaip pakeisti kalbos parametrai mažmeninės prekybos šiuolaikinės POS (MPOS) ir debesies POS.

<a name="overview"></a>Apžvalga
========

Mažmeninės prekybos šiuolaikinės POS (MPOS) ir debesies POS palaiko aplinkoje, kur kalbos parametrus ir vertimai gali skirtis tarp parduotuvės ir vartotojo parametrus. Pvz., parduotuvės galėtų būti įsikūrusi regione, kur anglų kalba yra labiausiai paplitusi savo klientams, bet kai kurie darbuotojai labiau linkę naudoti programą su prancūzų vertimai.

## <a name="data-language"></a>Duomenų kalba
Neatsižvelgiant į vartotojo parametrus, MPOS ir debesies POS visada naudos parduotuvės kalbos parametrai nustatyti naudojami duomenų vertimus. Tai užtikrins, kad visi vartotojai ir klientai turės suderinti patirtį.  Duomenų pavyzdžiai:

-   Produktai
-   Atributai ir reikšmės
-   Kategorijų pavadinimai
-   Išspausdinti arba el. paštu išsiųsti operacijų kvitai
-   Mokėjimo būdo pavadinimai
-   Eilutės rodymo pranešimai

Parduotuvės kalba bus taip pat naudojamas pagrindinis POS prisijungimo ekrane, nes vartotojas nėra žinoma prieš prisijungdami. Jei vertimas nėra parduotuvės kalbos, Go grįš į bendrovės kalba.

### <a name="configuring-the-stores-language-setting"></a>Parduotuvės kalbos parametro konfigūravimas

Parduotuvės kalbos parametras nustatytas nuo **visi mažmeninės prekybos parduotuvėse** ant, **mažmeninės prekybos parduotuvėje** puslapio pagal ** bendrosios &gt;regiono parametrai &gt;kalba. ** Naudoti kritimo žemyn norėdami pasirinkti kalbą kiekvienos parduotuvės.

## <a name="user-interface-language"></a>Vartotojo sąsajos kalba
POS naudotojo kalbos parametras nustato vertimų naudojama programos vartotojo sąsajos. Tai apima visas etiketes, meniu ir sąrašai, kurie nėra laikomi duomenys. Viena išimtis yra tekstas, kuris rodomas POS mygtukynų. Mygtukyno nepalaiko vertimus, todėl jie bus visada Rodyti tekstą kaip apibrėžta mygtuką. Siekiant remti išverstų mygtukus, jūs turite kopijuoti ir išlaikyti atskirus mygtukynų ir jas priskirti vartotojams atitinkamai.

### <a name="configuring-the-users-language-setting"></a>Vartotojo kalbos parametro konfigūravimas

POS naudotojo kalbos parametras nustatytas nuo **visiems darbuotojams** ant, **darbuotojo** puslapio pagal **mažmeninės prekybos &gt;kalba**.  Jis nustatytas pagrindinis profilis skirtuką.  Šis parametras naudojamas ne iš EKA. Jei nenustatyta vartotojo kalba arba nustatyta kalba, kurios vertimų nėra, EKA iš naujo nustatys parduotuvės kalbą.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Vartotojo sąsajos kalbos** ** **      | **Duomenų kalba (produktų, gavimo kvitų formatų, eilutės rodymo ir kt.)** |
| **Įmonė** | Numatytoji                    | Numatytoji                                                           |
| **Parduotuvė**   | Perrašoma įmonė          | Perrašoma įmonė                                                 |
| **User**    | Perrašoma parduotuvė arba įmonė | Niekada                                                             |




