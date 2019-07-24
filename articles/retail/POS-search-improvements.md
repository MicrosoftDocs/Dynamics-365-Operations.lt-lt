---
title: Produktų ir klientų paieška elektroniniame kasos aparate (EKA)
description: Šioje temoje apžvelgiama, kaip patobulinta „Microsoft Dynamics 365 for Retail“ produktų ir klientų ieškos funkcija.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: b2f1d522a60721c746d03e477615265f9a8ba9a0
ms.sourcegitcommit: 3d8c951898e05febc160515127c1bcc5de5882a1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/12/2019
ms.locfileid: "1625647"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Produktų ir klientų paieška elektroniniame kasos aparate (EKA)

[!include [banner](includes/banner.md)]

Į modernųjį elektroninį kasos aparatą (MEKA) ir debesies elektroninį kasos aparatą (DEKA) įtraukta lengvai naudojama funkcija. Kadangi MEKA ir DEKA langų viršuje visada yra ieškos juosta, darbuotojai galėtų greitai rasti produktus ir klientus.

Darbuotojai gali ieškoti produktų asortimentuose ir kataloguose, susietuose su dabartine parduotuve. Be to, jie gali ieškoti asortimentuose ir kataloguose, susietuose su bet kuria kita įmonės parduotuve. Todėl kasininkai gali parduoti ir grąžinti į parduotuvės asortimentą neįtrauktus produktus. Panašiai darbuotojai gali ieškoti klientų, susietų su dabartine parduotuve arba bet kuria kita įmonės parduotuve. Be to, darbuotojai gali ieškoti klientų, susietų su kita pirminės organizacijos įmone.

## <a name="product-search"></a>Produktų paieška

Pagal numatytuosius parametrus produktų ieškoma parduotuvės asortimente. Šis ieškos tipas vadinamas *vietine produktų ieška*. Tačiau darbuotojai gali lengvai pereiti į bet kokį su dabartine parduotuve susietą katalogą arba jie gali ieškoti kitoje parduotuvėje. Šis ieškos tipas vadinamas *nuotoline produktų ieška*. Norėdami pakeisti katalogą, pasirinkite kairėje puslapio pusėje esantį mygtuką **Kategorijos**. Pasirodžiusios srities viršuje pasirinkite mygtuką **Keisti katalogą**, tada pasirinkite vieną iš galimų katalogų, kad jį galėtumėte naršyti. Sistema pasirinktame kataloge ieškos produktų.

Puslapyje **Keisti katalogą** darbuotojai gali lengvai pasirinkti bet kurią parduotuvę arba produktų jie gali ieškoti visose parduotuvėse.

![Katalogo keitimas](./media/Changecatalog.png "Katalogo keitimas")

Atliekant vietinę produktų iešką, ieškoma tolesnėse produktų ypatybėse.

- Produkto numeris
- Produkto pavadinimas
- aprašymas
- Dimensijos
- Brūkšninis kodas
- Ieškos pavadinimas

### <a name="enhancements-to-local-product-searches"></a>Vietinių produktų ieškų patobulinimai

Vietinių produktų ieškų veikimas dabar patogesnis vartotojui. Atlikti tolesni patobulinimai.

- Į ieškos juostą įtraukti produktų ir klientų išplečiamieji meniu, kad darbuotojai prieš atlikdami iešką galėtų pasirinkti **Produktas** arba **Klientas**. Pagal numatytuosius parametrus pasirinkta **Produktas**, kaip parodyta tolesnėje iliustracijoje.
- Atlikdami ieškas su keliais raktažodžiais (t. y., atlikdami ieškas, kuriose naudojami ieškos terminai), mažmenininkai gali sukonfigūruoti, ar į ieškos rezultatus reikia įtraukti rezultatus, atitinkančius *bet kurį* ieškos terminą, ar tik tuos rezultatus, kurie atitinka *visus* ieškos terminus. Šios funkcijos parametras pasiekiamas naujoje EKA funkcijų profilio grupėje pavadinimu **Produktų ieška**. Numatytasis parametras yra **Atitinka bet kurį ieškos terminą**. Šis parametras taip pat yra rekomenduojamas parametras. Kai naudojamas parametras **Atitinka bet kurį ieškos terminą**, kaip rezultatai pateikiami visi produktai, visiškai ar iš dalies atitinkantys vieną ar kelis ieškos terminus. Tuose rezultatuose didėjimo tvarka surikiuojami produktai su daugiausiai raktažodžių atitikčių (visiškų arba dalinių).

    Naudojant parametrą **Atitinka visus ieškos terminus**, pateikiami tik tie produktai, kurie atitinka visus ieškos terminus (visiškai arba iš dalies). Šis parametras naudingas, kai produktų pavadinimai yra ilgi ir darbuotojai ieškos rezultatuose nori matyti tik ribotą produktų skaičių. Tačiau šio tipo ieška turi du tolesnius apribojimus.

    - Ieška atliekama atskirose produktų ypatybėse. Pavyzdžiui, pateikiami tik tie produktai, kurių bent vienoje ypatybėje yra visi ieškomi raktažodžiai.
    - Dimensijose neieškoma.

- Mažmenininkai dabar produktų iešką gali sukonfigūruoti taip, kad, vartotojams vedant produktų pavadinimus, būtų rodomi ieškos pasiūlymai. Naujas šios funkcijos parametras pasiekiamas EKA funkcijų profilio grupėje pavadinimu **Produktų ieška**. Parametro pavadinimas yra **Vedant tekstą rodyti ieškos pasiūlymus**. Ši funkcija darbuotojams gali padėti greitai rasti ieškomą produktą, nes jiems nereikia rankiniu būdu įvesti viso pavadinimo.
- Produktų ieškos algoritmas ieškomų terminų dabar taip pat ieško produkto ypatybėje **Ieškos pavadinimas**.

![Produktų pasiūlymai](./media/Productsuggestions.png "Produktų pasiūlymai")

## <a name="customer-search"></a>Kliento ieška

Naudojant klientų iešką, įvairiais tikslais ieškoma klientų. Pavyzdžiui, kasininkai gali norėti peržiūrėti kliento pageidavimų sąrašą ar pirkimo istoriją, arba klientą įtraukti į operaciją. Ieškos algoritmas atitinka ieškos terminus pagal vertes, nurodytas šiose kliento ypatybėse:

- Pavadinimas / vardas ir (arba) pavardė
- El. pašto adresas
- Telefono numeris
- Lojalumo kortelės numeris
- Adresas 
- Sąskaitos numeris

Iš visų šių ypatybių, pavadinimas / vardas ir (arba) pavardė suteikia daugiausiai lankstumo ieškant kelių raktinių žodžių, nes algoritmas pateikia visus klientus, kurie atitinka bet kurį iš ieškomų raktažodžių. Daugiausia raktažodžių atitinkantys klientai rodomi rezultatų viršuje. Tai naudinga kasininkams, kai jie ieško įvesdami vardą ir pavardę, bet pirmą kartą įvedant duomenis pavardė ir vardas buvo sukeisti vietomis. Tačiau dėl funkcionalumo, visose kitose ypatybėse išlaikoma ieškos raktažodžių tvarka. Todėl, jei ieškos raktinių žodžių tvarka nesutampa su tvarka, kuria duomenys išsaugomi, nebus pateikta jokių rezultatų.

Pagal numatytuosius parametrus klientų ieškoma su parduotuve susietose klientų adresų knygelėse. Šis ieškos tipas vadinamas *vietine klientų ieška*. Tačiau darbuotojai klientų taip pat gali ieškoti visuotinai. Kitaip tariant, jie gali ieškoti visose įmonės parduotuvėse ir visuose kituose juridiniuose subjektuose. Šis ieškos tipas vadinamas *nuotoline klientų ieška*.

Norėdami ieškoti visuotinai, darbuotojai gali pasirinkti puslapio apačioje esantį mygtuką **Filtruoti rezultatus**, o tada pasirinkti parinktį **Ieškoti visose parduotuvėse**, kaip parodyta tolesnėje iliustracijoje. Tokiu atveju pateikiami ne tik klientai. Taip pat pateikiamos visų tipų šalys, priklausančios bet kuriai būstinės adresų knygelei. Šios šalys – tai darbininkai, tiekėjai, kontaktai ir konkurentai.

> [!NOTE]
> Kad nuotolinė klientų ieška pateiktų rezultatų, reikia įvesti mažiausiai keturis simbolius.

Atliekant nuotolinę klientų iešką, kitų juridinių subjektų klientų ID nerodomi, nes dabartinėje įmonėje tų šalių klientų ID nėra sukurta. Tačiau, jei darbuotojas atidaro kliento informacijos puslapį, sistema automatiškai sugeneruoja šalies kliento ID ir su klientu susieja parduotuvės klientų adresų knygeles. Todėl klientas bus matomas vėliau atliekamose vietinėse parduotuvių ieškose.

![Visuotinė klientų ieška](./media/Globalcustomersearch.png "Visuotinė klientų ieška")

### <a name="enhancements-to-local-customer-search"></a>Vietinių klientų ieškos patobulinimai

Ieška pagal telefono numerį supaprastinta. Atliekant tokią iešką dabar ignoruojami specialieji simboliai, pvz., tarpai, brūkšneliai ir skliausteliai, kurie galėjo būti pridėti sukūrus klientą. Todėl informacijos ieškantiems kasininkams nereikia nerimauti dėl telefono numerio formato. Jie taip pat gali ieškoti klientų įvesdami dalinį telefono numerį. Jei telefono numeryje yra specialių simbolių, jį taip pat galima surasti ieškant skaitmenų, kurie pateikti po specialiųjų simbolių. Pavyzdžiui, jei kliento telefono numeris buvo įvestas kaip **123-456-7890**, kasininkas kliento gali ieškoti įvesdamas **123**, **456**, **7890** arba **1234567890**, arba įvesdamas pirmuosius keletą telefono numerio skaitmenų.

Įprastinė kliento ieška gali užimti daug laiko, nes ji vykdoma daugelyje laukų. Dabar kasininkai gali ieškoti vieno kliento laukuose, pvz., vardo ir pavardės, el. pašto adreso arba telefono numerio. Kliento ieškos algoritmo naudojamos ypatybės kartu vadinamos *kliento ieškos kriterijais*. Sistemos administratorius gali lengvai sukonfigūruoti vieną arba kelis kriterijus kaip nuorodas, kurios bus rodomos EKA. Kadangi ieška apribojama iki vieno kriterijaus, rodomi tik tinkami ieškos rezultatai ir efektyvumas yra daug didesnis nei įprastos kliento ieškos efektyvumas. Toliau nurodytame paveikslėlyje pavaizduotos EKA kliento ieškos nuorodos.

![Kliento ieškos nuorodos](./media/SearchShortcutsPOS.png "Kliento ieškos nuorodos")

Norėdamas nustatyti ieškos kriterijus kaip nuorodas, administratorius turi atidaryti puslapį **Mažmeninės prekybos parametrai** programoje „Microsoft Dynamics 365 for Finance and Operations“, tada skirtuke **EKA ieškos kriterijai** pasirinkti kriterijus, kurie turėtų būti rodomi kaip nuorodos.

![Ieškos nuorodų konfigūravimas](./media/ConfigureShortcutsAX.png "Ieškos nuorodų konfigūravimas")

> [!NOTE]
> Jei įtrauksite per daug nuorodų, EKA ieškos juostos išplečiamasis meniu bus perpildytas ir darbuotojui gali būti sunkiau ieškoti informacijos. Rekomenduojame įtraukti tik tiek nuorodų, kaip jums reikia.

Lauke **Rodymo tvarka** laukas nurodoma tvarka, kuria nuorodos rodomos EKA. Rodomi kriterijai yra paruoštos naudoti ypatybės, kurias kliento ieškos algoritmas naudoja klientams ieškoti. Tačiau partneriai kaip ieškos nuorodas gali įtraukti pasirinktinių ypatybių. Norėdamas kaip ieškos nuorodas įtraukti pasirinktinių ypatybių, sistemos administratorius turi išplėsti išplečiamąjį išvardijimą (išvardijimas), kuris naudojamas kliento ieškos kriterijams nustatyti, ir tada pažymėti partnerio pasirinktines ypatybes kaip nuorodas. Partneriai yra atsakingi už kodą rašymą rezultatams rasti, kai ieškose naudojamos jų pasirinktinės nuorodos.

> [!NOTE]
> Į išvardijimą įtraukta pasirinktinė ypatybė, neturi įtakos standartiniam klientų ieškos algoritmui. Kitaip tariant, klientų ieškos algoritmas neieškos pasirinktinėje ypatybėje. Vartotojai ieškodami gali naudoti pasirinktines ypatybes tik jei tos pasirinktinės ypatybės yra įtrauktos kaip nuorodos arba jei numatytasis ieškos algoritmas yra perrašytas.

Būsimame „Microsoft Dynamics 365 for Retail“ leidime pardavėjai galės nustatyti numatytąjį EKA kliento ieškos režimą, kad būtų **Ieškoma visose parduotuvėse**. Ši konfigūracija gali būti naudinga scenarijuose, kuriuose būtina nedelsiant rasti už EKA ribų sukurtus klientus (pvz., net prieš vykdant paskirstymo užduotį). Galima naudotis nauja EKA funkcijų šablono parinktimi **Numatytasis kliento ieškos režimas**. Nustatykite, kad ši parinktis būtų **Įjungta**, kad būtų galima nustatyti numatytojo ieškos režimo parinktį **Ieškoma visose parduotuvėse**. Po kiekvieno kliento ieškos bandymo realiuoju laiku kreipiamasi į būstinę.

Siekiant išvengti nenumatytų funkcionalumo problemų, ši konfigūracija paslėpta už versijos vėliavėlės, kurios pavadinimas **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. Todėl norėdamas, kad vartotojo sąsajoje (UI) būtų rodoma nuostata **Numatytasis kliento ieškos režimas**, pardavėjas turi sukurti palaikymo bilietą vartotojo priėmimo bandymui (UAT) ir gamybos aplinkas. Gavusi bilietą inžinierių komanda dirba su pardavėju, kad įsitikintų, jog pardavėjas bandymą atlieka ne gamybos aplinkose, kad įvertintų efektyvumą ir įdiegtų visus reikiamus optimizavimus.
