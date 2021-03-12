---
title: Elektroninio kasos aparato (EKA) programos ir vartotojo kalbos parametrai
description: Šioje temoje aprašoma, kaip pakeisti kalbos parametrus „Modern POS“ (MPOS) ir „Cloud POS“.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0f196b3077b0a8d80cac93a8b6b3f8c5c08c3c96
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000565"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a>Elektroninio kasos aparato (EKA) programos ir vartotojo kalbos parametrai

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip pakeisti kalbos parametrus „Modern POS“ (MPOS) ir „Cloud POS“.

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

|             | Vartotojo sąsajos kalba                   | Duomenų kalba (produktų, gavimo kvitų formatų, eilutės rodymo ir kt.) |
|-------------|----------------------------|---------------------------------------------------------------|
| **Įmonė** | Numatytoji                    | Numatytoji                                                       |
| **Parduotuvė**   | Perrašoma įmonė          | Perrašoma įmonė                                             |
| **Vartotojas**    | Perrašoma parduotuvė arba įmonė | Niekada                                                         |
