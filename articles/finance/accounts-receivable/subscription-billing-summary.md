---
title: Prenumeratų sąskaitų valdymo apžvalga
description: Šioje temoje aprašomas prenumeratos atsiskaitymas " Microsoft Dynamics 365 Finance".
author: JodiChristiansen
ms.date: 04/13/2022
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
ms.openlocfilehash: 9d46492cca3cc435048fa497f6b1f3a28b77140a
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644533"
---
# <a name="subscription-billing-overview"></a>Prenumeratų sąskaitų valdymo apžvalga

[!include [banner](../includes/banner.md)]

Prenumeratos atsiskaitymas leidžia organizacijoms valdyti prenumeratos pajamų galimybes ir periodinį atsiskaitymą per atsiskaitymo grafikus. Sudėtingi kainodaros ir atsiskaitymo modeliai bei pajamų paskirstymas yra lengvai valdomi ir apmokestinami bei pripažįstami eilutės lygiu. Kelių elementų pajamų paskirstymas leidžia paskirstyti pajamas, kad jos atitiktų tarptautinius apskaitos standartus (15-asis \[tarptautinis finansinės atskaitomybės standartas 15 TFAS 15\]) ir visuotinai pripažintus apskaitos principų (JAV BAP) standartus (Apskaitos standartų kodifikavimo tema 606 \[ASC 606\]).

Sprendimas turi tris modulius, kuriuos galima naudoti savarankiškai. Arba visi trys moduliai gali būti naudojami kartu.

- **Pasikartojantis sutarties atsiskaitymas** – šis modulis leidžia pasikartojančiam atsiskaitymui ir kainų valdymui kontroliuoti kainodaros ir atsiskaitymo parametrus, atnaujinti sutartį ir konsoliduotą SF išrašymą.
- **Pajamų ir išlaidų atidėjimai** - Šis modulis pašalina rankinius procesus ir priklausomybę nuo išorinių sistemų, valdydamas pajamas ir įgalindamas realaus laiko įžvalgas apie mėnesines pasikartojančias pajamas.
- **Kelių elementų pajamų paskirstymas** – šis modulis padeda laikytis pajamų tvarkant kainodarą ir pajamų paskirstymą keliems elementams.

Daugiau informacijos apie prenumeratos atsiskaitymą ieškokite [Subscription billing Power BI content](sub-bill-power-bi.md).

Prenumeratos atsiskaitymas įgalintas valdant **funkcijas**. Tačiau jo negalima naudoti su pajamų atpažinimo **funkcija**. Todėl prieš įgalindami prenumeratos atsiskaitymą turite išjungti šią funkciją.

1. **Darbo srities Funkcijų valdymas** skirtuke **Visi** filtre įveskite **Įplaukų atpažinimas**, tada kaip filtrą pasirinkite funkcijos pavadinimą.
2. Pasirinkite įplaukų **atpažinimo** funkciją, tada pasirinkite **Išjungti**.
3. Dalyje **Funkcijų pavadinimo** filtras įveskite **Prenumeratos atsiskaitymas**, tada pasirinkite modulio filtrą.
4. **Pasirinkite prenumeratos atsiskaitymo** funkciją, tada pasirinkite **Įgalinti**.
5. Pasirinkite vieną iš trijų modulių iš ankstesnio sąrašo, tada pasirinkite **Įgalinti**. Pakartokite šį veiksmą kiekvienam iš kitų dviejų modulių.

    > [!IMPORTANT]
    > Prenumeratos **atsiskaitymo funkcija turi būti įjungta prieš įgalinant** bet kurį iš trijų modulių.
