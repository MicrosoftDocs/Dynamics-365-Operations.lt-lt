---
title: "Skambučių centro kanalo nustatymas"
description: "Šioje temoje pateikiama informacija apie tai, kaip apdoroti skambučių centrų užsakymus naudojant „Microsoft Dynamics 365 for Retail“."
author: josaw1
manager: AnnBe
ms.date: 04/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0d64a27aa8aed10c210ca3c2956dce67f8d634b8
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-a-call-center-channel"></a>Skambučių centro kanalo nustatymas

[!INCLUDE [banner](includes/banner.md)]

Programoje „Microsoft Dynamics 365 for Retail“ įmonė gali nurodyti keletą skambučių centro kanalų. Skambučių centro kanalai konfigūruojami pasirinkus **Mažmeninė prekyba** \> **Kanalai** \> **Skambučių centrai** \> **Visi skambučių centrai** ir jie būdingi konkrečiam juridiniam subjektui.

Sukūrus naują skambučių centro kanalą jam sistemingai priskiriamas valdymo vieneto numeris. Kadangi skambučių centrai kuriami kaip valdymo vienetai, vartotojai gali susieti skambučių centro kanalą su įvairiomis mažmeninės prekybos funkcijomis, pavyzdžiui, asortimentais, katalogais ir konkrečiais pristatymo būdais.

Numatytasis sandėlis gali būti konfigūruojamas skambučių centro kanale. Tame kanale sukūrus pardavimo užsakymų numatytasis sandėlys pardavimo užsakymo antraštėje įvedamas automatiškai, išskyrus tais atvejais, kai nurodomas kitas pardavimo užsakymui pasirinkto kliento sandėlis. Tokiu atveju kliento sandėlis įvedamas pagal numatytuosius nustatymus.

Norėdami naudotis skambučių centro funkcijomis, vartotojai turi būti susieti su skambučių centro kanalu. Visi vartotojo srityje Mažmeninė prekyba sukurti pardavimo užsakymai automatiškai susiejami su to vartotojo skambučių centro kanalu. Šiuo metu nėra galimybės vieną vartotoją vienu metu susieti su keliais skambučių centro kanalais.

Skambučių centro kanale taip pat galima sukonfigūruoti el. paštu siunčiamo pranešimo šabloną. Šablone nurodomas naudojantis skambučių centro kanalu pateikiantiems užsakymus klientams siunčiamų el. pašto šablonų rinkinys. Galima sukonfigūruoti, kad el. paštas būtų paleidžiamas vykstant tam tikriems sistemos įvykiams, pvz., pateikiant arba išsiunčiant užsakymą.

Norinti, kad pardavimus būtų galima tinkamai apdoroti naudojantis skambučių centro kanalu, būtina nurodyti tinkamus kanalo [mokėjimo](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-payments) ir pristatymo būdus.

Skambučių centro kanalo lygiu galite nurodyti kitas numatytąsias su finansinėmis dimensijomis susijusias vertes, kurios bus susiejamos su to kanalo sukurtais užsakymais.

## <a name="options-for-order-processing-behavior"></a>Užsakymo apdorojimo elgsenos parinktys

Šie trys skambučių centro konfigūracijos parametrai turi didelės įtakos naudojantis tuo skambučių centru sukurtiems pardavimo užsakymams taikomoms funkcijoms: **Įgalinti užsakymo baigimą**, **Įgalinti tiesioginį pardavimą** ir **Įgalinti užsakymo kainos kontrolę**.

### <a name="enable-order-completion"></a>Įgalinti užsakymo baigimą

Skambučių centro kanalo nustatymas **Įgalinti užsakymo baigimą** turi didelės įtakos įvestų to kanalo pardavimo užsakymų apdorojimo eigai. Įjungus šį nustatymą prieš patvirtinant pardavimo užsakymus visi jie turi būti patikrinami vadovaujantis tam tikru taisyklių rinkiniu. Šios taisyklės paleidžiamos paspaudus pardavimo užsakymo puslapio srityje Veiksmų sritis esantį mygtuką **Baigti**. Visiems įjungus nustatymą **Įgalinti užsakymo baigimą** sukurtiems pardavimo užsakymams privalo būti atliktas užsakymo baigimo procesas. Vykstant šiam procesui vykdomas mokėjimo fiksavimas ir mokėjimo patvirtinimo logika. Vykstant užsakymo pateikimo procesui ne tik vykdomas mokėjimas, taip pat gali būti sukuriami jūsų sistemoje konfigūruojami [apgaulingi čekiai](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/set-up-fraud-alerts). Tokie elementai kaip užsakymai, kurių nepavyksta apmokėti, taip pat apgaulingos patikros sustabdomi ir jų negalima paleisti tolesniam apdorojimui (pvz., paėmimui arba siuntimui) kol neišsprendžiama sustabdymą sukėlusi problema.

Įjungus skambučių centro kanalo nustatymą **Įgalinti užsakymo baigimą**, jei pardavimo užsakyme įvedami eilutės elementai ir kanalo vartotojas bando uždaryti pardavimo užsakymo formą arba pereiti prie kitos formos nepasirinkęs **Užbaigti**, sistema vykdo užsakymo baigimo procesą – atidaromas pardavimo užsakymo apžvalgos puslapis ir reikalaujama, kad vartotojas tinkmai pateiktų užsakymą. Jei užsakymo negalima tinkamai pateikti kartu su mokėjimu, vartotojas gali pasinaudoti funkcija [užsakymų sulaikymas](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/work-with-order-holds) ir sulaikyti užsakymą. Jei vartotojas bando atšaukti užsakymą, jis turi būti atšaukiamas tinkamai naudojantis funkcija Atšaukti arba Naikinti, priklausomai nuo to, kokia funkcija leidžiama pagal vartotojo saugą.

Jei įjungtas skambučių centro kanalo nustatymas **Įgalinti užsakymo baigimą** bus pažymėtas užsakymo laukas **Mokėjimo būsena**. Pateikus pardavimo užsakymą sistema apskaičiuoja **Mokėjimo būseną**. Sistema praleidžia ir toliau apdoroja (pvz., paima ir išsiunčia) tik tuos užsakymus, kurių mokėjimo būsena Patvirtinta. Jei mokėjimai atmesti, įgalinama išsamios užsakymo būsenos žymė **neapdoroti** ir užsakymas sulaikomas, kol bus išspręsta mokėjimo problema.

Be to, jei įjungtas nustatymas **Įgalinti užsakymo baigimą**, darbuotojams sukūrus pardavimo užsakymus ir įjungus eilutės elemento įvedimo režimą pagrindinėje pardavimo užsakymo antraštėje bus rodomas laukas **Šaltinis**. Laukas **Šaltinis** naudojamas norint pagal tiesioginio rinkodaros pardavimo scenarijų fiksuoti [katalogo šaltinio kodą](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/call-center-catalogs). Pagal šį kodą gali būti nustatomos specialios kainos ir nuolaidos.

Net jei nustatymas **Įgalinti užsakymo baigimą** išjungtas, vartotojai vis tiek gali taikyti šaltinio kodą pardavimo užsakymui. Tačiau, norėdami įjungti lauką **Šaltinis**, pirmiausia jie turi atidaryti pardavimo užsakymo antraštės informaciją. Kitaip tariant, reikia atlikti keletą papildomų spustelėjimų. Ta pati elgsena taikoma naudojantis, pavyzdžiui, siuntimo baigimo ir pagreitintų užsakymų funkcijomis. Šios funkcijos taikomos visiems skambučių centre sukurtiems užsakymams. Tačiau kai įjungtas nustatymas **Įgalinti užsakymo baigimą**, vartotojai gali matyti šių funkcijų konfigūraciją pardavimo antraštėje įjungę eilutės įrašo rodinį. Norėdami rasti tinkamus nustatymus ir laukus, jie neturi gilintis į pardavimo užsakymo antraštėje nurodomas detales.

### <a name="enable-direct-selling"></a>Įgalinti tiesioginį pardavimą

Jei įjungtas skambučių centro kanalo nustatymas **Įgalinti tiesioginį pardavimą**, vartotojai gali pasinaudoti srities Mažmeninė prekyba papildomo ir kryžminio pardavimo funkcijomis. Tokiu atveju įvedant užsakymą rodomi iššokantieji langai ir siūloma pasirinkti kitus produktus, kuriuos skambučių centro vartotojas galėtų pasiūlyti klientui. Produkai siūlomi pagal ką tik pardavimo užsakymo eilutėje nurodytą užsakytą produktą. Šiuo metu papildomo ir kryžminio pardavimo pasiūlymai konfigūruojami prekės lygiu pagal produktus ar katalogus. Jei skambučių centro kanalo nustatymas **Įgalinti tiesioginį pardavimą** išjungtas, įvedant užsakymą iššokantieji langai nerodomi net jei buvo nurodyta tinkama užsakomos prekės papildomo arba kryžminio pardavimo vertė.

Jei nustatymas **Įgalinti tiesioginį pardavimą** įjungtas, taip pat įjungiami pardavimo užsakymo įvedimo puslapio scenarijai bei vaizdų funkcijos. Tokiu atveju atliekant užsakymo įvedimą dešinėje puslapio pusėje matoma informacijos sritis. Šioje srityje gali būti rodomi su bendruoju užsakymo įvedimo procesu susiję scenarijai, taikytas katalogo šaltinio kodas arba su užsakomomis prekėmis susiję scenarijai. Be to, vaizdų srityje gali būti rodomas užsakomų prekių paveikslėlis, jei toks paveikslėlis nurodytas produkto sąrankoje.

### <a name="enable-order-price-control"></a>Įgalinti užsakymo kainos kontrolę

Įjungus nustatymą **Įgalinti užsakymo kainos kontrolę** įvedant užsakymą prekės pardavimo kainą gali keisti tik įgaliotieji vartotojai. Keičiant kainą turi būti paisoma nurodytų leistinų nuokrypių. Vartotojai, kuriems nebuvo suteiktas tinkamas įgaliojimas, privalo pateikti prašymą dėl kainos keitimo. Vykstant sistemos darbo eigoms užklausa apdorojama, peržiūrima ir patvirtinama.

## <a name="channel-users"></a>Kanalo vartotojai

Nurodžius skambučių centro kanalą to kanalo vartotojus būtina susieti su skambučių centru. To nepadarius skambučių centro sistemoje naudoti negalima. Vartotojams prisijungus prie srities Mažmeninė prekyba ir su užsakymo įvedimu susijusiame puslapyje įvedus pardavimo užsakymus arba gražinimo užsakymus jų vartotojo ID tikrinama pagal skambučių centro kanalo konfigūraciją. Jei vartotojas susietas su konkrečiu skambučių centro kanalu, vartotojo sukurtiems užsakymams būdingi to kanalo bruožai ir numatytosios vertės.

Pagal numatytuosius nustatymus visų to skambučių centro vartotojų sukurtų pardavimo užsakymų antraščių žymė **Mažmeninė prekyba** įjungta. Tada pateikiant užsakymus galima pasinaudoti sistemos mažmeninei prekybai būdingos kainos ir nuolaidos funkcijomis.

Su skambučių centro kanalu nesusieti vartotojai naudojasi standartinėmis „Microsoft Dynamics 365 for Finance and Operations“ užsakymo įvedimo funkcijomis. Šių vartotojų pildant pardavimo užsakymo įvedimo formą įvestų užsakymų sistema nepripažįsta kaip mažmeninės prekybos užsakymų. Be to, šiems šių vartotojų įvestiems užsakymams netaikomos jokios baigto užsakymo apdorojimo taisyklės, mažmeninės prekybos kainų logika ar kiti atliekant skambučių centro kanalo konfigūraciją arba nurodant skambučių centro sistemos parametrus galimi taikyti kriterijai.

Baigę konfigūruoti skambučių centro kanalą ir nurodę kanalo vartotojus, siekdami užtikrinti reikiamą sistemos elgseną, įsitikinkite, kad srityje **Mažmeninė prekyba** \> **Kanalo sąranka** \> **Skambučių centro sąranka** \> **Skambučių centro parametrai** nurodyti visi reikiami skambučių centro parametrai. Įsitikinkite, kad būtų nurodomos ir susijusios numeracijos.

