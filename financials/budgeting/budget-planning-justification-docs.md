---
title: "Biudžeto planavimo pagrindimo dokumentai"
description: "Pagrindimo dokumentuose pateikiama pasakojimas tiems, kurie prašo paaiškinti, kodėl būtina konkreti sąmata biudžeto."
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

Pagrindimo dokumentuose pateikiama pasakojimas tiems, kurie prašo paaiškinti, kodėl būtina konkreti sąmata biudžeto. 

Biudžeto plano šablonas sukuriamas biudžeto valdytojo programoje "Microsoft Word" ir priskirti dabartinio biudžeto planavimo procesą. Biudžeto savininkai gali tada atidarykite šabloną ir turite duomenis programoje "Word" automatiškai apgyvendintos remiantis jų biudžeto prašymą. Jie tada gali įtraukti papildomą tekstą arba duomenis prieš įrašant ir pritvirtinti savo asmeninį Lygiavimo dokumentas savo biudžeto planą.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Nustatyti Microsoft Dynamics Office papildinys – Microsoft Word

1.  Atidarykite naują Microsoft Word dokumentą.
2.  Spustelėkite **įterpti** ant juostelės, ir spustelėkite **parduotuvė**.
3.  Microsoft Dynamics Office papildinys ieškoti ir spustelėkite **pridėti**.
4.  Žodžiu, dešiniojoje srityje spustelėkite **įtraukti serverio informacija**.
5.  Įveskite arba įklijuokite serverio URL ir spustelėkite **gerai**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Apibrėžti pagrindimas šabloną programoje "Microsoft Word"

1.  Spustelėkite **dizaino** Microsoft Dynamics Office Add-in po to, kai prisijungsite.
2.  Antraštės informaciją, naudokite su **įtraukti laukus** mygtuką.
3.  Pasirinkite BudgetPlanJustification subjekto duomenų šaltinį, ir spustelėkite **kitas**. **Pastaba:** šiam subjektui nereikia jokių pagrindimo dokumentą. Kiti asmenys gali būti naudojamas bet įkelti atgal į Microsoft Dynamics 365 operacijų nepavyksta, jei šis subjektas nėra įtrauktas.
4.  Pridėti BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ir DocumentNumber etiketės ir vertybes į Word dokumentą. **Pastaba:** galite naudoti pasirinktines etiketes, o ne standartines žymes, kurias, jei reikia.
5.  Spustelėkite **padaryti** užbaigti antraštės sekcijos.
6.  Eilutės lygio detalės biudžeto planą sumų, spustelėkite **pridėti lentelę**.
7.  Dar kartą, pasirinkite BudgetPlanJustification subjekto duomenų šaltinį, ir spustelėkite **kitas**.
8.  Pridėti laukus, EffectiveDate, ScenarioName, AccountDisplayValue ir AccountingCurrencyExpenseAmount. **Pastaba:** jei komentarai yra įtraukti per atskiras biudžeto eilutes, tas gali būti įtraukti į lentelę čia.
9.  Pridėti jokių papildomų nurodymų pateikti galutiniam vartotojui, ir atlikti visus būtinus formatavimo ar stilius į dokumentą.
10. Įrašyti dokumentą į vietinį kompiuterį, ir uždarykite failą, prieš tęsdami.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Nustatyti biudžeto planavimo procesą naudoti pagrindimas šablonas

1.  Microsoft Dynamics 365 operacijoms, eikite į **sudaromo biudžeto**&gt;**nustatymo**&gt;**biudžeto planavimas**&gt;**pagrindimo dokumentų šablonus**.
2.  Spustelėkite **naujas** ir suraskite jūsų naujai sukurtą programos Microsoft Word dokumente.
3.  Įveskite šabloną rodomas pavadinimas ir aprašymas. Click **OK**.
4.  Eikite į **sudaromo biudžeto**&gt;**nustatymo**&gt;**biudžeto****planavimo**&gt;**biudžeto planavimo proceso**.
5.  Pasirinkite procesas kur pagrindimas šabloną galima vartoti, ir spustelėkite **redaguoti**.
6.  – Į **pagrindimo dokumento šabloną** srityje, pasirinkite tinkamą šabloną ir išsaugokite.

##### <a name="edit-and-save-personalized-justification-documents"></a>Redaguoti ir įrašyti asmeninį pagrindimo dokumentai

1.  Dynamics 365 operacijoms, sukurti naują biudžeto planą arba atidarykite esamą biudžeto planą.
2.  – Į **pagrindimas** išskleidžiamajame meniu pasirinkite **sukurti naują pagrindimas**.
3.  Užpildę duomenis, pasirinkite nusiųsti asmeninį dokumentą iš į **pagrindo** išskleidžiamajame meniu.



