---
title: RCS patobulintas filtravimas RCS / bendrojoje saugykloje
description: Šioje temoje aprašomos išplėstos RCS visuotinės saugyklos filtravimo galimybės, dėl kurių galima įtraukti papildomus filtrus.
author: JaneA07
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0aa172550f86a9918a9aaa811e49cb20e7befcdb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359254"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>RCS patobulintos filtravimo parinktys, ieškant konfigūracijų RCS / bendrojoje saugykloje

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos patobulintos „Regulatory Configuration Service“ (RCS) bendrosios saugyklos galimybės, dėl kurių galima filtruoti, kai taikomi toliau nurodyti kriterijai. 
- **Šalis / regionas** – pagal ISO šalių kodus  
- **Žymų** tipai, skirti toliau nurodytiems dalykams.
  - Funkcinė sritis
  - Funkcijos sritis
  - Rinka 
  - Verslo dokumentas 

Norėdami lengviau rasti konkrečias arba susijusias konfigūracijas, galite taikyti filtrus atskirai arba kaip grupę. Pavyzdžiui, norėdami rasti vieno tipo konfigūruojamus verslo dokumentus, susijusius su tiekėjo SF, galite taikyti filtrą **Verslo dokumento tipas** to tipo dokumentui ieškoti. 

[![Filtravimo skyrius bendrajai saugyklai.](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Galite patikslinti iešką pasirinkdami dokumento tipą, pvz., tiekėjo SF, ir spustelėti **Taikyti filtrą**. Toliau pateikiamame pavyzdyje parodomi rezultatai, gauti filtruojant **Verslo dokumento tipas**, įtraukus dokumento tipą. 

[![Verslo dokumento tipo filtravimas ir importavimas.](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Filtruotus rezultatus galima importuoti į vartotojo RCS saugyklą arba „Dynamics 365 Finance” aplinką atskirai arba kaip rinkinį. Norėdami tai atlikti, pasirinkite konfigūracijų grupę ir spustelėkite **Importuoti**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]