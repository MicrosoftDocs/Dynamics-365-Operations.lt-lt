---
title: "Gamybos proceso apžvalga"
description: "Šiame straipsnyje apžvelgti gamybos procesai. Jame aprašomi įvairūs gamybos užsakymų, paketinių užsakymų ir „kanban‟ užduočių etapai – nuo užsakymų kūrimo iki finansinio laikotarpio uždarymo."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdStatusListPage, JmgShopSupervisorWorkspace, Kanban, ProdTable, ProdTableOverview
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19832
ms.assetid: 0e83c7ea-feba-4ed6-8717-8b48a3b8804a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 6a33117f454b5b0d109c8a5c460fa218eab5c0f7
ms.lasthandoff: 03/31/2017


---

# <a name="production-process-overview"></a>Gamybos proceso apžvalga

[!include[banner](../includes/banner.md)]


Šiame straipsnyje apžvelgti gamybos procesai. Jame aprašomi įvairūs gamybos užsakymų, paketinių užsakymų ir „kanban‟ užduočių etapai – nuo užsakymų kūrimo iki finansinio laikotarpio uždarymo. 

Produktų gamyba, procesas, kartais dar vadinamas gamybos ciklu, vykdoma atliekant konkrečius veiksmus, kurių reikia norint pagaminti prekę. Ciklas pradedamas sukūrus gamybos užsakymą, užsakymo paketą arba „kanban“. Jis baigiamas pagaminus prekę, parengtą pateikti klientui, arba kitu gamybos etapu. Kiekvienam proceso ciklo veiksmui būtina skirtinga informacija, kad būtų užbaigtas procesas. Užbaigus kiekvieną veiksmą, gamybos užsakyme, užsakymo pakete arba „kanban“ rodoma, kad pasikeitė gamybos būsena. Skirtingiems produktams reikia skirtingų gamybos procesų.  

Modulis **Gamybos kontrolė** yra susijęs su kitais moduliais, pavyzdžiui, **Produkto informacijos valdymas**, **Atsargų valdymas**, **Didžioji knyga**, **Sandėlio valdymas**, **Projekto apskaita** ir **Organizacijos administravimas**. Ši integracija palaiko informacijos srautą, reikalingą galutinei prekei pagaminti.  

Gamybos procesui paprastai įtaką daro išlaidų apskaitos ir atsargų vertinimo būdai, kurie pasirenkami konkrečiam gamybos procesui. „Dynamics 365 for Operations“ palaiko tiek faktines išlaidas („pirmosios įvestos, pirmosios nurašomos“ \[FIFO\]; „paskutinės įvestos, pirmosios nurašomos“ \[LIFO\]; slankusis vidurkis; laikotarpio svertinis vidurkis), tiek standartinius išlaidų metodus. „Lean manufacturing“ įdiegiamas pagal įkainojimo atvirkštine tvarka principą.  

Išlaidų matavimo metodo pasirinkimas taip pat apibrėžia ataskaitų apie medžiagų ir išteklių suvartojimą gamybos proceso metu reikalavimus. Paprastai faktinių išlaidų metodai reikalauja tiksliai kurti užduoties lygio ataskaitas, o periodiniai įkainojimo metodai užtikrina ne tokių smulkių medžiagų ir išteklių suvartojimo ataskaitų kūrimą.

## <a name="mixed-mode-manufacturing"></a>Gamyba mišriuoju režimu
Įvairūs produktai ir gamybos topologijos reikalauja taikyti skirtingus užsakymo tipus. Naudodami „Dynamics 365 for Operations“, dirbdami mišriuoju režimu galite taikyti įvairius užsakymo tipus. Kitaip tariant, gaminant vieną baigtą produktą iki galo, proceso metu galimi visi užsakymo tipai.

-   **Gamybos užsakymas** – tai klasikinis užsakymo tipas, skirtas konkretaus produkto arba produkto varianto nurodytam kiekiui tam tikrą datą gaminti. Gamybos užsakymai pagrįsti komplektavimo specifikacijomis (KS) ir maršrutais.
-   **Paketinis užsakymas** – šis užsakymo tipas naudojamas proceso pramonės šakoms ir atskiriems procesams, kur gamybos konvertavimas pagrįstas formule, kurioje sudėtiniai ir šalutiniai produktai gali būti baigti produktai arba kartu su pagrindiniu produktu, arba vietoje jo. Paketiniuose užsakymuose naudojami tipo **Formulė** KS ir maršrutai.
-   **Kanban** – „Kanban“ naudojami nurodyti pasikartojantys „lean manufacturing“ procesai, pagrįsti gamybos eiga, „kanban“ taisyklėmis ir KS.
-   **Projektas** – gamybos projektas apima produktus ir paslaugas su nurodytu grafiku ir biudžetu. Projekto gamybos dalis gali būti pristatyta per bet kurį kitą užsakymo tipą.

## <a name="manufacturing-principles"></a>Gamybos principai
Norėdami pasirinkti gamybos principą, kuris labiausiai tinka konkrečiam produktui ir susijusiai rinkai, turite atsižvelgti į gamybos bei logistikos ir kliento lūkesčių dėl pristatymo vykdymo laiko reikalavimus.

-   **Gamyba siekiant saugoti** – tai klasikinis gamybos principas, kai produktai gaminami siekiant saugoti remiantis prognoze arba minimalioms atsargoms papildyti (tai paprastai apskaičiuojama pagal prognozę ar istorinius suvartojimo duomenis).
-   **Gamyba užsakyti** – standartiniai produktai gaminami arba baigiami, kad būtų užsakomi. Nors pasirengiama gamybai gali būti taikant gamybos siekiant saugoti principą, vertės grandinės brangūs veiksmai arba veiksmai, kuriuos atliekant kuriami variantai, suaktyvinami pardavimo užsakymo ar perkėlimo užsakymo.
-   **Konfigūravimas užsakymui** – kaip ir taikant gamybos užsakyti principą, galutinės vertės grandinės operacijos skirtos užsakyti. Sukuriamas faktinis produkto variantas nėra iš anksto nustatytas, bet sukuriamas įvedant užsakymą, pagrįstas pardavimo produkto konfigūracijos modeliu. Principui Konfigūravimas užsakymui reikalingas konkrečios produkto eilutės tam tikras proceso susijungimo lygis.
-   **Projektavimas užsakymui** – projektavimo užsakymui procesai paprastai sprendžiami pagal projektą ir paprastai prasideda projektavimo etape. Projektavimo etape suprojektuojamas ir aprašomas faktinis produktas, kurio reikia siekiant įvykdyti užsakymą. Tada gali būti sukurti gamybos užsakymai, paketiniai užsakymai arba „kanban“, kad būtų galima gaminti produktus.

## <a name="overview-of-the-production-life-cycle"></a>Gamybos proceso ciklo apžvalga
Visų mišriojo režimo gamybos užsakymų tipų gamybos cikle galimi toliau nurodyti veiksmai. Tačiau ne visi jie nurodomi kaip aiški užsakymo būsena.

1.  **Sukurta** – galite neautomatiniu būdu kurti gamybos užsakymą, paketinį užsakymą arba „kanban“ arba galite konfigūruoti sistemą, kad jie būtų generuojami pagal įvairius poreikio signalus. Bendrojo planavimo metu patvirtinant suplanuotus užsakymus sukuriami gamybos užsakymai, paketiniai užsakymai arba „kanban“. Kiti poreikio signalai yra pardavimo užsakymai arba iškviesto tiekimo signalai iš kitų gamybos užsakymų ar „kanban“. Esant fiksuoto kiekio „kanban“, poreikio signalai generuojami, kai „kanban“ užregistruoti kaip tušti.
2.  **Įvertinta** – galite apskaičiuoti medžiagų ir išteklių suvartojimo įvertinimus. Įvertinimas generuoja žaliavų, kurių būsena yra **Užsakyta**, atsargų operacijas. Pagrindinių produktų, sudėtinių produktų ir šalutinių produktų gavimai generuojami, kai įvertinami gamybos užsakymai arba paketiniai užsakymai. Jei KS yra eilučių, kurių tipas **Iškviestas tiekimas**, medžiagų pirkimo užsakymai arba subrangos operacijų paslaugos generuojamos ir susiejamos su gamybos užsakymu arba paketiniu užsakymu. Prekės ar užsakymai rezervuojami pagal gamybos užsakymo rezervavimo strategiją, o pagamintų prekių kaina skaičiuojama pagal parametrų nuostatas.
3.  **Suplanuota** – galite planuoti gamybą remdamiesi operacijomis, atskiromis užduotimis, arba abiem šiais punktais.
    -   **Operacijų planavimas** – šis planavimo būdas užtikrina apytikrį ilgalaikį planą. Naudodami šį būdą galite priskirti pradžios ir pabaigos datas gamybos užsakymams. Jei gamybos užsakymai yra pridėti prie maršruto operacijų, galite priskirti juos prie išlaidų centrų grupių.
    -   **Užduočių planavimas** – šis planavimo būdas užtikrina smulkų planą. Kiekviena operacija suskirstoma į atskiras užduotis, nurodomos konkrečios jų datos, laikas ir priskirti operacijų ištekliai. Jei naudojamas ribotas pajėgumas, užduotys priskiriamos operacijų ištekliams remiantis prieinamumu. Galite peržiūrėti ir pakeisti tvarkaraštį Ganto diagramoje.
    -   **„Kanban“ grafikas** – „kanban“ užduotys suplanuotos „kanban“ grafiko srityje ar automatiškai suplanuotos pagal „kanban“ taisyklių automatinio planavimo konfigūraciją.

4.  **Išleista** – galite išleisti gamybos užsakymą arba paketinį užsakymą, kai tvarkaraštis yra baigtas ir medžiagą galima paimti ar paruošti. Medžiagų prieinamumo patikra padeda darbo laiko prižiūrėtojui įvertinti medžiagų prieinamumą gamybos užsakymams ar paketiniams užsakymams. Taip pat galite atspausdinti tokius gamybos užsakymo dokumentus, kaip išrinkimo dokumentai, užduočių kortelė, technologinė kortelė ir maršruto užduotis. Išleidus gamybos užsakymą, užsakymo būsena pasikeičia, rodydama, kad galima pradėti gamybą. Naudojant sandėlio valdymo funkciją, gamybos užsakymo arba paketinio užsakymo išleidimas išleidžia gamybos KS eilutes į sandėlio valdymo sistemą. Sandėlio bangos ir sandėlio darbas generuojami pagal sandėlio nuostatas.
5.  **Parengta**/**paimta** – kai visos medžiagos ir ištekliai buvo suskirstyti gamybos vietoje, gamybos KS eilutės arba „kanban“ eilutės atnaujinamos į būseną **Paimta**. Iškviesto tiekimo užsakymai ir susijęs sandėlio darbas šiame etape paprastai būna atlikti. „Kanban“ korteles arba užduočių korteles, reikalingas pateikti gamybos eigos ataskaitą, reikia priskirti ir spausdinti.
6.  **Pradėta** – pradėję gamybos užsakymą, paketinį užsakymą arba „kanban“, galite pranešti apie medžiagų ir išteklių suvartojimą pagal užsakymą. Sistema gali būti sukonfigūruota, kad automatiškai registruotų medžiagų, priskirtų užsakymui, kai užsakymas pradedamas, ir išteklių suvartojimą. Šis paskirstymas žinomas kaip išankstinis sunaudojimas, iš anksto taikomas sunaudojimas arba automatinis sunaudojimas. Galite patys paskirstyti medžiagas gamybos užsakymams ar paketiniams užsakymams sukurdami papildomų išrinkimo dokumentų žurnalų. Taip pat galite rankiniu būdu paskirstyti darbo ir kitas maršruto išlaidas užsakymui. Jei naudojate operacijų planavimo funkciją, galite paskirstyti šias išlaidas sukurdami technologinės kortelės žurnalą. Jei naudojate darbo planavimo funkciją, galite paskirstyti išlaidas sukurdami darbo kortelės žurnalą. Gamybos užsakymų ar paketinius užsakymus galima pradėti prašomo galutinio kiekio paketais. Gamybos užsakymo, paketinio užsakymo ar „kanban“ sukuriamos užduotys gali būti pradedamos ir pateikiamos jų ataskaitos atskirai žurnaluose, gamybos vykdymo terminale (MES terminale) arba „kanban“ srityse.
7.  Pranešimas apie eigą / užduotys, kurių būsena **Baigta** – naudokite MES terminalą, gamybos žurnalus, „kanban“ sritis arba mobiliojo nuskaitymo funkcijas norėdami pranešti apie gamybos eigą pagal užduotį arba išteklių. Medžiagų ir išteklių suvartojimas bus užregistruotas, o susijusių „kanban“, gamybos užsakymų ir paketinių užsakymų būsena gali būti atnaujinta į **Gauta** arba **Paskelbta, kad užbaigta**. Gali būti sukurtas sandėlio atidėjimo darbas, atsižvelgiant į sandėlio konfigūraciją.
8.  **Paskelbta, kad užbaigta** (produkto gavimas) – kai gamybos užsakymas arba paketinis užsakymas paskelbiamas baigtu, pagamintų prekių kiekis yra atnaujinamas atsargų modulyje. Šis kiekis apima atitinkamų sudėtinių ir šalutinių produktų kiekį. Jei naudojate vykdomo proceso (VP) apskaitą, sugeneruojamas DK žurnalas, skirtas VP sąskaitoms sumažinti ir pagamintų prekių atsargoms padidinti. Kai apskaičiuojamos gamybos užsakymo išlaidos, užregistruojamos faktinės gamybos išlaidos. Jei medžiagų ir darbo išlaidos, susietos su gamyba, nėra paskirstytos žurnale arba išankstinio suvartojimo fiksavime, jos gali būti automatiškai paskirstomos. Paskirstymas pagal atgalinį suvartojimą apima vėlesnio atsargų operacijos procesų nustatymą. Jei gamybos užsakymas yra užbaigtas, pažymėkite žymės langelį **Baigti užduotį**, norėdami pakeisti būseną į **Baigta**. Kitu atveju lauką palikite tuščią ir įjunkite pranešimą apie papildomą apdorojamą kiekį.
9.  **Kokybės vertinimas** – produkto gavimas gali suaktyvinti kokybės užsakymų kūrimą, atsižvelgiant į tikrinimo procesų ir kokybės taisyklių, nustatomų konkretiems produktams, konfigūraciją. Kadangi pagal kokybės užsakymą galima atnaujinti atsargų būseną arba patikrintų produktų paketo atributus, kokybės vertinimas yra privalomas procesas daugelyje pramonės šakų.
10. **Atidėti** ir **Siųsti pagal užsakymą** – gavus produktą ir įvertinus kokybę pasirinktinė darbo atidėjimo funkcija nukreipia gautus produktus į kitą suvartojimo tašką, į pagamintų prekių sandėlio ar siuntimo zoną, jei yra užsakymo siuntimo reikalavimų.
11. **Baigta** – prieš gamybos pabaigą apskaičiuojamos faktinės pagaminto prekių kiekio išlaidos. Visos numatytosios medžiagų, darbo ir papildomos išlaidos yra anuliuojamos ir pakeičiamos faktinėmis išlaidomis. Jei pasirenkate žymės langelį **Baigti užduotį**, paleidus išlaidų apskaičiavimą, gamybos užsakymo būsena pasikeičia į **Baigta**. Ši būsena neleidžia registruoti jokių papildomų išlaidų užbaigtam gamybos užsakymui.
12. **Laikotarpio pabaiga** – kai kuriems išlaidų apskaitos principams, pvz., laikotarpio vidurkiui, įkainojimui atvirkštine tvarka, FIFO arba LIFO, reikia atlikti periodiškai pasikartojančias operacijas, kad būtų uždarytas atsargų arba ataskaitinis laikotarpis. Paprastai sistema bando pranešti apie visų medžiagų ir išteklių suvartojimą ir atsargų bei atliekų taisymus prieš uždarant laikotarpius. Šios ataskaitos paprastai pateikiamos naudojant atsargų perkėlimo žurnalus ar koregavimo žurnalus. Tikslas yra įvertinti valdymo vienetų ekonominį efektyvumą per tam tikrą laikotarpį. Kai kuriais atvejais, kai vykdomi ilgalaikiai gamybos užsakymai, apimantys kelis finansinius ataskaitinius laikotarpius, naudojami gamybos žurnalai siekiant pranešti apie gamybos eigą ir išteklių suvartojimą laikotarpio pabaigoje.


<a name="see-also"></a>Taip pat žiūrėkite
--------

[Gamybos grįžtamasis ryšys](production-feedback.md)

[Produkto konfigūracijos modeliai](../pim/product-configuration-models.md)

[„Lean manufacturing“](lean-manufacturing-overview.md)




