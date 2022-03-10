---
title: DUK apie darbo eigas
description: Šioje temoje atsakoma į dažnai užduodamus klausimus apie darbo eigos sistemą.
author: ChrisGarty
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e9e2000684081035f35ea55e1c773a4f6976d74
ms.sourcegitcommit: 967b93bb42413b5b38b817f924015468312a93a0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/01/2022
ms.locfileid: "8370885"
---
# <a name="workflow-faq"></a>DUK apie darbo eigas

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Šioje temoje atsakoma į dažnai užduodamus klausimus apie darbo eigos sistemą.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Kodėl gaunami keli pranešimai, kai atmetamas darbo elementas?
Kai atmetamas darbo elementas, tas darbo elementas užbaigiamas kaip atmestas. Sukuriamas kitas darbo elementas ir priskiriamas iniciatoriui. Tai reiškia, kad iniciatorius gaus pranešimą apie atmestą darbo elementą, taip pat atskiras pranešimas bus išsiųstas vartotojui, kuris priskirtas naujam darbo elementui „reikalaujama keisti“. 

Kiekvienas pranešimas skirtas skirtingam darbo elementui, tačiau dėl panašumų gali kilti painiava. Ieškome būdų, kaip šią situaciją išspręsti būsimuose leidimuose.

## <a name="why-are-my-workflow-exports-failing"></a>Kodėl man nepavyksta eksportuoti darbo eigos?
Šiuo metu darbo eigos eksportavimo funkcija yra ribojama darbo eigos pavadinimams neleidžiant viršyti 48 ženklų. Naudojant ilgesnius kaip 48 ženklų pavadinimus, pateikiama klaida „Serveriui nepavyko autentifikuoti užklausos“ ir (arba) neleidžiama eksportuoti failo be failo tipo. Šiame tinklaraščio įraše pateikiama išsamesnė informacija, [Darbo eigos eksportavimo trikčių šalinimas](https://community.dynamics.com/365/financeandoperations/b/elandaxdynamicsaxupgradesanddevelopment/posts/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Ar darbo eigos pateikėjas gali ją taip pat ir tvirtinti?
Taip, darbo eigos pateikėjas taip pat gali ją tvirtinti, jei darbo eiga taip sukonfigūruota. Jei norite to neleisti, nustatykite **Sistemos administravimas > Darbo eiga > Darbo eigos parametrai > Bendra > Tvirtintojas > Neleisti tvirtinti pateikėjui** reikšmę **Taip**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Ar galiu įtraukti įspėjimų į darbo eigas, kad vartotojams būtų teikiami pranešimai?
Toliau pateikiamos kelios pagrindinės sritys, susijusios su įspėjimų įtraukimų į darbo sritis norint teikti pranešimus vartotojams, į kurias reikia atkreipti dėmesį.
- Įspėjimų palyginimas su darbo eigų pranešimų mechanizmais
    - Galima nustatyti įrašų pakeitimų įspėjimus. Darbo eigos keičia įrašus, todėl galima nustatyti įspėjimą, susijusį su darbo eigos inicijuotu įrašo pakeitimu. Vis dėlto, įspėjimų naudojimas nėra tobulas sprendimas, nes darbo eigose įtaisytos skirtingos pranešimų parinktys.
- Standartiniai darbo eigų pranešimai 
    - Darbo eigose yra įtaisytų el. pašto pranešimų. Klientas gali konfigūruoti pranešimus, kad vartotojams būtų siunčiami el. laiškai. Šie pranešimai neinicijuoja veiksmų centro pranešimų vartotojams.
    - Būsimame naujinime veiksmų centro pranešimą, kad vartotojui būtų priskirtas darbo eigos darbo elementas. 
- Pranešimų įtraukimas į darbo eigas
    - Galima sukurti veiksmų centro pranešimų konkretiems vartotojams, pvz., darbo eigos pranešimų, sukurtų naudojant X++.
    - [Darbo eigose yra verslo įvykių](../../dev-itpro/business-events/business-events-workflow.md), kuriuos klientas gali naudoti norėdamas suaktyvinti srautus su ieškomais pranešimais.   

Apibendrinant, jei vartotojas negauna tinkamo pranešimo iš veiksmų centro, kai jam priskiriamas darbo eigos darbo elementas, naudokite [darbo eigos verslo įvykius](../../dev-itpro/business-events/business-events-workflow.md) programoje „Microsoft Power Automate, kad pateiktumėte papildomų arba kitokių pranešimų.

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>Kodėl nepavyksta paleisti darbo eigos rengyklės, naudojant AD FS?
Kai darbo eigos rengyklė veikia naudojant „Active Directory“ susiejimo tarnybą (AD FS) atnaujintoje aplinkoje, gali nepavykti paleisti rengyklę. Šiuo atveju įsitikinkite, kad URL "https://dynamicsaxworkfloweditor/" įtrauktas į ypatybę **„Microsoft Dynamics 365 for Operations“ (vietinė) - Darbo eiga - Vietinė programa** ADFS parametruose.

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>Kodėl apdorojant darbo eigą atsiranda SQL aklaviečių? 
Puslapyje **Darbo eigos parametrai** esančio lauko **Darbo eigos elementų skaičius vienoje paketinėje** numatytoji reikšmė yra 0. Jei reikšmė yra 0, numatytoji reikšmė keičiasi į 20 elementų vienoje paketinėje. Būkite atsargūs, koreguodami šią reikšmę, nes dėl didelio elementų skaičiaus vienoje paketinėje (> 40) gali atsirasti SQL aklaviečių.

## <a name="what-is-the-workflow-enhanced-error-feature"></a>Kas yra patobulinta darbo eigos klaidos funkcija?
Darbo eigos patobulinta klaidos funkcija, esanti versijoje 10.0.13, įtraukia klaidų kodus, kad būtų galima atskirti skirtingas darbo eigos klaidų klases. Klaidos pranešimai, apie kuriuos pranešama, dažniausiai bus panašūs su nedideliais skirtumais, kad jie būtų aiškesni.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
