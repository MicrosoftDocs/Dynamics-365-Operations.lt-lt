---
title: Abonemento sąskaitų pateikimo peržiūra
description: Šioje temoje aprašomos abonemento sąskaitos iš "Microsoft"Dynamics 365 Finance.
author: JodiChristiansen
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-02-09
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: b94ac36e49d55ad42909877d77903cd40cb22cbe
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182714"
---
# <a name="subscription-billing-overview"></a>Abonemento sąskaitų pateikimo peržiūra

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Abonemento sąskaitų išrašymas leidžia organizacijoms valdyti abonemento įplaukų galimybes ir periodinius sąskaitų pateikimo grafikus. Sudėtingas įkainojimo ir atsiskaitymo modelis bei įplaukų paskirstymas yra lengvai valdomi ir išrašomos bei atpažįstamos eilutės lygiu. Kelių elementų įplaukų paskirstymas įgalina įplaukų paskirstymą siekiant laikytis Tarptautinių apskaitos standartų (Tarptautinis 15 IFRS 15 \[\] standartas) ir bendrai priimtų apskaitos principų (JAV GAAP) standartų (Apskaitos standartų kodifikavimo tema 606 \[ASC 606\]).

Sprendimas turi tris modulius, kuriuos galima naudoti atskirai. Taip pat kartu galima naudoti visus tris modulius.

- **Pasikartojantis sutarties atsiskaitymas** – šis modulis įgalina periodinį atsiskaitymą ir kainos valdymą, siekiant užtikrinti kainodaros ir atsiskaitymo parametrų valdymą, sutarties atnaujinimą ir konsoliduotą SF išrašymą.
- **Įplaukų ir išlaidų atidėjimai – šis modulis pašalina rankinius** procesus ir priklausomybę nuo išorinių sistemų valdydami įplaukas ir įgalindami realiuoju laiku informacijos apie pasikartojančias mėnesio įplaukas.
- **Kelių elementų įplaukų paskirstymas** – šis modulis padeda užtikrinti įplaukų atitikimą tvarkant kelių prekių kainodarą ir įplaukų paskirstymą.

Abonemento sąskaitos išrašymas įgalintas naudojant **funkcijų valdymą**. Tačiau jo negalima naudoti su įplaukų pripažinimo **funkcija**. Todėl prieš įjungdami abonemento sąskaitų apmokėjimą turite išjungti šią funkciją.

1. Funkcijų valdymo **darbo srityje**, skirtuke **Viskas**, **filtre** įveskite Įplaukų atpažinimą, tada kaip filtrą pasirinkite priemonės pavadinimą.
2. Pasirinkite įplaukų **atpažinimo** funkciją, tada pasirinkite **Išjungti**.
3. Funkcijų **vardų** filtre įveskite **Abonemento atsiskaitymas**, tada pasirinkite modulio filtrą.
4. Pasirinkite Abonemento **atsiskaitymo funkciją**, tada pasirinkite **Įgalinti**.
5. Iš ankstesnio sąrašo pasirinkite vieną iš trijų modulių, tada pasirinkite **Įgalinti**. Pakartokite šį žingsnį su kiekvienu iš kitų dviejų modulių.

    > [!IMPORTANT]
    > Kad **būtų galima įgalinti** bet kurį iš trijų modulių, pirmiausia reikia įgalinti abonemento atsiskaitymo funkciją.
