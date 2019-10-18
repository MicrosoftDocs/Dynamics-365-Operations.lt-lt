---
title: „PowerApps“ programų įdėjimas
description: Šioje temoje aprašoma, kaip įdėti „PowerApps“ klientą, siekiant padidinti produkto funkcijų skaičių.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
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
ms.openlocfilehash: 37faf2a7a880c384f6f01d06ef5c9f28055d5006
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191183"
---
# <a name="embed-powerapps-apps"></a>„PowerApps“ programų įdėjimas

[!include [banner](../includes/banner.md)]

14 platformos naujinys palaiko integravimą su „Microsoft PowerApps“, kūrėjams ir įprastiems vartotojams skirta paslauga, kurią naudojant galima kurti pasirinktines verslo programas, skirtas mobiliesiems įrenginiams, planšetiniams kompiuteriams ir žiniatinkliui nerašant kodo. „PowerApps” programas, kurias sukūrėte jūs, jūsų organizacija arba platesnė bendruomenė, galima įdėti „Finance and Operations“ programas ir padidinti produkto funkcijų skaičių. Pavyzdžiui, galite kurti „PowerApp“, kad papildytumėte „Finance and Operations“ programas informacija, gauta iš kitos sistemos.

Norėdami daugiau sužinoti apie „PowerApps“ įdėjimą, peržiūrėkite trumpą vaizdo įrašą [Kaip įdėti „PowerApps“](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Įdėtosios „PowerApp“ įtraukimas į puslapį

### <a name="overview"></a>Apžvalga

Prieš įdedant „PowerApp“ į klientą, pirmiausia reikia rasti arba sukurti „PowerApp“ norimais vaizdiniais elementais ir (arba) funkcijomis. Čia nepateiksime išsamaus „PowerApp“ kūrimo proceso. Jei esate naujas „PowerApps“ naudotojas, gera vieta pradėti – tema [„PowerApps“ pristatymas](https://docs.microsoft.com/powerapps/getting-started).

Kai būsite pasirengę įdėti konkrečią „PowerApp“ programą, galite pasirinkti sau tinkamesnį vieną iš dviejų būdų, kaip pasiekti „PowerApp“ puslapyje. Pirmasis prieigos būdas yra mygtukas „PowerApps“, kuris įtrauktas į standartinę veiksmų sritį. Naudojant šį mechanizmą įtraukos „PowerApps“ programos bus rodomos kaip meniu mygtuko „PowerApps“ meniu elementai. Pasirinkus bet kurį iš šių meniu elementų, atsidarys šoninė sritis, kurioje bus pateikta įdėtoji „PowerApp“. Taip pat galite pasirinkti rodyti „PowerApp“ puslapyje tiesiogiai kaip naują skirtuką, „FastTab“, mentę arba naują skiltį darbo srityje.

Konfigūruodami savo įdėtąją „PowerApp“, galite pasirinkti vieną lauką, kurį kaip įvestį norite siųsti „PowerApp“. Tai „PowerApp“ suteikia galimybę atsakyti į komandas pagal duomenis, kuriuos tuo metu peržiūrite.

### <a name="details"></a>Išsami informacija

Toliau pateiktose instrukcijose parodyta, kaip įdėti „PowerApp“ į žiniatinklio klientą.

1. Atidarykite puslapį, kuriame norite įdėti „PowerApp“. Tai bus tas pats puslapis, talpinantis duomenis, kuriuos reikia kaip įvestį perduoti „PowerApp“.
2. Atidarykite sritį **Įterpti „PowerApp“**.

    - Spustelėkite **Parinktys** ir tada pasirinkite **Pritaikyti šią formą asmeniniams poreikiams**. Meniu **Įterpti** pasirinkite **PowerApp**. Galiausiai pasirinkite regioną, kuriame norite įtraukti „PowerApp“. Jei norite įdėti „PowerApp“ į meniu mygtuką „PowerApps“, pasirinkti veiksmų sritį. Jei norite įdėti „PowerApp“ tiesiai į puslapį, pasirinkite atitinkamą skirtuką, „FastTab“, mentę arba skiltį (jei naudojate darbo sritį).
    - Jei „PowerApp“ bus pasiekiama naudojant meniu mygtuką „PowerApps“, taip pat galite spustelėti standartinės veiksmų srities meniu mygtuką **„PowerApps”** ir tada pasirinkti **Įterpti į „PowerApp“**.

3. Įdėtosios „PowerApp“ konfigūravimas

    - Laukas **Pavadinimas** nurodo mygtuke arba skirtuke, kuriame bus įdėtoji „PowerApp“, rodomą tekstą. Dažnai galite pakartoti „PowerApp“ šiame lauke pateikiamą pavadinimą.
    - **Programos ID** yra GUID, skirtas „PowerApp“, kurią norite įterpti. Norėdami gauti šią reikšmę, raskite „PowerApp“ puslapyje [web.powerapps.com](https://web.powerapps.com) ir raskite lauką **Programos ID**, pateiktą dalyje **Informacija**.
    - Dalyje **„PowerApp“ įvesties duomenys** galite pasirinktinai pasirinkti lauką, talpinantį duomenis, kuriuos kaip įvestį norite perduoti „PowerApp“. Informacijos apie tai, kaip „PowerApp“ gali pasiekti duomenis, išsiųstus iš „Finance and Operations“ programų, žr. šioje temoje pavadinimu [„PowerApp“, kuri naudoja „Finance and Operations“ programų duomenis, kūrimas](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps).
    - Pasirinkite **programos dydį**, atitinkantį įdedamos „PowerApp“ tipą. Jei kuriate mobiliesiems įrenginiams skirtas „PowerApps“, pasirinkite parinktį **Plona**, o jei kuriate planšetiniams kompiuteriams skirtas „PowerApps“, pasirinkite **Plati**. Taip užtikrinama, kad įdėtajai „PowerApp“ bus skirta pakankamai vietos.
    - „FastTab“ **Juridiniai subjektai** pateikiama galimybė rinktis, kurie juridiniams subjektams „PowerApp“ bus priskirta. Pagal numatytuosius parametrus „PowerApp“ priskiriama visiems juridiniams asmenims.

4. Įsitikinę, kad konfigūracija teisinga, spustelėkite **Įterpti**, kad įdėtumėte „PowerApp“ į puslapį. Būsite paraginti atnaujinti naršyklę, kad pamatytumėte įdėtąją „PowerApp“.

## <a name="sharing-an-embedded-powerapp"></a>Įdėtosios „PowerApp“ bendrinimas

Įdėję „PowerApp“ į puslapį ir įsitikinę, kad ji veikia tinkamai ir visas duomenų kontekstas perduodamas iš puslapio, galite šią įdėtąją „PowerApp“ bendrinti su kitais sistemos vartotojais. Tai galima atlikti toliau nurodytais dviem skirtingais būdais, naudojant produkto personalizavimo galimybes.

- Rekomenduojamas atvejis – kreiptis į sistemos administratorių, kuris asmeniniams poreikiams pritaikytą elementą gali perduoti visiems vartotojams arba vartotojų subrinkiniui.
- Taip pat savo puslapio asmeniniams poreikiams pritaikytus elementus galite eksportuoti, siųsti vienam ar keliems vartotojams, kad kiekvienas iš jų jūsų tuos keitimus importuotų. Eksportuoti ir importuoti personalizavimus galite pasirinkę personalizavimo įrankių juostos parinktį Valdyti.

Informacijos apie produkto pritaikymo galimybes ir kaip jas naudoti žr. temoje [Vartotojo patirties pritaikymas asmeniniams poreikiams](personalize-user-experience.md).

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps"></a>„PowerApp“, kuri naudoja „Finance and Operations“ programų duomenis, kūrimas

Kuriant „PowerApp“, kuri bus įdėta į „Finance and Operations“ programas, svarbu panaudoti „Finance and Operations“ programų įvesties duomenis. „PowerApp“ viduje tuos įvesties duomenis galima pasiekti naudojant kintamąjį Param (EntityId).

Pvz., „PowerApp“ funkcijoje „OnStart“ galite nustatyti „Finance and Operations“ programų įvesties duomenis į kintamąjį toliau nurodytu būdu.

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-powerapp"></a>Įdėtosios „PowerApp“ peržiūra

Norėdami įdėtąją „PowerApp“ peržiūrėti „Finance and Operations“ programų puslapyje, tiesiog atidarykite puslapį, kuriame yra įdėtoji „PowerApp“. Atminkite, kad „PowerApps“ galima pasiekti naudojant mygtuką „PowerApps“ standartinėje veiksmų srityje arba jos gali būti tiesiogiai pateikiamos puslapyje kaip naujas skirtukas, „FastTab“, mentė arba nauja skiltis darbo srityje. Kai vartotojas pirmą kartą bando įkelti „PowerApp“ į puslapį, jis bus paragintas prisijungti prie „PowerApps“, siekiant užtikrinti, kad vartotojas turi tinkamas „PowerApp“ naudojimo teises.

## <a name="editing-an-embedded-powerapp"></a>Įdėtosios „PowerApp“ redagavimas

Įdėjus „PowerApp“ į puslapį, gali reikėti atlikti tam tikrus „PowerApp“ konfigūracijos keitimus. Pavyzdžiui, galbūt norėsite modifikuoti su įdėtąja „PowerApp“ susietą žymę arba galbūt buvo sukurta nauja „PowerApp“ versija ir jums reikia atnaujinti programos ID bei nurodyti naujausią „PowerApp“.

Atlikite toliau nurodytus veiksmus norėdami redaguoti įdėtosios PowerApp konfigūraciją.

1. Pasirinkite sritį **„PowerApp“ redagavimas**.

    - Jei įdėtoji „PowerApp“ pasiekiama per meniu mygtuką „PowerApps“, dešiniuoju pelės mygtuku spustelėkite meniu mygtuką „PowerApps“ ir pasirinkite **Pritaikyti asmeniniams poreikiams**. Pasirinkite, kurią „PowerApp“ norite konfigūruoti, išplečiamajame meniu **Pasirinkti „PowerApp“**.
    - Jei įdėtoji „PowerApp“ rodoma tiesiogiai puslapyje, pasirinkite **Parinktys**, tada pasirinkite **Pritaikyti šią formą asmeniniams poreikiams**. Naudodami įrankį **Pasirinkti** spustelėkite įdėtąją „PowerApp“.

2. Atlikite reikiamus „PowerApps“ konfigūracijos keitimus, tada spustelėkite **Įrašyti**.

## <a name="removing-an-embedded-powerapp"></a>Įdėtosios „PowerApp“ šalinimas

Įdėjus „PowerApp“ į puslapį, jei reikia, ją galima pašalinti dviem būdais.

- Pasirinkite sritį **„PowerApp“ redagavimas** naudodami instrukcijas iš ankstesnio šios temos skyriaus [Įdėtosios „PowerApp“ redagavimas](#editing-an-embedded-powerapp). Įsitikinkite, kad srityje rodoma įdėtosios „PowerApp“, kurią norite pašalinti, informacija, tada spustelėkite mygtuką **Naikinti**.
- Kadangi įdėtoji „PowerApp“ įrašoma kaip pritaikymo asmeniniams poreikiams duomenys, išvalius puslapio pritaikymo asmeniniams poreikiams elementus taip pat bus pašalintos visos to puslapio įdėtosios „PowerApps“. Atminkite, kad puslapio pritaikymo asmeniniams poreikiams elementų šalinimas yra nuolatinis veiksmas ir jo atšaukti negalima. Norėdami šalinti puslapio pritaikymo asmeniniams poreikiams elementus, pasirinkite **Parinktys** ir tada spustelėkite **Pritaikyti šią formą**. Meniu **Valdyti** pasirinkite formą mygtuką **Išvalyti**. Atnaujinus naršyklę bus pašalinti visi ankstesni šio puslapio pritaikymo asmeniniams poreikiams elementai. Daugiau informacijos apie tai, kaip optimizuoti puslapius naudojant pritaikymo asmeniniams poreikiams elementus, žr. puslapyje [Vartotojo patirties pritaikymas asmeniniams poreikiams](personalize-user-experience.md).

## <a name="appendix"></a>Priedas

### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Kūrėjo valdymas, kurioje vietoje „PowerApp“ galima įterpti

Pagal numatytuosius parametrus vartotojai gali įdėti „PowerApps“ bet kuriame puslapyje – į meniu mygtuką „PowerApps“ arba tiesiogiai į puslapį kaip skirtuką, „FastTab“, mentę ar naują skiltį darbo srityje. Tačiau, jei reikia, kūrėjai gali taip pat sukonfigūruoti šią funkciją, kad „PowerApps“ būtų galima įdėti tik tam tikruose puslapiuose, naudodami toliau pateiktus būdus.

- **isPowerAppPersonalizationEnabled** – jei šis būdas pateikia konkretaus puslapio reikšmę „false“, tada meniu mygtukas „PowerApps“ nebus rodomas, o vartotojai negalės „PowerApps“ įdėti į jokią šio puslapio vietą, įskaitant skirtukus.
- **isPowerAppTabPersonalizationEnabled** – jei šis būdas pateikia tam tikro puslapio reikšmę „false“, tada vartotojai negalės tiesiogiai įdėti „PowerApps“ į puslapį kaip skirtuką, „FastTab“ arba panoraminę skiltį. Vartotojai vis tiek galės įdėti „PowerApps“ per meniu mygtuką „PowerApps“, jei įdėjimo funkciją tame puslapyje galima naudoti.

Toliau pateiktame pavyzdyje parodoma nauja klasė ir du būdai, kaip sukonfigūruoti, kur galima įdėti „PowerApps“.

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
