---
title: Šablonų ir maketų apžvalga
description: Šiame straipsnyje aprašomas šablonai ir maketai Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/26/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 0664dd1ae06d09557cf8b8ec58baf6d27c1198bd
ms.sourcegitcommit: 023ae5557e1351a8329a59a41a551e8901db99a8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733390"
---
# <a name="templates-and-layouts-overview"></a>Šablonų ir maketų apžvalga


[!include [banner](includes/banner.md)]

Šablonai yra pagrindinis „Microsoft Dynamics 365 Commerce“ puslapio modelio elementas. Jei siekiate maksimaliai padidinti svetainių kūrimo darbo eigų efektyvumą ir nuoseklumą, svarbu išsiaiškinti, kaip pasinaudoti svetainės šablonų privalumais. Pirmieji sprendimai dėl šablono struktūros yra svarbūs ir gali smarkiai paveikti kasdienių, sezoninių ir visos svetainės prekės ženklų atnaujinimų savikainą ir lankstumą. Tinkamos struktūros šablonai turi ir kitų privalumų. Pavyzdžiui, jie padeda pagerinti visos svetainės ieškos modulio optimizavimo (SEO) rezultatus ir sumažinti trikčių skaičių.

Tinkamas būdas pradėti dirbti su šablonais – suprasti šablonų ir maketų funkcinius privalumus, šablonų ir maketų skirtumus bei hierarchiją.

Toliau pateiktoje iliustracijoje rodoma sugeneruoto tinklalapio puslapio modelio hierarchija.

![Puslapio modelio diagrama.](../commerce/media/page-model-diagram.png)

| Objektas        | Pagrindinė funkcija |
|---------------|----------------|
| Šablonas      | Šablonai apibrėžia modulio parinktis ir pagrindinius išdėstymo ir puslapio egzempliorių rinkinio pastolius. |
| Maketas        | Maketai apibrėžia galutinį puslapio ar puslapių rinkinio modulių pasirinkimą ir išdėstymą. |
| Puslapio egzempliorius | Puslapio egzemplioriai nustato konkrečių puslapių duomenis ir turinį. |

## <a name="templates"></a>Šablonai

Šablonai yra „Dynamics 365 Commerce“ puslapio modelio hierarchijos viršuje ir reiškia svarbų svetainės konfigūravimo ankstyvąjį žingsnį. Kalbant teoriškai, šablonai padeda kontroliuoti nuoseklumą antrinių maketų ir puslapių grupėje, nurodydami pagrindinės struktūros ir kūrimo parinktis tolesnio maketo kūrimui ir puslapio kūrimo darbo eigoms. Šablonai gali padėti supaprastinti turinio kūrimo procesą naudodami iš anksto apibrėžtus, centralizuotai valdomus elementus (pvz., antraštes ir poraštes) ir valdomus kūrimo srautus, padedančius užtikrinti, kad modulio konfigūracijos pasirinkimai atitinka prekės ženklą.

### <a name="controlling-consistency"></a>Nuoseklumo valdymas

Kai kuriate šabloną, svarbiausias verslo sprendimas, kurį turite atlikti – kiek šablonas gali valdyti puslapio kūrimo procesą. Šablonas, kuriame viskas prieinama tolesniam autoriui, yra lengviausiai sukuriamas šablono tipas, tačiau dėl jo gali kilti ilgalaikių pasekmių pagal šį šabloną sukurtų puslapių priežiūrai. Tinkamai parengtas šablonas teikia nurodymus ir supaprastintą kūrimo patirtį, bet taip pat suteikia autoriams pakankamo lankstumo, kad jie galėtų atlikti savo užduotis. Visi šie aspektai priklauso nuo kontrolės lygio, kurį priverstinai taiko šablonas.

Šablonai gali padėti turinio autoriams dirbti efektyviau ir atsižvelgti į prekių ženklą toliau nurodytais būdais.

- Ribodami modulius, kuriuos galima naudoti puslapyje.
- Siūlydami numatytąjį modulį ir konfigūracijos pasirinkimus.
- Tiesiogiai atlikti kai kuriuos modulio ir konfigūravimo pasirinkimus, kurie kontroliuojami šablono lygiu. Šis procesas dar vadinamas parametro *fiksavimu*.

Toliau pateiktame pavyzdyje parodyta, kaip gali būti sukonfigūruotas pagrindinis šablonas (šablonas X).

- Visi šablono X antriniai maketai turi turėti antraštės konteinerį, pagrindinės dalies konteinerį ir poraštės konteinerį.
- Šablone X antraštės konteinerio konfigūracija yra užrakinta ir gali būti keičiama tik pačiame šablone X. Visi antriniai maketai ir puslapiai visada turi šią antraštę.
- Pagrindinės dalies konteineriui reikalingas bent vienas modulis, o šiame konteineryje gali būti ne daugiau kaip dešimt modulių. Šiuos modulius apibrėžia tolesni maketai ir puslapiai.
- Pagrindinės dalies konteineryje galimi pagrindinės reklamos juostos, ypatybės, karuselės ir reklamos juostos moduliai.
- Šablone X poraštės konteineris sukonfigūruotas, bet jo galima nepaisyti naudojant tolesnius maketus ir puslapius.

Šiame pavyzdyje šablonas nustato paprastą struktūrą ir parinkčių rinkinį, skirtus tolesnio turinio autoriams. Atkreipkite dėmesį, kad kai kurios puslapio dalys (šiuo atveju antraštė) šablone yra išsamiai apibrėžtos ir užrakintos, todėl tolesni autoriai jų pakeisti negali. Kitas dalis (šiuo atveju pagrindinę dalį) gali nustatyti tolesni autoriai, laikydamiesi konkrečių nurodymų (šiuo atveju konkrečių tipų modulių mažiausias skaičius ir didžiausias skaičius). O kitos dalys (šiuo atveju poraštė) yra apibrėžtos šablone, tačiau tolesni autoriai gali jų nepaisyti.

Svarbus pradinis veiksmas, kurį turi atlikti svetainės ir prekių ženklo autoriai – nustatyti tinkamą antrinių maketų ir puslapių autorių apribojimų ir lankstumo pusiausvyrą. Naudojant šablonus ši pusiausvyra yra visiškai konfigūruojama. Ji turi įtakos tam, ar puslapio elementai atnaujinami centralizuotai (užrakinti šablone), ar paliekami pagal atskirus antrinius lygius, kurie puslapio hierarchijoje yra žemesni.

### <a name="relationship-between-template-defaults-and-page-content"></a>Ryšys tarp numatytųjų šablono nustatymų ir puslapio turinio

Pirminė šablono funkcija yra supaprastinti modulio kūrimo patirtį kuriant puslapį. Net jei šablone nustatyti arba net užblokuoti numatytieji modulio numatytieji nustatymai, daugiau nėra duomenų ryšio tarp puslapio modulio konfigūracijų ir šablono numatytųjų parametrų, išskyrus atvejus, kai puslapis redaguojamas. Šablonai kontroliuoja puslapio struktūros kūrimo patirtį, o sukūrus puslapį, šablono numatytieji parametrai nebeturi būti susieti su šiame puslapyje esamu lokalizuojamu turiniu. Kitaip tariant, modulio numatytosios funkcijos, nustatytos šablono valdiklio, leidžiančios kurti antrinius puslapius. Jie nekontroliuoja tų puslapių turinio po to, kai puslapiai sukuriami ir redaguojami.

Vienintelė anksčiau aprašyto veikimo būdo išimtis įvyksta, kai [į šabloną įtraukiamas fragmentas](work-with-fragments.md). Fragmentai gali būti naudojami dinamiškai pridėti ar redaguoti lokalizuojamą turinį visuose antriniuose šablono ar maketo puslapiuose bet kuriuo metu, net po to, kai iš davimo šablono sukurta daug puslapių. Geriausia šablonuose ir maketuose naudoti fragmentus, kai lokalizuojamas turinys turėtų būti dinamiškai pridedamas, pašalinamas arba redaguojamas visuose antriniuose puslapiuose. Pavyzdžiui, fragmentai turi būti naudojami antraštėms, poraštėms, bendrims metaduomenims ar scenarijams, ar bet kokiam kitam turiniui, kuris turi būti centralizuotai redaguojamas ir toks pat visuose antriniuose puslapiuose. Fragmentai suteikia būdą, kaip naudoti šablonus ir maketus, kad būtų galima valdyti visų antrinių puslapių turinį.

Norėdami pradėti naudoti šablonus, žr. [Darbą su šablonais](work-with-templates.md).

## <a name="layouts"></a>Maketai

Maketai yra kitas puslapio modelio hierarchijos lygis, einantis po šablonų. Šablonas apibrėžia visus puslapyje leidžiamus modulius, o maketas yra aiškus modulių pasirinkimas ir išdėstymas. Puslapiai yra kitas puslapio modelio hierarchijos lygis, einantis po maketų. Jie apibrėžia modelyje pasirinktų modulių lokalizuotą turinį.

Toliau pateiktame pavyzdyje naudojamas šablono pavyzdys iš ankstesnio skyriaus ir rodoma, kaip galima sukonfigūruoti pagrindinį maketą.

- Pirminiam maketo šablonui reikia, kad pagrindinės dalies konteineryje būtų nuo vieno iki dešimties modulių. Šie moduliai gali būti tik pagrindinės reklamos juostos, ypatybės, karuselės ir reklamos juostos moduliai. Todėl maketas gali apibrėžti toliau nurodytą modulių pasirinkimą ir išdėstymą.

    - Pirmas pagrindinės dalies konteinerio modulis yra reklamos juostos modulis, o po jo eina pagrindinės reklamos juostos modulis ir du ypatybių moduliai.
    - Pirmasis ypatybės modulis yra sulygiuotas kairėje, o antrasis ypatybės modulis yra sulygiuotas dešinėje.

- Nors numatytoji poraštė yra paveldėta iš pirminio šablono, šablono autorius poraštę paliko atrakintą. Todėl maketas gali jo nepaisyti apibrėždamas kitokį antraštės fragmentą.

Šiame pavyzdyje maketas apibrėžia galutinį antrinių puslapių modulių išdėstymą. Kaip ir šablonas, maketas gali apibrėžti numatytąsias arba užrakintas modulio ypatybes (pvz., ypatybių modulių lygiuotę), kurias antriniai puslapiai visada paveldės. Tada kiekvieno maketo modulio faktinis turinys arba duomenys apibrėžiami toliau hierarchijoje, kiekviename antrinio puslapio egzemplioriuje. Šiuo atveju svarbus skirtumas yra tas, kad maketuose tiesiogiai nėra lokalizuojamo turinio, o jų antriniuose puslapiuose tokio turinio yra. Pagrindinė maketo funkcija yra nustatyti jo antrinių puslapių modulių galutinį išdėstymą ir numatytąją konfigūraciją.

Ši hierarchija yra galinga dėl dviejų priežasčių. Pirma, maketai, kuriuose naudojamas tas pats pirminis šablonas, laikomi tinkamais maketo perjungimo scenarijams. Todėl bet kurio puslapio maketą galima pakeisti į kitą maketą iš tos pačios šablono hierarchijos, nereikalaujant, kad puslapio lygio turinys būtų sukurtas iš naujo. Galite pasinaudoti šia galimybe, norėdami atlikti sezoninius dizaino atnaujinimus, eksperimentuoti, arba atlikti nuolatinę svetaines pertvarką. Antra, maketai yra kitas būdas centralizuotai modifikuoti puslapių grupės bendrai naudojamus elementus, nereikalaujant atnaujinti atskirų puslapių. Pavyzdžiui, jei produkto kategorijoje yra 1 000 puslapių, kuriuose naudojamas tas pats maketas, modulius makete galima pertvarkyti, ir šis pakeitimas bus iš karto matomas visame 1 000 antrinių puslapių.

Suprasdami šią hierarchiją galite sukurti lanksčią ir efektyvią svetainės struktūrą, kuri padeda sumažinti savikainą, yra keičiamo dydžio ir užtikrina geresnius rezultatus, kai bėgant laikui svetainė vystoma.

### <a name="preset-and-custom-layouts"></a>Iš anksto nustatyti ir pasirinktiniai maketai

Svetainės maketai gali būti *iš anksto nustatyti* arba *pasirinktiniai*.

- **Iš anksto nustatyti maketai** leidžia naudoti puslapio kūrimo darbo eigą, kurioje visi moduliai jau yra pasirinkti ir išdėstyti, o reikia tik įvesti duomenis. Šis būdas gali padėti sutaupyti laiko, kai reikia sukurti daug puslapių, kuriems taikomi tie patys maketo reikalavimai. Iš anksto nustatyti maketai su savo antriniais puslapiais turi ryšį vienas su daugeliu. Todėl galima naudoti vieną iš anksto nustatytą maketą, kad būtų centralizuotai valdomas šimtų ar tūkstančių antrinių puslapių modulių išdėstymas.
- **Pasirinktiniai maketai** iš esmės yra vienkartinio naudojimo maketai, įdedami į vieną puslapį. Jie nerodomi kaip parinktis kuriant kitus naujus puslapius arba maketo perjungimo scenarijuose. Šio būdo privalumas yra tai, kad autorius gali eksperimentuoti kurdamas puslapį, kuriame naudojamas pasirinktinis modelis. Tada, jei autorius nori pakartotinai naudoti maketą kituose puslapiuose, jį galima lengvai konvertuoti į iš anksto nustatytą maketą. Tada naujas iš anksto nustatytas maketas bus rodomas kaip parinktis tos pačios šablonų hierarchijos puslapių puslapio kūrimo darbo eigose ir maketo perjungimo scenarijuose. Atvirkščiai, iš anksto nustatytus maketus galima išskirti į pasirinktinius maketus. Taip autorius puslapį gali atskirti nuo iš anksto nustatyto maketo ir sukurti naują vienkartinio naudojimo pasirinktinį maketą. (Šiam naujam pasirinktiniam maketui vis tiek taikomi bet kokie pirminio šablono apribojimai.)

Iš anksto nustatytas maketas ir pasirinktiniai maketai redaguojami skirtingose kūrimo įrankių rinkinio dalyse. Kadangi pasirinktiniai maketai neturi priklausomybių kituose puslapiuose, jie redaguojami tiesiogiai puslapio rengyklėje. Tokiu atveju maketo buvimas yra dažniausiai permatomas vartotojui ir rodomas tik puslapio lygio ypatybėse ir maketo parinkčių veiksmuose. Tačiau, kadangi iš anksto nustatytų maketų pakeitimai gali turėti įtakos daugybei antrinių puslapių, jie turi būti redaguojami maketo rengyklėje, kurioje publikavimo veiksmais įvertinamas visas tolesnis poveikis antriniams puslapiams.

Šioje iliustracijoje pateikiami iš anksto nustatytų ir pasirinktinių maketų scenarijai.

![Iš anksto nustatytų ir pasirinktinių maketų scenarijai.](../commerce/media/template-figure1.png)

Norėdami pradėti naudoti iš anksto nustatytus maketus, žr. [Darbas su iš anksto nustatytais maketais](work-with-layouts.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Darbas su šablonais](work-with-templates.md)

[Darbas su esamais maketais](work-with-layouts.md)

[Darbas su publikavimo grupėmis](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
