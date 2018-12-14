---
title: "Darbų kūrimas, tvirtinimas ir registravimas sprendime „Attract“"
description: "Šioje temoje aprašomi „Attract“ darbo elementai. Taip pat paaiškinama, kaip sukurti darbą."
author: josaw
manager: AnnBe
ms.date: 10/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-24
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: af945042c150fff1a95cdb046f2a712cb2c2c061
ms.contentlocale: lt-lt
ms.lasthandoff: 10/24/2018

---

# <a name="create-approve-and-post-jobs-in-attract"></a>Darbų kūrimas, tvirtinimas ir registravimas sprendime „Attract“

[!include [banner](includes/banner.md)]

Šioje temoje aprašomi darbo elementai: „Microsoft Dynamics 365 for Talent: Attract“. Taip pat paaiškinama, kaip sukurti darbą.

## <a name="job-creation"></a>Darbo kūrimas

Darbo vietas gali kurti administratoriai, darbdaviai ir samdos vadovai. Kai sukursite darbą, būsite paraginti pasirinkti savo proceso vaidmenį: samdos vadovas arba įdarbintojas. Pasirinkę vaidmenį, būsite paraginti pasirinkti proceso šabloną. Jei pasirinksite **Praleisti**, naudojamas numatytasis šablonas. Daugiau informacijos apie proceso šablonus žr. [Proceso šablono kūrimas sprendime „Attract“](./process-templates-attract.md).

„Attract“ darbe nurodyta darbo informacija, samdos komanda, samdos procesas, darbo skelbimai ir analizė.

## <a name="job-details"></a>Darbo informacija

Skirtuke **Darbo informacija** pateikiama informacija apie darbo atsakomybes ir atributus. Pareigų pavadinimo, užduoties aprašo ir darbo vietos laukai turi būti užpildyti. Kiti laukai nėra būtini.

Pagal numatytuosius parametrus laukas **Laisvų darbo vietų skaičius** nustatytas į **1**. Tačiau reikšmę galite keisti. Kai darbo pasiūlymas paruoštas, lauko **Galimų laisvų darbo vietų skaičius** reikšmė sumažinama.

Jei pareigų valdymo funkcija įjungta administravimo centre, galima naudoti peržvalgą **Naujinti pareigas**. Ši peržvalga nuskaito „Common Data Service for Apps“ objektą JobPosition ir pateikia pareigų, kurias galima pasirinkti ir priskirti darbui, sąrašą. Jei pasirinktų pareigų skaičius viršija laisvų pareigų skaičių, gausite įspėjimą. Taip pat gausite įspėjimą, jei pareigos naudojamos keliuose darbuose.

> [!NOTE]
> Pareigų valdymo funkcija teikiama su išsamios įdarbinimo informacijos priedu.

Atsižvelgiant į samdos proceso pasiūlymo veiklos parametruose, pareigų skaičių pasiūlyme galima naudoti du kartus. Daugiau informacijos žr. [Samdos procesas](./activities-attract.md).

„Attract“ apima numatytąjį **įgūdžių** rinkinį. Šių įgūdžių rodomi kaip pasiūlymai jums įvedant tekstą. Galite įtraukti daugiau įgūdžių įvesdami naujo įgūdžio tekstą lauke ir tada paspausdami klavišą „Enter“.

„Attract“ apima numatytąjį **darbo funkcijų** rinkinį. Galite įtraukti iki trijų papildomų darbo funkcijų, lauke įvesdami naują darbo funkciją ir tada paspausdami klavišą „Enter“.

„Attract“ apima numatytąjį **įmonės pramonės** rinkinį. Galite įtraukti iki trijų papildomų įmonės pramonės šakų, lauke įvesdami naują įmonės pramonės šaką ir tada paspausdami klavišą „Enter“.

## <a name="hiring-team"></a>Samdos komanda

Skirtuke **Samdos komanda** pateikiamas asmenų, kurie bus įtraukti į darbą, sąrašas. Kai vartotojai įtraukiami į samdos komandą, jiems turi būti priskirtas samdos komandos vaidmuo. Vaidmuo apibrėžia duomenis, kuriuos vartotojai gali pasiekti, ir pranešimus, kuriuos jie gauna. Galima pasirinkti šiuos vaidmenis: **Įdarbintojas**, **Samdos vadovas**, **Perėmėjas** ir **Kalbintojas**. Daugiau informacijos apie vaidmenų teises žr. dokumente „Vaidmenų valdymas“. Įdarbintojai ir samdos vadovai gali paskirti vieną ar daugiau perėmėjų, kurie dirbs jų vardu. Daugiau informacijos apie perėmėjus žr. [Sauga ir vaidmenų valdymas sprendime „Attract“](./security-attract.md).

Samdos komandą galima atnaujinti, kai darbas suaktyvintas.

## <a name="process"></a>Procesas

Numatytoji samdos proceso informacija pagrėsta proceso šablonu, kuris buvo pasirinktas kuriant darbą. Jei tuo metu nebuvo pasirinktas konkretus šablonas, naudojamas numatytasis šablonas. Kai nustatote samdos procesą, galite įtraukti arba pašalinti įvairius etapus, išskyrus etapus Potencialus klientas, Prašymo teikimas ir Pasiūlymas. Nors etapo Potencialus klientas, pašalinti negalima, jį galima išjungti. Kiekviename etape galite įtraukti arba pašalinti vieną ar daugiau iš anksto nustatytų veiklų.

Daugiau informacijos apie veiklas, kurias galima įtraukti į samdos procesą, žr. [Samdos proceso veiklos sprendime „Attract“](./activities-attract.md).

> [!NOTE]
> Samdos proceso negalima atnaujinti, kai darbas suaktyvintas.

## <a name="postings"></a>Registravimai

Suaktyvinus darbą, jį galima registruoti. Darbus gali registruoti tik įdarbintojai ir administratoriai. Darbą galima registruoti puslapyje Talentų karjeros „Microsoft Dynamics 365 for Talent“ karjeros svetainėje arba „LinkedIn“. „Attract“ komanda nuolat bendradarbiauja su darbo skelbimų platformų kūrėjais. Todėl šis sąrašas bus išplėstas.

Daugiau informacijos apie darbo skelbimus žr. [Karjeros svetainės funkcija sprendime „Attract“](./career-site.md).

> [!NOTE]
> Darbo registravimo funkciją galima naudoti tik turint „Attract“ skirtą išsamios įdarbinimo informacijos priedą.

## <a name="activate"></a>Aktyvinti

Suaktyvinus darbą, galima jį užregistruoti ir į jį įtraukti potencialių klientų bei pretendentų. Potencialaus kliento įtraukimo į darbą parinktis nustatoma samdos proceso potencialaus kliento veikloje.

> [!NOTE]
> Samdos proceso negalima atnaujinti, kai darbas suaktyvintas.

## <a name="prospects-and-applicants"></a>Potencialūs klientai ir pretendentai

Potencialaus kliento įtraukimo į darbą parinktis nustatoma samdos proceso [potencialaus kliento veikloje](./activities-attract.md#prospect-activity). Ši parinktis turi būti nustatyta prieš suaktyvinant darbą. Suaktyvinus darbą, į jį galima įtraukti potencialių klientų bei pretendentų.

## <a name="approvals"></a>Patvirtinimai

„Attract“ galima pateikti tvirtinti. Ne visus darbus reikia tvirtinti. Reikalavimas nustatomas šablono lygiu. Pagal numatytuosius parametrus šablone tvirtinimai yra išjungti. Norėdami nustatyti tvirtinimus, atidarykite proceso šabloną ir nustatykite lauko **Tvirtinimas** parinktį Numatyta. Tada kurdami užduotį pasirinkite šabloną.

Išsaugojus darbą, galima jį pateikti tvirtinti. Šioje lentelėje išvardijamos dokumento, kuriame naudojami tvirtinimai, būsenos.

| Būsena   | Apskritis                                                               |
|----------|---------------------------------------------------------------------|
| Juodraštis    | Darbas buvo įrašytas, tačiau jis buvo pateiktas į darbo eigą. |
| Laukiama  | Darbas buvo pateiktas tvirtintojams.                            |
| Aprobuota | Darbas buvo patvirtintas, bet nebuvo suaktyvintas.            |
| Atmestas | Darbas buvo atmestas ir jo negalima suaktyvinti.               |
| Aktyvusis   | Darbas buvo patvirtintas ir suaktyvuotas.                            |

Darbų sąraše galite filtruoti darbų būsenas.

Tvirtinimus galima siųsti bet kuriam įmonės „Microsoft Azure Active Directory“ („Azure AD“) vartotojui. Tvirtinimai paraleliai siunčiami visiems žmonėms, kurie nurodyti kaip tvirtintojai. Patvirtinus darbą, galima jį suaktyvinti.

Žmonės, kurie nurodyti tvirtintojai, gaus pranešimą sprendime „Attract“, kuris nurodys, kad jie turi patvirtinti elementą. Patvirtinimo elementas taip pat bus rodomas ataskaitų srities skiltyje **Priskirta jums**. Kai kas nors priima arba patvirtina užduotį, samdos komanda gaus pranešimą. Galiausiai samdos komanda gaus pranešimą, kai darbas yra patvirtintas.

## <a name="create-a-job"></a>Užduoties sukūrimas

Norėdami kurti darbą, atlikite toliau nurodytus veiksmus.

1. Pasirinkite **Darbai**.
2. Pasirinkite **Nauja**.
3. Lauke **Pareigų pavadinimas** įveskite pareigų pavadinimą. Lauke **Vaidmuo** įveskite savo vaidmenį.
4. Lauke **Šablonas** pasirinkite šabloną. Arba pasirinkite **Praleisti**. Jei pasirinksite **Praleisti**, naudojamas šablonas, kuris pažymėtas kaip numatytasis šablonas.

    Jei dokumentui taikomas tvirtinimo procesas, pasirinkite šabloną, kurio laukas **Tvirtinimo procesas** nustatytas į parinktį **Numatytasis**.

5. Skirtuke **Informacija** įveskite išsamią darbo informaciją. Laukai **Pareigų pavadinimas**, **Užduoties aprašas** ir **Darbo vieta** turi būti užpildyti.
6. Pasirinkite **Įrašyti**.
7. Skirtuke **Samdos komanda** įtraukite samdos vadovą, įdarbintoją arba kalbintoją.
8. Pasirinkite **Įrašyti**.
9. Skirtuke **Procesas** pagal poreikį įtraukite arba pašalinkite etapus.

    - Norėdami įtraukti etapą, pasirinkite **+ Naujas etapas**.
    - Norėdami pašalinti etapą, laikykite žymeklį virš etapo, kad jį pašalintumėte, tada pasirinkite pasirodantį šiukšliadėžės mygtuką.

        > [!NOTE]
        > Potencialus kliento, prašymo ir pasiūlymo etapų pašalinti negalima.

10. Pagal poreikį įtraukite arba pašalinkite veiklas.

    - Norėdami įtraukti veiklą, vilkite ją iš dešinėje pateikto sąrašo į atitinkamą etapą. Taip pat dukart spustelėkite veiklą ir pasirinkite, į kurį etapą norite ją įtraukti.
    - Norėdami veiklą pašalinti, veiklą išplėskite, tada veiklos antraštėje pasirinkite šiukšliadėžės mygtuką.

11. Pasirinkite **Įrašyti**.
12. Jei pasirinkote naudoti tvirtinimo procesą, atlikite toliau nurodytus veiksmus.

    1. Pasirinkite **+ Įtraukti tvirtintoją**, tada įveskite vartotoją, kuris turi „Azure AD“ paskyrą. Galite įtraukti kelis tvirtintojus.
    2. Pasirinkite **Siųsti tvirtintojams**.

    Darbo laukas **Darbo būsena** nustatomas į parinktį **Laukiama**. Kai lauko **Darbo būsena** reikšmė pasikeičia į **Patvirtinta**, darbą galima suaktyvinti.

13. Norėdami suaktyvinti darbą, pasirinkite **Aktyvinti**.
14. Norėdami registruoti užduotį, pasirinkite **Registravimas**, tada pasirinkite parinktį **Registruoti dabar**, pateiktą talentų karjeros svetainėje arba „LinkedIn“.
