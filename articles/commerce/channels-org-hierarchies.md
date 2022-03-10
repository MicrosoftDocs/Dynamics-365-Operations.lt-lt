---
title: Organizacijų hierarchijų nustatymas
description: Šioje temoje aprašoma, kaip nustatyti „Microsoft Dynamics 365 Commerce“ organizacijos hierarchijas.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ce0732f32a9a80fc5b0ede7ae9f1c1ab9a68a89b2fb0b1821cb5df123ca5ca4a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746021"
---
# <a name="set-up-organization-hierarchies"></a>Organizacijų hierarchijų nustatymas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip nustatyti „Microsoft Dynamics 365 Commerce“ organizacijos hierarchijas.

Prieš kurdami kanalus turite įsitikinti, kad jums reikia nustatyti organizacijos hierarchijas.

Naudodami organizacijos hierarchijas galite peržiūrėti informaciją apie įvairius savo įmonės aspektus ir sukurti atitinkamas ataskaitas. Pavyzdžiui, galite nustatyti vieną hierarchiją, skirtą mokesčių, juridinėms arba privalomoms ataskaitoms kurti. Tada galite nustatyti kitą hierarchiją, kad būtų kuriamos finansinės informacijos, kurios nebūtina pateikti, bet kuri naudojama vidaus ataskaitose, ataskaitos.

Prieš kurdami organizacijos hierarchiją turite sukurti organizacijas. Daugiau informacijos žr. [Juridinių subjektų kūrimas](channels-legal-entities.md) arba [Valdymo vienetų kūrimas](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Daugiau informacijos ieškokite šiose temose.
- [Organizacijų ir organizacijų hierarchijų apžvalga](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [Organizacijos hierarchijos planavimas](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [Organizacijos hierarchijos kūrimas](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Organizacijos hierarchijos kūrimas

Norėdami sukurti organizacijos hierarchiją, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje eikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Organizacijos hierarchijos**.
1. Veiksmų srityje pasirinkite **Nauja**.
1. Lauke **Pavadinimas** įveskite reikšmę.
1. Skyriuje **Tikslas** pasirinkite **Priskirti tikslą**.
1. Sąraše raskite ir pasirinkite norimą įrašą. Pasirinkite paskirtį, priskirtiną jūsų organizacijos hierarchijai.
1. Skyriuje **Priskirtos hierarchijos** pasirinkite **Įtraukti**.
1. Sąraše pažymėkite pasirinktą eilutę. Suraskite ką tik savo sukurtą hierarchiją.
1. Pasirinkite **Gerai**.

Toliau pateiktame paveiksle rodomas organizacijos hierarchijos, sukurtos fiktyviam „Adventure Works“ parduotuvių tinklui, pavyzdys.

![Organizacijos hierarchijos pavyzdys.](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Organizacijų įtraukimas į hierarchiją

Norėdami įtraukti organizacijas į hierarchiją, atlikite toliau nurodytus veiksmus.

1. Sąraše raskite ir pasirinkite norimą įrašą. Pasirinkite savo hierarchiją.
1. Veiksmų srityje pasirinkite **Peržiūrėti**.
1. Pagal poreikį įtraukite organizacijų.
1. Norėdami įtraukti organizaciją, pasirinkite **Redaguoti** ir pasirinkite **Įterpti**. Atlikę visus norimus pakeitimus, galite įrašyti juodraštį ir publikuoti pakeitimus.

Toliau pateiktame paveiksle rodomas juridinis subjektas, įtrauktas į hierarchijos šaknį su keturiais išlaidų centrais, skirtais kanalams „Prekybos centras“, „Parduotuvė“, „Internetinė parduotuvė“ ir „Skambučių centras“. Po to į kiekvieną galima įtraukti įvairius mažmeninės prekybos, skambučių centro ir internetinės parduotuvės kanalus.

![Hierarchijos konstruktoriaus pavyzdys.](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[Organizacijų ir organizacijų hierarchijų apžvalga](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organizacijos hierarchijos planavimas](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Juridinių subjektų kūrimas](channels-legal-entities.md)

[Valdymo vienetų kūrimas](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Kanalų apžvalga](channels-overview.md)

[Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
