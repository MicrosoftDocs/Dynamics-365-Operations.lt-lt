---
title: Įjungti kiekio ir neatitikties valdymą
description: Šioje temoje pateikiama kokybės ir neatitikties valdymo funkcijų nustatymo ir konfigūravimo proceso „Microsoft Dynamics 365 Supply Chain Management“ apžvalga.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2c8b7e9a1a8d7692e1d2215e38de1b0f4d2d82
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567420"
---
# <a name="enable-quality-and-nonconformance-management"></a>Įjungti kiekio ir neatitikties valdymą

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama kokybės ir neatitikties valdymo funkcijų nustatymo ir konfigūravimo proceso „Microsoft Dynamics 365 Supply Chain Management“ apžvalga.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>Įjungti kiekio ir neatitikties valdymą

Norėdami įjungti kokybės valdymą sistemoje, atlikite šiuos veiksmus.

1. Eikite į **Atsargų valdymas\> Sąranka \> Atsargų ir sandėlio valdymo parametrai**.
1. Skirtuke **Kokybės** valdymas nustatykite parinktį Naudoti kokybės valdymą **kaip** *Taip*.
1. Lauke **Valandinis tarifas** įveskite valandinį darbo tarifą vietine valiuta. Valandinis tarifas naudojamas apskaičiuojant su neatitikimu susijusias operacijų išlaidas. Valandinis tarifas ir apskaičiuotos išlaidos suteikia nuorodinės informacijos apie neatitiktį. Jie nesąveikauja su kitomis funkcijomis.
1. Rinkitės **Ataskaitos nustatymas**.
1. Pridėti naujų eilučių įvairiems ataskaitų tipams ir pasirinkti dokumento tipą, kuris bus naudojamas kiekvienoje ataskaitoje.
1. Uždarykite puslapį.
1. Uždarykite puslapį.

## <a name="quality-management-configuration-process"></a>Kokybės valdymo konfigūravimo procesas

Prieš pradėdami naudoti kokybės valdymo funkcijas ir generuoti kokybės užsakymus, turite sukonfigūruoti sistemą ir būtinuosius komponentus. Čia pateikiamas veiksmų, kurių reikia norint konfigūruoti kokybės valdymą, sąrašas.

1. [Įjungti kiekio ir neatitikties valdymą](#enable-qm).
1. Pasirinktinai: [konfigūruokite bandymo](quality-test-instruments.md) priemones.
1. [Tarifų konfigūravimas](quality-tests.md).
1. [Konfigūruokite bandymo kintamuosius ir](quality-test-variables.md) rezultatus.
1. [Konfigūruoti bandymų](quality-test-groups.md) grupes.
1. Pasirinktinai: [konfigūruokite kokybės grupes ir sąsają su](quality-groups.md) produktais.
1. Pasirinktinai: [sukonfigūruokite kokybės](quality-associations.md) susiejimus.

Baigę konfigūruoti galite pradėti kurti ir apdoroti kokybės užsakymus. Daugiau informacijos apie tai, kaip kurti ir dirbti su kokybės užsakymais rasite [Kokybės užsakymai](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Neatitikties valdymo konfigūravimo procesas

Prieš pradėdami naudoti neatitikties valdymo funkcijas ir generuoti neatitikties užsakymus, turite sukonfigūruoti sistemą ir būtinuosius komponentus. Čia pateikiamas veiksmų, kurių reikia norint konfigūruoti neatitikties valdymą, sąrašas.

1. [Įjungti kiekio ir neatitikties valdymą](#enable-qm).
1. [Konfigūruoti darbuotojus, atsakingus už neatitikties](quality-responsible-workers.md) tvirtinimą.
1. [Konfigūruokite problemų](quality-problem-types.md) tipus.
1. [Konfigūruokite sulaikymo](quality-quarantine-zones.md) zonas.
1. [Konfigūruoti diagnostinius tipus](quality-diagnostic-types.md).
1. [Operacijų konfigūravimas](quality-operations.md).
1. Pasirinktinai: [sukonfigūruokite kokybės](quality-charges.md) mokesčius.

Baigę konfigūruoti galite pradėti kurti ir apdoroti neatitikties užsakymus. Daugiau informacijos apie tai, kaip kurti ir dirbti su neatitikimais, žr. dalį [Neatitikčių kūrimas ir darbas su jomis](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Papildomi ištekliai

- [Kokybės valdymo apžvalga](quality-management-processes.md)
- [Įjungti kiekio ir neatitikties valdymą](enable-quality-management.md)
- [Sandėlio procesų kokybės valdymas](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
