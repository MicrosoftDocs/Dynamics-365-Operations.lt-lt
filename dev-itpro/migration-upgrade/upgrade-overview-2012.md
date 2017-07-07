---
title: "„Dynamics AX 2012“ naujinimas į „Dynamics 365 for Finance and Operations“, „Enterprise‟ leidimą"
description: "Šioje temoje aprašomas procesas, kurį gali naudoti klientai, šiuo metu naudojantys „Microsoft Dynamics AX 2012“, norėdami perkelti savo duomenis ir kodą į „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimą."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 13507fcf9c0d626709aeb4e00a8632411204c20f
ms.contentlocale: lt-lt
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-microsoft-dynamics-ax-2012-to-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>„Microsoft Dynamics AX 2012“ naujinimas į „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise‟ leidimą

[!include[banner](../includes/banner.md)]

8 platformos naujinime „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidime, pateikiamas naujinimo maršrutas, kurį gali naudoti klientai, šiuo metu naudojantys „Microsoft Dynamics AX 2012“, kad perkeltų duomenis ir kodą į „Finance and Operations“. Naujinimo procesas yra pagrįstas šiais elementais:

- Įrankiai, kurie padės perkelti esamą pasirinktinį programos kodą iš „AX 2012“.
- Duomenų naujinimo procesas, kurį galite naudoti norėdami perkelti savo duomenų bazę. Todėl jūs galite atnaujinti visą operacijų retrospektyvą.

## <a name="overview"></a>Apžvalga

Bendras naujinimo procesas gali būti pavaizduotas kaip trys viską apimantys etapai: analizuoti, vykdyti ir patikrinti.

Pateiktoje diagramoje rodomas visas naujinimo procesas ir veikla, kurią laikome kiekvieno etapo dalimi. 

![Naujinimo procesas](./media/upgrade-process.png)

## <a name="analyze"></a>Analizė

Analizės etapo veikla padeda įvertinti pastangas, kurių reikės naujinant. Be to, ji padeda paruošti projekto planą. Ši veikla gali būti atlikta prieš įsigyjant „Finance and Operations“. Ji padės jums priimti pagrįstą pirkimo sprendimą – suteiks duomenų elementą, rodantį, kiek pastangų ir išteklių reikės.

### <a name="sign-up-for-a-public-preview-in-lcs"></a>Registracija norint LCS naudoti viešąją vertinimo versiją

Norėdami atlikti analizės veiklą prieš pirkdami „Finance and Operations“, galite registruotis ir pasinaudoti viešąja vertinimo versija. Viešoji vertinimo versija leidžia įdiegti savo „Finance and Operations“ aplinką. Ji taip pat suteikia prieigą prie „Microsoft Dynamics Lifecycle Services“ (LCS) įrankių, kurie naudojami norint įvertinti jūsų „AX 2012“ aplinką ir esamą pasirinktinį kodą.

Jei turite LCS projektą, skirtą „AX 2012“, vis tiek reikia registruotis dėl papildomo naujo projekto, kad įvertintumėte „Finance and Operations“.

Informacijos apie tai, kaip gauti viešąją vertinimo versiją klientams, žr. https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Informacijos apie tai, kaip gauti viešąją vertinimo versiją partneriams, žr. https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Turėkite omenyje, kad ši viešoji vertinimo versija skiriasi nuo [30 dienų bandomosios versijos](https://aka.ms/D365OperationTrials). Trisdešimties dienų išbandymas suteikia įdiegtą „Finance and Operations“ egzempliorių, kurį galite naudoti norėdami programą ištirti ir įvertinti. Tačiau analizės veikla reikalauja visos LCS patirties ir įrankių.

### <a name="select-the-upgrade-methodology"></a>Pasirinkite naujinimo metodiką
Savo naujame LCS projekte nustatykite projekto metodiką į **Naujinti „AX 2012“ į „Dynamics 365 for Operations“**. Ši metodika specialiai sukurta „AX 2012“ klientams, kurie naujina. Joje išsamiai aprašomi trys etapai ir pateikiamos pagalbinių proceso dokumentų nuorodos.

![Naujinimo metodika(./media/methodology.png)
 
### <a name="run-the-upgrade-analyzer"></a>Paleiskite naujinimo analizatorių
Naujinimo analizatoriaus įrankis veikia jūsų „AX 2012“ aplinkoje ir nustato užduotis, kurias reikėtų atlikti norint paruošti „AX 2012“ aplinką, kad naujinimo patirtis būtų sklandesnė ir pigesnė:

- **Duomenų valymas** – šis procesas padeda nustatyti duomenis, kuriuos galite pašalinti neprarasdami funkcijų. Įrankis nustato įvairių tipų duomenis, kuriuos galima sumažinti paleidus valymo procesą. Dėl kiekvieno tipo duomenų pateikiamas paaiškinimas apie valymo poveikį. Tada galite nuspręsti, ar paleisti valymo procesą. „Finance and Operations“ prenumeratos kainos dalis priklauso nuo duomenų bazės dydžio. Todėl sumažindami dydį galite sumažinti to komponento prenumeratos kainą ir sutrumpinti laiką, reikalingą naujinimo procesui. Mažesnė duomenų bazė padeda užtikrinti spartesnį naujinimą.
- **SQL konfigūracija** – šis procesas peržiūri SQL konfigūraciją ir rekomenduoja optimizavimą. Užtikrinus optimalų SQL veikimą, šis procesas padeda sutrumpinti laiką, būtiną naujinimo procesui.
- **Pasenusios funkcijos** – šis procesas nustato funkcijas, kurias dabar naudojate, bet kurios nepasiekiamos „Finance and Operations“. Procesas padeda anksti atrasti funkcionalumo spragas. Be to, pateikia alternatyvių pasiūlymų.

Be to, atlikdami šį veiksmą turite įdiegti KBXXXXXXX „AX 2012“ aplinkoje. Ši karštoji pataisa suteikia išankstinį naujinimo kontrolinį sąrašą. „AX 2012“ aplinkoje galite naudoti šį kontrolinį sąrašą norėdami įvesti duomenis, kurių reikės naujinant. Pvz., vienoje išankstinio naujinimo kontrolinio sąrašo užduotyje nurodote kiekvieno dabartinio „AX 2012“ vartotojo „Microsoft Azure Active Directory“ („Azure AD“) prisijungimo informaciją, kad kiekvienas vartotojas galėtų prisijungti prie „Finance and Operations“.

Šio veiksmo išvestis tampa jūsų „AX 2012“ sistemos administratorių naujinimo projekto plano darbo srautu.

Daugiau informacijos rasite [Analizė: naujinimo analizatoriaus naudojamas perkėlimo darbui planuoti](upgrade-analyzer-tool.md).

### <a name="run-the-code-upgrade-estimation-tools"></a>Paleiskite kodo naujinimo įvertinimo įrankius
Šiuo veiksmu paimamas jūsų kodas iš „AX 2012“, konvertuojamas į naują formatą ir pateikiamas atsiliepimas apie nesuderinamumus, kuriuos programuotojas turi pašalinti vėliau. Šis veiksmas yra pagrindas norint apskaičiuoti kodo naujinimo kainą.

Norėdami atlikti šį veiksmą turite eksportuoti savo kodą iš „AX 2012“ (kaip modelių saugyklos eksportavimas) ir įkelti į LCS kodo naujinimo įrankį. Kodo naujinimo įrankis pateiks atnaujintą kodo versiją ir ataskaitą apie likusius nesuderinamumus, kuriuos reikia pašalinti. Tada jūsų programuotojas gali peržiūrėti atnaujintą kodą ir ataskaitą, kad nustatytų pastangas, kurių reikės norint atnaujinti kodo pagrindą.

Šio veiksmo išvestis pateikia jūsų „Microsoft Dynamics AX“ programuotojams naujinimo projekto plano darbo srautą.

Daugiau informacijos rasite [Analizė: kodo naujinimo pastangų įvertinimas](analyze-code-upgrade.md).

### <a name="deploy-a-demo-environment"></a>Demonstracinės aplinkos diegimas
Demonstracinės aplinkos yra numatytosios aplinkos, kuriose yra demonstracinių duomenų (tai ne jūsų duomenys) ir standartinis kodas (be tinkinimo). Rekomenduojame įdiegti demonstracinę aplinką siekiant įvertinti naujas funkcijas ir atlikti pagrindinę standartinių „AX 2012“ naudojamų procesų, kurie galėjo pasikeisti „Finance and Operations“, trūkumų analizę. Arba galite įdiegti šias demonstracines aplinkas „Azure“ ar atsisiųsti jas kaip virtualųjį įrenginį (VM), kurį galima paleisti savo aparatūroje. Jei įdiegiate jas „Azure“, turite pateikti savo „Azure“ prenumeratą, nes vis dar naudojate viešosios vertinimo versijos projektą ir nesate įsigiję „Finance and Operations“ prenumeratos.

Šio veiksmo išvestis pateikia naujinimo projekto plano darbo srautą jūsų funkciniams arba verslo vartotojams.

Daugiau informacijos rasite [Analizė: smėlio dėžės aplinkos diegimas](analysis-sandbox.md)

### <a name="create-a-project-plan"></a>Kurti projekto planą
Projekto plano šablonas pateikiamas naujinimo metodikoje. Šiame veiksme ankstesnių analizės etapo veiksmų išvestis naudojama norint užpildyti naujinimo projekto planą. Projekto plane bus ir visa bandymo informacija: duomenų naujinimo bandymo, visiško perkėlimo bandymo, sėkmingo funkcinio testo pakartojimai bei informacija apie įvairius toms užduotims priskiriamus išteklius.

Šiame etape projekto planas pateikia duomenų elementą, kuris gali padėti suprasti, kiek reikės laiko ir išlaidų norint atnaujinti į „Finance and Operations“.

## <a name="execute"></a>Vykdyti
Vykdymo etapo metu atliksite užduotis, kurias suplanavote analizės etapo metu. Norėdami pereiti prie vykdymo etapo turite įsigyti „Finance and Operations“ ir turėti pakankamai išteklių, kad būtų galima atnaujinti.

### <a name="switch-to-the-lcs-implementation-project"></a>Pereiti prie LCS diegimo projekto
Viešosios vertinimo versijos projektas, kurį naudojote analizės etape, savo darbą atliko. Dabar galite jo atsisakyti. Per likusius veiksmus reikia tik projekto plano, kurį sukūrėte paskutiniuoju analizės etapo veiksmu.

Kai įsigysite „Finance and Operations“ prenumeratą, gausite informacijos, kaip užsiregistruoti dėl naujo LCS projekto. Šis projektas yra žinomas kaip diegimo projektas ir bus naujas nuolatinis jūsų prenumeratos LCS projektas tol, kol turėsite tą prenumeratą. Šis projektas skiriasi nuo viešosios vertinimo versijos projekto tuo, kad jį valdo „Microsoft“. Todėl šiam projektui būdingos šios savybės:

- Visos projekto aplinkos yra laikomos „Azure“.
- „Azure“ prenumerata, susijusi su „Microsoft“ valdomu projektu. Todėl nereikia atskirai mokėti už „Azure“. Išlaidos įtrauktos į jūsų „Finance and Operations“ prenumeratą.
- Projekto gamybos aplinką prižiūri „Microsoft“. Todėl kodo diegimą, naujinimus ir infrastruktūros priežiūrą tiesiogiai vykdo „Microsoft“, o ne jūsų darbuotojai. 

### <a name="perform-the-ax-2012-preparation-tasks"></a>Atlikite „AX 2012“ paruošimo užduotis
Atlikite užduotis, kurias aptiko naujinimo analizatoriaus įrankis ir kurios buvo įtrauktos į jūsų naujinimo projekto planą. Šias užduotis turi atlikti jūsų „Microsoft Dynamics AX“ sistemos administratorius ir duomenų bazės administratorius (DBA).

[Duomenų naujinimas iš „AX 2012“ į „Dynamics 365 for Operations“ – išankstinis naujinimo kontrolinis sąrašas „AX 2012“](prepare-data-upgrade.md)

### <a name="perform-code-upgrade"></a>Atnaujinkite kodą
Atlikite užduotis, kurios buvo suplanuotos atliekant analizės etapo kodo naujinimo įvertinimo veiksmą. Šias užduotis turi atlikti jūsų programuotojai.

Nuo šio momento „AX 2012“ kodo pakeitimai turėtų būti sustabdyti. „AX 2012“ galima atlikti tik avarinius kodo pakeitimus. Jei pakeičiama, tai turi būti rankiniu būdu perkelta į naujo kodo pagrindą.

### <a name="develop-new-code"></a>Sukurkite naują kodą
Atlikite trūkumų analizės užduotis; trūkumų analizė buvo atlikta analizės etapo veiksmu „Diegti demonstracinę aplinką“. Tikriausiai šios užduotys bus funkcinių užduočių, kurios apibrėžia tinkinimo konfigūravimo ir kūrimo užduotis, susijusias su naujomis funkcijomis, mišinys.

### <a name="data-upgrade-development-environment"></a>Duomenų naujinimas (programavimo aplinka)
Baigę kodo naujinimo užduotis galite pirmą kartą atnaujinti savo „AX 2012“ duomenų bazę į „Finance and Operation“. Šis pirmasis naujinimas vyksta programavimo aplinkoje, kad galėtumėte lengviau išspręsti problemas, aptinkamas šiame etape. Programavimo aplinkoje problemą galima išspręsti iš karto, pataisyti kodą ir per kelias minutes vėl paleisti naujinimą. Didesnės smėlio dėžės aplinkos nesuteikia šio lankstumo ir reikia bent keleto valandų norint išspręsti problemas, atnaujinti kodą, įdiegti atnaujintą kodą bei iš naujo paleisti naujinimą.

Procesas parodytas tolesniame paveikslėlyje. Sukurkite „AX 2012“ duomenų bazės atsarginę kopiją, įkelkite ją į „Azure“, atkurkite „Finance and Operations“ aplinkoje ir paleiskite duomenų naujinimą.

![Duomenų naujinimas programavimo aplinkoje](./media/data-upgrade-dev.png)
 
Duomenų naujinimas vykdomas naudojant specialaus tipo diegiamą paketą. Toks pat mechanizmas naudojamas norint įdiegti naują „Finance and Operations“ kodą iš vienos aplinkos į kitą.

Pagrindinė sistema, naudojama norint konvertuoti duomenų bazės duomenis šio proceso metu, iš esmės yra tokia pati kaip „AX 2012“ naujinimo sistema, pagrįsta X++ paketinėmis užduotimis, kurios vykdo **ReleaseUpdatexxx** klases.

Daugiau informacijos rasite [Duomenų naujinimas iš „AX 2012“ į „Dynamics 365 for Operations“ programavimo aplinkoje](data-upgrade-2012.md).

### <a name="data-upgrade-sandbox-environments"></a>Duomenų naujinimas (smėlio dėžės aplinkos)
Kai duomenys atnaujinami programavimo aplinkoje, tokį patį procesą galima atlikti smėlio dėžės aplinkoje. Smėlio dėžės aplinka yra aplinka, kurioje verslo vartotojai ir funkcinės komandos nariai gali patikrinti verslo procesus naudodami atnaujintus „AX 2012“ duomenis ir kodą.

Pateiktame paveikslėlyje rodomas duomenų naujinimo procesas smėlio dėžės aplinkoje. Skirtumas yra tas, kad vietoj tradicinės SQL atsarginės kopijos naudojamas „bacpac“ įrankis. Šis įrankis būtinas norint konvertuoti tarp „Microsoft SQL Server“ ir „Azure“ SQL duomenų bazės. Tai yra standartinis SQL įrankis, jis nėra būdingas vien tik „Finance and Operations“.

![Duomenų atnaujinimas smėlio dėžės aplinkoje](./media/data-upgrade-sandbox.png)

Daugiau informacijos rasite [Duomenų naujinimas iš „AX 2012“ į „Dynamics 365 for Operations“ smėlio dėžės aplinkoje](upgrade-data-sandbox.md).
 
## <a name="validate"></a>Tikrinti
Kai pasieksite tikrinimo etapą, turėsite aplinkų, kuriose bus atnaujintas pasirinktinis kodas ir atnaujinti duomenys. Šiame etape aprašomas tikrinimo ir bandymo procesas, kad atnaujinta aplinka veiktų taip, kaip norima. Be to, aprašomas paruošimo galutinai paleisti procesas.

### <a name="perform-cutover-testing-and-create-a-cutover-plan"></a>Atlikite visiško perkėlimo bandymą ir sukurkite visiško perkėlimo planą
Terminas _visiškas perkėlimas_ čia vartojamas norint aprašyti galutinio naujos sistemos paleidimo procesą. Šį procesą sudaro užduotys, kurias reikia atlikti išjungus „AX 2012“ ir prieš įjungiant „Finance and Operations“. 

Bandymo tikslas yra išbandyti visiško perkėlimo procesą. Tokiu būdu galite padėti užtikrinti, kad visiems, dalyvaujantiems faktiniame visiškame perkėlime, darbai vyktų sklandžiai.

Yra du pagrindiniai darbo srautai:

- **Techninis darbo srautas** – šis darbo srautas yra duomenų naujinimo procesas. Jūsų įmonė taikys leidžiamos prastovos limitą. Esant šiai prastovai nebus galima naudoti nei AX 2012, nei „Finance and Operations‟. Techninis darbo srautas gali turėti pritaikyti duomenų naujinimo procedūros našumą, kad atitiktų verslo prastovos apribojimą. 
- **Funkcinis darbo srautas** – atnaujinus duomenis, „Finance and Operations“ aplinkoje reikės atlikti keletą konfigūravimo užduočių. Visos šios užduotys turi būti dokumentuotos ir įvertintos kiekybiškai, joms priskirti ištekliai, nes jos turi atitikti technines užduotis ir verslo prastovos apribojimą.

Daugiau informacijos rasite 
- [Tikrinti: visiško perkėlimo bandymas](upgrade-cutover-testing.md)
- [Tikrinti: programos tikrinimo procesas](app-validation-process.md)

### <a name="functional-test-pass"></a>Sėkmingas funkcinis testas
Atlikite išsamų visų verslo procesų funkcinį testą. Tai bus išsamus pakartotinis visų „Finance and Operations“ verslo procesų testas. Šie verslo procesai apima senus procesus, kurie buvo perkelti iš „AX 2012“, ir naujus procesus, apimančius naujas funkcijas, kurios „Finance and Operations“ pasirodė pirmą kartą. 

Priklausomai nuo kodo kokybės, problemų sprendimas ir pakartotinis tikrinimas gali reikalauti keleto funkcinio testo pakartojimų. Kai problema išsprendžiama, būtinai dar kartą patikrinkite visus susijusius procesus, siekdami užtikrinti, kad pakeitimas nepaveikė proceso pabaigos arba pradžios.

Daugiau informacijos rasite [Tikrinti: funkcinis bandymas](upgrade-functional-validation.md).

### <a name="pre-go-live-checklist"></a>Kontrolinis sąrašas prieš galutinai paleidžiant
Kontrolinis sąrašas prieš galutinai paleidžiant yra rekomenduojama procedūra, padedanti sumažinti klaidų tikimybę per galutinį perkėlimą. Savaitę prieš galutinai paleidžiant nutraukite „AX 2012“ pakeitimus (dalyje \<modulis\>\nustatymas). Šis konfigūracijos pakeitimų apribojimas yra tik procedūrinis. „Microsoft Dynamics AX“ sistemos administratoriai tiesiog sutinka nuo to momento sustabdyti šio tipo pakeitimus.

Rekomenduojame, kad ir jūs nutrauktumėte „Finance and Operations“ kodo pagrindo pakeitimus. Jokie kiti pakeitimai neturi būti leidžiami, nebent jie buvo įvertinti ir parodyta, kad nekliudys galutiniam paleidimui.  

Kai konfigūracijos apribojimas ir kodo blokavimas yra vietoje, paskutinį kartą prieš visišką perkėlimą reikia atnaujinti duomenis. Taip galite užtikrinti, kad viskas veiks taip kaip tikimasi. 

Daugiau informacijos rasite [Tikrinti: pasiruošimas galutinai paleisti](upgrade-go-live-prep.md).



### <a name="supported-upgrade-paths"></a>Palaikomi naujinimo maršrutai
Nuo 2017 m. birželio naujinimas į „Microsoft Dynamics 365 for Finance and Operations“, „Enterprise“ leidimas, 0617 versija, palaikomas iš „Microsoft Dynamics AX 2012 R3“. Palaikomi visi kaupiamieji „AX 2012 R3“ naujinimai.

„Microsoft Dynamics AX 2012 R2“ ir „Microsoft Dynamics AX 2012 RTM“ šiuo metu nepalaikomos. Palaikymas bus įtrauktas vėliau 2017 m.

Palaikomas tik naujinimas į „Finance and Operations“ debesyje įdiegtą versiją. Nepalaikomas naujinimas į vietinę versiją. Naujinimo į vietinę versiją palaikymas bus įtrauktas vėliau 2017 m.

