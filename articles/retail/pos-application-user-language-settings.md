---
title: EKA programos ir vartotojo kalbos parametrai
description: "Šioje temoje aprašoma, kaip keisti kalbos parametrus naudojant „Retail Modern POS“ (MPOS) ir „Cloud POS“."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cabb63aea0da4b264aec8e0cc4d43b3e1014e71b
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="pos-application-and-user-language-settings"></a>EKA programos ir vartotojo kalbos parametrai

[!include[banner](includes/banner.md)]


Šioje temoje aprašoma, kaip keisti kalbos parametrus naudojant „Retail Modern POS“ (MPOS) ir „Cloud POS“.

<a name="overview"></a>Apžvalga
========

„Retail Modern POS“ (MPOS) ir „Cloud POS“ palaiko aplinkas, kuriose parduotuvės ir vartotojų nustatyti kalbos parametrai ir vertimai gali skirtis. Pavyzdžiui, parduotuvė gali būti regione, kuriame klientai dažniausiai vartoja anglų kalbą, bet kai kurie darbuotojai labiau norėtų naudoti programą, kuri išversta į prancūzų kalbą.

## <a name="data-language"></a>Duomenų kalba
Nepriklausomai nuo to, kokie yra vartotojo parametrai, nusprendžiant, kokius naudoti duomenų vertimus, MPOS ir „Cloud POS“ visada naudojami parduotuvės kalbos parametrai. Taip užtikrinama, kad visų vartotojų ir klientų patirtis būtų nuosekli.  Duomenų pavyzdžiai:

-   Produktai
-   Atributai ir reikšmės
-   Kategorijų pavadinimai
-   Išspausdinti arba el. paštu išsiųsti operacijų kvitai
-   Mokėjimo būdo pavadinimai
-   Eilutės rodymo pranešimai

Parduotuvės kalba taip pat naudojama pagrindiniame EKA prisijungimo ekrane, nes kol neprisijungiama vartotojas nežinomas. Jei parduotuvės kalba vertimo nėra, EKA iš naujo nustatys įmonės kalbą.

### <a name="configuring-the-stores-language-setting"></a>Parduotuvės kalbos parametro konfigūravimas

Parduotuvės kalbos parametras yra nustatomas dalyje **Visos mažmeninės prekybos parduotuvės**, kurią galima rasti puslapyje **Mažmeninės prekybos parduotuvė** pasirinkus **Bendrieji parametrai &gt; Regiono parametrai &gt; Kalba. **Naudodami išskleidžiamąjį sąrašą pasirinkite kiekvienos parduotuvės kalbą.

## <a name="user-interface-language"></a>Vartotojo sąsajos kalba
Pagal EKA vartotojo kalbos parametrus nustatomi programos vartotojo sąsajoje naudojami vertimai. Vertimai naudojami visose etiketėse, meniu ir sąrašuose, kurie nelaikomi duomenimis. Viena išimtis yra EKA mygtukynuose rodomas tekstas. Mygtukynuose vertimai nepalaikomi, todėl tekstas juose visada rodomas taip, kaip nurodyta ant mygtuko. Norint, kad būtų palaikomi išversti mygtukai, reikia nukopijuoti ir išlaikyti atskirus mygtukynus ir priskirti juos atitinkamiems vartotojams.

### <a name="configuring-the-users-language-setting"></a>Vartotojo kalbos parametro konfigūravimas

EKA vartotojo kalbos parametras yra nustatomas dalyje **Visi darbuotoji**, kurią galima rasti puslapyje **Darbuotojas** pasirinkus **Mažmeninė prekyba &gt; Kalba**.  Jis nėra nustatomas pagrindiniame profilio skirtuke. EKA šio parametro nenaudoja. Jei nenustatyta vartotojo kalba arba nustatyta kalba, kurios vertimų nėra, EKA iš naujo nustatys parduotuvės kalbą.  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | **Vartotojo sąsajos kalba** ** **      | **Duomenų kalba (produktų, gavimo kvitų formatų, eilutės rodymo ir kt.)** |
| **Įmonė** | Numatytoji                    | Numatytoji                                                           |
| **Parduotuvė**   | Perrašoma įmonė          | Perrašoma įmonė                                                 |
| **Vartotojas**    | Perrašoma parduotuvė arba įmonė | Niekada                                                             |






