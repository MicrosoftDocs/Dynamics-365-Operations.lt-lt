---
title: Darbas su esamais maketais
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ dirbti su iš anksto nustatytais maketais.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 56ad992b6a9fd6fce09cadad70b8098acdc74ac0
ms.sourcegitcommit: 1eef00796f7c5511f432b01800cdf8920992d7d5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/04/2022
ms.locfileid: "8090850"
---
# <a name="work-with-preset-layouts"></a>Darbas su esamais maketais

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“ dirbti su iš anksto nustatytais maketais.

Prieš atlikdami šioje temoje aprašytas procedūras, būtinai perskaitykite temą [Iš anksto nustatyti ir pasirinktiniai maketai](templates-layouts-overview.md#preset-and-custom-layouts). Bendra apžvalga pateikiama temoje [Šablonų ir maketų apžvalga](templates-layouts-overview.md).

## <a name="create-a-new-preset-layout"></a>Naujo iš anksto nustatyto maketo kūrimas

Iš anksto nustatytą maketą galima kurti dviem būdais. Esamą pasirinktinį maketą galite įrašyti kaip naują iš anksto nustatytą maketą arba iš anksto nustatytą maketą galite kurti nuo pradžių.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Iš anksto nustatyto maketo kūrimas naudojant esamą pasirinktinį maketą

Norėdami iš anksto nustatytą maketą kurti naudodami esamą pasirinktinį maketą, atlikite toliau nurodytus veiksmus.

1. Atidarykite esamą puslapį, kuriame šiuo metu nenaudojamas iš anksto nustatytas maketas, ir kurio modulių struktūrą norite pakartotinai naudoti kituose svetainės puslapiuose.
1. Norėdami patikrinti puslapį, pasirinkite **Redaguoti**.
1. Pasirinkite **Įrašyti kaip naują maketą**. Rodomas dialogo langas **Įrašyti kaip naują maketą**.
1. Įveskite iš anksto nustatyto maketo pavadinimą ir aprašymą. Jūsų įvestos reikšmės bus rodomos kitiems autoriams, kai jie kurs naujus puslapius naudodami jūsų maketą arba jį įjungs. Todėl įveskite reikšmes, kurios bus naudingos puslapio autoriams.
1. Pasirinkite **Gerai**.

Iš anksto nustatytas maketas nuo šiol bus pasiekiamas kuriant naujus puslapius arba pasirenkant kitą puslapio toje pačioje šablono hierarchijoje maketą.

> [!TIP]
> Norėdami greitai peržiūrėti, ar konkretus puslapis šiuo metu yra susietas su iš anksto nustatytu maketu, puslapių sąrašo rodinyje pasirinkite puslapį ir ypatybių srityje dešinėje patikrinkite maketo metaduomenis.

### <a name="create-a-new-preset-layout"></a>Naujo iš anksto nustatyto maketo kūrimas

Norėdami iš anksto nustatytą maketą kurti nuo pradžių, atlikite toliau nurodytus veiksmus.

1. Kairėje naršymo srityje pasirinkite **Maketai**.
1. Pasirinkite **Naujas maketas**. Rodomas dialogo langas **Naujas maketas**.
1. Pasirinkite šabloną, kurį naudosite iš anksto nustatytam maketui.
1. Įveskite iš anksto nustatyto maketo pavadinimą ir aprašymą. Jūsų įvestos reikšmės bus rodomos kitiems autoriams, kai jie kurs naujus puslapius naudodami jūsų maketą arba jį įjungs. Todėl įveskite reikšmes, kurios bus naudingos puslapio autoriams.
1. Pasirinkite **Gerai**, kad sukurtumėte naują iš anksto nustatytą maketą ir atidarytumėte maketų rengyklę.
1. Maketų rengyklėje įtraukite modulių ir juos konfigūruokite naudodami struktūros medį kairėje pusėje ir ypatybių sritį dešinėje pusėje. (Šis procesas panašus į šablono modulių įtraukimo ir konfigūravimo naudojant šablonų rengyklę procesą.) Modulių išdėstymas ir bet kokie užrakinti numatytieji parametrai tampa bet kokių puslapių, kuriuose naudojamas šis iš anksto nustatytas maketas, centralizuota modulių konfigūracija.

## <a name="modify-a-preset-layout"></a>Iš anksto nustatyto maketo modifikavimas

Norėdami modifikuoti iš anksto nustatytą maketą, atlikite toliau nurodytus veiksmus.

1. Kairėje naršymo srityje pasirinkite **Maketai**.
1. Maketo rengyklės kairėje pusėje esančiame struktūros medyje pasirinkite modulį, kurį norite modifikuoti. Tuomet atlikite bet kuriuos iš toliau nurodytų veiksmų.

    - Norėdami modulį perkelti aukštyn arba žemyn jo pirminiame modulyje, pasirinkite modulio daugtaškio mygtuką (**...**), tada pasirinkite **Perkelti aukštyn** arba **Perkelti žemyn**.
    - Norėdami pakeisti modulio numatytuosius parametrus, naudokite ypatybių sritį, kad įvestumėte numatytąsias reikšmes ir pasirinktinai jas užfiksuotumėte visuose paskesniuose puslapiuose.
    - Norėdami į konteinerio modulius įtraukti naujų modulių ar fragmentų, pasirinkite daugtaškio mygtuką, tada pasirinkite **Įtraukti modulį** arba **Įtraukti fragmentą**.
    - Norėdami iš maketo pašalinti modulį, pasirinkite daugtaškio mygtuką, tada pasirinkite **Naikinti**.

## <a name="change-a-preset-layout-theme"></a>Iš anksto nustatyto maketo temos keitimas

Paprastai nustatoma visų puslapių, kuriuose naudojamas iš anksto nustatytas maketas, numatytoji tema.

Norėdami nustatyti arba pakeisti visų antrinių puslapių, kuriuose naudojamas iš anksto nustatytas maketas, temą, atlikite toliau nurodytus veiksmus.

1. Maketo rengyklės kairėje pusėje esančiame struktūros medyje pasirinkite puslapio konteinerio modulį. (Paprastai šis modulis yra antrasis mazgas, o jo pavadinimas yra **Numatytasis puslapis**.)
1. Viduje konors **tema** ypatybių srities dešinėje pasirinkite temą.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Iš anksto nustatyto maketo įrašymas, įregistravimas, peržiūra ir publikavimas

Norėdami įrašyti ir įregistruoti savo iš anksto nustatytą maketą, atlikite toliau nurodytus veiksmus.

1. Maketo rengyklės viršuje pasirinkite **Įrašyti**. Įrašyti keitimai neturės įtakos tolesniems puslapiams, kol jie nebus įrašomi ir atrakinami.
1. Pasirinkite **Baigti redagavimą**. Dabar jūsų keitimai yra aptinkami atsiuntimo srauto darbo eigose.

Norėdami peržiūrėti keitimus atidarykite esamą puslapį, kuriame naudojamas iš anksto nustatytas maketas, arba naudodami maketą sukurkite naują puslapį.

Kai peržiūrėsite iš anksto nustatyto maketo keitimus, atlikite vieną iš toliau nurodytų veiksmų, kad maketas būtų publikuojamas jūsų aktyvioje svetainėje.

1. Eikite į **Maketai**, pasirinkite maketą, tada pasirinkite **Publikuoti**.
1. Norėdami atidaryti maketų rengyklę pasirinkite maketo pavadinimą, tada pasirinkite **Publikuoti**.
1. Publikuokite puslapį, kuris nurodo nepaskelbtą maketą. Maketas bus publikuotas automatiškai.

> [!WARNING]
> Iš anksto nustatyti maketai gali būti nurodyti keliuose puslapiuose. Kai publikuosite iš anksto nustatytą maketą, atkreipkite dėmesį, kad tai gali turėti įtakos kelių puslapių maketui.

## <a name="rename-a-preset-layout"></a>Pervardykite iš anksto nustatytą išdėstymą

Norėdami pervardyti iš anksto nustatytą išdėstymą svetainių kūrimo priemonėje, atlikite šiuos veiksmus.

1. Kairiojoje naršymo srityje pasirinkite **Maketai**.
1. Pasirinkite maketo, kurį norite pervardyti, išdėstymo pavadinimą.
1. Pasirinkite **Redaguoti** norėdami pradėti redaguoti išdėstymą.
1. Išdėstymo ypatybių srityje pasirinkite rašiklio simbolį šalia maketo pavadinimo.
1. Jei reikia, redaguokite išdėstymo pavadinimą.
1. Pažymėkite varnelę, kad patvirtintumėte pavadinimo pakeitimą.
1. Pasirinkite **Baigti redagavimą**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Šablonų ir maketų apžvalga](templates-layouts-overview.md)

[Darbas su šablonais](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
