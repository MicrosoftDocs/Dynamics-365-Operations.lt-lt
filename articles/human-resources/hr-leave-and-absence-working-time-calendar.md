---
title: Darbo laiko kalendoriaus kūrimas
description: Darbo laiko kalendoriaus, šventinių dienų ir ne darbo laiko nustatymas programoje „Dynamics 365 Human Resources“.
author: andreabichsel
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8ea55ad7f86e0c7d5ccc6e6de0af475299b05639
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052438"
---
# <a name="create-a-working-time-calendar"></a>Darbo laiko kalendoriaus kūrimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Darbo laiko kalendoriuje programoje „Dynamics 365 Human Resources“ rodomos dienos ir valandos, kurias darbuotojai dirba jūsų organizacijoje. Pateikdamas atostogų užklausą, darbuotojas neturi nerimauti dėl švenčių ir nedarbo dienų.

Norėdami racionalizuoti atostogų užklausas, konfigūruokite šiuos elementus savo organizacijoje:

- Darbo laiko kalendorius
- Šventės ir nedarbo dienos
- Ne darbo laikas

Nustatydami darbo laiko kalendorių, galite pridėti paskutinius du elementus. Taip pat galite juos konfigūruoti arba atnaujinti atskirai.

## <a name="set-up-a-working-time-calendar"></a>Darbo laiko kalendoriaus nustatymas

Nustatykite bent vieną darbo kalendorių, kuriame parodytos darbo dienos ir valandos. Jeigu jūsų darbo vietos yra keliose šalyse ir regionuose, galite nustatyti kiekvienos vietos darbo laiko kalendorių.

1. Puslapyje **Organizacijos administravimas** pasirinkite **Kalendorius**.

2. Pasirinkite **Naujas** ir įveskite kalendoriaus pavadinimą bei aprašą.

3. Dalyje **Generavimo pasirinktys** pasirinkite savo organizacijos darbo dienas ir įveskite darbo laiką. 
   - Norėdami pridėti švenčių ar nedarbo dienų, pasirinkite šalia dalies **Šventės ir darbo dienos** esantį mygtuką **Pridėti**.
   - Norėdami pridėti ne darbo laiką, pvz., pietus arba pertraukas, pasirinkite **Pridėti** dalyje **NE DARBO LAIKAS** ir įveskite pavadinimą ir laiko intervalą.

4. Dalyje **Dienos** pasirinkite **Generuoti**, kad sugeneruotumėte dienų kalendorių. Įveskite kalendoriaus datų intervalą, tada pasirinkite **Generuoti dienas**.

5. Norėdami pridėti darbo grafikus, dalyje **Darbo grafikas** pasirinkite **Pridėti** ir įveskite kiekvieno darbo grafiko laiką.

## <a name="configure-holidays-and-closures"></a>Švenčių ir nedarbo dienų konfigūravimas

Galite pridėti arba keisti šventes ir nedarbo dienas atskirai nuo darbo laiko kalendoriaus.

1. Puslapyje **Organizacijos administravimas** pasirinkite **Šventės ir nedarbo dienos**.

2. Pasirinkite **Nauja** ir įveskite šventės ar nedarbo dienos pavadinimą bei datą.

## <a name="configure-non-work-time"></a>Ne darbo laiko konfigūravimas

Galite pridėti arba keisti ne darbo laiką atskirai nuo darbo laiko kalendoriaus.

1. Puslapyje **Organizacijos administravimas** pasirinkite **Ne darbo laikas**.

2. Pasirinkite **Naujas** ir įveskite ne darbo laiko pavadinimą bei laiko intervalą.

Jeigu įgalinote atostogų ir neatvykimų koregavimų peržiūros funkciją, „Human Resources“ naudoja atostogų ir nedarbo dienų datas, kad nustatytų dienų, kurias reikia koreguoti kalendoriuje užregistruotiems darbuotojams, skaičių.

## <a name="see-also"></a>Taip pat žiūrėkite

- [Atostogų ir neatvykimų apžvalga](hr-leave-and-absence-overview.md)
- [Atostogų ir neatvykimų tipai konfigūravimas](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]