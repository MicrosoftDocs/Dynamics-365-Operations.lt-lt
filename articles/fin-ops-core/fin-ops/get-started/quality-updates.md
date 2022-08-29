---
title: Proactive kokybės atnaujinimai
description: Šiame straipsnyje pateikiama informacija apie iniciatyvų kokybės naujinimų pristatymą.
author: rashmansur
ms.date: 08/23/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9d81cb15e9a127e7bea7ad9b5e0f50a1ee543f71
ms.sourcegitcommit: 78e85ad49634cd31459fdb7325cb273352bf1501
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/23/2022
ms.locfileid: "9338143"
---
# <a name="proactive-quality-updates"></a>Proactive kokybės atnaujinimai

[!include[banner](../includes/banner.md)]

Per keletą paskutinių metų Microsoft toliau truko tai, ką vadiname viena [versija](../../dev-itpro/lifecycle-services/oneversion-overview.md). Vienos versijos patalpos yra paprastos: kuo arčiau visų klientų gauti tą pačią programinės įrangos versiją, tuo aukštesnė kokybės, kurią galime pristatyti. Surandame ir ištaisome problemas vieną kartą, ir šiuos sprendimus naudojame daugiau klientų.

Šias patalpas patvirtina rezultatai: mažesnis incidentų skaičius mūsų produktuose. Kai klientai nėra toje pačioje versijoje, kreipkite dėmesį, kad jiems daro poveikį problemos, dėl kurių sprendimas jau galimas. Mes jau atlikome daug darbo su "Dynamics 365 Finance", "Dynamics 365" Dynamics 365 Project Operations Dynamics 365 Commerce tiekimo grandine ir dėkojame už naujausią techninio progresą, dabar galima pereiti prie kito veiksmo. Ši informacija pateikia daugiau informacijos, ką ketiname daryti, ką jau padarėme, norėdami nustatyti etapą ir kaip ir kada mes pristatome naujus pajėgumus be klaidos.

## <a name="focus-on-quality-updates"></a>Aktyvinti kokybės naujinimus

Šiuo metu mes teikiame septynis [tarnybos naujinimus](public-preview-releases.md) per metus. Pavyzdžiui, 10.0.29 versija yra tarnybos atnaujinimas. Iki šiol buvo aštuoni atnaujinimai per metus. Tačiau mes numetėme vieną atnaujinimą, atsakydami į klientų grįžtamąjį ryšį, kuris išvengė noro išvengti pakeitimų iki kalendorinių metų pabaigos.

Mes nepasikeičiame aptarnavimo naujinimų kadastros. Vietoj to, mūsų kitas žingsnis į priekį vienos versijos žingsnyje daug dėmesio skiriama *kokybės naujams*. Kokybės naujinimai yra kaupiamieji karštųjų pataisų versijos. Jose nėra naujų funkcijų. Bet kuriuo metu mūsų visa klientų bendruomenė yra paskirstyta tarp trijų ar keturių naujausių aptarnavimo naujinimų. Tačiau bet kokiam pateiktam aptarnavimo atnaujinimų tuzinai skirtingų kokybės naujinimo versijų gali būti naudojami grupėje, atsižvelgiant į žmonių įdiegti datas. Sekame žingsnyje aktyviai išsiuntinsime kokybės atnaujinimus. Šį modelį jau naudojame mūsų programoms Dataverse ir gavome tikėtinus rezultatus, nes pagerėja jo kokybė ir sumažėja palaikymo incidentai.

Žinoma, defektų sumažinimas gali sumažinti arba visiškai panaikinti kokybės atnaujinimų poreikį. Mes naudojame kelias iniciatyvas skrydžio metu, kad sumažinsime defektus, kuriuos reikia atnaujinti. Net jei kokybės naujinime sumažinami mokami kroviniai, klientų sistemos vientisumas pagerina palaikymo galimybes, greičiau pagerins klientus ir sumažins klientų, susiduriančių su jau esamais sprendimais, dažnumą.

## <a name="making-proactive-distribution-possible"></a>Galimas aktyvus paskirstymas

Jau įdiegti keli išankstiniai avansai, kurie įgalina išankstinį kokybės naujinimų pristatymą:

- **Beveik nulinis** prasto laiko atnaujinimas – norint stumyti daugiau dažnesnių aplinkoje, būtina sumažinti poveikį aplinkos pasiekiamumui, kad būtų išlaikomos "Dynamics 365" paslaugų lygio sutartys (SLA). Iš pradžių buvo įdiegtas beveik nulinis prasto laiko atnaujinimas, siekiant padėti pagerinti mėnesinį operacinės sistemos pataisų tobulinimą, naudojant klasterio rinkmenų permetimą, kad atnaujintas vaizdas būtų aktyvinamas šiek tiek vėliau. Naujinimų taikymo mechanizmas yra patobulintas, kad jis dar mažiau nutrikdytų ir apimtų operacinės sistemos pataisų ir kokybės atnaujinimo diegimą.

    Interaktyviems vartotojams aktyvus seansas gali būti pertrauktas, o kartojimo programa pereis į dabar atnaujintą aplinką. Įdiegus prioritetinį [paketinį](../../dev-itpro/sysadmin/priority-based-batch-scheduling.md) planavimą, kuris dabar galimas pasirinkus, paketinis planavimas ir apdorojimas atsistato ir tęsiami iškart po atnaujinimo. Prioritetinis paketinis planavimas bus skirtas klientams, prieš jiems pradedant dalyvauti proaktyvioje savo gamybos aplinkose kokybės naujinimų paskirstyme.

- **Tamsos** valandos – tamsesnės valandos nustatomos kiekvienam "Azure" regionui ir beveik nulinis downtime atnaujinimas bus naujuose valandų laikotarpiu.

## <a name="the-proactive-update-process"></a>Iniciatyvaus atnaujinimo procesas

Aktyvių kokybės atnaujinimų diegimas bus po saugaus diegimo proceso (SDP). SDP specifikos gali keistis, tačiau kokybės atnaujinimai iš pradžių bus įdiegti į sandbox aplinkas. Procesas bus prasidės aplinka, kurioje galima diegti anksti. Sėkmingai įdiegtos sanddės padidėjimo procentinė dalis, bus pradėtas diegti gamybos aplinkose. Procesas prasidės aplinka, kuri vėl pradės diegti anksčiau. Klausymo sistemos bus stebimi sistemos telemetikos ir seniausios versijos incidentai, o jei aptinkama kokia nors regresija, sustabdys konkrečios versijos iškliaumą. Jei reikia, klientai vis dar galės gauti kokybės naujinimus anksčiau už iniciatyvų diegimą.

Dabartiniai paleidimo valdymo duomenys rodo, kad į kokybės atnaujinimus įtraukta mažiau nei 3 procentai regresijų. Kuo daugiau dėmesio bus skiriama regresijos pašalinimui ir išplėstiniam SDP, galimas regresijų poveikis bus atitinkamai mažesnis nei kokybės pelnas, kurį pasieks daug greičiau gaunant klientams įdiegtas pataisas.

## <a name="process-changes"></a>Keitimų apdorojimas

Proceso pakeitimų rinkinys įgyvendintas prieš suaktyvinus aktyvią kokybės naujinimo įdiegtį:

- **Schema** – įrankis užtikrina, kad kokybės naujinimo versijos apima tik schemos pakeitimus, kurie gali būti taikomi paslaugai internete. Šis būdas padės išlaikyti galimybę taikyti atnaujinimą beveik nulinio nulio laiku.
- **Padidintas pokytis per** daug – šiuo metu yra papildomas proceso žingsnis, skirtas patvirtinti įtraukimo į kokybės naujinimą pakeitimus. Papildomas veiksmas bus padidintas, kad būtų sumažintas galimas regresijų potencialas. Kokybės naujinimų pakeitimai negali būti atlikti, todėl padidintas keitimų skaičius padės užtikrinti, kad šį tikslą atitiksime.
- **Matomumas** – mes išsiųsime pranešimus el. paštu ir ciklo tarnybose (LCS) dėl būsimų aktyvių kokybės naujinimų. Be to, palaikymo komandos ir galimi klientai galės matyti, kur sėkmingai įdiegti kokybės atnaujinimai.
- **Versijos atsarginis** – skrydžio sistema bus naudojama norint sugrupuoti visus aktyvių kokybės atnaujinimų pakeitimus. Jei po iniciatyvaus diegimo reikia atsarginio diegimo, jį galima atlikti naudojant skrydžio sistemą.
- **Sandbox sinchronizavimo** paskirtis – mažiau nei 20 procentų klientų šiuo metu turi keletą sanddėlių ir išlaikyti vieną sandų dėžę įdiegtą, kur versija atitinka gamybą, kad būtų padedama šalinti triktis. Norime ateityje įdiegti klientams galimybę nurodyti sandbox aplinką, kuri neturi gauti aktyvios kokybės atnaujinimo diegimo kartu su kitomis sandboxe, tačiau vietoj to ją gauti vėliau kartu su gamybos aplinka. Atminkite, kad jei klientas naudoja sandų dėžę, kad galėtų patikrinti naujesnę versiją, o ne jų gamybą, sand. langelyje bus gauti naujesnės versijos kokybės naujinimai.
- 
## <a name="when-will-proactive-quality-updates-start"></a>Kada bus pradėti aktyvūs kokybės atnaujinimai?

Numatyta, kad "Azure" viešų debesies klientų aktyvių kokybės naujinimų paskirstymas bus pradėtas 2022 m. spalio pabaigoje arba spalio mėn. Tuo metu bandomoji aplinka taip pat pradės gauti iniciatyvų naujinimo diegimą. Rugsėjo mėnesį bus išsiųstas pranešimas kiekvienam klientui, informuos apie numatomą jų aplinkos grafiką. Proactive atnaujinto paskirstymo proceso išimtys bus leidžiamos tik FDA reguliuojamųjų klientų. Mes vis dar veikiame, kaip bus valdomos reguliuojamos aplinkos ir vyriausybės debesies klientai bei vyriausybės debesies klientai.

Per kitą šešių mėnesių laikotarpį palaipsniui didinsime sandbox aplinkos, kurios gauna aktyvius naujinimus, procentą, kol visos nustatytos aplinkos bus įtrauktos ir vykdoma gamybos aplinkos atnaujinimo eiga. Visu laikotarpiu stebėsime, kaip užtikrinti, kad diegimo procesas būtų nuoseklias ir kad mes atsveiksime savo nenuosklandinių mokamųjų krūvių tikslą.

Kadangi klientai reguliariai gaus mažesnius mokėjimo krūvius, tikitės, kad dabartinis procesas taps paprastesnis. Mes koreguosime atnaujinimo diegimo dažnumą, nes pademonstruosime galimybę vykdyti procesą be jokios galimybės. Šis procesas jau efektyviai veikia mūsų platformai Dataverse ir programoms ir pateikia numatomus paslaugų kokybės patobulinimus. Norime atlikti tą patį žingsnį į priekį ir finansų, ir operacijų programoms.
