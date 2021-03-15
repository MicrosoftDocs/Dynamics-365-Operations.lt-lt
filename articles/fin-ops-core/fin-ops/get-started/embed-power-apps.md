---
title: Drobės programų įdėjimas iš „Power Apps”
description: Šioje temoje aiškinama, kaip įdėti drobės programas iš „Microsoft Power Apps“ į klientą, siekiant padidinti produkto funkcijų skaičių.
author: jasongre
manager: AnnBe
ms.date: 11/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: fbdd4dd1bb0b850319b12e55b0e68d6fdc516ad6
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798382"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Drobės programų įdėjimas iš „Power Apps”

[!include [banner](../includes/banner.md)]

„Microsoft Power Apps“ yra paslauga, leidžianti kūrėjams ir įprastiems vartotojams kurti pasirinktines verslo programas, skirtas mobiliesiems įrenginiams, planšetiniams kompiuteriams ir žiniatinkliui, nerašant kodo. „Finance and Operations” programos palaiko integravimą su „Power Apps”. Drobės programas, kurias sukūrėte jūs, jūsų organizacija arba platesnė bendruomenė, galima įdėti į „Finance and Operations“ programas ir padidinti produkto funkcijų skaičių. Pavyzdžiui, „Power Apps“ pagrindu galite sukurti drobės programą, kad papildytumėte „Finance and Operations“ programą informacija, gauta iš kitos sistemos.

Norėdami daugiau sužinoti apie „Power Apps“ įdėjimą, peržiūrėkite trumpą vaizdo įrašą [Kaip įdėti „Power Apps“](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Įdėtosios „Power Apps“ drobės programos įtraukimas į puslapį

### <a name="overview"></a>Peržiūra

Prieš įdedant drobės programą iš „Power Apps“ į klientą, reikia rasti arba sukurti programą su norimais vaizdiniais elementais arba funkcijomis. Šioje temoje nėra išsamaus programų kūrimo proceso aprašo. Jei naudojate „Power Apps” pirmą kartą, žr. [„Power Apps” dokumentaciją](https://docs.microsoft.com/powerapps/).

Yra du būdai, kaip pasiekti konkrečią drobės programą puslapyje, kai esate pasiruošę įdėti programą. Galite pasirinkti, kuris būdas geriau atitinka jūsų scenarijų. Pirmasis būdas naudoja mygtuką **„Power Apps“**, kuris įtrauktas į standartinę veiksmų sritį. Programos, kurias įtraukiate naudodami šį būdą , rodomos kaip meniu mygtuko **„Power Apps”** elementai. Pasirinkus bet kurį iš šių elementų, pasirodys šoninė sritis, kurioje bus pateikta įdėtoji programa. Taip pat galite įdėti programą į puslapį tiesiogiai kaip naują skirtuką, „FastTab“, mentę arba naują skiltį darbo srityje.

Konfigūruodami savo įdėtąją drobės programą, galite pasirinkti vieną lauką, kurį norite siųsti kaip kontekstą į programą. Šis veiksmas programai suteikia galimybę reaguoti pagal duomenis, kuriuos tuo metu peržiūrite.

> [!NOTE]
> Šiuo metu negalima naudoti šio mechanizmo modeliuotoms programos įdėti.  

### <a name="details"></a>Išsamiai

Toliau pateiktoje procedūroje parodyta, kaip įdėti drobės programą iš „Power Apps“ į žiniatinklio klientą.

1. Atidarykite puslapį, kuriame norite įdėti drobės programą. Tai bus puslapis su duomenimis, kuriuos reikia kaip įvestį perduoti programai.
2. Atidarykite sritį **Įtraukti programą iš „Power Apps“**, atlikę tolesnius veiksmus.

    - Spustelėkite **Parinktys** ir tada pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams**. Meniu **Įterpti** pasirinkite **„Power Apps“**. Galiausiai pasirinkite regioną, kuriame norite įtraukti programą. Jei norite įdėti programą į meniu mygtuką „Power Apps“, pasirinkite veiksmų sritį. Jei norite įdėti programą tiesiai į puslapį, pasirinkite atitinkamą skirtuką, „FastTab“, mentę arba skyrių (jei naudojate darbo sritį).
    - Jei programa bus pasiekiama naudojant meniu mygtuką „Power Apps“, taip pat galite spustelėti standartinės veiksmų srities meniu mygtuką **„Power Apps”** ir tada pasirinkti **Įtraukti programą**.

3. Konfigūruokite įdėtąją programą, atlikę tolesnius veiksmus.

    - Lauke **Pavadinimas** nurodomas mygtuke arba skirtuke, kuriame bus įdėtoji programa, rodomas tekstas. Daugeliu atveju patartina pakartoti programos pavadinimą šiame lauke.
    - Laukas **Programos ID** nurodo globaliai unikalų identifikatorių (GUID), skirtą drobės programai, kurią norite įdėti. Norėdami gauti šią reikšmę, raskite programą puslapyje [make.powerapps.com](https://make.powerapps.com) ir raskite lauką **Programos ID**, pateiktą dalyje **Informacija**.
    - Dalyje **Programos įvesties kontekstas** galite pasirinktinai pasirinkti lauką su duomenimis, kuriuos kaip įvestį norite perduoti programai. Informacijos apie tai, kaip programa gali pasiekti duomenis, išsiųstus iš „Finance and Operations“ programų, žr. šios temos skyriuje [Programos, naudojančios „Finance and Operations“ programų siųstus duomenis, kūrimas](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps).
    - Pasirinkite parinktį **Programos dydis**, atitinkančią įdedamos programos tipą. Jei kuriate mobiliesiems įrenginiams skirtas programas, pasirinkite parinktį **Plona**, o jei kuriate planšetiniams kompiuteriams skirtas programas, pasirinkite **Plati**. Taip užtikrinama, kad įdėtajai programai bus skirta pakankamai vietos.
    - „FastTab“ **Juridiniai subjektai** pateikiama galimybė rinktis, kuriems juridiniams subjektams suteikiama programa. Pagal numatytuosius parametrus programa suteikiama visiems juridiniams subjektams. Ši parinktis galima tik tada, kai funkcija [Įrašyti rodiniai](saved-views.md) yra išjungta. 

4. Įsitikinę, kad konfigūracija teisinga, spustelėkite **Įterpti**, kad įdėtumėte „Power App“ į puslapį. Būsite paraginti atnaujinti naršyklę, kad pamatytumėte įdėtąją programą.

## <a name="sharing-an-embedded-app"></a>Įdėtosios programos bendrinimas

Įdėję drobės programą į puslapį ir įsitikinę, kad ji veikia tinkamai su bet kokiu duomenų kontekstu, perduotu iš to puslapio, galite programą bendrinti su kitais sistemos vartotojais. Norėdami bendrinti įdėtąją drobės programą, atlikite toliau pateiktus veiksmus.

1. [Bendrinkite drobės programą](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) su tinkamais vartotojais, kad jie galėtų pasiekti programą, esančią „Power Apps”. 

2. Įsitikinkite, kad nustatytas atitinkamas tikslinių vartotojų personalizavimas, kad įdėtoji programa būtų rodoma šiems vartotojams peržiūrint puslapį. Galite naudoti bet kurį iš toliau nurodytų būdų.

    - Rekomenduojama naudoti funkciją [Įrašyti rodiniai](saved-views.md), kad būtų sukurtas ir publikuotas rodinys, įtraukiantis įdėtąją programą. Šis būdas užtikrina, kad visi vartotojai, turintys saugos vaidmenis, kuriems skirtas publikuotas rodinys, matys programą „Finance and Operations” programose. 
    - Jei nesate įjungę funkcijos Įrašyti rodiniai, sistemos administratorius gali skirti personalizavimą, įtraukiantį įdėtąją programą visiems vartotojams arba vartotojų pogrupiui. Taip pat galite eksportuoti jūsų puslapio personalizavimus ir siųsti juos vienam ar keliems vartotojams. Tada kiekvienas iš šių vartotojų gali importuoti personalizavimus. Eksportuoti ir importuoti personalizavimus galite pasirinkę personalizavimo įrankių juostos veiksmus. 
    
> [!NOTE]
> Jei drobės programa bendrinama su išoriniais vartotojais, šie vartotojai negali naudoti įdėtosios programos „Finance and Operations” programose. Tačiau jie gali pasiekti programą tiesiogiai programoje „Power Apps”. Išoriniai vartotojai įtraukia svečių ir vartotojų, nepriklausančių „Microsoft 365 Azure Directory”, kur įdiegta „Finance and Operations” programa.

Informacijos apie produkto pritaikymo galimybes ir kaip jas naudoti žr. temoje [Vartotojo patirties pritaikymas asmeniniams poreikiams](personalize-user-experience.md).

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Drobės programos, naudojančios iš „Finance and Operations” programų siunčiamus duomenis, kūrimas

Kai kuriate drobės programą, kuri bus įdėta į „Finance and Operations” programą, svarbi naudoti įvesties duomenis iš tos „Finance and Operations” programos. „Power Apps“ kūrimo patirtyje iš „Finance and Operations“ programos perkeliamus įvesties duomenis galima pasiekti naudojant kintamąjį **Param("EntityId")**.

Pvz., programos funkcijoje „OnStart“ galite nustatyti „Finance and Operations“ programų įvesties duomenis į kintamąjį toliau nurodytu būdu.

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a>Drobė programos peržiūra

Norėdami įdėtąją drobės programą peržiūrėti „Finance and Operations“ programų puslapyje, tiesiog atidarykite puslapį, kuriame yra įdėtoji programa. Atminkite, kad programas galima pasiekti naudojant mygtuką **„Power Apps”**, esantį standartinėje veiksmų srityje. Taip pat jos gali atsirasti puslapyje tiesiogiai kaip naujas skirtukas, „FastTab“, mentė arba nauja skiltis darbo srityje. Vartotojams pirmą kartą bandant įkelti programą į puslapį, jie bus paraginti prisijungti. Šis veiksmas užtikrina, kad vartotojai turėtų atitinkamas teises programėlei naudoti.

## <a name="editing-an-embedded-app"></a>Įdėtosios programos redagavimas

Įdėjus programą į puslapį, gali reikėti atlikti tam tikrus programos konfigūracijos keitimus. Pavyzdžiui, galbūt norėsite modifikuoti su įdėtąja programa susietą žymę arba galbūt buvo sukurta nauja programos versija ir jums reikia atnaujinti programos ID bei nurodyti naujausią programą.

Atlikite toliau nurodytus veiksmus norėdami redaguoti įdėtosios programos konfigūraciją.

1. Pasirinkite sritį **Redaguoti programą**.

    - Jei įdėtoji programa pasiekiama per meniu mygtuką „Power Apps“, dešiniuoju pelės mygtuku spustelėkite meniu mygtuką „Power Apps“ ir pasirinkite **Pritaikyti asmeniniams poreikiams**. Išplečiamajame meniu **Pasirinkti programą** pasirinkite, kurią programą norite konfigūruoti.
    - Jei įdėtoji programa rodoma tiesiogiai puslapyje, pasirinkite **Parinktys**, tada pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams**. Naudodami įrankį **Pasirinkti** spustelėkite įdėtąją programą.

2. Atlikite reikiamus programos konfigūracijos keitimus, tada spustelėkite **Įrašyti**.

## <a name="removing-an-app"></a>Programos pašalinimas

Įdėjus programą į puslapį, jei reikia, ją galima pašalinti dviem būdais.

- Pasirinkite sritį **Redaguoti programą**, vadovaudamiesi instrukcijomis iš ankstesnio šios temos skyriaus [Įdėtosios programos redagavimas](#editing-an-embedded-app). Įsitikinkite, kad srityje rodoma įdėtosios programos, kurią norite pašalinti, informacija, tada spustelėkite mygtuką **Naikinti**.
- Kadangi įdėtoji programa įrašoma kaip pritaikymo asmeniniams poreikiams duomenys, išvalius puslapio pritaikymo asmeniniams poreikiams elementus taip pat bus pašalintos visos to puslapio įdėtosios programos. Atminkite, kad puslapio pritaikymo asmeniniams poreikiams elementų šalinimas yra nuolatinis veiksmas ir jo atšaukti negalima. Norėdami šalinti puslapio pritaikymo asmeniniams poreikiams elementus, pasirinkite **Parinktys**, tada pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams** ir galiausiai spustelėkite mygtuką **Išvalyti**. Atnaujinus naršyklę bus pašalinti visi ankstesni šio puslapio pritaikymo asmeniniams poreikiams elementai. Daugiau informacijos apie tai, kaip optimizuoti puslapius naudojant pritaikymo asmeniniams poreikiams elementus, žr. puslapyje [Vartotojo patirties pritaikymas asmeniniams poreikiams](personalize-user-experience.md).

## <a name="appendix"></a>Priedas

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Kūrėjas] Nurodymas, kurioje vietoje galima įdėti programą

Pagal numatytuosius parametrus vartotojai gali įdėti programas bet kuriame puslapyje – į meniu mygtuką „Power Apps“ arba tiesiogiai į puslapį kaip skirtuką, „FastTab“, mentę ar naują skyrių darbo srityje. Tačiau, jei reikia, kūrėjai gali taip pat sukonfigūruoti šią funkciją, kad programas būtų galima įdėti tik tam tikruose puslapiuose, naudodami toliau pateiktus būdus.

- **isPowerAppPersonalizationEnabled** – jei šis būdas pateikia tam tikro puslapio reikšmę „false“, tada meniu mygtukas „Power Apps“ nebus rodomas, o vartotojai negalės įdėti programų į jokią šio puslapio vietą, įskaitant skirtukus.
- **isPowerAppTabPersonalizationEnabled** – jei šis būdas pateikia tam tikro puslapio reikšmę „false“, tada vartotojai negalės tiesiogiai įdėti programų į puslapį kaip skirtuką, „FastTab“ arba panoraminę skiltį. Vartotojai vis tiek galės įdėti programas per meniu mygtuką „Power Apps“, jei įdėjimo funkciją tame puslapyje galima naudoti.

Toliau pateiktame pavyzdyje parodoma nauja klasė ir du būdai, kaip sukonfigūruoti, kur galima įdėti programas.

```powerapps
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]