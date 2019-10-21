---
title: DUK apie „Attract” integravimą su „LinkedIn“
description: Ši tema atsako į klausimus, kurie gali kilti dėl integravimo „LinkedIn” ir „Microsoft Dynamics 365 Talent - Attract” integravimo.
author: hasrivas
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: d66ebc01597f8038a38b46a9f1b70feaa5dc505e
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008644"
---
# <a name="linkedin-integration-faq"></a>DUK apie „LinkedIn‟ integravimą

[!include [banner](includes/banner.md)]

„LinkedIn” yra didžiausias pasaulyje profesionalų internetinis tinklas. „Microsoft Dynamics Talent: Attract” integravimas su „LinkedIn” suteikia jums prieigą prie pasaulio talentingiausiųjų. „Attract” leidžia jums registruoti darbo skelbimus tiesiai į „LinkedIn”, taip pat programa leidžia perkelti kandidatų informaciją iš „LinkedIn” į „Attract”.

## <a name="for-recruiters-and-hiring-managers"></a>Samdos vadovams ir įdarbintojams

Čia rasite atsakymus į dažniausiai užduodamus klausimus apie tai, kaip kartu naudoti „Attract“ ir „LinkedIn“.

### <a name="what-linkedin-features-do-i-get-with-attract"></a>Kokias „LinkedIn“ funkcijas gaunu naudodamas „Attract“?

„Attract“ integravimas su „LinkedIn” leidžia jums atlikti toliau nurodytas užduotis.

- [Registruoti darbo skelbimus „LinkedIn”](./attract-post-jobs-to-linkedin.md) (kaip nemokamus apribotus skelbimus).
- [Eksportuoti kandidatų informaciją iš „LinkedIn” į „Attract”](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [Leisti kandidatams pretenduoti į jūsų darbo vietą naudojant „LinkedIn”](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>Ko reikia, kad galėčiau registruoti darbo skelbimus į „LinkedIn”?

Jūsų administratorius privalo [sukonfigūruoti „LinkedIn” integraciją programoje „Attract”](./attract-admin-linkedin.md#configure-job-posting-to-linkedin). Po nurodytų veiksmų atlikimo, esate pasiruošę pradėti darbą.

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>Kaip registruoti darbo skelbimus „LinkedIn“ iš „Attract“?

Po darbo skelbimo sukūrimo programoje „Attract”, jums tereikia pasirinkti „LinkedIn” atitinkantį mygtuką **Registruoti dabar**. Jei norite gauti daugiau informacijos, žr. [Registruoti darbo skelbimus „LinkedIn” iš „Attract”](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin).

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>Ar galiu perkelti kandidatų informaciją iš „LinkedIn“ į „Attract“?

Taip. Jei „LinkedIn” randate tinkamą kandidatą, galite lengvai eksportuoti kandidato informaciją į „Attract”. Daugiau informacijos žr. [Kandidatų ieška naudojant „LinkedIn Recruiter“](attract-linkedin-recruiter.md).

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>Kaip gauti pagalbos norint prisijungti prie „LinkedIn” iš „Attract”?

Jei jums kyla problemų prisijungiant ar registruojant darbo skelbimus „LinkedIn”, žr. [„LinkedIn” integravimo trikčių diagnostika](./attract-troubleshoot-linkedin.md).

Iškilus kitokioms problemoms, susijusioms su „Attract”, žr. [Pagalba dėl „Talent“](./talent-support.md). Jei reikia pagalbos dėl „LinkedIn”, žr. [„LinkedIn“ palaikymo tarnybos puslapis](https://www.linkedin.com/help).

## <a name="for-admins-and-developers"></a>Administratoriams ir kūrėjams

Čia rasite atsakymus į dažniausiai užduodamus klausimus apie tai, kaip konfigūruoti „Attract“ ir „LinkedIn“ integravimą.

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>Kaip sukonfigūruoti „Attract“, kad darbdaviai ir samdos vadovai galėtų registruoti darbo skelbimus „LinkedIn”?

Galimas parinktis galite konfigūruoti skirtuke **„LinkedIn” integravimas**, esančiame administravimo centre. Daugiau informacijos žr. [Integravimo su „LinkedIn” nustatymas](./attract-admin-linkedin.md).

### <a name="can-i-export-candidate-information-from-linkedin"></a>Ar galima eksportuoti kandidatų informaciją iš „LinkedIn” į „Attract”?

Taip, bet pirmiausia turite sukonfigūruoti integravimą su „LinkedIn Recruiter”. Daugiau informacijos žr. [Integravimo su „LinkedIn” nustatymas](./attract-admin-linkedin.md).

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>Kaip galima registruoti darbo skelbimus į „Premium” darbo vietas tinkle „LinkedIn”?

Nors „Attract“ pateikia efektyvų darbo skelbimų registravimo „LinkedIn” sprendimą, galite pastebėti, kad reikia daugiau lankstumo. Pavyzdžiui, galbūt norėsite registruoti „Premium” darbo vietas kartu su nemokamais apribotais skelbimais arba norėsite, kad „LinkedIn” apdorotų jūsų paketinius darbo skelbimus daugiau nei vieną kartą per dieną.

#### <a name="types-of-linkedin-job-posts"></a>„LinkedIn” darbo skelbimų tipai

„LinkedIn” siūlo toliau nurodytus darbo skelbimų tipus.

- **Apriboti skelbimai** – nemokami darbo skelbimai, rodomi ieškos rezultatuose, kai kandidatai ieško darbo „LinkedIn” tinkle ir įmonės „LinkedIn” puslapyje. Apriboti skelbimai yra skirti aktyviems darbo ieškantiems asmenims. Šio tipo skelbimus „Attract“ teikia „LinkedIn”. „LinkedIn” negalite reklamuoti apribotų darbo skelbimų. Jei norite reklamuoti apribotus skelbimus, turite dirbti su „LinkedIn”, kad įgalintumėte automatinį darbų skelbimą. Daugiau informacijos apie automatinį darbų skelbimą žr. [Apriboti skelbimai palyginti su „Premium“ darbų vietomis naudojant automatinį darbų skelbimą](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping) ir [Automatinio darbų skelbimo DUK](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions).
- **„Premium” darbo vietos** – įsigyti registravimai, rodomi įvairiose „LinkedIn” vietose, pvz., „LinkedIn” informacijos santraukoje, el. laiškuose ir srityje **„Darbai, kurie galbūt jus domintų”**. „Premium” darbo vietos yra skirtos pasyviems kandidatams, bet jos taip pat rodomos darbo paieškose.

„Attract” registruoja darbo skelbimus „LinkedIn” kaip apribotus skelbimus. Jei norite naudoti „Premium” darbo vietas, turite naudoti automatinį darbų skelbimą naudojant „LinkedIn Recruiter”. Automatiniam darbų skelbimui reikalinga automatinio darbų skelbimo sutartis su „LinkedIn”. Daugiau informacijos žr. [Automatinis darbų skelbimas naudojant „LinkedIn Recruiter” – apžvalga](https://www.linkedin.com/help/recruiter/answer/79037).

#### <a name="frequency-of-batch-processing-on-linkedin"></a>Paketinio vykdymo dažnumas „LinkedIn” tinkle

„LinkedIn” apdoroja darbo skelbimus kaip paketinę užduotį vieną kartą per dieną, naudojant „Attract”. Todėl gali užtrukti iki 48 valandų, kol darbo skelbimai bus rodomi „LinkedIn” po to, kai jie užregistruojami naudojant „Attract”. Jei norite, kad darbo skelbimai „LinkedIn” būtų rodomi anksčiau, arba jei jums reikia daugiau lankstumo, galite naudoti „Recruiter System Connect” taikomojo programavimo sąsają (API) iš „LinkedIn”. Daugiau informacijos žr. [„Recruiter System Connect”](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect).

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>Darbo skelbimų registravimo tinkle „LinkedIn” parinkčių lentelė

Toliau nurodomoje lentelėje aprašomos įvairios darbo skelbimų registravimo į „LinkedIn” parinktys. Lentelėje pateikiami kiekvienos parinkties pranašumai ir papildoma informacija.

|  | „Attract“ | Automatinis darbų skelbimas naudojant „LinkedIn Recruiter” | „Recruiter System Connect” API |
|---|---|---|---|
| **Aprašas** | „Attract” registruoja darbo skelbimus „LinkedIn” kaip XML informacijos santrauką. | Įmonė sudaro sutartį su „LinkedIn” ir pateikia XML informacijos santrauką, skirtą darbo skelbimams registruoti. | Klientas naudoja API „Attract” ir „LinkedIn Recruiter” informacijai sinchronizuoti. |
| **Kokio tipo darbo skelbimą galima registruoti?** | Apribotus skelbimus | „Premium” darbo vietas arba apribotus skelbimus | Apribotus skelbimus |
| **Ar galima reklamuoti darbo skelbimą „LinkedIn”?** | Ne | „Premium” darbo vietos: taip<br>Apriboti skelbimai: ne | Ne |
| **Kaip dažnai „LinkedIn” registruoja darbo skelbimus?** | Kartą per parą | Kartą per parą | Kelis kartus per dieną, kaip nustatyta API |
| **Rekomenduoja „LinkedIn”?** | Ne | Taip | Ne |
| **Ko reikia?** | „Attract” įsigijimas | Automatinio darbų skelbimo sutartis su „LinkedIn” ir „Premium” darbo vietų pirkimas | API sutartis su „LinkedIn” | 
| **Kur galima rasti daugiau informacijos?** | [Integravimo su „LinkedIn“ nustatymas](./attract-admin-linkedin.md) | [Automatinis darbų skelbimas naudojant „LinkedIn Recruiter” – apžvalga](https://www.linkedin.com/help/recruiter/answer/79037) | [„Recruiter System Connect”](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> Jums nereikia „LinkedIn Recruiter System Connect“ licencijos, kad būtų galima registruoti darbo skelbimus „LinkedIn” naudojant „Attract”.

## <a name="see-also"></a>Taip pat žiūrėkite

[Integravimo su „LinkedIn“ nustatymas](./attract-admin-linkedin.md)

[Darbo skelbimų registravimas „LinkedIn“ iš „Attract“](./attract-post-jobs-to-linkedin.md)

[Kandidatų ieška naudojant „LinkedIn Recruiter”](./attract-linkedin-recruiter.md)

[Integravimo su „LinkedIn“ trikčių diagnostika](./attract-troubleshoot-linkedin.md)
