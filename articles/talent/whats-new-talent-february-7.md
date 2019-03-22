---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. vasario 7 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 for Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 23386d04fac5a41682d3ced448ce07e6729def3c
ms.sourcegitcommit: b3b21795f36e5852ffe18200d6fe0b93363b1cbd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/08/2019
ms.locfileid: "377749"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-7-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 for Talent“ (2019 m. vasario 7 d.)

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

### <a name="interview-scheduling-enhancements"></a>Pokalbio planavimo patobulinimai
Atlikti visapusės pokalbių planavimo sąsajos patobulinimai. Dabar galite matyti vidinio kandidato kalendorių pasiekiamumą ir naudoti vidinio kandidato kalendorių grafiko rekomendacijose. Daugiau informacijos žr. [Pokalbio planavimas ir atsiliepimas](interview-scheduling-feedback.md).

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>Darbo registravimas „LinkedIn“ – pašalinta įmonės neatitikimo problema
Pašalinta problema, dėl kurios „LinkedIn“ registruojami „Attract“ darbai buvo priskiriami įmonei netinkamu pavadinimu. Daugiau informacijos žr. [„Attract“ darbų kūrimas, tvirtinimas ir registravimas](creating-jobs-attract.md).

### <a name="career-site-url-displayed-in-admin-settings"></a>Karjeros svetainės URL rodomas administravimo parametruose
Dabar karjeros svetainės pagrindinio puslapio URL rodomas skiltyje **Administravimo parametrai**, pateiktoje dalyje **Karjeros svetainės valdymas**.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

**8.1.2134 versija**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>Užduotyse palaikomi keli kompensacijų lygiai
Šis pakeitimas suteikia galimybę užduotyje nurodyti daugiau nei vieną kompensacijos lygį, todėl galima naudoti darbuotojų pastoviųjų atlyginimo dalių diapazonus, kurie planuose gali skirtis, kai naudojama tą pati užduotis. 

Pavyzdys:    
*Užduotis* – Paskyros vadovas *Susijusių kompensacijų lygiai:* B1 ir B2 – kiekvienam lygiui priskirtas nustatytas reikšmių diapazonas. B1 = min. 50 000, vid. 60 000, maks. 75 000 ir B2 = min. 65 000, vid. 74 000, maks. 85 000. Dabar kuriant darbuotojų pastoviąją atlyginimo dalį pagal nustatytas tinkamumo taisykles kiekvienas ilgalaikis planas gali nurodyti tą pačią užduotį skirtingus lygius užduotyje. Tai suteikia galimybę planus nustatyti skirtinguose regionuose / įmonėse ir nurodyti tą pačia užduotį, bet skirtingus diapazonus, nesukuriant užduočių dublikatų dėl šių skirtumų.

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>Kompensacijos lygio laukas įtrauktas objektą Darbuotojo fiksuota atlyginimo dalis 
Šiame naujinime objektas Darbuotojo fiksuota atlyginimo dalis buvo atnaujinta – į ją įtrauktas laukas **Kompensacijos lygis**. Šis pakeitimas palengvina darbuotojų pastoviosios atlyginimo dalies planų naujinimą. 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>Užduočių grupės naujinimas naujinant ir kuriant naujas pareigas
Keičiant pareigų užduotį, **Užduočių grupė** bus nustatyta priklausomai nuo pasirinktos užduoties.

### <a name="performance-improvements-when-rendering-workspaces"></a>Darbo sričių atvaizdavimo našumo patobulinimai
Dabar darbo sričių analizės skirtukai bus įkeliami tik atidarant tuos puslapius. Pradinio puslapio generavimo metu viršutiniame kairiajame puslapio kampe bus rodomas indikatorius.
