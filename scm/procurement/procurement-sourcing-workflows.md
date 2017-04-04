---
title: "Įsigijimo ir šaltinio pasirinkimo darbo eigos"
description: "Kai kurios organizacijos reikalauja, kad pirkimo paraiškas ir pirkimo užsakymus patvirtintų ne operaciją įvedęs vartotojas. Jei norite nustatyti patvirtinimo procesą, galite sukurti darbo eigą."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 27c211e6ded17e085559add916c28a48c40e5b8e
ms.lasthandoff: 03/31/2017


---

# <a name="procurement-and-sourcing-workflows"></a>Paraiškų darbo eigos

Kai kurios organizacijos reikalauja, kad pirkimo paraiškas ir pirkimo užsakymus patvirtintų ne operaciją įvedęs vartotojas. Jei norite nustatyti patvirtinimo procesą, galite sukurti darbo eigą.

Darbo eiga rodo verslo procesą. Ji nustato dokumento kelią sistemoje ir parodo, kas turi atlikti užduotį arba patvirtinti dokumentą. Darbo eigos sistemos naudojimas jūsų organizacijoje duoda keleriopos naudos:
-   **Procesų nuoseklumas** — galite nustatyti konkrečių dokumentų, pvz., pirkimo paraiškų ir išlaidų ataskaitų, patvirtinimo procesą. Darbo eigos sistemos naudojimas padeda užtikrinti, kad dokumentai bus apdoroti ir patvirtinti nuosekliai ir veiksmingai.
-   **Proceso matomumas** — galite sekti konkretaus darbo eigos egzemplioriaus efektyvumo metriką. Tai padeda nustatyti, ar reikia atlikti darbo eigos pokyčius, siekiant gerinti efektyvumą.
-   **Centralizuotas darbų sąrašas**— vartotojai gali peržiūrėti centralizuotas darbų sąraše, Norėdami peržiūrėti darbo eigos užduočių ir jiems priskirtas visoje jie dalyvauja visos darbo eigos patvirtinimus. Tai yra darbo elementus puslapyje.

## <a name="the-types-of-workflows-that-you-can-create"></a> Darbo eigų tipai, kuriuos galite sukurti
Įsigijimo ir šaltinio pasirinkimo procese galima naudoti toliau išvardintų tipų darbo eigas.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Tipas**                         | **Naudokite šį tipą norėdami**                                          |
| Pirkimo paraiškos peržiūra      | Kurkite peržiūros darbo eigas pirkimo paraiškoms.            |
| Pirkimo paraiškos eilutės peržiūra | Kurkite peržiūros darbo eigas pirkimo paraiškų eilutėms.       |
| Pirkimo užsakymo darbo eiga          | Kurkite peržiūros ir patvirtinimo darbo eigas pirkimo užsakymams.     |
| Pirkimo užsakymo eilutės darbo eiga     | Kurkite peržiūros ir patvirtinimo darbo eigas pirkimo užsakymų eilutėms. |

## <a name="creating-a-workflow"></a>Darbo eigos kūrimas
Norėdami sukurti darbo eigą, eikite į pirkimo ir apsirūpinimo &gt;nustatymo &gt;pirkimo ir apsirūpinimo darbo eigos ir sukurti naują darbo eigą, pasirinkę kuriamo darbo eigos tipą.  

Darbo eigos srityje darbo eigos elementus galite nuvilkti į kūrimo priemonę ir susieti elementus su eiga. Darbo eigos elementai turi būti sukonfigūruoti. Konfigūruodami patvirtinimo ir užduoties darbo eigos elementus galite nustatyti, kuris dalyvis turėtų atlikti veiksmą.
Dalyvių tipai
----------------------

Galite priskirti patvirtinimo veiksmą toliau nurodytoms dalyvių grupėms.

| Vartotojų grupė    | Prekės/Paslaugos pavadinimas                                                               |
|---------------|---------------------------------------------------------------------------|
| Dalyvis   | Priskirkite patvirtinimo veiksmą grupės arba vaidmens nariams.                   |
| Hierarchija     | Priskirkite patvirtinimo veiksmą konkrečios organizacijos hierarchijos vartotojams. |
| Darbo eigos vartotojas | Priskirkite patvirtinimo veiksmą šios darbo eigos vartotojams.                       |
| Darbo grupė         | Priskirti patvirtinimo veiksmą darbo elementų eilei.                            |
| Vartotojas          | Priskirkite patvirtinimo veiksmą konkretiems vartotojams.                               |



<a name="see-also"></a>Taip pat žiūrėkite
--------

[Pirkimo paraiškų verslo procesų darbo eigų nustatymas](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Purchase requisition workflow](purchase-requisitions-workflow.md)


