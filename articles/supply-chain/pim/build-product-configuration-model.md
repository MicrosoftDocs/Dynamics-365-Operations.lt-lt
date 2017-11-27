---
title: "Produkto konfigūracijos modelio kūrimas"
description: "Įmonė-įmonei ir įmonė-vartotojui sektoriuose tampa įprasta konfigūruoti produktus, kad būtų patenkinami konkretūs poreikiai."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 75083
ms.assetid: f08072b8-cb0b-43aa-9509-f5ec32caecd9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b096f366f13406a4c80d7eccfa8f27d8f8f712e4
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="build-a-product-configuration-model"></a>Produkto konfigūracijos modelio kūrimas

[!include[banner](../includes/banner.md)]


Įmonė-įmonei ir įmonė-vartotojui sektoriuose tampa įprasta konfigūruoti produktus, kad būtų patenkinami konkretūs poreikiai.

Gamintojas, kuris palaiko konfigūracijos pagal užsakymą scenarijus, gali geriau prisitaikyti prie klientų poreikių. Be to, gamintojas, sandėliuodamas ne pagamintus produktus, o bendruosius dar iki galo nepagamintų prekių komponentus, gali sumažinti su atsargomis susieto kapitalo kiekį.  

Norint sėkmingai pereiti nuo pagamintų ir sandėliuojamų prekių sąrankos prie konfigūracijos pagal užsakymą sąrankos, būtina išsamiai išanalizuoti produktų struktūras, nustatyti produktų grupes ir komponentus. Norint sumažinti dalių skaičių bei minimaliai sumažinti gaminamų prekių skaičių, labai svarbu išsiaiškinti produktų tarpusavio ryšius bei sukurti įvairiuose produktuose naudojamas dalis.  

Taikomi keli produkto konfigūracijos modelių kūrimo principai, pvz., modeliavimas pagal taisykles, dimensijas ir apribojimus. Atlikus tyrimus nustatyta, kad taikant kūrimo pagal apribojimus metodiką galima sumažinti kodo eilučių modeliuose skaičių maždaug 50 procentų, palyginti su kitais modeliavimo principais. Taigi taikant šią metodiką galima sumažinti bendrąją nuosavybės kainą (TCO). Pakeitus pagal taisykles sukurtą modelį, kuris kuriamas X++ kodo pagrindu, į pagal apribojimus sukurtą modelį nebereikės turėti programuotojo licencijos, kad būtų galima tvarkyti produktų modelius.

## <a name="product-configuration"></a>Produkto konfigūracija
Industrializacijos laikotarpiu pasiekta, kad aukštos kokybės ir daug funkcijų turintys produktai būtų gaminami prieinamomis kainomis. Dėl masto ekonomijos daugeliui išsivysčiusiose šalyse gyvenusių žmonių tapo įmanoma įsigyti automobilius, televizorius, buitinius prietaisus ir kitas prekes, kurias daugelis žmonių laiko būtina kasdienio gyvenimo dalimi.  

Daug produktų pradėti masiškai naudoti, todėl atsirado poreikis juos modifikuoti. Gamintojai iš karto sureagavo į šį iššūkį ir sukūrė kiekvieno produkto variantų, kad klientai turėtų daugiau pasirinkimo galimybių. Taikant šią strategiją tapo sunkiau prognozuoti, padidėjo atsargų išlaidos ir neparduotų technologiškai pasenusių produktų kiekiai.  

Gamintojai, pritaikę konfigūracijos pagal užsakymą koncepciją, gali patenkinti klientų unikalių produktų poreikius bei sumažinti technologiškai pasenusių atsargų prekių kiekius arba jas visas parduoti. Pakeitus pagamintų ir sandėliuojamų prekių koncepciją į konfigūracijos pagal užsakymą koncepciją kyla iššūkis, į kurį reikia sureaguoti iš karto: trumpo gamybos laiko poreikis turi būti suderinamas su mažu atsargų lygiu.  

Norint sėkmingai įgyvendinti šį uždavinį, reikia išsamiai išanalizuoti produktų portfelį bei numatyti produktų funkcijų ir procesų modelius. Taip pat reikia nustatyti bendruosius komponentus, kuriuos galima pagaminti ta pačia įranga ir naudoti visuose variantuose.  

Naujajame funkcijų rinkinyje Produkto konfigūracija yra vartotojo sąsaja (UI), kurią naudojant galima peržiūrėti vaizdinę produkto konfigūracijos modelio struktūrą, o taikant šio rinkinio funkcijas naudojama deklaratyvioji apribojimų sintaksė, kurios nereikia kompiliuoti. Taigi įmonėms lengviau pradėti naudoti konfigūracijos modelius. Toliau esančiuose skyriuose nurodyta, kad produkto kūrėjui nebereikalinga programuotojo pagalba kuriant produkto konfigūracijos modelį, jį tikrinant ir išleidžiant pardavimo organizacijoje.

## <a name="building-a-product-configuration-model"></a>Produkto konfigūracijos modelio kūrimas
Vartotojas gali taikyti kelis metodus, skirtus produkto konfigūracijos modeliui sukurti. Galima taikyti nuoseklaus srauto metodą: pirmiausia sukuriami visi nuorodos duomenys, pvz., bendrieji produktai, išskirtieji produktai ar veiklos ištekliai, tada jie įtraukiami kaip komponentai, komplektavimo specifikacijos (KS) eilutės, maršruto operacijos ar kaip kiti produkto konfigūracijos modelio elementai. Be to, galima pasirinkti populiaresnį metodą, kuomet pirmiausia sukuriamas modelis, o prireikus įtraukiami nuorodos duomenys.

### <a name="components"></a>Komponentai

Produkto konfigūracijos modelį sudaro vienas ar keli komponentai, tarpusavyje susieti subkomponentų ryšiais. Komponentai apibrėžiami vieną kartą, o tada juos galima naudoti daug kartų viename arba keliuose produkto konfigūracijos modeliuose. Komponentai yra pagrindiniai kuriami produkto konfigūracijos modelio elementai ir su jais susieta beveik visa informacija apie modelį.

### <a name="attributes"></a>Atributai

Kiekviename komponente naudojamas bent vienas jo ypatybes nustatantis atributas. Atributai – tai vartotojų per konfigūravimo procesą pasirenkami elementai. Naudojant atributus valdomi ryšiai tarp komponentų ir vidiniai komponento ryšiai, kurie įtraukiami į apribojimus arba apskaičiavimus. Pagal KS eilutėms taikomas sąlygas atributus galima naudoti faktinėms dalims, iš kurių bus sudarytas sukonfigūruotas produktas, nustatyti. Be to, naudojant atributą ir susiejimo mechanizmą galima valdyti KS eilutės ypatybę. Panašios su įtraukimo ir ypatybių parametrais susijusios funkcijos taikomos maršruto operacijoms.

### <a name="expression-constraints"></a>Išraiškos apribojimai

Kai vartotojas naudoja pagal apribojimus sukurtą produkto konfigūracijos modelį ir renkasi įvairių atributų reikšmes, taikomi tam tikri apribojimai. Šie apribojimai gali būti įvykdomi kaip išraiškos apribojimai naudojant optimizuoto modeliavimo kalbą (OML). Be to, apribojimą galima įvykdyti kaip lentelės apribojimą.

### <a name="table-constraints"></a>Lentelės apribojimai

Lentelės apribojimai gali būti nustatomi vartotojo arba apibrėžtos sistemos.  

Vartotojas pats sukuria vartotojo apibrėžiamą lentelės apribojimą. Vartotojas, pasirinkęs įvairių tipų atributus, sudaro lentelės stulpelius, tada, įvedęs pasirinktų tipų atributų domenų reikšmes, sudaro lentelės apribojimo eilutes.  

Sistemoje apibrėžiamas lentelės apribojimas nustatomas tokia tvarka: pasirenkama kaip nuoroda naudotina „Microsoft Dynamics 365 for Finance and Operations“ lentelė, tada pasirinkus šios lentelės laukus sudaromi apribojimo stulpeliai. Lentelės apribojimo eilutės – tai konfigūruojant esančios „Finance and Operations“ lentelės eilutės.  

Lentelės apribojimas įtraukiamas į produkto konfigūracijos modelį nurodžius lentelės apribojimo aprašą ir susiejus atitinkamus modelio atributus su lentelės apribojimo stulpeliais.

### <a name="calculations"></a>Skaičiavimai

Skaičiavimai atitinka mechanizmą, skirtą aritmetinėms operacijoms konfigūracijos modelyje atlikti. Pavyzdžiui, naudojant skaičiavimą galima nustatyti konkrečios žaliavos ilgį arba poliravimo operacijos vykdymo laiką. Skaičiavimus būtina naudoti, o juos taikant nustatoma paskirties atributo reikšmė, kai jau galima naudoti visas į skaičiavimo išraišką įtrauktas atributo reikšmes.

### <a name="subcomponents"></a>Subkomponentai

Subkomponentai nurodo produkto konfigūracijos modelio struktūros mazgus. Kiekvieno subkomponento ryšys turi būti nurodomas su bendruoju produktu, kurio variantų konfigūravimo technologijos reikšmė nustatyta kaip konfigūravimas pagal apribojimus.

### <a name="user-requirements"></a>Vartotojo reikalavimai

Vartotojo reikalavimą sudaro visi sudedamieji subkomponento elementai. Vienintelis skirtumas – vartotojo reikalavimas nesusietas su bendruoju produktu. Praktinė šio skirtumo reikšmė – bet kurios kuriant vartotojo reikalavimą apibrėžiamos KS eilutės arba maršruto operacijos sutraukiamos į pirminę komponentų KS struktūrą arba maršrutą. Fiktyvios KS veikimo principas panašus.

### <a name="bom-lines"></a>KS eilutės

KS eilutės yra įtraukiamos, kad būtų identifikuota kiekvieno komponento gamybos KS. KS eilutėje turi būti nurodyta prekė, o visų prekės ypatybių reikšmė gali būti nustatyta fiksuota arba šios ypatybės gali būti susietos su atributu.

### <a name="route-operations"></a>Maršruto operacijos

Maršruto operacijos yra įtraukiamos, kad būtų identifikuotas gamybos maršrutas. Maršruto operacijoje turi būti nurodyta apibrėžta operacija, o visų operacijos ypatybių reikšmė gali būti nustatyta fiksuota. Visas ypatybes, išskyrus išteklių reikalavimus, galima susieti su atributu ir nesusieti su reikšme.

## <a name="validating-and-testing-a-product-configuration-model"></a>Produkto konfigūracijos modelio tikrinimas
Produkto konfigūracijos modelį galima tikrinti keliais etapais, kurių mastai skiriasi. Vienos išraiškos apribojimo tikrinimo etapas yra paprasčiausias. Šiuo atveju dažniausiai produkto kūrėjas tikrina išraiškos sintaksės teisingumą.  

Atskirai galima patikrinti ir KS eilutės arba maršruto operacijos sąlygą.  

Taip pat galima tikrinti vartotojo apibrėžtų lentelės apribojimų aprašą. Tokiu atveju vartotojas gali patikrinti, ar kiekviename lauke įvestos reikšmės yra atitinkamų tipų atributų domene.  

Galiausiai galima patikrinti visą produkto konfigūracijos modelį bei visos sintaksės teisingumą ir visų vardų suteikimo ir modeliavimo taisyklių laikymąsi.

### <a name="testing"></a>Tikrinimas

Modelio tikrinimo procesas primena faktinio konfigūravimo seanso vykdymą. Vartotojas gali peržiūrėti konfigūracijos puslapius ir patikrinti, ar taikant modelio struktūrą konfigūravimo procesas yra galimas. Vartotojas gali patikrinti, ar atributų reikšmės teisingos, ir ar vartotojas, vadovaudamasis atributų aprašais, pasirinks teisingas reikšmes. Galiausiai užbaigus tikrinimo seansą sistemoje bandoma sukurti pasirinktas atributų reikšmes atitinkančią KS ir maršrutą, o įvykus klaidai pateikiamas klaidos pranešimas.

### <a name="the-configuration-page"></a>Konfigūracijos puslapis

Norėdami pereiti nuo vieno komponento prie kito, spustelėkite **Kitas** arba produkto konfigūracijos modelio medyje spustelėkite komponentą, kad jį atidarytumėte.

## <a name="finalizing-a-model-for-configuration"></a>Konfigūracijos modelio užbaigimas
Kai produkto konfigūracijos modelis paruoštas naudoti su konfigūracijos pagal užsakymą scenarijais, būtina sukurti versiją. Tačiau galima naudoti kelias modelių kūrimą palengvinančias parinktis.

### <a name="user-interface"></a>Vartotojo sąsaja

Galima modifikuoti konfigūravimo vartotojo sąsają į vieną arba kelis subkomponentus įtraukiant atributų grupes. Naudojant šias grupes galima pabrėžti konkrečių atributų ryšius, o konfigūracijos vartotojas galės lengviau nustatyti peržiūrimo produkto sritį.

### <a name="templates"></a>Šablonai

Norint pagreitinti konfigūravimo procesą, galima sukurti vieną ar kelis konfigūracijos šablonus. Be to, šablonus galima sukurti, norint reklamuoti konkrečius atributų derinius, pvz., kai pardavimo kampanijoje didžiausias dėmesys skiriamas konkrečiam produkto funkcijų rinkiniui.

### <a name="translations"></a>Vertimai

Jei produktas bus parduodamas įvairiose šalyse / regionuose, galima išversti visą konfigūravimo vartotojo sąsajoje rodomą tekstą. Šiame tekste bus nurodytos ne tik pavadinimo ir aprašo laukų, tačiau ir atributų teksto reikšmės.

### <a name="versions"></a>Versijos

Paskutinis ir svarbiausias užbaigimo proceso veiksmas – produkto konfigūracijos modelio versijos sukūrimas. Versija nurodo bendrojo produkto, kurį užsakymo arba pasiūlymo eilutėje galima pasirinkti su konfigūracijos modeliu, ir produkto konfigūracijos modelio ryšį. Versija turi būti patvirtinta ir suaktyvinta, kad ją būtų galima naudoti per konfigūravimo seansą.

## <a name="extending-a-product-configuration-model-through-the-api"></a>Produkto konfigūracijos modelio išplėtimas naudojant API
Kad partneriai ir kiti programuotojo licenciją turintys asmenys galėtų išplėsti produkto konfigūracijos modelio galimybes, buvo įdiegta skirtoji programų programavimo sąsaja (API). Buvo iškeltas pagrindinis tikslas sukurti mechanizmą, kurį taikydami partneriai ir esamą produktų generatorių naudojantys klientai galėtų įdėtąjį produktų generatoriaus modelių kodą perkelti į API. Tokiu būdu jie gali perkelti modelius iš produktų generatoriaus į produkto konfigūracijos modelį. Tačiau nauji partneriai ir klientai taip pat gali naudodami API išplėsti naujus produkto konfigūracijos modelius.

### <a name="pcadaptor-class"></a>„PCAdaptor“ klasė

API įdiegiama naudojant produkto konfigūracijos modelių duomenų struktūrą nurodančių **PCAdaptor** klasių rinkinį. **PCAdaptor** klasės egzempliorius turi būti sukurtas su visais išplečiamais modeliais. Užbaigus konfigūravimo seansą, sistemoje tikrinama, ar yra šios klasės egzempliorius, kuris bus paleidžiamas, jei bus surastas.  

Toliau pateiktoje struktūrinėje schemoje apibūdintas procesas.  

[![Struktūrinė schema](./media/product_configuration_2.png)](./media/product_configuration_2.png)  

Produkto konfigūracijos API struktūrinė schema

## <a name="product-configuration"></a>Produkto konfigūracija
Produkto konfigūravimo procesą galima atlikti toliau pateiktose vietose.

-   Pardavimo užsakymo eilutė
-   Pardavimo pasiūlymo eilutė
-   Pirkimo užsakymo eilutė
-   Gamybos užsakymo eilutė
-   Prekės poreikio eilutė (projektas)

Vykdant konfigūravimo procesą siekiama sukurti išskirtąjį produkto variantą, kuris atitiktų kliento poreikius. Sukuriamas unikalus kiekvienos naujos konfigūracijos ID. Naudojant šį ID sekamos atsargos.

### <a name="multiple-sites-and-intercompany"></a>Kelios vietos ir vidinė įmonė

Jei konfigūravimo procesas bus vykdomas ne gamybos vietoje ar įmonėje, KS ir maršrutas bus sukurti ir naudojami tiekėjo įmonės vietoje. Produkto variantas bus išleistas visose tiekimo grandinės įmonėse.




