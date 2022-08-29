---
title: Elektroninio kasos aparato (EKA) programos ir vartotojo kalbos parametrai
description: Šiame straipsnyje aprašoma, kaip pakeisti "Modern POS" (MPOS) ir "Cloud POS" kalbos parametrus.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.industry: Retail
ms.search.form: HcmWorker, RetailStoreTable
ms.openlocfilehash: 663e9a3558bd4d0556644fe5ad6f7f832a18ded5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288385"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Elektroninio kasos aparato (EKA) programos ir vartotojo kalbos parametrai

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip pakeisti "Modern POS" (MPOS) ir "Cloud POS" kalbos parametrus.

## <a name="overview"></a>Peržiūrėti
„Modern POS“ (MPOS) ir „Cloud POS“ palaiko aplinkas, kuriose kalbos parametrai ir vertimai gali skirtis priklausomai nuo parduotuvės ir vartotojo nustatymų. Pavyzdžiui, parduotuvė gali būti regione, kuriame klientai dažniausiai vartoja anglų kalbą, bet kai kurie darbuotojai labiau norėtų naudoti programą, kuri išversta į prancūzų kalbą.

## <a name="data-language"></a>Duomenų kalba

Nepriklausomai nuo to, kokie yra vartotojo parametrai, nusprendžiant, kokius naudoti duomenų vertimus, MPOS ir „Cloud POS“ visada naudojami parduotuvės kalbos parametrai. Taip užtikrinama, kad visų vartotojų ir klientų patirtis būtų nuosekli. Duomenų pavyzdžiai:

- Produktai
- Atributai ir reikšmės
- Kategorijų pavadinimai
- Išspausdinti arba el. paštu išsiųsti operacijų kvitai
- Mokėjimo būdo pavadinimai
- Eilutės rodymo pranešimai

Parduotuvės kalba taip pat naudojama pagrindiniame EKA prisijungimo ekrane, nes kol neprisijungiama, vartotojas nežinomas. Jei parduotuvės kalba vertimo nėra, EKA iš naujo nustatys įmonės kalbą.

### <a name="configuring-the-stores-language-setting"></a>Parduotuvės kalbos parametro konfigūravimas

Parduotuvės kalbos parametras nustatomas puslapyje **Parduotuvė**, skyriuje **Visos parduotuvės**, **Bendra &gt; Regiono parametrai &gt; Kalba**. Norėdami pasirinkti kiekvienos parduotuvės kalbą, naudokite išplečiamąjį sąrašą.

## <a name="user-interface-language"></a>Vartotojo sąsajos kalba

Pagal EKA vartotojo kalbos parametrą nustatomi programos vartotojo sąsajoje naudojami vertimai. Vertimai naudojami visose etiketėse, meniu ir sąrašuose, kurie nelaikomi duomenimis. Viena išimtis yra EKA mygtukynuose rodomas tekstas. Mygtukynuose vertimai nepalaikomi, todėl tekstas juose visada rodomas taip, kaip nurodyta ant mygtuko. Norint, kad būtų palaikomi išversti mygtukai, reikia nukopijuoti ir išlaikyti atskirus mygtukynus ir priskirti juos atitinkamiems vartotojams.

### <a name="configuring-the-users-language-setting"></a>Vartotojo kalbos parametro konfigūravimas

EKA vartotojo kalbos parametras nustatomas puslapyje **Darbininkas**, skyriuje **Visi darbininkai**, **„Retail and Commerce“ &gt; Kalba**. Jis nenustatomas pagrindiniame profilio skirtuke. EKA šio parametro nenaudoja. Jei nenustatyta vartotojo kalba arba nustatyta kalba, kurios vertimų nėra, EKA iš naujo nustatys parduotuvės kalbą.

| &nbsp;      | Vartotojo sąsajos kalba                | Duomenų kalba (produktų, gavimo kvitų formatų, eilutės rodymo ir kt.) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Įmonė** | Numatytoji                    | Numatytoji                                                       |
| **Parduotuvė**   | Perrašoma įmonė          | Perrašoma įmonė                                             |
| **Vartotojas**    | Perrašoma parduotuvė arba įmonė | Niekada                                                         |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
