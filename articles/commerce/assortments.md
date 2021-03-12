---
title: Asortimento valdymas
description: Šioje temoje paaiškinamos pagrindinės asortimento valdymo sprendime „Dynamics 365 Commerce“ sąvokos ir nurodoma, apie ką reikėtų pagalvoti diegiant projektą.
author: jblucher
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.openlocfilehash: 981d1c604a7ed461f207e78c8c7f073aff03be9e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980003"
---
# <a name="assortment-management"></a>Asortimento valdymas

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Peržiūrėti

Sprendime „Dynamics 365 Commerce“ galima naudoti *asortimentus*, kurie leidžia valdyti produktų prieinamumą įvairiuose kanaluose. Asortimentais nustatoma, kurių produktų galima įsigyti konkrečiose parduotuvėse ir konkrečiu laikotarpiu.

Sprendime „Commerce“ asortimentas yra vieno ar kelių kanalų (arba kanalų grupių, kai naudojamos organizacijos hierarchijos) susiejimas su vienu ar keliais produktais (ar produktų grupėmis, kai naudojamos kategorijų hierarchijos).

Bendrąjį kanalo produktų derinį nustato tam kanalui priskirti publikuoti asortimentai. Todėl viename kanale galite sukonfigūruoti kelis aktyvius asortimentus.

### <a name="basic-assortment-setup"></a>Pagrindinė asortimentų sąranka

Tolesniame pavyzdyje kiekvienai parduotuvei sukonfigūruotas unikalus asortimentas. Šiuo atveju 1 parduotuvėje galima įsigyti tik 1 produktą, o 2 parduotuvėje – tik 2 produktą.

![Kiekvieną produktą galima įsigyti vienoje parduotuvėje](./media/Managing-assortments-figure1.png)

Kad 2 produktą būtų galima įsigyti 1 parduotuvėje, jį galite įtraukti į 1 asortimentą.

![2 produktas įtrauktas į 1 asortimentą](./media/Managing-assortments-figure2.png)

Arba galite 1 parduotuvę įtraukti į 2 asortimentą.

![1 parduotuvė įtraukta į 2 asortimentą](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a>Organizacijų hierarchijos

Situacijose, kai keliuose kanaluose naudojami tokie patys produktų asortimentai, asortimentus galite sukonfigūruoti naudodami organizacijos hierarchiją Prekybos asortimentas. Įtraukus šios hierarchijos mazgus, bus įtraukti visi tų mazgų kanalai ir antriniai mazgai.

![Organizacijos hierarchija](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a>Produkto kategorijos

Panašiai produktų pusėje produktų grupių galite įtraukti naudodami produktų kategorijų hierarchijas. Galite konfigūruoti asortimentus įtraukdami vieną ar kelis kategorijų hierarchijų mazgus. Šiuo atveju į asortimentą bus įtraukti visi to kategorijos mazgo ir jo antrinių mazgų produktai.

![Produkto kategorijos](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a>Neįtraukti produktai ar kategorijos

Be produktų ir kategorijų įtraukimo į asortimentus galite naudoti parinktį Neįtraukti, kad apibrėžtumėte konkrečius produktus ar kategorijas, kurių į asortimentus nereikėtų įtraukti. Tolesniame pavyzdyje į konkrečią kategoriją norite įtraukti visus produktus, išskyrus 2 produktą. Šiuo atveju asortimento nebūtina apibrėžti po vieną produktą ar kurti papildomų kategorijų mazgų. Vietoj to galite tiesiog įtraukti kategoriją, tačiau neįtraukti produkto.

> [!NOTE]
> Jei pagal apibrėžimą produktas viename ar keliuose asortimentuose yra ir įtrauktas, ir neįtrauktas, jis bus visada laikomas neįtrauktu.

![Produktas neįtrauktas](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a>Visuotiniai ir išleisti produktai

Asortimentai yra apibrėžiami visuotiniu lygiu ir juose gali būti kanalų iš kelių juridinių subjektų. Į asortimentus įtrauktus produktus ir kategorijas taip pat bendrai naudoja juridiniai subjektai. Tačiau produktas turi būti išleistas, kad jį būtų galima faktiškai parduoti, užsakyti, skaičiuoti ar gauti kanale (pavyzdžiui, elektroniniame kasos aparate \[EKA\]). Todėl nors dvi parduotuvės skirtinguose juridiniuose subjektuose gali bendrai naudoti asortimentą su tais pačiais produktais, juos įsigyti galima, tik jei jie išleisti tiems juridiniams subjektams.

### <a name="dynamic-and-static-assortments"></a>Dinaminiai ir statiniai asortimentai

Asortimentus galima apibrėžti naudojant konkrečius kanalus ir produktus arba įtraukiant organizacijos vienetų ir kategorijų. Asortimentai su nuorodomis į šias grupes laikomi dinaminiais asortimentais. Jei, asortimentui esant aktyviam, pakinta šių grupių apibrėžtis ar turinys, taip pat pakinta asortimento apibrėžtis.

Pavyzdžiui, asortimentas iš pradžių apibrėžiamas ir publikuojamas taip, kad nurodytų produktų kategoriją. Jei vėliau į kategoriją įtraukiama papildomų produktų, jie automatiškai įtraukiami į esamo asortimento apibrėžtį. Į asortimentą įtraukti produktų nebūtina rankiniu būdu. Panašiai, jei organizacijos vienetas įtraukiamas į kitą mazgą, organizacijos vieneto asortimentas automatiškai pakoreguojamas pagal šią apibrėžtį

### <a name="stopped-products"></a>Sustabdyti produktai

Įjungdami atitinkamą parametrą **numatytuosiuose užsakymų** parametruose, galite sustabdyti išleistų produktų pardavimo procesą. Šis parametras dažniausiai naudojamas, kai baigiasi produkto galiojimas ir jo nereikėtų parduoti jokiame kanale. Asortimentai laikosi šio parametro ir sustabdyti produktai nebus pateikiami nepaisant asortimento konfigūracijos.

### <a name="blocked-products"></a>Užblokuotas produktas

Galite ne tik sustabdyti produkto pardavimą, bet ir laikinai jo pardavimą užblokuoti. Šį parametrą galite konfigūruoti išleisto produkto skirtuke **Prekyba**. Užblokuoti produktai vis tiek pateikiami, tačiau el. kasos aparate gausite pranešimą, nurodantį, kad produkto negalima parduoti.

### <a name="date-effectivity"></a>Datos galiojimas

Asortimentai taikomi pagal datą. Todėl mažmenininkai gali sukonfigūruoti, kada produktai turi arba neturi būti prieinami kiekviename kanale. Apibrėžti ir publikuoti asortimentus galite iš anksto bei galite nurodyti jų pradžios ir pabaigos datas. Produktai automatiškai taps prieinami arba neprieinami nurodytomis datomis.

### <a name="process-assortments-batch-job"></a>Asortimentų apdorojimo paketinė užduotis

Kad sprendime „Commerce“ apibrėžti asortimentai įsigaliotų, juos reikia apdoroti. Šis apdorojimas atliekamas dėl tolesnių priežasčių.

- Asortimentų apibrėžtis reikia nenormalizuoti, kad kanalai galėtų lengviau juos naudoti. Kanalo produktų derinį galima apibrėžti naudojant kelis asortimentus, apimančius įvairius datų intervalus. Kai tam tikra šios informacijos dalis serveryje apskaičiuojama iš anksto, padidėja kanalo našumas.
- Asortimento produktai ir kanalai gali kisti už paties asortimento ribų. Dinaminius asortimentus su nuorodomis į kategorijas ar organizacijos vienetus būtina periodiškai apdoroti, kad į juos įrašai būtų įtraukiami arba neįtraukiami pagal dabartinį priskyrimą.

## <a name="implementation-considerations"></a>Diegimo aplinkybės

Planuodami ir valdydami savo mažmeninės prekybos asortimentus, apsvarstykite tolesnius prekybos vykdymo reikalavimus.

- **Duomenų dubliavimas ir duomenų bazės dydis** – nors asortimentai padeda patenkinti verslo poreikį valdyti produktų prieinamumą, jie taip pat yra svarbus kanalo ir autonominių duomenų bazių dydžio valdymo įrankis. Tinkamai valdomi asortimentai padeda sumažinti duomenų, kuriuos būtina apdoroti ir dubliuoti kanalo bei autonominėse duomenų bazėse, kiekį. Jie taip pat padeda sumažinti būtinų išlaikyti įrašų skaičių. Šiose duomenų bazėse esant mažiau įrašų, padidėja našumas į operaciją įtraukiant prekių, ieškant ir naršant produktus.
- **Pagal datą taikomi / baigiantys galioti asortimentai** – vienas iš efektyviausių įrankių valdyti kanalo ir autonominėse duomenų bazėse esančių produktų skaičių yra asortimentų taikymas pagal datą. Jei paliksite sezoninių produktų ar baigiančių galioti produktų neriboto laiko (nebaigiančius galioti) asortimentus, šios duomenų bazės neribotai augs. Padėti suvaldyti šią situaciją galite įvairiais būdais. Pavyzdžiui, galite turėti atskirus asortimentus sezoniniams produktams ir visada prieinamiems produktams.
- **Į asortimentus neįtrauktų produktų pardavimas ir grąžinimas** – ši galimybė mažmenininkams padeda efektyviai valdyti savo asortimentus – leidžiama prieinamus produktus apriboti iki produktų, kurie priklauso pagrindiniam parduotuvės produktų deriniui. Ši galimybė mažmenininkams taip pat padeda valdyti situacijas, kai produktas buvo klaidingai neįtrauktas į asortimentą arba kai produktas buvo grąžintas pasibaigus asortimento galiojimui.

Jei kanalo duomenų bazėje nėra produktų duomenų, EKA realiuoju laiku kreipiasi į būstinę, kad gautų reikiamą informaciją ir kad produktą būtų galima parduoti, grąžinti ar įtraukti į kliento užsakymą. Taip gauta produktų informacija prieinama tik tos operacijos aprėptyje. Produktas į asortimento apibrėžtį neįtraukiamas. Todėl vėliau realiuoju laiku kreiptis į būstinę reikės pagal poreikį.
