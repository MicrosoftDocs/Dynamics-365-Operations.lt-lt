---
title: "Nusidėvėjimo knygų versijos naujinimo apžvalga"
description: "Ankstesnėse laidose, ten buvo du vertinimo sąvokas turtų - vertinimo modelių ir nusidėvėjimo knygas. „Microsoft Dynamics 365 for Operations“ 1611 versijoje vertinimo modelio funkcija ir nusidėvėjimo knygų funkcija buvo sujungtos į vieną sąvoką, vadinama knyga. Šioje temoje pateikta keletas pastabų apie naujinimą."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer
ms.search.scope: Operations, Core
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: bec019d218d80ba059d5a1c232072f46b1ae3ee2
ms.openlocfilehash: d29cb7bc5acc29be93332b4211adebc4486a7a25
ms.lasthandoff: 03/31/2017


---

# <a name="depreciation-book-upgrade-overview"></a>Nusidėvėjimo knygų versijos naujinimo apžvalga

Ankstesnėse laidose, ten buvo du vertinimo sąvokas turtų - vertinimo modelių ir nusidėvėjimo knygas. „Microsoft Dynamics 365 for Operations“ 1611 versijoje vertinimo modelio funkcija ir nusidėvėjimo knygų funkcija buvo sujungtos į vieną sąvoką, vadinama knyga. Šioje temoje pateikta keletas pastabų apie naujinimą. 

Atnaujinimo procesas perkels esamą jūsų sąranką ir visas esamas jūsų operacijas į naują knygos struktūrą. Vertės modeliai liks tokie patys, kokie yra šiuo metu, kaip knyga, kuri registruoja į didžiąją knygą. Nusidėvėjimo knygos bus perkeltos į knygą, kurioje nustatyta parinkties **Registruoti į DK** nuostata **Ne**. Nusidėvėjimo knygos žurnalo pavadinimai bus perkeltas į DK žurnalo pavadinimo nustatyti registravimo sluoksnis **niekas**. Nusidėvėjimo knygos operacijos bus perkelta į ilgalaikio turto operacijas. 

Prieš vykdydami duomenų naujinimą, turite susipažinti su dviem būdais, kaip nusidėvėjimo knygos žurnalo eilutes naujinti į operacijos kvitus, ir kvitų serijos numeraciją, kuri bus naudojama. 

1 būdas: **Sistemos nustatyta numeracija** – tai yra numatytoji parinktis naujinimo našumui optimizuoti. Naujinant nebus naudojama numeracijų sistema, bet kvitai bus paskirstomi naudojant rinkiniu pagrįstą metodą. Po atnaujinimo, bus sukurta nauja numeracija su į **kitą, numeriu, nurodytu** atitinkamai pagal atnaujintą operacijas. Pagal numatytuosius nustatymus bus skaičių seką, FADBUpgr\#\#\#\#\#\#\#\#\# formatu. Yra keli parametrai jums pataisyti formą naudojant šį metodą:

-   **Skaičių Numeracijos kodas** – nustatyti numeracijos kodą. Šios Numeracijos kodas negali egzistuoti, nes ji bus sukurta programinės įrangos naujinimas.
    -   Pastovus pavadinimas: **NumberSequenceDefaultCode**
    -   Numatytoji reikšmė: FADBUpgr
-   **Prefiksas** – pastovi eilutės reikšmė, kuri bus naudojama kaip kvitų numerių priešvardis.
    -   Pastovus pavadinimas: **NumberSequenceDefaultParameterPrefix**
    -   Numatytoji reikšmė: FADBUpgr
-   **Raidinių-skaitinių simbolių ilgis** – numeracijos raidinių-skaitinių simbolių segmento ilgis.
    -   Pastovus vardas: ** NumberSequenceDefaultParameterAlpanumericLength **
    -   Numatytoji reikšmė: 9
-   **Pradinis numeris** – pirmasis numeris, naudojamas numeracijoje.
    -   Pastovus vardas: ** NumberSequenceDefaultParameterStartNumber **
    -   Numatytoji reikšmė: 1

2 variantas: **esamas vartotojo apibrėžiamų numeracijos** -Ši galimybė leis jums nustatyti numeraciją galima atnaujinti. Apsvarstyti, naudojant šią parinktį, jei turite Išplėstinė skaičių seka konfigūracija. Norėdami naudoti numeraciją, turite modifikuoti atnaujinti klasės ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans su šia informacija:

-   **Numeracijos kodas** – numeracijos kodas.
    -   Pastovus vardas: ** NumberSequenceExistingCode **
    -   Numatytoji reikšmė: nėra. Reikia atnaujinti į numeracijos kodą.
-   **Bendrai naudojama numeracija** – Būlio logikos reikšmė, skirta nustatyti numeracijos aprėptį. Naudokite „true“, kai numeracijos turi būti bendrai naudojamos visose įmonėse, arba „false“, kai jei numeracija skirta konkrečiai įmonei. Naudojant "klaidinga", kiekviena įmonė, kuri yra nusidėvėjimo knygos operacijos turi būti numeracija su nurodytu pavadinimu. Bendrai naudojamą numeraciją egzistuoja kiekvieną skaidinį, kuriame yra nusidėvėjimo knygos operacijas.
    -   Pastovus vardas: ** NumberSequenceExistingIsShared **
    -   Numatytoji reikšmė: „true“

Parametrai yra pradžioje, ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans klasė. 

*Nurodykite geriau požiūris kvitų paskirstymas*<ph id="t1">
</ph>*/ / tiesa, jei norite naudoti, esamos numeracijos kodas*<ph id="t2">
</ph>*/ / false, jei jūs ketinate naudoti sistemos skaičių seką (numatytoji)* konstanta Bulio logikos NumberSequenceUseExistingCode = false;  

*Jei naudojate sistemos skaičių sekos metodas, nurodykite parametrų numeracija. *<ph id="t3">
</ph>*/ / Nauja numeracija bus sukurtas su šiais parametrais.* Konstanta str NumberSequenceDefaultCode = 'FADBUpgr'; konstanta str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; konstanta int NumberSequenceDefaultParameterAlpanumericLength = 9; konstanta int NumberSequenceDefaultParameterStartNumber = 1;   

*Jei naudojant esamą skaičių seka požiūris, nurodykite esamą Numeracijos kodas. *<ph id="t4">
</ph>*/ / Kvitų paskirstymas bus pereiti vieną eilutę po kitos esamos numeracijų.* Konstanta str NumberSequenceExistingCode = ''; */ / Nurodykite taikomos esamos numeracijos kodas*<ph id="t5">
</ph>*/ / tiesa, jei nustatyta numeracija yra bendra*<ph id="t6">
</ph>*/ / false, jei nurodytos numeracijos kiekvienai bendrovei*<ph id="t7">
</ph>*/ / numatytąjį sistemos numeracija bus naudojamas, jei nerandama numeracijos kodą su nurodyta apimtimi.* const boolean NumberSequenceExistingIsShared = true; 

Perkurkite projektą, jei modifikavus konstantas jame yra klasė. 

Naudoti sistemos sugeneruota skaitmenų seka požiūris (1 variantas), atnaujinti panaudos pagrindu sukurti perdirbimo priskirti kvitų numerius, kaip nurodyta atnaujinimo scenarijų parametrus. Ji taip pat bus sukurti naują numeracijos su nurodytais parametrais po paskirstymo. 

Kai naudojate vartotojo nustatytos numeracijos metodą (2 būdą), naujinant duomenis patikrinama, ar duomenų bazėje yra nurodytos aprėpties numeracija, skirta kiekvienam skaidiniui ir įmonės su nusidėvėjimo knygos operacijomis. Jei jis egzistuoja, atnaujinimo naudos vieną eilutę po kitos perdirbimo priskirti kvitų numerius, kaip nurodyta naudojant skaičių seka pagal numeraciją. Jei numeracija nėra nurodytos apimties, atnaujinimo taikys numatytąjį sistemos skaičių seka metodą priskirti kvitų numerius ir sukurs naują numeracijos su nurodyta numatytoji parametrai po paskirstymo.

Kurį metodą benaudotumėte, duomenų naujinimo scenarijus taip pat taikys naujai sukurtų DK žurnalų pavadinimų lauko **Kvitų serija** numeraciją anksčiau naudotiems nusidėvėjimo knygos žurnalų pavadinimams.


