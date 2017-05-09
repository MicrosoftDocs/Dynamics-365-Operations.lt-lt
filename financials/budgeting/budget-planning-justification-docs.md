---
title: "Biudžeto planavimo pagrindimo dokumentai"
description: "Pagrindimo dokumentai prašantiems biudžeto asmenims suteikia informacijos, padedančios paaiškinti, kodėl konkretus biudžetas yra reikalingas."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Biudžeto planavimo pagrindimo dokumentai

[!include[banner](../includes/banner.md)]


Pagrindimo dokumentai prašantiems biudžeto asmenims suteikia informacijos, padedančios paaiškinti, kodėl konkretus biudžetas yra reikalingas. 

Biudžeto plano šabloną sukuria biudžeto vadovas programoje „Microsoft Word“ ir priskiria dabartiniam biudžeto planavimo procesui. Tada biudžeto savininkai gali atidaryti šabloną ir automatiškai įvesti duomenis į „Word“ dokumentą pagal savo biudžeto užklausą. Tada jie gali įtraukti papildomo teksto arba duomenų, prieš įrašydami ir pridėdami savo pritaikytą pagrindimo dokumentą prie savo biudžeto plano.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>„Microsoft Dynamics Office“ papildinio, skirto „Microsoft Word“, nustatymas

1.  Atidarykite naują „Microsoft Word“ dokumentą.
2.  Juostelėje spustelėkite **Įterpti** ir spustelėkite **Parduotuvė**.
3.  Raskite „Microsoft Dynamics Office“ papildinį ir spustelėkite **Įtraukti**.
4.  Programos „Word“ kairiojoje srityje spustelėkite **Įtraukti serverio informaciją**.
5.  Įveskite arba įklijuokite serverio URL ir spustelėkite **Gerai**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Pagrindimo šablono nurodymas programoje „Microsoft Word“

1.  Kai prisijungsite, „Microsoft Dynamics Office“ papildinyje spustelėkite **Dizainas**.
2.  Norėdami tvarkyti antraštės informaciją, naudokite mygtuką **Įtraukti laukų**.
3.  Pasirinkite BudgetPlanJustification objekto duomenų šaltinį ir spustelėkite **Toliau**. **Pastaba:** šis objektas reikalingas visiems pagrindimo dokumentams. Galima naudoti kitus objektus, bet jei šis objektas nėra įtrauktas, nusiuntimas į „Microsoft Dynamics 365 for Operations“ nepavyks.
4.  Į „Word“ dokumentą įtraukite BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ir DocumentNumber žymas ir reikšmes. **Pastaba:** jei reikia, galite naudoti savo pasirinktines žymas, o ne standartines žymas.
5.  Norėdami baigti tvarkyti antraštės dalį, spustelėkite **Atlikta**.
6.  Norėdami tvarkyti biudžeto plano eilutės lygio informaciją, spustelėkite **Įtraukti lentelę**.
7.  Vėl pasirinkite BudgetPlanJustification objekto duomenų šaltinį ir spustelėkite **Toliau**.
8.  Įtraukite laukus EffectiveDate, ScenarioName, AccountDisplayValue ir AccountingCurrencyExpenseAmount. **Pastaba:** jei komentarus galima įtraukti į atskiras biudžeto plano eilutes, juos galima įtraukti į lentelę čia.
9.  Įtraukite bet kokias papildomas instrukcijas galutiniam vartotojui ir atlikite visus reikalingus dokumento formatavimo arba stiliaus keitimo veiksmus.
10. Prieš tęsdami įrašykite dokumentą į vietinį kompiuterį ir uždarykite failą.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Biudžeto planavimo proceso nustatymas naudoti pagrindimo šabloną

1.  Programoje „Microsoft Dynamics 365 for Operations‟ atidarykite **Biudžeto sudarymas** &gt; **Sąranka** &gt; **Biudžeto planavimas** &gt; **Pagrindimo dokumento šablonai**.
2.  Spustelėkite **Naujas** ir naršydami atidarykite naujai sukurtą „Microsoft Word“ dokumentą.
3.  Įveskite šablono rodomą pavadinimą ir aprašą. Spustelėkite **Gerai**.
4.  Atidarykite **Biudžeto sudarymas** &gt; **Sąranka** &gt; **Biudžeto** **planavimas** &gt; **Biudžeto planavimo procesas**.
5.  Pasirinkite procesą, kuriame bus naudojamas pagrindimo šablonas, ir spustelėkite **Redaguoti**.
6.  Lauke **Pagrindimo dokumento šablonas** pasirinkite reikiamą šabloną ir įrašykite.

##### <a name="edit-and-save-personalized-justification-documents"></a>Pritaikytų pagrindimo dokumentų redagavimas ir įrašymas

1.  Programoje „Dynamics 365 for Operations“ sukurkite naują arba atidarykite esamą biudžeto planą.
2.  Išplečiamajame meniu **Pagrindimas** pasirinkite **Kurti naują pagrindimą**.
3.  Įvedę informaciją pasirinkite įkelti pritaikytą dokumentą iš išplečiamojo meniu **Pagrindimas**.





