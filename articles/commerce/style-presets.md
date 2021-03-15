---
title: Darbas su išankstinėmis stilių parinktimis
description: Šioje temoje aprašoma, kaip svetainių daryklėje „Microsoft Dynamics 365 Commerce“ dirbti su išankstinėmis stilių parinktimis.
author: phinneyridge
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1bd8f6e31afa300c5e7687a657ae2807995af8d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006315"
---
# <a name="work-with-style-presets"></a>Darbas su išankstinėmis stilių parinktimis

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip svetainių daryklėje „Microsoft Dynamics 365 Commerce“ dirbti su išankstinėmis stilių parinktimis.

## <a name="overview"></a>Peržiūra

Išankstinė stilių parinktis yra visų autentiškų stilių verčių rinkinys, naudojamas svetainės temoje. Jis gali būti naudojamas norint iš karto pakeisti svetainės įvaizdį iš svetainės daryklės. Išankstinė stilių parinktis suteikia galimybę „Commerce” svetainės daryklės autoriams greitai pakeisti, peržiūrėti ir suaktyvinti savo svetainės stilių vertes nenaudodami „Cascading Style Sheets ” (CSS) arba nediegiant temų. Šrifto stiliai, mygtukų stiliai ir svetainės spalvos yra tipiški stiliaus kintamųjų, kuriuos galima tvarkyti naudojant išankstinėmis stilių parinktimis, pavyzdžiai.

Stiliaus kintamųjų rinkinys, prieinamas svetainėje, nustatomas pagal temą ir modulio biblioteką, kuri įdiegiama į svetainės nuomininką. „Dynamics 365 Commerce” internetinis programinės įrangos kūrimo rinkinys (SDK – angl. software development kit) leidžia kūrėjams pritaikyti didžiausią kiekį (arba tik kelis) reikiamus autentiškus stilių kintamuosius per skirtą laiką. Įgalinę daugiau stilių kintamųjų, temos kūrėjas gali patikėti galutinius svetainės stilių svetainės pakeitimus daryklės autoriams. Todėl ne kūrėjai gali atnaujinti ir peržiūrėti svetainės stilius naudodami įrankių rinkinį. Funkcija taip pat naudinga bet kokiam scenarijui, kai tiesioginiai temų pakeitimai arba „CSS” sukels nereikalingų pridėtinių išlaidų.

Temoms, kuriose įgalinti autentiški stiliaus kintamieji, reikia numatytosios išankstinės stiliaus parinkties. Jie pasirinktinai gali įtraukti papildomas parinktis, nes tai įeina į įdiegtos temos paketą. Pavyzdžiui, galima įdiegti temą, kuri turi vieną numatytąją „šiuolaikiškas šviesus” stiliaus parinktį. Taip pat gali būti ir papildomų išankstinių stiliaus parinkčių be numatytosios, pavyzdžiui, „šiuolaikiškas tamsus”, „senoviškas šviesus” arba „senoviškas tamsus”. Kūrėjai kuria šias integruotas temų išankstines parinktis ir jos gali būti naudojamos kaip pirmieji svetainių stilių potėpiai.

Svetainės daryklėje kūrėjai gali pasirinkti iš integruotų temų parinkčių arba gali sukurti savo pačių stilių išankstines parinktis ir tinkinimą naudojant įgalintus stilių kintamuosius.  Išankstinė stiliaus parinktis gali būti peržiūrėta svetainės daryklėje prieš aktyvuojant ją tiesioginėje svetainėje. Peržiūrėjus kūrėjo stiliaus pakeitimus, išankstinė stiliaus parinktis gali būti nustatyta kaip „aktyvi” tiesioginėje svetainėje.

## <a name="preview-a-style-preset"></a>Išankstinės stiliaus parinkties peržiūra

Norėdami peržiūrėti išankstinę stiliaus parinktį svetainėje svetainės daryklėje, atlikite šiuos veiksmus.

1. Kairiojoje jūsų svetainės naršymo srityje eikite į **Svetainės parametrai \> Dizainas**.
1. **Išankstinės stiliaus parinktys** skirtuke, dizaino rengyklės viršuje, **Galimos išankstinės parinktys** sąraše pasirinkite **Peržiūrėti**, kad pereitumėte į išankstinių parinkčių doroklį.

    Jei **Galimos išankstinės parinktys** sąraše šiuo metu nėra išankstinių parinkčių, peržiūrėkite [Pasirinktos išankstinės parinkties kūrimas](#create-a-custom-style-preset), kad sužinotumėte, kaip sukurti pasirinktinę išankstinę stiliaus parinktį.

    > [!NOTE]
    > Išankstinės parinktys, įtrauktos į temą, pažymėtos **Integruota** ženkleliu. Šios integruotos išankstinės parinktys yra skirtos tik skaityti. Norėdami nukopijuoti integruotą išankstinę parinktį kaip naują tinkinamą išankstinę parinktį , pasirinkite elipsės mygtuką (**...**)  parinkčiai ir pasirinkite **Įrašyti kaip**.

1. Komandų juostoje pasirinkite **Peržiūrėti**.
1. Pasirinkite URL iš savo svetainės, kad galėtumėte peržiūrėti išankstinę stiliaus parinktį, tada pasirinkite **Gerai**.
1. Pasirinkite kanalui ir lokalei būdingą URL variantą pasirinkdami varianto pavadinimą. Atidaromas naujas peržiūros naršyklės langas, kuriame pasirinkta išankstinė stiliaus parinktis pritaikoma konkrečiam puslapiui.

> [!NOTE]
> Peržiūros URL yra nuolatinis ir autentifikuotas. Todėl galite kopijuoti, įklijuoti ir siųsti kitiems patvirtintiems bendradarbiams peržiūrai prieš nustačius į „aktyvi ” būsena savo tiesioginėje svetainėje. URL peržiūra taip pat naudinga tikrinant stilius skirtinguose įrenginiuose, skirtingose naršyklėse ir skirtinguose ekranuose.

> [!TIP]
> Redaguojant išankstinę stiliaus parinktį, gali būti naudinga palikti atvirą peržiūros naršyklės langą, kad jį atidarytumėte atskirame naršyklės lange, kad galėtumėte greitai patikrinti savo keitimus. Išsaugoję išankstinės parinkties pakeitimus, atnaujinkite atidarytą peržiūros naršyklės langą, kad patikrintumėte vartotojo patirtį.

## <a name="create-a-custom-style-preset"></a>Pasirinktinos išankstinės stiliaus parinkties kūrimas

Norėdami sukurti pasirinktiną išankstinę stiliaus parinktį svetainėje svetainės daryklėje , atlikite šiuos veiksmus.

1. Kairiojoje jūsų svetainės naršymo srityje eikite į **Svetainės parametrai \> Dizainas**.
1. **Išankstinės stiliaus parinktys** skirtuke dizaino rengyklės viršuje, komandų juostoje, pasirinkite **Nauja išankstinė parinktis**.
1. Įveskite naujos išankstinės parinkties pavadinimą ir aprašą ir pasirinkite **Įrašyti**. Sukuriama nauja tinkinama išankstinė parinktis, kuri naudoja numatytąsias temos vertes kaip pradžios tašką.

> [!NOTE]
> Taip pat galite kurti naują pasirinktinę išankstinę stiliaus parinktį pagal esamą parinktį pažymėję elipsės mygtuką ( **...**) tai parinkčiai ir tada pasirinkdami **Įrašyti kaip**. Kitu atveju galite pasirinkti **Įrašyti kaip** esamo doroklio komandų juostoje.

## <a name="modify-global-and-module-type-style-values"></a>Visuotino ir modulio tipo stiliaus verčių modifikavimas

Kai kurie temos stiliaus kintamieji yra bendrai naudojami su keliais modulių tipais. Šie stiliaus kintamieji vadinami *visuotinais* stiliaus kintamaisiais. Pavyzdžiuose yra pirminės svetainės spalvos, numatytieji šrifto stiliai ir mygtukų stiliai. Nustatydami visuotinius kintamuosius, galite pakeisti skirtingų modulių tipų įvaizdį.

Kai kurios stiliaus vertės gali būti unikalios modulio tipui arba jos gali pasirinktinai perrašyti numatytąją visuotiną vertę. Jei svetainės tema įdiegė modulio tipo stiliaus kintamuosius, svetainės daryklės autoriai gali tinkinti modulio tipo stilių nepaisydami visuotinių parametrų. Modulio tipo kintamieji gali padidinti arba perrašyti visuotino stiliaus kintamuosius temoje.

> [!NOTE]
> Stiliaus verčių hierarchija svetainėje elgiasi taip:. Stiliaus vertės, atsirandančios toliau į dešinę, perrašo stiliaus vertes, esančias kairėje pusėje.
>
> Temos numatytosios vertės \<Visuotino stiliaus vertės \< Modulio tipo stiliaus vertės \<CSS perrašyti

Norėdami keisti išankstinę stiliaus parinktį arba modulio tipo vertes svetainės daryklėje, atlikite šiuos veiksmus.

1. Kairiojoje jūsų svetainės naršymo srityje eikite į **Svetainės parametrai \> Dizainas**.
1. **Išankstinės stiliaus parinktys** skirtuke, dizaino rengyklės viršuje pasirinkite bet kurios išankstinės stiliaus parinkties **Peržiūrėti**, kad patektumėte į išankstinės stiliaus parinkties doroklį.
1. Pasirinkite **Peržiūrėti** ir tada vykdykite URL žymėjimo veiksmus, kad peržiūrėtumėte išankstinę stiliaus parinktį visame naršyklės lange. Palikite šį peržiūros naršyklės langą atidarytą.
1. Išankstinės parinkties doroklyje, viršutiniame dešiniajame kampe, pasirinkite **Redaguoti**.
1. Norėdami pakeisti kai kurias visuotino stiliaus vertes, naudokite stiliaus kintamųjų valdiklius.
1. Doroklio viršuje **Moduliai** skirtuke **Visuotinas** skirtuko dešinėje, pasirinkite modulio tipą, kurį norite stilizuoti.
1. Naudokite stiliaus valdiklius, kad pakeistumėte kai kurias modulio tipo vertes.
1. Kai esate pasiruošę peržiūrėti savo keitimus, pasirinkite **Įrašyti** komandų juostoje.
1. Sugrįžkite į atvirą peržiūros naršyklės langą ir atnaujinkite jį. Viso naršyklės lango peržiūra naudinga tikrinant stilių pakeitimus skirtingais rodinio stabdos taškais skirtingose naršyklėse ir skirtingose renginių platformose.
1. Pabaigę visus keitimus ir patikrintus, pasirinkite **Baigti redagavimą** viršutiniame dešiniajame doroklio kampe.

> [!NOTE]
> Jeigu redaguojate išankstinę stiliaus parinktį, kuri šiuo metu aktyvi jūsų svetainėje, doroklyje pamatysite mėlyną ženklelį **Aktyvus**. Šis ženklelis nurodo, kad šiuo metu išankstinė parinktis yra aktyvi jūsų svetainėje. Pakeitus aktyvią parinktį, pasirinkite **Publikuoti**, kad tie pakeitimai atsirastų jūsų tiesioginėje svetainėje.

## <a name="make-a-new-style-preset-active-on-your-live-site"></a>Sukurkite naują išankstinę stiliaus parinktį aktyvią jūsų tiesioginėje svetainėje

Norėdami nustatyti išankstinę stiliaus parinktį kaip naują aktyvią išankstinę parinktį savo svetainėje, atlikite šiuos veiksmus.

- Pasirinkite **Nustatyti kaip aktyvų mygtuką** vienoje iš šių vietų:

    - Komandų juosta išankstinės stiliaus parinkties doroklyje
    - Elipsės meniu (**...**) bet kuriai galimai išankstinei parinkčiai pagrindiniame rodinyje, esančiame **Išankstinės stiliaus parinktys** skirtuke **Svetainės parametrai \>Dizainas**

Išankstinės stiliaus parinkties vertės yra aktyvios jūsų viešoje svetainėje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Įtraukti logotipą](add-logo.md)

[Pasirinkti svetainės temą](select-site-theme.md)

[Darbas su CSS perrašymo failais](css-override-files.md)

[Įtraukti parankinių piktogramą](add-favicon.md)

[Įtraukti pasveikinimo pranešimą](add-welcome-message.md)

[Įtraukti informaciją apie autorių teises](add-copyright-notice.md)

[Kalbų įtraukimas į savo svetainę](add-languages-to-site.md)

[Įtraukite scenarijaus kodą į svetainės puslapius, kad būtų palaikoma telemetrija](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]