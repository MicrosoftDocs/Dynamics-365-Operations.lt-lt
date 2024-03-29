---
title: Drobės programų įdėjimas iš „Power Apps”
description: Šiame straipsnyje paaiškinama, kaip įdėti žiniatinklio programėles Microsoft Power Apps iš kliento į kliento, kad būtų padidintos produkto funkcijos.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: d7dc45e56c5fa616c288ebb4b919f039b7358794
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123661"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Drobės programų įdėjimas iš „Power Apps”

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

„Microsoft Power Apps“ yra paslauga, leidžianti kūrėjams ir įprastiems vartotojams kurti pasirinktines verslo programas, skirtas mobiliesiems įrenginiams, planšetiniams kompiuteriams ir žiniatinkliui, nerašant kodo. Finansų ir operacijų programėlės palaiko integravimą su Power Apps. Lauko programėles, kurias jūs, jūsų organizacija ar platesnė struktūra gali būti įdėtos į finansų ir operacijų programėles, kad būtų padidintos produkto funkcijos. Pavyzdžiui, galite sukurti lauko programą, kuri Power Apps papildo finansų ir operacijų programėlę informacija, nuskaitoma iš kitos sistemos.

Norėdami daugiau sužinoti apie drobės programų įdėjimą, peržiūrėkite trumpą vaizdo įrašą [Kaip patalpinti drobės programas](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Įdėtosios „Power Apps“ drobės programos įtraukimas į puslapį

Prieš įdedant drobės programą iš „Power Apps“ į klientą, reikia rasti arba sukurti programą su norimais vaizdiniais elementais arba funkcijomis. Šiame straipsnyje nėra išsamaus programėlių kūrimo proceso aprašymo. Jei naudojate „Power Apps” pirmą kartą, žr. [„Power Apps” dokumentaciją](/powerapps/).

Yra trys būdai įtraukti lauko programą į finansų ir operacijų programą. Galite naudoti geriausiai jūsų scenarijui tinkantį būdą. 

- Drobės programos įdėjimas į **„Power Apps”** mygtuką puslapio standartinėje veiksmų srityje. Tokiu būdu pridėtos programos bus rodomos kaip **„Power Apps”** meniu mygtuko elementai, o programos bus atidaromos šoninėse srityse. 
- Drobės programos įdėjimas tiesiai į esamą puslapį kaip naują skirtuko puslapį (pagrindinį tabuliacijos skirtuką, „FastTab", mentę arba darbo srities skyrių).
- Naudodami skelbimų skelbimų sritį sukurkite naują drobės programos viso puslapio patirtį.

Konfigūruodami savo įdėtąją drobės programą, galite pasirinkti vieną lauką, kurį norite siųsti kaip kontekstą į programą. Šis veiksmas programai suteikia galimybę reaguoti pagal duomenis, kuriuos tuo metu peržiūrite.

> [!NOTE]
> Negalima naudoti šio mechanizmo modeliu pagrįstoms programoms įdėti.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>Drobės programos įdėjimas esamame puslapyje

Toliau pateiktoje procedūroje parodyta, kaip įdėti drobės programą iš „Power Apps“ į esamą puslapį.

1. Atidarykite puslapį, kuriame norite įdėti drobės programą. Tai bus puslapis su duomenimis, kuriuos reikia kaip įvestį perduoti programai.
2. Atidarykite sritį **Įtraukti programą iš „Power Apps“**, atlikę tolesnius veiksmus.

    - Jei programa bus įdedama tiesiai į puslapį, pasirinkite **Parinktys** \> **Pritaikyti šį puslapį asmeniniams poreikiams** \> **Daugiau**, tada atlikite vieną iš toliau nurodytų veiksmų.

        - Jei įjungta funkcija **Viso puslapio programos**, pasirinkite **Įtraukti puslapį**, tada pasirinkite sritį, į kurią norite įtraukti programą. Norėdami įdėti programą į **„Power Apps”** meniu mygtuką, pasirinkite veiksmų sritį. Jei norite įdėti programą tiesiai į puslapį, pasirinkite atitinkamą skirtuką, „FastTab“, mentę arba skyrių (jei naudojate darbo sritį). Tada srityje **Įtraukti programą** pasirinkite **„Power Apps”**.
        - Jei funkcija **Viso puslapio programos** išjungta, pasirinkite **Įtraukti programą iš „Power Apps”**, tada pasirinkite sritį, į kurią norite įtraukti programą. Norėdami įdėti programą į **„Power Apps”** meniu mygtuką, pasirinkite veiksmų sritį. Jei norite įdėti programą tiesiai į puslapį, pasirinkite atitinkamą skirtuką, „FastTab“, mentę arba skyrių (jei naudojate darbo sritį).

    - Jei programa bus pasiekiama naudojant meniu mygtuką **„Power Apps“**, taip pat galite pasirinkti standartinės veiksmų srities meniu mygtuką **„Power Apps”** ir tada pasirinkti **Įtraukti programą**.

3. Konfigūruokite įdėtąją programą. Norėdami gauti daugiau informacijos, toliau šiame [straipsnyje žr. skyrių Interneto](#configuring-a-canvas-app) programos konfigūravimas.
4. Patvirtinę, kad konfigūracija teisinga, pasirinkite **Įterpti**.

    - Jei funkcija **Įrašyti rodiniai** išjungta, būsite paraginti atnaujinti naršyklę, kad pamatytumėte įdėtąją programą.
    - Jei funkcija **Įrašyti rodiniai** įjungta, turite įrašyti rodinį, kad pakeitimas būtų išlaikytas.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>Drobės programos įdėjimas kaip viso puslapio patirties iš ataskaitų srities

Galbūt norėsite įdėti lauko programėlę iš skelbimų skelbimų lentos, jei programa nėra susijusi su esamu puslapiu arba jei tiesiog norite išk patalpėti programą kaip viso puslapio patirtį finansų ir operacijų programoje.

> [!NOTE]
> Kad šį galimybė būtų pasiekiama, naudodami funkcijų valdymą turite įjungti funkciją **Viso puslapio programos**. 

1. Atidarykite numatytąją ataskaitų sritį.
2. Pasirinkite ir sulaikykite (arba spustelėkite dešiniuoju pelės mygtuku) puslapį, pasirinkite Pritaikyti asmeniniams **poreikiams**, tada **pasirinkite Įtraukti** puslapį.
3. Srityje **Įtraukti puslapį** pasirinkite **„Power Apps”**.
4. Konfigūruokite įdėtąją programą. Norėdami gauti daugiau informacijos, toliau šiame [straipsnyje žr. skyrių Interneto](#configuring-a-canvas-app) programos konfigūravimas.
5. Norėdami **įtraukti programą į** skelbimų skelbimų skelbimų sritį kaip naują išklotąją sritį, pasirinkite Įrašyti.
6. Pasirinkite naują ataskaitų srities plytelę ir patvirtinkite, kad drobės programa rodoma taip, kaip tikėtasi.

### <a name="configuring-a-canvas-app"></a>Drobės programos konfigūravimas

Kai įdedate drobės programą, turite nustatyti toliau pateikiamus parametrus.

- **Pavadinimas** – įveskite tekstą, kuris turi būti rodomas mygtuke ar skirtuke, kuriame bus įdėtoji programa. Daugeliu atveju patartina pakartoti programos pavadinimą šiame lauke.
- **Programos ID** – nurodomas globaliai unikalus identifikatorius (GUID), skirtas drobės programai, kurią norite įdėti. Norėdami gauti šią reikšmę, raskite programą puslapyje [make.powerapps.com](https://make.powerapps.com) ir raskite lauką **Programos ID**, pateiktą dalyje **Informacija**.
- **Programos įvesties kontekstas** – galite pasirinktinai pasirinkti lauką su duomenimis, kuriuos kaip įvestį norite perduoti programai. Norėdami gauti informacijos apie tai, kaip programa gali pasiekti duomenis, išsiųstus iš finansų ir operacijų programėlių, [žr](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps). programos, kuri vėliau padeda kurti duomenis, siunčiamus iš finansų ir operacijų programėlių, toliau šiame straipsnyje.

    Pradedant 10.0.19 versija, dabartinis juridinis subjektas taip pat perduodamas kaip kontekstas drobės programai naudojant **cmp** URL parametrą. Toks veikimo būdas neturės įtakos tikslinei drobės programai, kol ši programa naudos šią informaciją.

- **Programos dydis** – pasirinkite įdedamos programos tipą. Jei kuriate mobiliesiems įrenginiams skirtas programas, pasirinkite parinktį **Plona**, o jei kuriate planšetiniams kompiuteriams skirtas programas, pasirinkite **Plati**. Šiuo parametru užtikrinama, kad įdėtajai programai bus skirta pakankamai vietos.
- **Juridiniai subjektai** – galite pasirinkti juridinius subjektus, kurie galės naudoti programą. Pagal numatytuosius parametrus programa pasiekiama visiems juridiniams subjektams. Ši parinktis pasiekiama, tik kai įdedate tiesiai į esamą puslapį, o funkcija **[Įrašyti rodiniai](saved-views.md)** yra išjungta.

## <a name="sharing-an-embedded-app"></a>Įdėtosios programos bendrinimas

Įdėję drobės programą į puslapį ir įsitikinę, kad ji veikia tinkamai, galite programą bendrinti su kitais sistemos vartotojais. Norėdami bendrinti įdėtąją drobės programą, atlikite toliau pateiktus veiksmus.

1. [Bendrinkite drobės programą „Power Apps”](/powerapps/maker/canvas-apps/share-app) su tinkamais vartotojais, kad jie galėtų pasiekti programą tiesiai „Power Apps”.
2. Personalizavimo, susieto su įdėtąją programa, bendrinimas su norimais vartotojais. Galite naudoti bet kurį iš toliau nurodytų būdų.

    - **Publikuoti rodinį (rekomenduojama):** jei funkcija **[Įrašyti rodiniai](saved-views.md)** yra įjungta, rekomenduojamas ir pageidaujamas būdas yra kurti rodinį, kuriame yra įdėtoji drobės programa, ir publikuoti šį rodinį norimiems vartotojams. Šis būdas užtikrina, kad visi vartotojai, turintys saugos vaidmenis, kuriems skirtas publikuotas rodinys, matys drobės programą puslapyje.

        Taip pat galite publikuoti drobės programą, kuri skelbimų srityje buvo įdėtoji kaip viso puslapio informacija. Skelbimų srityje pasirinkite ir laikykite (arba spustelėkite dešiniuoju pelės mygtuku) išklotąją dalį, susijusią su programa, pasirinkite Personalizuoti, tada **pasirinkite** puslapį **Publikuoti**. Rodoma patirtis, panaši į patirtį *Publikavimo rodiniai*, ir galite pasirinkti saugos vaidmenis, į kuriuos ją publikuosite. Jei 10.0.21 arba naujesniame naujinyje įjungta funkcija **Įrašytų rodinių pagerintas juridinių subjektų palaikymas**, taip pat galite publikuoti programą į norimus juridinius objektus.

    - Jei įjungta funkcija **Įrašyti rodiniai**, sistemos administratoriai gali pateikti personalizavimą, kuriame yra drobės programa, atitinkamai vartotojų grupei per puslapį **Personalizavimas**. Taip pat galite eksportuoti jūsų puslapio personalizavimus ir siųsti juos vienam ar keliems vartotojams. Tada kiekvienas iš šių vartotojų gali importuoti personalizavimą. Eksportuoti ir importuoti personalizavimus galite pasirinkę personalizavimo įrankių juostos mygtukus.

> [!NOTE]
> Jei lauko programa bendrinama su išoriniais vartotojais, jie negali naudoti įdėtosios programos finansų ir operacijų programėlių viduje. Tačiau jie gali pasiekti programą tiesiogiai programoje „Power Apps”. Išoriniai vartotojai apima svečius ir vartotojus, kurie nepriklauso Microsoft 365 "Azure Directory", kurioje įdiegta finansų ir operacijų programa.

Informacijos apie produkto pritaikymo galimybes ir kaip jas naudoti žr. temoje [Vartotojo patirties pritaikymas asmeniniams poreikiams](personalize-user-experience.md).

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Kurti lauko programą, kurioje naudojami duomenys, siunčiami iš finansų ir operacijų programėlių

Kuriant lauko programą, kuri bus įdėta į finansų ir operacijų programą, viena svarbi proceso dalis yra naudoti įvesties duomenis iš tos finansų ir operacijų programos. Iš programavimo Power Apps patirties, įvesties duomenis, kurie perduoti iš finansų ir operacijų programos, galima pasiekti naudojant **Param("EntityId") kintamąjį**. Taip pat, pradedant nuo versijos 10.0.19, dabartinis juridinis subjektas taip pat bus perduotas kaip kontekstas žiniatinklio programai naudojant **Param (cmp)** URL parametrą. 

Pavyzdžiui, programos funkcijoje "OnStart" galite nustatyti įvesties duomenis iš finansų ir operacijų programėlių kaip kintamąjį, pvz.:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Drobė programos peržiūra

Norėdami peržiūrėti finansų ir operacijų programėlių puslapyje įdėtąją lauko programą, tiesiog eikite į puslapį, kuriame yra įdėtoji programa. Atminkite, kad programas galima pasiekti naudojant mygtuką **„Power Apps”**, esantį standartinėje veiksmų srityje. Taip pat jos gali atsirasti puslapyje tiesiogiai kaip naujas skirtukas, „FastTab“, mentė arba nauja skiltis darbo srityje. Vartotojams pirmą kartą bandant įkelti programą į puslapį, jie bus paraginti prisijungti. Šis veiksmas užtikrina, kad vartotojai turėtų atitinkamas teises programėlei naudoti.

## <a name="editing-an-embedded-app"></a>Įdėtosios programos redagavimas

Įdėjus programą į puslapį, gali reikėti atlikti tam tikrus programos konfigūracijos keitimus. Pavyzdžiui, galbūt norėsite modifikuoti su įdėtąja programa susietą žymę arba galbūt buvo sukurta nauja programos versija ir jums reikia atnaujinti programos ID bei nurodyti naujausią programą.

Atlikite toliau nurodytus veiksmus norėdami redaguoti įdėtosios programos konfigūraciją.

1. Pasirinkite sritį **Redaguoti programą**.

    - Jei įdėtoji programa pasiekiama per meniu mygtuką „Power Apps“, pasirinkite ir laikykite (arba dešiniuoju pelės mygtuku spustelėkite) meniu mygtuką „Power Apps“ ir pasirinkite **Pritaikyti asmeniniams poreikiams**. Išplečiamajame meniu **Pasirinkti programą** pasirinkite, kurią programą norite konfigūruoti.
    - Jei įdėtoji programa rodoma tiesiogiai puslapyje, pasirinkite **Parinktys**, tada pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams**. Naudodami įrankį **Pasirinkti** spustelėkite įdėtąją programą.
    - Jei įdėtoji programa buvo įtraukta iš ataskaitų srities, atidarykite ataskaitų sritį, pasirinkite ir laikykite (arba dešiniuoju pelės klavišu spustelėkite) plytelę, susietą su drobės programa, pasirinkite **Pritaikyti asmeniniams poreikiams**, tada – **Redaguoti puslapį**.

2. Atlikite reikiamus programos konfigūracijos keitimus, tada spustelėkite **Įrašyti**.

## <a name="removing-an-app"></a>Programos pašalinimas

Įdėjus programą į puslapį, jei reikia, ją galima pašalinti keliais būdais.

- Eikite į **programos srities redagavimą** naudodami instrukcijas, pateiktas anksčiau [šiame straipsnyje skyriuje](#editing-an-embedded-app) Įdėtųjų programų redagavimas. Įsitikinkite, kad srityje rodoma įdėtosios programos, kurią norite pašalinti, informacija, tada spustelėkite mygtuką **Naikinti**.
- Jei įdėtoji programa buvo įtraukta iš ataskaitų srities, atidarykite ataskaitų sritį, pasirinkite ir laikykite (arba dešiniuoju pelės klavišu spustelėkite) plytelę, susietą su drobės programa, pasirinkite **Pritaikyti asmeniniams poreikiams**, tada – **Pašalinti puslapį**. 
- Kadangi įdėtoji programa įrašoma kaip pritaikymo asmeniniams poreikiams duomenys, išvalius puslapio pritaikymo asmeniniams poreikiams elementus taip pat bus pašalintos visos to puslapio įdėtosios programos. Atminkite, kad puslapio pritaikymo asmeniniams poreikiams elementų šalinimas yra nuolatinis veiksmas ir jo atšaukti negalima. Norėdami šalinti puslapio pritaikymo asmeniniams poreikiams elementus, pasirinkite **Parinktys**, tada pasirinkite **Pritaikyti šį puslapį asmeniniams poreikiams** ir galiausiai spustelėkite mygtuką **Išvalyti**. Atnaujinus naršyklę bus pašalinti visi ankstesni šio puslapio pritaikymo asmeniniams poreikiams elementai. Daugiau informacijos apie tai, kaip optimizuoti puslapius naudojant pritaikymo asmeniniams poreikiams elementus, žr. puslapyje [Vartotojo patirties pritaikymas asmeniniams poreikiams](personalize-user-experience.md).

## <a name="appendix"></a>Priedas

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Programuotojas] Formos app modeliavimas

Šiame straipsnyje daugiausia dėmesio skiriama įdėtoms žiniatinklio programoms naudojant personalizavimą, Visual Studio programuotojai taip pat gali pasirinkti pridėti programėlę iš interneto svetainių naudodami programavimo patirtį. Norėdami tai padaryti, tiesiog į formą pridėkite PowerAppsHostControl. Valdiklyje galimos metaduomenų ypatybės suteikia tų pačių galimybių kaip ir personalizavimo funkcijos.

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

