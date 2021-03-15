---
title: Darbas su šablonais
description: Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“dirbti su šablonais.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f4ed3b6797127113450949aa957437125f37394f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995721"
---
# <a name="work-with-templates"></a>Darbas su šablonais


[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip programoje „Microsoft Dynamics 365 Commerce“dirbti su šablonais.

## <a name="overview"></a>Peržiūrėti

Kaip buvo aptarta [šablonų ir maketų apžvalgoje](templates-layouts-overview.md), šablonai apibrėžia parinkčių rinkinį, pasiekiamą tolesniems autoriams. Šablonai yra naudingi įmonės kūrimo žiniatinklyje komandai dėl kelių priežasčių, o gerai struktūriškai apibrėžti šablonai gali būti naudingi siekiant visų šių tikslų:

- Supaprastinkite kasdienių turinio rengyklės vaidmenų kūrimo patirtį.

    - Filtruokite modulio parinktis, kad būtų rodomi tik tam tikro puslapio skyriaus atitinkami moduliai. (Pvz., šablono rinkodaros sekciją galima konfigūruot, kad filtruotų nereikšmingus modulius, kurie neturėtų būti naudojami tame kontekste ir kurie tik apsunkintų turinio kūrimo užduotis, jei jos rodomos.)
    - Sukonfigūruokite numatytąjį modulio parametrą, kad kūrimas būtų efektyvesnis.
    - Nustatykite numatytuosius puslapio fragmentus, siekdami pagerinti kūrimo efektyvumą. (Pvz., šablono antraštės ir poraštės fragmentai bus automatiškai rodomi kiekviename paskesniame puslapyje.)

- Išlaikykite savo įmonės įvaizdžio vientisumą svetainėse, nustatydami patvirtintą modulio išdėstymo ir konfigūracijos parinkčių rinkinį.

    > [!TIP] 
    > Sėkmingos el. prekybos svetainės teikia klientams žinomus, pakartojamus ir atitinkančius įmonės įvaizdį vartotojo patirties (UX) dizaino modelius. Naudodami šablonus užtikrinsite vientisumą savo svetainėje.

- Pagerinkite ieškos modulio optimizavimo (SEO) rezultatus, užtikrindami pakartojamus ir programiškai apibrėžtus puslapių aprašus ir metaduomenis.

> [!NOTE]
> Nors šablonai yra sukurti, kad būtų galima valdyti vientisumą svetainėje, jie teoriškai gali būti sukonfigūruoti taip, kad nereikalautų vientisumo. Prekės ženklo ir svetainės administratoriai gali nustatyti bet kokį savo svetainės puslapių kintamumo lygį. Pavyzdžiui, šabloną galima palikti visiškai atidarytą, kad turinio autoriai galėtų sukurti bet kurį pasirinktą puslapio dizainą. Šiuo atveju ankstesniame sąraše aprašytos funkcijos nėra taikomos.

## <a name="modify-a-template"></a>Šablono modifikavimas

Šablonai modifikuojami naudojant šablonų rengyklę.

Norėdami atidaryti šablonų rengyklę, atlikite vieną iš šių veiksmų:

- Savo svetainės naršymo srityje pasirinkite **Šablonai** ir pasirinkite šabloną, kurį norite modifikuoti.
- Esamo puslapio puslapių rengyklėje pasirinkite viršutinį mazgą kairiajame struktūros medyje. Tada, dešiniojoje ypatybių srityje pasirinkite **Redaguoti šabloną**.

Kairėje esančiame struktūros medžio rodinyje rodomos modulio parinktys ir struktūros, kurias galima naudoti antriniams maketams ir puslapiams. Kai struktūros medyje pasirenkate modulį, dešinėje pusėje esančioje ypatybių srityje galite peržiūrėti pasirinkto modulio šablono ypatybes. Kai kurios iš šių ypatybių yra pasiekiamos tik redaguojant šabloną. Pateiktoje lentelėje aprašomos šios ypatybės.

| Ypatybės pavadinimas | Aprašymas |
|---|---|
| Min. pasikartojimų skaičius | Ši ypatybė apibrėžia minimalų pasirinkto modulio pasikartojimų skaičių. Pavyzdžiui, jei vertė nustatyta kaip **1**, modulis reikalingas tolesniems autoriams, o jei vertė nustatyta kaip **0** (nulis), modulis yra pasirinktinis. |
| Maks. pasikartojimų skaičius | Ši ypatybė apibrėžia maksimalų pasirinkto modulio pasikartojimų skaičių. Pavyzdžiui, jei vertė nustatyta kaip **1**, modulis gali būti pridėtas tik vieną kartą. |
| Min. modulių (konteinerių) skaičius | Moduliuose, kuriuose yra kitų modulių (t. y. *konteinerių modulių*), ši ypatybė nurodo mažiausią visų modulių, kuriuos reikia įtraukti į antrinius modulius, skaičių. Pvz., naudojant karuselės modulį, vertė gali būti nustatyta kaip skaičius, kuris yra didesnis nei 1. |
| Maks. modulių (konteinerių) skaičius | Konteinerių moduliuose ši ypatybė nurodo maksimalų visų modulių, kuriuos reikia įtraukti kaip antrinius modulius, skaičių. Pvz., naudojant karuselės modulį, vertė gali būti nustatyta kaip skaičius, kuris yra mažesnis nei 10. |
| Užblokuota | Bulio logikos valdiklis **Užblokuota** atsiranda šalia visų pagrindinių modulio ypatybių. Juo šablono autorius gali užblokuoti modulio parametrus šablone. Užblokuoto modulio parametro negalima perrašyti naudojant bet kuriuos antrinius maketus arba puslapius. Jis tampa centralizuotai redaguotina visų maketų ir puslapių, kuriuose naudojamas šis šablonas, ypatybė. |

## <a name="create-a-new-template"></a>Sukurkite naują šabloną

Norėdami sukurti naują šabloną, atlikite toliau nurodytus veiksmus.

1. Savo svetainės naršymo srityje pasirinkite **Šablonai**, kad atidarytumėte šablono inspektoriaus rodinį.
1. Pasirinkti **Naujas šablonas**.
1. Šablono kūrimo dialogo lange įveskite šablono pavadinimą ir aprašą. Vertės, kurias įvedate, bus rodomos autoriams kuriant naujus puslapius. Todėl įveskite metaduomenis, kurie bus naudingi puslapio autoriams. Pavyzdžiui, įveskite **Naudoti šabloną kurti bendruosius rinkodaros puslapius** kaip aprašą. Šiuos metaduomenis galima redaguoti vėliau.
1. Pasirinkite **Gerai**, kad sukurtumėte naują šabloną ir atidarytumėte šablonų rengyklę. Šablonų rengyklės kairėje rodomas struktūros medis, o dešinėje – ypatybių sritis.
1. Struktūros medyje išplėskite mazgus ir pasirinkite atkarpą **HTML antraštė**.
1. Jei šioje atkarpoje dar nėra modulių, pasirinkite daugtaškio mygtuką (**...**) ir pasirinkite **Įtraukti modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite **Numatytojo puslapio suvestinė** ir pasirinkite **Gerai**.
1. Struktūros medyje pasirinkite naują modulį, o tada ypatybių srityje įveskite visus numatytuosius parametrus, kurie turi būti automatiškai sukonfigūruoti visiems antriniams šablono puslapiams. Jei nenorite jokių numatytųjų parametrų, palikite vertes tuščias.
1. Struktūros medyje pasirinkite atkarpą **Pagrindinė dalis**, pasirinkite daugtaškio mygtuką (...), tada – **Įtraukti modulį**.
1. Pasirinkite puslapio konteinerio modulį (gali būti tik vienas pasirinkimas), tada pasirinkite **Gerai**.

Naujo puslapio konteinerio modulyje matysite naują atkarpų rinkinį **(Antraštė**, **Pagrindinis** ir t. t.). Čia galite pridėti ir konfigūruoti modulio parinktis, kurios bus prieinamos autoriams kuriant šio šablono puslapius. Numatyta, kad, jei į atkarpą neįtrauksite jokių modulių, joje bus palaikomi visų galimų modulių tipai.

Šablonas dabar yra techniškai tinkamas ir jį galima įrašyti, įrašyti ir atrakinti ir naudoti kuriant naujus puslapius. Tačiau kitos trys sekcijos apibūdina kitus numatytuosius parametrus, kuriuos galbūt pirmiau norėsite konfigūruoti.

## <a name="add-a-header-and-a-footer"></a>Antraštės ir poraštės įtraukimas

Jei jūsų svetainėje jau yra antraštės fragmentas, atlikite šiuos veiksmus, kad į šabloną įtrauktumėte antraštę ir poraštę.

1. Struktūros medyje išplėskite atkarpą **Pagrindinė dalis** ir jos antrinį puslapio modulį.
1. Pasirinkite atkarpą **Antraštė**.
1. Pasirinkite atkarpos **Antraštė** daugtaškio mygtuką, tada – **Įtraukti fragmentą**.
1. Ieškokokite savo svetainės antraštės fragmento ir jį pasirinkti, tada pasirinkite **Gerai**.

Visi puslapiai, naudojantys šabloną, dabar automatiškai paveldės šį antraštės fragmentą.

Jei jūsų svetainėje dar nėra antraštės fragmento, žr. temoje [Fragmento kūrimas](work-with-fragments.md#create-a-fragment) dėl informacijos apie tai, kaip jį sukurti, o tada užbaikite ankstesnę procedūrą.

## <a name="change-the-template-theme"></a>Šablono temos keitimas

Norėdami nustatyti numatytąją temą visiems puslapiams, kurie naudoja šabloną, atlikite šiuos veiksmus.

1. Struktūros medyje kairėje išplėskite atkarpą **Pagrindinė dalis**.
1. Atkarpoje **Pagrindinė dalis** pasirinkite puslapio konteinerio modulį (pvz., **Numatytasis puslapis**).
1. Dešinėje ypatybės srityje, lauke **Tema** pasirinkite temą.

Pagal numatytuosius parametrus visuose naujuose puslapiuose dabar bus naudojama pažymėta tema. Norėdami, maketo ar puslapio lygiu neleisti puslapiams keisti šio parametro, nustatykite Bulio logikos valdiklį **Užblokuota** į **Teisinga**.

## <a name="add-a-script-to-a-template"></a>Scenarijaus įtraukimas į šabloną

Prie šablono galite pridėti HTML **&lt;scenarijaus&gt;** elementų, kuriuose yra „JavaScript“. Tokiu būdu galite pateikti numatytąjį scenarijaus veikimą HTML antraštės, pagrindinės dalies pradžios ir pagrindinės dalies pabaigos puslapių skyriams.

Norėdami įtraukti scenarijų į šabloną, atlikite toliau nurodytus veiksmus.

1. Kairėje esančiame struktūros medyje pasirinkite atkarpą, į kurią norite įtraukti **&lt;scenarijaus&gt;** elementą (pvz., HTML antraštę, pagrindinės dalies pradžią ar pagrindinės dalies pabaigą).
1. Pasirinkite prie atkarpos esantį daugtaškio mygtuką, tada – **Įtraukti modulį**.
1. Dialogo lange **įtraukti modulį** pasirinkite scenarijaus modulį (pvz., **Išorinis scenarijus** arba **Įdėtasis scenarijus**).
1. Dešiniojoje ypatybių sriyje, tinkamame scenarijaus ypatybių valdiklyje (pvz.,**Įdėtasis scenarijus** arba **Scenarijaus žymės**), įveskite savo scenarijų.
1. Ypatybių srityje įveskite kitus pasirinktinius parametrus, kuriuos norite konfigūruoti.

> [!TIP]
> Jei norite pakartotinai naudoti bet kuruos scenarijų modulius kituose šablonuose, galite juos konvertuoti į fragmentus. Tokiu būdu padedate kūrimo prodesą daryti efektyvesnį bei centralizuojate naujinimo procesą. Norėdami gauti informacijos apie tai, kaip konvertuoti scenarijaus modulį į fragmentą, žr. [Esamos modulio konfigūracijos įrašymas fragmentu](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).

## <a name="save-check-in-preview-and-publish-a-template"></a>Šablono įrašymas, įrašymas bei atrakinimas ir publikavimas

Norėdami įrašyti ir įrašyti bei atrakinti šabloną, atlikite šiuos veiksmus.

1. Šablono rengyklės viršuje pasirinkite **Įrašyti**. Įrašyti keitimai neturės įtakos tolesniems puslapiams, kol jie nebus įrašomi ir atrakinami.
1. Pasirinkite **Baigti redagavimą**. Dabar jūsų keitimai yra aptinkami atsiuntimo srauto darbo eigose.

Norėdami peržiūrėti keitimus atidarykite esamą puslapį, kuriame naudojamas išablonas, arba naudodami šabloną sukurkite naują puslapį.

Kai peržiūrėsite šablono keitimus, atlikite vieną iš toliau nurodytų veiksmų, kad šablonas būtų publikuojamas jūsų aktyvioje svetainėje.

* Eikite į **Šablonai**, pasirinkite šabloną, tada – **Publikuoti**.
* Norėdami atidaryti maketų rengyklę pasirinkite maketo pavadinimą, tada pasirinkite **Publikuoti**.
* Publikuokite puslapį, kuris nurodo nepublikuotą šabloną. Šablonas automatiškai publikuojamas.

> [!WARNING]
> Kai šablonas arba bet kuris kitas turinio valdymo sistemos (TVS) elementas publikuojamas, jis aptinkamas internete. Nepublikuokite dokumentų arba šaltinių, kol nebūsite pasirengę juos publikuoti. Dokumento versijos, kurios buvo įrašytos ir atrakintos, bet nebuvo publikuotos, yra matomos tik autentifikuotiems sistemos vartotojams.

## <a name="additional-resources"></a>Papildomi ištekliai

[Šablonų ir maketų apžvalga](templates-layouts-overview.md)

[Darbas su esamais maketais](work-with-layouts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]