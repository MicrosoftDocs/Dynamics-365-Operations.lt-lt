---
title: Lanksčiųjų kreditų programų sąranka
description: Galite naudoti lanksčiųju kreditų programas programoje „Microsoft Dynamics 365 Human Resources”, kad užregistruotumėte darbuotojus išmokoms gauti pagal iš anksto nustatytą lanksčiųjų kreditų skaičių.
author: twheeloc
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ff3bd2c4d39a4411b5a5cb82e4281ff4af98ff0d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337329"
---
# <a name="set-up-flex-credit-programs"></a>Lanksčiųjų kreditų programų sąranka

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Galite naudoti lanksčiųju kreditų programas programoje „Microsoft Dynamics 365 Human Resources”, kad užregistruotumėte darbuotojus išmokoms gauti pagal iš anksto nustatytą lanksčiųjų kreditų skaičių. Darbuotojai gali pasirinkti, kaip priskirti savo lanksčiuosius kreditus. Pavyzdžiui, jeigu darbuotojui taikomas sutuoktinio sveikatos draudimo planas, jie gali norėti naudoti kreditus, kuriuos būtų naudoję sveikatos draudimui, kitoms išmokoms. 

1. Darbo srities **Išmokų valdymas** dalyje **Planai** pasirinkite **Lanksčiųjų kreditų programos**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Išmokos kredito ID** | Unikalus lanksčiųjų kreditų programos identifikatorius. |
   | **Aprašymas** | Lanksčiųjų kreditų programos aprašas. | 
   | **Data Nuo** | Lanksčiųjų kreditų aktyvinimo data ir laikas. |
   | **Data Iki** | Lanksčiųjų kreditų programos pabaigos data. Galite palikti numatytąją vertę (2154-12-31), kad nurodytumėte, jog lanksčiųjų kreditų programai nėra suplanuotos galiojimo pabaigos. |
   | **Bendra kreditų vertė** | Kreditų skaičius, kurį kiekvienas darbuotojas turės naudoti savo išmokoms. |
   | **Proporcingumo taisyklė** | Taisyklė, naudojama proporcingai paskirstyti lanksčiuosius kreditus, kai darbuotojas pasamdytas lanksčiųjų kreditų laikotarpio viduryje. </br></br><ul><li>**Nėra** – darbuotojas negauna lanksčiųjų kreditų, jei jis pasamdytas po lanksčiųjų kreditų programos laikotarpio pradžios.</li><li>**Visas kreditas** – darbuotojas gauna visą lanksčiųjų kreditų sumą, neatsižvelgiant į tai, kada jis įdarbintas.</li><li>**Proporcingai paskirstyti** – darbuotojas gauna proporcingai paskirstytą lanksčiųjų kreditų sumą, pagrįstą pagal tai, kada įdarbinimo pradžios data.</li></ul> |
   | **Lanksčiųjų kreditų proporcingumo formulė** | Taisyklė, naudojama proporcingai paskirstyti lanksčiuosius kreditus darbuotojams, pasamdytiems lanksčiųjų kreditų programos išmokų laikotarpio viduryje. Proporcingumas paremtas įdarbinimo pradžios data. Šis laukas naudojamas, tik jei lauke **Proporcingumo taisyklė** pasirinkote **Proporcingai paskirstyti**. </br></br><ul><li>**Kasdien** – proporcingai paskirstomas lanksčiųjų kreditų skaičius, kurį darbuotojas gauna kasdien. Bendras lanksčiųjų kreditų skaičius padalijamas iš laikotarpio dienų skaičiaus. Pavyzdžiui, jeigu jūsų išmokų laikotarpis yra 400 dienų, sistema padalins bendrą lanksčiųjų kreditų skaičių iš 400, kad apskaičiuotų lanksčiųjų kreditų skaičių, kurį per dieną gauna darbuotojai.</li><li>**Einamasis mėnuo** – proporcingai paskirstomas lanksčiųjų kreditų skaičius, kurį darbuotojas gauna per mėnesį, ir suapvalinamas iki esamo mėnesio. Bendras lanksčiųjų kreditų skaičius padalijamas iš laikotarpio mėnesių skaičiaus. Pavyzdžiui, jeigu jūsų išmokų laikotarpis yra 15 mėnesių, sistema padalins bendrą lanksčiųjų kreditų skaičių iš 15, kad apskaičiuotų lanksčiųjų kreditų skaičių, kurį per mėnesį gauna darbuotojai.</li><li>**Kitas mėnuo** – proporcingai paskirstomas lanksčiųjų kreditų skaičius, kurį darbuotojas gauna per mėnesį, ir suapvalinamas iki kito mėnesio. Bendras lanksčiųjų kreditų skaičius padalijamas iš laikotarpio mėnesių skaičiaus. Pavyzdžiui, jeigu jūsų išmokų laikotarpis yra 15 mėnesių, sistema padalina bendrą lanksčiųjų kreditų skaičių iš 15, kad apskaičiuotų lanksčiųjų kreditų skaičių, kurį per mėnesį gauna darbuotojai.</li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
