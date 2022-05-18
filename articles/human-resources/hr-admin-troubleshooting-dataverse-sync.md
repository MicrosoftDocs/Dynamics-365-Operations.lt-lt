---
title: Atkurti „Dataverse“ sinchronizavimą
description: Šioje temoje aprašoma, kaip šalinti įrašus, kurie nesinchronizuojami teisingai tarp ir personalo valdymo „Microsoft Dynamics 365 Human Resources“ (HCM) bendro sprendimo „Microsoft Dataverse“.
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 8bfcd51b023c02590919155abbb836326408d298
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696241"
---
# <a name="reset-dataverse-synchronization"></a>Atkurti „Dataverse“ sinchronizavimą


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Problema

Įrašai nesinchronizuojami tarp ir personalo valdymo „Microsoft Dynamics 365 Human Resources“ (HCM) bendrojo sprendimo objektų „Microsoft Dataverse“. Norėdami gauti daugiau informacijos apie sinchronizavimą, eikite į [Konfigūruoti „Dataverse“ integravimą](hr-admin-integration-common-data-service.md). Nepavyko tinkamai sinchronizuoti, kai integravimo **Dataverse kartojimo** ar **Dataverse integravimo praleistos užklausos sinchronizavimo** paketo darbai yra užstrigę **Vykdymo** būsenoje.

## <a name="resolution"></a>Sprendimas

Kai **Dataverse integravimo paleidimo** ar **Dataverse integravimo praleistų užklausų sinchronizavimas** paketo darbai yra užstrigę **Vykdymo** ar **Atšaukimo** būsenoje, galite atšaukti šią būseną. Tai galima padaryti atšaukus paketinę užduotį, jei vadovu iš naujo [nustatykite paketines užduotis](hr-admin-troubleshooting-batch-execution.md). Atšaukę paketinę užduotį galite ją nustatyti iš naujo, nustatydami laukimo **būseną**. Paketinė užduotis bus vykdoma kito suplanuoto vykdymo metu.

1. Jei to dar nepadarėte, funkcijų valdymo **srityje įgalinkite funkciją** Išplėstinis **paketo nutraukimas**.
   1. Eikite į **funkcijų valdymo** puslapį (**Sistemos administravimo** > **Suvestinės** > **Funkcijų valdymas**).
   2. Pasirinkite skirtuką **Visi**.
   3. Pasirinkite **funkcijos pavadinimo** stulpelį ir filtruokite **pagal išplėstinį paketą**.
   4. Jei dar **Įgalintas**, pasirinkite veiksmą Įgalinti.

2. „Dataverse“ integravimo išjungimas.
   1. Eikite į **Microsoft Dataverse integravimo** puslapį (**Sistemos administravimas** eikite į **Integravimo** > **saitų** > **Dataverse konfigūracija**).
   2. Nustatykite parinktį **Įgalinti „Dataverse” integravimą** į **Ne**.

3. Atšaukite integravimo **Dataverse kartojimo** paketinę užduotį.
   1. Eikite į **Paketinės užduotys** puslapį (**Sistemos administravimas** eikite į **Nuorodos** > **Paketinės užduotys** > **Paketinės užduotys**).
   2. Filtruoti **užduoties aprašymo** stulpelį pagal **integravimą**.
   3. Rinkitės integravimo **Dataverse kartojimo** paketinę užduotį.
   4. Veiksmų juostelėje pasirinkite **Paketinė užduotis**, **Priversti atšaukti** ir tada rinkitės **Taip** patvirtinti.

   > [!NOTE]
   > Priklausomai nuo to, kada pirmą kartą buvo įgalintas integravimas, paketinėje užduotyje gali būti pateiktas aprašymo **Common Data Service integravimo kartojimo** procesas. Pasirinkite šią paketinę užduotį, jei ji pateikta, vietoj **integravimo Dataverse kartojimo** paketinės užduoties.

4. Naikinti visas integravimo Dataverse paketines užduotis.
   1. Puslapyje **Paketinės užduotys** rinkitės **Dataverse integravimo praleistą užklausos sinchronizavimą**, **Dataverse integravimo kartojimo**, ir **Dataverse integravimo pradinių sinchronizavimo** paketines užduotis.
   2. Veiksmų juostoje rinkitės veiksmą **Keisti būseną**. 
   3. Pasirinkite jį, tada pasirinkite **Sulaikyti** ir **Gerai**.
   4. Veiksmų juostelėje pasirinkite veiksmą **Naikinti**, tada, norėdami patvirtinti **veiksmą**, pasirinkite Taip.

5. Įjunkite integravimo „Dataverse“ paketines užduotis.
   1. Eikite į **Microsoft Dataverse integravimo** puslapį (**Sistemos administravimas** > **Nuorodos** > **Integravimo** > **Dataverse konfigūracija**).
   2. Nustatykite parinktį **Įgalinti „Dataverse” integravimą** į **Taip**.

6. Eikite į **paketinių užduočių** puslapį ir patvirtinkite, kad  **Dataverse integravimo kartojimo** ir **Dataverse integravimo praleistos užklausos** sinchronizavimo paketinės užduotys.

Kai paketinės užduotys atkurtos, galite stebėti integravimo kartojimo paketinę užduotį, kad pamatytumėte, kiek laiko **Dataverse užduočiai vykdyti**. Tada galite patikrinti, ar įrašai tinkamai sinchronizuojami su HCM Common „Microsoft Dataverse“ sprendimu.

## <a name="see-also"></a>Taip pat žiūrėkite

[„Dataverse“ integravimo konfigūravimas](hr-admin-integration-common-data-service.md)<br>
[Užstrigusių paketinių užduočių nustatymas iš naujo](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
