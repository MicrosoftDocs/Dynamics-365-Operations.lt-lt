---
title: "Poreikio prognozių nustatymas"
description: "Šioje temoje aprašomos nustatymo užduotys, kurias turite atlikti, norėdami prognozuoti poreikį."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>Poreikio prognozių nustatymas

Šioje temoje aprašomos nustatymo užduotys, kurias turite atlikti, norėdami prognozuoti poreikį.  

Nustatymo užduotys apima toliau nurodytų duomenų ir parametrų nustatymą.

## <a name="item-allocation-key"></a>Prekių paskirstymo raktas
Poreikio prognozė skaičiuojama pagal prekę ir jos dimensijas tik tada, jei prekė yra prekių paskirstymo rakto dalis. Ši taisyklė yra vykdomas grupė daug daiktų, kad paklausos prognozes galima sukurti daug greičiau. Prekės paskirstymo raktas procentas yra nepaisoma, kai paklausos prognozes yra generuojami. Prognozės kuriamos remiantis tik retrospektyviniais duomenimis. 

Prekė ir jos dimensijos turi būti tik vieno prekių paskirstymo rakto dalis, jei prekių paskirstymo raktas naudojamas kuriant prognozę. 

Norėdami pridėti atsargų saugojimo vienetas (SKU) prekių paskirstymo raktą, eikite į **kapitonas planavimo**&gt;**nustatymo**&gt;**paklausos prognozavimo**&gt;**prekių paskirstymo raktus**. Naudokite puslapį **Priskirti prekes**, norėdami prekę priskirti paskirstymo raktui.

## <a name="intercompany-planning-groups"></a>Vidinės įmonės planavimo grupės
Poreikio prognozės generuoja visų įmonių prognozes. Microsoft Dynamics 365 operacijoms, įmonių, kurias planuojama kartu yra sugrupuotos į vieną vidinės įmonės planavimo grupės. Nurodyti įmonės, kurioje prekių paskirstymo raktus reikėtų apsvarstyti paklausos prognozavimo, susieti prekių paskirstymo raktą su vidinės įmonės planavimo grupės narys, eikite į **kapitonas planavimo**&gt;**nustatymo**&gt;**vidinės įmonės planavimo grupės**. 

Pagal numatytuosius nustatymus, jei jokių prekių paskirstymo raktus priskirti vidinės įmonės planavimo grupės nariai, paklausos prognozė apskaičiuojama visus elementus, kurie yra priskirti visi prekių paskirstymo raktus iš "365" Dynamics visus veiklos įmonėms. Puslapyje **Generuoti pagrindinę statistinę prognozę** galima naudoti papildomas įmonių ir prekių paskirstymo raktų filtravimo parinktis. 

Peržiūrėkite prognozuojamų prekių skaičių. Nereikalingos prekės gali padidinti išlaidas, kai naudojate „Microsoft Azure“ mašininį mokymą.

## <a name="demand-forecasting-parameters"></a>Poreikio prognozės parametrai
Norėdami nustatyti paklausos prognozavimo parametrus, eikite į **kapitonas planavimo**&gt;**nustatymo**&gt;**paklausos prognozavimo parametrai**. Kadangi vykdoma visų įmonių poreikio prognozė, sąranka yra visuotinė. Kitaip tariant, sąranka taikoma visoms įmonėms. 

Poreikio prognozės generuoja prognozes, išreikštas kiekiais. Todėl lauke **Poreikio prognozės vienetas** reikia nurodyti matavimo vienetą, kuriuo prognozė turi būti išreikšta. Matavimo vienetas turi būti unikalus, siekiant užtikrinti, kad telkimas ir procentinis paskirstymas būtų logiški. Daugiau informacijos apie telkimą ir paskirstymo procentą žr. [Neautomatinis pagrindinės prognozės koregavimas](manual-adjustments-baseline-forecast.md). Įsitikinkite, kad nustatyta kiekvieno į poreikio prognozę įtraukto SKU naudojamo matavimo vieneto ir bendrojo prognozės matavimo vieneto konvertavimo taisyklė. Vykdant prognozių generavimą užregistruojamas visų prekių, kurių matavimo vienetų negalima konvertuoti, sąrašas, kad būtų galima lengvai koreguoti sąranką. 

Poreikio prognozes galima naudoti norint nustatyti tiek priklausomą, tiek nepriklausomą poreikį. Pavyzdžiui, jei pažymėtas tik žymės langelis **Pardavimo užsakymas** ir jei visos prekės, įtrauktos į poreikio prognozę, yra parduodamos, sistema apskaičiuoja nepriklausomą poreikį. Tačiau į prekių paskirstymo raktus ir poreikio prognozes galima įtraukti kritinių subkomponentų. Tokiu atveju, jei pažymėtas žymės langelis **Gamybos eilutė**, skaičiuojama priklausomo poreikio prognozė. 

Yra du būdai kurti pradinis prognozė Dynamics 365 operacijoms. Galite naudoti retrospektyvinius duomenis ir prognozės modelius arba tiesiog galite retrospektyvinius duomenis nukopijuoti į prognozę. Lauke **Prognozės generavimo strategija** galima pasirinkti vieną iš šių dviejų būdų. Norėdami naudoti prognozės modelius, pasirinkite **„Azure“ mašininis mokymas**. 

Spustelėdami kairiojoje puslapio **Poreikio prognozės parametrai** srityje esančią dalį **Prognozės dimensijos** taip pat galite pasirinkti, kurį prognozės dimensijų rinkinį naudoti generuojant poreikio prognozę. Prognozės dimensija nurodo nustatytą prognozės išsamumo lygį. Įmonė, teritorija ir prekių paskirstymo raktas yra privalomos prognozės dimensijos, bet prognozes taip pat galima generuoti sandėlio, atsargų būsenos, klientų grupės, kliento sąskaitos, šalies / regiono, būsenos ir prekės bei visų prekių dimensijų lygiuose. 

Prognozės dimensijas į naudojamų poreikio prognozės dimensijų sąrašą įtraukti galite bet kuriuo metu. Taip pat galite prognozės dimensijas iš sąrašo pašalinti. Tačiau įtraukus arba pašalinus prognozės dimensiją, neautomatiniai koregavimai bus panaikinti. 

Ne visos prekių elgsena prognozuojant poreikį vienoda. Panašias prekes galima sugrupuoti į vieną prekės paskirstymo raktą, o kiekvienam prekių paskirstymo raktui galima nustatyti konkrečius parametrus, pvz., operacijų tipus ir prognozės metodo parametrus. Kairėje puslapio **Poreikio prognozės parametrai** srityje spustelėkite **Prekių paskirstymo raktai**. 

Norėdami sukurti prognozę, Dynamics 365 operacijų naudoja Machine Learning interneto paslauga. Norėdami prisijungti prie paslaugos serverio, jums turi Dynamics 365 operacijoms tokią informaciją jei jums prisijungti prie Microsoft Azure mašinos mokymosi studija:

-   Žiniatinklio tarnybos taikomojo programavimo sąsajos (API) raktas
-   Žiniatinklio tarnybos galinio punkto URL
-   „Azure“ saugyklos abonemento pavadinimas
-   „Azure“ saugyklos abonemento raktas

**Pastaba:** „Azure“ saugyklos abonemento pavadinimas ir raktas yra privalomi tik jei naudojate pasirinktinį saugyklos abonementą. Jei diegdami vietinę versiją, turite pasirinktinės saugyklos į Azure, kad mašinos mokymosi paslauga galėtų naudotis istoriniai duomenys. 

Sukurti paklausos prognozių, jūs galite panaudoti savo paslaugas naudojant mašinos mokymosi Studio ir Dynamics 365 operacijų paklausos prognozavimo eksperimentus. Informacijos apie Dynamics 365 operacijų paklausos prognozavimo eksperimentų kaip web paslauga yra prieinama Dynamics 365 operacijoms. Puslapyje **Poreikio prognozės parametrai** spustelėkite skirtuką **„Azure“ mašininis mokymas**.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Parametrų dinamika 365 operacijų paklausos prognozavimo mašina mokymosi paslaugas
Norėdami peržiūrėti parametrų, kurie gali būti konfigūruojamas Dynamics "365" dėl operacijų paklausos prognozavimo tarnybos, eikite į **bendrojo planavimo**&gt;**parametrai**&gt;**paklausos prognozavimo**&gt;**prognozavimo algoritmą parametrų**. Į **prognozavimo algoritmą parametrų** puslapyje rodomas pagal nutylėjimą parametrams. Šiuos parametrus galite perrašyti į **paklausos prognozavimo parametrai** puslapis. Naudokite skirtuką **Bendra**, jei parametrus norite perrašyti skirtuke visuotinai, arba naudokite skirtuką **Prekių paskirstymo raktai**, jei norite perrašyti konkrečių prekių paskirstymo raktų parametrus. Perrašyti konkretaus prekių paskirstymo rakto parametrai turi įtakos tik su tuo prekių paskirstymo raktu susietų prekių prognozei.

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)


