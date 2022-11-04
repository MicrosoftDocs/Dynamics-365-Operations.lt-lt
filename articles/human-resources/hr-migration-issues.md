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
ms.openlocfilehash: 28c2c10a9293d00e26dfcc80ab08b89a122a6135
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2022
ms.locfileid: "9732775"
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

## <a name="licensing"></a>Licencijavimas

Šiose srityse licencijavimo pakeitimų nėra Dynamics 365 Human Resources: 

- **Mažiausias licencijos pirkimo reikalavimo skaičius**
- **Gamybos** aplinkos ir sandbox aplinkos licencijos – jei turite atskiras personalo licencijas, kurias sudaro viena gamybos aplinka ir viena sandbox aplinka, finansų ir operacijų infrastruktūrai bus galima naudoti tą patį licencijų skaičių.
- **Papildomos sandbox** licencijos – jei įsigijote papildomų sandbox licencijų atskirai personalo programai, bus galima naudoti tą patį licencijų skaičių sandbox aplinkai finansų ir operacijų infrastruktūrai. 
