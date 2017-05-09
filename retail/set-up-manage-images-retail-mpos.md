---
title: "„Retail Modern POS“ vaizdų nustatymas ir tvarkymas"
description: "Šiame straipsnyje paaiškinami įvairių objektų vaizdų, rodomų srityje „Retail Modern POS‟ (MPOS), nustatymo ir valdymo veiksmai."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dbcf6d2ca3a6009c1631636309ff55cebb0551e6
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-and-manage-images-for-retail-modern-pos"></a>„Retail Modern POS“ vaizdų nustatymas ir tvarkymas

[!include[banner](includes/banner.md)]


Šiame straipsnyje paaiškinami įvairių objektų vaizdų, rodomų srityje „Retail Modern POS‟ (MPOS), nustatymo ir valdymo veiksmai.

<a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Medijos pagrindinio URL nustatymas ir medijos šablonų apibrėžimas siekiant konfigūruoti URL vaizdų formatą
-------------------------------------------------------------------------------------------------

„Retail Modern POS“ (MPOS) rodomi vaizdai turi būti nuomojami išorėje, o ne „Microsoft Dynamics 365 for Operations“ – versijoje „Retail“. Paprastai jie nuomojami turinio valdymo sistemoje, turinio pristatymo tinkle (CDN) arba medijos serveryje. Tada MPOS išrenka ir rodo atitinkamų objektų, pvz., produktų ir katalogų, vaizdus, prisijungdama prie paskirties URL. Siekiant rasti šiuos išoriškai nuomojamus vaizdus, MPOS reikia teisingo formato URL. Reikiamą vaizdų URL formatą galite konfigūruoti nustatydami lauko **Medijos pagrindinis URL** reikšmę kanalo šablone ir naudodami kiekvieno objekto funkciją **Nustatyti medijos šabloną**. Taip pat galite perrašyti objektų subrinkinio standartinį URL formatą, naudodami funkciją **Redaguoti programoje „Excel“**. **Svarbi pastaba:** dabartinėje „Dynamics 365 for Operations“ versijoje nebegalima nustatyti URL formato naudojant MPOS atributo XML **Vaizdas** objektų atributų grupėje **Numatyta**. Jei esate susipažinę su „Microsoft Dynamics AX 2012 R3“ ir šiuo metu naudojate dabartinę „Dynamics 365 for Operations“ versiją, įsitikinkite, kad visada naudojate naują funkciją **Nustatyti medijos šabloną** vaizdams nustatyti. Nenaudokite ir nemodifikuokite atributo **Vaizdo** objektų atributų grupėje **Numatyta**, įskaitant produktus. Pakeitimai, kuriuos tiesiogiai atliekate vaizdų atributų grupėje **Numatyta**, rodomi nebus. Ši parinktis būsimame leidime bus išjungta. Tolesnėse procedūrose pagal pavyzdį nustatomi objekto Katalogas vaizdai. Šios procedūros padės užtikrinti, kad visų katalogo vaizdų, turinčių bendrą kelią, vaizdo paskirties kelias būtų nustatytas netiesiogiai. Pvz., jei išoriškai nustatėte medijos serverį arba CDN ir norite, kad pasirinktos parduotuvės vaizdai būtų rodomi MPOS, funkcija **Nustatyti medijos šabloną** padės nustatyti kelią, kuriuo MPOS gali ieškoti vaizdų ir juos nuskaityti. **Pastaba:** šiame demonstracinių duomenų pavyzdyje medijos serveris yra įdiegtas „Retail Server“. Tačiau jis gali būti bet kur kitur, ne „Dynamics 365 for Operations“.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Kanalo medijos pagrindinio URL nustatymas

1.  Atidarykite „Dynamics 365 for Operations“ HQ portalą.
2.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Kanalo nustatymas** &gt; **Kanalo šablonai**. [![1 kanalo šablonas](./media/channel-profile1.png)](./media/channel-profile1.png)
3.  Jūsų parduotuvės naudojamame MPOS skirtame kanalo šablone atnaujinkite lauką **Medijos pagrindinis URL**, įvesdami savo medijos serverio arba CDN pagrindinį URL. Pagrindas URL yra pirmoji URL dalis, kurią bendrai naudoja visi skirtingų objektų vaizdų aplankai.[![2 kanalo šablonas](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Objekto medijos šablono nustatymas

1.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Katalogo valdymas** &gt; **Katalogo vaizdai**.
2.  Puslapio **Katalogo vaizdai** veiksmų srityje spustelėkite **Nustatyti medijos šabloną**. Dialogo lango **Nustatyti medijos šabloną** lauke **Objektas** pagal numatytuosius nustatymus turi būti nustatyta parinktis **Katalogas**.
3.  „FasTab“ **Medijos kelias** įveskite likusį vaizdo vietos kelią. Medijos kelias palaiko **LanguageID** kaip kintamąjį. Pvz., demonstraciniams duomenims galite sukurti visų jūsų medijos serverio medijos pagrindinio URL katalogo vaizdų aplanką **Katalogas** (https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer). Tada galite sukurti aplanką kiekvienai kalbai, pvz., en-US arba fr FR, ir į kiekvieną aplanką nukopijuoti atitinkamus vaizdus. Jei neturite skirtingų įvairių kalbų vaizdų, galite neįtraukti kintamojo **LanguageID** į aplanko struktūrą ir tiesiogiai nurodyti katalogų aplanką, kuriame yra katalogo vaizdai. **Pastaba:** dabartinė „Dynamics AX“ versija palaiko objektų Katalogas, Produktas ir Kategorija atpažinimo ženklą **{LanguageId}**. (Nepalaikomas objektų Klientas ir Darbuotojas atpažinimo ženklas **{LanguageID}**, atsižvelgiant į esamą standartą, kuris galioja nuo „Microsoft Dynamics AX“ 6.x.)
4.  Vaizdų failo vardo formatas yra užprogramuotas kaip katalogo pavadinimas ir jo keisti negalima. Todėl pervardykite vaizdus, kad jie turi atitinkamus katalogų pavadinimus, siekdami užtikrinti, kad MPOS tvarko juos teisingai.
5.  Lauke **Failo plėtinys** pasirinkite numatomą failo vardo plėtinį, priklausomai nuo turimų vaizdų tipo. Pavyzdžiui, demonstracinių duomenų katalogo vaizdų plėtinys yra nustatytas kaip .jpg. (Vaizdo failai yra taip pat pervardinami, kad turėtų katalogo pavadinimus.)
6.  Spustelėkite **Gerai**.
7.  Norėdami patikrinti, ar vaizdų medijos šablonas buvo įrašytas teisingai, puslapyje **Katalogo vaizdai** dar kartą spustelėkite **Nustatyti medijos šabloną**. Norėdami šabloną tikrinti neuždarydami dialogo lango **Nustatyti medijos šabloną**, galite naudoti „FastTab“ **Generuoti vaizdų URL, skirtus „Excel“**. Patikrinkite vaizdo URL rodinį ir įsitikinkite, kad URL atitinka anksčiau nurodytą šablono standartą. Dabar dialogo langas **Nustatyti medijos šabloną** netiesiogiai nustatė visų katalogų vaizdų, naudojančių bendrą URL kelią, vaizdo kelią. Šis URL kelias yra taikomas visiems katalogo vaizdams, nebent jie yra perrašomi. Pirmoji vaizdo kelio dalis yra paimta iš medijos pagrindinio URL, kurį nurodėte kanalo šablone. Likusi kelio dalis yra paimta iš kelio, kurį nurodėte medijos šablone. Abi dalys yra sujungiamos ir pateikiamas visas vaizdų vietos URL. Pavyzdžiui, demonstracinių duomenų katalogas yra pavadintas „Fabrikam“ pagrindiniu katalogu. Todėl vaizdo pavadinimas turi būti „Fabrikam“ pagrindinis katalogas.jpg, t. y. turi būti panaudotas katalogo pavadinimas ir šablone sukonfigūruotas failo vardo plėtinys .jpg. Šiuo atveju po sujungimo URL bus https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam pagrindinis katalogas.jpg.
8.  Vykdykite sinchronizavimo užduotis ir įtraukite naują šabloną į kanalo duomenų bazę, kad MPOS galėtų šabloną naudoti vaizdams pasiekti.
9.  Norint, kad katalogo vaizdų medijos šabloną atnaujintų kanalas, reikia paleisti užduotį **1150 katalogo užduotis** iš **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**.[![1 katalogas](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Vaizdo peržiūra objekto lygyje
1.  Objekto prekės HQ puslapyje galite peržiūrėti vaizdą, kuris naudoja vaizdo URL, gautą iš medijos šablono. Šiame pavyzdyje pasirinkite atitinkamą katalogą ir tada veiksmų srityje spustelėkite **Medija** &gt; **Vaizdai**. Naudokite išplečiamąjį sąrašą norėdami pasirinkti įvairias parduotuves, kurios gali turėti skirtingus kanalų šablonus.
2.  Norėdami redaguoti arba šalinti netiesioginį medijos šabloną, turite vėl pasirinkti dialogo langą **Nustatyti medijos šabloną** puslapyje **Katalogo vaizdai**.
3.  Galite naudoti mygtukus **Įtraukti** ir **Šalinti**, norėdami patys pakeisti kelią, kuris pagrįstas netiesioginiu šablonu ir kurį naudoja konkretus vaizdas. Norėdami gauti daugiau informacijos, žr. tolesnį šio straipsnio skyrių „Objekto prekių medijos šablono perrašymas“.
4.  Peržiūrėję vaizdą ir atlikę reikiamus keitimus, paleiskite atitinkamos parduotuvės MPOS egzempliorių ir patikrinkite, ar rodomi katalogo vaizdai.[![4 katalogas](./media/catalog4.png)](./media/catalog4.png)

**Pastaba:** tą pačią procedūrą galite naudoti su visais penkiais palaikomais objektais, kurie yra: Darbuotojas, Klientas, Katalogas, Kategorija ir Produktai. „Katalogo produktai“ (katalogų lygyje nustatyti produktai) ir „Kanalo produktai“ (kanalo lygyje nustatyti produktai) naudoja nustatytą objekto Produktai medijos šabloną. Galite pasirinkti, kiek objekto Produktai medijos šablono produkto vaizdų rodyti kiekvienam produktui. Taip pat galite nustatyti konkretaus produkto numatytąjį vaizdą. Tokiu būdu galite išvengti tuščių vaizdų rodymo MPOS ir padėti kontroliuoti, kuris vaizdas bus naudojamas kaip numatytasis produkto vaizdas. Tolesniame pavyzdyje kiekvienas produktas turi penkis vaizdus, o pirmasis vaizdas yra nustatytas kaip numatytasis. Produktų variantai yra valdomi taip pat, kaip bendrieji produktai. Vaizdo failo vardas turi būti nustatytas pagal produkto numerį. Kai kurie simboliai pradingo, kol buvo generuojamas failo vardas. Todėl rekomenduojama patikrinti failo vardą naudojant sekciją **Generuoti vaizdų URL. skirtus „Excel“**. [![prod.](./media/prods.png)](./media/prods.png)  

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Sinchronizavimo užduotys, skirtos medijos šabloną siųsti kanalui
Dirbdami su visais penkiais palaikomais objektais (Darbuotojas, Klientas, Katalogas, kategorija ir Produktai), kiekvieną kartą, kai atnaujinate dialogo langą **Nustatyti medijos šabloną**, norėdami nustatyti vaizdą, būtinai vykdykite užduotį Katalogas (1150), pasirinkdami **Mažmeninės prekybos IT** &gt; **Paskirstymo grafikas**. Atlikus šią užduotį, atnaujintą medijos šabloną bus galima sinchronizuojami su kanalu ir MPOS galės jį naudoti. Paleisti užduotį Katalogas (1150), atlikę toliau pateiktus keitimus.

-   Atnaujinę objekto Katalogas vaizdo medijos šabloną pasirinkdami **Katalogo vaizdai** &gt; **Nustatyti medijos šabloną**.
-   Atnaujinę objekto Darbuotojas vaizdo medijos šabloną pasirinkdami **Darbuotojo vaizdai** &gt; **Nustatyti medijos šabloną**.
-   Atnaujinę objekto Klientas vaizdo medijos šabloną pasirinkdami **Kliento vaizdas** &gt; **Nustatyti medijos šabloną**.
-   Atnaujinę objekto Produktas vaizdo medijos šabloną pasirinkdami **Produkto vaizdai** &gt; **Nustatyti medijos šabloną**.
-   Atnaujinę objekto Kategorija vaizdo medijos šabloną pasirinkdami **Kategorijos vaizdai** &gt; **Nustatyti medijos šabloną**. Taip pat turite publikuoti kanalą.

## <a name="overwriting-the-media-template-for-entity-items"></a>Objekto prekių medijos šablono perrašymas
Kaip sužinojote ankstesniame skyriuje, nurodyto objekto medijos šablonas palaiko tik vieną bendrą kelią. Šis kelias yra pagrįstas sukonfigūruotu medijos pagrindiniu URL ir nustatytu medijos keliu. Tačiau daugeliu atvejų mažmenininkas nori turėti galimybę objekto prekių subrinkinyje naudoti vaizdus iš įvairių šaltinių. Pvz., parduotuvė naudoja savarankiškai nuomojamą medijos serverį vienam katalogo vaizdų rinkiniui, bet kitam naudoja CDN URL. Norėdami perrašyti vaizdų URL, pagrįstus objekto lygio objekto vaizdų medijos šablonu, galite naudoti funkcijas Redaguoti programoje „Excel“ ir Neautomatinis redagavimas, esančias puslapyje **Peržiūra**.

### <a name="overwrite-by-using-edit-in-excel"></a>Perrašyti naudojant funkciją Redaguoti programoje „Excel“

1.  Spustelėkite **Mažmeninė prekyba ir prekyba** &gt; **Katalogo valdymas** &gt; **Katalogo vaizdai**.
2.  Puslapyje **Katalogo vaizdai** spustelėkite **Nustatyti medijos šabloną**. Dialogo lango **Nustatyti medijos šabloną** lauke **Objektas** turi būti nustatyta parinktis **Katalogas**.
3.  Įsidėmėkite vaizdo vietą, pateikiamą „FastTab“ **Medijos kelias**.
4.  „FastTab“ **Generuoti vaizdų URL. skirtus „Excel“** spustelėkite **Generuoti**. **Svarbu:** kai pakeičiamas medijos šablonas, turite spustelėti **Generuoti** prieš norėdami naudodami funkciją Redaguoti programoje „Excel“. [![excel1](./media/excel1.jpg)](./media/excel1.jpg) Dabar matote vaizdų URL, sugeneruotus pagal paskutinį įrašytą medijos šabloną. [![excel2](./media/excel2.png)](./media/excel2.png) **Pastaba:** „Excel“ sugeneruoti URL naudoja nustatyto medijos šablono kelią ir nuostatas. Šios nuostatos apima failų vardų kūrimo nuostatas. Tikimasi, kad faktinius vaizdus nustatysite ne „Dynamics AX“, o vaizdus bus galima nuskaityti iš URL, kurie yra išvesti iš anksčiau nurodyto medijos šablono. Šiuos išvestus URL galite perrašyti, naudodami funkciją Redaguoti programoje „Excel“.
5.  Spustelėkite **Redaguoti programoje „Excel“**.
6.  Atidarę „Microsoft Excel“ darbalapį, spustelėkite **Įjungti redagavimą**, kai būsite paprašyti.
7.  Kai paraginama, spustelėkite **Pasitikėti šiuo priedu** dešiniojoje srityje ir laukite, kol priedas bus įdiegtas. [![Pasitikėti šiuo papildiniu](./media/excel4.jpg)](./media/excel4.jpg)
8.  Jei būsite paraginti prisijungti, įveskite kredencialus, kuriuos naudojate prisijungdami prie HQ. [![Raginimas prisijungti](./media/excel5.png)](./media/excel5.png)
9.  Prisijungę galėsite peržiūrėti įvairių katalogo įrašų vaizdų URL sąrašą.
10. Įvairių objektų prekių vaizdų URL galite redaguoti, įtraukti ir šalinti.
11. Galite perrašyti visų, išskyrus objekto Produktai, vaizdų URL. Modifikuokite esamą vaizdo URL, kad jis naudotų naują vaizdo paskirties URL, ir atnaujinkite failo vardą, įvesdami naują vaizdo failo vardą. Failo vardas turi būti unikalus, siekiant užtikrinti, kad įrašas yra unikalus. [![Perrašyti vaizdų URL programoje „Excel“](./media/excel6.jpg)](./media/excel6.jpg) **Pastaba:** kai objektų Produktai vaizdų URL perrašote naudodami funkciją Redaguoti programoje „Excel“ arba objekto prekių puslapį, MPOS visada kartu rodo medijos šablono vaizdų URL ir perrašytus vaizdų URL.
12. Atlikę keitimus, spustelėkite **Publikuoti programoje „Excel“** ir sukurkite naują tiesioginio susiejimo įrašą.
13. Vėl atidarykite HQ ir spustelėkite **Gerai**.
14. Vykdykite atitinkamas objekto sinchronizavimo užduotis ir patikrinkite objekto puslapio arba MPOS rodinį.

#### <a name="creating-new-records"></a>Naujų įrašų kūrimas

Programoje „Excel“ galite kurti naujus įrašus. Tačiau įsitikinkite, kad pateikiate teisingą informaciją. Pavyzdžiui, norėdami kurti naują katalogo įrašą, įsitikinkite, kad katalogo ID ir katalogo pavadinimas yra teisingi, taip pat suteikite unikalų failo vardą. Unikalus failo vardas yra labai svarbus, nes publikuojant tikrinamas įrašų unikalumas programoje „Excel“. Pirmiausia nukopijuokite informaciją iš katalogo, kuro naują įrašą norite kurti, ir nukopijuokite įrašą. Jums tereikia atnaujinti failo vardą ir URL, nes likusi informacija bus tokia pati. Norėdami kurti objekto Produktai prekes, atlikite tą pačią paprastą procedūrą. „Excel“ darbalapyje nukopijuokite esamą produkto, kurio naują įrašą norite kurti, įrašą, tada pakeiskite vaizdo URL ir failo vardą. Įsitikinkite, kad failo vardas yra unikalus.

#### <a name="deleting-an-existing-record"></a>Esamo įrašo kūrimas

Naikinti galima tik perrašytus vaizdų URL įrašus. Panaikinus vaizdą ir atlikus sinchronizavimą, vaizdas nebebus rodomas puslapyje **Peržiūra** arba MPOS. Vaizdų URL įrašai, kurie išvesti iš medijos šablono, negali būti panaikinti, nes šie įrašai yra visada kiekvieną kartą išvedami iš medijos šablono.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Perrašymas objektų lygio puslapyje Peržiūra

Galite perrašyti pasirinktos bet kurio objekto, išskyrus objektus Produktai, prekės vaizdo URL objekto prekės lygyje naudodami puslapį **Peržiūra**. Objektams Produktai galite naudoti objekto puslapį „Katalogo Produktai“. Šis pavyzdys parodo, kaip perrašyti katalogo vaizdą.

1.  Spustelėkite **Katalogai** &gt; **Medija** &gt; **Vaizdai** ir pasirinkite, kurį katalogo vaizdą norite naujinti.
2.  Spustelėkite **Įtraukti** ir įveskite vaizdo URL, kuriuo perrašysite medijos šablono URL.
3.  Jei norite, kad šis katalogo vaizdas būtų rodomas MPOS, galite jį nustatyti kaip numatytąjį vaizdą.
4.  Spustelėkite **GERAI**. Atnaujintas šio katalogo vaizdo URL ir rodomas rodinys. [![3 peržiūra](./media/preview3.png)](./media/preview3.png)
5.  Taip pat galite peržiūrėti visų perrašytų vaizdų URL rodinius galerijos puslapyje **Katalogo vaizdai**.

**[![4 peržiūra](./media/preview-4.png)](./media/preview-4.png)Pastaba:** šiuo metu galerijoje medijos šablono vaizdų URL vaizdo rodiniai nerodomi. Jei vartotojas naudodamas šį puslapį tiesiogiai pateikia objektų Katalogas, Darbuotojas, Klientas ir Kategorija URL, rekomenduojame nurodyti, kuris vaizdas yra numatytasis vaizdas, nes „Retail Server“ klientai rodo tik vieną vaizdą viename objekte Katalogas, Klientas, Darbuotojas arba Kategorija. Jei vartotojas nenurodo numatytojo vaizdo, sistema nustato numatytąjį vaizdą ir siunčia jį mažmeninės prekybos tarnybos kvietyklei (MPOS arba „Ecommerce“).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Katalogo produkto vaizdų URL perrašymas iš puslapio Peržiūra

Norėdami perrašyti katalogo produkto vaizdų URL, turite naudoti puslapį **Peržiūra**. Negalite naudoti funkcijos Redaguoti programoje „Excel“.

1.  Norėdami perrašyti produkto vaizdus katalogo lygyje, pasirinkite katalogą ir pasirinkite produktą, kurio vaizdą perrašysite.
2.  Spustelėkite **Atributai**.
3.  Kitame puslapyje pasirinkite **Vaizdas**, tada spustelėkite **Redaguoti**. Puslapis **Peržiūra** atidaromas kaip slenkantis dialogo langas.
4.  Spustelėkite **Įtraukti** ir perrašykite vaizdo URL įvesdami naują URL.
5.  Spustelėkite **GERAI**. Dabar galite pamatyti naujo vaizdo rodinį ir nustatyti jį kaip numatytąjį vaizdą.

**[![3 kat.](./media/cat3.png)](./media/cat3.png)Pastaba:** susieję kategorijos vaizdus, turite publikuoti kanalą ir paleisti užduotį Kanalas, siekdami užtikrinti, kad keitimai būtų publikuojami kanalo duomenų bazėje.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Vaizdų rodymo MPOS atjungties režimu nustatymas
MPOS veikia internetiniu režimu (kai MPOS prijungta prie „Retail Server“) arba atjungties režimu (kai nėra ryšio su „Retail Server“ arba tinklu, o operacijos saugomos vietinėje autonominėje duomenų bazėje). Kai MPOS veikia atjungties režimu, ji negali vaizdų gauti iš išorinio vaizdų serverio ir rodyti ir „Retail Server“, nes prarastas ryšys su „Retail Server“. Tačiau jūs vis tiek galite nustatyti vaizdus, kad jie būtų rodomi, kai MPOS veikia atjungties režimu.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Produkto vaizdų rodymo MPOS atjungties režimu nustatymas

Produkto vaizdus, kuriuos reikia naudoti atjungties režimu, galima nustatyti nusiunčiant reikiamą faktinį vaizdą į pagrindinio produkto vaizdą.

1.  Spustelėkite **Produkto informacijos valdymas** &gt; **Produktai** &gt; **Produktai**.
2.  Pasirinkite, kurio produkto autonominį vaizdą nustatyti.
3.  Spustelėkite **Redaguoti**, o tada spustelėkite rodyklę dešiniajame kampe, kad būtų rodoma dešinioji sritis.
4.  „FastTab“ **Produkto vaizdas** spustelėkite **Keisti vaizdą** ir nusiųskite faktinį pasirinkto produkto vaizdą, kuris bus naudojamas atjungties režimu.
5.  Įrašykite ir uždarykite puslapį.
6.  Kol MPOS veikia atjungties režimu, vykdykite užduotį Katalogas HQ, kad įsitikintumėte, jog duomenys buvo bent vieną kartą nusiųsti į autonominę duomenų bazę.
7.  Perjunkite MPOS į atjungties režimą. Turėtumėte matyti nusiųstą konkretaus produkto vaizdą HQ. [![1 neprisijungus](./media/offline1.png)](./media/offline1.png)

 

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Katalogo, kategorijos, darbuotojo ir kliento vaizdų rodymo MPOS atjungties režimu nustatymas

Katalogo, kategorijos, darbuotojo ir kliento vaizdus, kuriuos reikia naudoti atjungties režimu, galima nustatyti įtraukiant reikiamo vaizdo paskirties saitą į galeriją ir nustatant vaizdą kaip numatytąjį pasirinkto objekto vaizdą.

1.  Eikite į katalogą, tada veiksmų srityje spustelėkite **Medija** &gt; **Vaizdai**.
2.  Vykdykite dalyje **Perrašymas objektų lygio puslapyje Peržiūra** nurodytus veiksmus, kad įtrauktumėte išorinio vaizdo URL.
3.  Pažymėkite šį vaizdą kaip numatytąjį katalogo vaizdą, pažymėdami žymės langelį, esantį prie tinklelyje rodomo vaizdo.
4.  Vykdykite užduotį Katalogas. Šis vaizdas dabar bus naudojamas kaip autonominis to katalogo vaizdas MPOS.
5.  Tokiu pat būdu nustatykite kitų objektų, pvz., Kategorija, Darbuotojas arba Klientas, vaizdus.

[![2 neprisijungus](./media/offline2.png)](./media/offline2.png)    




