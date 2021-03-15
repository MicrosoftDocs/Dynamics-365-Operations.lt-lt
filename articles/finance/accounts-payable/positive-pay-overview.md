---
title: Teigiamo mokėjimo apžvalga
description: Šiame straipsnyje pateikiama informacija apie teikiamą mokėjimą, kuris naudojamas norint generuoti elektroninį čekių sąrašą, kurį galima teikti bankui.
author: panolte
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: ffb2ded8c6f1e86657f298f3638da39ac4c63b66
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972111"
---
# <a name="positive-pay-overview"></a>Teigiamo mokėjimo apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie teikiamą mokėjimą, kuris naudojamas norint generuoti elektroninį čekių sąrašą, kurį galima teikti bankui. 

Teigiamas mokėjimas naudojamas norint generuoti elektroninį čekių sąrašą, kurį galima teikti bankui. Naudojant teigiamo mokėjimo failus, bankams lengviau išvengti su čekiais susijusio sukčiavimo. Teigiamas mokėjimas nustatomas, kad būtų generuojamas elektroninis čekių sąrašas, kiekvieną kartą spausdinant čekius. Tada, čekį pateikus bankui, bankas jį lygina su jūsų anksčiau pateiktu čekių sąrašu. Jei čekis atitinka sąraše esantįjį, bankas jį patvirtina. Jei čekis sąraše esančio čekio neatitinka, bankas jį pasilieka peržiūrėti.

Teigiamas mokėjimas dar vadinamas „SafePay‟. 

Teigiamo mokėjimo failuose gali būti neskelbtinos informacijos apie mokėjimų gavėjus ir čekių sumas. Todėl būtinai naudokite reikiamas saugos priemones nuo failų sugeneravimo akimirkos iki jų gavimo banke. Teigiamo mokėjimo failai atsisiunčiami pagal žiniatinklio naršyklės atsisiuntimo instrukcijas. 

Teigiamo mokėjimo failai kuriami naudojant duomenų objektus. Prieš generuodami teigiamo mokėjimo failą, turite nustatyti XML transformavimo formatus, kuriais duomenys paverčiami į formatą, kurį gali naudoti bankas. 

Kiekvienai banko sąskaitai, kuriai norite generuoti teigiamo mokėjimo informaciją, turite priskirti teigiamo mokėjimo formatą. Sugeneravę mokėjimus galite generuoti teigiamo mokėjimo failą vienam juridiniam subjektui ir vienai banko sąskaitai. Taip pat tuo pačiu metu teigiamo mokėjimo failus galite generuoti keliems juridiniams subjektams ir banko sąskaitoms. 

Po to, kai teigiamo mokėjimo faile nurodyti čekiai apmokami, iš bango gausite patvirtinimo numerį. Tada teigiamo mokėjimo failą galite patvirtinti sistemoje. 

Jei turite teigiamo mokėjimo failą pakeisti, galite jį atšaukti. Tada iš naujo nustatomas kiekvieno teigiamo mokėjimo failo čekio laukas, kuriame nurodoma, ar tas čekis įtrauktas į teigiamo mokėjimo failą.

Norėdami gauti daugiau informacijos, žr. [Teigiamų mokėjimų failų nustatymas ir generavimas](set-up-generate-positive-pay-files.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]