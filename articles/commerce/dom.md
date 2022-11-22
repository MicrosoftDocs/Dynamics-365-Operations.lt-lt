---
title: Paskirstytų užsakymų tvarkymas (DOM)
description: Šiame straipsnyje aprašoma „Dynamics 365 Commerce“ paskirstytų užsakymų tvarkymo (DOM) funkcija.
author: josaw1
ms.date: 02/08/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a18441c44869e0e95cf79e35045dd7eacca7e43d
ms.sourcegitcommit: 4f987aad3ff65fe021057ac9d7d6922fb74f980e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/14/2022
ms.locfileid: "9764186"
---
# <a name="distributed-order-management-dom"></a>Paskirstytų užsakymų tvarkymas (DOM)

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma „Microsoft Dynamics 365 Commerce“ paskirstytų užsakymų tvarkymo (DOM) funkcija.

DOM yra daugiakanalių užsakymų įvykdymo optimizavimo sprendimas, padedantis maksimaliai padidinti užsakymų įvykdymą tiekimo grandinės tinkle. DOM padeda užtikrinti, kad produktai klientams bus pristatyti tinkamais kiekiais, iš reikiamų šaltinių ir tinkamu laiku. DOM taip pat gali padėti maksimaliai padidinti pelną, sumažinti išlaidas ir patenkinti aptarnavimo lygio reikalavimus.

DOM naudoja mišraus skaičių programavimo (MIP) ir numatymo analizės modelius, kad būtų galima optimizuoti paketų lygiu ir atskirų užsakymų lygių. Ši galimybė leidžia mažmenininkams naudoti nustatytas taisykles, siekiant suderinti daugelį nesuderinamų užsakymo vykdymo poreikių. Moderniame tiekimo tinkle, kuriame produkto įvykdymas gali būti įgyvendinamas keliais kanalais, organizacijos privalo greitai prisitaikyti prie užsakymų pakeitimų, tiekimo pasiekiamumo problemų ir poreikio pikų. DOM padeda maksimaliai padidinti užsakymų vykdymą ir rasti tinkamus produktų pristatymo šaltinius, atsižvelgiant į verslo apribojimus ir tikslus, pavyzdžiui, mažinant išlaidas įvykdant užsakymus iš artimiausių šaltinių. DOM naudoja atstumą tarp produkto įvykdymo šaltinių ir siuntimo paskirties vietų, išlaidų veiksnius, kurie apibrėžti kaip optimizavimo tikslai, ir taisykles, kurios apibrėžiamos kaip apribojimai, tokie kaip atsargos įvykdymo mazguose, siekiant optimizuoti užsakymų vykdymą. DOM leidžia apibrėžti kelis profilius, kurie įgalina įmones vykdyti skirtingas optimizavimo strategijas, atsižvelgiant į verslo arba vartotojo segmento tipą. 

Tolesnėje iliustracijoje rodomas pardavimo užsakymo ciklas DOM sistemoje.

![Pardavimo užsakymo ciklas DOM kontekste.](./media/flow.png "Pardavimo užsakymo ciklas DOM kontekste")

## <a name="set-up-dom"></a>Nustatyti DOM

1. Eikite į **Sistemos administravimas \> Sąranka \> Licencijos konfigūracija**.
2. Skirtuke **Konfigūracijos raktai** išplėskite mazgą **Prekyba** ir pažymėkite žymės langelį **Paskirstytų užsakymų tvarkymas**.
3. Eikite į **„Retail“ ir „Commerce“ \> Paskirstytų užsakymų tvarkymas \> Sąranka \> DOM parametrai**.
4. Skirtuke **Bendra** nustatykite tolesnes reikšmes.

    - **Įjungti paskirstytų užsakymų tvarkymą** – šią parinktį nustatykite kaip **Taip**.
    - **Patvirtinti „Bing“ žemėlapių naudojimą DOM sistemoje** – šią parinktį nustatykite kaip **Taip**.

        > [!NOTE]
        > Šią parinktį nustatyti kaip **Taip** galite, tik jei kaip **Taip** taip pat nustatyta puslapio **Bendrai naudojami prekybos parametrai** (**„Retail“ ir „Commerce“ \> Būstinės sąranka \> Parametrai \> Bendrai naudojami prekybos parametrai**) skirtuke **„Bing“ žemėlapiai** esanti parinktis **Įjungti „Bing“ žemėlapius** ir jei lauke **„Bing“ žemėlapių raktas** įvestas tinkamas raktas.
        >
        > [„Bing“ žemėlapių kūrimo centro](https://www.bingmapsportal.com/) portalas leidžia apriboti prieigą prie jūsų „Bing“ žemėlapių API raktų iki jūsų nustatytų domenų rinkinio. Naudodami šią funkciją klientai gali nustatyti griežtą reikšmių ar IP adresų diapazonų, pagal kuriuos bus tikrinamas raktas, rinkinį. Užklausos, esančios jūsų leidžiamųjų sąraše, bus apdorojamos įprastai, o užklausos ne iš jūsų sąrašo pateiks atsakymą apie draudžiamą prieigą. Domeno saugos įtraukimas į jūsų API raktą yra pasirinktinis, o palikti raktai veiks toliau. Rakto leidžiamų sąrašas yra nepriklausomas nuo visų kitų raktų, todėl įgalina kiekvienam raktui naudoti skirtingas taisykles. Paskirstytų užsakymų tvarkymas nepalaiko domene nurodytų ypatybių nustatymo.

    - **Saugojimo laikotarpis dienomis** – nurodykite, kiek laiko sistemoje laikomi DOM vykdymų metu generuojami įvykdymo planai. Paketinė užduotis **DOM įvykdymo duomenų naikinimo užduoties sąranka** panaikins visus įvykdymo planus, kurie yra senesni nei čia jūsų nurodytas dienų skaičius.
    - **Atmetimo laikotarpis (dienomis)** – nurodykite, kiek laiko turi praeiti, kol atmestą užsakymo eilutę bus galima priskirti tai pačiai vietai.

5. Skirtuke **Sprendimo priemonė** nustatykite tolesnes reikšmes.

    - **Didžiausias automatinio įvykdymo bandymų skaičius** – nurodykite, kiek kartų DOM mechanizmas bandys kokią nors užsakymo eilutę tarpininkaudamas perkelti į kokią nors vietą. Jei DOM mechanizmui kokios nors užsakymo eilutės tarpininkaujant perkelti į kokią nors vietą nepavyks nurodytą mėginimų kartų skaičių, jis užsakymo eilutę pažymės kaip išimtį. Tada būsimų vykdymų metu jis tą eilutę praleis, kol būsena nebus iš naujo nustatyta rankiniu būdu.
    - **Vietos parduotuvių regiono spindulys** – įveskite reikšmę. Šis laukas padeda nustatyti, kaip vietos yra grupuojamos ir laikomos vienodomis atstumo atžvilgiu. Pavyzdžiui, jei įvedate **100**, kiekviena parduotuvė ar platinimo centras, nuo įvykdymo adreso nutolę iki 100 mylių spinduliu, atstumo atžvilgiu laikomi vienodais.
    - **Sprendimo priemonės tipas** – pasirinkite reikšmę. Su prekyba yra išleistos dviejų tipų sprendimo priemonės: **gamybos sprendimo priemonė** ir **supaprastintoji sprendimo priemonė**. Visoms mašinoms, kuriose bus vykdoma DOM sistema (t. y., visiems serveriams, priklausantiems grupei DOMBatch), reikia parinkti **gamybos sprendimo priemonę**. Gamybos sprendimo priemonei reikia specialaus licencijos rakto, kuris pagal numatytuosius parametrus yra licencijuojamas ir įdiegiamas gamybos aplinkose. Naujesnėse 2 ir aukštesnės pakopos aplinkose gamybos sprendimų priemonė jau bus įgalinta. Ne gamybos aplinkose šį licencijos raktą reikia įdiegti rankiniu būdu. Norėdami rankiniu būdu įdiegti šį licencijos raktą, atlikite tolesnius veiksmus.

        1. „Microsoft Dynamics“ portale „Lifecycle Services“ atidarykite biblioteką Bendrai naudojamas turtas, kaip turto tipą pasirinkite **Modelis** ir atsisiųskite **DOM licencijos** failą.
        1. Paleiskite „Microsoft“ informacinių interneto paslaugų (IIS) tvarkytuvą, dešiniuoju pelės mygtuku spustelėkite **AOSService svetainė** ir pasirinkite **Naršyti**. Atidaromas „Windows Explorer“ langas su katalogu **\<AOS service root\>\\webroot**. Pasižymėkite \<AOS Service root\> kelią, nes jį naudosite atlikdami kitą veiksmą.
        1. Nukopijuokite kataloge **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\bin** esantį konfigūracijos failą.
        1. Eikite į būstinės klientą ir atidarykite puslapį **DOM parametrai**. Skirtuko **Sprendimo priemonė** lauke **Sprendimo priemonės tipas** pasirinkite **Gamybos sprendimo priemonė** ir įsitikinkite, kad nerodoma klaidų pranešimų.

        > [!NOTE]
        > Supaprastintoji sprendimo priemonė suteikiama tam, kad pardavėjai DOM funkciją galėtų išbandyti nediegdami specialios licencijos. Organizacijos supaprastintosios sprendimo priemonės neturėtų naudoti gamybos aplinkose.
        >
        > Gamybos sprendimo patobulina veikimą (ribojama, kiek užsakymų ir užsakymų eilučių galima apdoroti vieno vykdymo metu) ir rezultatų konvergavimą (kai kuriose situacijose naudojant tam tikrą užsakymų paketą galima gauti ne geriausią rezultatą). Taisyklei **Daliniai užsakymai** reikia gamybos sprendimo priemonės.

6. Grįžkite į **Mažmeninės prekybos ir prekybos \> Paskirstytų užsakymų tvarkymas \> Sąranka \> DOM parametrai**.
7. Skirtuke **Numeracijos** įvairiems DOM objektams priskirkite reikiamas numeracijas.

    > [!NOTE]
    > Kad objektams būtų galima priskirti numeracijas, jos turi būti apibrėžtos puslapyje **Numeracijos** (**Organizacijos administravimas \> Numeracijos \> Numeracijos**).

8. DOM funkcija palaiko galimybę apibrėžti įvairių tipų DOM taisykles, o organizacijos pagal savo verslo poreikius gali sukonfigūruoti keletą taisyklių. DOM taisykles galima apibrėžti vietų grupei arba atskiroms vietoms bei konkrečiai produktų kategorijai, konkrečiam produktui ar variantui. Norėdami sukurti vietų grupę, kurią reikia naudoti su DOM taisyklėmis, atlikite tolesnius veiksmus.

    1. Eikite į **„Retail“ ir „Commerce“ \> Kanalų sąranka \> Įvykdymo grupės**.
    2. Pasirinkite **Nauja** ir įveskite naujosios grupės pavadinimą bei aprašą.
    3. Pasirinkite **Įrašyti**.
    4. Norėdami į grupę įtraukti vieną vietą, pasirinkite **Įtraukti eilutę**. Jei norite įtraukti kelias vietas, pasirinkite **Įtraukti eilučių**.

    > [!NOTE]
    > „Commerce“ 10.0.12 ir naujesnėse versijose **Galimybė nurodyti vietas kaip „Siuntimas“ arba „Paėmimas“ įjungta įvykdymo grupėje** turi būti įjungta **funkcijų valdymo** darbo srityje.
    >
    > Šia funkcija įtraukiamos naujos konfigūracijos į **įvykdymo grupės** puslapį, kad galėtumėte nustatyti, ar sandėlis gali būti naudojamas siuntimui, ar sandėlis ir parduotuvė kartu gali būti naudojami siuntimui ir (arba) paėmimui. 
    >
    > Įjungus šia funkciją, bus atnaujintos vietos pasirinkimo parinktys, kai EKA kuriate paėmimo ar siuntimo užsakymus.
    >
    > Įjungus šią funkciją taip pat atnaujinami puslapiai EKA, kai pasirenkamos operacijos „siųsti viską“ arba „siųsti pasirinktus“.

9. Norėdami apibrėžti taisykles, eikite į **„Retail“ ir „Commerce“ \> Paskirstytų užsakymų tvarkymas \> Sąranka \> Tvarkyti taisykles**. Šiuo metu palaikomos tolesnės DOM taisyklės.

    - **Minimalių atsargų taisyklė** – šio tipo taisyklė organizacijoms leidžia kitu nei užsakymų įvykdymas tikslu „aptverti“ konkretų produkto kiekį. Pavyzdžiui, organizacijos gali norėti, kad DOM užsakymams įvykdyti pasiekiamomis laikytų ne visas parduotuvėje esančias atsargas. Jos gali norėti kažkiek atsargų rezervuoti į parduotuvę užeinantiems klientams. Kai naudojama šio tipo taisyklė, galite nustatyti minimalias norimas išlaikyti tam tikros produktų kategorijos, atskiro produkto ar produkto varianto vienoje vietoje ar vietų grupėje atsargas. Naudojant papildomų kategorijų hierarchiją, taip pat galima nurodyti minimalias atsargas. Jei produktas patenka į kelias kategorijas, papildomai kategorijai suteikiama didžiausia svarba visoms taisyklėms, kurioms galima naudoti kategorijas.
    - **Įvykdymo vietos prioriteto taisyklė** – šio tipo taisyklė organizacijoms leidžia nustatyti vietų hierarchiją ir prioritetą, į kurį atsižvelgia DOM mechanizmas, bandydamas nustatyti įvykdymo vietas konkretiems produktams. Tinkamas prioritetų intervalas yra nuo 1 iki 10 – 1 yra didžiausias prioritetas, o 10 – mažiausias. Į didesnio prioriteto vietas atsižvelgiama pirmiau nei į mažesnio prioriteto vietas. Jei taisyklė nustatoma kaip labai ribota, užsakymai tarpininkaujant perkeliami tik į tas vietas, kurioms nustatyti prioritetai. DOM teikia pirmenybę siuntimo užsakymams iš vienos vietos. Todėl jei visas užsakymas ir jo eilutės nepasiekiamos vietoje, kurios prioritetas 1, DOM bandys jį įvykdyti iš vietos, kurios prioritetas 2.
    - **Dalinių užsakymų taisyklė** – „Retail” 10.0.5 versijoje parametras **Užsakymą įvykdyti tik iš vienos vietos** buvo pakeistas į **Maksimalus įvykdymo vietų skaičius**. Senas parametras įgalintas vartotojams konfigūruoti, ar užsakymai gali būti įvykdomi tik iš vienos vietos, ar iš tiek vietų, kiek įmanoma. Naujas parametras leidžia vartotojams nurodyti, ar įvykdymas gali būti iš nustatyto vietų rinkinio (iki penkių) ar iš tiek vietų, kiek įmanoma. Visoms parinktims, išskyrus įvykdymą iš vienos vietos, DOM padalins eilutę, nes užsakymo apdorojami pagal eilutes. Ši taisyklė veikia tik su gamybos sprendimo priemone.
    - **Neprijungtos įvykdymo vietos taisyklė** – ši taisyklė organizacijoms leidžia tam tikrą vietą ar vietų grupę nurodyti kaip neprijungtą ar nepasiekiamą DOM sistemai, kad toms vietoms nebūtų galima priskirti užsakymų, kuriuos reikia įvykdyti.
    - **Didžiausio atmetimų skaičiaus taisyklė** – ši taisyklė organizacijoms leidžia nustatyti atmetimų ribą. Kai bus pasiekta ši riba, DOM doroklė užsakymą arba užsakymo eilutę pažymės kaip išimtį ir jų neįtrauks į kitą apdorojimo etapą. Siekiant užtikrinti našumą, DOM neatsižvelgs į visų atmetimų istoriją. 

        Tam tikrai vietai priskyrus užsakymo eilučių, ta vieta gali priskirtą užsakymo eilutę atmesti, nes dėl tam tikrų priežasčių ji gali tos eilutės negalėti įvykdyti. Atmestos eilutės yra pažymimos kaip išimtys ir grąžinamos į telkinį, kad būtų apdorojamos kito vykdymo metu. Kito vykdymo metu DOM atmestą eilutę bandys priskirti kitai vietai. Naujoji vieta taip pat gali atmesti priskirtą užsakymo eilutę. Toks priskyrimo ir atmetimo ciklas gali įvykti keletą kartų. Kai atmetimų skaičius pasieks nustatytą ribą, DOM užsakymo eilutę pažymės kaip nuolatinę išimtį ir jos nebeims priskirti. DOM tokią užsakymo eilutę iš naujo priskirti svarstys, tik jei vartotojas rankiniu būdu iš naujo nustatys užsakymo eilutės būseną.

    - **Didžiausio atstumo taisyklė** – ši taisyklė organizacijoms leidžia nustatyti didžiausią atstumą, kuriuo gali būti nutolusi vieta ar vietų grupė, iš kurios įvykdomas užsakymas. Jei vietai nustatomos persidengiančios didžiausio atstumo taisyklės, DOM taikys tai vietai nustatytą trumpiausią didžiausią atstumą.
    - **Didžiausio užsakymų skaičiaus taisyklė** – ši taisyklė organizacijoms leidžia nustatyti didžiausią užsakymų skaičių, kurį vieta ar vietų grupė gali apdoroti. Optimizavimo proceso metu sistema nagrinės užsakymus, kurie nebuvo išsiųsti iš tų vietų. Šis tikrinimas atliekamas visuose profiliuose. Todėl jei persidengia didžiausias užsakymų skaičius, nustatytas tos pačios vietos šablonuose, sistema išnagrinės didžiausią užsakymų skaičių, kuris nustatomas visuose šablonuose. 

    Toliau pateikiama keletas bendrų atributų, kuriuos galima nustatyti visų ankstesnių tipų taisyklėms.

    - **Pradžios data** ir **Pabaigos data** – šiuos laukus galima naudoti, kad būtų aktyvi kiekvienos taisyklės data.
    - **Išjungta** – DOM vykdymo metu svarstoma tik apie tas taisykles, kuriose šio lauko reikšmė yra **Ne**.
    - **Labai ribota** – taisyklę galima nustatyti kaip labai ribotą arba nelabai ribotą. Kiekvienas DOM vykdymas atliekamas du kartus. Pirmą kartą kiekviena taisyklė laikoma labai ribota taisykle, neatsižvelgiant į šio lauko parametrą. Kitaip tariant, pritaikoma kiekviena taisyklė. Vienintelė išimtis yra taisyklė **Vietos prioritetas**. Antrą kartą taisyklės, kurios nebuvo nustatytos kaip labai ribotos, yra pašalinamos ir vietoms priskiriamas tas užsakymas ar tos užsakymo eilutės, kurios nebuvo priskirtos vietoms pritaikius visas taisykles.

10. Naudojant įvykdymo profilius grupuojamas taisyklių, juridinių subjektų, pardavimo užsakymų kilmių ir pristatymo būdų rinkinys. Kiekvienas DOM vykdymas atliekamas konkrečiam įvykdymo profiliui. Taip organizacijos tam tikras taisykles gali nustatyti ir vykdyti tam tikriems juridiniams subjektams (užsakymuose su konkrečiomis pardavimo užsakymų kilmėmis ir pristatymo būdais). Todėl, jei skirtingoms pardavimo užsakymų kilmėms ar skirtingiems pristatymo būdams reikia vykdyti skirtingas taisykles, įvykdymo profilius galima nustatyti atitinkamai. Norėdami nustatyti įvykdymo profilius, atlikite tolesnius veiksmus.  

    1. Eikite į **„Retail“ ir „Commerce“ \> Paskirstytų užsakymų tvarkymas \> Sąranka \> Įvykdymo profiliai**.
    2. Pasirinkite **Naujas**.
    3. Įveskite reikšmes laukuose **Profilis** ir **Aprašas**.
    4. Nustatykite parinktį **Automatiškai taikyti rezultatą**. Jei šią parinktį nustatysite kaip **Taip**, profilio DOM vykdymo rezultatai bus automatiškai pritaikyti pardavimo užsakymų eilutėms. Jei ją nustatote kaip **Ne**, rezultatus galima peržiūrėti tik įvykdymo plane. Jie nebus taikomi pardavimo užsakymų eilutėms.
    5. Jei norite, kad DOM profilis būtų vykdomas užsakymams su visomis pardavimo užsakymų kilmėmis, įskaitant užsakymus, kurių pardavimo užsakymo kilmė yra nenustatyta, parinktį **Apdoroti užsakymus be nurodytos pardavimo kilmės** nustatykite kaip **Taip**. Norėdami profilį vykdyti tik kelioms pardavimo užsakymų kilmėms, jas galite nustatyti puslapyje **Pardavimo kilmės**, kaip paaiškinta vėliau.

        > [!NOTE]
        > „Commerce“ 10.0.12 ir naujesnėje versijoje **Galimybė priskirti įvykdymo grupę įvykdymo profiliui** turi būti įjungta **funkcijų valdymo** darbo srityje. Ši priemonė leidžia nurodyti sandėlių sąrašą, į kurį DOM privalo atsižvelgti, kai optimizavimas vykdomas su įvykdymo profiliu. Jei šis sandėlių sąrašas nenurodytas, DOM peržiūrės visus juridinių subjektų, kurie apibrėžti profilyje, sandėlius.
        >
        > Šia funkcija įtraukiama nauja konfigūracija į **įvykdymo profilio** puslapį, kuris gali būti susietas su viena įvykdymo grupe. 
        >
        > Jei pasirinksite įvykdymo grupę, to įvykdymo profilio DOM taisyklės bus veiksmingai vykdomos į įvykdymo grupę įtrauktuose siuntimo sandėliuose. 
        > 
        > Norėdami veiksmingai naudoti šią funkciją, įsitikinkite, kad yra viena įvykdymo grupė, į kurią įtraukti visi siuntimo sandėliai, ir tada susiekite tą įvykdymo grupę su įvykdymo profiliu.

    6. „FastTab“ **Juridiniai subjektai** pasirinkite **Įtraukti**, tada – juridinį subjektą.
    7. „FastTab“ **Taisyklės** pasirinkite **Įtraukti**, tada – su profiliu susietiną taisyklę.
    8. Kartokite ankstesnius du veiksmus tol, kol su profiliu bus susietos visos reikiamos taisyklės.
    9. Pasirinkite **Įrašyti**.
    10. Veiksmų srities skirtuke **Sąranka** pasirinkite **Pristatymo būdai**.
    11. Puslapyje **Pristatymo būdai** pasirinkite **Naujas**.
    12. Lauke **Įmonė** pasirinkite juridinį subjektą. Įmonių sąraše rodomi tik jūsų anksčiau įtraukti juridiniai subjektai.
    13. Lauke **Pristatymo būdas** pasirinkite su šiuo profiliu susietiną pristatymo būdą. Pristatymo būdo negalima susieti su keliais aktyviais profiliais.
    14. Kartokite ankstesnius du veiksmus tol, kol su profiliu bus susieti visi reikiami pristatymo būdai.
    15. Puslapį **Pristatymo būdai** uždarykite.
    16. Veiksmų srities skirtuke **Sąranka** pasirinkite **Pardavimo užsakymų kilmės**.
    17. Puslapyje **Pardavimo kilmės** pasirinkite **Nauja**.
    18. Lauke **Įmonė** pasirinkite juridinį subjektą. Įmonių sąraše rodomi tik jūsų anksčiau įtraukti juridiniai subjektai.
    19. Lauke **Pardavimo kilmė** pasirinkite su šiuo profiliu susietiną pardavimo kilmę. Pardavimo kilmės negalima susieti su keliais aktyviais profiliais.
    20. Kartokite ankstesnius du veiksmus tol, kol su profiliu bus susietos visos pardavimo kilmės.
    21. Puslapį **Pardavimo kilmės** uždarykite.
    22. Parinktį **Įjungti profilį** nustatykite kaip **Taip**. Jei sąrankoje yra klaidų, gaunate įspėjamąjį pranešimą.

## <a name="dom-processing"></a>DOM apdorojimas

DOM sistema bus vykdoma tik paketinėje užduotyje. Norėdami sukonfigūruoti paketinę užduotį DOM vykdymams, atlikite tolesnius veiksmus.

1. Eikite į **„Retail“ ir „Commerce“ \> Paskirstytų užsakymų tvarkymas \> Paketinis apdorojimas \> DOM doroklės užduoties sąranka**.
1. „FastTab“ **Parametrai** lauke **Įvykdymo profilis** pasirinkite profilį, kuriam turi būti vykdoma DOM sistema.
1. „FastTab“ **Vykdyti fone** lauke **Paketų grupė** pasirinkite sukonfigūruotą paketų grupę.
1. Lauke **Užduoties aprašas** įveskite paketinės užduoties pavadinimą.
1. Pasirinkite **Pasikartojimas** ir nustatykite paketinės užduoties pasikartojimą.
1. Pasirinkite **Gerai**.

Apdorojimo metu DOM užsakymą ir užsakymo eilutes svarstys taip, kaip aprašyta toliau.

- Užsakymo eilutės, atitinkančios DOM profilyje nustatytus pardavimo užsakymų kilmių, pristatymo būdų ir juridinių subjektų kriterijus bei bet kuriuos iš tolesnių kriterijų.

    - Jos yra sukurtos iš prekybos kanalų.
    - Jų niekada tarpininkaudama neperkėlė DOM.
    - Jas tarpininkaudama yra perkėlusi DOM, tačiau jos yra pažymėtos kaip išimtys ir nesiekia didžiausios mėginimų ribos.
    - Pristatymo būdas nėra paėmimas ar elektroninis pristatymas.
    - Jos nėra pažymėtos pristatyti.
    - Jos nėra rankiniu būdu neįtrauktos.

- Nesulaikyti užsakymai

Pritaikiusi taisykles, atsargų apribojimus ir optimizavusi, DOM pasirenka arčiausiai kliento pristatymo adreso esančią vietą. DOM konvertuoja **pristatymo** tipo adresus platumos ir ilgumos vertes. Tada sistema konvertuoja pardavimo užsakymo pristatymo adresą į platumos ir ilgumos vertes bei atnaujina adreso platumos ir ilgumos vertes, kad jas būtų galima naudoti ateityje. DOM priklauso nuo „Bing“ žemėlapių, kad nustatytų tikslias platumos ir ilgumos vertes, atsižvelgiant į adresą, miestą ir pašto indeksų informaciją.

DOM naudoja „Bing“ žemėlapių API, kad apskaičiuotų ploto ar kelio atstumą, priklausomai nuo nustatymų. Tada ji naudoja šią informaciją, kad nustatytų siuntimo išlaidas. Optimizavimo modelis prioritetizuoja baigto užsakymo įvykdymą iš vienos vietos. Net jei užsakymo dalis prieinama tame pačiame mieste ar pašto kode, modelis buvo optimizuotas siekiant sumažinti siuntų skaičių. 

DOM peržiūrės turimas atsargas sandėlio V2 objektuose. Kiekvieno paketinio vykdymo metu DOM skirsto užsakymus į paketus, atsižvelgiant į profilyje nustatytų užduočių **DOM procesoriaus** parametro vertę. Šio parametro numatytoji vertė yra **2000**. Pavyzdžiui, jei vykdymo metu optimizuota 10 000 užsakymo eilučių, **DOM procesoriaus** parametro numatytoji vertė yra **2000**, DOM sukuria penkis paketus, kurie apdorojami vienu metu. Tada įvykdymo planai gaunami iš optimizatoriaus ir taikomi eilutėje. Jei užsakymo eilutę reikia padalyti po dvi vietas, DOM užtikrina, kad kainos ir mokesčiai tinkamai paskirstomi eilutėse.

![Pardavimo užsakymų kriterijai.](./media/ordercriteria.png "Pardavimo užsakymų kriterijai")

## <a name="results-of-dom-runs"></a>DOM vykdymų rezultatai

Jei įvykdymo profilis nustatytas kaip **Automatiškai taikyti**, vykdymo rezultatai bus automatiškai pritaikyti pardavimo užsakymų eilutėms, o įvykdymo planą bus galima peržiūrėti atskirai. Tačiau, jei įvykdymo profilis nėra nustatytas kaip **Automatiškai taikyti**, vykdymo rezultatus galima matyti tik įvykdymo plano rodinyje. 

Norėdami peržiūrėti visus sugeneruotus įvykdymo planus, atlikite tolesnius veiksmus.

1. Eikite į **„Retail“ ir „Commerce“ \> Paskirstytų užsakymų tvarkymas \> Paskirstytų užsakymų tvarkymas**.
2. Darbo srityje **Paskirstytų užsakymų tvarkymas** pasirinkite plytelę **Įvykdymo planai**.
3. Norėdami peržiūrėti konkretų užsakymo įvykdymo planą, pasirinkite jo ID.

    Įvykdymo plano išsamios užsakymo informacijos dalyje rodomos pradinės pardavimo užsakymo eilutės, kurioms buvo taikomas vykdymas. Be standartinių su pardavimo užsakymų eilutėmis susijusių laukų išsamios užsakymo informacijos dalyje taip pat yra tolesni trys su DOM susiję laukai.

    - **Įvykdymo tipas** – šis laukas nurodo, ar pardavimo užsakymo eilutė tarpininkaujant į vietą perkelta visiškai, iš dalies ar apskritai neperkelta.
    - **Išskaidyta** – šis laukas nurodo, ar viena pardavimo užsakymo eilutė išskaidyta ir tarpininkaujant perkelta į skirtingas vietas.
    - **Įvykdymo vietų skaičius** – šis laukas nurodo, kiek įvykdymo eilučių buvo sukurta vienai pardavimo užsakymo eilutei (pagal vietų, į kurias tarpininkaujant buvo perkelta pradinė pardavimo užsakymo eilutė, skaičių).

    Išsamios užsakymo įvykdymo informacijos dalyje rodomas pradinių pardavimo užsakymo eilučių priskyrimas skirtingoms vietoms ir jų kiekiai.

## <a name="order-line-actions-and-statuses"></a>Užsakymo eilučių veiksmai ir būsenos

Toliau aprašomi užsakymo eilutės parametrai. Norėdami atidaryti užsakymo eilutę, eikite į **„Retail“ ir „Commerce“ \> Klientai \> Visi pardavimo užsakymai**.

- Jei pardavimo užsakymo eilutės skirtuke **Bendra** esančią parinktį **Neįtraukti į DOM apdorojimą** nustatysite kaip **Taip**, užsakymas ar užsakymo eilutė nebus įtraukti į DOM apdorojimo procesą.
- Pardavimo užsakymo eilutės skirtuke **Bendra** esantį lauką **DOM būsena** galima nustatyti kaip vieną iš tolesnių reikšmių.

    - **Nėra** – užsakymo eilutė niekada tarpininkaujant neperkelta.
    - **Baigta** – užsakymo eilutė sėkmingai tarpininkaujant perkelta ir priskirta vietai.
    - **Išimtis** – užsakymo eilutė tarpininkaujant perkelta, tačiau jos negalima priskirti vietai. Išimtys turi kelis toliau nurodytus potipius, kuriuos galima peržiūrėti DOM darbo srityje.

        - **Nėra kiekio** – vietose nėra kiekio, kuriam būtų galima priskirti užsakymą.
        - **Didžiausias atmetimų skaičius** – užsakymo eilutė pasiekė didžiausią atmetimų ribą.
        - **Duomenų modifikavimo konfliktas** – nuo tada, kai pardavimo užsakymas buvo tarpininkaujant perkeltas, pakeista užsakymo eilutė. Todėl įvykdymo plano užsakymui taikyti negalima.
        - **Konkrečios užsakymo eilutės išimtis** – yra kelios užsakymo eilutės išimtys.

- Įvedant pardavimo užsakymus, DOM galima vykdyti interaktyviuoju režimu. Kai, įvesdami užsakymo eilutę, nurodote produktą ir kiekį, galite pasirinkti **Atnaujinti eilutę**, o tada dalyje **DOM** pasirinkti **Siūlyti įvykdymo vietą**. Tada matote DOM taisyklėmis paremtą sąrašą vietų, kurios gali įvykdyti užsakymo eilutėje nurodytą kiekį. Šis sąrašas surikiuotas pagal atstumą. Pasirinkite vietą, kad pardavimo užsakymo eilutėje nustatytumėte atitinkamą objektą ir sandėlį. Kad ši funkcija veiktų, turi būti aktyvus įvykdymo profilis, atitinkantis pardavimo eilutėje nurodytą pardavimo kilmę ir pristatymo būdą.
- Norėdami peržiūrėti pardavimo užsakymo eilutės DOM vykdymų žurnalus, pasirinkite **Pardavimo užsakymo eilutė**, tada dalyje **DOM** pasirinkite **Peržiūrėti DOM žurnalus**. DOM žurnaluose rodomi visi DOM sugeneruoti įvykiai ir žurnalai. Žurnalai gali padėti suprasti, kodėl užsakymo eilutei buvo priskirta konkreti vieta ir kokios taisyklės bei kokie apribojimai buvo svarstomi ją priskiriant. Skirtuke **Valdyti** DOM žurnalus taip pat galima peržiūrėti pardavimo užsakymo antraštės lygyje.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>DOM įvykdymo planų valymo užduoties vykdymas

Vykdant DOM apdorojimą, kuriami įvykdymo planai. Ilgainiui sistemoje bus laikoma daugybė įvykdymo planų. Norėdami valdyti sistemos laikomų įvykdymo planų skaičių, galite sukonfigūruoti paketinę užduotį, kurį pagal lauko **Saugojimo laikotarpis dienomis** reikšmę panaikintų senesnius įvykdymo planus.

1. Eikite į **„Retail“ ir „Commerce“ \> Paskirstytų užsakymų tvarkymas \> Paketinis apdorojimas \> DOM įvykdymo duomenų naikinimo užduoties sąranka**. 
1. Lauke **Paketų grupė** pasirinkite sukonfigūruotą paketų grupę.
1. Pasirinkite **Pasikartojimas** ir nustatykite paketinės užduoties pasikartojimą.
1. Pasirinkite **Gerai**.

## <a name="more-information"></a>Daugiau informacijos

Naudojant DOM funkciją reikėtų atsižvelgti į tolesnius dalykus.

- Šiuo metu DOM analizuoja tik tuos užsakymus, kurie yra sukurti iš prekybos kanalų. Kai parinktis **Prekyba** yra nustatyta kaip **Taip**, pardavimo užsakymai identifikuojami kaip mažmeninės prekybos pardavimo užsakymai.
- Su išplėstinėmis sandėlio valdymo funkcijomis „Microsoft“ DOM neišbandė. Klientai ir partneriai turi atidžiai nustatyti, ar DOM yra suderinama su jiems aktualiomis išplėstinėmis sandėlio valdymo galimybėmis ir procesais. Išplėstinis sandėliavimas įgalina konfigūruotinas dimensijas, pvz., atsargų būseną, kurios nepateikia tikslaus supratimo apie turimas atsargas. DOM suteikia išplečiamą metodą turimų atsargų nustatymui diegimo metu, kuris naudoja išplėstinį sandėliavimą. Ją galima naudoti norint dirbti su pritaikytomis atsargų būsenos vertėmis ir kitomis dimensijomis.

    Išplečiamumas DOM yra ribotas, nes optimizavimas vyksta iš anksto sukurtame MIP modelyje, kuris atsižvelgia į optimizavimą ir jo apribojimus. Jau pasiekiami keli atsargų ir tolesnio apdorojimo optimizavimo išplėstinių taškų atsargų nustatymo taškai. DOM profiliai gali skirtis pagal pardavimo kilmę ir pristatymo režimą. Pardavimo užsakymo kilmę galima nustatyti atliekant užsakymų veiksmus ir atsižvelgiant į šias vertes galima naudoti skirtingas optimizavimo strategijas. DOM taip pat palaiko pasirinktinių paketinių užduočių, kurios gali atlikti DOM procesoriaus užduotį kaip įvestį ir įgalinti profilį, kaip parametrą, kūrimą. Todėl norint palaikyti skirtingus verslo scenarijus galima paleisti vieną optimizavimą po kito.

- DOM pasiekiama tik naudojant „Commerce“ debesies versiją. Vietinėse įdiegtyse ji nėra palaikoma.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
