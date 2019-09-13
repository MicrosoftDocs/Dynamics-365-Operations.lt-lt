---
title: Įrašyti rodiniai
description: Šioje temoje aprašoma, kaip naudotis įrašytų rodinių funkcijomis.
author: jasongre
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 43f25796e6271f14acfc72f931398ab63338a307
ms.sourcegitcommit: b068b17ef708a0b349db8df1542e4244bb983d13
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2019
ms.locfileid: "1870838"
---
# <a name="saved-views"></a>Įrašyti rodiniai

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Įžanga
Personalizavimas atlieka svarbų vaidmenį, kadangi vartotojai ir organizacijos gali pagal savo poreikius optimizuoti „Microsoft Dynamics 365 for Finance and Operations“ vartotojo patirtį. Daugiau informacijos apie personalizavimą žr. [Vartotojo patirties personalizavimas](personalize-user-experience.md).

Naudodami įprastą personalizavimą vartotojai gali turėti tik vieną vienos formos personalizavimų rinkinį. Naudojantis įrašytais rodiniais personalizavimas išplečiamas keliais svarbiais būdais.

-    Naudodamiesi rodiniais vartotojai gali turėti kelis pavadintus vienos formos personalizavimo rinkinius ir greitai įjungti reikiamą bet kurį iš jų. Taigi vartotojas gali sukurti kelis optimizuotus puslapio rodinius, kad kiekvienas rodinys būtų pritaikytas konkrečioms verslo užduotims atlikti. 

-    Tam tikro tipo puslapiams sukurti rodiniai taip pat gali apimti vartotojo įtrauktus filtrus arba rūšiavimus, kuriais naudodamiesi vartotojai gali greitai grįžti į dažniausiai filtruotus duomenų rinkinius. Daugiau informacijos ieškokite skyriuje [Kurie puslapiai palaiko rodinius](saved-views.md#what-pages-support-views). 

-    Rodinius galima publikuoti saugos vaidmenyse, o tai reiškia, kad kiekvienas tam tikrą vaidmenį turintis vartotojas galės pasiekti ir naudoti tam tikrą rodinį, nepriklausomai nuo to, ką vartotojas gali personalizuoti. Naudodamosi šia publikavimo galimybe organizacijos gali apibrėžti standartinius savo verslui optimizuotus įmonės rodinius. Daugiau informacijos ieškokite skyriuje [Personalizavimų valdymas organizacijos lygiu naudojant rodinius](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).

-    Kitaip nei įprasto personalizavimo atveju, rodiniai automatiškai neįrašomi vartotojui atliekant tiesioginius personalizavimus ar filtruojant sąrašą. Aiškiai įrašyti reikia tam, kad būtų užtikrintas lankstumas kuriant rodinį prieš atliekant su tokiu rodiniu susijusius pakeitimus arba po jų ir netyčia nebūtų pakeisti rodinio apibrėžimai naudojant filtrus ar personalizavimus, kurie nėra skirti ilgalaikiam naudojimui.  

## <a name="switching-between-views"></a>Rodinių perjungimas
Įgalinus rodinių naudojimą tam tikroje aplinkoje, bet kuriame rodinius palaikančio puslapio formos, kurioje rodomas dabartinio rodinio pavadinimas, viršuje pateikiamas sutrauktų rodinių išrinkiklio valdiklis.  

Rodinių išrinkiklių esama dviejų dydžių. 

-   **Dideli rodinių išrinkikliai**: puslapių, kuriuose aiškiai esama sąrašo, rodinių išrinkiklis bus didesnis dėl kelių priežasčių. Svarbiausia nepamiršti, kad didesnis rodinių išrinkiklis reiškia tai, kad puslapių rodiniai gali apimti vartotojo nustatytus filtrus. Kadangi į rodinius įtraukti filtrai, didesnio dydžio išrinkiklis reikalingas ir todėl, kad rodinio pavadinimai dažnai yra geriausias ekrane rodomų duomenų aprašymas ir tikimasi, kad šio tipo puslapiuose vartotojai dažniau perjungs rodinius.  
 
-   **Mažo rodinio išrinkikliai**: visose kitose viso puslapio formose (išskyrus darbo sritis ir informacijos suvestinę) yra mažesnis rodmenų parinkiklis, rodomas šalia puslapio antraštės. Šių puslapių rodiniai apima tik personalizavimus (o ne vartotojo nustatytus filtrus). Šiuose puslapiuose formos antraštė arba įrašo pavadinimas dažnai yra svarbiausia informacija, esanti formos viršuje. Mažesnis dydis taip pat reiškia mažesnį tikėtiną šių puslapių rodinių perjungimo dažnumą. 
 
Spustelėjus rodinio pavadinimą, atidaromas rodinių išrinkiklis ir rodomas galimų šio puslapio rodinių sąrašas

-    **Klasikinis rodinys**: tai parengtas naudoti puslapio rodinys, kai netaikomi jokie tiesioginiai personalizavimai.  
-    **Asmeniniai rodiniai**: rodiniai be spynų yra jūsų asmeniniai rodiniai. Tai jūsų sukurti arba administratoriaus jums suteikti rodiniai.  
-    **Užrakinti rodiniai**: išrinkiklyje šalia kai kurių rodinių (pvz., klasikinio rodinio ir visų jūsų vaidmeniui publikuotų rodinių) rodoma spyna, o tai reiškia, kad šių rodinių redaguoti negalite. Tačiau automatiškai įrašomi netiesioginiai puslapio naudojimo personalizavimai, pvz., keičiant tinklelio stulpelio plotį arba išplečiant arba sutraukiant „FastTab“. Tačiau, jei turite personalizavimo teises, atlikdami veiksmą **Įrašyti kopiją** pagal užrakintą rodinį galite sukurti asmeninį rodinį.
-    **Nauji rodiniai**: publikuotų, bet dar neatidarytų rodinių pavadinimo kairėje pusėje vaizduojama kibirkštis.  

Norėdami perjungti kitą rodinį, pirmiausia atidarykite rodinių išrinkiklį ir pasirinkite norimą įkelti rodinį. 

## <a name="creating-and-modifying-views"></a>Rodinių kūrimas ir modifikavimas
Kitaip nei įprasto personalizavimo atveju, rodiniai automatiškai neįrašomi vartotojui atliekant tiesioginius personalizavimus (ar filtruojant sąrašą). Norint išsaugoti šiuos rodinio pakeitimus, reikia atlikti akivaizdų veiksmą. Taip užtikrinamas vartotojo lankstumas kuriant rodinį prieš atliekant su tokiu rodiniu susijusius pakeitimus arba po jų, taip pat užtikrinama, kad netyčia nebūtų pakeisti rodinio apibrėžimai naudojant vienkartinius filtrus ar personalizavimus. Atkreipkite dėmesį, kad netiesioginiai personalizavimai (pvz., „FastTab“ išplėtimas arba sutraukimas arba tinklelio stulpelio pločio keitimas) automatiškai įrašomi į dabartinį rodinį net ir užrakintus rodinius. 

Siekiant užtikrinti, kad būtų žinoma dabartinė rodinio būsena, pradedant atlikti rodinio pakeitimus, atliekant tiesioginį personalizavimą arba filtravimą, šalia dabartinio rodinio pavadinimo rodoma žvaigždutė, o tai reiškia, kad rodomas neįrašytas, modifikuotas rodinys.

Norėdami įrašyti šiuos pakeitimus, atlikite toliau nurodytus veiksmus.
1.  Pasirinkę rodinio pavadinimą atidarykite rodinių išrinkiklį.
2.  Norėdami modifikuoti esamą rodinį, atlikite toliau nurodytą veiksmą.
     1. Pasirinkite **Įrašyti**. Atkreipkite dėmesį, kad šio veiksmo negalima atlikti užrakintiems rodiniams. 
3.  Norėdami sukurti naują rodinį, atlikite toliau nurodytus veiksmus.
     1.    Pasirinkite **Įrašyti kopiją**. 
     2.    Įveskite rodinio pavadinimą ir aprašą (nebūtinai).
     3.    Pasirinkite **Įrašyti**.

## <a name="changing-the-default-view"></a>Numatytojo rodinio keitimas
Numatytasis rodinys yra rodinys, kurį sistema bandys atidaryti, kai pirmą kartą pereisite į puslapį. Turėtumėte nustatyti, kad tai būtų rodinys, kurį tikitės naudoti dažnai.  

Norėdami pakeisti puslapio numatytąjį rodinį, atlikite tolesnius veiksmus. 
1.  Įjunkite rodinį, kuris naudojamas kaip numatytasis. 
2.  Pasirinkę rodinio pavadinimą atidarykite rodinių išrinkiklį. 
3.  Pasirinkite **Daugiau**, o paskui – **Prisegti kaip numatytąjį**.  

Arba sukūrę naują rodinį (naudodamiesi veiksmu **Įrašyti kopiją**) galite nustatyti, kad naujas rodinys būtų numatytasis rodinys, t. y. prieš įrašydami rodinį pasirinkti parinktį **Prisegti kaip numatytąjį**.  

Atkreipkite dėmesį, kad kai kuriais atvejais su numatytuoju rodiniu susieta užklausa nevykdoma į puslapį perėjus pirmą kartą. Pavyzdžiui, perėjus į puslapį naudojantis plytele, plytelės užklausa bus vykdoma neatsižvelgiant į su numatytuoju rodiniu susietą užklausą. Taip pat jei perėjus į puslapį, kurio klasikiniame rodinyje jau nurodyta užklausa, iš pradžių bus vykdoma ne numatytojo rodinio užklausa, o pradinė užklausa. Taip nutikus, įkeliant rodinį rodomas įspėjantis informacinis pranešimas. Perjungus rodinius, kai puslapis įkeltas, rodinio užklausą turėtų būti leidžiama vykdyti kaip numatyta.

## <a name="managing-personal-views"></a>Asmeninių rodinių valdymas 
Dialogo lange **Valdyti mano rodinius** suteikiama galimybė atlikti pagrindinę asmeninių rodinių priežiūrą ir nurodyti rodinių tvarką rodinių išrinkiklyje. Norėdami atidaryti šį puslapį, spustelėkite rodinio pavadinimą, norėdami atidaryti rodinių išrinkiklio išplečiamąjį meniu, pasirinkite **Daugiau**, o paskui – **Valdyti mano rodinius**.  

Toliau išvardyti su galimų to puslapio rodinių sąrašu galimi atlikti veiksmai.  
-    **Pakeisti numatytąjį rodinį**: atlikus veiksmą **Prisegti kaip numatytąjį** šiuo metu paryškintas rodinys tampa numatytuoju šio puslapio rodiniu.  
-    **Keisti rodinių tvarką**: atlikus veiksmus **Perkelti aukštyn** ir **Perkelti žemyn** rodiniai pertvarkomi tam tikra tvarka.  
-    **Pervardyti rodinį**: atlikus veiksmą **Pervardyti** pakeičiamas šiuo metu paryškinto asmeninio rodinio pavadinimas. Šis veiksmas išjungtas užrakintiems rodiniams. 
-    **Panaikinti rodinį**: atlikus veiksmą **Pašalinti** šiuo metu paryškintas rodinys visam laikui panaikinamas iš puslapio. Pašalinus rodinį, nėra jokių galimybių jį atkurti.  

Visi šiame dialogo lange atlikti pakeitimai įsigalios pasirinkus mygtuką **Įrašyti**.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Personalizavimų valdymas organizacijos lygiu naudojant rodinius
Norėdami suprasti personalizavimų organizacijos lygiu valdymo patobulinimus, pirmiausia peržvelkite, kaip personalizavimas buvo valdomas, kol rodinių nebuvo.  

Kai rodinių nebuvo, administratoriai taikydavo puslapio personalizavimų rinkinį vartotojui, vartotojų grupei arba personalizavimo formą naudojantiems vartotojams. Jei tie vartotojai turėjo personalizavimo teises, personalizavimai būdavo taikomi tam puslapiui. Tačiau nepavyko išvengti tolesnio vartotojų atliekamo puslapio personalizavimo, o tai reiškė, kad organizacija negalėjo užtikrinti, kad jos vartotojai turi nuoseklią vartotojo sąsają. Jei kuris nors iš vartotojų neturėdavo personalizavimo teisių, administratoriaus jiems suteikti personalizavimai nebūdavo įkeliami. Taip pat, jei organizacija pasamdydavo naujų vartotojų, administratoriai turėdavo patys įkelti vartotojui skirtą personalizavimų rinkinį. Nebūdavo automatinio mechanizmo, kuris nurodytų, kai esama tam tikro vartotojui skirto personalizavimų rinkinio.

Naudojant įrašytų rodinių funkciją, organizacijos personalizavimų valdymas daug paprastesnis, pirmiausia dėl galimybės publikuoti rodinius saugos vaidmenims. Kai rodinys publikuojamas, kiekvienas tam tikrą vaidmenį turintis vartotojas gali pasiekti ir naudoti tam tikrą rodinį, nepriklausomai nuo to, ką vartotojas gali personalizuoti. Nors kiekvienas vartotojas turi publikuoto rodinio, kuriame automatiškai taikomas puslapio naudojimas (numanomi personalizavimai), kopiją, nė vienas vartotojas negali įrašyti tiesioginių personalizavimų ar užklausos naujinių į publikuotą rodinį (tai reiškia, kad publikuoti rodiniai užrakinti). Be to, jei naujiems vartotojams suteikiamas vaidmuo, kuriam rodinys buvo publikuotas, jie automatiškai matys su savo vaidmenimis susijusius rodinius, administratoriui neatliekant jokio veiksmo. Taip pat vartotojui pakeitus organizacijoje atliekamus vaidmenis, su senu vaidmeniu susieti rodiniai administratoriui neatliekant jokių veiksmų jam bus nebepasiekiami. Publikuoto rodinio naujinius paprasta išplatinti vartotojams iš naujo publikuojant rodinį atitinkamiems saugos vaidmenims.

Naudodamosi publikavimo galimybe organizacijos gali apibrėžti standartinius savo verslui optimizuotus įmonės rodinius, skirtus konkrečius saugos vaidmenis turintiems vartotojams.  

## <a name="publishing-views"></a>Rodinių publikavimas
Publikavimo proceso metu rodiniams galima priskirti vieną ar kelis saugos vaidmenis, o tai reiškia, kad visi tą vaidmenį turintys vartotojai turės prieigą prie to rodinio ir galės juo naudotis, nors rodinio redaguoti negalės. Šiuo metu tik sistemos administratoriai turi teisę atlikti rodinio išrinkiklio išplečiamojo meniu veiksmą **Publikuoti**, tačiau naujas saugos vaidmuo, kuriuo publikavimo teisės galės būti suteikiamos kitiems patikrintiems vartotojams, bus pridėtas būsimame atnaujinime.  

Norėdami publikuoti rodinį, atlikite toliau nurodytus veiksmus. 
1.  Sukurkite ir įrašykite norimo publikuoti rodinio asmeninę kopiją. 
2.  Jei tas rodinys šiuo metu įkeltas, pasirinkę rodinio pavadinimą atidarykite rodinių išrinkiklio išplečiamąjį meniu. 
3.  Pasirinkite mygtuką **Daugiau**, o paskui pasirinkite **Publikuoti**. Atsidarys publikavimo dialogo langas.  
4.  Nurodykite naujojo rodinio pavadinimą ir aprašą (nebūtinai). Tai pavadinimas, kurį vartotojai, gaunantys šį rodinį, matys savo rodinių išrinkikliuose. Atkreipkite dėmesį, kad publikuotų puslapio rodinių pavadinimai negali kartotis, net jei skiriasi jiems taikomų vaidmenų sąrašas.  
5.  Pridėkite visus šį rodinį gaunantiems vartotojams taikomus saugos vaidmenis.  
6.  Pasirinkite **Publikuoti**.

Atkreipkite dėmesį, kad kai kuriose aplinkose gali šiek tiek užtrukti (iki valandos), kol vartotojai pamatys publikuotą rodinį.

## <a name="modifying-a-published-view"></a>Publikuoto rodinio modifikavimas
Kai rodinys jau publikuojamas, gali būti, kad norite keisti publikuotą rodinį. Nors negalite atlikti tiesioginių publikuoto rodinio keitimų, nes visiems vartotojams (taip pat leidėjams) šių rodinių redagavimo funkcija užrakinta, galite iš naujo publikuoti rodinį, kad būtų galima jį atnaujinti.  

Jeigu publikuotam rodiniui norimi atlikti pakeitimai apima tik publikavimo parametrus (rodinio pavadinimą ir aprašą arba saugos vaidmenis, kuriems rodinys publikuojamas), atlikite toliau nurodytus veiksmus. 
1.  Įjunkite norimų atnaujinti parametrų publikuotą rodinį. 
2.  Rodinio išrinkiklio išplečiamajame meniu pasirinkite **Publikuoti**. 
3.  Pasirinkite **Taip**, jei norite atnaujinti esamą rodinį (arba **Ne**, jei norite jį publikuoti kitu pavadinimu).
4.  Atnaujinkite rodinio pavadinimą, aprašą ir (arba) saugos vaidmenis. 
5.  Pasirinkite **Publikuoti**. 
6.  Jei atnaujinote publikuoto rodinio pavadinimą, taip pat turite panaikinti publikuotą rodinį senu pavadinimu (daugiau informacijos žr. skyriuje **Publikuotų rodinių valdymas**). 

Jeigu publikuoto rodinio pakeitimai apima su rodiniu susietų personalizavimų ar filtrų modifikavimą, atlikite toliau nurodytus veiksmus. 
1.  Įjunkite norimą modifikuoti publikuotą rodinį. 
2.  Įrašyti publikuoto rodinio kopiją, kad būtų galima sukurti vietinį publikuoto rodinio juodraštį. 
3.  Modifikuokite vietinį juodraštį atlikdami reikiamus pakeitimus.
4.  Publikuokite rodinį nurodydami pradinį pavadinimą. 

## <a name="managing-published-views"></a>Publikuotų rodinių valdymas
Kaip ir valdant asmeninius rodinius, dialogo lange **Valdyti mano rodinius** vartotojams, turintiems publikavimo teisę, suteikiama galimybė atlikti pagrindinę publikuotų to puslapio rodinių (taip pat savo asmeninių rodinių) priežiūrą. Norėdami atidaryti šį puslapį, pasirinkite rodinio pavadinimą, norėdami atidaryti rodinių išrinkiklio išplečiamąjį meniu, pasirinkite **Daugiau**, o paskui – **Valdyti mano rodinius**.

Nors visi vartotojai mato skirtuką **Mano rodiniai**, kuriame rodomi jų asmeniniai rodiniai, publikavimo teises turintys vartotojai taip pat mato skirtuką **Publikuota**, kuriame rodomi visi publikuoti to puslapio rodiniai. Kadangi rodinius gali publikuoti keli vartotojai, svarbu galėti valdyti visą publikuotų rodinių sąrašą, nepriklausomai nuo to, ar esate faktiškai rodinį publikavęs vartotojas.

Toliau išvardyti su visų publikuotų puslapio rodinių sąrašu galimi atlikti veiksmai. 

-    **Publikuoti**: veiksmą **Publikuoti** naudokite norėdami iš naujo publikuoti rodinį su modifikuotais publikavimo parametrais (pavadinimas, aprašas, saugos vaidmenys).  
-    **Pašalinti**: veiksmą **Pašalinti** naudokite norėdami negrįžtamai panaikinti publikuotą rodinį. Šiuo veiksmu pašalinamas visų sistemos vartotojų rodinys.  
 
Visi šiame dialogo lange atlikti pakeitimai įsigalios pasirinkus mygtuką **Įrašyti**.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Kaip įgalinti įrašytus rodinius mano aplinkoje? 
Norėdami aktyvuoti įrašytus rodinius, kai funkcija veikia peržiūros režimu, atlikite toliau nurodytus veiksmus: 

1.  **Įgalinti testuojamą variantą**: vykdykite šį SQL teiginį: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **Iš naujo nustatykite IIS**, kad išvalytumėte statinę testuojamo varianto talpyklą. 

3.  **Raskite funkciją**: eikite į darbo sritį **Funkcijų valdymas**. Jei **Įrašytieji rodiniai** sąraše nerodomi, pasirinkite **Tikrinti, ar yra naujinimų**.   

4.  **Įjunkite funkciją**: funkcijų sąraše raskite funkciją **Įrašytieji rodiniai** ir išsamios informacijos srityje pasirinkite **Įjungti dabar**.

Visi vėlesni vartotojo seansai prasidės įjungus įrašytuosius rodinius.  

Atkreipkite dėmesį, kad jei aplinkos personalizavimas išjungtas, rodiniai bus įjungti, net jei atliksite pirmiau nurodytus veiksmus. Taip yra todėl, kad rodinių funkcija sukurta kaip personalizavimo posistemės papildas.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Kas atsitinka su esamais personalizavimais, kai rodiniai įgalinami? 
Įgalinus rodinius, visi esami vartotojo ir formos personalizavimai įrašomi į naują rodinį, pavadintą **Mano rodinys**, kuris automatiškai nustatomas kaip numatytasis rodinys. Taip siekiama prieš įgalinant rodinius ir juos įgalinus užtikrinti nuoseklią vartotojo patirtį, išskyrus tuos atvejus, kai formose rodomas rodinių išrinkiklio valdiklis.  

### <a name="what-pages-support-views"></a>Kurie puslapiai palaiko rodinius? 
Rodiniai galimi daugumoje „Finance and Operations“ puslapių, bet ne visuose. Rodiniai šiuo metu galimi visuose per visą ekraną rodomuose puslapiuose, išskyrus ataskaitų srityse ir darbo srityse. Šiuo metu rodiniai nepalaikomi ne viso ekrano puslapiuose, kuriuose yra dialogo langų, išplečiamųjų dialogo langų, patobulintų peržiūrų. Svarstoma, kad būsimuose naujiniuose rodiniai būtų palaikomi kitų tipų puslapiuose, pavyzdžiui, darbo srityse ir dialogo languose.   

### <a name="who-is-allowed-to-publish-views"></a>Kas gali publikuoti rodinius?
Šiuo metu sistemos administratoriai yra vieninteliai vartotojai, turintys teises publikuoti rodinius.  Numatomas naujas saugos vaidmuo, kuriuo būtų suteikiama daugiau lankstumo galinčių publikuoti klientų atžvilgiu.  

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Kodėl nepavyksta įrašyti filtrų naudojant šį rodinį? 
Yra keletas priežasčių, kodėl gali nepavykti su rodiniu įrašyti filtro. 

- Puslapyje gali būti nepalaikoma rodinio apraše nurodyta filtrų įrašymo funkcija. Atkreipkite dėmesį, kad personalizavimus ir užklausų modifikacijas kaip rodinį galima įrašyti tik tuose puslapiuose, kuriuose naudojami dideli rodinių išrinkikliai. Daugiau informacijos žr. skyriuje „Rodinių perjungimas“. 

- Jei tai numatytasis rodinys, o naršymo kelias į puslapį apima užklausą, rodinio užklausa iš pradžių gali būti netaikoma. Yra du pagrindiniai šios situacijos scenarijai. 
     - Perėjus į puslapį iš plytelės, plytelės užklausa bus vykdoma neatsižvelgiant į su numatytuoju rodiniu susietą užklausą. 
     - Jei perėjus į puslapį įrašo vietoje yra užklausa, iš pradžių bus vykdoma ne numatytojo rodinio užklausa, o pradinė užklausa. 
     
  Tokiais atvejais įkeliant rodinį turėtų būti rodomas įspėjantis informacinis pranešimas. Taip pat galite patvirtinti įjungdami šį rodinį įsikėlus puslapiui, nes tokiu atveju užklausa vis tiek galėtų būti vykdoma.  

- Reikiamame puslapyje rodiniai gali būti palaikomi netinkamai, kadangi rodinio užklausa gali būti visiškai nepaisoma arba veikti laikinoje lentelėje, kurios duomenys nėra pastovūs. 
