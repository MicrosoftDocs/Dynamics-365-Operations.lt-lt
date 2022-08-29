---
title: Darbo laiko kalendoriaus kūrimas
description: Darbo laiko kalendoriaus, šventinių dienų ir ne darbo laiko nustatymas programoje „Dynamics 365 Human Resources“.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dac3ad583be9e4cbd6eacbc6d228819bd298628b
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323580"
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
   - Norėdami įtraukti ne darbo laiką, pvz., priešpite ar pertraukas, **·** **pasirinkite Įtraukti dalyje Ne** darbo laikas ir įveskite pavadinimą bei laiko intervalą.

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
