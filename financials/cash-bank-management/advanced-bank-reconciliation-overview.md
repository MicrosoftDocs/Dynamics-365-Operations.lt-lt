---
title: "Išplėstinio banko suderinimo apžvalga"
description: "Šiame straipsnyje aprašytas pažangus banko suderinimo proceso srautas. Pažangaus banko suderinimo funkcija leidžia importuoti banko išrašus, kuriuos galima automatiškai suderinti iš banko operacijas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 00f022da597b1de2454e93123de31731c6a65962
ms.openlocfilehash: 20363ef1917f7d0796cb0d5cd8e623c598b5ee01
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Išplėstinio banko suderinimo apžvalga

[!include[banner](../includes/banner.md)]


Šiame straipsnyje aprašytas pažangus banko suderinimo proceso srautas. Pažangaus banko suderinimo funkcija leidžia importuoti banko išrašus, kuriuos galima automatiškai suderinti iš banko operacijas.

Naudodamiesi išplėstinio banko suderinimo funkcija galite importuoti banko išrašus. Importuotą banko išrašą galima automatiškai suderinti banko operacijose. Toliau pateikiami išplėstinio banko suderinimo eigos veiksmai.

1.  Nustatykite banko išrašo importavimą.
    -   Importuokite banko išrašus naudodami duomenų objekto sistemą.
    -   Paprastai yra įtaisyti trys banko išrašų formatai: ISO20022, BAI2 ir MT940.
    -   Funkcijas galima išplėsti į bet kokį formatą.

2.  Nustatykite numeraciją, kuri bus naudojama išplėstiniam banko suderinimui ir nurodykite banko suderinimo gretinimo taisykles.
    -   Derinimo gretinimo taisyklė – tai kriterijų rinkinys, naudojamas vykdant derinimo procesą, norint filtruoti banko išrašo eilutes ir „Microsoft Dynamics 365 for Operations“ banko operacijos eilutes. Priklausomai nuo jūsų verslo praktikos, norėdami automatizuoti ir optimizuoti derinimo procesą, galite nustatyti daugiau nei vieną gretinimo taisyklę.

3.  Suderinkite banko išrašus su „Dynamics 365 for Operations“ banko operacijomis.
    -   Atlikite automatinį gretinimą ir sukurkite derinimo žurnalus.
    -   Peržiūrėkite banko išrašus ir „Dynamics 365 for Operations“ banko operacijas vieną šalia kito.
    -   Automatiškai registruokite „Dynamics 365 for Operations“ banko operacijas, jei jos rodomos banko išraše, bet nebus rodomos „Dynamics 365 for Operations“.
    -   Sugeneruokite derinimo išrašą.






