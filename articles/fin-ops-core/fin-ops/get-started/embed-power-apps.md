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
ms.openlocfilehash: 8b5e64cb9ba916f9cbd628703394318b4044867b
ms.sourcegitcommit: dc953c316c396c45ddd596e25c2b358e39a95d84
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/02/2019
ms.locfileid: "2870246"
---
# <a name="embed-microsoft-power-apps"></a>„Microsoft Power Apps“ įdėjimas

[!include [banner](../includes/banner.md)]

14 platformos naujinys palaiko integravimą su „Microsoft Power Apps“, kūrėjams ir įprastiems vartotojams skirta paslauga, kurią naudojant galima kurti pasirinktines verslo programas, skirtas mobiliesiems įrenginiams, planšetiniams kompiuteriams ir žiniatinkliui nerašant kodo. „Power Apps” programas, kurias sukūrėte jūs, jūsų organizacija arba platesnė bendruomenė, galima įdėti „Finance and Operations“ programas ir padidinti produkto funkcijų skaičių. Pavyzdžiui, galite sukurti „Power App“, kad papildytumėte „Finance and Operations“ programas informacija, gauta iš kitos sistemos.

Norėdami daugiau sužinoti apie „Power Apps“ įdėjimą, peržiūrėkite trumpą vaizdo įrašą [Kaip įdėti „Power Apps“](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-power-app-to-a-page"></a>Įdėtosios „Power App“ įtraukimas į puslapį

### <a name="overview"></a>Apžvalga

Prieš įdedant „Power App“ į klientą, pirmiausia reikia rasti arba sukurti „Power App“ su norimais vaizdiniais elementais ir (arba) funkcijomis. Čia nepateiksime išsamaus „Power App“ kūrimo proceso. Jei esate naujas „Power Apps“ naudotojas, gera vieta pradėti – tema [„Power Apps“ pristatymas](https://docs.microsoft.com/powerapps/getting-started).

Kai būsite pasirengę įdėti konkrečią „Power App“ programą, galite pasirinkti sau tinkamesnį vieną iš dviejų būdų, kaip pasiekti „Power App“ puslapyje. Pirmasis prieigos būdas yra mygtukas „Power Apps“, kuris įtrauktas į standartinę veiksmų sritį. Naudojant šį mechanizmą įtraukos „Power Apps“ programos bus rodomos kaip meniu mygtuko „Power Apps“ meniu elementai. Pasirinkus bet kurį iš šių meniu elementų, atsidarys šoninė sritis, kurioje bus pateikta įdėtoji „Power App“. Taip pat galite pasirinkti rodyti „Power App“ puslapyje tiesiogiai kaip naują skirtuką, „FastTab“, mentę arba naują skiltį darbo srityje.

Konfigūruodami savo įdėtąją „Power App“, galite pasirinkti vieną lauką, kurį kaip įvestį norite siųsti „Power App“. Tai „Power App“ suteikia galimybę atsakyti į komandas pagal duomenis, kuriuos tuo metu peržiūrite.

### <a name="details"></a>Išsami informacija

Toliau pateiktose instrukcijose parodyta, kaip įdėti „Power App“ į žiniatinklio klientą.

1. Atidarykite puslapį, kuriame norite įdėti „Power App“. Tai bus tas pats puslapis, talpinantis duomenis, kuriuos reikia kaip įvestį perduoti „Power App“.
2. Atidarykite sritį **Įterpti „Power App“**.

    - Spustelėkite **Parinktys** ir tada pasirinkite **Pritaikyti šią formą asmeniniams poreikiams**. Meniu **Įterpti** pasirinkite **Power App**. Galiausiai pasirinkite regioną, kuriame norite įtraukti „Power App“. Jei norite įdėti „Power App“ į meniu mygtuką „Power Apps“, pasirinkti veiksmų sritį. Jei norite įdėti „Power App“ tiesiai į puslapį, pasirinkite atitinkamą skirtuką, „FastTab“, mentę arba skiltį (jei naudojate darbo sritį).
    - Jei „Power App“ bus pasiekiama naudojant meniu mygtuką „Power Apps“, taip pat galite spustelėti standartinės veiksmų srities meniu mygtuką **„Power Apps”** ir tada pasirinkti **Įterpti į „Power App“**.

3. Įdėtosios „Power App“ konfigūravimas

    - Laukas **Pavadinimas** nurodo mygtuke arba skirtuke, kuriame bus įdėtoji „Power App“, rodomą tekstą. Dažnai galite pakartoti „Power App“ šiame lauke pateikiamą pavadinimą.
    - **Programos ID** yra GUID, skirtas „Power App“, kurią norite įterpti. Norėdami gauti šią reikšmę, raskite „Power App“ puslapyje [web.powerapps.com](https://web.powerapps.com) ir raskite lauką **Programos ID**, pateiktą dalyje **Informacija**.
    - Dalyje **„Power App“ įvesties duomenys** galite pasirinktinai pasirinkti lauką, talpinantį duomenis, kuriuos kaip įvestį norite perduoti „Power App“. Informacijos apie tai, kaip „Power App“ gali pasiekti duomenis, išsiųstus iš „Finance and Operations“ programų, žr. šioje temoje pavadinimu [„Power App“, kuri naudoja „Finance and Operations“ programų duomenis, kūrimas](#building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps).
    - Pasirinkite **programos dydį**, atitinkantį įdedamos „Power App“ tipą. Jei kuriate mobiliesiems įrenginiams skirtas „Power Apps“, pasirinkite parinktį **Plona**, o jei kuriate planšetiniams kompiuteriams skirtas „Power Apps“, pasirinkite **Plati**. Taip užtikrinama, kad įdėtajai „Power App“ bus skirta pakankamai vietos.
    - „FastTab“ **Juridiniai subjektai** pateikiama galimybė rinktis, kuriems juridiniams subjektams „Power App“ bus priskirta. Pagal numatytuosius parametrus „Power App“ priskiriama visiems juridiniams asmenims.

4. Įsitikinę, kad konfigūracija teisinga, spustelėkite **Įterpti**, kad įdėtumėte „Power App“ į puslapį. Būsite paraginti atnaujinti naršyklę, kad pamatytumėte įdėtąją „Power App“.

## <a name="sharing-an-embedded-power-app"></a>Įdėtosios „Power App“ bendrinimas

Įdėję „Power App“ į puslapį ir įsitikinę, kad ji veikia tinkamai ir visas duomenų kontekstas perduodamas iš puslapio, galite šią įdėtąją „Power App“ bendrinti su kitais sistemos vartotojais. Tai galima atlikti toliau nurodytais dviem skirtingais būdais, naudojant produkto personalizavimo galimybes.

- Rekomenduojamas atvejis – kreiptis į sistemos administratorių, kuris asmeniniams poreikiams pritaikytą elementą gali perduoti visiems vartotojams arba vartotojų subrinkiniui.
- Taip pat savo puslapio asmeniniams poreikiams pritaikytus elementus galite eksportuoti, siųsti vienam ar keliems vartotojams, kad kiekvienas iš jų jūsų tuos keitimus importuotų. Eksportuoti ir importuoti personalizavimus galite pasirinkę personalizavimo įrankių juostos parinktį Valdyti.

Informacijos apie produkto pritaikymo galimybes ir kaip jas naudoti žr. temoje [Vartotojo patirties pritaikymas asmeniniams poreikiams](personalize-user-experience.md).

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>„Power App“, kuri naudoja „Finance and Operations“ programų duomenis, kūrimas

Kuriant „Power App“, kuri bus įdėta į „Finance and Operations“ programas, svarbu panaudoti „Finance and Operations“ programų įvesties duomenis. „Power App“ viduje tuos įvesties duomenis galima pasiekti naudojant kintamąjį Param (EntityId).

Pvz., „Power App“ funkcijoje „OnStart“ galite nustatyti „Finance and Operations“ programų įvesties duomenis į kintamąjį toliau nurodytu būdu.

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>Įdėtosios „Power App“ peržiūra

Norėdami įdėtąją „Power App“ peržiūrėti „Finance and Operations“ programų puslapyje, tiesiog atidarykite puslapį, kuriame yra įdėtoji „Power App“. Atminkite, kad „Power Apps“ galima pasiekti naudojant mygtuką „Power Apps“ standartinėje veiksmų srityje arba jos gali būti tiesiogiai pateikiamos puslapyje kaip naujas skirtukas, „FastTab“, mentė arba nauja skiltis darbo srityje. Kai vartotojas pirmą kartą bando įkelti „Power App“ į puslapį, jis bus paragintas prisijungti prie „Power Apps“, siekiant užtikrinti, kad vartotojas turi tinkamas „Power App“ naudojimo teises.

## <a name="editing-an-embedded-power-app"></a>Įdėtosios „Power App“ redagavimas

Įdėjus „Power App“ į puslapį, gali reikėti atlikti tam tikrus „Power App“ konfigūracijos keitimus. Pavyzdžiui, galbūt norėsite modifikuoti su įdėtąja „Power App“ susietą žymą arba galbūt buvo sukurta nauja „Power App“ versija ir jums reikia atnaujinti programos ID bei nurodyti naujausią „Power App“.

Atlikite toliau nurodytus veiksmus norėdami redaguoti įdėtosios „Power App“ konfigūraciją.

1. Pasirinkite sritį **„Power App“ redagavimas**.

    - Jei įdėtoji „Power App“ pasiekiama per meniu mygtuką „Power Apps“, dešiniuoju pelės mygtuku spustelėkite meniu mygtuką „Power Apps“ ir pasirinkite **Pritaikyti asmeniniams poreikiams**. Išplečiamajame meniu **Pasirinkti „Power App“** pasirinkite, kurią „Power App“ norite konfigūruoti.
    - Jei įdėtoji „Power App“ rodoma tiesiogiai puslapyje, pasirinkite **Parinktys**, tada pasirinkite **Pritaikyti šią formą asmeniniams poreikiams**. Naudodami įrankį **Pasirinkti** spustelėkite įdėtąją „Power App“.

2. Atlikite reikiamus „Power Apps“ konfigūracijos keitimus, tada spustelėkite **Įrašyti**.

## <a name="removing-an-embedded-power-app"></a>Įdėtosios „Power App“ šalinimas

Įdėjus „Power App“ į puslapį, jei reikia, ją galima pašalinti dviem būdais.

- Pasirinkite sritį **„Power App“ redagavimas** naudodami instrukcijas iš ankstesnio šios temos skyriaus [Įdėtosios „Power App“ redagavimas](#editing-an-embedded-power-app). Įsitikinkite, kad srityje rodoma įdėtosios „Power App“, kurią norite pašalinti, informacija, tada spustelėkite mygtuką **Naikinti**.
- Kadangi įdėtoji „Power App“ įrašoma kaip pritaikymo asmeniniams poreikiams duomenys, išvalius puslapio pritaikymo asmeniniams poreikiams elementus taip pat bus pašalintos visos to puslapio įdėtosios „Power Apps“. Atminkite, kad puslapio pritaikymo asmeniniams poreikiams elementų šalinimas yra nuolatinis veiksmas ir jo atšaukti negalima. Norėdami šalinti puslapio pritaikymo asmeniniams poreikiams elementus, pasirinkite **Parinktys** ir tada spustelėkite **Pritaikyti šią formą**. Meniu **Valdyti** pasirinkite formą mygtuką **Išvalyti**. Atnaujinus naršyklę bus pašalinti visi ankstesni šio puslapio pritaikymo asmeniniams poreikiams elementai. Daugiau informacijos apie tai, kaip optimizuoti puslapius naudojant pritaikymo asmeniniams poreikiams elementus, žr. puslapyje [Vartotojo patirties pritaikymas asmeniniams poreikiams](personalize-user-experience.md).

## <a name="appendix"></a>Priedas

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>Kūrėjo valdymas, kurioje vietoje „Power App“ galima įterpti

Pagal numatytuosius parametrus vartotojai gali įdėti „Power Apps“ bet kuriame puslapyje – į meniu mygtuką „Power Apps“ arba tiesiogiai į puslapį kaip skirtuką, „FastTab“, mentę ar naują skiltį darbo srityje. Tačiau, jei reikia, kūrėjai gali taip pat sukonfigūruoti šią funkciją, kad „Power Apps“ būtų galima įdėti tik tam tikruose puslapiuose, naudodami toliau pateiktus būdus.

- **isPowerAppPersonalizationEnabled** – jei šis būdas pateikia konkretaus puslapio reikšmę „false“, tada meniu mygtukas „Power Apps“ nebus rodomas, o vartotojai negalės „Power Apps“ įdėti į jokią šio puslapio vietą, įskaitant skirtukus.
- **isPowerAppTabPersonalizationEnabled** – jei šis būdas pateikia tam tikro puslapio reikšmę „false“, tada vartotojai negalės tiesiogiai įdėti „Power Apps“ į puslapį kaip skirtuką, „FastTab“ arba panoraminę skiltį. Vartotojai vis tiek galės įdėti „Power Apps“ per meniu mygtuką „Power Apps“, jei įdėjimo funkciją tame puslapyje galima naudoti.

Toliau pateiktame pavyzdyje parodoma nauja klasė ir du būdai, kaip sukonfigūruoti, kur galima įdėti „Power Apps“.

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
