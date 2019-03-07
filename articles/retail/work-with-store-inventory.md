---
title: Parduotuvės atsargų valdymas
description: Šioje temoje aprašyti dokumentų, kuriuos galite naudoti atsargoms valdyti, tipai.
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/29/2019
ms.locfileid: "339239"
---
# <a name="store-inventory-management"></a>Parduotuvės atsargų valdymas

[!include [banner](includes/banner.md)]

Šioje temoje aprašyti dokumentų, kuriuos galite naudoti atsargoms valdyti, tipai.

Valdyti savo organizacijos atsargoms galite naudoti tolesnius dokumentų tipus.

Dirbant su atsargų programoje „Dynamics 365 for Retail“ ir naudojant EKA programą, svarbu atminti, kad atsargų dimensijų ir tam tikrų atsargų prekių tipų palaikymas EKA yra ribotas.  

EKA sprendimas nepalaiko tolesnių prekių konfigūracijų.
- KS prekės (išskyrus rinkinio produktus, kurie naudoja keletą KS struktūros komponentų)
- Esamo svorio prekės
- Paketo valdomos prekės

Šiuo metu EKA programa nepalaiko toliau nurodytų dimensijų EKA.
- Paketo sekimo dimensija
- Savininko dimensija

EKA sprendimas ribotai palaiko toliau nurodytas dimensijas. Ribotas palaikymas nurodo, kad EKA gali nustatyti kai kurių iš šių dimensijų numatytąsias reikšmes į atsargų operacijas automatiškai, atsižvelgiant į sandėlio / parduotuvės sąrankos konfigūraciją. EKA dimensijų išsamiai nepalaikys, kaip jos yra palaikomos, jei į ERP neautomatiniu būdu įvedama į pardavimo operacija. 

- Buvimo vieta
- Numerio lentelė (taikoma tik kai parametras **Naudoti sandėlio valdymo procesą** įjungtas prekės ir parduotuvės sandėlyje)
- Serijos Nr.
- Atsargų būsena

> [!NOTE]
> Visos organizacijos turi patikrinti prekių konfigūracijas naudodamos EKA programavimo ar tikrinimo aplinkoje prieš jas diegdamos gamyboje. Tikrinkite prekes atlikdami reguliarias grynųjų pinigų pardavimo operacijas ir kurdami klientų užsakymus (jei taikoma) per EKA su savo prekėmis. Tikrinimas turi apimti išsamaus išrašo registravimo procesus tikrinimo aplinkoje ir patikrinimą, ar nėra problemų.
> Prekių konfigūravimas tokiu būdu, kurio nepalaiko EKA programa, tinkamai nepatikrinus, išrašo registravimo proceso metu gali kilti gamybos problemų ir jas išspręsti gali būti sudėtinga. Partnerio arba kliento programos tinkinimai gali būti taikomi pasirinktinai, kad šie registravimo procesai būtų sėkmingai užbaigti. Jei tinkinimai nėra būtini, organizacijos turi užtikrinti, kad produktų konfigūracijos būtų atliekamos tokiu būdu, kurį palaiko standartinė EKA programa / užsakymo kūrimas / išrašo registravimo procesas.

## <a name="purchase-orders"></a>Pirkimo užsakymai

Pirkimo užsakymai kuriami pagrindiniame biure. Jei mažmeninės prekybos sandėlis įtrauktas į pirkimo užsakymo antraštę, užsakymą parduotuvėje galima gauti naudojant modernų EKA (MPOS) arba debesies EKA, esančius programoje „Microsoft Dynamics 365 for Retail“. Kai parduotuvės pageidauti kiekiai įvedami, juos galima įrašyti vietoje ir papildomai modifikuoti. Taip pat kiekiai gali būti fiksuojami ir siunčiami į pagrindinį biurą. Pagrindiniame biure parduotuvėje gauti kiekiai rodomi programoje „Dynamics 365 for Retail“, pirkimo užsakymo lauke **Dabartinis gavimas**.

## <a name="transfer-orders"></a>Perkėlimo užsakymai

Perkėlimo užsakyme galima nurodyti, kad tam tikra parduotuvė yra vieta, iš kurios gali būti siunčiamos prekės. Šiuo atveju perkėlimo užsakymas parduotuvėje rodomas kaip MPOS arba debesies EKA paėmimo užklausa. Kai pageidauti kiekiai paimami, jie fiksuojami ir siunčiami į pagrindinį biurą. Pagrindiniame biure parduotuvėje paimti kiekiai rodomi programoje „Dynamics 365 for Retail“, perkėlimo užsakymo lauke **Dabartinis siuntimas**. Perkėlimo užsakyme galima nurodyti, kad tam tikra parduotuvė yra vieta, į kurią gali būti siunčiamos prekės. Šiuo atveju perkėlimo užsakymas parduotuvėje rodomas kaip MPOS arba debesies EKA gavimo užklausa. Kai parduotuvės pageidauti kiekiai įvedami, juos galima įrašyti vietoje ir papildomai modifikuoti. Taip pat kiekiai gali būti fiksuojami ir siunčiami į pagrindinį biurą. Pagrindiniame biure parduotuvėje gauti kiekiai rodomi programoje „Dynamics 365 for Retail“, perkėlimo užsakymo lauke **Dabartinis gavimas**.

## <a name="stock-counts"></a>Inventorizacijos

Inventorizacijos gali būti planinės arba neplaninės. Planinės inventorizacijos inicijuojamos pagrindiniame biure, kuris nurodo, kurias prekes reikia skaičiuoti. Pagrindinis biuras sukuria inventorizavimo dokumentą, kurį galima gauti parduotuvėje, kurioje faktinių turimų atsargų kiekiai įvedami į MPOS arba debesies EKA. Neplaninės inventorizacijos inicijuojamos parduotuvėje, o faktinių turimų atsargų kiekiai atnaujinami MPOS arba debesies EKA. Skirtingai nei planinės inventorizacijos, neplaninės inventorizacijos neturi iš anksto apibrėžto prekių sąrašo. Alikus bet kurio tipo inventorizaciją, ji fiksuojama ir siunčiama į pagrindinį biurą. Pagrindiniame biure inventorizacija patikrinama ir registruojama.

## <a name="inventory-lookup"></a>Atsargų peržvalga

Dabar keliose parduotuvėse ir sandėliuose turimą produktų kiekį galima peržiūrėti atsargų peržvalgos puslapyje. Neskaitant dabartinio turimo kiekio, galima pamatyti kiekvienos atskiros parduotuvės būsimus prieinamų atsargų (ATP) kiekius. Norėdami tai padaryti pasirinkite parduotuvę, kurios ATP norite peržiūrėti, ir tada spustelėkite **Rodyti parduotuvės pasiekiamumą**.
