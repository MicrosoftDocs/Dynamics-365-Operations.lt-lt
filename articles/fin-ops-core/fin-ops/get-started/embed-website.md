---
title: Įdėtos trečiosios šalies programėlės
description: Šioje temoje aiškinama, kaip įdėti trečiosios šalies programas siekiant padidinti produkto funkcijų skaičių.
author: jasongre
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b0471fd2ea9a5e8b07b9e8bc279da53f6a1539ca
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7345415"
---
# <a name="embed-third-party-apps"></a>Įdėtos trečiosios šalies programėlės

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Daugelis klientų verslui vykdyti naudoja įvairias programas. Kai kurios iš šių programų yra trečiųjų šalių žiniatinklio programėlės, kurios veikia kartu su „Finance and Operations“ programėle. Norėdami užtikrinti, kad vartotojas veiktų sklandžiai, galite naudoti viso puslapio programėlių funkciją, kad jos būtų įdėtos tiesiogiai į programėles (jei trečiosios šalies programėlės leidžia **save** „Finance and Operations“ įdėti). Tokiu būdu vartotojai gali pasiekti svetaines ir programėles, kurių jiems reikia, kad jiems nereikia perjungti skirtukų ar langų.

Kad būtų galima į produktą įdėti trečiųjų šalių programėles, funkcijų valdymo funkcija turi įjungti **viso puslapio programėles**. Tada, norėdami įdėti trečiosios šalies programą ar svetainę, galite naudoti vieną iš toliau nurodytų metodų. Šie metodai yra analoginiai metodams, kurie naudojami įdėtoms žiniatinklio programoms iš „Microsoft Power Apps“ į „Finance and Operations“ programėles.

- Į esamą puslapį įdėti programą ar svetainę kaip naują skirtuko puslapį (pagrindinį tabuliacijos skirtuką, „FastTab", „uždavimo" arba darbo srities skyrių).
- Naudodami skelbimų skelbimų sritį sukurkite naują programos arba svetainės viso puslapio patirtį.

## <a name="embed-a-website-on-an-existing-page"></a>Svetainė įdėta į esamą puslapį

Šią procedūrą naudokite, jei norite pridėti esamą sistemos puslapį įdėtąją programa.

1. Atidarykite puslapį, kuriame norite įdėti drobės programą.
2. Atidarykite **Įtraukti programą** juostoje:

    1. Pasirinkite **Nustatymai** ir tada **Suasmeninkite** tam, kad atidarytumėte **Personalizavimo** įrankių juostą.
    2. Pasirinkite **Daugiau \> įtraukti** programą.

3. Pasirinkite puslapio regioną, į kurį norite įtraukti programą. Šis regionas turi būti *suvestinės* skirtuko, „FastTab", „FastTab", „blokavimo" arba darbo srities skyriaus skirtukų konteineris.
4. Pasirinkite **svetainę**.
5. Konfigūruokite įdėtąją programą, atlikę tolesnius veiksmus.

    - **Pavadinimas** – įveskite tekstą, kuris turi būti rodomas skirtuke, kuriame yra įdėtoji programa. Dažnai norite, kad šis tekstas būtų programos pavadinimas.
    - **URL** – Nurodykite programos vietą.

    > [!IMPORTANT]
    > - Saugumo sumetimais URL turi naudoti „Hypertext Transfer Protocol Secure“ (HTTPS).
    > - Programa arba žiniatinklio svetainė turi būti sukonfigūruota taip, kad galėtų būti įdėtoji.

6. Pasirinkite **Įrašyti**, kad į puslapį įdėtumėte programą. Programa pridedama kaip paskutinis skirtukas arba grupės skyrius.
7. Patvirtinkite, kad programa atrodo taip, kaip tikėtasi. Jei programa nėra atvaizduota, žr. toliau šios temos [skyriuje](#troubleshooting) Trikčių diagnostika.
8. Atidarykite rodinio išrinkiklį ir pasirinkite Įrašyti (jei programa turi būti susieta su dabartiniu rodiniu) arba Įrašyti kaip (norėdami įrašyti **programą** į kitą **rodinį**).

    Jei puslapyje nėra rodinio išrinkiklis (pvz., jei puslapis yra dialogo langas arba darbo sritis), šį veiksmą galite praleisti.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Svetainė įdėta kaip viso puslapio patirtis iš skelbimų skelbimų lentos

Šią procedūrą naudokite, jei programa, kurią norite įdėti, nėra susijusi su esamu puslapiu arba jei norite, kad programai programoje būtų rodomas visas „Finance and Operations“ puslapis.

1. Atidarykite numatytąją ataskaitų sritį.
2. Pasirinkite ir laikykite (arba spustelėkite dešiniuoju pelės mygtuku) ataskaitų sritį, pasirinkite **Pritaikyti asmeniniams poreikiams**, tada pasirinkite **Įtraukti puslapį**.
3. Srityje **Įtraukti puslapį** pasirinkite **Žiniatinklio svetainė**.
4. Konfigūruokite įdėtąją programą, atlikę tolesnius veiksmus.

    - **Pavadinimas** – įveskite tekstą, kuris turi būti rodomas ant išklotinės dalies, kuri pridėta prie įdėtosios programos skelbimų srityje. Dažnai norite, kad šis tekstas būtų programos pavadinimas.
    - **URL** – Nurodykite programos vietą.

    > [!IMPORTANT]
    > - Saugos sumetimais URL turi naudoti HTTPS.
    > - Programa arba žiniatinklio svetainė turi būti sukonfigūruota taip, kad galėtų būti įdėtoji.

5. Norėdami **įtraukti programą į** skelbimų skelbimų skelbimų sritį kaip naują išklotąją sritį, pasirinkite Įrašyti.
6. Pasirinkite naują skelbimų lentos išklotinę programą ir patvirtinkite, kad programa atrodo taip, kaip tikėtasi. Jei programa neatvaizduojama, žr. toliau šios temos skyrių [Trikčių šalinimas](#troubleshooting).

## <a name="sharing-embedded-apps"></a>Įdėtųjų programų bendrinimas

Kai įdėjote programą naudodami vieną iš ankstesniuose skyriuose aprašytų metodų, galite norėti bendrai naudoti rodinį su kitais sistemos vartotojais. Norėdami bendrai naudoti įdėtąją programą, naudokite vieną iš šių būdų:

- **Publikuoti rodinį (rekomenduojama):** jei įdėtoji programa buvo įrašyta į rodinį, rekomenduojamas ir pageidaujamas būdas ją bendrinti yra skelbti rodinį vartotojams, kurie turi tinkamus saugos vaidmenis tiksliniuose juridiniuose objektuose. Tokiu atveju tik norimi vartotojai matys šią įdėtąją programą šiame puslapyje. Daugiau informacijos, kaip publikuoti įsigijimo katalogą, žr. [Publikavimo rodiniai](saved-views.md#publishing-views).

    Taip pat galite publikuoti programą, kuri skelbimų srityje buvo įdėtoji kaip viso puslapio informacija. Skelbimų srityje pasirinkite ir laikykite (arba spustelėkite dešiniuoju pelės mygtuku) išklotąją dalį, susijusią su programa, pasirinkite Personalizuoti, tada **pasirinkite** puslapį **Publikuoti**. Rodoma patirtis, panaši į patirtį *Publikavimo rodiniai*, ir galite pasirinkti saugos vaidmenis, į kuriuos ją publikuosite. Jei 10.0.21 arba naujesniame naujinyje įjungta funkcija **Įrašytų rodinių pagerintas juridinių subjektų palaikymas**, taip pat galite publikuoti programą į norimus juridinius objektus.

- **Kopijuokite personalizavimą: puslapiams, kurie nepalaiko rodinių (pvz., dialogo langų ar darbo sričių), arba, jei naudojate viso puslapio programą, galite nukopijuoti personalizavimą** atitinkamiems vartotojams. Daugiau informacijos rasite skyriuje [Personalizavimų bendrinimas](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Įdėtųjų programų peržiūra

Norėdami įdėtąją drobės programą peržiūrėti „Finance and Operations“ programų puslapyje, tiesiog atidarykite puslapį, kuriame yra įdėtoji programa. Atminkite, kad kai kuriuose puslapiuose, įdėtas programas galima pasiekti naudojant mygtuką **„Power Apps”**, esantį standartinėje veiksmų srityje. Taip pat jos gali atsirasti puslapyje tiesiogiai kaip naujas skirtukas, „FastTab“, mentė arba nauja skiltis darbo srityje.

## <a name="editing-or-removing-embedded-apps"></a>Įdėtųjų programėlių redagavimas arba šalinimas

Kai puslapyje įdėta programa, gali tekti redaguoti jos konfigūraciją (pavyzdžiui, keičiant skyriaus žymę arba URL). Taip pat gali tekti pašalinti jį iš puslapio. Norėdami redaguoti įdėtosios programos konfigūraciją arba visiškai pašalinti, naudokite vieną iš toliau nurodytų procedūrų.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Esamose puslapiuose įdėtos programėlės

1. Atidarykite puslapį, kuriame norite įdėti programą.
2. Pasirinkite **Nustatymai** ir tada **Suasmeninkite** tam, kad atidarytumėte **Personalizavimo** įrankių juostą.
3. Pasirinkite įrankį **Pasirinkti**, o tada pasirinkite įdėtąją programą.
4. Norėdami redaguoti programą, atlikite reikalingus konfigūracijos pakeitimus ir pasirinkite **Įrašyti**.

    Arba, norėdami pašalinti programą, pasirinkite **Naikinti**.

5. Iš naujo įrašykite arba paskelbkite rodinį. Atkreipkite dėmesį, kad jei išeisite iš puslapio tiesiogiai neįrašę rodinio, nebus tvarkomi veiksmai, atlikti redagavimo **svetainės** srityje.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Iš skelbimų lentos įdėtosios programėlės

1. Atidarykite numatytąją ataskaitų sritį.
2. Pasirinkite ir laikykite (dešiniuoju klavišu) pavadinimą, kuris susietas su patalpinta programa ir tada rinkitės **Personalizuoti**.
3. Norėdami redaguoti programą, pasirinkite **Redaguoti** puslapį. Juostoje **Redaguokite svetainę** rinkitės būtinus keitimus programos konfigūracijoje ir tada rinkitės **Įrašyti**.

    Arba, norėdami pašalinti programą, pasirinkite **Panaikinkite puslapį**.

## <a name="appendix"></a>Priedas

### <a name="troubleshooting"></a>Trikčių šalinimas

Jei svetainė nebus tinkamai atvaizduota po to, kai ji bus įdėta į „Finance and Operation“ programą, arba jei gausite klaidos pranešimą, kuriame teigiama, kad URL buvo atmestas, galbūt svetainė sukonfigūruota taip, kad nebūtų įdėta pati į „iframe“. Norėdami nustatyti, ar galima įdėti svetainę, atlikite šiuos veiksmus.

1. Atidarykite programuotojo įrankius, siųsdami naršyklę, kurią naudojate.
2. Skirtuke **Tinklas** raskite ir pasirinkite atsakymą iš įdėtosios svetainės.
3. Skirtuko **Antraštės** dalyje Atsakymo **antraštės ieškokite** x **rėmelio** pasirinkčių. Jei atsakymų antraštėse yra x rėmo pasirinktys ir jų  **vertė** YRA DENY **arba** ta pati kilmė **, svetainės šiuo metu** įdėti negalima. Turėsite dirbti su programos savininku, kad ji būtų saugiai įdėtoji.

### <a name="developer-modeling-a-website-on-a-form"></a>[Programuotojas] Svetainės modeliavimas formoje

Nors ši tema skirta įdėtoms trečiųjų šalių programėles ar svetaines naudojant personalizavimą, programuotojai taip pat gali įtraukti jas į formą naudodami „Visual Studio“ programavimo patirtį. Tiesiog įtraukite **WebsiteHostControl** valdiklį į formą. Valdiklyje galimos metaduomenų ypatybės, kurios prieinamos ir suteikia tų pačių galimybių kaip ir personalizavimo funkcijos.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
