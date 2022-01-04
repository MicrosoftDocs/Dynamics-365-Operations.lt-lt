---
title: Atsargų matomumo patarimai
description: Šioje temoje pateikiami keli patarimai, į kuriuos turėtumėte atsižvelgti nustatant ir naudojant atsargų matomumo priedą.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f5fb4c7cb941b352bbc6e2fcf5347244e1c8a40c
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920859"
---
# <a name="inventory-visibility-tips"></a>Atsargų matomumo patarimai

[!include [banner](../includes/banner.md)]

Štai keli patarimai, į kuriuos turėtumėte atsižvelgti nustatant ir naudojant atsargų matomumo priedą:

- Šiuo metu atsargų matomumo priedas palaiko tik aplinkas, kurios sukurtos naudojant ciklo Microsoft Dataverse Microsoft Dynamics tarnybas (LCS). Jei jūsų aplinka buvo sukurta kokiu nors kitu būdu (pavyzdžiui, naudojant administravimo centrą) ir jei ji susieta su jūsų aplinka, pirmiausia turite paprašyti atsargų matomumo produkto komandos išspręsti susiejimo Dataverse Power AppsDynamics 365 Supply Chain Management problemą. Galite susisiekti su komandos darbuotojais [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Komanda leis jums žinoti, kada jūsų aplinka parengta įdiegti atsargų matomumą.
- Jei turite daugiau nei vieną LCS aplinką, kiekvienai aplinkai sukurkite Azure Active Directory Azure AD kitą () programą. Jei norėdami įdiegti atsargų matomumo priedą skirtingoms aplinkai naudojate tą patį programos ID ir nuomininko ID, atpažinimo ženklo išdavimas bus taikomas senesnėms aplinkai. Galioja tik paskutinis įdiegto atsargų matomumo priedo egzempliorius.
- Šiuo metu atsargų matomumas nepalaikomas debesyje laikomose aplinkose. Jis palaikomas tik Tier-2+ aplinkose.
- Programos programavimo sąsaja (API) šiuo metu palaiko užklausas iki 100 atskirų prekių pagal `ProductID` vertę. Šioje `SiteID``LocationID` užklausoje dar galima nurodyti keletą verčių. Maksimali riba apibrėžiama kaip `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Duomenų `fno` šaltinis rezervuotas tiekimo grandinės valdymui. Jei jūsų atsargų matomumo priedas yra integruotas tiekimo grandinės valdymo aplinkoje, rekomenduojame nenaiknti su duomenų šaltiniu `fno`[susijusių konfigūracijų.](inventory-visibility-configuration.md#data-source-configuration)
- Šiuo [metu](inventory-visibility-configuration.md#partition-configuration) skaidinio konfigūraciją sudaro dvi pagrindinės dimensijos `SiteId``LocationId` (ir), kurios nurodo, kaip paskirstomi duomenys. To paties skaidinio operacijos gali padidinti našumą už mažesnes išlaidas. Sprendimas apima šio skaidinio konfigūraciją pagal numatytuosius nustatymus. Todėl *jums nereikia jų patiems nurodyti*. Nepritaikykite numatytosios skaidinio konfigūracijos. Jei jį panaikinsite arba pakeisite, tikėtina, kad įvyko netikėta klaida.
- Pagrindinės dimensijos, kurios nustatytos skaidinio konfigūracijoje, neturėtų būti apibrėžtos produkto [indekso hierarchijos konfigūracijoje.](inventory-visibility-configuration.md#index-configuration)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
