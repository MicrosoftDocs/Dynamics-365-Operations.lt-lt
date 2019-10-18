---
title: „Retail Modern POS“ (MPOS) ir „Cloud POS“ užduočių įrašymo priemonė bei žinynas
description: Šioje temoje aprašoma, kaip naudoti užduočių įrašymo priemonę „Retail Modern POS“ ir „Cloud POS“.
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 70fef8035fce7792b44a3d96d1fba342eae88541
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024757"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a>„Retail Modern POS“ (MPOS) ir „Cloud POS“ užduočių įrašymo priemonė bei žinynas

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip naudoti užduočių įrašymo priemonę „Retail Modern POS“ ir „Cloud POS“.

## <a name="overview"></a>Peržiūrėti

Užduočių įrašymo priemonė „Retail Modern POS“ arba „Cloud POS“ yra naujas sprendimas, kurį kuriant didelis dėmesys skirtas modifikavimo galimybėms padidinti. Ji pateikia lanksčią tarnybos programavimo sąsają (API), kuri užtikrina išplėtimą ir sklandų integravimą su verslo proceso įrašų vartotojais. Be to, pristatytas užduočių įrašymo priemonės integravimas su „Microsoft Dynamics Lifecycle Services“ verslo procesų modeliavimo (BPM) įrankiu ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)). Todėl vartotojai gali toliau iš įrašų kurti vaizdingas verslo procesų diagramas, kad galėtų analizuoti ir kurti savo programas.

## <a name="architecture"></a>Architektūra

Užduočių įrašymo priemonė gali labai tiksliai įrašyti vartotojo veiksmus kliente. Kiekvienas valdiklis užduočių įrašymo priemonei praneša apie atliktą vartotojo veiksmą. Valdiklis praneša užduočių įrašymo priemonei, kad įvyko įvykis, ir perduoda visą reikiamą informaciją apie atitinkamą vartotojo veiksmą realiuoju laiku. Pagal šią informaciją užduočių įrašymo priemonė gali fiksuoti vartotojo veiksmo tipą (pvz., mygtuko spustelėjimą, vertės įrašymą arba naršymą) ir bet kokius duomenis, kurie susiję su vartotojo veiksmais (pvz., įvesties duomenų vertę ir tipą, formos kontekstą arba įrašo konteksto). Užduočių įrašymo priemonė įrašo informaciją pakankamai išsamiai ir užtikrina, kad atkuriant įrašą būtų galima atlikti įrašytus veiksmus lygiai taip pat, kaip juos atliko vartotojas. (Atkūrimo funkcija dar nėra įdiegta „Retail modern POS“ arba „Cloud POS“.)

## <a name="basic-configuration"></a>Pagrindinė konfigūracija

Norėdami įjungti užduočių įrašymą EKA, atlikite toliau nurodytus veiksmus.

1. Spustelėkite **Mažmeninė prekyba** &gt; **Kanalų sąranka** &gt; **EKA sąranka** &gt; **Registrai**.
2. Spustelėkite registrą, kuriame norite įjungti užduočių įrašymą.
3. Skirtuko **Registras** „FastTab“ **Bendra** nustatykite parinktį **Įjungti užduočių įrašymą** į **Taip**.
4. Spustelėkite **Įrašyti**.
5. Eikite į **Mažmeninė prekyba** &gt; **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.
6. Pasirinkite užduotį **Registrai (1090)** ir tada spustelėkite **Vykdyti dabar**.

## <a name="create-a-recording"></a>Įrašo kūrimas

Atlikite šiuos veiksmus, jei norite kurti naują įrašą naudodami užduočių įrašymo priemonę.

1. Paleiskite „Retail Modern POS“ arba „Cloud POS“ ir prisijunkite.
2. Puslapio **Parametrai** dalyje **Užduočių įrašymo priemonė** spustelėkite **Atidaryti užduočių įrašymo priemonę**. Pasirodo sritis **Užduočių įrašymo priemonė**. Galite spustelėti mygtuką **Uždaryti** (**X**) viršutiniame dešiniajame kampe, kad prieš pradėdami naują įrašymo veiksmą uždarytumėte sritį **Užduočių įrašymo priemonė**. Norėdami vėl atidaryti sritį, pakartokite 2 veiksmą.

    [![Sritis Užduočių įrašymo priemonė](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3. Įveskite įrašo pavadinimą bei aprašą ir spustelėkite **Pradėti**. Įrašymo sesija prasideda iškart, kai spustelėjate **Pradėti**.

    > [!NOTE]
    > Viršutiniame dešiniajame kampe spustelėjus mygtuką **Uždaryti** (**X**), kai vyksta įrašymas, sritis **Užduočių įrašymo priemonė** uždaroma, bet įrašymo seansas tęsiamas. Norėdami vėl atidaryti sritį Užduočių įrašymo priemonė, ekrano viršuje spustelėkite mygtuką **Žinynas** (klaustuko ženklas).
    >
    > [![Klaustuko ženklas](./media/help.jpg)](./media/help.jpg)

4. Kai spustelėsite **Pradėti**, įjungiamas užduočių įrašymo priemonės įrašymo režimas. Srityje **Užduočių įrašymo priemonė** rodoma informacija ir valdikliai, kurie susiję su įrašymo procesu.
5. Atlikti veiksmus, kuriuos norite atlikti „Retail Modern POS“ arba „Cloud POS“ vartotojo sąsajoje (UI).
6. Norėdami baigti įrašymo seansą, spustelėkite **Stabdyti**.

## <a name="download-options"></a>Atsisiuntimo parinktys

Užbaigus įrašymo seansą, rodomos kelios parinktys, kad galėtumėte atsisiųsti savo įrašą.

[![Atsisiuntimo parinktys](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Įrašyti šiame kompiuteryje

Galite naudoti įrašo paketą, norėdami atkurti užduočių vedlį, tvarkyti įrašą arba redaguoti įrašo komentarus. (Ši funkcija dar nėra įdiegta „Retail Modern POS“ arba „Cloud POS“.)

### <a name="export-as-word-document"></a>Eksportuoti kaip „Word“ dokumentą

Įrašą galite įrašyti kaip „Microsoft Word“ dokumentą. Dokumente bus įrašyti veiksmai ir užfiksuotos ekrano kopijos.

### <a name="save-as-developer-recording"></a>Įrašyti kaip kūrėjo įrašą

Neapdorotas įrašo failas naudingas kūrėjo scenarijams, pvz., norint patikrinti kodo generavimą. (Ši funkcija nėra dar neįdiegta.)

## <a name="recording-controls"></a>Įrašymo valdikliai

[![Įrašymo valdikliai](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>Sustabdyti

Norėdami baigti įrašymo seansą, spustelėkite **Stabdyti**. Atminkite, kad baigę seansą negalite jo paleisti iš naujo. Todėl prieš baigdami seansą įsitikinkite, kad įrašymas atliktas.

### <a name="pause"></a>Pauzė

Spustelėkite **Pristabdyti**, kad laikinai sustabdytumėte (pristabdytumėte) įrašymo seansą ir tęstumėte operaciją. Veiksmai, atlikti po to, kai spustelėjama **Pristabdyti**, neįrašomi.

### <a name="continue"></a>Tęsti

Norėdami tęsti įrašymo seansą po to, kai jį pristabdėte, spustelėkite **Tęsti**.

### <a name="capture-screenshots"></a>Užfiksuoti ekrano kopijas

Užduočių įrašymo priemonė gali fiksuoti „Retail Modern POS“ vartotojo sąsajos ekrano kopijas įrašinėjant verslo procesus. Norėdami įjungti ekrano kopijų fiksavimo funkciją, nustatykite parinktį **Fiksuoti ekrano kopijas** į **Taip**, o tada pradėkite įrašymą. Kai įrašymas baigtas, spustelėkite **Sustabdyti** ir atsisiųskite „Word“ dokumentą. Dokumente bus nurodyti veiksmai ir atitinkamos ekrano kopijos.

> [!NOTE]
> Ekrano kopijų fiksavimo funkcija nepalaikoma „Cloud POS“.

### <a name="start-task-and-end-task"></a>Užduoties pradėjimas ir baigimas

Galite nurodyti sugrupuotų veiksmų rinkinio pradžią ir pabaigą, naudodami mygtukus **Pradėti užduotį** ir **Baigti** **užduotį**. Spustelėkite **Pradėti užduotį**, kad įtrauktumėte veiksmą „Pradėti užduotį“, tada atlikite veiksmus, kuriuos reikia įtraukti į grupę. Atlikę grupės veiksmus, spustelėkite **Baigti užduotį**. Užduotys padeda tvarkyti savo procedūras. Užduotis galima įterpti į kitas užduotis. Tokiu būdu galima geriau tvarkyti labai ilgus ir sudėtingus verslo procesus.

## <a name="adding-annotations"></a>Komentarų įtraukimas

Komentaras yra papildomas tekstas, įtraukiamas į įrašo veiksmą. Pavyzdžiui, galite naudoti komentarus, norėdami vartotojui suteikti daugiau konteksto arba instrukcijų. Galite įtraukti komentarų prieš arba po veiksmo. Galite įtraukti komentarą į bet kurį veiksmą, spustelėdami mygtuką **Redaguoti** (pieštuko simbolis) dešinėje veiksmo pusėje.

[![Veiksmo mygtukas Redaguoti](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Tekstas ir pastabos

Galite naudoti laukus **Tekstas** ir **Pastabos**, norėdami įtraukti tekstą, kuris turi būti susietas su užduočių vedlio veiksmu.

[![Laukai Tekstas ir Pastabos](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Tekstas

Lauke **Tekstas** įvestas tekstas rodomas *virš* veiksmo teksto užduočių vedlyje. Ši vieta tinka tekstui, kurį vartotojas turėtų perskaityti prieš atlikdamas veiksmą.

#### <a name="notes"></a>Pastabos

Lauke **Pastabos** įvestas tekstas rodomas *po* veiksmo teksto užduočių vedlyje. Norėdamas perskaityti pastabų tekstą, vartotojas turi išplėsti veiksmo tekstą iššokančiajame lange. Ši vieta tinka norint pateikti pasirinktinę skaitomą medžiagą arba kitą informaciją, kuri gali būti naudinga vartotojui, bet nėra privaloma norint atlikti veiksmą.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>„Retail Modern POS“ ir „Cloud POS“ žinynas

Tam, kad tinkinti užduočių įrašai būtų pateikiami „Retail Modern POS“ ir „Cloud POS“ žinyno srityje ir juos būtų galima peržiūrėti kaip tekstą, užduočių įrašus turite įrašyti į savo BPM biblioteką, tada atnaujinti žinyno sistemos parametrus, kad būtų nurodoma BPM biblioteka. Norėdami gauti daugiau informacijos, žr. [Žinyno sistemos prijungimas](../fin-and-ops/get-started/help-connect.md). „Retail Modern POS“ ir „Cloud POS“ žinynas atlieka iešką LCS realiuoju laiku. Ieška vykdoma visose BPM bibliotekose, kurios pasirinktos „Retail“ žinyno sistemos parametruose, ir rodomi atitinkami rezultatai. Norėdami pasiekti meniu **Žinynas**, ekrano viršuje spustelėkite mygtuką **Žinynas** (klaustukas) ir ieškos lauke įveskite savo proceso pavadinimą bei spustelėkite ieškos mygtuką.

[![Mygtukas Pagalba](./media/help.jpg)](./media/help.jpg)

Ieškos rezultatuose spustelėjus užduočių vedlį, veiksmus galima peržiūrėti kaip žinyno temą arba eksportuoti į „Word“ dokumentą.

> [!NOTE]
> „Retail Modern POS“ ir „Cloud POS“ žinyno sistema neatidarys užduočių vedlių pagal jūsų atidarytą formą ar atliekamą operaciją. Proceso pavadinimą turite įvesti į ieškos lauką ir spustelėti **Ieškoti**.
