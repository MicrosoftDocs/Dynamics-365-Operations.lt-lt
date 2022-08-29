---
title: Patarimai dėl atsargų matomumo
description: Šiame straipsnyje pateikiami keli patarimai, į kuriuos turėtumėte atsižvelgti nustatant ir naudojant atsargų matomumo priedą.
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
ms.openlocfilehash: 3bdd161815a15d5c39b3c0afc176a288c8d9055a
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306092"
---
# <a name="inventory-visibility-tips"></a>Patarimai dėl atsargų matomumo

[!include [banner](../includes/banner.md)]

Štai keli patarimai, į kuriuos turėtumėte atsižvelgti nustatant ir naudojant atsargų matomumo priedą:

- Šiuo metu atsargų matomumo priedas palaiko tik aplinkas Microsoft Dataverse, kurios sukurtos Microsoft Dynamics naudojant ciklo tarnybas (LCS). Jei jūsų Dataverse aplinka buvo sukurta kokiu nors kitu būdu (pavyzdžiui, Power Apps naudojant administravimo centrą) Dynamics 365 Supply Chain Management ir jei ji susieta su jūsų aplinka, pirmiausia turite paprašyti atsargų matomumo produkto komandos išspręsti susiejimo problemą. Galite susisiekti su komanda šiuo [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Komanda leis jums žinoti, kada jūsų aplinka parengta įdiegti atsargų matomumą.
- Jei turite daugiau nei vieną LCS aplinką, kiekvienai aplinkai sukurkite Azure Active Directory kitą (Azure AD) programą. Jei norėdami įdiegti atsargų matomumo priedą skirtingoms aplinkai naudojate tą patį programos ID ir nuomininko ID, atpažinimo ženklo išdavimas bus taikomas senesnėms aplinkai. Galioja tik paskutinis įdiegto atsargų matomumo priedo egzempliorius.
- Šiuo metu atsargų matomumas nepalaikomas debesyje laikomose aplinkose. Jis palaikomas tik Tier-2+ aplinkose.
- Programos programavimo sąsaja (API) šiuo metu palaiko užklausas iki 100 atskirų prekių pagal `ProductID` vertę. Šioje `SiteID` užklausoje `LocationID` dar galima nurodyti keletą verčių. Maksimali riba apibrėžiama kaip `NumOf(SiteID) * NumOf(LocationID) <= 100`.
- Masinis API gali pateikti ne daugiau kaip 512 kiekvienos užklausos įrašų.
- Duomenų `fno` šaltinis rezervuotas tiekimo grandinės valdymui. Jei jūsų atsargų matomumo priedas yra integruotas `fno`[tiekimo grandinės valdymo aplinkoje, rekomenduojame nenaiknti su duomenų šaltiniu susijusių konfigūracijų](inventory-visibility-configuration.md#data-source-configuration).
- Atsargų matomumas negali keisti jokių duomenų šaltinio `fno` duomenų. Duomenų srautas yra vien way, o tai reiškia, kad visi `fno` duomenų šaltinio kiekio pakeitimai turi būti gauti iš jūsų tiekimo grandinės valdymo aplinkos. Todėl negalite naudoti API, norėdami siųsti turimos informacijos keitimo ar rezervavimo užklausas duomenų `fno` šaltiniui.
- Jei į savo tiekimo grandinės valdymo aplinką įtraukiate vieną ar daugiau naujų priemonių, turėtumėte įtraukti juos ir į atsargų matomumą. Tačiau visi naujų priemonių kiekio pakeitimai turi būti atlikti iš jūsų tiekimo grandinės valdymo aplinkos.
- Šiuo [metu skaidinio](inventory-visibility-configuration.md#partition-configuration) konfigūraciją sudaro dvi pagrindinės dimensijos (`SiteId` ir `LocationId`), kurios nurodo, kaip paskirstomi duomenys. To paties skaidinio operacijos gali padidinti našumą už mažesnes išlaidas. Sprendimas apima šio skaidinio konfigūraciją pagal numatytuosius nustatymus. *Todėl jums nereikia jų patiems nurodyti*. Nepritaikykite numatytosios skaidinio konfigūracijos. Jei jį panaikinsite arba pakeisite, tikėtina, kad įvyko netikėta klaida.
- Pagrindinės dimensijos, kurios nustatytos skaidinio konfigūracijoje, neturėtų būti apibrėžtos produkto indekso [hierarchijos konfigūracijoje](inventory-visibility-configuration.md#index-configuration).
- Jūsų [produktų indeksų](inventory-visibility-configuration.md#index-configuration) hierarchijos konfigūracijoje turi būti bent viena indeksų hierarchija (pvz., `Empty` kurioje yra pagrindinė dimensija), kitu atveju užklausų atlikti nepavyks, nes bus klaida "Nenustatyta indekso hierarchija".
- Duomenų šaltinis yra `@iv` iš anksto nustatytas duomenų šaltinis, o su prefiksu `@iv` apibrėžti faktiniai duomenys yra `@` iš anksto nustatyti duomenys. Šios priemonės yra iš anksto nustatyta paskirstymo funkcijos konfigūracija, todėl nekeiskite jų ar nenaikykite jų arba, tikėtina, kad įvyksta netikėtos klaidos naudojant paskirstymo funkciją.
- Galite pridėti naujų faktinių matų prie iš anksto apskaičiuoto matavimo `@iv.@available_to_allocate`, tačiau jo pavadinimo keisti negalima.
- Atkūrus tiekimo grandinės valdymo duomenų bazę, atkurtoje duomenų bazėje gali būti duomenų, kurie nebeatitinka anksčiau atsargų matomumo sinchronizuotų duomenų Dataverse. Dėl šių duomenų nenuoseklumo gali kilti sistemos klaidų ir kitų problemų. Todėl svarbu prieš atkurdami Dataverse tiekimo grandinės valdymo duomenų bazę visada išvalyti visus susijusius atsargų matomumo duomenis. Norėdami gauti daugiau informacijos, [prieš atkurdami Dataverse tiekimo grandinės valdymo duomenų bazę, išvalykite atsargų matomumo duomenis](inventory-visibility-setup.md#restore-environment-database).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
