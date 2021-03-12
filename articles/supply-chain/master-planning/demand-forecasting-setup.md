---
title: Poreikio prognozių nustatymas
description: Šioje temoje aprašomos nustatymo užduotys, kurias turite atlikti, norėdami prognozuoti poreikį.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7b0976494a8bb128ae6bb40cbcdf7c691185f23
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970511"
---
# <a name="demand-forecasting-setup"></a>Poreikio prognozių nustatymas

[!include [banner](../includes/banner.md)]

Šioje temoje aprašomos nustatymo užduotys, kurias turite atlikti, norėdami prognozuoti poreikį.  

Nustatymo užduotys apima toliau nurodytų duomenų ir parametrų nustatymą.

## <a name="item-allocation-key"></a>Prekių paskirstymo raktas
Poreikio prognozė skaičiuojama pagal prekę ir jos dimensijas tik tada, jei prekė yra prekių paskirstymo rakto dalis. Ši taisyklė naudojama dideliems prekių kiekiams grupuoti, kad poreikio prognozes būtų galima kurti greičiau. Prekių paskirstymo rakto procentas yra ignoruojamas, kai generuojamos poreikio prognozės. Prognozės kuriamos remiantis tik retrospektyviniais duomenimis. 

Prekė ir jos dimensijos turi būti tik vieno prekių paskirstymo rakto dalis, jei prekių paskirstymo raktas naudojamas kuriant prognozę. 

Norėdami sandėliavimo vienetą (SKU) įtraukti į prekių paskirstymo raktą, pasirinkite **Bendrasis planavimas** &gt; **Sąranka** &gt; **Poreikio prognozės** &gt; **Prekių paskirstymo raktai**. Naudokite puslapį **Priskirti prekes**, norėdami prekę priskirti paskirstymo raktui.

## <a name="intercompany-planning-groups"></a>Vidinės įmonės planavimo grupės
Poreikio prognozės generuoja visų įmonių prognozes. Programoje „Dynamics 365 Supply Chain Management“ kartu suplanuotos įmonės yra sugrupuojamos į vieną vidinės įmonės planavimo grupę. Norėdami nurodyti, kurie kiekvienos įmonės prekių paskirstymo raktai turėtų būtų naudojami prognozuojant poreikį, susiekite vidinės įmonės planavimo grupės narį su prekės paskirstymo raktu pasirinkdami **Bendrasis planavimas** &gt; **Sąranka** &gt; **Vidinės įmonės planavimo grupės**. 

Pagal numatytuosius parametrus, jei prekių paskirstymo raktai nėra priskirti vidinės įmonės planavimo grupės nariams, skaičiuojama visų prekių, priskirtų visiems prekių paskirstymo raktams iš visų įmonių, poreikio prognozė. Puslapyje **Generuoti pagrindinę statistinę prognozę** galima naudoti papildomas įmonių ir prekių paskirstymo raktų filtravimo parinktis. 

Peržiūrėkite prognozuojamų prekių skaičių. Nereikalingos prekės gali padidinti išlaidas, kai naudojate „Microsoft Azure“ mašininį mokymą.

## <a name="demand-forecasting-parameters"></a>Poreikio prognozės parametrai
Norėdami nustatyti poreikio prognozės parametrus, pasirinkite **Bendrasis planavimas** &gt; **Sąranka** &gt; **Poreikio prognozės parametrai**. Kadangi vykdoma visų įmonių poreikio prognozė, sąranka yra visuotinė. Kitaip tariant, sąranka taikoma visoms įmonėms. 

Poreikio prognozės generuoja prognozes, išreikštas kiekiais. Todėl lauke **Poreikio prognozės vienetas** reikia nurodyti matavimo vienetą, kuriuo prognozė turi būti išreikšta. Matavimo vienetas turi būti unikalus, siekiant užtikrinti, kad telkimas ir procentinis paskirstymas būtų logiški. Daugiau informacijos apie telkimą ir paskirstymo procentą žr. [Neautomatinis pagrindinės prognozės koregavimas](manual-adjustments-baseline-forecast.md). Įsitikinkite, kad nustatyta kiekvieno į poreikio prognozę įtraukto SKU naudojamo matavimo vieneto ir bendrojo prognozės matavimo vieneto konvertavimo taisyklė. Vykdant prognozių generavimą užregistruojamas visų prekių, kurių matavimo vienetų negalima konvertuoti, sąrašas, kad būtų galima lengvai koreguoti sąranką. 

Poreikio prognozes galima naudoti norint nustatyti tiek priklausomą, tiek nepriklausomą poreikį. Pavyzdžiui, jei pažymėtas tik žymės langelis **Pardavimo užsakymas** ir jei visos prekės, įtrauktos į poreikio prognozę, yra parduodamos, sistema apskaičiuoja nepriklausomą poreikį. Tačiau į prekių paskirstymo raktus ir poreikio prognozes galima įtraukti kritinių subkomponentų. Tokiu atveju, jei pažymėtas žymės langelis **Gamybos eilutė**, skaičiuojama priklausomo poreikio prognozė. 

Pagrindinę prognozę galima kurti dviem būdais. Galite naudoti retrospektyvinius duomenis ir prognozės modelius arba tiesiog galite retrospektyvinius duomenis nukopijuoti į prognozę. Lauke **Prognozės generavimo strategija** galima pasirinkti vieną iš šių dviejų būdų. Norėdami naudoti prognozės modelius, pasirinkite **„Azure“ mašininis mokymas**. 

Spustelėdami kairiojoje puslapio **Poreikio prognozės parametrai** srityje esančią dalį **Prognozės dimensijos** taip pat galite pasirinkti, kurį prognozės dimensijų rinkinį naudoti generuojant poreikio prognozę. Prognozės dimensija nurodo nustatytą prognozės išsamumo lygį. Įmonė, teritorija ir prekių paskirstymo raktas yra privalomos prognozės dimensijos, bet prognozes taip pat galima generuoti sandėlio, atsargų būsenos, klientų grupės, kliento sąskaitos, šalies / regiono, būsenos ir prekės bei visų prekių dimensijų lygiuose. 

Prognozės dimensijas į naudojamų poreikio prognozės dimensijų sąrašą įtraukti galite bet kuriuo metu. Taip pat galite prognozės dimensijas iš sąrašo pašalinti. Tačiau įtraukus arba pašalinus prognozės dimensiją, neautomatiniai koregavimai bus panaikinti. 

Ne visos prekių elgsena prognozuojant poreikį vienoda. Panašias prekes galima sugrupuoti į vieną prekės paskirstymo raktą, o kiekvienam prekių paskirstymo raktui galima nustatyti konkrečius parametrus, pvz., operacijų tipus ir prognozės metodo parametrus. Kairėje puslapio **Poreikio prognozės parametrai** srityje spustelėkite **Prekių paskirstymo raktai**. 

„Supply Chain Management“ naudoja mašininio mokymo žiniatinklio tarnybą prognozei generuoti. Norėdami prisijungti prie tarnybos, turite pateikti toliau nurodytą informaciją, jei prisijungiate prie „Microsoft Azure“ mašininio mokymo studijos (klasikinės).

-   Žiniatinklio tarnybos taikomojo programavimo sąsajos (API) raktas
-   Žiniatinklio tarnybos galinio punkto URL
-   „Azure“ saugyklos abonemento pavadinimas
-   „Azure“ saugyklos abonemento raktas

> [!NOTE]
> „Azure“ saugyklos abonemento pavadinimas ir raktas yra privalomi tik tada, jei naudojate pasirinktinį saugyklos abonementą. Jei diegiate vietinę versiją, privalote turėti pasirinktinę „Azure“ saugyklos paskyrą, kad mašininio mokymo tarnyba galėtų pasiekti retrospektyvinius duomenis. 

Norėdami kurti poreikio prognozes, galite įdiegti savo tarnybą naudodami mašininio mokymo studiją arba „Supply Chain Management“ poreikio prognozės bandymus. Poreikio prognozės bandymų kaip tinklo tarnybos diegimo instrukcijos pateikiamos „Supply Chain Management“. Puslapyje **Poreikio prognozės parametrai** spustelėkite skirtuką **„Azure“ mašininis mokymas**.

## <a name="settings-for-the-demand-forecasting-machine-learning-service"></a>Poreikio prognozės mašininio mokymo tarnybos parametrai
Norėdami peržiūrėti poreikio prognozės tarnybos parametrus, kuriuos galima konfigūruoti, pasirinkite **Bendrasis planavimas** &gt; **Sąranka** &gt; **Poreikio prognozė** &gt; **Prognozavimo algoritmo parametrai**. Puslapyje **Prognozavimo algoritmo parametrai** rodomos numatytosios parametrų reikšmės. Šiuos parametrus galima perrašyti puslapyje **Poreikio prognozės parametrai**. Naudokite skirtuką **Bendra**, jei parametrus norite perrašyti skirtuke visuotinai, arba naudokite skirtuką **Prekių paskirstymo raktai**, jei norite perrašyti konkrečių prekių paskirstymo raktų parametrus. Perrašyti konkretaus prekių paskirstymo rakto parametrai turi įtakos tik su tuo prekių paskirstymo raktu susietų prekių prognozei.

### <a name="forecast-algorithm-parameters"></a>Prognozės algoritmo parametrai

Skirtuke **Paskirstymo raktai** galite nustatyti **prognozės algoritmo parametrus** kiekvienam prekių paskirstymo raktui. Galimos toliau nurodytos pasirinktys.
- **Patikimumo lygis procentais**. Patikimumo intervalą sudaro reikšmės, kurios nurodo tinkamus poreikio prognozės įvertinimus. 95 procentų patikimumo lygio procentas nurodo 5 procentų tikimybę, kad ateities poreikis nepateks į patikimumo intervalo diapazoną.
- **Priverstinis sezoniškumas**. Nurodo, ar reikia priverstinai naudoti modelį, kad būtų naudojamas tam tikras sezoniškumas. Tai taikoma tik pasirinktims ARIMA ir ETS. Pasirinktys: AUTO (numatytoji), NONE, ADDITIVE, MULTIPLICATIVE.
- **Prognozės modelis**. Pasirinktys: ARIMA, ETS, STL, ETS+ARIMA, ETS+STL, ALL. Norėdami pasirinkti tinkamiausią modelį, naudokite pasirinktį **ALL**.
- **Didžiausia prognozuota vertė**. Nurodo didžiausią vertę, kurią reikia naudoti prognozėje. Formatas: +1E[n] arba skaitinė konstanta.
- **Mažiausia prognozuota vertė**. Nurodo mažiausią vertę, kurią reikia naudoti prognozėje. Formatas: ‑1E[n] arba skaitinė konstanta.
- **Trūkstamos vertės pakaitalai**. Nurodo, kaip užpildomos praeities duomenų spragos. Pasirinktys: skaitinė vertė, MEAN, PREVIOUS, INTERPOLATE LINEAR, INTERPOLATE POLYNOMIAL.
- **Trūkstamos vertės pakaitalų apimtis**. Nurodo, ar vertės keitimas taikomas tik kiekvienam atskiram duomenų diapazono detalumo atributui ar visam duomenų rinkiniui. Pasirinktys: GRANULARITY_ATTRIBUTE (numatytoji), GLOBAL.
- **Užuomina apie sezoniškumą**. Jei naudojate sezoninius duomenis, pateikite prognozės modeliui užuominą, kad pagerintumėte prognozės tikslumą. Formatas: sveikasis skaičius, nurodantis poreikio kartojimosi šabloną. Pavyzdžiui, įvesdami 6 nurodykite duomenis, kurie kartojasi kas 6 mėnesius.
- **Rinkinio dydžio procento tikrinimas**. Praeities duomenų procentas, kurį reikia naudoti kaip testinį rinkinį skaičiuojant prognozės tikslumą. 

<a name="additional-resources"></a>Papildomi ištekliai
--------

[Poreikio prognozavimo apžvalga](introduction-demand-forecasting.md)

[Pagrindinės statistinės prognozės generavimas](generate-statistical-baseline-forecast.md)

[Neautomatiniai pagrindinės prognozės koregavimai](manual-adjustments-baseline-forecast.md)



