---
title: Išplėstinio banko suderinimo apžvalga
description: Šiame straipsnyje aprašytas pažangus banko suderinimo proceso srautas. Pažangaus banko suderinimo funkcija leidžia importuoti banko išrašus, kuriuos galima automatiškai suderinti iš banko operacijas.
author: panolte
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ebddf6c77df227f896e6f275f741ea69fb68474
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983597"
---
# <a name="advanced-bank-reconciliation-overview"></a>Išplėstinio banko suderinimo apžvalga

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašytas pažangus banko suderinimo proceso srautas. Pažangaus banko suderinimo funkcija leidžia importuoti banko išrašus, kuriuos galima automatiškai suderinti iš banko operacijas.

Naudodamiesi išplėstinio banko suderinimo funkcija galite importuoti banko išrašus. Importuotą banko išrašą galima automatiškai suderinti banko operacijose. Toliau pateikiami išplėstinio banko suderinimo eigos veiksmai.

1.  Nustatykite banko išrašo importavimą.
    -   Importuokite banko išrašus naudodami duomenų objekto sistemą.
    -   Paprastai yra įtaisyti trys banko išrašų formatai: ISO20022, BAI2 ir MT940.
    -   Funkcijas galima išplėsti į bet kokį formatą.

2.  Nustatykite numeraciją, kuri bus naudojama išplėstiniam banko suderinimui ir nurodykite banko suderinimo gretinimo taisykles.
    -   Derinimo gretinimo taisyklė – tai kriterijų rinkinys, naudojamas vykdant derinimo procesą, norint filtruoti banko išrašo eilutes ir „Microsoft Dynamics 365 Finance“ banko operacijos eilutes. Priklausomai nuo jūsų verslo praktikos, norėdami automatizuoti ir optimizuoti derinimo procesą, galite nustatyti daugiau nei vieną gretinimo taisyklę.

3.  Suderinkite banko išrašus su „Finance“ banko operacijomis.
    -   Atlikite automatinį gretinimą ir sukurkite derinimo žurnalus.
    -   Peržiūrėkite banko išrašus ir „Finance“ banko operacijas vieną šalia kito.
    -   Automatiškai registruokite „Finance“ banko operacijas, jei jos rodomos banko išraše, bet nebus rodomos „Finance“ programoje.
    -   Sugeneruokite derinimo išrašą.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]