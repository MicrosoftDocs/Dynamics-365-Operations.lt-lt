---
title: "Perėjimo bandymas plėtojant"
description: "Šioje temoje paaiškinama, kaip išbandyti užduotis, vykstančias išjungus AX 2012, tačiau prieš įjungiant „Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimą."
author: tariqbell
manager: AnnBe
ms.date: 05/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations, UnifiedOperations, Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 711ad5cc3aafacf209704349effb4e08019205ac
ms.contentlocale: lt-lt
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-cutover-testing"></a>Perėjimo bandymas plėtojant

[!include[banner](../includes/banner.md)]

[!include[upgrade banner](../includes/upgrade-banner.md)]

Terminą *perėjimas* naudojame apibūdindami galutinį naujos sistemos paleidimo procesą. Perėjimo procesą sudaro užduotys, vykstančios išjungus „Microsoft Dynamics AX 2012‟, tačiau prieš įjungiant „Microsoft Dynamics 365 for Finance and Operations‟ „Enterprise‟ leidimą. Perėjimo bandymo plėtojant tikslas – išbandyti perėjimo procesą, kad būtų lengviau užtikrinti sklandų veikimą visiems asmenims, dalyvaujantiems faktinio perėjimo procese.

Perėjimo procesą sudaro du pagrindiniai darbo srautai, nurodyti toliau.

- **Techninis darbo srautas** – į šį darbo srautą įeina duomenų plėtojimo vykdymo procesas. Jūsų įmonė taikys leidžiamos prastovos limitą. Esant šiai prastovai nebus galima naudoti nei AX 2012, nei „Finance and Operations‟. Šis darbo srautas gali turėti pritaikyti duomenų plėtojimo procedūrą, kad atitiktų įmonės prastovos limitą.
- **Funkcinis darbo srautas** – į šį darbo srautą įeina konfigūravimo užduotys, atliekamos išplėtojus duomenis. Visos šios užduotys turi būti dokumentuotos ir įvertintos kiekybiškai, joms priskirti ištekliai, nes tiek funkcinis, tiek techninis darbo srautai turi atitikti įmonės prastovos limitą.

Tolesniame pavyzdyje parodytas visas perėjimo prie naujo sprendimo procesas, kuris bus vykdomas gamybos aplinkoje.

![Perėjimo procesas](./media/cutover_1.png)

Šis perėjimo procesas nuo pagrindinio duomenų plėtojimo smėlio dėžės aplinkoje skiriasi tolesniais aspektais.

- AX 2012 duomenų bazė nėra kopijuojama, o tik sukuriama jos atsarginė kopija, o tada modifikuojama pradinė duomenų bazė. Šis metodas yra greitesnis ir atsarginė kopija užtikrina keitimų atšaukimo galimybę, jei jos reikia.
- Kadangi „Finance and Operations‟ gamybos aplinkos prieiga yra ribota, užduotis, kurios anksčiau buvo atliekamos programos objektų serverio (AOS) smėlio dėžės egzemplioriuje, dabar atlieka „Microsoft‟ DSE komanda. Į šias užduotis įeina „bacpac‟ failo atsisiuntimas ir importavimas bei paketo MajorversionDataUpgrade.zip paleidimas.
- Įtraukėme tolesnes užduotis.

    - Bandymo atlikimas.
    - Programų sąrankos užduočių atlikimas. Šis veiksmas gali daug apimti – tai priklauso nuo naudojamų funkcijų. Atlikdama šį veiksmą funkcinė komanda sukonfigūruoja naujas programos funkcijas, kad ji būtų paruošta naudoti išplėtotoje sistemoje.
    - Sistemos naudojimo teisių grąžinimas vartotojams. Savo vartotojų bazei praneškite, kad sistema išplėtota ir kad jie vėl gali naudoti sistemą.

## <a name="technical-workstream"></a>Techninis darbo srautas

Techninis darbo srautas apima įvairius techninės komandos narius: duomenų bazės administratorių (DBA), AX 2012 sistemos administratorių, serverių administratorius ir programuotojus, kurie yra susipažinę su AX 2012 ir „Finance and Operations‟. Šioje temoje bus paaiškinta, kurios užduotys apima kuriuos vaidmenis.

Atlikdama perėjimo bandymus techninė komanda dėmesį skiria duomenų plėtojimo proceso našumo ir patikimumo bandymui, kad įsitikintų, jog laikomasi įmonės prastovos limito. Atliekant šį procesą naudojama daug aparatūros ir programinės įrangos elementų. Kai kurie iš šių elementų yra vietiniai, o kiti yra „Microsoft‟ debesyje. Be to, naudojama daug pasirinktinio programų kodo ir standartinio kodo elementų. Atlikus šiuos bandymus turėtų būti galima pasikliauti aplinkos perėjimo procesu.

### <a name="turn-off-the-ax-2012-aos-instances"></a>AX 2012 AOS egzempliorių išjungimas

Šią užduotį atlieka AX 2012 sistemos administratorius ir serverių administratoriai.

Reikia pasirinkti tolesnes sritis.

- **Perėjimo metu vykdomas paketines užduotis** – dėl jau paleistos ilgai vykdomos paketinės užduoties nebus galima sustabdyti sistemos. Planuokite į priekį, kad AOS egzempliorius galėtumėte sustabdyti norimu metu. Gali reikėti paketines užduotis suplanuoti, kad jos būtų baigtos dar iki išjungiant AX 2012.
- **Integruotas sistemas** – su jūsų AX 2012 aplinka gali būti integruota kitų sistemų. Norėdami išjungti AX 2012, į šias sistemas turite atsižvelgti savo plane. Pavyzdžiui, gali reikėti integruotas sistemas išjungti dar gerokai prieš išjungiant pačią AX 2012, kad būtų galima baigti visas likusias vykdomas operacijas. Įvairiose įmonėse integruotų sistemų reikalavimai labai skiriasi. Todėl jūsų ekspertų komanda šiai situacijai turi pasirengti atskirai.

### <a name="create-a-backup-of-the-ax-2012-database"></a>Atsarginės AX 2012 kopijos kūrimas

Ši užduotis apima DBA. Jei reikia atšaukti keitimus, bus naudojama atsarginė kopija. Ji taip pat bus naudojama kaip atskaitos taškas, kuris bus saugomas tam tikrą laikotarpį ir rodys sistemos būseną perėjimo momentu.

Reikia pasirinkti tolesnes sritis.

- Gaukite konkretų atsarginės kopijos kūrimo proceso laiką.
- Pakoreguokite naudojamas atsarginių kopijų parinktis (pavyzdžiui, glaudinimo ir ne), kad būtų užtikrinamas kiek įmanoma greitesnis atsarginių kopijų kūrimo procesas.

### <a name="export-the-database-to-bacpac"></a>Duomenų bazės eksportavimas į „bacpac‟

Ši užduotis apima DBA. Šios užduoties rezultatas – eksportavimo failas, kuris bus nusiųstas į naujos sistemos „Microsoft Azure‟.

Reikia pasirinkti tolesnes sritis.

- Gaukite konkretų atsarginės kopijos kūrimo proceso laiką.
- Optimizuokite eksportavimo procesą, kad būtų galima lengviau užtikrinti kiek įmanoma greitesnį veikimą. Norint optimizuoti, gali reikėti atlikti tolesnes užduotis.

    - Eksportuojant matuoti sistemos išteklius, pvz., CPU, disko įvestį / išvestį ir atmintį.
    - Radus ribotosios spartos išteklių sukurti jų mažinimo planą. Paprastai tokių ribotosios spartos išteklių mažinama priskiriant daugiau reikiamo ištekliaus.

### <a name="upload-the-bacpac-file-to-azure-storage"></a>„bacpac“ failo nusiuntimas į „Azure“ saugyklą

Ši užduotis apima DBA arba serverių administratorius. Atliekant šią užduotį, „bacpac‟ failas perkeliamas į „Azure‟.

Reikia pasirinkti tolesnes sritis.

- Pasirinkite įrenginį, kuris bus naudojamas nusiunčiant, ir įsitikinkite, kad sukonfigūruotas ir parengtas naudoti „Azure‟ naršyklės įrankis.
- Gaukite konkretų nusiuntimo proceso laiką kelis kartus jį matuodami. Nusiuntimo laikas skirsis – jis priklauso nuo jūsų interneto ryšio greičio ir „Azure‟ duomenų centro geografinės vietos jūsų vietos atžvilgiu.

### <a name="download-and-import-the-bacpac-file-to-the-azure-sql-database"></a>„bacpac‟ failo atsisiuntimas ir importavimas į „Azure SQL‟ duomenų bazę

Kai ši užduotis atsiranda perėjus prie naujos sistemos, ją vykdys „Microsoft‟ DSE komanda. Tačiau atliekant perėjimo bandymą ji apima jūsų DBA. Šios užduoties rezultatas – eksportavimo failas, kuris bus nusiųstas į naujos sistemos „Azure‟.

Reikia pasirinkti tolesnes sritis.

- Gaukite konkretų importavimo proceso laiką.
- Optimizuokite eksportavimo procesą, kad būtų galima lengviau užtikrinti kiek įmanoma greitesnį veikimą. Norint optimizuoti, gali reikėti atlikti tolesnes užduotis.

    - Eksportuojant matuoti sistemos išteklius. Štai keletas pavyzdžių:

        - **AOS įrenginyje:** CPU, disko įvestis / išvestis ir atmintis
        - **„Azure SQL Database‟ egzemplioriuje:** SQL duomenų bazės našumas (DTU). „Azure SQL‟ DTU galite stebėti AOS įrenginyje veikiančioje „Microsoft SQL Server Management Studio‟ pažvelgę į sistemos rodinį sys.dm_resource_stats.

    - Radus ribotosios spartos išteklių sukurti jų mažinimo planą. Paprastai tokių ribotosios spartos išteklių mažinama priskiriant daugiau reikiamo ištekliaus. Kadangi šio įrenginio veikimą užtikrina „Microsoft‟, nustatę ribotosios spartos išteklių ir norėdami jų padidinti, turite pateikti užklausą „Microsoft‟.

### <a name="run-the-majorversiondataupgradezip-package"></a>Paleiskite MajorVersiondataUpgrade.zip paketą

Kai ši užduotis atsiranda perėjus prie naujos sistemos, ją vykdys „Microsoft‟ DSE komanda. Tačiau atliekant perėjimo bandymą ji apima programuotojus. Atliekant šią užduotį sena duomenų bazės struktūra transformuojama į naujos sistemos struktūrą.

Atliekant šią užduotį taip pat vykdomas duomenų bazės sinchronizavimo procesas. Kai kuriais atvejais duomenų bazės sinchronizavimas gali trukti ilgai, pvz., kai lentelėje pasikeičia klasterinis indeksas, nes tai – daug išteklių reikalaujanti SQL operacija.

Primygtinai rekomenduojame analizę ir derinimo procesą pirmiausia atlikti programavimo aplinkoje. Smėlio dėžės aplinkoje derinimo ir analizės parinktys yra labiau ribotos. Siekiama, kad atliekant perėjimo bandymą problemų, kurias reikia spręsti, nebūtų arba jų būtų nedaug.

Reikia pasirinkti tolesnes sritis.

- Gaukite konkretų importavimo proceso laiką.
- Optimizuokite procesą, kad būtų galima lengviau užtikrinti greičiausią veikimą. Norint optimizuoti, gali reikėti atlikti tolesnes užduotis.

    - Naudojant lentelę ReleaseUpdateScriptsExecution stebėti atskirtų plėtotės scenarijų našumą.
    - Siekiant optimizuoti našumą, scenarijus koreguoti. Norint atlikti šią užduotį gali reikėti tinkinti scenarijaus X++ kodą, kad jis būtų optimizuotas jūsų duomenų rinkiniui.
    - Naudojant „Microsoft Dynamics Lifecycle Services‟ (LCS) stebėjimo funkciją arba „Management Studio‟ sistemos rodinį sys.dm_resources_stats stebėti „Azure SQL‟ DTU. Jei naudojami jau visi ištekliai, gali reikėti „Microsoft‟ DSE komandos prašyti didesnio duomenų bazės lygio.

### <a name="roll-back-to-ax-2012"></a>Grįžimas prie AX 2012

Šia užduotimi siekiama atkurti duomenų bazę naudojant atsarginę kopiją, kuri buvo sukurta išjungiant AX 2012, o tada vėl įjungti AX 2012. Taip pat gali reikėti atkurti integruotų sistemų būseną. Tačiau kadangi integruotos sistemos įvairiose įmonėse skiriasi, šiai situacijai turite pasirengti atskirai, atsižvelgdami į konkrečias aplinkybes. Nors nėra tikėtina, kad reikės grįžti, labai svarbu tam atvejui išbandyti procesą.

## <a name="functional-workstream"></a>Funkcinis darbo srautas

Išplėtojus duomenis, naujoje aplinkoje reikės atlikti keletą konfigūravimo užduočių. Šio darbo srauto tikslas – dokumentuoti ir kiekybiškai išmatuoti visas konfigūravimo užduotis ir kiekvienai užduočiai priskirti išteklių, kad būtų lengviau užtikrinti, jog šias užduotis galima atlikti kartu su techniniu darbo srautu per prastovos laikotarpį.

Paprastai atliekant funkcines užduotis keičiamos konkrečių sistemos parametrų ar kitų konfigūravimo duomenų reikšmės. Šios užduotys nustatomos naudojant visišką funkcinį testą, kuris yra atskira veikla nuo perėjimo bandymo. Nustačius šio tipo užduotį, ją reikia peržiūrėti kartu su funkciniu ištekliumi ir programuotoju.

Norint atlikti didesnius keitimus, gali reikėti sukurti naują pasirinktinį duomenų plėtotės scenarijų, kad duomenis būtų galima atnaujinti duomenų plėtotės proceso metu. Tačiau išplėtojus duomenis funkcinis išteklius mažesnius keitimus gali atlikti rankiniu būdu, naudodamas naują sistemą.

Didesnius keitimus su duomenų plėtotės scenarijais reikia išbandyti. Todėl reikės kartą ar kelis kartus paleisti paketą MajorVersionDataUpgrade.zip. Svarbu pasverti pakartotinio paketo paleidimo kaštus ir juos palyginti su rankinio duomenų įvedimo kaštais.

Atliekant kiekvieną rankinį keitimą, į perėjimo plano dokumentą reikia įtraukti užduotį. Su užduotimi turi būti rodoma tolesnė informacija.

-   Kokia tai užduotis ir ką reikia padaryti?
-   Kas ją turi atlikti?
-   Kiek ji trunka?

