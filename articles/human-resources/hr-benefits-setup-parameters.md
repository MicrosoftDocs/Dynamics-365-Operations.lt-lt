---
title: Nustatykite Priedų valdymą ir Darbuotojo savitarnos parametrus visoms įmonėms
description: Konfigūruokite parametrus naudų valdymui ir darbuotojo savitarnai „Microsoft Dynamics 365 Human Resources“.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10f5310ba4feba4a196d02c406ff3217637e447e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791490"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a>Nustatykite Priedų valdymą ir Darbuotojo savitarnos parametrus visoms įmonėms

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Prieš tai, kai nustatysite priedų planus „Microsoft Dynamics 365 Human Resources“, turite sukonfigūruoti Priedų valdymo parametrus. Pagal šios parametrus nustatomos numatytosios vertės, priežasčių kodai ir kitos pasirinktys. 

## <a name="configure-general-parameters"></a>Bendrųjų parametrų konfigūravimas

1. **Išmokų valdymo** darbo srityje, **Nustatymo** skyriuje, pasirinkite **Žmogiškųjų išteklių pasidalyti parametrai**.

2. Skirtuke **Išmokų valdymas** įveskite toliau pateiktų laukų reikšmes.

   | Laukas | aprašymas |
   | --- | --- |
   | **Šalis/regionas** | Laukas **Šalis / regionas** nustato pašto indeksų / valstijų rodymo tvarką. Pasirinkta šalis rodoma pirma išplečiamajame sąraše. |
   | **Registracijos priežasties kodas** | Pasirinkite numatytąjį priežasties kodą, kuris bus naudojamas, kai kuriami darbuotojų planai apdorojant atvirą registraciją. |
   | **Atšaukimo priežasties kodas** | Priežasties kodas, naudojamas atšaukiant darbuotojo išmokų planą. Jis rodomas dialogo lange vykdant atšaukimo procesą. Jei reikia, vartotojai gali keisti **atšaukimo priežasties kodą**. |
   | **Pakartotinai atidaryti priežasties kodą** | Priežasties kodas, naudojamas pakartotinai atidarant darbuotojo išmokų planą. Jis rodomas dialogo lange vykdant atšaukimo procesą. Jei reikia, vartotojai gali keisti **pakartotinio atidarymo priežasties kodą**. | 
   | **Gyvenimo įvykio priežasties kodas** | Priežasties kodas, kuris bus naudojamas įvykus gyvenimo įvykiui. |
   | **Tarifo pakeitimo priežasties kodas** | Priežasties kodas, kuris bus naudojamas atšaukiant ir iš naujo atidarant darbuotojo išmokų planą tarifo keitimo atnaujinimo proceso metu. Jis nurodo, kokie įrašai buvo pakeisti vykdant tarifo keitimo atnaujinimo procesą. |
   | **Metinis išmokų atlyginimas** | Leidžia jums nustatyti **Metinės išmokos naudos** sumą darbuotojui. Žmogiškieji ištekliai naudos **Metinės algos išmokos** sumą nustatydami padengiamas sumas, o ne fiksuotą metinio atlyginimo sumą. |
   | **Nauja samda tinkama** | Nurodo, ar naujos samdos yra tinkamos. |
   | **Naujos samdos registracijos laikotarpis** | Laikotarpis, kuriuo leidžiama naujos samdos registracija.</br></br>**Pastaba**. Šiuo parametru perrašomas bet koks naujas registracijos laikotarpis, kurį nustatėte plano tinkamumo taisyklėje. |
   | **Numatytasis mokėjimo dažnumas** | Nustatytasis mokėjimo dažnumas naudotinas, kai yra įtraukiami nauji darbuotojai. |
   | **Įgalinti gyvenimo įvykiai** | Įgalinami gyvenimo įvykiai. |
   | **Slėpti pasenusias išmokų formas** | Leidžia slėpti pasenusias išmokų formas. |
   | **Išmokos patvirtinimas** | Patvirtinimo tekstas, naudojamas išsiregistruojant iš savitarnos išmokų dalies. |
   | **Automatiškai parinkti gavėjus** | Nurodo, ar automatiškai pasirinkti priklausinius ir naudos gavėjus pagal jų tinkamumą plano parinktims. |

3. Pasirinkite **Įrašyti**.

## <a name="configure-employee-self-service-parameters"></a>Konfigūruoti darbuotojo savitarnos parametrus

1. **Išmokų valdymo** darbo srityje, **Nustatymo** skyriuje, pasirinkite **Žmogiškųjų išteklių pasidalyti parametrai**.

2. Skirtuke **Išmokų valdymas** įveskite toliau pateiktų laukų reikšmes.

   | Laukas | Aprašas |
   | --- | --- |
   | **Išmokos patvirtinimas** | Patvirtinimo tekstas, naudojamas išsiregistruojant iš savitarnos išmokų dalies. |
   | **Automatiškai parinkti gavėjus** | Nurodoma, ar automatiškai pasirenkami priklausomieji ir išmokų gavėjai atsižvelgiant į tinkamumą plano parinktims. |

3. Pasirinkite **Įrašyti**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]