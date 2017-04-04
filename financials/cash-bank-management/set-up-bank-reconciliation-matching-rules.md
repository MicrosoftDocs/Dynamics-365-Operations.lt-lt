---
title: "Banko derinimo gretinimo taisyklių nustatymas"
description: "Šiame straipsnyje paaiškinta, kaip nustatyti derinimo gretinimo taisykles ir derinimo gretinimo taisyklių rinkinius, kad būtų lengviau atlikti banko derinimo procesą. Derinimo gretinimo taisyklės – tai rinkinys kriterijų, naudojamų filtruojant banko išrašo eilutes ir banko dokumento eilutes, kai vykdomas derinimo procesas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: e4c07a6afb90535c57f372d5b850919b5b34aaa4
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Banko derinimo gretinimo taisyklių nustatymas

Šiame straipsnyje paaiškinta, kaip nustatyti derinimo gretinimo taisykles ir derinimo gretinimo taisyklių rinkinius, kad būtų lengviau atlikti banko derinimo procesą. Derinimo gretinimo taisyklės – tai rinkinys kriterijų, naudojamų filtruojant banko išrašo eilutes ir banko dokumento eilutes, kai vykdomas derinimo procesas.

Galite nustatyti derinimo gretinimo taisykles ir derinimo gretinimo taisyklių rinkinius, kad būtų lengviau atlikti banko derinimo procesą. Susitaikymo atitikimo taisyklė yra kriterijus, kurie yra naudojami filtruoti banko ataskaitos eilutes ir Microsoft Dynamics 365 operacijas banko operacijos eilutes susitaikymo proceso metu. Norėdami nustatyti derinimo gretinimo taisykles, naudokite puslapį **Derinimo gretinimo taisyklės**. Galite nustatyti daugiau nei vieną gretinimo taisyklę ir pyslapyje **Derinimo gretinimo taisyklių rinkiniai** sukurti derinimo gretinimo taisyklių rinkinį. 

> [!NOTE] 
> Banko susitaikymo atitikimo taisyklės naudojamos, jei galite suderinti elektroninių Banko išrašas naudojant iš anksto banko sąskaitų derinimo. 

Puslapyje **Derinimo gretinimo taisyklės** galite pasirinkti, kokie veiksmai ir pasirinkimo kriterijai naudojami vykdant gretinimo taisyklę. – Į **veiklos** laukų grupėje, pasirinkite veiksmą, kuris bus atliekamas, kai atitikimo taisyklės yra susitaikymo proceso metu.  

> [!NOTE] 
> Pasirinkite variantą duomenų laukus, kurie atrodo.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Veiksmas**                         |                                                                                                                                                                                                                                                                                                               | **Pasirinkus veiksmą galimi pasirinkimo kriterijai**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Sugretinti su banko dokumentu **       | Kurdami kriterijus nurodykite, kaip bus gretinami banko dokumentai ir banko išrašo eilutės, kai vykdoma puslapio **Banko suderinimo darbalapis** gretinimo taisyklė. Operacijų eilutės atrenkamos pagal papildomus „FastTab“ skirtukuose nustatytus kriterijus.                                | **1 veiksmas: Nustatyti atitikimo taisyklės** – pasirinkite kriterijus nurodyti banko teiginius sutapdinamas su Dynamics 365 operacijas banko operacijų. **2 veiksmas (pasirinktinai): pasirinkite išrašo eilutes, pagal kurias turi būti vykdomos gretinimo taisyklės:** pritaikykite filtrą, nurodantį, pagal kurią išrašo eilutę vykdyti taisykles.                                                                                                                                                                                                                                                                                                               |
| **Išvalyti atšaukimo išrašo eilutes ** | Kurdami kriterijus nurodykite, kaip bus gretinami banko dokumentai ir banko išrašo eilutės, kai vykdoma puslapio **Banko suderinimo darbalapis** gretinimo taisyklė. Ši parinktis naudojama, kai dėl banko klaidos importuotame banko išraše yra dvi banko išrašo eilutės, kurias reikia derinti. | **1 veiksmas**:** rasti atšaukimo išrašo eilutes **– įtraukite pasirinkimo kriterijų, pagal kuriuos pasirenkamos atšaukimo banko išrašo eilutės. Pavyzdžiui, norėdami pasirinkti tik čekius, lauke Laukas pasirinkite **Banko operacijos kodas**, lauke **Operatorius** pasirinkite pliuso ženklą (+) ir lauke Reikšmė įveskite **Čekiai**. **2 veiksmas: rasti pirminio išrašo eilutes** – galite pridėti pasirinkimo kriterijų, pagal kuriuos banko dokumento eilutės bus gretinamos su banko išrašo eilutėmis. ** 3 veiksmas: Rasti Dynamics 365 operacijas banko operacijų ** – galite pridėti atrankos kriterijus suderinti Dynamics 365 operacijas banko operacijų banko ataskaitos eilutes. |
| **Mark new transactions**          | Kurdami kriterijus nurodykite, kaip puslapyje **Banko suderinimo darbalapis** turėtų būti pažymėtos naujos operacijos, kai vykdoma gretinimo taisyklė.                                                                                                                                                                 | **1 veiksmas: rasti išrašo eilutes **– įtraukite pasirinkimo laukų, kurie nurodytų, kurios puslapio **Banko suderinimo darbalapis** banko išrašo eilutės turėtų būti pasirinktos. ** 2 žingsnis: Rasti Dynamics 365 operacijas banko operacijų ** – galite pridėti atrankos kriterijus ieškoti banko dokumento eilutes. Jei nerandamas joks banko dokumentas, išrašo eilutė bus pažymėta kaip nauja operacija.                                                                                                                                                                                                                                             |

 





