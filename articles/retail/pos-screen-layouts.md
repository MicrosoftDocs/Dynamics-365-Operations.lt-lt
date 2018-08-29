---
title: Elektroninio kasos aparato (EKA) ekrano maketai
description: "Šioje temoje pateikiama informacija apie „Microsoft Dynamics 365 for Retail“ elektroninio kasos aparato (EKA) patirčių ekrano išdėstymus."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ced27adb8fe481270cb008e187693cda96773339
ms.contentlocale: lt-lt
ms.lasthandoff: 08/09/2018

---

# <a name="screen-layouts-for-the-point-of-sale-pos"></a>Elektroninio kasos aparato (EKA) ekrano maketai

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama informacija apie „Microsoft Dynamics 365 for Retail“ elektroninio kasos aparato (EKA) patirčių ekrano išdėstymus.

„Retail“ EKA vartotojo sąsają (UI) galima sukonfigūruoti naudojant parduotuvėms, kasos aparatams ir (arba) vartotojams priskirtų vaizdo profilių ir ekrano išdėstymų kombinaciją.

Tolesnėje iliustracijoje parodyti ryšiai tarp įvairių objektų, kuriuos galima konfigūruoti EKA vartotojo sąsajoje.

![EKA ekrano išdėstymų objektai](../retail/media/POS-layout-configuration-entities-diagram.png)

## <a name="visual-profile"></a>Vaizdo šablonas
Vaizdo profiliai priskiriami kasos aparatams ir jais nurodoma pagal kasos aparatą suskirstytus ir vartotojų bendrai naudojamus vaizdo elementus. Kiekvienas prie kasos aparato prisijungęs vartotojas mato tą pačią temą, spalvas ir vaizdus.

![EKA darbo pradžios ekranas su šviesia tema](../retail/media/POS-Welcome-Screen-with-Light-theme.png)

![EKA operacijų ekranas su tamsia tema](../retail/media/POS-Transaction-Screen-with-Dark-theme.png)

- **Profilio numeris** – tai unikalusis vaizdo profilio identifikatorius.
- **Aprašas** – galite nurodyti prasmingą pavadinimą, kuris padėtų nuspręsti, kuris profilis tinkamas jūsų atveju.
- **Tema** – galite pasirinkti šviesią arba tamsią programos temą. Nuo temos priklauso visos programos šriftų ir fono spalvos.
- **Akcento spalva** – tai spalva, kuri naudojama elektroniniame kasos aparate norint atskirti arba paryškinti konkrečius vaizdo elementus, pvz., plyteles, komandų mygtukus ir hipersaitus. Paprastai su šiais elementais galima atlikti veiksmų.
- **Antraštės spalva** – puslapio antraštės spalvą galite konfigūruoti pagal pardavėjo prekių ženklų reikalavimus. Ši funkcija pasiekiama tik „Microsoft Dynamics 365 for Retail‟ 1611 versijoje.
- **Prisijungimo fonai** – gali nurodyti, koks fono vaizdas bus naudojamas prisijungimo ekrane. Fono vaizdų failų dydis turėtų būti kuo mažesnis, nes saugant ir įkeliant didelius failus gali pablogėti programos veikimas ir našumas.
- **Programos fonas** – galite nurodyti fono vaizdą, kuris visoje programoje būtų naudojamas vietoj vienspalvės temos. Kaip ir prisijungimo fonų, šių fonų failų dydis turėtų būti kuo mažesnis.

## <a name="screen-layouts"></a>Ekrano maketai
Nuo ekrano išdėstymo konfigūracijų priklauso, kokie bus UI valdiklių veiksmai, turinys ir išdėstymo tvarka EKA darbo pradžios ekrane ir **operacijų** ekrane.

![EKA ekrano išdėstymo rodinys](../retail/media/POS-Screen-Layout-View.png)

- **Darbo pradžios ekranas** – daugeliu atvejų tai puslapis, kurį vartotojai mato pirmą kartą prisijungę prie EKA. Darbo pradžios ekrane gali būti prekės ženklo vaizdas ir mygtukynai, suteikiantys prieigą prie EKA operacijų. Paprastai šiame ekrane pateikiamos operacijos, kurios nepriklauso nuo dabartinės operacijos.

    ![EKA darbo pradžios ekranas](../retail/media/POS-Welcome-Screen.png)

- **Operacijų ekranas** – **operacijų** ekranas yra pagrindinis EKA ekranas, skirtas apdoroti pardavimo operacijas ir užsakymus. Turinys ir išdėstymas konfigūruojami naudojant ekrano išdėstymo dizaino įrankį.

    ![EKA operacijų ekranas](../retail/media/POS-Transaction-Screen.png)

- **Numatytasis pradžios ekranas** – kai kurie mažmenininkai pageidauja, kad prisijungę kasininkai eitų tiesiai į **operacijų** ekraną. Parametras **Numatytasis pradžios ekranas** leidžia nurodyti numatytąjį kiekvieno ekrano išdėstymo ekraną, rodomą prisijungus.

### <a name="assignment"></a>Priskyrimas

Ekranų išdėstymus galima priskirti pagal parduotuvę, registrą arba vartotoją. Pasirinkus vartotojo priskyrimą nepaisoma kasos aparato ir parduotuvės priskyrimų, o pasirinkus kasos aparato priskyrimą nepaisoma parduotuvės priskyrimo. Paprastoje situacijoje, kai visi vartotojai naudoja tą patį išdėstymą (nesvarbu, koks kasos aparatas ar vaidmuo), ekrano išdėstymą galima nustatyti tik parduotuvės lygiu. Tose situacijose, kai konkretiems kasos aparatams ar vartotojams reikalingi specializuoti išdėstymai, galima juos priskirti.

### <a name="layout-sizes"></a>Maketo dydžiai

Didžioji EKA UI dalis yra reaguojanti, o išdėstymo dydis keičiamas ir pats išdėstymas reguliuojamas automatiškai, pagal ekrano dydį ir padėtį. Tačiau EKA **operacijų** ekraną būtina sukonfigūruoti kiekvienai numatomai ekrano skiriamajai gebai.

Paleidžiama EKA programa automatiškai pasirenka artimiausią sukonfigūruotą įrenginio išdėstymo dydį. Ekrano išdėstyme taip pat gali būti konfigūracijų stačiam ir gulsčiam režimams bei tiek viso dydžio, tiek kompaktiniams įrenginiams. Todėl vartotojams gali būti priskirtas vienas ekrano išdėstymas, veikiantis su įvairiais parduotuvėje esančiais dydžiais ir formos veiksniais.

![EKA išdėstymo dydžiai](../retail/media/POS-Screen-Layout-Sizes.png)

- **Pavadinimas** – galite įvesti prasmingą pavadinimą ekrano dydžiui identifikuoti.
- **Išdėstymo tipas** – EKA programa savo UI gali rodyti įvairiais režimais ir taip konkrečiame įrenginyje užtikrinti geriausią vartotojų patirtį.

    - **„Modern POS“ – visas** – visus išdėstymus paprastai geriausia naudoti didesniems ekranams, pvz., kompiuterių monitoriams ir planšetiniams kompiuteriams. Galite pasirinkti įtrauktinus UI elementus, nurodyti tų elementų dydį bei išdėstymą ir konfigūruoti tikslias ypatybes. Pasirinkus pilnus išdėstymus palaikomos vertikalios ir horizontalios konfigūracijos.
    - **„Modern POS“ – kompaktinis** – kompaktinius išdėstymus paprastai geriausia naudoti telefonams ir nedideliems planšetiniams kompiuteriams. Kompaktinių įrenginių dizaino galimybės ribotos. Galite sukonfigūruoti kvitų ir bendrųjų sumų skydelių stulpelius bei laukus.

- **Plotis / aukštis** – šios reikšmės nurodo numatomą faktinį ekrano dydį pikseliais. Atminkite, kad kai kuriose operacinėse sistemose su didelės skiriamosios gebos ekranais naudojama mastelio keitimo funkcija.

> [!TIP]
> Sužinoti, kokio dydžio išdėstymo reikia EKA ekranui, galite peržiūrėję skiriamąją gebą programoje. Paleiskite EKA ir eikite į **Parametrai \> Seanso informacija**. EKA rodo šiuo metu įkeltą išdėstymą, jo dydį ir programos lango skiriamąją gebą.

![EKA išdėstymo dydžiai](../retail/media/POS-Session-Information.png)

### <a name="button-grids"></a>Mygtukynai
Kiekvienam ekrano išdėstymo dydžiui galite sukonfigūruoti ir priskirti EKA darbo pradžios ekrano ir **operacijų** ekrano mygtukynus. Darbo pradžios ekrano mygtukynai automatiškai išdėstomi iš kairės į dešinę, nuo mažiausio skaičiaus (1 darbo pradžios ekranas) iki didžiausio.

Viso dydžio EKA išdėstymuose mygtukynų išdėstymas nurodomas ekrano išdėstymų dizaino įrankyje.

Kompaktiniuose EKA išdėstymuose mygtukynai automatiškai išdėstomi iš viršaus į apačią, nuo mažiausio skaičiaus (1 operacijų ekranas) iki didžiausio. Juos galima pasiekti meniu **Veiksmai**.

![Kompaktinių išdėstymų mygtukynai](../retail/media/Compact-View-Button-Grids.png)

### <a name="images"></a>Vaizdai
Kiekvienam ekrano išdėstymo dydžiui galite nurodyti į EKA UI įtrauktinus vaizdus. Viso dydžio EKA išdėstymuose galima nurodyti vieną darbo pradžios ekrano vaizdą. Šis vaizdas rodomas kaip pirmas UI elementas iš kairės. **Operacijų** ekrane vaizdai gali būti naudojami kaip skirtukų vaizdai arba kaip logotipas. Kompaktiniuose EKA išdėstymuose šie vaizdai nenaudojami.

### <a name="screen-layout-designer"></a>Ekrano maketo dizaineris

Ekrano išdėstymų dizaino įrankis leidžia konfigūruoti įvairius kiekvieno išdėstymo dydžio EKA **operacijų** ekrano aspektus (tiek stačio, tiek gulsčio režimų ir tiek viso dydžio, tiek kompaktinių išdėstymų). Vartotojui kiekvieną kartą įjungus programą, naudodamas diegimo technologiją „ClickOnce“ ekrano išdėstymų dizaino įrankis atsisiunčia, įdiegia ir paleidžia naujausią programos versiją. Būtinai patikrinkite „ClickOnce“ reikalavimus naršyklėms. Kai kuriose naršyklėse, pvz., „Google Chrome“, reikalingi plėtiniai.

> [!IMPORTANT]
> Turite sukonfigūruoti kiekvieno apibrėžto ir EKA naudojamo išdėstymo dydžio ekrano išdėstymą.

### <a name="full-layout-designer"></a>Viso dydžio išdėstymų dizaino įrankis

Viso dydžio išdėstymų dizaino įrankis vartotojams leidžia į EKA **operacijų** ekraną nuvilkti UI valdiklių ir konfigūruoti tų valdiklių parametrus.

![EKA viso dydžio išdėstymų dizaino įrankis (gulsčias režimas)](../retail/media/POS-Full-Layout-Designer-Landscape.png)

- **Importuoti išdėstymą / eksportuoti išdėstymą** – EKA ekrano išdėstymų dizainus galite eksportuoti ir importuoti kaip XML failus, kad juos galėtumėte lengvai pakartotinai naudoti ir bendrinti visose aplinkose. Svarbu importuoti teisingų dydžių išdėstymus. Kitu atveju UI elementai gali būti neteisingai išdėstyti ekrane.
- **Gulsčias / stačias** – jei EKA įrenginys vartotojams leidžia įjungti gulsčią ir stačią režimus, ekrano išdėstymą turite apibrėžti kiekvienam režimui. EKA automatiškai aptinka ekrano pasukimą ir rodo teisingą išdėstymą.
- **Išdėstymo tinklelis** – EKA išdėstymų dizaino įrankis naudoja 4 pikselių tinklelį. Kad būtų lengviau teisingai sulygiuoti turinį, UI valdikliai prisikabina prie tinklelio.
- **Dizaino įrankio mastelio keitimas** – kad geriau matytumėte EKA ekrano turinį, dizaino įrankio rodinį galite didinti ir mažinti. Ši funkcija yra naudinga, kai EKA ekrano skiriamoji geba labai skiriasi nuo ekrano, naudojamo dizaino įrankyje, skiriamosios gebos.
- **Rodyti / slėpti naršymo juostą** – viso dydžio EKA išdėstymuose galite pasirinkti, ar **operacijų** ekrane matoma kairioji naršymo juosta. Ši funkcija naudinga naudojant mažesnės skiriamosios gebos ekranus. Norėdami nustatyti matomumą, dizaino įrankyje dešiniuoju pelės mygtuku spustelėkite naršymo juostą ir pažymėkite arba išvalykite žymės langelį **Visada matoma**. Jei naršymo juosta yra paslėpta, ją pasiekti EKA vartotojai vis dar gali naudodami viršutinėje kairiojoje dalyje esantį meniu.

    ![Rodyti / slėpti naršymo juostą](../retail/media/Navigation-Bar.PNG)

- **EKA valdikliai** – EKA išdėstymų dizaino įrankis palaiko tolesnius valdiklius. Daug valdiklių galite konfigūruoti dešiniuoju pelės klavišu spustelėdami ir naudodami kontekstinį meniu.

    ![EKA UI valdikliai](../retail/media/POS-UI-Controls.png)

    - **Skaičių klaviatūra** – tai pagrindinis vartotojų įvesties EKA **operacijų** ekrane mechanizmas. Valdiklį galite sukonfigūruoti taip, kad būtų rodoma visa skaičių klaviatūra. Ši parinktis puikiai tinka įrenginiams su jutikliniais ekranais. Taip pat jį galite sukonfigūruoti taip, kad būtų rodomas tik įvesties laukas. Tokiu atveju įvesčiai naudojama fizinė klaviatūra. Skaičių klaviatūros parametrus galima nustatyti tik naudojant viso dydžio išdėstymus. Kompaktiniuose išdėstymuose visa skaičių klaviatūra visada rodoma **operacijų** ekrane.
    - **Bendrųjų sumų skydelis** – galite sukonfigūruoti, kad bendrųjų sumų skydelis būtų rodomas vienu arba dviem stulpeliais, kuriuose rodomos tam tikros reikšmės, pvz., eilučių skaičius, nuolaidos suma, išlaidos, tarpinė suma ir mokestis. Kompaktiniuose išdėstymuose galima naudoti tik vieną stulpelį.
    - **Gavimo kvitų skydelis** – gavimo kvitų skydelyje pateikiamos naudojant EKA apdorotų produktų ir paslaugų pardavimo eilutės, mokėjimų eilutės ir pristatymo informacija. Galite nurodyti stulpelius, pločius ir išdėstymo tvarką. Kompaktiniuose išdėstymuose taip pat galite sukonfigūruoti papildomą informaciją, rodomą po pagrindine eilute esančioje eilutėje.
    - **Kliento kortelė** – kliento kortelėje rodoma informacija apie klientą, susietą su dabartine operacija. Kliento kortelę galite sukonfigūruoti taip, kad joje papildoma informacija būtų slepiama arba rodoma.
    - **Skirtuko valdiklis** – į ekrano išdėstymą galite įtraukti skirtuko valdiklį, o į jį įdėti kitų valdiklių, pvz., skaičių klaviatūrą, kliento kortelę ar mygtukynų. Skirtuko valdiklis – tai konteineris, padedantis ekrane sutalpinti daugiau turinio. Skirtuko valdiklį galima įtraukti tik naudojant viso dydžio išdėstymus.
    - **Vaizdas** – vaizdo valdiklį galite naudoti, jei norite, kad **operacijų** ekrane būtų rodomas parduotuvės logotipas arba kitas prekės ženklo vaizdas. Vaizdo valdiklį galima įtraukti tik naudojant viso dydžio išdėstymus.
    - **Rekomenduojami produktai** – jei sukonfigūruotas aplinkos rekomenduojamų produktų valdiklis, jame pagal mašininį mokymą rodomi produktų pasiūlymai.
    - **Pasirinktinis valdiklis** – pasirinktinis valdiklis ekrano išdėstyme veikia kaip vietos rezervavimo ženklas ir leidžia rezervuoti vietą pasirinktiniam turiniui. Pasirinktinį valdiklį galima įtraukti tik naudojant viso dydžio išdėstymus.

### <a name="compact-layout-designer"></a>Kompaktinių išdėstymų dizaino įrankis
Kaip ir viso dydžio išdėstymų dizaino įrankis, kompaktinių išdėstymų dizaino įrankis leidžia konfigūruoti EKA ekrano išdėstymą telefonams ir mažiems planšetiniams kompiuteriams. Tačiau šiuo atveju pats išdėstymas yra fiksuotas. Išdėstyme valdiklius galite konfigūruoti dešiniuoju pelės klavišu spustelėdami ir naudodami kontekstinį meniu. Tačiau negalite naudoti nuvilkimo operacijų su papildomu turiniu.

![Kompaktinių išdėstymų dizaino įrankis](../retail/media/Compact-Layout-Designer.png)

### <a name="button-grid-designer"></a>Mygtukynų dizaino įrankis
Mygtukynų dizaino įrankis leidžia konfigūruoti mygtukynus, kuriuos galima naudoti EKA viso dydžio ir kompaktinių išdėstymų darbo pradžios ekrane bei **operacijų** ekrane. Tą patį mygtukyną galima naudoti įvairiuose išdėstymuose ir su įvairiais išdėstymų tipais. Kaip ir ekrano išdėstymų dizaino įrankis, vartotojui kiekvieną kartą įjungus programą, naudodamas diegimo technologiją „ClickOnce“ mygtukynų dizaino įrankis atsisiunčia, įdiegia ir paleidžia naujausią programos versiją. Būtinai patikrinkite „ClickOnce“ reikalavimus naršyklėms. Kai kuriose naršyklėse, pvz., „Google Chrome“, reikalingi plėtiniai.

![Mygtukynų dizaino įrankis](../retail/media/Button-Grid-Designer.png)

- **Naujas mygtukas** – spustelėkite, jei į mygtukyną norite įtraukti naują mygtuką. Pagal numatytuosius parametrus nauji mygtukai rodomi viršutiniame kairiajame mygtukyno kampe. Tačiau mygtukus galite išdėstyti juos vilkdami išdėstyme.

    > [!IMPORTANT]
    > Mygtukyno turinys gali persidengti. Išdėstydami mygtukus įsitikinkite, kad jie nepaslepia kitų mygtukų.

- **Naujas dizainas** – spustelėkite, jei mygtukyno išdėstymą norite nustatyti automatiškai, nurodydami kiekvienos eilutės ir stulpelio mygtukų skaičių.
- **Mygtuko ypatybės** – mygtuko ypatybes galite konfigūruoti dešiniuoju pelės mygtuku spustelėdami mygtuką ir naudodami kontekstinį meniu.

    > [!IMPORTANT]
    > Kai kurie mygtukynų parametrai taikomi tik įmonės EKA aparatui, o „Retail Moden POS“ ar „Cloud POS“ – ne.

    ![Mygtukynų mygtukų ypatybės](../retail/media/Button-grid-button-properties.png)

    - **Veiksmas** – taikytinų EKA operacijų sąraše pasirinkite operaciją, iškviečiamą EKA aparate spustelėjus mygtuką.

        Norėdami matyti palaikomų EKA operacijų sąrašą, žr. [EKA operacijos, prisijungus ir neprisijungus prie interneto](pos-operations.md).

    - **Veiksmo parametrai** – kai kurios EKA operacijos iškviestos naudoja papildomų parametrų. Pavyzdžiui, naudodami operaciją Įtraukti produktą, vartotojai gali nurodyti įtrauktiną produktą.
    - **Mygtuko tekstas** nurodykite tekstą, rodomą ant EKA mygtuko.
    - **Slėpti mygtuko tekstą** – naudodami šį žymės langelį galite slėpti arba rodyti mygtuko tekstą. Mažų mygtukų, kuriuose rodoma tik piktograma, tekstas dažnai yra paslėptas.
    - **Patarimas** – nurodykite papildomą pagalbos tekstą, rodomą vartotojams virš mygtuko užvedus pele.
    - **Dydis stulpeliais / dydis eilutėmis** – galite nurodyti mygtuko aukštį ir plotį.

        ![EKA mygtukų dydžiai eilutėmis ir stulpeliais](../retail/media/POS-Button-Sizes-In-Rows-And-Columns.png)

    - **Pasirinktinis šriftas** – pažymėję žymės langelį **Įjungti pasirinktinį EKA šriftą**, galite nurodyti kitą šriftą nei numatytasis EKA sistemos šriftas.
    - **Pasirinktinė tema** – pagal numatytuosius parametrus EKA mygtukuose naudojama akcento spalva iš vaizdo profilio. Pažymėję žymės langelį **Naudoti pasirinktinę temą**, galite nurodyti papildomų spalvų.

        > [!NOTE]
        > „Retail Modern POS“ ir „Cloud POS“ naudoja tik reikšmes **Fono spalva** ir **Šrifto spalva**.

    - **Mygtuko vaizdas** – į mygtukus galima įtraukti vaizdų ar piktogramų. Galite rinktis iš vaizdų, nurodytų dalyje **Mažmeninė prekyba \> Kanalų sąranka \> EKA sąranka \> EKA \> Vaizdai**.

![EKA mygtukyno pavyzdys](../retail/media/Example-Button-Grid-In-POS.png)

## <a name="additional-resources"></a>Papildomi ištekliai

[„Retail POS“ maketo dizaino įrankio diegimas](install-pos-layout-designer.md)

