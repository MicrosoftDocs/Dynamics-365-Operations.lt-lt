---
title: „Power Apps“ įdėjimas
description: Šioje temoje aprašoma, kaip įdėti „Power Apps“ klientą, siekiant padidinti produkto funkcijų skaičių.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 9585d5a399ebf45b0ad7640f3c4e48d8afc46cd8
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017733"
---
# <a name="embed-microsoft-power-apps"></a>„Microsoft Power Apps“ įdėjimas

[!include [banner](../includes/banner.md)]

„Finance and Operations“ palaiko integravimą su „Microsoft Power Apps“, kūrėjams ir įprastiems vartotojams skirta paslauga, kurią naudojant galima kurti pasirinktines verslo programas, skirtas mobiliesiems įrenginiams, planšetiniams kompiuteriams ir žiniatinkliui nerašant kodo. „Power Apps”, kurias sukūrėte jūs, jūsų organizacija arba platesnė bendruomenė, galima įdėti į „Finance and Operations“ programas ir padidinti produkto funkcijų skaičių. Pavyzdžiui, „Power Apps“ pagrindu galite sukurti programą, kad papildytumėte programą „Finance and Operations“ informacija, gauta iš kitos sistemos.

Norėdami daugiau sužinoti apie „Power Apps“ įdėjimą, peržiūrėkite trumpą vaizdo įrašą [Kaip įdėti „Power Apps“](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>Įdėtosios „Power Apps“ programos įtraukimas į puslapį

### <a name="overview"></a>Peržiūrėti

Prieš įdedant programą iš „Power Apps“ į klientą, pirmiausia reikia rasti arba sukurti programą su norimais vaizdiniais elementais ir (arba) funkcijomis. Čia nepateiksime išsamaus programų kūrimo proceso aprašo. Jei esate naujas „Power Apps“ naudotojas, gera vieta pradėti – tema [„Power Apps“ pristatymas](https://docs.microsoft.com/powerapps/getting-started).

Kai būsite pasirengę įdėti konkrečią programą, galite pasirinkti sau tinkamesnį vieną iš dviejų būdų, kaip pasiekti programą puslapyje. Pirmasis prieigos būdas yra mygtukas „Power Apps“, kuris įtrauktas į standartinę veiksmų sritį. Naudojant šį mechanizmą įtrauktos programos bus rodomos kaip meniu mygtuko „Power Apps“ meniu elementai. Pasirinkus bet kurį iš šių meniu elementų, atsidarys šoninė sritis, kurioje bus pateikta įdėtoji programa. Taip pat galite pasirinkti įdėti programą į puslapį tiesiogiai kaip naują skirtuką, „FastTab“, mentę arba naują skiltį darbo srityje.

Konfigūruodami savo įdėtąją programą, galite pasirinkti vieną lauką, kurį norite siųsti kaip kontekstą į programą. Tai programai suteikia galimybę reaguoti pagal duomenis, kuriuos tuo metu peržiūrite.

### <a name="details"></a>Išsami informacija

Toliau pateiktose instrukcijose parodyta, kaip įdėti programą iš „Power Apps“ į žiniatinklio klientą.

1. Atidarykite puslapį, kuriame norite įdėti programą. Tai bus puslapis su duomenimis, kuriuos reikia kaip įvestį perduoti programai.
2. Atidarykite sritį **Įtraukti programą iš „Power Apps“**, atlikę tolesnius veiksmus.

    - Spustelėkite **Parinktys** ir tada pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams**. Meniu **Įterpti** pasirinkite **„Power Apps“**. Galiausiai pasirinkite regioną, kuriame norite įtraukti programą. Jei norite įdėti programą į meniu mygtuką „Power Apps“, pasirinkite veiksmų sritį. Jei norite įdėti programą tiesiai į puslapį, pasirinkite atitinkamą skirtuką, „FastTab“, mentę arba skyrių (jei naudojate darbo sritį).
    - Jei programa bus pasiekiama naudojant meniu mygtuką „Power Apps“, taip pat galite spustelėti standartinės veiksmų srities meniu mygtuką **„Power Apps”** ir tada pasirinkti **Įtraukti programą**.

3. Konfigūruokite įdėtąją programą, atlikę tolesnius veiksmus.

    - Lauke **Pavadinimas** nurodomas mygtuke arba skirtuke, kuriame bus įdėtoji programa, rodomas tekstas. Daugeliu atveju patartina pakartoti programos pavadinimą šiame lauke.
    - **Programos ID** yra programos, kurią norite įdėti, GUID. Norėdami gauti šią reikšmę, raskite programą puslapyje [web.powerapps.com](https://web.powerapps.com) ir raskite lauką **Programos ID**, pateiktą dalyje **Informacija**.
    - Dalyje **Programos įvesties kontekstas** galite pasirinktinai pasirinkti lauką su duomenimis, kuriuos kaip įvestį norite perduoti programai. Informacijos apie tai, kaip programa gali pasiekti duomenis, išsiųstus iš „Finance and Operations“ programų, žr. šios temos skyriuje [Programų, kurios naudoja „Finance and Operations“ programų duomenis, kūrimas](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps).
    - Pasirinkite parinktį **Programos dydis**, atitinkančią įdedamos programos tipą. Jei kuriate mobiliesiems įrenginiams skirtas programas, pasirinkite parinktį **Plona**, o jei kuriate planšetiniams kompiuteriams skirtas programas, pasirinkite **Plati**. Taip užtikrinama, kad įdėtajai programai bus skirta pakankamai vietos.
    - „FastTab“ **Juridiniai subjektai** pateikiama galimybė rinktis, kuriems juridiniams subjektams suteikiama programa. Pagal numatytuosius parametrus programa suteikiama visiems juridiniams subjektams. Ši parinktis galima tik tada, kai funkcija [Įrašyti rodiniai](saved-views.md) yra išjungta. 

4. Įsitikinę, kad konfigūracija teisinga, spustelėkite **Įterpti**, kad įdėtumėte „Power App“ į puslapį. Būsite paraginti atnaujinti naršyklę, kad pamatytumėte įdėtąją programą.

## <a name="sharing-an-embedded-app"></a>Įdėtosios programos bendrinimas

Įdėję programą į puslapį ir įsitikinę, kad ji veikia tinkamai ir visas duomenų kontekstas perduodamas iš puslapio, galite šią programą bendrinti su kitais sistemos vartotojais. Tai galima atlikti toliau nurodytais dviem skirtingais būdais, naudojant produkto personalizavimo galimybes.

- Rekomenduojamas atvejis – kreiptis į sistemos administratorių, kuris asmeniniams poreikiams pritaikytą elementą gali perduoti visiems vartotojams arba vartotojų subrinkiniui.
- Taip pat savo puslapio asmeniniams poreikiams pritaikytus elementus galite eksportuoti, siųsti vienam ar keliems vartotojams, kad kiekvienas iš jų jūsų tuos keitimus importuotų. Eksportuoti ir importuoti personalizavimus galite pasirinkę personalizavimo įrankių juostos veiksmus.

Informacijos apie produkto pritaikymo galimybes ir kaip jas naudoti žr. temoje [Vartotojo patirties pritaikymas asmeniniams poreikiams](personalize-user-experience.md).

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Programos, kuri naudoja duomenis, siunčiamus iš „Finance and Operations“ programų, kūrimas

Kuriant programą iš „Power Apps“, kuri bus įdėta į „Finance and Operations“ programą, svarbu naudojant įvesties duomenis iš tos programos. „Power Apps“ kūrimo patirtyje iš „Finance and Operations“ programos perkeliamus įvesties duomenis galima pasiekti naudojant kintamąjį Param("EntityId") .

Pvz., programos funkcijoje „OnStart“ galite nustatyti „Finance and Operations“ programų įvesties duomenis į kintamąjį toliau nurodytu būdu.

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>Programos peržiūra

Norėdami įdėtąją programą peržiūrėti „Finance and Operations“ programų puslapyje, tiesiog atidarykite puslapį, kuriame yra įdėtoji programa. Atminkite, kad programas galima pasiekti naudojant mygtuką „Power Apps“ standartinėje veiksmų srityje arba jos gali būti tiesiogiai pateikiamos puslapyje kaip naujas skirtukas, „FastTab“, mentė arba naujas skyrius darbo srityje. Kai vartotojas pirmą kartą bando įkelti programą į puslapį, jis bus paragintas prisijungti, siekiant užtikrinti, kad vartotojas turi tinkamas programos naudojimo teises.

## <a name="editing-an-embedded-app"></a>Įdėtosios programos redagavimas

Įdėjus programą į puslapį, gali reikėti atlikti tam tikrus programos konfigūracijos keitimus. Pavyzdžiui, galbūt norėsite modifikuoti su įdėtąja programa susietą žymę arba galbūt buvo sukurta nauja programos versija ir jums reikia atnaujinti programos ID bei nurodyti naujausią programą.

Atlikite toliau nurodytus veiksmus norėdami redaguoti įdėtosios programos konfigūraciją.

1. Pasirinkite sritį **Redaguoti programą**.

    - Jei įdėtoji programa pasiekiama per meniu mygtuką „Power Apps“, dešiniuoju pelės mygtuku spustelėkite meniu mygtuką „Power Apps“ ir pasirinkite **Pritaikyti asmeniniams poreikiams**. Išplečiamajame meniu **Pasirinkti programą** pasirinkite, kurią programą norite konfigūruoti.
    - Jei įdėtoji programa rodoma tiesiogiai puslapyje, pasirinkite **Parinktys**, tada pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams**. Naudodami įrankį **Pasirinkti** spustelėkite įdėtąją programą.

2. Atlikite reikiamus programos konfigūracijos keitimus, tada spustelėkite **Įrašyti**.

## <a name="removing-an-app"></a>Programos pašalinimas

Įdėjus programą į puslapį, jei reikia, ją galima pašalinti dviem būdais.

- Pasirinkite sritį **Redaguoti programą**, vadovaudamiesi instrukcijomis iš ankstesnio šios temos skyriaus [Įdėtosios programos redagavimas](#editing-an-embedded-power-app). Įsitikinkite, kad srityje rodoma įdėtosios programos, kurią norite pašalinti, informacija, tada spustelėkite mygtuką **Naikinti**.
- Kadangi įdėtoji programa įrašoma kaip pritaikymo asmeniniams poreikiams duomenys, išvalius puslapio pritaikymo asmeniniams poreikiams elementus taip pat bus pašalintos visos to puslapio įdėtosios programos. Atminkite, kad puslapio pritaikymo asmeniniams poreikiams elementų šalinimas yra nuolatinis veiksmas ir jo atšaukti negalima. Norėdami šalinti puslapio pritaikymo asmeniniams poreikiams elementus, pasirinkite **Parinktys**, tada pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams** ir galiausiai spustelėkite mygtuką **Išvalyti**. Atnaujinus naršyklę bus pašalinti visi ankstesni šio puslapio pritaikymo asmeniniams poreikiams elementai. Daugiau informacijos apie tai, kaip optimizuoti puslapius naudojant pritaikymo asmeniniams poreikiams elementus, žr. puslapyje [Vartotojo patirties pritaikymas asmeniniams poreikiams](personalize-user-experience.md).

## <a name="appendix"></a>Priedas

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>Kūrėjo valdymas, kurioje vietoje galima įdėti programą

Pagal numatytuosius parametrus vartotojai gali įdėti programas bet kuriame puslapyje – į meniu mygtuką „Power Apps“ arba tiesiogiai į puslapį kaip skirtuką, „FastTab“, mentę ar naują skyrių darbo srityje. Tačiau, jei reikia, kūrėjai gali taip pat sukonfigūruoti šią funkciją, kad programas būtų galima įdėti tik tam tikruose puslapiuose, naudodami toliau pateiktus būdus.

- **isPowerAppPersonalizationEnabled** – jei šis būdas pateikia tam tikro puslapio reikšmę „false“, tada meniu mygtukas „Power Apps“ nebus rodomas, o vartotojai negalės įdėti programų į jokią šio puslapio vietą, įskaitant skirtukus.
- **isPowerAppTabPersonalizationEnabled** – jei šis būdas pateikia tam tikro puslapio reikšmę „false“, tada vartotojai negalės tiesiogiai įdėti programų į puslapį kaip skirtuką, „FastTab“ arba panoraminę skiltį. Vartotojai vis tiek galės įdėti programas per meniu mygtuką „Power Apps“, jei įdėjimo funkciją tame puslapyje galima naudoti.

Toliau pateiktame pavyzdyje parodoma nauja klasė ir du būdai, kaip sukonfigūruoti, kur galima įdėti programas.

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```
