---
title: Bendrųjų duomenų peržvalgos aplinkos nustatymas
description: Šioje temoje paaiškinama, kaip nustatyti aplinką, kad būtų galima naudoti Mokesčių skaičiavimo bendrųjų duomenų peržvalgos funkciją.
author: kai-cloud
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: pashao
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eda093a75898bace2f3c7968933b83ccafa7fabb
ms.sourcegitcommit: 66095f1b7e0fd2756aa29fd7deb9ce5392b7e0b2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/08/2021
ms.locfileid: "5869085"
---
# <a name="set-up-an-environment-for-master-data-lookup"></a>Bendrųjų duomenų peržvalgos aplinkos nustatymas

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šioje temoje paaiškinama, kaip nustatyti aplinką, kad būtų galima naudoti Mokesčių skaičiavimo bendrųjų duomenų peržvalgos funkciją.

1. Nustatykite „Power Platform” integravimą „Lifecycle Services” (LCS). Daugiau informacijos rasite [„Microsoft Power Platform” integravimas – Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
2. Nustatykite „Dynamics 365 Finance” ir „Microsoft Dataverse”. Daugiau informacijos rasite [Gauti sprendimą](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#getting-the-solution) ir [Autentifikavimas ir autorizacija](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md#authentication-and-authorization).
3. Importuokite *Būtinąjį mokesčių tarnybos virtualiojo objekto sprendimą* iš [Mokesčių tarnybos virtualiojo objekto](https://go.microsoft.com/fwlink/?linkid=2158160).
4. Nustatykite „Dynamics 365 Regulatory Configuration Service” (RCS). 
5. Sukurkite „Microsoft” paslaugos užklausą, kad būtų galima naudoti šias funkcijas:

      - „ERCds” Funkciją
      - Mokesčių tarnybos „CDS” funkciją

6. „Finance” programoje eikite į darbo sritį **Funkcijų valdymas** ir įjunkite šias funkcijas:

      - (Peržiūros versija) Elektroninių ataskaitų „Dataverse” duomenų šaltinių palaikymas
      - (Peržiūros versija) Mokesčių tarnybos „Dataverse“ duomenų šaltinių palaikymas
      - (Peržiūros versija) Globalizacijos funkcijos

5. Prisijunkite prie RCS naudodami nuomotojo administratoriaus paskyrą.
6. Eikite į **Elektroninėmis ataskaitos** > **Prijungtos programos**. 
7. Pasirinkite **Nauja** įrašui pridėti ir įveskite toliau nurodytą lauko informaciją. 

   - Lauke **Pavadinimas** įveskite pavadinimą.
   - Lauke **Tipas** pasirinkite **„Dataverse”**.
   - Lauke **Programa** įveskite savo „Dataverse” URL.
   - Lauke **Nuomotojas** įveskite savo nuomotoją.
   - Lauke **Pasirinktinis URL** įveskite savo „Dataverse” URL ir sujunkite jį su „/api/data/v9.1”.

8. Pasirinkite **Tikrinti ryšį** ir užbaikite ryšio procesą. 

   [![Mygtukas Tikrinti ryšį](./media/tax-service-setup-environment-for-mater-date-pic1.png)](./media/tax-service-setup-environment-for-mater-date-pic1.png)

9. Eikite į **Elektroninės ataskaitos** > **Mokesčių konfigūracijos** ir importuokite mokesčių konfigūracijas iš [Mokesčių konfigūracijų](https://go.microsoft.com/fwlink/?linkid=2158352).

   [![Mokesčių konfigūracijų puslapis, Mokesčių duomenų modelio medis](./media/tax-service-setup-environment-for-mater-date-pic2.png)](./media/tax-service-setup-environment-for-mater-date-pic2.png)

10. Eikite į **Apmokestinto dokumento modelio susiejimas** arba **„Dataverse” modelio susiejimas**, jeigu naudojate „Microsoft” konfigūraciją ir lauke **Prijungta programa** pasirinkite įrašą, kurį sukūrėte 7 veiksme.
11. Nustatykite **Numatytasis modelių susiejimui** į **Taip**.

   [![Modelio susiejimo puslapis](./media/tax-service-setup-environment-for-mater-date-pic3.png)](./media/tax-service-setup-environment-for-mater-date-pic3.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
