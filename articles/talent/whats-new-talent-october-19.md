---
title: "Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. spalio 16 d.)"
description: "Šioje temoje aprašomos naujos ir pakeistos šio „Microsoft Dynamics 365 for Talent“ „Core HR“ funkcijos."
author: Darinkramer
manager: AnnBe
ms.date: 10/22/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-22
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 2eb46f436305a4c81ea99553e4dc07288ee74008
ms.openlocfilehash: 7da597a682006cddb44ff9354813b07c15c1a449
ms.contentlocale: lt-lt
ms.lasthandoff: 10/22/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-19-2018"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent Core HR“ (2018 m. spalio 19 d.)

[!include[banner](includes/banner.md)]

**8.1.1067 versija**

Šioje temoje aprašomos naujos ir pakeistos „Core HR“ funkcijos.

## <a name="allow-managers-to-update-time-off-requests"></a>Leisti vadovams atnaujinti prašymus išleisti iš darbo

Darbo eigoje patvirtinus darbuotų prašymus išleisti iš darbo, juos gali reikėti atnaujinti. Daugeliu atvejų šiuos atnaujinimus darbuotojo vardu atlieka vadovas. Ši nauja funkcija suteikia vadovams galimybę darbuotojų vardu atnaujinti ne darbo laiką arba atšaukti prašymus išleisti iš darbo. Ši galimybė kontroliuojama parametru **Darbas kito asmens vardu**, kurį galima nustatyti puslapyje **Personalo parametrai**. 
 
## <a name="allow-hr-to-update-time-off-requests"></a>Leisti personalo skyriui atnaujinti prašymus išleisti iš darbo

Panašiai kaip ir naudojant anksčiau minėtą funkciją, darbo eigoje patvirtinus darbuotojų prašymus išleisti iš darbo, juos gali reikėti atnaujinti personalo skyriaus darbuotojui. Ši funkcija suteikia galimybę personalo skyriaus vartotojams atnaujinti prašymus išleisti iš darbo. Šią galimybę galima įjungti darbo srityje **Žmonės** ir puslapyje **Darbininkas** naudojantis nauja parinktimi **Rodyti ne darbo laiką**. Šiuose puslapiuose personalo skyriaus vartotojai gali peržiūrėti prašymus ir atnaujinti ne darbo laiko operacijas panašiai, kaip šiuos veiksmus gali atlikti vadovai.

Prieigą prie šios funkcijos kontroliuoja ši saugos pareiga:
- Pareiga: prižiūrėti darbininkų atostogų ir neatvykimų procesus
- Teisė: tvarkyti visų darbininkų atostogų ir leidimo neatvykti prašymus

## <a name="other-changes"></a>Kiti pakeitimai
Šiame leidime atlikti toliau nurodyti naujinimai.
- Pakeisti darbininkų samdymo veiksmai, kad jie daugiau „nebestrigtų“ būsenoje **Darbo eiga baigta**.
- Dabar įdarbinimo įrašą galima sukurti be įdarbinimo pradžios datos.
- Dabar darbuotojų savitarnoje rodomai „Dynamics 365 for Talent“ kursų registravino datai taikomas šios datos laiko juostos poslinkis.
- „Excel“ failų negalima importuoti kelis kartus be klaidų naudojant parinktį **Darbuotojo objektas**.

## <a name="known-issue"></a>Žinoma problema

- **Problema**: įtraukiant naują priedą į darbininko puslapį mygtukai **Naujas** ir **Redaguoti** yra papilkinti. 
- **Problemos sprendimas:** prieš atidarydami priedų puslapį įsitikinkite, kad „FactBoxes“ laukai puslapyje **Darbininkas** yra uždaryti. Jei „FactBoxes“ laukai yra uždaryti, įkeliant puslapį **Darbininkas** priedų mygtukai bus įjungti. (Ši problema bus pašalinta kitame platformos naujinime.)

