---
title: "Kurkite dokumentus ar mokymus naudodami Užduočių įrašus"
description: "Šioje temoje aiškinama, kokie užduočių rašytuvą ir užduočių vadovai yra, kaip sukurti užduočių įrašus, ir kaip tinkinti užduočių &quot;Microsoft&quot; vadovai ir įtraukti juos į jūsų pagalbos."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 38bce4a843f0db575c8d1ba08b7dc2ece8366663
ms.lasthandoff: 03/31/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Kurkite dokumentus ar mokymus naudodami Užduočių įrašus
Šioje temoje aiškinama, kokie užduočių rašytuvą ir užduočių vadovai yra, kaip sukurti užduočių įrašus, ir kaip tinkinti užduočių "Microsoft" vadovai ir įtraukti juos į jūsų pagalbos.

<a name="learn-about-task-recorder"></a>Sužinokite daugiau apie Užduočių įrašytuvą
-------------------------

Užduočių rašytuvas yra Microsoft Dynamics 365 operacijų įrankis, kurį naudodami galite įrašyti veiksmus, kuriuos galite atlikti produkto vartotojo sąsajos (UI). Kai naudojate Užduočių įrašytuvą, fiksuojami visi įvykiai, kuriuos atliekate naudotojo sąsajoje su serveriu, įskaitant reikšmių pridėjimą, nuostatų keitimą, duomenų šalinimą. Veiksmai, kuriuos įrašote, bendrai vadinami *užduoties įrašu*. Užduočių įrašus galima naudoti įvairiais būdais.

-   **Užduočių įrašus galima paleisti kaip užduočių vadovus.** Užduočių vadovai yra neatskiriama dalis Dynamics 365 patirtį operacijų pagalba. Užduoties vadovas yra kontroliuojamas, ekskursijos, interaktyvios patirties verslo proceso veiksmus. Naudotojui atlikti kiekvieną veiksmą nurodoma iššokančiuoju raginimu („burbuliuku‟), kurio animacija rodoma visoje UI ir kuris nurodo į UI elementą, su kuriuo naudotojas turėtų sąveikauti. "Burbulo" taip pat pateikiama informacija apie tai, kaip bendrauti su elementų, tokių kaip "Spauskite čia" arba "Šiame lauke įveskite reikšmę." Užduoties vadovas veikia nuo vartotojo naudojamo duomenų rinkinio ir įvesto duomenys išsaugomi vartotojo aplinkoje.
-   **Užduoties įrašai gali būti rodomi kaip procesinių veiksmų pagalbos srityje.** Pagalbos srityje galite ieškoti ir Rodyti užduočių įrašus. Pagalbos srityje galite pasiekti spustelėdami į **?** Piktogramą, esančią viršutinėje naršymo juostoje arba jūs galite naudoti sarčiųjų klavišų derinį, **Ctrl + Shift +?**. Galite skaityti veiksmus užduoties įrašymas pagalbos srityje, arba galite pasirinkti žaisti kaip užduoties vadovas įrašymo, todėl jis padės jums per vartotojo Sąsają.
-   **Užduočių įrašus galima įrašyti į BPM.** Savo užduoties įrašą galite įrašyti į „Lifecycle Services‟ (LCS) verslo procesų modeliavimo įrankio (BPM) bibliotekos hierarchijos eilutę. Iš įrašo bus sugeneruotas veiksmų sąrašas ir verslo procesų srauto diagrama. Užduočių įrašus, įrašytą į BPM biblioteką galima įrodyti Dynamics "365" dėl veiklos, kaip žinynas.
-   **Užduočių įrašus galima įrašyti kaip „Word‟ dokumentus.** Taip galite lengvai kurti spausdinamus mokymo vadovus.

Galite sukurti savo užduoties įrašų, tenka užduotis įrašų pateikia "Microsoft" arba modifikuoti "Microsoft" pateiktą užduotį įrašai atspindi jūsų konfigūracijos. Daugiau informacijos apie užduočių rašytuvas, rasite [užduočių rašytuvą Dynamics 365 operacijoms](task-recorder.md).

## <a name="plan-your-task-recording"></a>Planuokite savo užduoties įrašą
Kurdami naują užduoties įrašą ar savo įrašą kurdami pagal „Microsoft‟ užduoties įrašą, turėkite omenyje toliau nurodytą informaciją.

-   Įrašą planuokite taip, kaip planuotumėte vaizdo įrašą. Visus sprendimus priimkite iš anksto.
-   Kartą ar du pereikite per verslo procesą jo neįrašydami, kad suprastumėte veiksmus.
-   Kai prieš įrašymą einate per procesą, atkreipkite dėmesį, kur naudojate sparčiuosius klavišus ar klavišą **Įvesti**, kad jų nenaudotumėte pačio įrašymo metu.
-   Identifikuokite tolesnius dalykus.
    -   Ar norite veiksmus sugrupuoti į papildomas užduotis? Papildomos užduotys vizualiai atskiria proceso dalis. Pavyzdžiui, jei kuriate įrašą, skirtą „Produkto kūrimui ir išleidimui‟, galbūt norėsite sugrupuoti veiksmus, kurių reikia norint sukurti produktą, o tada sugrupuoti veiksmus, kurių reikia norint produktą išleisti. Papildomos užduotys taip pat palengvina ilgesnių procesų skaitymą.
    -   Ar norite pridėti komentarų ir, jei taip, kur? Daugiau informacijos rasite toliau: „Skirtingų komentarų tipų supratimas‟.
    -   Kokias reikšmes pridėsite įvairiuose laukuose, atlikdami verslo proceso veiksmus? Naudinga žinoti, ką toliau pasirinksite ar įvesite, kad įrašant nereikėtų grįžti ar taisyti klaidų.

**Savo aprašus ir komentarus rašykite iš anksto**

-   Kiekvieno užduoties įrašo pradžioje yra aprašo laukas, kuriame galite įvesti įrašo įvadą. Naudinga aprašą parašyti ir įrašyti iš anksto atskirame dokumente, kad įrašydami galėtumėte jį nukopijuoti bei įklijuoti į įrašą. Tokiu būdu tikslinti tekstą galite ne įrašymo proceso metu. Tekstą iškerpant ir įklijuojant, įrašymo procesą galima vykdyti greičiau ir sklandžiau.
-   Prie kiekvieno užduoties įrašo veiksmo galite sukurti komentarų. Atkuriant užduoties vadovą, komentarai rodomi „burbuliuke‟ kaip pastabos virš ar žemiau veiksmo teksto. Žiūrint kaip pagalbos srityje, komentarai rodomi kaip inline teksto žingsnis. Kaip ir aprašą, komentarus naudinga parašyti ir įrašyti atskirame dokumente. Įrašydami užduoties įrašą, komentarus iškirpkite ir įklijuokite iš to dokumento.

**Supraskite skirtingus komentarų tipus** Visi komentarai nėra privalomi. Jų pridėkite tik kai jie naudotojui suteikia naudingos informacijos.

-   **Pavadinimas**: pavadinimas Anotacija pasirodys prieš žingsnis tekstą, užduotį įrašymo įrenginys automatiškai generuoja. Užduoties vadovas, pavadinimas komentaras rodomas virš automatiškai sugeneruotą teksto. Šį komentaro tipą naudokite norėdami paaiškinti, kodėl naudotojas atlieką veiksmą, arba norėdami suteikti papildomo konteksto.

Tai redagavimo sritis, kurią matote, kai kurdami įrašą pridedate komentarą. Įveskite komentaro pavadinimą lauke **Pavadinimas**. 

[![screen1](./media/screen1.png)](./media/screen1.png) 

Taip atrodo pavadinimo komentaras užduočių vedlio „burbuliuke‟. 

[![2 Fiberglass](./media/screen2.png)](./media/screen2.png)

-   **Pastabos.** Pastabų komentaras bus rodomas po veiksmo teksto, kurį automatiškai sugeneruoja užduočių įrašytuvas. Jis užduoties vadove bus matomas tik jei naudotojas užduoties vadovo burbuliuke spustelės saitą **Rodyti daugiau**. Šį komentaro tipą naudokite norėdami apibūdinti dalykus, kuriuos, norėdamas atlikti veiksmą, turi žinoti naudotojas.

Tai redagavimo sritis, kurią matote, kai kurdami įrašą pridedate komentarą. Įveskite pastabų komentarą lauke **Pastabos**. 

[![3](./media/screen3.png)](./media/screen3.png) 

Tai, kas pažymi komentarą atrodo "burbulas" užduočių vedlyje.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Info žingsnis**: šiuos komentarus kuriami dešiniuoju pelės klavišu valdiklį arba bet kur forma &lt;**užduočių rašytuvą**&lt; ** pridėti info žingsnis. ** Info veiksmus rodomi sunumeruoti žingsnis ne kokia vieta jį įterpti, nors jokių veiksmų buvo įrašytas vartotojo sąsaja. Galite pridėti formos lygio informacijos veiksmą arba su valdikliu susietą informacijos veiksmą. Kai informacijos veiksmas susietas su forma, leidžiant užduoties vadovą, jo „burbuliukas‟ atsiras kažkur formoje, be žymeklio. Kai info žingsnis yra susijęs su valdymo pultu, užduoties vadovas "burbulas" nukreips į kontrolės grojant užduoties vadovas. Pagalbos srityje info žingsnis komentaras pasirodys kaip sunumeruoti žingsnis su tekstą, kurį įvedėte. Naudoti informacijos priemonių parengti vartotojo tolimesnius veiksmus, apibūdinti priemones, kurių reikia padaryti ne Dynamics 365 operacijoms, arba kreiptis į kitus įrašus (nors jūs negalite sukurti hyperinks komentarai.).

**Nustatykite, kokia turėtų būti jūsų įrašo trukmė**

-   Naudotojas paprastai įrašą skaitys arba leis nuo pradžios iki pabaigos, todėl nejunkite veiksmų ar užduočių, kuriuos geriau atlikti atskirai.
-   Stenkitės neįrašinėti ilgo scenarijaus, apimančio kelis antrinius procesus. Pvz., „Naudokite parduotuvės klientų aptarnavimo tarnybą‟ yra per platu; jį išskaidykite į trumpesnes užduotis, pvz., „Priimti grąžinimus‟ ir „Pridėti į dovanų kortelę‟.
-   Jei užduotis gali būti atlikta kaip kelių skirtingų verslo procesų dalis, sukurkite atskirą jos įrašą, į kurį nurodyti galite kituose įrašuose.
-   Jei procesas apima keletą užduočių, kurias asmuo greičiausiai atlieka visas vienu metu, jas galite išsaugoti viename įraše, pvz., „Nustatykite ir priskirkite funkcijų profilius‟.
-   Jei kokia nors užduotis atliekama vieną kartą (pvz., konfigūracija), o iš karto po to atliekama kita užduotis, tačiau ši gali būti atliekama pakartotinai ir savarankiškai, jas išskaidykite į du užduočių įrašus.

**Nuspręsti, kur, UI, Norėdami pradėti įrašą** puslapio, kuriame esate Jei pradedate įrašyti užduoties įrašymas turi įtakos kuris puslapis rodomas užduoties vadovas. Pavyzdžiui, jei norite, kad jūsų darbo įrašymas į pateiktas pagalbos srityje, kai vartotojas spusteli pagalbos DK parametrų puslapyje, turite paleisti savo registravimo DK parametrų puslapyje. **Įrašus įrašykite kaip .axtr failus** Kai baigiate kurti ar redaguoti užduoties įrašą, jums pateikiamos kelios parinktys, kaip įrašą atsisiųsti ar įrašyti. Atsisiųsti failą galite kaip užduoties įrašo paketą (.axtr), kaip neapdorotą įrašo failą (.xml), kaip „Word‟ dokumentą arba jį įrašyti į LCS biblioteką. Naudinga užduoties įrašą visada įrašyti kaip užduoties įrašo paketo failą (.axtr). Taip bus lengviau failą prižiūrėti, jei vėliau reikėtų keisti procedūras ar komentarus. Jei failą norite atsisiųsti kaip „Word‟ dokumentą, taip pat jį įrašykite kaip užduoties įrašo paketo failą.

## <a name="create-your-task-recording"></a>Kurkite užduoties įrašą
Išsamiai pateiktus veiksmus, rasite [kaip sukurti užduočių įrašymo](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Kopijuokite ir tinkinkite „Microsoft‟ užduočių įrašus
Galite atsisiųsti ir redaguoti "Microsoft' užduočių įrašus ir juos naudoti savo žinyno dokumentacija ar mokomąją medžiagą. Norėdami atsisiųsti „Microsoft‟ užduoties įrašą, atlikite tolesnius veiksmus.

1.  Dynamics 365 operacijoms, Atidarykite užduočių rašytuvą. Užduočių įrašytuvas yra **Nuostatų** meniu.
2.  Užduočių įrašytuvo srityje spustelėkite **Prižiūrėti įrašą**.
3.  Srityje **Kur yra įrašas**, spustelėkite **Jis yra LCS bibliotekoje**.
4.  Spustelėkite **Pasirinkti LCS biblioteką**.
5.  Pasirinkite "Microsoft" pasaulinės bibliotekos.
6.  Medyje pasirinkite verslo procesų bibliotekos mazgą, su kuriuo susietas užduoties įrašas.
7.  Spustelėkite **GERAI**.
8.  Spustelėkite **Pradėti**.
9.  Šiuo metu, nesinaudojant įrašymas, keitimas laiptelius, kaip jūs einate į naujo įrašo ji. **Pastaba**: jei jums reikia tik pakeisti teksto įrašymo, galite atidaryti įrašyti į **redaguoti įrašymą 's komentarus** režimu, ir tada išsaugokite jį.
10. Įrašą atkūrę iki pabaigos, ekrano viršuje esančioje užduočių įrašytuvo juostoje spustelėkite **Sustabdyti**.
11. Pasirinkite, kaip norite įrašyti užduoties įrašą.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Jūsų užduotis įrašams pagalbos srityje
Parodyti savo pasirinktinės užduočių įrašų pagalbos srityje taip, kad galima atkurti kaip užduočių vadovai ar žiūrima kaip tekstą, galite įrašyti savo užduočių įrašus savo bibliotekoje, BPM, ir tada atnaujinti jūsų pagalbos sistemos parametrai rodo, kad bibliotekoje BPM. Daugiau informacijos rasite [prisijungti žinyno sistemoje.](../get-started/help-connect.md)

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Dinamika 365 operacijoms padėti](..\get-started\help-overview.md)

[Prijunkite žinynas](..\get-started\help-connect.md)

[Užduočių rašytuvas dinamikoje 365 operacijoms](task-recorder.md)

[Neseniai pridėti užduotį įrašymo funkcijos](\core\get-started\recently-added-editing-features-in-task-recorder)

[Sukurti naujas mokymo bibliotekas Dynamics AX per gyvavimo ciklo paslaugų naudodami užduočių rašytuvą (išorinė nuoroda)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Kurti turtingas Žinyno temose naudodami užduočių rašytuvą (išorinė nuoroda)](https://mbspartner.microsoft.com/AX/Videos/970)


