---
title: Įrašyti rodiniai
description: Šiame straipsnyje aprašoma, kaip naudoti įrašytas rodinių priemones.
author: jasongre
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 571a4f403da0d20256f788c791cab273827c91b5
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799497"
---
# <a name="saved-views"></a>Įrašyti rodiniai

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

[!INCLUDE [PEAP](../../../includes/peap-1.md)]

## <a name="introduction"></a>Įžanga

Personalizavimas atlieka svarbų vaidmenį, kadangi vartotojai ir organizacijos gali pagal poreikius optimizuoti vartotojo patirtį. Daugiau informacijos apie personalizavimą žr. [Vartotojo patirties personalizavimas](personalize-user-experience.md).

Tradicinis personalizavimas leidžia vartotojams turėti tik vieną personalizavimo rinkinį puslapyje. **Išsaugotų peržiūrų** funkcija praplėčia personalizavimą keliais svarbiais būdais:

- Naudodamiesi rodiniais vartotojai gali turėti kelis pavadintus vienos formos personalizavimo rinkinius ir greitai įjungti reikiamą bet kurį iš jų. Taigi vartotojas gali sukurti kelis optimizuotus puslapio rodinius, kad kiekvienas rodinys būtų pritaikytas konkrečioms verslo užduotims atlikti. 
- Tam tikro tipo puslapiams sukurti rodiniai taip pat gali apimti vartotojo įtrauktus filtrus arba rūšiavimus, kuriais naudodamiesi vartotojai gali greitai grįžti į dažniausiai filtruotus duomenų rinkinius. Daugiau informacijos ieškokite skyriuje [Kurie puslapiai palaiko rodinius](saved-views.md#what-pages-support-views). 
- Rodinius galima publikuoti vartotojams, atliekantiems konkrečius saugos vaidmenis ir priklausantiems konkretiems juridiniams subjektams. Todėl bet kuris vartotojas, kuris turi nustatytą vaidmenį ir prieigą prie nurodyto juridinio subjekto, gali pasiekti ir naudoti šį rodinį, net jei tas vartotojas neturi teisės pritaikyti. Naudodamosi šia publikavimo galimybe, organizacijos gali apibrėžti standartinius verslui optimizuotus įmonės rodinius. Daugiau informacijos ieškokite skyriuje [Personalizavimų valdymas organizacijos lygiu naudojant rodinius](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).
- Skirtingai nei tradicinis personalizavimas, peržiūros yra automatiškai išsaugojamas, kai naudotojas atlieka personalizavimą ar sąrašo filtravimą. Atskiri įrašymai yra reikalaujami siekiant suteikti naudotojams lankstumo kuriant peržiūras prieš ar po pakeitimų, kurie yra susiję su viena sukurta peržiūra. Šis reikalavimas taip pat užtikrina, kad peržiūros apibrėžimai nebūtų netyčia pakeisti filtrais ar personalizavimu, kurie nėra skirti naudoti ilgą laiką. Elementai, kuriuos sistema automatiškai talpina kaip dalį įprasto puslapio naudojimo (pavyzdžiui, stulpelių pločiai ar išplėstos ar sutrauktos skyrių būsenos) bus išsaugoti peržiūroje.
- Rodinius galima įtraukti į darbo sritis kaip plyteles, sąrašus arba saitus. Dėl to, filtruoti duomenys gali būti pasirenkami darbo srityje ir naudotojai gali susieti personalizuotą rinkinį, atitinkantį būtent tą duomenų rinkinį su saitu ar plytele.

## <a name="switching-between-views"></a>Rodinių perjungimas

Kai peržiūros yra įjungiamas aplinkoje, bet kurio puslapio viršus, palaikantis peržiūras, įtrauks sutrauktą peržiūros parinkėjų valdymą rodantį esamos peržiūros pavadinimą.

Rodinių išrinkiklių esama dviejų dydžių. 

- **Didelės peržiūros parinkėjai** – Puslapiai, kurie iškiliai apima sąrašo funkciją, turintį didesnius peržiūrų parinkėjus dėl kelių priežasčių. Svarbiausia, jei didesnis rodinio išrinkiklis nurodo puslapius, kuriuose rodinyje gali būti vartotojo nustatytų filtrų ir rūšiavimų. Filtrus ir rūšiavimus galima įtraukti į rodinius, todėl didesnis išrinkėjo dydis taip pat gali būti garantinis, nes rodinio pavadinimai dažniausiai yra geriausias ekrane rodomo duomenų aprašas, o tikti, kad vartotojai kas labiau pereis iš vieno rodinio į kitą šių tipų puslapiuose. Grupavimą tinklelyje taip pat galima įrašyti rodiniuose puslapyje, kuriame yra dideli rodinio parinkėjai. 
    
    [![Didelio rodinio išrinkiklis, palaikantis užklausos modifikacijas rodinyje.](./media/views-largeViewSelector.png)](./media/views-largeViewSelector.png)

- **Mažos peržiūros selektoriai** – Visi viso ekrano puslapiai (išskyrus darbo sritis ir ataskaitų sritis) turi mažus peržiūros selektorius, kurie pasirodo šalia puslapio aprėpties. Peržiūros šiuose puslapiuose apima tik personalizavimus, ne vartotojo nustatytus filtrus. Šiuose puslapiuose aprėptis ar įrašo plyta dažnai yra svarbiausia informacija puslapio viršuje. Mažesnis peržiūros selektoriaus dydis taip pat atspindi žemesnį perjungimo peržiūros dažnį nei tikėtinas šiuose puslapiuose. 
    
    [![Smulkaus rodinio išrinkiklis, kuris nepalaiko rodinio užklausos modifikacijų.](./media/views-smallViewSelector.png)](./media/views-smallViewSelector.png)
 
Jei pasirenkate peržiūrėti pavadinimą, peržiūros selektorius yra atidaromas ir rodo puslapyje esamų peržiūrų sąrašą.

Jei patobulintas **juridinio subjekto palaikymas įrašytai rodinių** funkcijai įjungtas, rodinio išrinkiklis rodo galimų rodinių dviejuose skyriuose. Pirmojoje dalyje rodomi visi rodiniai, kurie yra specifiniai dabartiniam juridiniam subjektui, o antrajame – rodiniai, galimi visiems juridiniams subjektams. Pirmoji sekcija matoma tik tada, kai yra juridinio subjekto – konkrečių puslapio rodinių.

- **Standartinė peržiūra** – **Standartinė** peržiūra yra nestandartinė puslapio peržiūra, kurioje nėra taikomi jokie personalizavimai.
- **Personalinės peržiūros** – Peržiūros be spynų rodo jūsų personalines peržiūras. Tai jūsų sukurti arba administratoriaus jums suteikti rodiniai.
- **Užrakintos peržiūros** – Kai kuriso peržiūros (tokios kaip **Standartinės** peržiūros ir visos peržiūros, kurios yra publikuojamos jūsų vaidmenyje) turi spynos simbolį šalia peržiūros selektoriaus. Šis simbolis nurodo, kad šių rodinių redaguoti negalima. Nepaisant to, pakeitimai atspindintys puslapio naudojimą yra įrašomi automatiškai. Šie pakeitimai apima stulpelio tinklelio pločio pakeitimus ir išplėsto bei sutraukto „FastTab“ statuso pakeitimus. Tačiau, jei turite personalizavimo teises, atlikdami veiksmą **Įrašyti kaip** galite sukurti asmeninį rodinį, pagrįstą užrakintu rodiniu.
- **Naujos peržiūros** – Publikuotos peržiūros, kurios dar nebuvo atidarytos turi kibirkšties simbolį peržiūros pavadinimo kairėje.

Norėdami perjungti kitą rodinį, pirmiausia atidarykite rodinių išrinkiklį ir pasirinkite norimą įkelti rodinį. 

## <a name="creating-and-modifying-views"></a>Rodinių kūrimas ir modifikavimas

Skirtingai nei tradicinis personalizavimas, peržiūros yra automatiškai išsaugojamas, kai naudotojas personalizuoja puslapį arba kai naudotojas taiko filtrą sąrašui ar jį rūšiuoja. Norint išsaugoti šiuos rodinio pakeitimus, reikia atlikti akivaizdų veiksmą. Šis reikalavimas suteikia naudotojams lankstumo kuriant peržiūras prieš ar po pakeitimų, kurie yra susiję su viena sukurta peržiūra. Jis taip pat užtikrina, kad peržiūros apibrėžimai nebūtų netyčia pakeisti vienkartiniais filtrais ar personalizavimu. Atkreipkite dėmesį, kad įprastos puslapio naudojamos elementai (pavyzdžiui, stulpelių pločiai ar išplėstos ar sutrauktos skyrių būsenos) yra automatiškai įrašomi esamoje peržiūroje ar netgi užrarkintos peržiūros.

Siekiant užtikrinti, kad esama peržiūros būsena yra žinoma, jums pradedant keisti personalizavimo ar filtravimo peržiūrą, žvaigždutė (\*) pasirodo šalia esamo peržiūros pavadinimo. Šis simoblis rodo, kad ieškote neišsaugotos, pakeistos peržiūros versijos.

[![Neįrašyti rodinio pakeitimai.](./media/views-unsavedChanges.png)](./media/views-unsavedChanges.png)

Norėdami įrašyti šiuos pakeitimus, atlikite toliau nurodytus veiksmus.

1. Pasirinkę rodinio pavadinimą atidarykite rodinių išrinkiklį.
2. Tam, kad keistumėte esančia peržiūrą, pasirinkite **Įrašyti**. Atkreipkite dėmesį, kad šis veiksmas nėra galimas užrakintoms peržiūroms. 
3. Norėdami sukurti naują rodinį, atlikite toliau nurodytus veiksmus.

    1. Pasirinkite **Įrašyti kaip**. 
    2. Rodinyje **Įrašyti kaip** įveskite rodinio pavadinimą ir, pasirinktinai, aprašymą.
    3. Jei norite, kad šis rodinys būtų numatytasis, pasirinkite **Pin kaip numatytąjį**. Daugiau informacijos apie numatytuosius rodinius žiūrėkite [toliau pateikiamame numatytojo](#changing-the-default-view) rodinio skyriaus keitimas. 
    4. Jei patobulintas **juridinio** subjekto palaikymas įrašytų rodinių funkcijai įjungtas, galite pasirinkti, ar norite, kad šis rodinys būtų galimas visiems juridiniams subjektams, ar tik jų subrinkinį.
    5. Pasirinkite **Įrašyti**.

## <a name="changing-the-default-view"></a>Numatytojo rodinio keitimas

Iš anksto nustatyta peržiūra yra peržiūra, kurią sistema bando atidaryti, kai pirmą kartą atveriate puslapį. Turite nustatyti iš anksto nustatytą peržiūrą, kad peržiūrėtumėte tai, ką tikitės dažniausiai naudoti. 

> [!NOTE]
> - Pagrindinėse **įrašytų rodinių** funkcijose juridiniuose subjektuose yra vienas visuotinis numatytasis rodinys. Jei keičiate nustatytą peržiūrą, ji bus atidaroma pagal nutylėjimą nepriklausomai nuo teisinio subjektu, kuriame šiuo metu esate.
> - Kai įjungtas **patobulinto juridinio subjekto** palaikymas įrašytų rodinių funkcijai, kiekvienas juridinis subjektas gali turėti savo numatytąjį rodinį puslapyje.

Norėdami pakeisti puslapio numatytąjį rodinį, atlikite tolesnius veiksmus.

1. Įjunkite rodinį, kuris naudojamas kaip numatytasis. 
2. Pasirinkę rodinio pavadinimą atidarykite rodinių išrinkiklį. 
3. Pasirinkite **Daugiau**, o paskui – **Prisegti kaip numatytąjį**.

Arba kurdami naują rodinį (naudodami veiksmą **Įrašyti kaip**) galite nustatyti, kad naujas rodinys būtų numatytasis rodinys – prieš įrašydami rodinį pasirinkite parinktį **Prisegti kaip numatytąjį**.

> [!WARNING]
> Atkreipkite dėmesį, kad kai kuriais atvejais su nustatyta peržiūra susieta užklausa neveikia, kai pirmą kartą atidarote puslapį. Pavyzdžiui, jei atidarote puslapį per plytą, jos užklausa veiks nepriklausomai nuo užklausos, kuri yra susieta su nustatytąja peržiūra. Be ti, jei atidarote puslapį, kuris turi **Standartinę** peržiūrą jau turinčią nustatytą užklausą, pirminė užklausa bus vykdoma vietoje nustatytosios peržiūros užklausos. Tokiu atveju gausite informacinį pranešimą, kai rodinys bus įkeltas su įdėtuoju veiksmu, kuris leidžia tiesiogiai įkelti numatytojo rodinio užklausą. Jei perjungiate peržiūras po to, kai puslapis buvo įkeltas, peržiūros užklausa turi galėti veikti, kaip tikėtasi. 

## <a name="managing-personal-views"></a>Asmeninių rodinių valdymas

Dialogo lange **Valdyti mano rodinius** suteikiama galimybė atlikti pagrindinę asmeninių rodinių priežiūrą ir nurodyti rodinių tvarką rodinių išrinkiklyje. Norėdami atidaryti šį puslapį, pasirinkite rodinio pavadinimą, norėdami atidaryti rodinių išrinkiklio išplečiamąjį meniu, pasirinkite **Daugiau**, o paskui – **Valdyti mano rodinius**.

Jei patobulintas juridinio **subjekto palaikymas įrašytai rodinių funkcijai įjungtas, skyriuje Mano rodiniai,**  **·**  **esantis dialogo lango Valdyti mano rodinius, rodo galimų rodinių puslapį skyriuose.**  Bet kokie dabartiniam juridiniam subjektui būsūs rodiniai rodomi savo skyriuje. **Visuotinių rodinių** skyrius visada rodomas, kad būtų galima valdyti rodinius, prieinamus puslapiui visuose juridiniuose subjektuose. 

Toliau išvardyti su galimų to puslapio rodinių sąrašu galimi atlikti veiksmai.

- **Peržiūrėti nustatytąją peržiūrą** – Naudokite **Smeigtuką kaip nustatytąjį** veiksmą tam, kad šiuo metu pasirinktumėte nustatytąjį peržiūrą šiam puslapiui. Jei **importavimo juridinio subjekto palaikymas įrašytai rodinių** funkcijai įjungtas, **visuotinių rodinių** skyrius leidžia peržiūrėti numatytąjį rodinį dabartiniam juridiniam subjektui arba visiems juridiniams subjektams.
- **Įrašykite savo peržiūras** – Naudokite **Eiti aukštyn** ir **Eiti žemyn** veiksmus tam, kad sutvarkytumėte iš naujo savo peržiūras konkrečia tvarka.
- **Pervardinti peržiūrą** – Naudokite **Pervardinti** veiksmą tam, pakeistumėte šiuo metu pasirinktos asmeninės peržiūros pavadinimą. Šis veiksmas išjungtas užrakintiems rodiniams. 
- **Šalinti peržiūrą** – Naudokite **Šalinti** veiksmą tam, nuolatos pašalintumėte esamą pasirinktą puslapio peržiūrą. Pašalinus rodinį, nėra jokių galimybių jį atkurti.

Visi šiame dialogo lange atlikti pakeitimai įsigalios pasirinkus mygtuką **Naujinti**.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Personalizavimų valdymas organizacijos lygiu naudojant rodinius

Tam, kad padėtumėte suprasti, kaip įrašytos peržiūros padeda pagerinti personalizavimo valdymą organizaciniu lygiu, šis skyrius aprašo keletą personalizavimo valdymo skirtumų su ir be **Įrašytų peržiūrų** funkcijos.

Kai rodinių nebuvo, administratoriai taikydavo puslapio personalizavimų rinkinį vartotojui, vartotojų grupei arba personalizavimo formą naudojantiems vartotojams. Jei tie vartotojai turėjo personalizavimo teises, personalizavimai būdavo taikomi tam puslapiui. Tačiau nepavyko išvengti tolesnio vartotojų atliekamo puslapio personalizavimo, o tai reiškė, kad organizacija negalėjo užtikrinti, kad jos vartotojai turi nuoseklią vartotojo sąsają. Jei kuris nors iš vartotojų neturėjo personalizavimo teisių, administratoriaus jiems suteikti personalizavimai nebūdavo įkeliami. Taip pat, jei organizacija pasamdydavo naujų vartotojų, administratoriai turėdavo patys įkelti vartotojui skirtą personalizavimų rinkinį. Nebūdavo automatinio mechanizmo, kuris nurodytų, kai esama tam tikro vartotojui skirto personalizavimų rinkinio.

**Įrašytos peržiūros** funkcija leidžia daug paprasčiau organizuoti personalizavimo valdymą, daugiausiai dėl to, kad peržiūras galima publikuoti vartotojų grupėms. Kai rodinys paskelbtas, bet kuris vartotojas, kuris turi vieną iš apibrėžtų saugos vaidmenų ir gali prieiti prie vieno iš nurodytų juridinių subjektų, gali matyti ir naudoti rodinį, net jei šis vartotojas neturi prieigos prie personalizavimo. Nepaisant to, kad visi vartotojai turi publikuotos peržiūros kopiją, kurioje automatiškai nustatytas puslapio elementų naudojimas, jokie vartotojai negali išsaugoti personalzavimo ar užklausos atnaujinimo publikuotose peržiūrose. Kitaip tariant, paskelbtos peržiūros yra užrakintos. Taip pat, jei nauji vartotojai turi priskirtus vaidmenis teisiniuose subjektuose, kurių peržiūros buvo publikuotos, jei automatiškai matys peržiūras susietas su jų vaidmenimis ir teisinius subjektus. Administratorius neturi atlikti jokių papildomų veiksmų. Taip pat, jei vartotojai keičia vaidmenis organizacijoje arba jiems suteikiama prieiga prie skirtingų juridinių subjektų, jie gali nebeturėti galimybės pasiekti anksčiau publikuotų rodinių. Ir šiuo atveju administratoriui nereikia atlikti jokių papildomų veiksmų.

Publikuoto rodinio naujinius paprasta išplatinti vartotojams iš naujo publikuojant rodinį atitinkamiems saugos vaidmenims ir juridiniams subjektams.

Naudodamosi publikavimo galimybe organizacijos gali apibrėžti standartinius savo verslui optimizuotus įmonės rodinius, skirtus konkrečius saugos vaidmenis turintiems vartotojams.

## <a name="publishing-views"></a>Rodinių publikavimas

Publikavimo proceso metu peržiūros gali būti priskirtos vienam ar keletui saugos vaidmenų vienam ar keliems teisiniams subjektams. Dėl to, bet kuris vartotojas turėdamas prieigą prie teisinio subjekto ir priskirtas vienam iš šių vaidmenų gali prieiti ir naudoti peržiūras. Nepaisant to, vartotojas negali redaguoti peržiūrų. Pagal nutylėjimą, sistemų administratoriai turi prieigą prie **Publikavimo** veiksmo peržiūros selektoriaus iškrentančiame meniu. Tačiau kitiems patikimiems jūsų organizacijos vartotojams taip pat gali būti suteikta prieiga prie rodinio publikavimo naudojant naują vaidmenį **Įrašytų rodinių administratorius**.

Norėdami publikuoti rodinį, atlikite toliau nurodytus veiksmus.

1. Sukurkite ir įrašykite norimo publikuoti rodinio asmeninę kopiją. 
2. Jei tas rodinys šiuo metu įkeltas, pasirinkę rodinio pavadinimą atidarykite rodinių išrinkiklio išplečiamąjį meniu. 
3. Pasirinkite mygtuką **Daugiau**, o paskui pasirinkite **Publikuoti**. Atsidarys **dialogo** langas Publikuoti.
4. Įveskite rodinio pavadinimą. Įvestas pavadinimas yra pavadinimas, kurį vartotojai, gaunantys šį rodinį, matys savo rodinių išrinkikliuose. Publikuotų puslapio rodinių pavadinimai turi būti unikalūs. Pavadinimai negali kartotis, net jei skiriasi vaidmenų arba juridinių subjektų, kuriems taikomi rodiniai, sąrašas.
5. Jei organizacijos **rodinių** vertimo funkcija įjungta, galite įtraukti rodinio pavadinimo vertimus į tiek kalbų, **·**  **kiek** reikalauja jūsų organizacija, pasirinkdami mygtuką Vertimai, esantį šalia lauko Pavadinimas. Tada rodinio pavadinimas bus rodomas vartotojams jų pasirinkta kalba. Taip pat galite nustatyti numatytąją kalbą, kad būtų galima nurodyti vertimą tiems vartotojams, kurių vertimo kalbos aprašo nėra.
5. Pasirinktina: įveskite rodinio aprašymą, kad vartotojai, kurie gaus šį rodinį, galėtų geriau suprasti jo paskirtį. 
6. Nuspręskite, ar rodinys turėtų būti paskelbtas kaip numatytasis rodinys pasirinktiems vartotojams. Kai peržiūra yra paversta nustatytąja, vartotojai ją matys kitą kartą, kai atidarys paskirties puslapį. Bus pakeista viena, iš anksto nustatyta globali peržiūra visų galutinių vartotojų. Nepaisant to, vartotojai dar gali keisti jų nustatytąją peržiūrą po jos publikavimo.

    > [!NOTE]
    > Publikuodami rodinį kaip numatytąjį elgesį, publikuojate rodinį kaip numatytą:
    >
    > - Jei publikuojate rodinį kaip numatytąjį rodinį kai kuriems arba visiems juridiniams subjektams, vyksta toliau nurodytas veikimo būdas:
    >
    >    - Jei įjungta tik **pagrindinė įrašytų** rodinių funkcija, vienas visuotinis numatytasis rodinys bus pakeistas kiekvienam tiksliniam vartotojui. 
    >    - ** Jei patobulintas **juridinio** subjekto palaikymas įrašytų rodinių funkcijai įjungtas ir publikuojate rodinį juridinių subjektų subgrupyje, tų juridinių subjektų numatytasis rodinys bus pakeistas kiekvienam tiksliniam vartotojui.
    >
    > - Jei vartotojas turi vaidmenis, kuriuos keletas peržiūrų yra publikuojama kaip nustatytosios, paskutinė publikuota peržiūra bus naudojama kaip vartotojo nustatytoji peržiūra. 
    > - Publikavimas nebus naudojamas vaidmenų priskyrimui naudojant AAD grupes. 

8. Pridėkite vartotojams, kuriems skirtas šis rodinys, taikomus saugos vaidmenis. 
9. Nuspręskite, ar norite paskelbti rodinį kiekvieno pasirinkto saugos vaidmens antriniams vaidmenims. Jei taip atliekate, pasirinkite **Įtraukti vaikų vaidmenis** pažymimą laukelį eilutėje atitinkamiems saugos vaidmenims. Atkreipkite dėmesį, kad šis žymimas laukelis nėra prieinamas vaidmenims, neturintiems vaikų vaidmenų.
10. Pridėkite juridinius subjektus, kuriems turi būti pasiekiamas šis rodinys. 

    > [!NOTE]
    > Atsiminkite toliau pateiktas išimtis, kai publikuojate peržiūrą į teisinį subjektą ar kai publikuojate elgesį kaip nustatytąjį:
    >
    > - Jei įjungta tik bazinių įrašytų rodinių funkcija, vartotojo rodinio išrinkiklis puslapyje iš pradžių rodo rodinį tik **nurodytiems juridiniams** subjektams. Nepaisant to, po peržiūros įkėlimo pirmą kartą, ji visuomet bus vartotojo peržiūros selektoriuje tame puslapyje nepriklausomai nuo teisinio subjekto.
    > - Jei patobulintas **juridinio subjekto palaikymas įrašytų** rodinių funkcijai įjungtas, rodinio išrinkiklis niekada rodys tik nurodytų juridinių subjektų rodinį.

11. Pasirinkite **Publikuoti**.

Atkreipkite dėmesį, kad kai kuriose aplinkose gali šiek tiek užtrukti (iki valandos), kol vartotojai pamatys publikuotą rodinį.

## <a name="modifying-a-published-view"></a>Publikuoto rodinio modifikavimas

Po peržiūros publikavimo, jums gali prireikti jį keisti. Nepaisant to, kad negalite atlikti einamųjų pakeitimų publikuotoje peržiūroje, nes šios peržiūros redagavimas visiems vartotojams yra užrakintas (įskaitant publikuotojus), galite iš naujo publikuoti peržiūrą jos atnaujinimui.

Jeigu publikuotam rodiniui norimi atlikti pakeitimai apima tik publikavimo parametrus (rodinio pavadinimą ir aprašą arba saugos vaidmenis, kuriems rodinys publikuojamas), atlikite toliau nurodytus veiksmus.

1. Įjunkite norimų atnaujinti parametrų publikuotą rodinį. 
2. Peržiūros selektoriuje iškrentančiame meniu pasirinkite **Publikuoti iš naujo**. Jei naudojate 10.0.12 versiją ar ankstesnė, turite pasirinkti **Publikuoti** ir tuomet **Taip** tam, kad atnaujintumėte esančią peržiūrą.
3. Atnaujinkite pavadinimą, aprašą, saugos vaidmenis ir teisinius subjektus peržiūrai. 
4. Pasirinkite **Publikuoti**. Jei iš pradžių pasirinkote šį paskelbtą rodinį kaip numatytąjį, jums jį iš naujo paskelbus, vartotojai jį matys kaip numatytąjį. 

Jeigu publikuoto rodinio pakeitimai apima su rodiniu susietą personalizavimą ar modifikuotus filtrus, atlikite toliau nurodytus veiksmus.

1. Įkelkite publikuotą peržiūrą, kurią norite pakeisti. 
2. Atlikite būtinus pakeitimus vietiniame šablone.
3. Peržiūros selektoriuje iškrentančiame meniu pasirinkite **Publikuoti iš naujo**.
4. Pasirinkite **Taip** tam, kad nurodytumėte, kad norite publikuoti peržiūrą kartu su neišsaugotais pakeitimais. 
5. Keiskite visus publikuotus parametrus, kurių reikia keitimui ir tuomet pasirinkite **Publikuoti**. 

## <a name="managing-published-views"></a>Publikuotų rodinių valdymas

Kaip ir valdant asmeninius rodinius, dialogo lange **Valdyti mano rodinius** vartotojams, turintiems publikavimo teisę, suteikiama galimybė atlikti pagrindinius publikuotų to puslapio rodinių (taip pat savo asmeninių rodinių) priežiūros veiksmus. Norėdami atidaryti šį puslapį, pasirinkite rodinio pavadinimą, norėdami atidaryti rodinių išrinkiklio išplečiamąjį meniu, pasirinkite **Daugiau**, o paskui – **Valdyti mano rodinius**.

Nors visi vartotojai **turi** skirtuką Mano rodiniai, kuriame rodomi jų asmeniniai rodiniai, vartotojai, kurie turi publikavimo teises, **taip** pat turi organizacijos rodinių skirtuką, kuriame rodomi visi paskelbti ir nepaskelbtai to puslapio rodiniai. Kadangi keli vartotojai gali publikuoti peržiūras, svarbu, kad galėtumėte valdyti visą publikuotų peržiūrų sąrašą, net jei nesate vartotojas publikuojantis esamą peržiūrą.

Toliau išvardyti su visų publikuotų puslapio rodinių sąrašu galimi atlikti veiksmai. 

- **Publikuoti iš naujo** – Naudoja **Publikuoti iš naujo** veiksmą tam, kad būtų publikuojama peržiūra po parametrų publikavimo (pavadinimas, aprašas, saugumo vaidmenys ar teisiniai subjektai) pakeitimų.
- **Publikuoti** – Naudokite **Publikuoti** veiksmą tam, kad publikuotumėte peržiūrą, kuri šiuo metu nepublikuota. 
- **Nepublikuoti** – Naudokite **Nepublikuoti** veiksmą tam, kad peržiūrą padarytumėte neaktyvią. Peržiūra dar bus prieinama sistemoje, tačiau vartotojai nematys jos peržiūros selektoriuje, kol peržiūra nebus dar kartą publikuojama.
- **Įrašyti kaip asmeninį** – naudokite **Įrašyti kaip asmeninį** veiksmą, kad sukurtumėte publikavimo rodinio asmeninį juodraštį. Ši funkcija gali padėti suprasti rodinio turinį, kuris nebuvo jums publikuotas arba kuris dar nebuvo publikuotas. Taip pat galite naudoti jį redaguoti, o tada iš naujo publikuoti rodinį.
- **Šalinti peržiūrą** – Naudokite **Šalinti** veiksmą tam, nuolatos pašalintumėte publikuotą ar nepublikuotą peržiūrą. Šis veiksmas taip pat pašalina vartotojų peržiūrą sistemoje. Publikuotų peržiūrų pašalinimas įsigalioja po to, kai **Įrašyti** mygtukas yra pasirenkamas. Pašalinus peržūrą, jos atstatyti nebeįmanoma. 

## <a name="managing-views-globally"></a>Rodinių valdymas visame pasaulyje

Nors kai kurios valdymo galimybės yra išksaugotos kiekviename puslapyje, kaip nurodyta šiame straipsnyje, **·**  **·**  **sistemos administratoriai ir įrašyti rodinio administratoriai gali tvarkyti sistemos rodinius kelis kartus personalizavimo** puslapyje. Detaliau tyrinėjant, šiame puslapyje yra šie skyriai ir funkcijos: 

- **Publikuoti rodiniai** – šiame skyriuje išvardyti visi jūsų organizacijai publikuoti rodiniai. Iš čia galite iš naujo publikuoti rodinį po to, kai pakoreguojate saugos vaidmenis arba juridinius asmenis, į kuriuos rodinys orientuotas. Galite taip pat eksportuoti, pašalinti ar nepublikuoti peržiūrų. Spustelėję **Įrašyti kaip asmeninį**, galite sukurti rodinio asmeninę kopiją, kad galėtumėte jį atnaujinti arba geriau suprasti jo turinį. 
- **Nepublikuotos peržiūros** – Šis skyrius išvardyja visas organizacijos peržiūras jūsų sistemoje, kurios šiuo metu nėra publikuotos. Šiso peržiūros dažniausiai patenka į sistemą per importavimo savybes. Galite publikuoti, eksportuoti ar naikinti šiuos rodinius. Dėl **Greito publikavimas** veiksmo, kuris buvo pridėtas 10.0.12 versijoje, šiame skyriuje galima publikuoti kelis rodinius vienu veiksmu, naudojant esamą saugos vaidmenį ir juridinio asmens konfigūracijas. Galite naudoti veiksmą **Įrašyti kaip asmeninį,** norėdami sukurti asmenines šių rodinių kopijas, kad geriau suprastumėte jų turinį.
- **Asmeniniai rodiniai** – šiame skyriuje pateikiami visi vartotojų sistemoje sukurti rodiniai. Nuo čia galite publikuoti asmeninį rodinį organizacijai arba nukopijuoti vieną ar daugiau šių rodinių kitiems vartotojams. Taip pat galite pagal poreikį eksportuoti ar naikinti šiuos rodinius.
- **Vartotojo parametrai** – Pasirinkite peržiūrimą vartotoją ar keiskite vartotojo galimybes personalizavimo naudojimui visoje sistemoje ar konkrečiuose puslapiuose, kuriuos vartotojas aplankė. Galite peržiūrėti ir sąveikauti su vartotojo personalizavimais sistemoje. Galite taip pat pašalinti visus personalizavimus tam vartotojui ar panaikinti funkcijos iškvietimus jam. Jei funkcijos iškvietimai yra paleidžiami iš naujo, visi iššokantys langai pristatantys naują funkciją ir vartotojo anksčiau atmesti langai pasirodys dar kartą, kai vartotojas kitą kartą susidurs su šiomis funkcijomis.
- **Sistemos nustatymai** – Galite laikinai išjungti personalizavimą visiems vartotojams sistemoje. Tuo atveju, joks personalizavimas nebus taikomas jokiam vartotojui ir visi puslapiai bus paleidžiami iš naujo į savo nustatytąsias būsenas. Jeigu vėliau vėl įjungsite personalizavimą, visi personalizavimai bus pritaikyti iš naujo. Taip pat galite visam laikui išjungti visus visų vartotojų sistemos personalizavimus. Panaikintų personalizavimų atkurti neįmanoma. Todėl prieš atlikdami šią užduotį būtinai eksportuokite visus personalizavimus, kurių vėliau gali prireikti.

Vartotojai turintys prieigą prie **Personalziavimo** puslapio gali taip pat importuoti asmenines ar organizacijos peržiūras naudodami **Importavimo peržiūros** mygtuką veiksmų juostoje. Organizacijos rodiniams galite pasirinkti **Paskelbti nedelsiant**, kad rodiniai taptų prieinami visiems vartotojams be papildomo paskelbimo.

## <a name="known-issues"></a>Žinomos problemos

Dėl žinomų problemų sąrašo su įrašytomis peržiūromis, prašome žr. [Kurkite formas, kurio visiškai naudoja įrašytas peržiūras](../../dev-itpro/user-interface/understanding-saved-views.md).

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Kaip įgalinti įrašytus rodinius mano aplinkoje?

> [!NOTE]
> Įrašytų **rodinių** funkcija reikalauja įgalinti finansų ir operacijų programėlių personalizavimo sistemą. Jei suasmeninimas išjungtas visoje aplinkoje, rodiniai taip pat bus išjungti, net jei atliksite toliau nurodytus veiksmus. 

Funkciją **Įrašyti rodiniai** galite įjungti ir išjungti per Funkcijų valdymą bet kurioje aplinkoje. Ją įjungus, įrašyti rodiniai bus įjungti visuose tolesniuose vartotojo seansuose.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Kas atsitinka su esamais personalizavimais, kai rodiniai įgalinami? 

Įgalinus rodinius, visi esami vartotojo ir formos personalizavimai įrašomi į naują rodinį, pavadintą **Mano rodinys**, kuris automatiškai nustatomas kaip numatytasis rodinys. Taip siekiama prieš įgalinant rodinius ir juos įgalinus užtikrinti nuoseklią vartotojo patirtį, išskyrus tuos atvejus, kai formose rodomas rodinių išrinkiklio valdiklis.

### <a name="what-pages-support-views"></a>Kurie puslapiai palaiko rodinius? 

Rodiniai yra visuose, bet ne visuose, puslapiuose. Rodiniai yra tik visuose viso ekrano puslapiuose, išskyrus skelbimų skelbimų skydus. Peržiūrėti darbo sričių palaikymą galima naudojant įrašytus **rodinių palaikymą darbo sričių funkcijai** . Dauguma ne viso ekrano puslapių, kuriuose yra išplečiamasis dialogo langas, peržvalgos ir patobulintos peržiūros, šiuo metu nepalaiko rodinių. Dialogo langų palaikymą galima peržiūrėti naudojant įrašytus **rodinių dialogo lango palaikymą** .

### <a name="who-is-allowed-to-publish-views"></a>Kas gali publikuoti rodinius?

Tik sistemos administratoriai ir vartotojai, kurie buvo priskirti vaidmeniui **Įrašytų rodinių administratorius**, turi teisę publikuoti rodinius. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Kodėl nepavyksta įrašyti filtrų naudojant šį rodinį? 

Yra keletas priežasčių, kodėl gali nepavykti su rodiniu įrašyti filtro. 

- Puslapyje gali būti nepalaikoma rodinio apraše nurodyta filtrų įrašymo funkcija. Įsidėmėkite, kad suasmeninimus ir užklausų modifikacijas galima išsaugoti kaip rodinį tik tokiuose puslapiuose, kurie turi didelius rodinių išrinkiklius. Daugiau informacijos rasite temoje **Rodinių perjungimas**. 
- Reikiamame puslapyje rodiniai gali būti palaikomi netinkamai, kadangi rodinio užklausa gali būti visiškai nepaisoma arba veikti laikinoje lentelėje, kurios duomenys nėra pastovūs. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Kokius duomenis matysiu apsilankydamas puslapyje?

Puslapiuose, kurie turi mažesnius peržiūros selektorius (tik personalizavimas gali būti įrašytas peržiūroje), matysite tokius pačius duomenis, kokius visuomet turėjote lankydamiesi puslapyje. 

Puslapiams, kurie turi didelius peržiūros selektorius (tiek personalizavimo, tiek ir užklausos gali būti įrašomos peržiūroje) dažniausiai matysite duomenis, kurie yra susieti su užklausa, susieta su jūsų nustatytąja peržiūra. Esama dviejų išimčių:

- Perėjus į puslapį iš plytelės, plytelės užklausa bus vykdoma neatsižvelgiant į su numatytuoju rodiniu susietą užklausą. Jei sukūrėte tą išklotinę įjungę rodinius, pasirinkus išklotinę atsidarys puslapis su rodiniu, susietu su ta išklotine.
- Jei perėjus į puslapį įvesties vietoje yra užklausa, iš pradžių bus vykdoma ne numatytojo rodinio užklausa, o pradinė užklausa. Būkite atidūs, kai tai įvyksta informaciniu pranešimu, kai įkeliamas vaizdas. Taip pat galite patvirtinti įjungdami šį rodinį įsikėlus puslapiui, nes tokiu atveju užklausa vis tiek galėtų būti vykdoma.

### <a name="why-is-a-view-that-was-published-for-a-specific-legal-entity-visible-in-all-legal-entities"></a>Kodėl rodinys, kuris buvo publikuotas konkrečiam juridiniam subjektui, matomas visuose juridiniuose subjektuose?

Atsiminkite toliau pateiktas išimtis, kai publikuojate peržiūrą į teisinį subjektą ar kai publikuojate elgesį kaip nustatytąjį:

- Jei įjungta tik bazinių įrašytų rodinių funkcija, vartotojo rodinio išrinkiklis puslapyje iš pradžių rodo rodinį tik **nurodytiems juridiniams** subjektams. Nepaisant to, po peržiūros įkėlimo pirmą kartą, ji visuomet bus vartotojo peržiūros selektoriuje tame puslapyje nepriklausomai nuo teisinio subjekto. Taip nutinka todėl, kad vartotojai gauna savo asmeninę publikuoto rodinio kopiją, kai jis įkeliamas, o asmeniniai rodiniai yra visuotiniai.
- Jei patobulintas **juridinio subjekto palaikymas įrašytų** rodinių funkcijai įjungtas, rodinio išrinkiklis niekada rodys tik nurodytų juridinių subjektų rodinį. Taip nutinka, nes funkcija įgalina rodinius (įskaitant asmeninius rodinius) susieti su konkrečiais juridiniais subjektais.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

