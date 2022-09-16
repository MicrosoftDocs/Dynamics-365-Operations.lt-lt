---
title: Iniciatyvūs kokybės atnaujinimai
description: Šiame straipsnyje pateikiama informacija apie iniciatyvų kokybės naujinimų pristatymą.
author: rashmansur
ms.date: 09/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2022-08-19
ms.search.form: ''
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 985800aad3711a1b28613f0f82585b4d592cdf58
ms.sourcegitcommit: de989037d83393bea013cd58c061159765305b4f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473611"
---
# <a name="proactive-quality-updates"></a>Iniciatyvūs kokybės atnaujinimai

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
- **Sandbox sinchronizavimo** paskirtis – mažiau nei 20 procentų klientų šiuo metu turi keletą sanddėlių ir išlaikyti vieną sandų dėžę įdiegtą, kur versija atitinka gamybą, kad būtų padedama šalinti triktis. Jei klientas naudoja sandbox, kad galėtų patikrinti naujesnę versiją, o ne jų gamybą, tą sandinę bus gauti tos naujesnės versijos kokybės naujinimai.

## <a name="what-is-the-rollout-roadmap-for-quality-updates"></a>Koks kokybės naujinimų iškeitimų kokybės atnaujinimas?

Numatyta, kad "Azure" viešų debesies klientų aktyvių kokybės naujinimų paskirstymas bus pradėtas 2022 m. spalio pabaigoje arba spalio mėn. Tuo metu bandomoji aplinka taip pat pradės gauti iniciatyvų naujinimo diegimą. Rugsėjo mėnesį bus išsiųstas pranešimas kiekvienam klientui, informuos apie numatomą jų aplinkos grafiką. Proactive atnaujinto paskirstymo proceso išimtys bus leidžiamos tik FDA reguliuojamųjų klientų. Mes vis dar veikiame, kaip bus valdomos reguliuojamos aplinkos ir vyriausybės debesies klientai bei vyriausybės debesies klientai.

Per kitą šešių mėnesių laikotarpį palaipsniui didinsime sandbox aplinkos, kurios gauna aktyvius naujinimus, procentą, kol visos nustatytos aplinkos bus įtrauktos ir vykdoma gamybos aplinkos atnaujinimo eiga. Visu laikotarpiu stebėsime, kaip užtikrinti, kad diegimo procesas būtų nuoseklias ir kad mes atsveiksime savo nenuosklandinių mokamųjų krūvių tikslą.

Kadangi klientai reguliariai gaus mažesnius mokėjimo krūvius, tikitės, kad dabartinis procesas taps paprastesnis. Mes koreguosime atnaujinimo diegimo dažnumą, nes pademonstruosime galimybę vykdyti procesą be jokios galimybės. Šis procesas jau efektyviai veikia mūsų platformai Dataverse ir programoms ir pateikia numatomus paslaugų kokybės patobulinimus. Norime atlikti tą patį žingsnį į priekį ir finansų, ir operacijų programoms.

## <a name="when-will-quality-updates-start-for-production-environments"></a>Kada bus pradėti gamybos aplinkos kokybės naujinimai?
Šiuo metu kokybės atnaujinimai yra tik tiksliniai sand. langeliai. Gamybos aplinkos bus pradedamos naujinti po 2022 m. lapkričio mėn.

## <a name="what-is-the-schedule-for-sandbox-quality-updates"></a>Koks sand dėžės kokybės naujinimų grafikas?
Norėdami gauti informacijos apie tamsaus regiono valandas, [žr. Kas yra aktyvių kokybės naujinimų grafikas](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-is-the-schedule-for-proactive-quality-updates)?

## <a name="how-are-the-dark-hours-handled-for-customers-that-have-one-finance-and-operations-apps-instance-but-are-active-in-multiple-time-zones"></a>Kaip klientų, kurie turi vieną finansų ir operacijų programėlių egzempliorių, bet kurie aktyvūs keliose laiko juostose, tamsos valandos tvarkomos? 
Nėra specialiųjų grafikų už tamsų valandų ribų, kur yra finansų ir operacijų programėlių egzempliorius, [nes mes planuojame įdiegti kokybės atnaujinimus minimaliai netrikdant n ŠIANDIENos veiksmų](../../dev-itpro/deployment/plannedmaintenance-selfservice.md#what-does-near-zero-downtime-maintenance-mean).

## <a name="how-will-microsoft-ensure-the-quality-of-these-updates"></a>Kaip "Microsoft" užtikrins šių naujinimų kokybę?
"Microsoft" pagal tai, kad paleidimo pardavimo galimybės būtų pakankamai efektyvios, kad būtų galima pristatyti smulkius mokančius komponentus, kad tikrinimo išlaidos būtų mažos. Kiekvienas kokybės atnaujinimo pataisas pereina per daug saugių ir saugių diegimų procesą, kuris padeda pagerinti kokybę ir patikimumą bei sumažina klientų įtaką. Diegimas bus vyksta etapais sandų dėžės aplinkose, po to – gamyboje. Diegiant į etapus leidžiama tinkamai stebėti, ar tolesnis diegimas yra saugus. Sustabdysime keitimų stabdymą, jei aptinkama problemų, aptiktų kiekvienoje įdiegtų klientų grupėje, ir užtikrinsime, kad kiekvienas iš sustabdytų veiksmų turi pakankamai laiko norint išmesti problemas. Būsimiems kokybės naujinimams mes suteiksime matomumą grafike atnaujindami viešus dokumentus ir el. laiškus, kad klientai galėtų planuoti ateities planus.

## <a name="can-customers-delay-reschedule-or-pause-a-quality-update"></a>Ar klientai gali atidėti, perplanuoti ar pristabdyti kokybės atnaujinimą?
Ne. Pagrindinis kokybės atnaujinimo tikslas yra užtikrinti pagrindinius reikalavimus, pvz., saugą, privatumą, patikimumą, prieinamumą ir efektyvumą, nuolat tobulinti savo klientus. Atidedama arba prisilaikant atnaujinimą, saugą, prieinamumą ir patikimumą bus rizikuojama.

## <a name="how-can-one-know-the-set-of-changes-that-went-into-a-quality-update-payload"></a>Kaip vienas gali žinoti pakeitimų rinkinį, nuėjo į kokybės atnaujinimo darbo krūvį?
Pereidami **į** skyrių Kokybės naujinimas LCS galėsite peržiūrėti visus KB straipsnius kokybės **naujinimo** puslapyje Aplinkos informacija. 

## <a name="what-is-the-process-if-a-critical-issue-is-found-after-a-quality-update"></a>Koks procesas, jei po kokybės atnaujinimo randama kritinė problema?
Kritinis išdavimas ar regresija yra vienas ar daugiau įvykių, dėl kurių keli klientai įprastai patiria vieno ar kelių paslaugų naudojimo patirtį. Dėl šių problemų gali atsirasti nesuplanuotų prasto laiko, įskaitant netinkamumą, našumo pereiimą ir aptarnavimo valdymo perėjimą. Jei dėl tokių atgalinių keitimų kyla labai svarbus klientas, sustabdysime kokybės atnaujinimo atnaujinimą, kol sugalėsime palaikyti ryšį ir išspręsti problemą. Paprastai tolesnis kokybės atnaujinimas turės reikiamą pataisą, kad būtų galima ištęsti.

Jei paveikiama vieno kliento aplinka, susisiekite su Microsoft pagalbos tarnyba, kad atidarytumėte bilietą. Remiantis pagrindimu, mes sustabdysime kokybės atnaujinimo išbaigimą visoms kitoms to projekto aplinkai, kol išdavimas bus sumažintas.

## <a name="can-customers-still-manually-apply-hotfix-updates-from-lcs"></a>Ar klientai vis dar gali rankiniu būdu taikyti karštųjų pataisų naujinimus iš LCS?
Taip. Kad būtų užtikrintas karštųjų pataisų darbo lygumas, karštųjų pataisų naujinimus vis tiek galima taikyti kliento aplinkai LCS. Tačiau svarbu pažymėti, kad karštosios pataisos, kurios įdiegtos kaip kokybės naujinimo dalis, pereis per standartinį SDP prieš įdiegiant naujinimą. Dėl to dėl aukštesnio kokybės sumažėja regresijų rizika. Rekomenduojame pasirinkti kokybės naujinimą rankiniu būdu taikant karštąsias pataisas, kad būtų padidintas patikimumas.

## <a name="can-customers-self-install-a-quality-update-build-by-themselves-ahead-of-the-schedule"></a>Ar klientai gali patys įdiegti kokybės naujinimo versiją anksčiau už grafiką?
Taip. Galite įdiegti kokybės naujinimą proaktyviai. "Microsoft" praleis atnaujinimą, jei dabartinė aplinkos versija yra lygi arba didesnė už šį kokybės naujinimą.

## <a name="if-an-environment-has-an-upcoming-scheduled-monthly-service-update-within-a-week-will-it-still-receive-quality-updates"></a>Jei aplinkoje yra suplanuotų mėnesio paslaugų atnaujinimo per savaitę, ar vis tiek bus gauti kokybės atnaujinimai?
- Kokybės atnaujinimai netaikomas, jei yra planuojamas planuojamas paslaugos naujinimas per savaitę, nuo kada suplanuotas kokybės atnaujinimas.
- Jei sandbox aplinkoje yra ta pati arba naujesnė versija nei laukiantis kokybės naujinimas, ji bus praleista.
- Jei gamybos aplinkos versija yra ta pati arba naujesnė nei laukiamas kokybės atnaujinimas, ji bus praleista.
- Jei dėl kokybės atnaujinimo arba neautomatinio gamybos atnaujinimo sanddėlyje yra ta pati arba naujesnė versija, gamyba vis tiek gaus suplanuotą mėnesinio tarnybos naujinimo versiją. Jei nenorite, kad suplanuotos gamybos aplinka būtų atnaujinta į tarnybos naujinimo versiją, galite pristabdyti tarnybos naujinimą iš LCS. 
- Rekomenduojame naudoti naujausią kokybės naujinimo versiją, kad būtų patikrinti būsimų tarnybos naujinimų pakeitimai, siekiant užtikrinti geresnį stabilumą ir rezultatus.

## <a name="can-an-environment-be-brought-back-to-its-previous-state-if-there-are-issues-after-a-quality-update-is-applied"></a>Ar galima aplinką grąžinti į ankstesnę būseną, jei pritaikius kokybės naujinimą kyla problemų?
Kai taikomas kokybės atnaujinimas, jokiais atvejais nėra keitimų atšaukimo. Yra tik pataisos persiuntimo pasirinktys, kurios gali sumažinti problemas.

## <a name="what-about-fda-regulation-and-gpx"></a>Ką apie FDA taisykles ir GPX?
Klientų, kuriems taikomas FDA tikrinimas ir taisyklės, planas dar tebėra taikomas. Greit tikimasi daugiau šios vietos naujinimų. Dabar visi tokie klientai atleidžiami nuo kokybės naujinimų.

## <a name="what-versions-of-service-updates-are-supported-for-these-quality-updates"></a>Kokios tarnybos naujinimų versijos palaikomos šiems kokybės naujinams?
Mažesnių nei ši N-2 versijų klientai negaus kokybės naujinimų. 

## <a name="finance-and-operations-apps-deployments-with-retail-components-typically-require-additional-work-in-addition-to-having-to-redeploy-mpos-how-will-these-quality-updates-impact-the-retailsdk"></a>Finansų ir operacijų programėlių diegimams su mažmeninės prekybos komponentais paprastai reikia papildomo darbo be to, kad reikia iš naujo įdiegti MPOS. Kaip šie kokybės naujinimai turės įtakos RetailSDK? 
Kadangi pačios karštųjų pataisų pobūdis nepasikeičia kokybės naujinimų mokamoji apkrova, mes nesitikite jokios papildomos įtakos šiuo metu, konkrečiai susijusiam su mažmeninės prekybos komponentais.

## <a name="is-there-any-impact-to-cloud-hosted-environments-che-"></a>Ar yra koks nors poveikis debesies nuomojamoms aplinkai (CHE)? ? 
Ne.

## <a name="are-there-any-integration-issues-with-microsoft-dataverse"></a>Ar yra integravimo problemų Microsoft Dataverse? 
Ne.

