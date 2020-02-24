---
title: Nustatyti išmokų valdymo parametrus
description: Išmokų valdymo parametrų konfigūravimas programoje „Microsoft Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009947"
---
# <a name="set-benefits-management-parameters"></a>Nustatyti išmokų valdymo parametrus

[!include [banner](includes/preview-feature.md)]

Jeigu norite nustatyti atostogų planus programoje „Microsoft Dynamics 365 Human Resources“, reikia sukonfigūruoti išmokų valdymo parametrus. Pagal šios parametrus nustatomos numatytosios vertės, priežasčių kodai ir kitos pasirinktys.

## <a name="configure-general-parameters"></a>Bendrųjų parametrų konfigūravimas

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Parametrai**.

2. Skirtuke **Bendra** įveskite šių laukų reikšmes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Šalis/regionas** | Laukas **Šalis / regionas** nustato pašto indeksų / valstijų rodymo tvarką. Pasirinkta šalis rodoma pirma išplečiamajame sąraše. |
   | **Registracijos priežasties kodas** | Pasirinkite numatytąjį priežasties kodą, kuris bus naudojamas, kai kuriami darbuotojų planai apdorojant atvirą registraciją. |
   | **Atšaukimo priežasties kodas** | Priežasties kodas, naudojamas atšaukiant darbuotojo išmokų planą. Jis rodomas dialogo lange vykdant atšaukimo procesą. Jei reikia, vartotojai gali keisti **atšaukimo priežasties kodą**. |
   | **Pakartotinai atidaryti priežasties kodą** | Priežasties kodas, naudojamas pakartotinai atidarant darbuotojo išmokų planą. Jis rodomas dialogo lange vykdant atšaukimo procesą. Jei reikia, vartotojai gali keisti **pakartotinio atidarymo priežasties kodą**. | 
   | **Gyvenimo įvykio priežasties kodas** | Priežasties kodas, kuris bus naudojamas įvykus gyvenimo įvykiui. |
   | **Tarifo pakeitimo priežasties kodas** | Priežasties kodas, kuris bus naudojamas atšaukiant ir iš naujo atidarant darbuotojo išmokų planą tarifo keitimo atnaujinimo proceso metu. Jis nurodo, kokie įrašai buvo pakeisti vykdant tarifo keitimo atnaujinimo procesą. |
   | **Nauja samda tinkama** | Nurodo, ar naujos samdos yra tinkamos. |
   | **Naujos samdos registracijos laikotarpis** | Laikotarpis, kuriuo leidžiama naujos samdos registracija.</br></br>**Pastaba**. Šiuo parametru perrašomas bet koks naujas registracijos laikotarpis, kurį nustatėte plano tinkamumo taisyklėje. | 
   | **Metinis atlyginimo didinimas** | Nurodoma, ar automatiškai apskaičiuoti sumą **Metinis išmokų atlyginimas** dalyje **Įdarbinimo išmokų informacija**. Ji grindžiama darbuotojo **pastoviosios atlyginimo dalies mokesčio tarifu**, **valandų vidurkiu** ir **mokėjimo dažnumu**.</br></br>**Valandų vidurkis** x **Fiksuotas mokėjimo tarifas** x **Mokėjimo dažnumas** (mokėjimo laikotarpių skaičius) = **Metinis išmokų atlyginimas** </br></br>Jei bet kurios reikšmės laukuose **Valandų vidurkis**, **Pastoviosios atlyginimo dalies mokesčio tarifas** arba **Mokėjimo dažnumas** pasikeičia, sistema automatiškai perskaičiuoja darbuotojo **metinio išmokų atlyginimo** sumą pagal pasikeitusias vertes. Sistema sukuria įrašą **Įsigaliojimo data**, kad būtų galima nustatyti tikslią pasikeitimo datą ir laiką. Jei reikia, galite neautomatiškai redaguoti **metinio išmokų atlyginimo** sumą. |
   | **Įgalinti gyvenimo įvykiai** | Įgalinami gyvenimo įvykiai. |
   | **Slėpti pasenusias išmokų formas** | Leidžia slėpti pasenusias išmokų formas. |

3. Pasirinkite **Įrašyti**.

## <a name="configure-employee-self-service-parameters"></a>Darbuotojų savitarnos dalies parametrų konfigūravimas

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Parametrai**.

2. Skirtuke **Darbuotojų savitarna** įveskite šių laukų reikšmes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Išmokos patvirtinimas** | Patvirtinimo tekstas, naudojamas išsiregistruojant iš savitarnos išmokų dalies. |
   | **Automatiškai parinkti gavėjus** | Nurodoma, ar automatiškai pasirenkami priklausomieji ir išmokų gavėjai atsižvelgiant į tinkamumą plano parinktims. |

3. Pasirinkite **Įrašyti**.
