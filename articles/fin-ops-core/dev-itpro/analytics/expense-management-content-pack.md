---
title: Išlaidų valdymas – „Power BI“ turinys
description: Šiame straipsnyje aprašoma, kas įtraukta į išlaidų valdymo Power BI turinio paketą.
author: panolte
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 78ae444c1c9803ed3708d71da7a359667df0252f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878319"
---
# <a name="expense-management-power-bi-content"></a>Išlaidų valdymas – „Power BI“ turinys

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kas yra išlaidų valdymo turinyje Power BI. 

## <a name="overview"></a>Apžvalga
Su Išlaidų valdymo versija 8.1 ir naujesne versija galima naudoti du „Power BI“ turinio paketus. 
- Išlaidų ataskaitas teikiantiems darbuotojams skirta asmeninė ataskaitų sritis. 

  Ataskaitų sritis pritaikyta asmenims pateikti pagrindinę informaciją apie nepateiktas ir pateiktas sumas, taip pat istoriją ir įžvalgas apie išlaidų operacijų retrospektyvą. Asmeninė ataskaitų sritis yra vienas puslapis, kuriame nurodoma svarbiausia informacija vartotojui.

- Mokėtinų sumų tarnautojams ir vadovams skirta administratoriaus ataskaitų sritis. Ataskaitų sritis pritaikyta stebėti bendras darbuotojo išlaidas ir rengti ataskaitas. Joje pateikiama pagrindinė išlaidų metrika, pvz., nepateiktos išlaidos, kilometražas ir vidutinės išlaidų ataskaitos sumos. Joje naudojami operaciniai duomenys ir pateikiami sujungti visų įmonių išlaidų valdymo duomenų rodiniai. Joje taip pat nurodymas pasiskirstymas kiekvienam darbuotojui ir galima pasirinkti įtraukti finansinės dimensijos duomenis. Administravimo išlaidų analizės turinys apima tai, kas išvardyta toliau. 
  - Peržiūros puslapis, kuriame pateikiama pagrindinė metrika apie išlaidų sumas ir įžvalgos apie juodraštines, vykstančias ir baigtas išlaidų ataskaitas. 
  - Darbuotojų statistikos puslapis, kuriame galima peržiūrėti asmeninę informaciją apie darbuotoją pagal laiką, išlaidų tipą ir statistikos grupė. 
  - Darbuotojų palyginimo puslapis, kuriame lyginami keli darbuotojai per tam tikrą laiką. 

Visos sumos rodomos įmonės valiuta. Rodomi visų įmonių duomenys, bet prireikus galite naudoti įmonės filtrą. 

## <a name="accessing-the-power-bi-content"></a>Prieiga prie „Power BI“ turinio
Expense Admin Dashboard.pbix ir Expense Personal Dashboard.pbix „Power BI“ turinį galite rasti „Microsoft Dynamics Lifecycle Services“ (LCS) bibliotekoje Bendrai naudojamas turtas. Norėdami gauti daugiau informacijos apie tai, kaip atsisiųsti turinį ir įdiegti jį savo organizacijoje, žr. [„Power BI“ turinys LCS iš „Microsoft“ ir jūsų partnerių](/archive/blogs/dynamicsaxbi/power-bi-content-from-microsoft-and-your-partners).
Turinys pasiekiamas darbo srityje Išlaidų valdymas kaip įdėtasis „Power Bi“ turinys. Bet kuris išlaidų savininkas gali pats surasti asmenines išlaidas, o prieigą prie administravimo duomenų turi ir visų vartotojų išlaidų duomenis peržiūrėti gali tik mokėtinų sumų tarnautojai ir vadovai.

## <a name="refreshing-the-power-bi-content"></a>„Power BI turinio atnaujinimas
Naudojantis „Power BI“ turiniu Išlaidų valdymas, būtina atnaujinti objektų saugyklos priemonę TrvBiExpenseMeasurement ir BudgetActivityMeasure. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Į „Power BI“ turinį įtrauktos metrikos
Į turinį įtrauktas ataskaitų puslapių rinkinys. Kiekvieną puslapį sudaro metrikų, pavaizduotų diagramomis, plytelėmis ir lentelėmis, rinkinys. Toliau pateiktoje lentelėje pateikiama „Power BI“ turinio vizualizacijų apžvalga.

**Asmeninių išlaidų analizė**

| Ataskaitų puslapis | Vizualizacija                             |
|-------------|-------------------------------------------|
| Mano išlaidos | Kilometražo suma                         |
|             | Proceso išlaidų ataskaitose                |
|             | Nr. nepateiktų išlaidų               |
|             | Mokėtinos asmeninės išlaidos              |
|             | Nepateikta suma                        |
|             | Pateikta suma                          |
|             | Kompensuotina suma             |
|             | Išlaidų ataskaitos, kuriose nurodytos sumos ir būsena   |
|             | Pateiktos, bet nepatvirtintos išlaidų ataskaitos.  |
|             | Išlaidos pagal savikainos tipą                     |
|             | Išlaidos pagal prekybininką                      |
|             | Išlaidos pagal apdorotas išlaidas            |
|             | Išlaidos pagal projektą                       |
|             | Bendra operacijos suma per tam tikrą laiką        |

**Administravimo išlaidų analizė**

| Ataskaitų puslapis         | Vizualizacija                           |           
|---------------------|-----------------------------------------|
| Išlaidų apžvalga    | Juodraštinė išlaidų suma                   |
|                     | Juodraštinių išlaidų eilučių skaičius           |
|                     | Juodraštinių išlaidų eilutės                     |
|                     | Išlaidų ataskaitos strategijos pažeidimai        |
|                     | Neapmokėta suma                      |
|                     | Pateiktos, bet nepatvirtintos išlaidos       |
|                     | Patvirtintos išlaidos                       |
|                     | Bendroji išlaidų suma                    |
|                     | Išlaidų ataskaitų suvestinės                |
|                     | Išlaidos pagal savikainos tipą                   |
|                     | Išlaidos pagal prekybininką                    |
|                     | Išlaidos pagal darbuotojus                   |
|                     | Išlaidos lyginant su projektu                     |
| Darbuotojų palyginimas | Išlaidų sumos                         |
|                     | Išlaidų sumos per tam tikrą laiką pagal darbuotoją   |
| Darbuotojo statistika | Išlaidų ataskaitos pagal savikainos tipą            |
|                     | Asmeninės išlaidos                       |
|                     | Išlaidų ataskaitos pagal statistikos grupę     |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]