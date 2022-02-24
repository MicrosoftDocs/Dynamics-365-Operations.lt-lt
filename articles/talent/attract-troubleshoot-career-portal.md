---
title: Programos „Attract“ vartotojai negali kandidatuoti į darbus iš karjeros portalo
description: Šiame skyriuje paaiškinama, kaip šalinti problemą, kada „Attract“ naudotojas negali kreiptis dėl darbų karjeros portale.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461961"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a>Programos „Attract“ vartotojai negali kandidatuoti į darbus iš karjeros portalo

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Išdavimas

„Attract“ naudotojai negali kreiptis dėl darbų karjeros portale. Jiems bandant kreiptis dėl darbo, kuris buvo sukurtas „Dynamics 365 Talent: Attract“, naršyklė nuolatos įkelia puslapį ir neužbaigia veiksmo.

## <a name="cause"></a>Priežastis

Ši problema atsitinka kai „Talent Relationship Team“ neturi „Talent“ naudotojo vaidmens.

## <a name="resolution"></a>Skiriamoji geba

Priskikrite „Talent“ naudotojo vaidmenį „Talent Relationship Team“.

1. Prisijunkite prie [„Power Platform“ administravimo centro](https://admin.powerplatform.microsoft.com) su bet kuriais iš toliau įvardytų administratoriaus prisijungimo duomenų:

   - „Dynamics 365“ administratorius
   - Globalus administratorius
   - „Power Platform“ administratorius

2. Naršymo juostoje pasirinkite **Aplinkos** ir tuomet pasirinkite aplinką, kurioje norite priskirite „Talent“ naudotojo vaidmenį „Talent Relationship Team“.

   ![Pasirinkite aplinką](./media/attract-troubleshoot-career-portal-select-environment.png)

3. **Aplinkų** juostoje pasirinkite **Aplinkos URL** ir prisijunkite prie aplinkos administravimo portalo (pavyzdžiui, https:<orgname>.crm.dynamics.com).

4. Pasirinkite **Nustatymai**, rinkitės **Sistema** ir tada rinkitės **Sauga**.

   ![Eikite į saugą](./media/attract-troubleshoot-career-portal-security.png)

5. Rinkitės **Komandos**.

   ![Rinkitės Komandos](./media/attract-troubleshoot-career-portal-security-teams.png)

6. Ieškokite **„Talent Relationship Team“** paieškos laukelyje ir tada pasirinkite komandą iš paieškos rezultatų.

7. Pasirinkite **TVARKYTI VAIDMENIS** juostoje.

8. Teksto laukelyje **Tvarkyti komandos vaidmenis** pasirinkite **„Talent“ naudotojas** iš esamo vaidmenų sąrašo ir rinkitės **GERAI** tam, kad taikytumėte vaidmenį.

   ![Taikykite vaidmenį](./media/attract-troubleshoot-career-portal-apply-role.png)

9. Išbandykite savo pokyčius:

   1. Prisijunkite prie karjeros portalo per naują naršyklės langą.
   2. Taikykite darbą iš karjeros portalo. 