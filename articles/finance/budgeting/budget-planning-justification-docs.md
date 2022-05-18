---
title: Biudžeto planavimo pagrindimo dokumentai
description: Pagrindimo dokumentai prašantiems biudžeto asmenims suteikia informacijos, padedančios paaiškinti, kodėl konkretus biudžetas yra reikalingas.
author: panolte
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: kfend
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 03780b36cb3a6a609350c61792f0c98f2c08244d
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711777"
---
# <a name="budget-planning-justification-documents"></a>Biudžeto planavimo pagrindimo dokumentai

[!include [banner](../includes/banner.md)]

Pagrindimo dokumentai prašantiems biudžeto asmenims suteikia informacijos, padedančios paaiškinti, kodėl konkretus biudžetas yra reikalingas. 

Biudžeto plano šabloną sukuria biudžeto vadovas programoje „Microsoft Word“ ir priskiria dabartiniam biudžeto planavimo procesui. Tada biudžeto savininkai gali atidaryti šabloną ir automatiškai įvesti duomenis į „Word“ dokumentą pagal savo biudžeto užklausą. Tada jie gali įtraukti papildomo teksto arba duomenų, prieš įrašydami ir pridėdami savo pritaikytą pagrindimo dokumentą prie savo biudžeto plano.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>„Microsoft Microsoft Dynamics“ papildinio, skirto „Microsoft Word“, nustatymas

1.  Atidarykite naują „Microsoft Word“ dokumentą.
2.  Juostelėje spustelėkite **Įterpti** ir spustelėkite **Parduotuvė**.
3.  Raskite „Microsoft Dynamics Office“ papildinį ir spustelėkite **Įtraukti**.
4.  Programos „Word“ kairiojoje srityje spustelėkite **Įtraukti serverio informaciją**.
5.  Įveskite arba įklijuokite serverio URL ir spustelėkite **Gerai**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Pagrindimo šablono nurodymas programoje „Microsoft Word“

1.  Kai prisijungsite, „Microsoft Dynamics Office“ papildinyje spustelėkite **Dizainas**.
2.  Norėdami tvarkyti antraštės informaciją, naudokite mygtuką **Įtraukti laukų**.
3.  Pasirinkite BudgetPlanJustification objekto duomenų šaltinį ir spustelėkite **Toliau**. **Pastaba:** šis objektas reikalingas visiems pagrindimo dokumentams. Galima naudoti kitus objektus, tačiau įkelti atgal į Microsoft Dynamics "365" finansus nepavyks, jei šis objektas nebus įtrauktas.
4.  Į „Word“ dokumentą įtraukite BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ir DocumentNumber žymas ir reikšmes. **Pastaba:** jei reikia, galite naudoti savo pasirinktines žymas, o ne standartines žymas.
5.  Norėdami baigti tvarkyti antraštės dalį, spustelėkite **Atlikta**.
6.  Norėdami tvarkyti biudžeto plano eilutės lygio informaciją, spustelėkite **Įtraukti lentelę**.
7.  Vėl pasirinkite BudgetPlanJustification objekto duomenų šaltinį ir spustelėkite **Toliau**.
8.  Įtraukite laukus EffectiveDate, ScenarioName, AccountDisplayValue ir AccountingCurrencyExpenseAmount. **Pastaba:** jei komentarus galima įtraukti į atskiras biudžeto plano eilutes, juos galima įtraukti į lentelę čia.
9.  Įtraukite bet kokias papildomas instrukcijas galutiniam vartotojui ir atlikite visus reikalingus dokumento formatavimo arba stiliaus keitimo veiksmus.
10. Prieš tęsdami įrašykite dokumentą į vietinį kompiuterį ir uždarykite failą.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Biudžeto planavimo proceso nustatymas naudoti pagrindimo šabloną

1.  Atidarykite **Biudžeto sudarymas** &gt; **Sąranka** &gt; **Biudžeto planavimas** &gt; **Pagrindimo dokumento šablonai**.
2.  Spustelėkite **Naujas** ir naršydami atidarykite naujai sukurtą „Microsoft Word“ dokumentą.
3.  Įveskite šablono rodomą pavadinimą ir aprašą. Spustelėkite **Gerai**.
4.  Atidarykite **Biudžeto sudarymas** &gt; **Sąranka** &gt; **Biudžeto** **planavimas** &gt; **Biudžeto planavimo procesas**.
5.  Pasirinkite procesą, kuriame bus naudojamas pagrindimo šablonas, ir spustelėkite **Redaguoti**.
6.  Lauke **Pagrindimo dokumento šablonas** pasirinkite reikiamą šabloną ir įrašykite.

##### <a name="edit-and-save-personalized-justification-documents"></a>Pritaikytų pagrindimo dokumentų redagavimas ir įrašymas

1.  Sukurkite naują biudžeto planą arba atidarykite esamą biudžeto planą.
2.  Išplečiamajame meniu **Pagrindimas** pasirinkite **Kurti naują pagrindimą**.
3.  Įvedę informaciją pasirinkite įkelti pritaikytą dokumentą iš išplečiamojo meniu **Pagrindimas**.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
