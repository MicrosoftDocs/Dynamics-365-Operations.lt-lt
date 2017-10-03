---
title: "Išplėstinio banko suderinimo apžvalga"
description: "Šiame straipsnyje aprašytas pažangus banko suderinimo proceso srautas. Pažangaus banko suderinimo funkcija leidžia importuoti banko išrašus, kuriuos galima automatiškai suderinti iš banko operacijas."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 67cd622d7766e5b177ccc58398431b007e8bda4e
ms.contentlocale: lt-lt
ms.lasthandoff: 06/13/2017


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
    -   Derinimo gretinimo taisyklė – tai kriterijų rinkinys, naudojamas vykdant derinimo procesą, norint filtruoti banko išrašo eilutes ir „Microsoft Dynamics 365 for Finance and Operations, Enterprise edition“ banko operacijos eilutes. Priklausomai nuo jūsų verslo praktikos, norėdami automatizuoti ir optimizuoti derinimo procesą, galite nustatyti daugiau nei vieną gretinimo taisyklę.

3.  Suderinkite banko išrašus su „Finance and Operations“ banko operacijomis.
    -   Atlikite automatinį gretinimą ir sukurkite derinimo žurnalus.
    -   Peržiūrėkite banko išrašus ir „Finance and Operations“ banko operacijas vieną šalia kito.
    -   Automatiškai registruokite „Finance and Operations“ banko operacijas, jei jos rodomos banko išraše, bet nebus rodomos „Finance and Operations“.
    -   Sugeneruokite derinimo išrašą.






