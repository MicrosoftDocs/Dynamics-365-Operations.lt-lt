---
title: Išlaidų darbo eiga
description: Šioje temoje paaiškinama, kaip, naudojant „Microsoft Dynamics 365 Finance“ darbo eigų sistemą, modulyje Išlaidų valdymas galima nustatyti išlaidų ataskaitų peržiūros procesą.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c52915860709e38013ec06204c52bb06de417eb1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187595"
---
# <a name="expense-workflow"></a>Išlaidų darbo eiga

[!include [banner](../includes/banner.md)]

Naudodami darbo eigų sistemą, modulyje Išlaidų valdymas galite nustatyti išlaidų ataskaitų peržiūros procesą. Nustatę darbo eigą, naudojančią tolesnius kriterijus, galite nustatyti, kas tvirtina išlaidų ataskaitas.

- Darbuotojų ataskaitų hierarchija ir iš anksto nustatyti tvirtinimo limitai
- Kelių lygių tvirtinimo funkcija, palaikanti laikinus tvirtintojus ir galutinį tvirtintoją
- Finansinės dimensijos ir projekto atsakomybė
- Priskyrimas konkretiems vartotojams ar vartotojų grupėms

Galima kurti išlaidų ataskaitų, kelionių paraiškų, avansų grynaisiais pinigais ir pridėtinės vertės mokesčio (PVM) susigrąžinimo darbo eigų tvirtinimus.

**Pavyzdys:**

Toliau pateiktas procesas yra išlaidų ataskaitos išlaidų valdymo darbo eigos pavyzdys.

1. Darbuotojas sukuria ir įrašo išlaidų ataskaitą.
2. Darbuotojas išlaidų ataskaitą pateikia tvirtinti. Tvirtintojas identifikuojamas pagal taisykles, apibrėžtas nustatant darbo eigą.
3. Tvirtintojas gauna pranešimą, kad išlaidų ataskaita paruošta tvirtinti. Tvirtintojas peržiūri išlaidų ataskaitą ir patikrina, ar tenkinamos tolesnės sąlygos.

    - Išlaidos nepažeidžia jokių išlaidų strategijų. Jei išlaidos pažeidžia strategiją, tvirtintojas patikrina, ar į išlaidų ataskaitą įtrauktas tinkamas verslo pagrindimas.
    - Prie išlaidų ataskaitos pridėti elektroniniai kvitai.

4. Tvirtintojas patvirtina išlaidų ataskaitą.
5. Išlaidų ataskaita priskiriama modulio Mokėtinos sumos koordinatoriui užregistruoti.
6. Atsižvelgiant į tai, ar sukonfigūruota automatinio registravimo funkcija, vykdomas vienas iš tolesnių veiksmų.

    - Jei automatinio registravimo funkcija sukonfigūruota, išlaidų ataskaita apdorojama mokėjimui atlikti, o išlaidų ataskaitos būsena atnaujinama.
    - Jei automatinio registravimo funkcija nesukonfigūruota, modulio Mokėtinos sumos koordinatorius patikrina, ar pateikti visi pradiniai kvitai ir ar jie sutampa su išlaidų ataskaitoje nurodytomis išlaidomis. Taip pat reikia patikrinti, ar teisingi visi išlaidų ataskaitoje įvesti mokesčių kodai.

Patikrinus visus šiuos reikalavimus, išlaidų ataskaita registruojama.

Užregistravus išlaidų ataskaitą, autorizuojamas mokėjimas už išlaidų ataskaitos išlaidas ir darbuotojui išmokama kompensacija.
