---
title: Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. lapkričio 5 d.)
description: Šioje temoje aprašomos naujos ir pakeistos „Microsoft Dynamics 365 Talent“ funkcijos.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6a81209c3c4a95ee51668533d40d4aecc1d58b9
ms.sourcegitcommit: a46fb06138f7f82e973dca3157d30f9b21d3a70b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778387"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Kas nauja ar pasikeitė sistemoje „Dynamics 365 Talent“ (2019 m. lapkričio 5 d.)

[!include [banner](includes/banner.md)]

Šioje temoje aprašomos naujos ir pakeistos „Dynamics 365 Talent“ funkcijos.

## <a name="changes-in-attract"></a>„Attract“ pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Attract“.

## <a name="changes-in-onboard"></a>Supažindinimo pakeitimai

Šiame leidime pataisytos nežymios klaidos programoje „Dynamics 365 Talent: Onboard“.

## <a name="changes-in-core-hr"></a>„Core HR“ pakeitimai

Šiame skyriuje aprašyti pakeitimai taikomi 8.1.2598 komponavimo versijai. Kai kurių antraščių skaičiai skliausteliuose nurodo palaikymo numerius „Microsoft Dynamics Lifecycle Services“ (LCS).

### <a name="copy-a-core-hr-instance"></a>„Core HR“ egzemplioriaus kopijavimas

Šios savaitės leidime galite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS), kad nukopijuotumėte „Microsoft Dynamics 365 Talent: Core HR“ duomenų bazę į smėlio dėžės aplinką. Jei turite kitą smėlio dėžės aplinką, taip pat galite kopijuoti duomenų bazę iš šios aplinkos į tikslinę smėlio dėžės aplinką. Daugiau informacijos ieškokite:

- [Platesnės aplinkos valdymas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) „Dynamics 365“: 2019 m. leidimo 2 planas

- [„Core HR“ kopijavimas](hr-copy-instance.md) į „Talent“ dokumentus

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>„Common Data Service“ integravimo paketinės užduotys nekuriamos, kai „Common Data Service“ integravimas įjungtas (388030)

Atlikus šį keitimą bus sukurtos paketinės užduotys, skirtos „Common Data Service“ integravimui, kai jis įjungtas.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity negali pakeisti asmens nuotraukos, kai ji įkeliama (369469)

Šios savaitės leidime pakeista, kaip keičiamas nuotraukų dydis dėl geresnio efektyvumo, kai nuotrauka įkeliama per duomenų valdymą.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>Pareigų, kurias galima priskirti, data gali būti ankstesnės už aktyvinimo datą (340103)

Atlikus šį keitimą, bus rodomas įspėjimas, jei pasirinksite **Galima priskyrimo data** ankstesnę nei pareigų **Aktyvinimo data**.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Negalima sukurti kompensacijos keitimo užklausos darbuotojo savitarnoje dėl veiksmais pagrįstų planų (376872)

Šis leidimas išsprendžia problemą, kai užklausiama kompensacija keičiasi darbuotojo savitarnoje dėl veiksmais pagrįstų planų. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Priežasties kodas nesinchronizuojamas su „Common Data Service“, jei aprašas ilgesnis nei 30 simbolių, „Core HR“ leidžia 60 simbolių (352682)

atlikus šį keitimą, priežasčių kodai iš 30 simbolių bus atnaujinti „Common Data Service“. Pakeitimai, atlikti „Common Data Service“, bus matomi ir „Talent“.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Adreso integravimas iš „Talent“ į „Finance and Operations“ (351961)

Šis leidimas išsprendžia problemą, kai adresas, atnaujintas „Talent“, nebuvo atnaujintas „Finance and Operations“. Adresų bloko keitimai dar bus atnaujinti.

## <a name="coming-soon"></a>Jau greitai

### <a name="print-performance-reviews"></a>Veiklos efektyvumo vertinimų spausdinimas

Žr. [Veiklos efektyvumo vertinimų spausdinimas](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) dirbant su „Dynamics 365“: 2019 leidimo 2 bangos planu.

### <a name="feature-management-workspace"></a>Funkcijos valdymo darbo sritis

Funkcijos įtraukiamos ir atnaujinamos kiekviename leidime. Funkcijų valdymo patirtis suteikia darbo sritį, kurioje galite peržiūrėti kiekviename leidime pristatytų funkcijų sąrašą. Pagal numatytuosius nustatymus naujos funkcijos yra išjungtos. Galite naudoti darbo sritį, norėdami jas įjungti ir peržiūrėti jų dokumentaciją.

Norėdami daugiau sužinoti apie pakeitimus, pristatytus su funkcijų valdymu, žr. [Funkcijų valdymo apžvalga](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
