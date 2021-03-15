---
title: Dokumentų ar mokymų kūrimas naudojant užduočių įrašymo priemonę
description: Šioje temoje paaiškinama, kas yra užduočių įrašymo priemonė ir užduočių vedliai, kaip sukurti užduočių įrašus bei kaip tinkinti „Microsoft“ užduočių vedlius ir juos įtraukti į žinyną.
author: josaw1
manager: AnnBe
ms.date: 03/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bc634a324e3cc12855a1b36b9a58a9cb38eb5d2
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092874"
---
# <a name="create-documentation-or-training-with-task-recorder"></a>Dokumentų ar mokymų kūrimas naudojant užduočių įrašymo priemonę

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kas yra užduočių įrašymo priemonė ir užduočių vedliai, kaip sukurti užduočių įrašus bei kaip tinkinti „Microsoft“ užduočių vedlius ir juos įtraukti į žinyną.

> [!IMPORTANT]
> Galite įrašyti savo užduotis vedlius, skirtus „Dynamics 365 Human Resources“, tačiau šiuo metu negalėsite jų įrašyti į verslo procesų modeliavimo įrankio (BPM) biblioteką arba jų atidaryti iš srities „Žinynas“. Galite juos įrašyti vietiniame diske arba tinklo vietoje ir tada atidaryti bei pakartotinai leisti naudodami užduočių įrašymo priemonę. 

<a name="learn-about-task-recorder"></a>Sužinokite daugiau apie Užduočių įrašytuvą
-------------------------

Užduočių įrašymo priemonė yra įrankis, naudojamas įrašyti veiksmams, kuriuos atliekate produkto vartotojo sąsajoje (UI). Kai naudojate Užduočių įrašytuvą, fiksuojami visi įvykiai, kuriuos atliekate naudotojo sąsajoje su serveriu, įskaitant reikšmių pridėjimą, nuostatų keitimą, duomenų šalinimą. Veiksmai, kuriuos įrašote, bendrai vadinami *užduoties įrašu*. Užduočių įrašus galima naudoti įvairiais būdais.

-   **Užduočių įrašus galima paleisti kaip užduočių vadovus.** Užduočių vedliai integruojami į žinyną. Užduočių vedlys – tai kontroliuojama, valdoma, interaktyvi priemonė, kuri naudojama atliekant verslo proceso veiksmus. Naudotojui atlikti kiekvieną veiksmą nurodoma iššokančiuoju raginimu („burbuliuku‟), kurio animacija rodoma visoje UI ir kuris nurodo į UI elementą, su kuriuo naudotojas turėtų sąveikauti. Burbuliuke taip pat pateikiama informacija apie sąveikavimo su elementu būdą, pvz., „Spustelėkite čia“ ar „Šiame lauke įveskite reikšmę“. Užduočių vedlys veikia naudodamas dabartinių vartotojo duomenų rinkinį, o įvesti duomenys įrašomi vartotojo aplinkoje.
-   **Užduočių įrašus galima įrašyti kaip „Word‟ dokumentus.** Taip galite lengvai kurti spausdinamus mokymo vadovus.

Galite kurti savo užduočių įrašus, leisti „Microsoft‟ pateiktus užduočių įrašus arba modifikuoti „Microsoft‟ pateiktus užduočių įrašus, kad jie atitiktų jūsų konfigūraciją. Norėdami gauti daugiau informacijos apie užduočių įrašymo priemonę, žr. [Užduočių įrašymo priemonė](task-recorder.md).

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
-   Prie kiekvieno užduoties įrašo veiksmo galite sukurti komentarų. Atkuriant užduoties vadovą, komentarai rodomi „burbuliuke‟ kaip pastabos virš ar žemiau veiksmo teksto. Komentarus peržiūrint kaip tekstą žinyno srityje, jie rodomi kaip įdėtasis veiksmo tekstas. Kaip ir aprašą, komentarus naudinga parašyti ir įrašyti atskirame dokumente. Įrašydami užduoties įrašą, komentarus iškirpkite ir įklijuokite iš to dokumento.

**Supraskite skirtingus komentarų tipus** Visi komentarai nėra privalomi. Jų pridėkite tik kai jie naudotojui suteikia naudingos informacijos.

-   **Pavadinimas**: pavadinimo komentaras bus pateikiamas prieš veiksmo tekstą, kurį automatiškai sugeneruoja užduočių įrašymo priemonė. Užduočių vedlyje pavadinimo komentaras pateikiamas virš automatiškai sugeneruoto teksto. Šį komentaro tipą naudokite norėdami paaiškinti, kodėl naudotojas atlieką veiksmą, arba norėdami suteikti papildomo konteksto.

Tai redagavimo sritis, kurią matote, kai kurdami įrašą pridedate komentarą. Įveskite komentaro pavadinimą lauke **Pavadinimas**. 

[![Redagavimo sritis su pavadinimo komentaru](./media/screen1.png)](./media/screen1.png) 

Taip atrodo pavadinimo komentaras užduočių vedlio „burbuliuke‟. 

[![Pavadinimo komentaro išvaizda užduočių vedlyje](./media/screen2.png)](./media/screen2.png)

-   **Pastabos.** Pastabų komentaras bus rodomas po veiksmo teksto, kurį automatiškai sugeneruoja užduočių įrašytuvas. Jis užduoties vadove bus matomas tik jei naudotojas užduoties vadovo burbuliuke spustelės saitą **Rodyti daugiau**. Šį komentaro tipą naudokite norėdami apibūdinti dalykus, kuriuos, norėdamas atlikti veiksmą, turi žinoti naudotojas.

Tai redagavimo sritis, kurią matote, kai kurdami įrašą pridedate komentarą. Įveskite pastabų komentarą lauke **Pastabos**. 

[![Redagavimo sritis su komentaru pastabų lauke](./media/screen3.png)](./media/screen3.png) 

Taip atrodo pastabų komentaras užduočių vedlio „burbuliuke‟.

[![Pastabų komentaro išvaizda užduočių vedlyje](./media/screen4.png)](./media/screen4.png)

-   **Informacijos veiksmas**: šie komentarai sukuriami dešiniuoju pelės mygtuku spustelėjus valdiklį ar bet kurią vietą formoje &lt; **Užduočių įrašymo priemonė** &lt; **Įtraukti informacijos veiksmą.** Informacijos veiksmas pateikiamas kaip sunumeruotas veiksmas bet kurioje vietoje, į kurią įterpsite šį veiksmą, nors vartotojo sąsajoje neįrašytas joks veiksmas. Galite pridėti formos lygio informacijos veiksmą arba su valdikliu susietą informacijos veiksmą. Kai informacijos veiksmas susietas su forma, leidžiant užduoties vadovą, jo „burbuliukas‟ atsiras kažkur formoje, be žymeklio. Kai informacijos veiksmas susietas su valdikliu, leidžiant užduočių vedlį jo „burbuliukas‟ bus nukreiptas į valdiklį. Žinyno srityje informacijos veiksmo komentaras bus pateikiamas kaip sunumeruotas veiksmas su bet kokiu įvestu tekstu. Naudokite informacijos veiksmus, kad padėtumėte vartotojui pasirengti tolesniems veiksmams, aprašytumėte veiksmus, kuriuos reikia atlikti ne programoje, arba nurodytumėte kitus įrašus (nors komentaruose hipersaitų kurti negalite).

**Nustatykite, kokia turėtų būti jūsų įrašo trukmė**

-   Naudotojas paprastai įrašą skaitys arba leis nuo pradžios iki pabaigos, todėl nejunkite veiksmų ar užduočių, kuriuos geriau atlikti atskirai.
-   Stenkitės neįrašinėti ilgo scenarijaus, apimančio kelis antrinius procesus. Pvz., „Naudokite parduotuvės klientų aptarnavimo tarnybą‟ yra per platu; jį išskaidykite į trumpesnes užduotis, pvz., „Priimti grąžinimus‟ ir „Pridėti į dovanų kortelę‟.
-   Jei užduotis gali būti atlikta kaip kelių skirtingų verslo procesų dalis, sukurkite atskirą jos įrašą, į kurį nurodyti galite kituose įrašuose.
-   Jei procesas apima keletą užduočių, kurias asmuo greičiausiai atlieka visas vienu metu, jas galite išsaugoti viename įraše, pvz., „Nustatykite ir priskirkite funkcijų profilius‟.
-   Jei kokia nors užduotis atliekama vieną kartą (pvz., konfigūracija), o iš karto po to atliekama kita užduotis, tačiau ši gali būti atliekama pakartotinai ir savarankiškai, jas išskaidykite į du užduočių įrašus.

**Nuspręskite, kurioje UI vietoje pradėti įrašą** Puslapis, kuriame esate pradėdami įrašyti užduoties įrašą, nulems puslapį, kurį pateiks užduočių vedlys. Pavyzdžiui, jei norite, kad užduoties įrašas žinyno srityje būtų pateikiamas vartotojui DK parametrų puslapyje spustelėjus žinyną, įrašą pradėti turite DK parametrų puslapyje. **Įrašus įrašykite kaip .axtr failus** Kai baigiate kurti ar redaguoti užduoties įrašą, jums pateikiamos kelios parinktys, kaip įrašą atsisiųsti ar įrašyti. Atsisiųsti failą galite kaip užduoties įrašo paketą (.axtr), kaip neapdorotą įrašo failą (.xml), kaip „Word‟ dokumentą arba jį įrašyti į LCS biblioteką. Naudinga užduoties įrašą visada įrašyti kaip užduoties įrašo paketo failą (.axtr). Taip bus lengviau failą prižiūrėti, jei vėliau reikėtų keisti procedūras ar komentarus. Jei failą norite atsisiųsti kaip „Word‟ dokumentą, taip pat jį įrašykite kaip užduoties įrašo paketo failą.

## <a name="create-your-task-recording"></a>Kurkite užduoties įrašą
Išsamius instrukcijų veiksmus žr. [Užduočių įrašymo priemonės ištekliai](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Kopijuokite ir tinkinkite „Microsoft‟ užduočių įrašus
Galite atsisiųsti bei redaguoti „Microsoft‟ užduočių įrašus ir juos naudoti žinyno dokumentacijoje ar mokymo medžiagoje. Norėdami atsisiųsti „Microsoft‟ užduoties įrašą, atlikite tolesnius veiksmus.

1.  Atidarykite užduočių įrašymo priemonę. Užduočių įrašytuvas yra **Nuostatų** meniu.
2.  Užduočių įrašytuvo srityje spustelėkite **Prižiūrėti įrašą**.
3.  Srityje **Kur yra įrašas**, spustelėkite **Jis yra LCS bibliotekoje**.
4.  Spustelėkite **Pasirinkti LCS biblioteką**.
5.  Pasirinkite „Microsoft“ visuotinę biblioteką.
6.  Medyje pasirinkite verslo procesų bibliotekos mazgą, su kuriuo susietas užduoties įrašas.
7.  Spustelėkite **GERAI**.
8.  Spustelėkite **Pradėti**.
9.  Šiame etape pereidami per įrašo veiksmus galite juos keisti – įrašas bus perrašytas. **Pastaba**. Jei reikia pakeisti tik įrašo tekstą, įrašą galite atidaryti esant režimui **Redaguoti įrašo komentarus** ir tada jį įrašyti.
10. Įrašą atkūrę iki pabaigos, ekrano viršuje esančioje užduočių įrašytuvo juostoje spustelėkite **Sustabdyti**.
11. Pasirinkite, kaip norite įrašyti užduoties įrašą.



<a name="additional-resources"></a>Papildomi ištekliai
--------

[Žinyno sistema](../../fin-ops/get-started/help-overview.md)

[Žinyno sistemos prijungimas](../../fin-ops/get-started/help-connect.md)

[Užduočių įrašymo priemonė](task-recorder.md)

[Naudingų žinyno temų kūrimas naudojant užduočių įrašymo priemonę (išorinis saitas)](https://mbspartner.microsoft.com/AX/Videos/970)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]