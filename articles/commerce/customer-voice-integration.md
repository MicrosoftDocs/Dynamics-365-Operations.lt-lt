---
title: „Customer Voice“ integravimas į el. prekybos svetainės puslapius
description: Šiame straipsnyje aprašoma, kaip integruoti "Microsoft Dynamics 365 Customer Voice " į Dynamics 365 Commerce el. komercijos svetainės puslapius.
author: samjarawan
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: c8c67ecf4950c92fc91c8d119e06e5e8afff0ddf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850335"
---
# <a name="integrate-customer-voice-into-e-commerce-site-pages"></a>„Customer Voice“ integravimas į el. prekybos svetainės puslapius

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip integruoti "Microsoft Dynamics 365 Customer Voice " į Dynamics 365 Commerce el. komercijos svetainės puslapius.

Norėdami rinkti [, analizuoti ir](https://dynamics.microsoft.com/customer-voice/overview/) stebėti klientų grįžtamąjį ryšį realiuoju laiku, galite integruoti Klientų Į savo el. komercijos svetainę. Norėdami pradėti integravimą, turite sukurti sąskaitą ir pasirinkti norimo rinkti grįžtamojo ryšio kliento Darbo projekto šabloną.

## <a name="integrate-the-customer-voice-service"></a>Integruoti klientų į darą paslaugą

Norėdami sukurti kliento Į žurnalo sąskaitą, eikite į [Kliento Vykdykite](https://dynamics.microsoft.com/customer-voice/overview/) ir vykdykite raginimus.

Po to, kai sukuriate kliento "Žurnalo" sąskaitą ir prisiregistruosite, pasirinkite norimo rinkti grįžtamojo ryšio tipo projekto šabloną.

Norėdami pasirinkti kliento "Aptarnavimo" projekto šabloną, atlikite šiuos veiksmus.

1. Eiti į kliento [Aptarnavimo projekto šablono puslapį](https://customervoice.microsoft.com/Pages/ProjectPage.aspx).
1. Pasirinkite **Pradėti**.
1. Pasirinkite grįžtamojo ryšio tipo projekto šabloną, kurį norite rinkti, tada pasirinkite **Pirmyn**.
1. Skirtuko Siųsti **dalyje** Pasirinkite įdėtojo **formato pasirinkite** įdėtinį formatą. Lauke **Įdėtasis** kodas rodomas kodas, kuris turi būti įdėtas į Komercijos svetainės generatorių.

Šiame straipsnyje pateikti pavyzdžiai naudoja periodinių klientų **apklausų projekto** šabloną ir įdėtojo **mygtuko** formatą.

Šiame pavyzdyje parodyta **periodinės** kliento apklausos projekto šablono puslapis, **kuriame** pasirinkta formato mygtuko įdėtis pasirinktis, **ir tos pasirinkties įdėtojo kodo kodas pasirodo lauke Įdėtasis** kodas. Trys atskiri veiksmai yra būtini, kad pateiktas kodas būtų įdėtas į jūsų svetainės puslapius, kaip aprašyta toliau skyriuose.

![Kliento Kvalifikacijos periodinės kliento apklausos puslapis su pasirinkta mygtuko pasirinktimi.](media/customer-voice-integration-1.png)

### <a name="embed-the-external-script-url"></a>Įdėtas išorinio scenarijaus URL

Visuose svetainės puslapiuose, kurie turi turėti kliento "Pagal kliento apklausą", turite įdėti išorinį scenarijaus URL, kurį klientas Parinktys pateikė į įdėtąjį kodą. Geriausias būdas įdėti scenarijų į kelis svetainės puslapius yra sukurti fragmentą svetainės generatoriuje, kuriame yra išorinio scenarijaus URL, ir tada pridėti fragmentą prie atitinkamų puslapių šablonų. Kai publikuojate atnaujintą šabloną, įdėtasis išorinis scenarijaus kodas paveiktame svetainės puslapiuose bus panašus į šį pavyzdį.

```html
<script src=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.js type="text/javascript"></script>
```

Norėdami gauti informacijos apie fragmentus, žr. [darbą su fragmentais](work-with-fragments.md).

> [!NOTE]
> Jums reikia tik įtraukti URL į fragmentą. Išorinis scenarijaus modulis įtrauks kitą scenarijaus kodą.

Norėdami įterpti išorinį scenarijaus URL į fragmentą, atlikite šiuos veiksmus.

1. Svetainės generatoriuje sukurkite fragmentą, pagrįstą išoriniu [scenarijaus moduliu](script-module.md).
1. Naujame fragmente pasirinkite numatytojo išorinio **scenarijaus laiko atminties** skaidytį.
1. Numatytojo **išorinio scenarijaus** ypatybės srityje, **Scenarijų** šaltinio lauke, įveskite išorinio scenarijaus URL, kaip parodyta toliau pateiktame pavyzdyje.

    ![Naujo fragmento išorinio scenarijaus URL scenarijų šaltinio lauke.](media/customer-voice-integration-2.png)

1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Norėdami **publikuoti fragmentą**, pasirinkite Publikuoti.

Naujas fragmentas, kuriame yra įdėtasis išorinis scenarijaus blokas, dabar yra parengtas pridėti prie atitinkamo puslapio šablono.

### <a name="embed-the-external-style-sheet-code"></a>Įdėtas išorinis stiliaus aprašo kodas

Po to visuose svetainės puslapiuose, kurie turi turėti apklausą apie klientą, turite įdėti išorinį stilių aprašo kodą, kurį kliento meniu pateikė įterpimo kodas. Kaip ir ankstesniame skyriuje, geriausias būdas išorinio stiliaus aprašo kodą įdėti į kelis svetainės puslapius yra sukurti fragmentą svetainės generatoriuje, kuriame yra stiliaus aprašo kodas, o tada pridėti fragmentą į atitinkamus puslapių šablonus. Įdėtasis išorinio stiliaus aprašo kodas bus panašus į toliau pateiktą pavyzdinį kodą.

```typescript
<link rel="stylesheet" type="text/css" href=https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/Embed.css />
```

Norėdami įterpti išorinį stiliaus aprašo kodą į fragmentą, atlikite šiuos veiksmus.

1. Svetainės generatoriuje sukurkite fragmentą, pagrįstą metatagų [moduliu](metatags-module.md).
1. Fragmente pasirinkite numatytųjų metaduomenų **atžymą**.
1. Numatytųjų **metaduomenų ypatybės** srityje metažymų **lauke** įveskite stiliaus aprašo kodą, kaip parodyta toliau pateiktame pavyzdyje.

    ![Naujo fragmento išorinio stiliaus aprašo kodas meta žymių lauke.](media/customer-voice-integration-3.png)

1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Norėdami **publikuoti fragmentą**, pasirinkite Publikuoti.

Naujas fragmentas, kuriame yra įdėtasis išorinio stiliaus aprašo kodas, paruoštas pridėti prie atitinkamo puslapio šablono.

### <a name="embed-the-inline-script-code"></a>Įdėtas įterpimo įterpimo scenarijaus kodas 

Po to visuose svetainės puslapiuose, kurie turi turėti apklausą apie klientą, turite įdėti įdėtą įterpimo kodą, kurį kliento meniu pateikė įterpimo kodas. Kaip ir ankstesniuose skyriuose, geriausias būdas įterpti inline scenarijaus kodą į kelis svetainės puslapius yra sukurti fragmentą svetainės generatoriuje, kuriame yra įdėtas įterpimo scenarijaus kodas, o tada pridėti fragmentą į atitinkamus puslapių šablonus.

Šiame pavyzdyje, kaip eilutės scenarijaus kodas, **SURVEY RAKTAS\_ yra** teksto ženklas. SURVEY RAKTO vertė **turi atitikti\_ faktinį apklausos raktą, kurį klientas Turi pridėti prie įdėtųjų kodų.** Paskutinė eilutė išklys kodą, kad apklausos mygtukas būtų sugeneruotas po vienos sekundės, siekiant užtikrinti, kad scenarijai turėtų pakankamai laiko, kurį reikia įkelti. Atsižvelgiant į pasirinktą apklausą gali reikėti įtraukti arba atnaujinti kitus metaduomenis, pvz., įmonės pavadinimą.

```html
function renderSurveyButton() {
    var se = new SurveyEmbed("SURVEY_KEY","https://customervoice.microsoft.com/","https://mfpembedcdnmsit.azureedge.net/mfpembedcontmsit/","true");

    var context = {
        "First Name":"",
        "Last Name": "",
        "locale": "en-us",
        "companyname": "Adventure Works"
    };
    se.renderButton(context);
}

setTimeout(renderSurveyButton, 4000);
```

Norėdami įterpti įterpimo į fragmentą inline scenarijų, atlikite šiuos veiksmus.

1. Svetainės generatoriuje sukurkite fragmentą, pagrįstą inline [scenarijaus moduliu](script-module.md).
1. Fragmente pasirinkite numatytąją eilučių **scenarijaus atminties** reikšmę.
1. Numatytojo **eilučių scenarijaus ypatybės** srityje, lauke Inline **scenarijus,** įveskite eilučių scenarijaus kodą, kaip parodyta toliau pateiktame pavyzdyje.

    ![Naujo fragmento eilučių scenarijaus lauke inline scenarijus.](media/customer-voice-integration-4.png)

1. Pasirinkite **Įrašyti**, tada – **Baigti redagavimą**.
1. Norėdami **publikuoti fragmentą**, pasirinkite Publikuoti.

Naujas fragmentas, kuriame yra įdėtasis į eilutės scenarijaus kodas, paruoštas pridėti prie atitinkamo puslapio šablono.

## <a name="add-fragments-to-a-template"></a>Fragmentų pridėjimas prie šablono

Baigę kurti fragmentus, kuriuose yra kliento Embedded kodas, turite juos pridėti prie puslapių šablonų, susietų su svetainės puslapiais, kuriuose norite juos naudoti. Šiame pavyzdyje kaip pavyzdys, į produkto informacijos puslapio (PDP) šabloną įtraukti trys pavyzdiniai fragmentai.

![Pavyzdžiui, fragmentai, įtraukti į PDP šabloną.](media/customer-voice-integration-5.png)

Po to, kai publikuojamas atnaujintas šablonas, klientų pagal šabloną vartotojų apklausa bus rodoma visuose puslapiuose, kuriuos valdo šablonas.

Informacijos apie šablonus ieškokite Darbas [su šablonais](work-with-templates.md).

## <a name="configure-content-security-policy"></a>Konfigūruoti turinio saugos strategiją

Pagal numatytuosius nustatymus turinio saugos strategija (CSP) neleidžia iškbenti kitas tarnybas, nebent atliekama papildoma konfigūracija. Todėl, kai publikuojate atnaujintus šablonus, tikėtina, kad apklausos nepavyks įkelti į atitinkamus svetainės puslapius. Norėdami peržiūrėti su CSP susijusias klaidas, atidarykite žiniatinklio naršyklės programuotojo įrankius (F12) ir eikite į apklausos puslapį. Su CSP susijusios klaidos bus rodomos konsolės išvestije.

Norėdami konfigūruoti CSP svetainės generatoriuje, kad būtų ištaisytos klaidos, atlikite šiuos veiksmus.

1. Eiti į **Svetainės parametrai \> Plėtiniai**.
1. Skirtuke **Turinio saugos** strategija pridėkite `https://customervoice.microsoft.com/` prie antrinio **src** direktyvos.
1. Pridėkite `https://customervoice.microsoft.com/` prie **rėmo src** direktyvos.
1. Įtraukti `https://mfpembedcdnmsit.azureedge.net` ir **azureedge.net** į **img-src** direktyvos.

Dėl platesnės informacijos, žr. [Turinio saugos politika](manage-csp.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Išorinio scenarijaus modulis](script-module.md)

[Metažymių modulis](metatags-module.md)

[Įeiti scenarijaus modulis](script-module.md)

[Turinio saugos strategija](manage-csp.md)

[Darbas su fragmentais](work-with-fragments.md)

[Darbas su šablonais](work-with-templates.md)
