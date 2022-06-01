---
title: Produktų ir klientų paieška elektroniniame kasos aparate (EKA)
description: Šioje temoje apžvelgiama, kaip patobulinta „Dynamics 365 Commerce“ produktų ir klientų ieškos funkcija.
author: ShalabhjainMSFT
ms.date: 05/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 460c7d3b00421ba43414f7343887edf9b8adad9c
ms.sourcegitcommit: 9dd2d32fc303023a509d58ec7b5935f89d1e9c6d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/26/2022
ms.locfileid: "8806433"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Produktų ir klientų paieška elektroniniame kasos aparate (EKA)

[!include [banner](includes/banner.md)]

Į modernųjį elektroninį kasos aparatą (MEKA) ir debesies elektroninį kasos aparatą (DEKA) įtraukta lengvai naudojama funkcija. Kadangi MEKA ir DEKA langų viršuje visada yra ieškos juosta, darbuotojai galėtų greitai rasti produktus ir klientus.

Darbuotojai gali ieškoti produktų asortimentuose ir kataloguose, susietuose su dabartine parduotuve. Be to, jie gali ieškoti asortimentuose ir kataloguose, susietuose su bet kuria kita įmonės parduotuve. Todėl kasininkai gali parduoti ir grąžinti į parduotuvės asortimentą neįtrauktus produktus. Panašiai darbuotojai gali ieškoti klientų, susietų su dabartine parduotuve arba bet kuria kita įmonės parduotuve. Be to, darbuotojai gali ieškoti klientų, susietų su kita pirminės organizacijos įmone.

## <a name="product-search"></a>Produktų paieška

Pagal numatytuosius parametrus produktų ieškoma parduotuvės asortimente. Šis ieškos tipas vadinamas *vietine produktų ieška*. Tačiau darbuotojai gali lengvai pereiti į bet kokį su dabartine parduotuve susietą katalogą arba jie gali ieškoti kitoje parduotuvėje. Šis ieškos tipas vadinamas *nuotoline produktų ieška*. Norėdami pakeisti katalogą, pasirinkite kairėje puslapio pusėje esantį mygtuką **Kategorijos**. Pasirodžiusios srities viršuje pasirinkite mygtuką **Keisti katalogą**, tada pasirinkite vieną iš galimų katalogų, kad jį galėtumėte naršyti. Sistema pasirinktame kataloge ieškos produktų.

Puslapyje **Keisti katalogą** darbuotojai gali lengvai pasirinkti bet kurią parduotuvę arba produktų jie gali ieškoti visose parduotuvėse.

![Katalogo keitimas.](./media/Changecatalog.png "Katalogo keitimas")

Atliekant vietinę produktų iešką, ieškoma tolesnėse produktų ypatybėse.

- Produkto numeris
- Produkto pavadinimas
- aprašymas
- Dimensijos
- Brūkšninis kodas
- Ieškos pavadinimas

### <a name="additional-local-product-search-capabilities-conventional-sql-full-text-search"></a>Papildomos vietinės produktų ieškos galimybės (pagal SQL viso teksto iešką) 

- Atlikdami ieškas su keliais raktažodžiais (t. y., atlikdami ieškas, kuriose naudojami ieškos terminai), mažmenininkai gali sukonfigūruoti, ar į ieškos rezultatus reikia įtraukti rezultatus, atitinkančius *bet kurį* ieškos terminą, ar tik tuos rezultatus, kurie atitinka *visus* ieškos terminus. Šios funkcijos parametras pasiekiamas naujoje EKA funkcijų profilio grupėje pavadinimu **Produktų ieška**. Numatytasis parametras yra **Atitinka bet kurį ieškos terminą**. Šis parametras taip pat yra rekomenduojamas parametras. Kai naudojamas parametras **Atitinka bet kurį ieškos terminą**, kaip rezultatai pateikiami visi produktai, visiškai ar iš dalies atitinkantys vieną ar kelis ieškos terminus. Tuose rezultatuose didėjimo tvarka surikiuojami produktai su daugiausiai raktažodžių atitikčių (visiškų arba dalinių).

    Naudojant parametrą **Atitinka visus ieškos terminus**, pateikiami tik tie produktai, kurie atitinka visus ieškos terminus (visiškai arba iš dalies). Šis parametras naudingas, kai produktų pavadinimai yra ilgi ir darbuotojai ieškos rezultatuose nori matyti tik ribotą produktų skaičių. Tačiau šio tipo ieška turi du tolesnius apribojimus.

    - Ieška atliekama atskirose produktų ypatybėse. Pavyzdžiui, pateikiami tik tie produktai, kurių bent vienoje ypatybėje yra visi ieškomi raktažodžiai.
    - Dimensijose neieškoma.
> [!NOTE]
> Šios bet kurio ieškos termino konfigūracijos **Atitinka bet kurią ieškomą sąvoką**/**Atitinka visas ieškomas sąvokas** EKA funkcijos profiliuose, kurie taikomi tik **vietos** produkto paieškose (įprastose SQL viso teksto paieškoje) patirtyse. Ši konfigūracija neturi įtakos ieškai debesyje. Naujasis ieškos modulis turi nuosavą išplėstinį algoritmą, kuris ieško produkto ieškos rezultatų atitikimą. 

- Mažmenininkai dabar produktų iešką gali sukonfigūruoti taip, kad, vartotojams vedant produktų pavadinimus, būtų rodomi ieškos pasiūlymai. Naujas šios funkcijos parametras pasiekiamas EKA funkcijų profilio grupėje pavadinimu **Produktų ieška**. Parametro pavadinimas yra **Vedant tekstą rodyti ieškos pasiūlymus**. Ši funkcija darbuotojams gali padėti greitai rasti ieškomą produktą, nes jiems nereikia rankiniu būdu įvesti viso pavadinimo.
- Produktų ieškos algoritmas ieškomų terminų dabar taip pat ieško produkto ypatybėje **Ieškos pavadinimas**.

![Produkto pasiūlymai.](./media/Productsuggestions.png "Produkto pasiūlymai")

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

Kliento ID nerodomas klientas, apie kuriuos užklausą pateikė juridiniai asmenys, nes kliento ID sukurtas tik toms šalims, esančioms dabartinėje įmonėje. Tačiau, jei darbuotojas atidaro kliento informacijos puslapį, sistema automatiškai sugeneruoja šalies kliento ID ir su klientu susieja parduotuvės klientų adresų knygeles. Todėl klientas bus matomas vėliau atliekamose vietinėse parduotuvių ieškose.

![Bendra klientų paieška.](./media/Globalcustomersearch.png "Bendra klientų paieška")

### <a name="additional-local-customer-search-capabilities"></a>Papildomos vietinės klientų ieškos galimybės

Kai naudotojas ieško telefono numerio, sistema ignoruoja specialius ženklus (pavyzdžiui, tarpus, brūkšnelius ir skliaustus), kurie galėjo būti pridėti kliento kūrimo metu. Todėl informacijos ieškantiems kasininkams nereikia nerimauti dėl telefono numerio formato. Pavyzdžiui, jei kliento telefono numeris buvo įvestas kaip **123-456-7890**, kasininkas kliento gali ieškoti įvesdamas **1234567890** arba įvesdamas pirmuosius keletą telefono numerio skaitmenų.

> [!NOTE]
> Klientas gali turėti daugybę telefono numerių ir elektroninio pašto adresų. Kliento paieškos algoritmas taip pat ieško šiuose antriniuose elektroniniuose paštuose ir telefono numeriuose, tačiau kliento paieškos rezultatų puslapis tik rodo pirminį elektroninį paštą ir telefono numerį. Tai gali sukelti tam tikrą sąmyšį, nes grįžę kliento rezultatai nerodys ieškoto elektroninio pašto ar telefono numerio. Ateities leidimuose planuojame pagerinti kliento ieškos rezultatų ekraną, kad jis rodytų šią informaciją.

Įprastinė kliento ieška gali užimti daug laiko, nes ji vykdoma daugelyje laukų. Vietoj to kasininkai gali ieškoti vieno kliento ypatybės, pvz., vardo ir pavardės, el. pašto adreso arba telefono numerio. Kliento ieškos algoritmo naudojamos ypatybės kartu vadinamos *kliento ieškos kriterijais*. Sistemos administratorius gali lengvai sukonfigūruoti vieną arba kelis kriterijus kaip nuorodas, kurios bus rodomos EKA. Kadangi ieška apribojama iki vieno kriterijaus, rodomi tik tinkami ieškos rezultatai ir efektyvumas yra daug didesnis nei įprastos kliento ieškos efektyvumas. Toliau nurodytame paveikslėlyje pavaizduotos EKA kliento ieškos nuorodos.

![Klientų paieškos nuorodos.](./media/SearchShortcutsPOS.png "Klientų paieškos nuorodos")

Norėdamas nustatyti paieškos kriterijus kaip nuorodas, administratorius turi atidaryti puslapį **„Commerce“ parametrai**, esantį „Commerce“, o tada skirtuke **EKA paieškos kriterijai** pasirinkti visus kriterijus, kurie turėtų būti rodomi kaip nuorodos.

![Paieškos nuorodų konfigūravimas.](./media/ConfigureShortcutsAX.png "Paieškos nuorodų konfigūravimas")

> [!NOTE]
> Jei įtrauksite per daug nuorodų, EKA ieškos juostos išplečiamasis meniu bus perpildytas ir darbuotojui gali būti sunkiau ieškoti informacijos. Rekomenduojame įtraukti tik tiek nuorodų, kaip jums reikia.

Lauke **Rodymo tvarka** laukas nurodoma tvarka, kuria nuorodos rodomos EKA. Rodomi kriterijai yra paruoštos naudoti ypatybės, kurias kliento ieškos algoritmas naudoja klientams ieškoti. Tačiau partneriai kaip ieškos nuorodas gali įtraukti pasirinktinių ypatybių. Norėdamas kaip ieškos nuorodas įtraukti pasirinktinių ypatybių, sistemos administratorius turi išplėsti išplečiamąjį išvardijimą (išvardijimas), kuris naudojamas kliento ieškos kriterijams nustatyti, ir tada pažymėti partnerio pasirinktines ypatybes kaip nuorodas. Partneriai yra atsakingi už kodą rašymą rezultatams rasti, kai ieškose naudojamos jų pasirinktinės nuorodos.

Jei norite, kad nuorodos būtų atvaizduotos EKA, reikia sparčiųjų klavišų vertimo. Jei jūsų kanalo kalba skiriasi nuo sistemos numatytosios kalbos, turite nustatyti kiekvienos nuorodos vertimą į numatomą kalbą. Vertimus galite nustatyti pasirinkdami Versti **kiekvienai** nuorodai. 

> [!NOTE]
> Į išvardijimą įtraukta pasirinktinė ypatybė, neturi įtakos standartiniam klientų ieškos algoritmui. Kitaip tariant, klientų ieškos algoritmas neieškos pasirinktinėje ypatybėje. Vartotojai ieškodami gali naudoti pasirinktines ypatybes tik jei tos pasirinktinės ypatybės yra įtrauktos kaip nuorodos arba jei numatytasis ieškos algoritmas yra perrašytas.

Mažmenininkai taip pat gali nustatyti numatytąjį kliento ieškos režimą EKA kaip **Ieškoti visose parduotuvėse**. Ši konfigūracija gali būti naudinga scenarijuose, kuriuose būtina nedelsiant rasti už EKA ribų sukurtus klientus (pvz., net prieš vykdant paskirstymo užduotį). Norėdami tai padaryti, mažmenininkas turi įjungti parinktį **Numatytasis kliento ieškos režimas** EKA funkcijų šablone. Kai ji nustatyta į **Taip** kiekvienas kliento mėginimas sukurs skambutį realiuoju laiku į būstinę.

Siekiant išvengti nenumatytų funkcionalumo problemų, ši konfigūracija paslėpta už versijos vėliavėlės, kurios pavadinimas **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. Todėl norėdamas, kad vartotojo sąsajoje (UI) būtų rodoma nuostata **Numatytasis kliento ieškos režimas**, pardavėjas turi sukurti palaikymo bilietą vartotojo priėmimo bandymui (UAT) ir gamybos aplinkas. Gavusi bilietą inžinierių komanda dirba su pardavėju, kad įsitikintų, jog pardavėjas bandymą atlieka ne gamybos aplinkose, kad įvertintų efektyvumą ir įdiegtų visus reikiamus optimizavimus.

## <a name="cloud-powered-customer-search"></a>Debesija paremta kliento paieška

Klientų ieškos galimybės viešoji peržiūra naudojant „Azure Cognitive Search” pridėta į naujus „Commerce 10.0.18” leidimo funkcionalumus. Be našumo patobulinimų, paslaugos vartotojams taip pat pravers raiškiosios kokybės patobulinimas ir pagerintos ryšio galimybės. Našumo patobulinimai ypač matomi, kai naudojama EKA visuotinės ieškos funkcija („Ieškoti visų parduotuvėse”). Taip yra todėl, kad ieškos rezultatai surenkami iš „Azure” ieškos indekso, o ne jų užklausa siunčiami iš „Commerce” būstinės duomenų. 

### <a name="enable-the-cloud-powered-search-feature"></a>Įjungti debesija paremtą ieškos funkciją

> [!NOTE]
> Būtina, kad „Commerce” būstinė ir „Commerce Scale Unit” būtų atnaujintos į 10.0.18 versiją. EKA atnaujinti nebūtina.

Norėdami atnaujinti debesija paremtą ieškos funkciją „Commerce” būstinę, atlikite šiuos žingsnius.

1. Eikite į **Sistemos administravimas \> Darbo sritys \> Funkcijų valdymas**.
1. Raskite ir pasirinkite **(Peržiūra) Debesija paremta kliento paieška** funkciją ir pasirinkite **Įgalinti dabar**.
1. Eikite į **Mažmeninė prekyba ir prekyba > Būstinės sąranka > Prekybos grafiko įrankis > Inicijuoti prekybos grafiko įrankį** ir pasirinkite **Gerai**, kad rodytų naują **1010_KlientoPaieška** užduotį **Paskirstymo grafikas** formoje.
1. Eikite į **Mažmeninė prekyba ir prekyba > Mažmeninė prekyba ir IT prekyba > Paskirstymo grafikas**.
1. Paleiskite **1010_KlientoPaieška** užduotį. Ši užduotis skelbia datą „Azure” ieškos indekse. Kai indekso publikavimas baigtas, užduoties būsena bus nustatyta į **Pritaikyta**.
1. Po to kai **1010_KlientoPaieška** užduoties būsena nustatyta į **Pritaikyta**, paleiskite **1110 - visuotinė konfigūracija** užduotį, kad naujai įjungtos funkcijos atnaujintumėte EKA kanalus **Funkcijų valdymas**.
1. Po to paleiskite palieskite **1010_KlientoPaieška** užduotį reguliariai intervalais, kad nusiųstumėte klientui atnaujinimus ieškos indekse.

> [!NOTE]
> Pradiniame indekso publikavime **1010_KlientoPaieška** užduotis gali užtrukti keletą valandų, kol ji bus pabaigta, kadangi ji išsiųs visus kliento įrašus į „Azure” paieškos indeksą. Vėlesni atnaujinimai gali užtrukti keletą minučių. Laikotarpiu, kai debesija paremta ieškos funkcija yra įjungta, bet indekso publikavimas dar nebaigtas, kliento ieška pagal EKA bus numatytoji pagal esamą SQL iešką. Taip užtikrinama, kad nėra trukdžių parduotuvės operacijoms.

### <a name="functional-differences-from-the-existing-search"></a>Funkciniai esamos ieškos skirtumai

Toliau pateiktame sąraše parodyta, kaip debesimi paremtos klientų ieškos funkcijos skiriasi nuo esamų ieškos funkcijų. 

- „Commerce” būstinėje sukurti ir redaguojami klientai nusiunčiami į „Azure” ieškos indeksą, kai **1010_KlientoPaieška** užduotis yra paleista. Šie atnaujinimai užtruks nuo 15 iki 20 minučių indeksui atnaujinti. EKA vartotojai galės ieškoti naujų klientų (arba ieškoti pagal atnaujintą informaciją) nuo 15 iki 20 minučių po įvykdytų atnaujinimų „Commerce” būstinėje. Jei jūsų verslo procesui reikia, kad klientai, sukurti „Commerce” būstinėje, būtų ieškomi EKA nedelsiant, tai gali būti ne jums tinkama paslauga.
- Nauji klientai, sukurti EKA, siunčiami į „Azure” ieškos indeksą iš „Commerce Scale Unit” ir nedelsdami ieškomi bet kurioje parduotuvėje. Tačiau jei „Asinchroninis” kliento kūrimo funkcija įjungta, nauji klientų įrašai nebus publikuojami „Azure” ieškos indekse iš „Commerce Scale Unit” ir nebus ieškomi iš EKA, kol kliento informacija nebus sinchronizuojama su „Commerce” būstinėje ir „Asinchroninis” klientams sukuriama klientų ID. Vėliau **1010_KlientoPaieška** užduotis galės išsiųsti „Asinchroninis” kliento įrašus į „Azure” ieškos indeksą. Vidutiniškai tai užtruks apie 30 minučių prieš tai, kai EKA bus ieškoma naujai sukurtų „Asinchroninis” klientų. Šiame apskaičiavime numatoma, kad **1010_KlientoPaieška**, **P-užduotis** ir **Sinchronizuoti klientus ir verslo partnerius iš asinchroninio režimo** užduotys ura numatytos vykdyti kas 15 minučių.
- Debesija paremta ieška taip pat ieško antrinių el. laiškų ir klientų telefonų numerių, tačiau šiuo metu klientų ieškos rezultatuose rodomas tik pirminis telefono numeris ir pirminis klientų el. pašto adresas. Iš pradžių gali atrodyti, kad pateikti neaktualūs ieškos rezultatai, tačiau antrinio kliento el. laiško ir kliento telefono numerio ieškos rezultatuose patikra gali padėti patikrinti, ar ieškomas raktažodis baigėsi klientų atitikimu. Norint išvengti tokios painiavos, planuojama patobulinti ieškos rezultatų puslapį, kad vartotojai lengviau suprastų, kodėl buvo pateikti ieškos rezultatai.
- Reikalavimas ieškoti naudojant bent 4 simbolius visuotinoje ieškoje („Ieškoti visose parduotuvėse”), netaikomas šiai paslaugai.

> [!NOTE]
> Klientų ieškos galimybė naudojant „Azure Cognitive Search” paslaugą prieinama visuose peržiūros ribotuose regionuose. Klientų ieškos galimybė *nėra* prieinama nurodytuose regionuose:
> - Brazilija
> - Indija

[!INCLUDE[footer-include](../includes/footer-banner.md)]
