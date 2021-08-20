---
title: Reiso būsenos nustatymas
description: Šioje temoje aprašoma, kaip nustatyti būsenos reikšmes, kurias vartotojai gali priskirti reisams.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 994ce5245ce36a3d063782aff738e752d33c8cc91b438b9dc683eedbd7f13a5a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760495"
---
# <a name="voyage-status-setup"></a>Reiso būsenos nustatymas

[!include [banner](../../includes/banner.md)]

Puslapyje **Reiso būsenos** jūs nustatote būsenos reikšmių, kurias vartotojai gali priskirti reisams, rinkinį. Vartotojai gali priskirti reiso būsenos reikšmes visiems reiso lygiams: reisui, gabenimo konteineriui, registracijai, pirkimo užsakymui ir prekei (pirkimo eilutėms ir perkėlimo užsakymo eilutėms). Jos yra naudojamos dviem tikslais:

- Informuoti vartotoją apie reiso, gabenimo konteinerio, registracijos, pirkimo užsakymo arba prekės (pirkimo eilučių ir perkėlimo užsakymo eilučių) būseną.
- Apriboti išlaidų srities naudojimą užkertant kelią modifikavimui arba naikinimui.

Norėdami nustatyti savo reiso būsenas, eikite į **Įkeltos išlaidos \> Nustatymas \> Reiso būsenos**. Ten galite įtraukti, pašalinti ir redaguoti būsenas naudodami veiksmų srities mygtukus.

Kiekviena išlaidų sritis turi nuosavą reiso būsenų rinkinį ir hierarchiją. Taigi, puslapio **Reiso būsenos** lauke **Išlaidų sritis** pirmiausia turite pasirinkti išlaidų sritį, kuriai norite peržiūrėti ar sukurti reiso būsenas. Tada, kiekvienai reiso būsenai nustatykite laukus, aprašytus toliau pateikiamoje lentelėje, kaip reikalaujama. Atkreipkite dėmesį, kad reiso būseną taip pat gali automatiškai pakeisti sistemos įvykiai, pavyzdžiui, taisyklės, kurios buvo nustatytos naudojant sekimo kontrolės centrą.

| Laukas | Aprašymas |
|---|---|
| Reiso būsena | Įvesti reiso būsenos pavadinimą. |
| Aprašymas | Įveskite reiso būsenos aprašą. |
| Modifikuoti | Pasirinkite šį žymės langelį, jeigu vartotojams leidžiama modifikuoti šios būsenos reisus. |
| Panaikinti | Pasirinkite šį žymės langelį, jeigu vartotojams leidžiama panaikinti šios būsenos reisus. |
| Privalomas | Pasirinkite šį žymės langelį, jei norite padaryti reiso būseną privaloma, kad jo nebūtų galima praleisti. |
| Pirminis | Naudokite šį lauką hierarchijos tarp būsenos reikšmių nustatymui. Reiso būsenos gali būti pakeistos (rankiniu arba automatiniu būdu) tik į žemesnę hierarchijos pakopą, nuo pirminės būsenos iki vienos iš jos antrinių būsenų.

> [!NOTE]
> Jūs turite nustatyti tik konkrečias reiso būsenas, kurias naudoja jūsų organizacija. Įprastos reiso būsenos yra *Patvirtinta*, *Prekės tranzite*, *Gauta*, *Paruošta įkainojimui* ir *Įkainota*. Tačiau gali būti ir kitokių būsenų.
