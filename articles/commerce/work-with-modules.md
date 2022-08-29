---
title: Darbas su moduliais
description: Šiame straipsnyje aprašoma, kaip ir kada naudoti modulius dalyje Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 91188590391501042ff0503bdc3592435c30fa63
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291952"
---
# <a name="work-with-modules"></a>Darbas su moduliais

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip ir kada naudoti modulius dalyje Microsoft Dynamics 365 Commerce.

Moduliai yra loginiai kūrimo blokai, kurie sudaro puslapio struktūrą, o jų paskirtis ir taikymo sritys yra įvairios. Kai kurie moduliai yra aukšto lygio konteineriai, o jų vienintelė paskirtis – laikyti ir organizuoti kitus modulius (antrinius modulius). Kitų modulių, pvz., paprasto vaizdų išdėstymo modulio, paskirtis yra labai konkreti. Kiti moduliai, pvz., karuselės modulis, patenka tarp šių dviejų kategorijų.

Pagal numatytuosius nustatymus jūsų „Dynamics 365 Commerce“ svetainėje yra modulių biblioteka, kuri leidžia įgyvendinti pagrindinius el. prekybos scenarijus. Tiesiog naudodami šiuos modulius greičiausiai galėsite sukurti visapusišką el. prekybos svetainę. Tačiau galbūt norėsite šiuos modulius tinkinti arba kurti naujus pasirinktinius modulius konkretiems poreikiams. Jei norite kurti pasirinktinius modulius, galite naudoti modulių kūrimo programinės įrangos kūrimo rinkinį (SDK), kuris padės sukurti pasirinktinių modulių biblioteką.

## <a name="container-modules-and-slots"></a>Konteinerio moduliai ir vietos

Kaip minėta anksčiau, kai kurie moduliai yra skirti laikyti antrinius modulius. Šie moduliai vadinami *konteineriais* ir leidžia naudoti įdėtųjų modulių hierarchijas. Konteinerio moduliai apima *vietas*. Vietos naudojamos antrinių modulių maketui ir paskirčiai konteineryje tvarkyti. Pavyzdys – pagrindinis puslapio konteinerio modulis (bet kurio puslapio aukščiausio lygio modulis), kuriame nustatytos kelios svarbios vietos.

- Antraštės vieta
- Papildomos antraštės vieta
- Pagrindinė vieta
- Poraštės vieta
- Papildomos poraštės vieta

Modulio kūrėjas apibrėžia šias vietas ir nustato, kuriuos antrinius modulius ir kiek antrinių modulių galima tiesiogiai įdėti jų viduje. Pavyzdžiui, antraštės vieta gali palaikyti tik vieną tipo **Antraštės modulis** modulį, o pagrindinės dalies vieta gali palaikyti neribotą skaičių bet kokio tipo modulių (išskyrus kitus puslapio konteinerio modulius).

Naudodami kūrimo įrankius puslapių autoriai neprivalo iš anksto žinoti, kuriuos modulius galima įdėti į kiekvieną vietą arba kurių modulių įdėti negalima. Kai puslapių autoriai pasirenka vietą ir bando pasirinkti modulį, kurį nori į šią vietą įtraukti, jie matys modulio tipų, kurie toje vietoje palaikomi, filtruotą rodinį.

## <a name="content-modules"></a>Turinio moduliai

Turinio moduliuose yra turinio ir medijos elementų, pvz., teksto (pvz., antraščių, pastraipų ir saitų) arba turto nuorodų (pavyzdžiui, vaizdų, vaizdo įrašų ir PDF failų). Įprasto turinio modulio tipai apima turinio bloką, teksto bloką ir skatinančios reklamjuostės modulius. Šių trijų tipų moduliuose gali būti teksto arba medijos, ir jiems nereikia jokių antrinių modulių, kad kokią nors informaciją būtų galima padaryti matoma puslapyje.

Dauguma įprastų, kasdienių puslapių ir turinio kūrimo užduočių apima turinio modulius, visų pirma todėl, kad šie moduliai apibrėžia faktinį turinį, kuris generuojamas jų pirminio konteinerio moduliuose. Yra daug turinio modulių ir jie paprastai yra paskutinės dalys, kurias įtrauksite į puslapio įdėtųjų modulių hierarchiją.

Toliau pateiktoje iliustracijoje parodyta, kaip moduliai yra įdėti į pirminio konteinerio modulio vietas.

![Modulių įdėjimas.](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Modulių įtraukimas arba pašalinimas

Tolesnėse procedūrose aprašoma, kaip įtraukti modulių arba juos pašalinti.

### <a name="add-a-module"></a>Modulio įtraukimas

Norėdami modulį įtraukti į vietą arba konteinerį puslapyje, atlikite šiuos veiksmus.

1. Išorinėje juostoje kairėje arba tiesiai pagrindinėje drobėje pasirinkite talpyklą ar vietą, į kurią galima įtraukti vaiko modulį.

    > [!NOTE]
    > Modulių dizaino įrankyje nustatytas modulių, kuriuos galima įtraukti į konkrečią modulio vietą, tipų sąrašas. Šablono autoriai tuomet gali išdirbti leidžiamas modulio parinktis tam, kad padėtų užtikrinti nuoseklų ieškos variklio optimizavimą (SEO) ir leidžiamą efektyvumą puslapiams, kurie yra sukurti pagal specialų šabloną. Įtraukdami modulį į vietą,**Modulio įtraukimas** teksto laukelis automatiškai filtruojamas taip, kad rodytų tik pasirinktoje talpykloje ar vietoje palaikomus modulius. Šis leidžiamų modulių sąrašas yra sudaromas puslapio šablone arba talpyklos modulio apraše.

1. Jei naudojate išorės juostą, pasirinkite elipsę (**...**) šalia modulio pavadinimo ir tuomet pasirinkite **Įtraukti modulį**. Jei naudojate valdiklius tiesiogiai drobėje, pasirinkite pliuso simbolį (**+**) tuščioje vietoje ar šalia prie šiuo metu pasirinkto modulio ir tuomet pasirinkite **Įtraukti modulį**.

    > [!NOTE]
    > Jei konteineris arba vieta nepalaiko naujų antrinių modulių, parinktis **Įtraukti modulį** nepasiekiama.

1. **Įtraukti modulį** teksto laukelyje pasirinkite modulį įtraukimui į jūsų puslapį.

    > [!TIP]
    > **Turinio blokavimas** yra geras modulio tipas pradedantiems su juo dirbti.

1. Pasirinkite **Gerai**, kad pasirinktą modulį įtrauktumėte į pasirinktą konteinerį arba vietą jūsų puslapyje.

### <a name="remove-a-module"></a>Modulio šalinimas

Norėdami modulį pašalinti iš vietos arba konteinerio puslapyje, atlikite šiuos veiksmus.

1. Išorinėje kairinėje juostoje pasirinkite elipsę (**...**) šalia šalinamo modulio pavadinimo ir tuomet pasirinkite šiukšlių dėžės simbolį. Kitu atveju, pagrindinėje drobėje galite pasirinkti fragmentą šiukšlių dėžės simbolį pasirinkto modulio įrankių juostoje.
1. Kai esate paskatinti patvirtinti, ar norite pašalinti modulį, pasirinkite **Gerai**.

## <a name="move-a-module-to-a-new-position"></a>Perkelkite modulį į naują padėtį

Modulio perkėlimui į naują padėtį puslapyje, naudokite bet kurį iš tolesnių metodų.

### <a name="move-a-module-using-the-outline-pane"></a>Perkelkite modulį naudodami išorės juostą

Modulio perkėlimui naudojant išorės juostą, atlikite šiuos žingsnius.

1. Pasirinkite ir laikykite norimą perkelti modulį išorės juostoje, tada tempkite modulį į naują padėtį išorėje. Mėlyna linija išorėje ir drobėje rodo, kur modulis gali būti padėtas.
1. Atleiskite modulį jo numetimui į naują vietą.

### <a name="move-a-module-directly-within-the-canvas"></a>Kelkite modulį tiesiai drobėje

Modulio perkėlimui tiesiai drobėje, atlikite šiuos žingsnius.

1. Pasirinkite modulį, kurį norite kelti drobėje. 
1. Pasirinkite vieną iš į viršų ar apačią rodančių rodyklių simbolių modulio įrankių juostoje ir tuomet tempkite rodyklę į naują padėtį puslapyje. Mėlyna linija išorėje ir drobėje rodo, kur modulis gali būti padėtas. Jei modulis negali būti judinamas aukštyn ar žemyn, rodyklės simbolis bus papilkėjęs. 
1. Atleiskite modulį jo numetimui į naują vietą.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Perkelkite modulį naudodami elipsės meniu

Modulio perkėlimui naudojant elipsės meniu, atlikite šiuos žingsnius.

1. Pasirinkite modulį išorėje ar drobėje.
1. Pasirinkite elipsę (**...**) šalia modulio pavadinimo išorės juostoje arba modulio įrankių juostoje drobėje.
1. Jei modulis gali būti judinamas aukštyn ar žemyne konteineryje ar vietoje, matysime parinktis **Judinti aukštyn** ar **Judinti žemyn**. Pasirinkite norimą judesio parinktį modulio judinimui aukštyn ar žemyn pagal jo gimines.

## <a name="configure-modules"></a>Modulių konfigūravimas

Tolesnėse procedūrose aprašoma, kaip konfigūruoti turinio ir konteinerio modulius.

### <a name="configure-a-content-module"></a>Turinio modulio konfigūravimas

Norėdami konfigūruoti turinio modulį puslapyje, atlikite šiuos veiksmus.

1. Išorės juostoje kairėje, išplėskite medį ir pasirinkite bet kurį turinio modulį (pavyzdžiui, **Turinio blokavimą**). Kitu atveju, galite pasirinkti modulį pagrindinėje drobėje.
1. Modulio parametrų juostoje dešinėje, įveskite parametrus bet kuriems norimo modulio valdikliams.
1. Komandų juostoje, pasirinkite **Įrašyti**. Tai padarius, taip pat bus atnaujinta peržiūros drobė.

### <a name="edit-module-text-properties"></a>Redaguokite modulio teksto parametrus

Tik skaitymui neskirti modulio teksto parametrai gali būti tiesiai redaguojami drobėje.

Modulio teksto parametrų redagavimui, atlikite tolesnius veiksmus.

1. Pasirinkite teksto valdiklį drobėje, tuomet padėkite savo rodyklę ten, kur norite redaguoti tekstą.
1. Įveskite teksto turinį.
1. Pasirinkite bet kur už teksto turinio ribų tam, kad tęstumėte kito turinio redagavimą.

### <a name="inline-image-selection"></a>Eilutės paveikslėlio pasirinkimas

Tik skaitymui neskirti modulio paveikslėliai parametrai gali būti tiesiai keičiami drobėje.

Tam, kad pasirinktumėte naują modulio turinio paveikslėlį, atlikite šiuos žingsnius.

1. Dukart spustelėję drobėje ant paveikslėlio. Tai atidarys medijos pasirinkimo langą.
1. Suraskite ir pasirinkite naują jūsų norimą naudoti paveikslėlį ir tuomet pasirinkite **Gerai**. Naujas paveikslėlis dabar bus rodomas drobėje.

### <a name="configure-a-container-module"></a>Konteinerio modulio konfigūravimas

Norėdami konfigūruoti konteinerio modulį puslapyje, atlikite šiuos veiksmus.

1. Savo puslapyje pasirinkite konteinerio modulį (pavyzdžiui, karuselės arba nepastovaus konteinerio modulį).
1. Ypatybių srityje dešinėje išplėskite įdėtuosius valdiklius pasirinkdami antraštes, tada nustatykite bet kokias reikiamas valdiklių reikšmes.
1. Struktūros srityje kairėje šalia konteinerio arba bet kokių konteineryje esančių vietų pavadinimo pasirinkite daugtaškio mygtuką, tada pasirinkite **Įtraukti modulį**. Tada į pasirinktą konteinerį įtraukite antrinių modulių. Norėdami gauti daugiau informacijos, žr. anksčiau [šiame straipsnyje skyriuje](#add-a-module) Darbas su moduliais.
1. Jei pirminiame konteineryje yra keli tos pačios kilmės antriniai moduliai, galite pakeisti jų rodymo pirminiame konteineryje tvarką. Pasirinkite modulio daugtaškio mygtuką, tada naudokite rodyklės aukštyn arba rodyklės žemyn mygtukus.

## <a name="additional-resources"></a>Papildomi ištekliai

[Šablonų ir maketų apžvalga](templates-layouts-overview.md)

[Darbas su šablonais](work-with-templates.md)

[Darbas su esamais maketais](work-with-layouts.md)

[Darbas su fragmentais](work-with-fragments.md)

[Konteinerio modulio įtraukimas į puslapį](add-container-module.md)

[Darbas su publikavimo grupėmis](publish-groups.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
