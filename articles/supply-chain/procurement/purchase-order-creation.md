---
title: "Pirkimo užsakymų sukūrimas"
description: "Šiame straipsnyje aprašomas pirkimo užsakymo kūrimo neautomatiniu būdu procesas ir parinktys."
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, Retail
ms.custom: 93053
ms.assetid: 25b1c9f1-20f8-4cf5-b87c-876e32f68846
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 1cf09af8de2a312ce17cd88ccc4d8c5c2c051927
ms.contentlocale: lt-lt
ms.lasthandoff: 09/29/2017

---

# <a name="create-purchase-orders"></a>Pirkimo užsakymų sukūrimas

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]


Šiame straipsnyje aprašomas pirkimo užsakymo kūrimo neautomatiniu būdu procesas ir parinktys.

Kai sukuriate pirkimo užsakymą (PU), bendroji informacija apie visą užsakymą yra nurodyta PU antraštėje, ir tada galite įtraukti vieną ar daugiau PU eilučių. Šiame straipsnyje aprašomos kai kurios dažniausiai naudojamos parinktys.  

Taip pat PU galite kurti kopijuodami eilutes iš kito PU dokumento arba pardavimo užsakymo. Šiuo atveju galite pakeisti ženklą atsargose taip, kaip pakeičiate ženklą SF siekdami nurodyti kreditą.  

Nors PU galite kurti neautomatiniu būdu, paprastai jie generuojami vykdant kitus procesus. Užsakymus galima automatiškai kurti pagal kitus dokumentus, pvz., paraiškas. Arba galima juos sukurti kaip pagrindinio planavimo proceso dalį naudojant suplanuotus PU. Jei naudojate pirkimo sutartis, PU galima sukurti atliekant veiksmą **Išleidimo užsakymas**. Taip pat PU galima automatiškai kurti pažangesniais būdais. Pvz., užsakymus galite kurti, kai naudojate tiesioginio pristatymo arba vidinės įmonės užsakymų grandines.

## <a name="creating-a-purchase-order-header"></a>Pirkimo užsakymo antraštės kūrimas
Kai sukuriate naują PU, rodomas dialogo langas, kuriame galite įvesti bendriausią PU antraštės informaciją. Kai spustelite **Gerai** norėdami uždaryti dialogo langą, sukuriamas užsakymas ir tada galite nurodyti papildomą antraštės informaciją.  

Kurdami PU pirmiausia turite atsižvelgti į užsakymo tipą. Dažniausiai naudojamas tipas **Pirkimo užsakymas**. Tačiau, jei reikalinga kredito SF, galite naudoti tipą **Grąžintas užsakymas**.  

Tiekėją turite nurodyti lauke **Tiekėjo kodas**. Šiame lauke galite nurodyti tiekėjo kodą arba pavadinimą. Jei tiekėjas pristato iš kelių vietų, bet naudoja vieną SF kodą, galite tą SF kodą pasirinkti lauke **SF kodas** ir tada naudoti jį su įvairiais tiekėjo kodais. Jei turite kurti produktų, kurie nebus užsakyti kelis kartus, PU, galite naudoti parinktį **Vienkartinis tiekėjas**. Naudojant šią parinktį automatiškai sukuriamas naujas tiekėjo kodas, kuris pažymimas kaip vienkartinis kodas, kad modulyje **Mokėtinos sumos** vėliau būtų galima vykdyti vienkartinių kodų valymo procesą. Pasirinkus tiekėjo kodą, daugelyje PO antraštės laukų naudojamos numatytosios reikšmės, nuskaitomos iš su tiekėjo kodu susietos informacijos. Pvz., iš tiekėjo informacijos nukopijuojami numatytoji pristatymo vieta ir numatytasis sandėlis. Tačiau, jei pirkimas siejamas su kita vieta, šias numatytąsias reikšmes galite perrašyti.  

Jei tiekėjas pateikia užsakymo nuorodos numerį, šią informaciją galite įrašyti lauke **Tiekėjo nuoroda**. Jei kuriate grąžinimo užsakymą, lauke **RMA** turite nustatyti reikšmę, kad nurodytumėte tiekėjo autorizavimo numerį, naudojamą grąžinimui apdoroti.  

Jei pirkimo sutartis susijusi su užsakymu, šią informaciją turite nurodyti lauke **Pirkimo sutartis**.  

PU antraštėje taip pat pateikiama informacija apie mokesčius, taikomus visam užsakymui, o ne atskiroms eilutėms. Mokesčius galima automatiškai įtraukti į užsakymą, jei buvo nustatyti tiekėjo arba tiekėjo mokesčių grupės automatinio mokesčiai. Mokesčius į užsakymo antraštę taip pat galite įtraukti neautomatiniu būdu, veiksmų srityje spustelėdami **Prižiūrėti išlaidas**.

## <a name="adding-purchase-order-lines"></a>Pirkimo užsakymo eilučių įtraukimas
PO gali būti skirti fiziniams produktams arba paslaugoms. Atsargų modelio grupės parametras nustato, ar tam tikras prekės numeris taikomas produktui, ar paslaugai. Paprastai perkama prekė nurodoma naudojant prekės numerį. Tačiau, jei užsakymas skirtas tiesiogiai vartojamiems produktams arba paslaugoms, prekę taip pat galite nurodyti naudodami įsigijimo kategoriją.  

PU eilutėse yra daug laukų, bet daugelyje šių laukų nustatytos numatytosios reikšmės arba reikšmės, nuskaitytos iš užsakymo antraštės. Papildomi laukai nustatomi pasirinkus produktą arba paslaugą. Laukai, kurie dažniausiai nustatomi neautomatiniu būdu, apima prekės numerio, kiekio ir pageidaujamos pristatymo datos laukus. Informacija apie vieneto kainą ir nuolaidas taip pat yra labai svarbi, bet šių laukų reikšmės dažnai nustatomos pagal prekybos sutartis arba pirkimo sutartis.  

Pasirinkus produktą, galima ieškoti viso produkto pavadinimo arba jo dalies, o ne prekės numerio. Jeigu yra keli produkto variantai, pavyzdžiui, skirtingo dydžio produktai, galite pamatyti turimų variantų apžvalgą, naudodami funkciją **Įtraukti eilutes** arba lauko **Varianto numeris** peržvalgos funkciją.  

Dažnai turėsite nurodyti keletą pasirinktos PU eilutės prekės dimensijų. Dimensijos, kurias reikia nurodyti, priklauso nuo dimensijų grupių, priskirtų bendrojo produkto aprašui. Pavyzdžiui, dažnai turėsite nurodyti teritoriją ir sandėlį, kad nurodytumėte vietą, į kurią produktas turėtų būti pristatytas. Produkto variantai identifikuojami nurodant varianto numerį arba įvedant vienos ar daugiau produkto dimensijų reikšmes, pavyzdžiui, spalvą, dydį, konfigūraciją arba stilių. Sekimo dimensijos, pvz., paketo ir serijos numeriai, suteikia galimybę unikaliai identifikuoti kiekvieną atsargų partiją. Sukūrę užsakymą, galite užfiksuoti užsakymo dimensijų reikšmes, naudodami veiksmą **Registracija**. Pavyzdžiui, jūs užsakėte penkių prekės vienetų kiekį. Vėliau nurodote, kad trys iš šių vienetų bus juodos, o du – mėlynos spalvos. Šis metodas yra alternatyvus būdas dimensijų informacijai pristatymo registravimo metu užfiksuoti.  

Galite patikrinti laikomų produktų atsargų operacijos būsenos informaciją. Pavyzdžiui, galbūt norėsite patikrinti turimas atsargas, kad lengviau nuspręstumėte, kiek prekių užsakyti. Arba galbūt norėsite peržiūrėti užsakyto kiekio atsargų būseną, kad pamatytumėte, ar įvyko gavimo registracija.  

PU eilutėje, kuri naudojama siekiant produktą grąžinti tiekėjui, kiekis bus neigiamas. Galite pasirinkti grąžinti konkrečią partiją, naudodami veiksmą **Rezervavimas**.  

Kartais galite norėti padalinti užsakytą kiekį, kad skirtingos jų dalys būtų pristatomos skirtingu laiku. Šiuos pristatymus galite nustatyti naudodami veiksmą **Pristatymo grafikas**, kurį galima rasti rodinio **Eilutės** meniu **pirkimo užsakymo eilutė**.  

Mokesčius galima automatiškai įtraukti į PU eilutes, jei buvo nustatyti tiekėjo arba tiekėjo mokesčių grupės ir prekės arba prekės mokesčių grupės automatinio mokesčiai. Tačiau labiau įprasta mokesčius įtraukti užsakymo eilutės lygiu neautomatiniu būdu. Norėdami įtraukti mokestį, atidarykite puslapį **Prižiūrėti išlaidas** naudodami rodinio **Eilutės** meniu **Finansai** veiksmą **Prižiūrėti išlaidas**. Mokesčių įtraukimo tiesiogiai užsakymo eilutės lygiu privalumas yra tai, kad mokestį galima paskirstyti kaip atsargų savikainą. Norėdami nustatyti sąskaitos produkto savikainos mokesčių kodus, naudokite debeto parinktį **Prekė**. Šių tipų mokesčiai turi būti paskirstyti iš PU antraštės į eilutes, kad būtų galima patvirtinti užsakymą. Pavyzdžiui, galite mokesčius paskirstyti pagal kiekį kiekvienoje eilutėje. Mokesčių kategorijai taip pat turi įtakos, kaip mokesčiai yra apskaitomi. Pvz., fiksuoti mokesčiai nurodo fiksuotą sumą, o mokesčių procentinė dalis apskaičiuojami kaip užsakymo eilutės grynosios sumos procentinė dalis. PU galima priskirti kroviniui, o krovinys gali apimti transportavimo išlaidų numatomų išlaidų įvertinimą. Šias išlaidas galite iš krovinio paskirstyti atgal į PU eilutes.

## <a name="purchase-order-actions"></a>Pirkimo užsakymo veiksmai
Įtraukę antraštę ir eilutes į PU, dažnai turėsite atlikti papildomus veiksmus, kad galėtumėte užsakymą patvirtinti. Kadangi galima naudoti daug parinkčių, gali būti naudinga naudoti funkciją [Veiksmo ieška](../../fin-and-ops/get-started/action-search.md), norint surasti atitinkamą meniu elementą.  

Galite konfigūruoti užsakymo produktus, kad jie turėtų papildomas prekes. Papildomos prekės yra produktai, kuriuos privaloma arba galima nupirkti kartu su kitais produktais. Papildomus produktus galima nemokamai pridėti kaip susijusius produktus arba galite turėti galimybę nuspręsti, ar juos įtraukti į užsakymą, ar ne. Papildomas prekes galite peržiūrėti įtraukę kiekvieną užsakymo eilutę. Tačiau tikriausiai patogiau bus peržiūrėti ir įtraukti visų užsakymo eilučių atitinkamas papildomas prekes, naudojant puslapį **Papildomos prekės**, kurį galima atidaryti iš veiksmų srities.  

Nuolaidos paprastai įtraukiamos į eilutes, jas kuriant. Tačiau keletas nuolaidų taikomos visam užsakymui.

-   Veiksmu **Bendra nuolaida** apskaičiuojamas visam užsakymui taikytinas bendros nuolaidos procentinis dydis. Nepainiokite šios nuolaidos su mokėjimo nuolaidos procentiniu dydžiu. Mokėjimo nuolaidos taikomos, kai SF yra apmokėta, ir jos priklauso nuo mokėjimo sudengimo iki tam tikros datos.
-   Jei kelių eilučių nuolaida taikoma, turite naudoti veiksmą **Kelių eilučių nuolaida**, norėdami ją apskaičiuoti ir priskirti užsakymui. Kelių eilučių nuolaidos yra nuolaidos, kurias galima siūlyti, jei įvairūs užsakymo produktai viršija bendrąją ribinę reikšmę. Šio tipo nuolaidą naudoja tik keletas įmonių.

Mokesčiai, kurių mokesčių tipas naudoja debeto tipą **Prekė**, turi būti priskirti eilutės lygiu, kad užsakymą būtų galima patvirtinti. Šiuos mokesčius gali būti patogu priskirti užsakymo antraštės lygiu, kad būtų galima nurodyti mokesčio bendrąją sumą. Tačiau šiuo atveju mokestis turi būti paskirstytas kiekvienoje eilutėje, kad būtų užsakymą būtų galima patvirtinti. Galite naudoti veiksmą **Paskirstyti išlaidas**, norėdami sumas atskirti nuo mokesčių, kurie antraštės lygiu priskirti užsakymo eilutėms. Mokesčiai gali būti skaidomi pagal kiekvienos eilutės grynąją sumą, pagal užsakytą kiekį arba tolygiai užsakymo eilutėse. Paskirsčius mokesčius į eilutes, mokestis yra pašalintas iš užsakymo antraštės.  

PU galima sukonfigūruoti taip, kad biudžeto lėšas būtų privaloma paskirstyti užsakymui, kad norint jį apdoroti. Šiuo atveju galite naudoti veiksmą **Biudžeto patikra** biudžetui paskirstyti.  

PU baigimą gali tekti atidėti. Pavyzdžiui, gali reikėti papildomos informacijos apie produktus ar paslaugas arba gali reikėti autorizuoti išlaidas. Užsakymą galima sulaikyti keletu būdų. Pavyzdžiui, galite prieš patvirtindami užsakymą palaukti. Arba, jei naudojama keitimų valdymo darbo eiga, galite neteikti užsakymo patvirtinti. Jei turite užblokuoti visus konkretaus tiekėjo užsakymus, tiekėjo bendruosiuose duomenyse taip pat galite apdorotino tiekėjo būseną pažymėti kaip **Sulaikyta**. Taip pat yra aplinkybių, kurios gali neleisti užsakymo apdoroti. Pvz., apdorojimas gali būti neleidžiamas, jei viršijamos kredito ribos arba jei reikiamų biudžeto lėšų nėra.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Pirkimo užsakymo apžvalga](purchase-order-overview.md)

[Pirkimo užsakymo patvirtinimas](purchase-order-approval-confirmation.md)

[Produkto gavimas pagal pirkimo užsakymą](product-receipt-against-purchase-orders.md)

[Tiekėjo SF apžvalga](../../financials/accounts-payable/vendor-invoices-overview.md)




