---
title: Nusidėvėjimo knygos atnaujinimo apžvalga
description: 'Ankstesniuose leidimuose buvo naudojamos dvi ilgalaikio turto vertinimo sąvokos: vertinimo modelis ir nusidėvėjimo knygos. „Microsoft Dynamics 365 for Operations“ (1611) vertinimo modelio funkcija ir nusidėvėjimo knygų funkcija buvo sujungtos į vieną sąvoką, vadinama knyga. Šioje temoje pateikta keletas pastabų apie naujinimą.'
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ef906393ef07661ecd3ceefdbe62310de5ceff21
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840654"
---
# <a name="depreciation-book-upgrade-overview"></a>Nusidėvėjimo knygos atnaujinimo apžvalga

[!include [banner](../includes/banner.md)]

Ankstesniuose leidimuose buvo naudojamos dvi ilgalaikio turto vertinimo sąvokos: vertinimo modelis ir nusidėvėjimo knygos. „Microsoft Dynamics 365 for Operations“ (1611) vertinimo modelio funkcija ir nusidėvėjimo knygų funkcija buvo sujungtos į vieną sąvoką, vadinama knyga. Šioje temoje pateikta keletas pastabų apie naujinimą. 

Atnaujinimo procesas perkels esamą jūsų sąranką ir visas esamas jūsų operacijas į naują knygos struktūrą. Vertės modeliai liks tokie patys, kokie yra šiuo metu, kaip knyga, kuri registruoja į didžiąją knygą. Nusidėvėjimo knygos bus perkeltos į knygą, kurioje nustatyta parinkties **Registruoti į DK** nuostata **Ne**. Nusidėvėjimo knygos žurnalų pavadinimai bus perkelti į DK žurnalo pavadinimą, kuriame nustatyta registravimo sluoksnio nuostata **Nėra**. Nusidėvėjimo knygos operacijos bus perkeltos į ilgalaikio turto operacijas. 

Prieš vykdydami duomenų naujinimą, turite susipažinti su dviem būdais, kaip nusidėvėjimo knygos žurnalo eilutes naujinti į operacijos kvitus, ir kvitų serijos numeraciją, kuri bus naudojama. 

1 būdas: **Sistemos nustatyta numeracija** – tai yra numatytoji parinktis naujinimo našumui optimizuoti. Naujinant nebus naudojama numeracijų sistema, bet kvitai bus paskirstomi naudojant rinkiniu pagrįstą metodą. Atnaujinus bus sukurta nauja numeracija su atitinkamu **kitu numeriu**, nustatytu pagal atnaujintas operacijas. Pagal numatytuosius parametrus numeracijoje bus naudojamas formatas FADBUpgr\#\#\#\#\#\#\#\#\#. Galite naudoti kelis parametrus, norėdami modifikuoti formatą, kai taikote šį metodą.

-   **Numeracijos kodas** – kodas, skirtas nustatyti numeraciją. Šio numeracijos kodo būti negali, nes jis sukuriamas naujinimo metu.
    -   Pastovus pavadinimas: **NumberSequenceDefaultCode**
    -   Numatytoji reikšmė: FADBUpgr
-   **Prefiksas** – pastovi eilutės reikšmė, kuri bus naudojama kaip kvitų numerių priešvardis.
    -   Pastovus pavadinimas: **NumberSequenceDefaultParameterPrefix**
    -   Numatytoji reikšmė: FADBUpgr
-   **Raidinių-skaitinių simbolių ilgis** – numeracijos raidinių-skaitinių simbolių segmento ilgis.
    -   Pastovus pavadinimas: **NumberSequenceDefaultParameterAlpanumericLength**
    -   Numatytoji reikšmė: 9
-   **Pradinis numeris** – pirmasis numeris, naudojamas numeracijoje.
    -   Pastovus pavadinimas: **NumberSequenceDefaultParameterStartNumber**
    -   Numatytoji reikšmė: 1

2 būdas: **Esama vartotojo nustatyta numeracija** – naudojant šią parinktį galima nustatyti numeraciją, kuri bus naudojama naujinant. Naudokite šią parinktį, jei jums reikia išplėstinės numeracijos konfigūracijos. Norėdami naudoti numeraciją, turite modifikuoti naujinimo klasę \_ReleaseUpdateDB70_FixedAssetJournalDepBookRemovalDepBookJournalTrans, nurodydami tolesnę informaciją.

-   **Numeracijos kodas** – numeracijos kodas.
    -   Pastovus pavadinimas: **NumberSequenceExistingCode**
    -   Numatytoji reikšmė: nėra. Reikia atnaujinti į numeracijos kodą.
-   **Bendrai naudojama numeracija** – Būlio logikos reikšmė, skirta nustatyti numeracijos aprėptį. Naudokite „true“, kai numeracijos turi būti bendrai naudojamos visose įmonėse, arba „false“, kai jei numeracija skirta konkrečiai įmonei. Naudojant „false“, numeracija nurodytu pavadinimu turi būti kiekvienoje įmonėje, kurioje yra nusidėvėjimo knygos operacijų. Bendrai naudojamos sekos pateikiamos kiekviename skaidinyje, kuriame yra nusidėvėjimo knygos operacijų.
    -   Pastovus pavadinimas: **NumberSequenceExistingIsShared**
    -   Numatytoji reikšmė: „true“

Parametrai yra pateikti klasės ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans pradžioje. 

*// Pageidaujamo kvitų paskirstymo metodo nurodymas* 
 *// „true“, jei norite naudoti esamos numeracijos kodą* 
 *// „false“, jei ketinate naudoti sistemos nustatytą numeraciją (numatytoji reikšmė)* const boolean NumberSequenceUseExistingCode = false;  

*// Jei naudojate sistemos nustatytos numeracijos metodą, nurodykite numeracijos parametrus.*
 *// Nauja numeracija bus sukurta naudojant šiuos parametrus.* const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;   

*// Jei naudojate esamos numeracijos metodą, nurodykite esamos numeracijos kodą.* 
 *// Esamų numeracijų kvitų paskirstymas bus vykdomas kiekvienoje eilutėje paeiliui.* const str NumberSequenceExistingCode = ''; *// Nurodykite esamos numeracijos kodo aprėptį* 
 *// „true“, jei nurodyta numeracija naudojama bendrai* 
 *// „false“, jei nurodyta numeracija skirta konkrečiai įmonei* 
 *// Bus naudojama numatytoji sistemos nustatyta numeracija, jei nurodytos aprėpties numeracijos kodas nebus rastas.* const boolean NumberSequenceExistingIsShared = true; 

Perkurkite projektą, jei modifikavus konstantas jame yra klasė. 

Kai naudojate sistemos sugeneruotos numeracijos metodą (1 būdą), naujinant bus naudojamas rinkiniu pagrįstas apdorojimas, kad kvitų numeriai būtų paskirstyti pagal naujinimo scenarijaus parametrus. Be to, po paskirstymo bus sukurta nauja numeracija naudojant nurodytus parametrus. 

Kai naudojate vartotojo nustatytos numeracijos metodą (2 būdą), naujinant duomenis patikrinama, ar duomenų bazėje yra nurodytos aprėpties numeracija, skirta kiekvienam skaidiniui ir įmonės su nusidėvėjimo knygos operacijomis. Jei jos nėra, naujinant bus naudojamas kiekvienos eilutės apdorojimo paeiliui funkcija, kad naudojant numeracijos sistemą kvitų numeriai būtų paskirstyti, kaip nurodyta numeracijoje. Jei nurodytos aprėpties numeracijos nėra, naujinant bus naudojamas numatytasis sistemos nustatytos numeracijos metodas kvitų numeriams paskirstyti ir po paskirstymo bus sukurta nauja numeracija naudojant nurodytus numatytuosius parametrus.

Kurį metodą benaudotumėte, duomenų naujinimo scenarijus taip pat taikys naujai sukurtų DK žurnalų pavadinimų lauko **Kvitų serija** numeraciją anksčiau naudotiems nusidėvėjimo knygos žurnalų pavadinimams.



