---
title: Įsigijimo ir šaltinio pasirinkimo darbo eigos
description: Kai kurios organizacijos reikalauja, kad pirkimo paraiškas ir pirkimo užsakymus patvirtintų ne operaciją įvedęs vartotojas. Jei norite nustatyti patvirtinimo procesą, galite sukurti darbo eigą.
author: kamaybac
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 126e9969f312ff7f6a6c64b733708754e7659214
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909236"
---
# <a name="procurement-and-sourcing-workflows"></a>Paraiškų darbo eigos

[!include [banner](../includes/banner.md)]

Kai kurios organizacijos reikalauja, kad pirkimo paraiškas ir pirkimo užsakymus patvirtintų ne operaciją įvedęs vartotojas. Jei norite nustatyti patvirtinimo procesą, galite sukurti darbo eigą.

Darbo eiga rodo verslo procesą. Ji nustato dokumento kelią sistemoje ir parodo, kas turi atlikti užduotį arba patvirtinti dokumentą. Darbo eigos sistemos naudojimas jūsų organizacijoje duoda keleriopos naudos:

- **Procesų nuoseklumas** — galite nustatyti konkrečių dokumentų, pvz., pirkimo paraiškų ir išlaidų ataskaitų, patvirtinimo procesą. Darbo eigos sistemos naudojimas padeda užtikrinti, kad dokumentai bus apdoroti ir patvirtinti nuosekliai ir veiksmingai.
- **Proceso matomumas** — galite sekti konkretaus darbo eigos egzemplioriaus efektyvumo metriką. Tai padeda nustatyti, ar reikia atlikti darbo eigos pokyčius, siekiant gerinti efektyvumą.
- **Centralizuotas darbų sąrašas**– vartotojai norėdami sužinoti darbo eigos užduotis ir patvirtinimus, jiems priskirtus visose darbo eigose, kuriose jie dalyvauja, gali peržiūrėti centralizuotų darbų sąrašą. Tai galima padaryti puslapyje Darbo elementai.

## <a name="the-types-of-workflows-that-you-can-create"></a>Darbo eigų tipai, kuriuos galite sukurti

Įsigijimo ir šaltinio pasirinkimo procese galima naudoti toliau išvardintų tipų darbo eigas.

| Tipas | Naudokite šį tipą norėdami |
|---|---|
| Pirkimo paraiškos peržiūra | Kurkite pirkimo paraiškų peržiūros ir patvirtinimo darbo eigas. |
| Pirkimo paraiškos eilutės peržiūra | Kurkite pirkimo paraiškų eilučių peržiūros ir patvirtinimo darbo eigas. |
| Pirkimo užsakymo darbo eiga | Kurkite peržiūros ir patvirtinimo darbo eigas pirkimo užsakymams. |
| Pirkimo užsakymo eilutės darbo eiga | Kurkite peržiūros ir patvirtinimo darbo eigas pirkimo užsakymų eilutėms. |
| Tiekėjo įtraukimo prašymo darbo eiga | Kurkite naujų tiekėjų įtraukimo naudojant tiekėjo užklausas peržiūros ir patvirtinimo darbo eigas. |

> [!IMPORTANT]
> Jums įtraukiant naują darbo eiga, galite taip pat matyti tolesnes nebeveikiančias darbo eigas sąraše **Sukurti darbo eigą** teksto laukelyje. Jos yra susijusios su *gavimo patvirtinimo* funkcija, kuri buvo prieinama [„Dynamics AX“ 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), bet dabar nebegalioja. Šios darbo eigos dabar jau nebepalaikomos.
> 
> - Pristatymo termino pranešimo darbo eiga
> - Pranešimo apie SF gavimą darbo eiga
> - Gavimo dokumentas neatitiko pranešimo darbo eigos.
> - Pranešimo apie nepatvirtinto gavimo dokumento atmetimą darbo eiga

## <a name="creating-a-workflow"></a>Darbo eigos kūrimas

Norėdami kurti darbo eigą, pasirinkite Įsigijimas ir šaltinio pasirinkimas &gt; Nustatymas &gt; Įsigijimo ir šaltinio pasirinkimo darbo eigos ir sukurkite naują darbo eigą, pasirinkdami norimą darbo eigos tipą. 

Darbo eigos srityje darbo eigos elementus galite nuvilkti į kūrimo priemonę ir susieti elementus su eiga. Darbo eigos elementai turi būti sukonfigūruoti. Konfigūruodami patvirtinimo ir užduoties darbo eigos elementus galite nustatyti, kuris dalyvis turėtų atlikti veiksmą.

## <a name="types-of-participants"></a>Dalyvių tipai

Galite priskirti patvirtinimo veiksmą toliau nurodytoms dalyvių grupėms.

| Vartotojų grupė | Prekės/Paslaugos pavadinimas |
|---|---|
| Dalyvis | Priskirkite patvirtinimo veiksmą grupės arba vaidmens nariams. |
| Hierarchija | Priskirkite patvirtinimo veiksmą konkrečios organizacijos hierarchijos vartotojams. |
| Darbo eigos vartotojas | Priskirkite patvirtinimo veiksmą šios darbo eigos vartotojams. |
| Darbo grupė | Priskirti patvirtinimo veiksmą darbo elementų eilei. |
| Vartotojas | Priskirkite patvirtinimo veiksmą konkretiems vartotojams. |

## <a name="additional-resources"></a>Papildomi ištekliai

- [Pirkimo paraiškų verslo procesų darbo eigų nustatymas](https://www.microsoft.com/download/details.aspx?id=101821)
- [Pirkimo paraiškos darbo eiga](purchase-requisitions-workflow.md)
- [Tiekėjų supažindinimas](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]