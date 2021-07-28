---
title: Algalapių integravimo API įžanga
description: Šioje temoje aprašomas „Dynamics 365 Human Resources” algalapio integravimo API.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3b6b01053a043477521d7eb1a41bb9f6f51fc0e4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360573"
---
# <a name="payroll-integration-api-introduction"></a>Algalapių integravimo API įžanga

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame dokumente aprašomas „Dynamics 365 Human Resources” algalapio integravimo API. API įgalina supaprastintą visapusišką integravimą tarp Personalo valdymo ir algalapio sistemų partnerių. Integravimo patirtis prasideda Personalo valdymo srityje su darbuotojo profilio, atlyginimo, atskaitymo ir įnašo informacija. Kai pasamdote darbuotoją ir įvedate reikiamą profilio bei mokėjimo informaciją į Personalo valdymo sritį, algalapio sistema naudoja šią informaciją algalapio apdorojimui. Bet kokie darbuotojo ar mokėjimo informacijos atnaujinimai taip pat yra naudojami vėlesniuose mokėjimo vykdymuose.

[![Algalapių integravimo srautas.](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

Dėl integravimo įgalinimo, Personalo valdyme yra šie komponentai:

- Funkcija pažymėti darbuotoją kaip pasirengusį mokėti
- Integravimo API, atveriantis naujas programų integravimo funkcijas

## <a name="microsoft-dataverse"></a>„Microsoft Dataverse“

API yra sukurtos „Microsoft Dataverse“ (anksčiau „Common Data Service“). Visos RESTful sąveikos su šiuo API yra daromos per „Microsoft Dataverse“ žiniatinklio API, kurios naudoja OData. Šis API yra papildomas rinkinys „Dataverse“ žiniatinklio API. „Dataverse“ žiniatinklio API nustato savybes, tokias kaip autentifikavimas, SLA, rinkinys, konkurencijos kontrolė ir klaidų tvarkymas.

Dėl bendresnės informacijos apie „Microsoft Dataverse“ žiniatinklio API, žr.:

- [Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)
- [Naudokite „Microsoft Dataverse“ žiniatinklio API](/powerapps/developer/data-platform/webapi/overview)
- [„Microsoft Dataverse“ kūrėjo gairės](/powerapps/developer/data-platform)

Šiame dokumente pateikiama išsami informacija ir gairės programuotojams, kaip naudoti „Dataverse” žiniatinklio API, įskaitant šias temas:

- [„Microsoft Dataverse” autentifikavimas su Žiniatinklio API](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Operacijų atlikimas naudojant Žiniatinklio API](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Paštininko naudojimas su Žiniatinklio API](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Keitimų sekimo naudojimas duomenims su išorinėmis sistemomis sinchronizuoti](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtualios lentelės žmogiškiesiems ištekliams „Dataverse“

Galiniai Algalapio integravimo API punktai naudoja virtualios lentelės platformos galimybes „Microsoft Dataverse“. Pagal nutylėjimą, virtualios lentelės ir jų susieti API galiniai punktai nėra diegiami Personalo valdymo aplinkose, taip įgalinant organizacijas nustatyti, kurie „OData” galiniai punktai turi būti rodomi aplinkoje. Norėdami naudoti API, virtualios lentelės, skirtos žmogiškųjų išteklių objektams, turi būti sukurtos aplinkoje.

Dėl informacijos apie virtualių lentelių kūrimą API, žr. [Konfigūruoti „Dataverse“ virtualias lenteles](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Duomenų modelis

Tolesnėje diagramoje rodomi santykiai su API. Keli tipai turi užsienio raktus su kitais, iš anksto esantys objektai žmogiškuosiuose ištekliuose čia nerodomi. Šiame dokumente pateikta informacija apie objektus, kurie yra būdingi algalapio integravimo scenarijams. Tačiau yra daugelis kitų Personalo valdymui skirto „Dataverse“ žiniatinklio API objektų, kurie taip pat gali būti svarbūs jūsų integravimui. Kai kurie iš šių objektų yra nurodyti išorinių raktų ryšiuose ar naršymo ypatybėse.

[![Algalapio integravimo API duomenų modelis.](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>Algalapio darbuotojas ir susiję objektai

Objektai:

- [Algalapio darbuotojas](hr-admin-integration-payroll-api-payroll-employee.md)
- [Algalapio darbuotojo adresas](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [Algalapio pastoviosios atlyginimo dalies planas](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [Algalapio kintamosios atlyginimo dalies planas](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [Algalapių padėties užduotis](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Algalapių padėtis](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>Taip pat žiūrėkite

[Algalapio objektų generavimas ir peržiūra](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Personalo valdymo parametrų konfigūravimas](hr-setup-parameters.md)<br>
[Bendrai naudojamų Personalo valdymo parametrų konfigūravimas](hr-setup-shared-parameters.md)<br>
[Kas yra „Microsoft Dataverse“?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Naudokite „Microsoft Dataverse“ žiniatinklio API](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
