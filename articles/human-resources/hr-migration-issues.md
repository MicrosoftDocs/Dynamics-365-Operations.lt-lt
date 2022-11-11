---
title: Dynamics 365 Human Resources ininfrastruktūrą sulieti žinomas problemas
description: Šiame straipsnyje pateikiamos problemos, kurios gali kilti "Microsoft" infrastruktūros Dynamics 365 Human Resources suliejimo metu.
author: twheeloc
ms.date: 10/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f5981801317ad9647f57a0f68f9b67b592256ab
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752696"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-known-issues"></a>Dynamics 365 Human Resources ininfrastruktūrą sulieti žinomas problemas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="shared-dataverse-environments"></a>Bendrai Dataverse naudojamos aplinkos

Dvigubo rašymo sistema nepalaiko dviejų finansų ir operacijų programų aplinkos susiejimo su ta pačia Dataverse aplinka. Jei turite tokią aplinką Dataverse, kuri bendrai naudojama su abiem šiais elementais, turite dubliuoti aplinką Dataverse arba ją išskaidyti:

- Finansų ir operacijų programa
- Dabartinė personalo aplinka

## <a name="environment-type-requirements"></a>Aplinkos tipo reikalavimai

Kad būtų galima perkelti, reikia šių aplinkos tipų:

- Jei neturite jokios sand. saugyklos atskirą aplinką, turite sukurti vieną, kad būtų galima tikrinti perkėlimą.
- Jei turite kelias atskiras gamybos aplinkas, vieną iš jų galima perkelti. Susisiekite su "Microsoft" palaikymo tarnyba ir pažymėkite kitas aplinkas kaip sand. dėžes.

## <a name="teams-integration"></a>„Teams“ integravimas

Esama komandų personalo programa šiuo metu perkeliama į Microsoft Power Platform sprendimą. Daugiau informacijos žr. [„Human Resources“ programa programoje „Teams“](hr-admin-teams-leave-app.md).

