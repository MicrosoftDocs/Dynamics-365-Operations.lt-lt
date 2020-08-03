---
title: Nustatyti išmokų valdymo parametrus
description: Išmokų valdymo parametrų konfigūravimas programoje „Microsoft Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 85bbe5d3b422f2f29f1d1fe8ee269b407da691c2
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599361"
---
# <a name="set-benefits-management-parameters"></a>Išmokų valdymo parametrų nustatymas

Jeigu norite nustatyti atostogų planus programoje „Microsoft Dynamics 365 Human Resources“, reikia sukonfigūruoti išmokų valdymo parametrus. Pagal šios parametrus nustatomos numatytosios vertės, priežasčių kodai ir kitos pasirinktys.

## <a name="configure-general-parameters"></a>Bendrųjų parametrų konfigūravimas

1. **Išmokų valdymo** darbo srityje, **Nustatymo** skyriuje, pasirinkite **Žmogiškųjų išteklių pasidalyti parametrai**.

2. Skirtuke **Bendra** įveskite šių laukų reikšmes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Šalis/regionas** | Laukas **Šalis / regionas** nustato pašto indeksų / valstijų rodymo tvarką. Pasirinkta šalis rodoma pirma išplečiamajame sąraše. |
   | **Registracijos priežasties kodas** | Pasirinkite numatytąjį priežasties kodą, kuris bus naudojamas, kai kuriami darbuotojų planai apdorojant atvirą registraciją. |
   | **Atšaukimo priežasties kodas** | Priežasties kodas, naudojamas atšaukiant darbuotojo išmokų planą. Jis rodomas dialogo lange vykdant atšaukimo procesą. Jei reikia, vartotojai gali keisti **atšaukimo priežasties kodą**. |
   | **Pakartotinai atidaryti priežasties kodą** | Priežasties kodas, naudojamas pakartotinai atidarant darbuotojo išmokų planą. Jis rodomas dialogo lange vykdant atšaukimo procesą. Jei reikia, vartotojai gali keisti **pakartotinio atidarymo priežasties kodą**. | 
   | **Gyvenimo įvykio priežasties kodas** | Priežasties kodas, kuris bus naudojamas įvykus gyvenimo įvykiui. |
   | **Tarifo pakeitimo priežasties kodas** | Priežasties kodas, kuris bus naudojamas atšaukiant ir iš naujo atidarant darbuotojo išmokų planą tarifo keitimo atnaujinimo proceso metu. Jis nurodo, kokie įrašai buvo pakeisti vykdant tarifo keitimo atnaujinimo procesą. |
   | **Metinis išmokų atlyginimas** | Leidžia jums nustatyti **Metinės išmokos naudos** sumą darbuotojui.  Žmogiškieji ištekliai naudos **Metinės algos išmokos** sumą nustatant padengiamas sumas, o ne fiksuotą metinio atlyginimo sumą. |
   | **Nauja samda tinkama** | Nurodo, ar naujos samdos yra tinkamos. |
   | **Naujos samdos registracijos laikotarpis** | Laikotarpis, kuriuo leidžiama naujos samdos registracija.</br></br>**Pastaba**. Šiuo parametru perrašomas bet koks naujas registracijos laikotarpis, kurį nustatėte plano tinkamumo taisyklėje. |
   | **Numatytasis mokėjimo dažnumas** | Nustatytasis mokėjimo dažnumas naudotinas, kai yra įtraukiami nauji darbuotojai. |
   | **Įgalinti gyvenimo įvykiai** | Įgalinami gyvenimo įvykiai. |
   | **Slėpti pasenusias išmokų formas** | Leidžia slėpti pasenusias išmokų formas. |

3. Pasirinkite **Įrašyti**.

## <a name="configure-employee-self-service-parameters"></a>Darbuotojų savitarnos dalies parametrų konfigūravimas

1. **Išmokų valdymo** darbo srityje, **Nustatymo** skyriuje, pasirinkite **Žmogiškųjų išteklių pasidalyti parametrai**.

2. Skirtuke **Darbuotojų savitarna** įveskite šių laukų reikšmes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Išmokos patvirtinimas** | Patvirtinimo tekstas, naudojamas išsiregistruojant iš savitarnos išmokų dalies. |
   | **Automatiškai parinkti gavėjus** | Nurodoma, ar automatiškai pasirenkami priklausomieji ir išmokų gavėjai atsižvelgiant į tinkamumą plano parinktims. |

3. Pasirinkite **Įrašyti**.
