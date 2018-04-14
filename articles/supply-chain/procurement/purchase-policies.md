---
title: Pirkimo strategijos
description: "Šiame straipsnyje pateikta informacija apie pirkimo strategijas. Pirkimo strategija yra taisyklių rinkinys, valdantis paraiškos procesą. Pirkimo strategijos padeda įsigijimo administratoriams įgyvendinti įsigijimo strategiją sukuriant strategijos struktūrą, suderintą su organizacijos strateginio pirkimo reikalavimais."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqSourcingPolicyRule, SysPolicy, SysPolicyListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 11614
ms.assetid: 729a304d-0f3f-4ccb-bd5b-46ee0976c57f
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 675a7a8b0da228e789ee37ca8fe1d0c0ea01c283
ms.contentlocale: lt-lt
ms.lasthandoff: 11/03/2017

---

# <a name="purchasing-policies"></a>Pirkimo strategijos

[!INCLUDE [banner](../includes/banner.md)]

Šiame straipsnyje pateikta informacija apie pirkimo strategijas. Pirkimo strategija yra taisyklių rinkinys, valdantis paraiškos procesą. Pirkimo strategijos padeda įsigijimo administratoriams įgyvendinti įsigijimo strategiją sukuriant strategijos struktūrą, suderintą su organizacijos strateginio pirkimo reikalavimais.

Pirkimo strategiją sudaro strategijos taisyklių rinkinys. Kai nustatote strategijos taisyklę, pirmiausia pasirenkate taisyklės tipą. Tada sukuriate pasirinkto taisyklės tipo taisyklę, nustatydami jos parametrus, pradžios datą ir pabaigos datą.  

Pavyzdžiui, administratorius sukuria strategiją, pasirenka taisyklės tipą **Katalogo strategija** ir į strategiją įtraukia strategijos taisyklę. Ši katalogo strategijos taisyklė nurodo, kad katalogą „Adventure“ reikia naudoti vykdant vidaus įsigijimą. Susiejus prikimo strategiją su konkrečia organizacija, tos organizacijos darbuotojai kurdami paraiškas matys katalogą „Adventure“.

## <a name="assigning-policies-to-organizations"></a>Strategijų priskyrimas organizacijoms
Strategija įsigalios tik susiejus ją su organizacija. Pirkimo strategijos yra susietos su hierarchijos paskirtimi **Įsigijimo vidinė kontrolė**. Todėl pirkimo strategijos taikomos organizacijoms tik tose hierarchijose, kurių hierarchijos paskirtis yra **Įsigijimo vidinė kontrolė**. Taip pat organizacijas galite pasirinkti iš lentelės „CompanyInfo“ standartinio juridinių subjektų sąrašo. Šie juridiniai subjektai strategijos sistemoje vadinami „Įmonėmis“.

## <a name="determining-which-rule-to-apply"></a>Nustatymas, kurią taisyklę taikyti
Atsižvelgiant į tai, kaip konfigūruojate savo pirkimo strategijas, vartotojus organizacijoje gali veikti kelios taisyklės. Toliau pateikti pavyzdžiai nurodo skirtingus būdus, kuriais galite konfigūruoti pirkimo strategijas ir nurodyti, kaip strategijos yra taikomos, kai vykdoma operacija.

### <a name="example-1-simple-purchasing-policy-configuration"></a>1 pavyzdys: paprastas pirkimo strategijos konfigūravimas

Mažos ir nesudėtingos organizacijos pirkimo strategijas gali nustatyti pagal juridinį subjektą ir naudoti tik organizacijos hierarchijos tipą Įmonės.  

„Fabrikam“ (smulkiojo verslo) pirkimo reikalavimai visoje organizacijoje skiriasi mažai. Pirkimo taisyklės skiriasi tik tarp organizacijos juridinių subjektų. Pvz., „Fabrikam Canada“ ir „Fabrikam U.S.“ darbuotojai prekes ir paslaugas perka iš skirtingų katalogų ir tiekėjų. Todėl „Fabrikam“ pirkimo strategijos nustatomos juridinio subjekto lygyje.  

„Fabrikam“ sukuria dvi pirkimo strategijas. A strategija taikoma jos JAV juridiniam subjektui, 1111. B strategija taikoma jos Kanados juridiniam subjektui, 2222. Kai 1111 juridinio subjekto darbuotojas kuria pirkimo paraišką, strategijos taisyklės išvedamos iš A strategijos. Pvz., darbuotojo matomas produktų katalogas yra nurodytas A strategijos katalogo strategijos taisyklėje.  

Kai 2222 juridinio subjekto darbuotojas kuria pirkimo paraišką, strategijos taisyklės išvedamos iš B strategijos.  

**Pastaba:** jei 1111 juridinio subjekto darbuotojas prekę perka 2222 juridinio subjekto darbuotojo vardu, taikomos 2222 juridinio subjekto nustatytos strategijos taisyklės (t. y. B strategijos taisyklės).

### <a name="example-2-complex-purchasing-policy-configuration"></a>2 pavyzdys: sudėtingas pirkimo strategijos konfigūravimas

Ankstesniame pavyzdyje visos pirkimo taisyklės buvo nurodytos vienoje organizacijos hierarchijoje – Įmonės. Tačiau sudėtinga organizacija gali nustatyti kelių organizacijos hierarchijų strategijas.  


„Contoso“ yra didelė įmonė, kuriai reikalingos sudėtingos pirkimo taisyklės paraiškų procesui valdyti. „Contoso“ nustatė šių dviejų skirtingų organizacijos hierarchijų taisykles: Padalinys ir Visuotinis pirkimo valdymas.  

123 strategija nustatyta pardavimo JK (pardavimo padalinio) organizacijos hierarchijai Padalinys. 123 strategijoje pirkimo paraiškos kontrolės taisyklė nurodo, kad minimaliems užsakymo kiekiams turi būti taikomi apribojimai. Šioje taisyklėje pasirenkama parinktis **Taikyti minimalaus užsakymo kiekio apribojimus**.  

456 strategija nustatyta pardavimo ir rinkodaros padalinio organizacijos hierarchijai Visuotinis pirkimo valdymas. 456 strategijoje pirkimo paraiškos kontrolės taisyklė nenurodo, kad minimaliems užsakymo kiekiams turi būti taikomi apribojimai. Šioje taisyklėje pasirenkama parinktis **Taikyti minimalaus užsakymo kiekio apribojimus**.  

Semas dirba „Contoso“ JK biuro pardavimo JK padalinyje. Šiam padaliniui taikomos abi organizacijos hierarchijos: Padalinys ir Visuotinis pirkimo valdymas. Kai Semas kuria pirkimo paraišką, sistema turi nustatyti, kokią strategiją taikyti. Sistemos administratorius nustato pirkimo strategijos parametrus, pagal kuriuos pirkimo strategijos turi būti taikomos toliau nurodyta pirmumo tvarka.

1.  Visuotinis pirkimo valdymas
2.  Padalinys
3.  Įmonės

Todėl Semo kuriamai pirkimo paraiškai taikoma 456 strategija ir netaikomi jokie pirkimo paraiškos minimalaus užsakymo kiekio apribojimai.

## <a name="policy-rules"></a>Strategijos taisyklės
### <a name="catalog-policy-rule"></a>Katalogo strategijos taisyklė

Katalogo strategijos taisyklė nurodo, kurį įsigijimo katalogą vartotojai matys kurdami pirkimo paraiškas. Jei vartotojui buvo suteikta teisė kito vartotojo vardu užsakyti produktų, paraiškoje naudojama katalogo strategijos taisyklė, nustatyta prašytojo juridinio subjekto ir valdymo vieneto, kad nustatytų, kurį katalogą rodyti. Prieš nustatydami katalogo strategijos taisyklę, turite sukurti ir publikuoti įsigijimo katalogą.

### <a name="category-access-policy-rule"></a>Kategorijos prieigos strategijos taisyklė

Kategorijos prieigos strategijos taisyklė nurodo, prie kurių kategorijų vartotojai turės prieigą kurdami pirkimo paraiškas. Jei nenurodyta jokia taisyklė, į pirkimo paraišką galima įtraukti visas įsigijimo kategorijas.

1.  Pasirinkite parinktį **Įtraukti pirminę taisyklę**, norėdami kategorijai taikyti pirminės organizacijos kategorijos prieigos strategijos taisyklę.
2.  Srityje **Galimos kategorijos** pasirinkite kategorijas, kurioms taikoma taisyklė. Kai pasirenkate kategoriją, visos hierarchijoje aukščiau esančios kategorijos taip pat įtraukiamos į sąrašą **Pasirinktos kategorijos**.
3.  Pasirinkite parinktį **Įtraukti subkategorijas**, norėdami taisyklę taikyti visoms pasirinktos kategorijos subkategorijoms.

### <a name="category-policy-rule"></a>Kategorijos strategijos taisyklė

Kategorijos strategijos taisyklė nurodo, kaip vartotojai gali pasirinkti kiekvienos kategorijos tiekėjus. Ji taip pat nustato gavimo ir SF išrašymo procesų reikalavimus.

### <a name="re-approval-rule-for-purchase-orders"></a>Pirkimo užsakymų pakartotinio patvirtinimo taisyklė

Pakartotinio patvirtinimo taisyklė yra pasirinktinė taisyklė, nurodanti būtinus pakeisto pirkimo užsakymo pakartotinio patvirtinimo kriterijus. Pasirinkti laukai yra vertinami pirkimo užsakymo darbo eigoje, kai darbo eigoje yra nustatyta sąlyga „Reikia iš naujo patvirtinti pirkimo užsakymą“.

> [!NOTE]
> Apskaitos paskirstymas visada bus nustatomas iš naujo, kai pakeičiamas patvirtintas pirkimo užsakymas, kurio keitimų valdymo funkcija įjungta. Todėl, jei nenorite, kad pakeitus tam tikrus laukus pirkimo užsakymas būtų patvirtinamas iš naujo, laukas Apskaitos paskirstymas.pakeistas NETURĖTŲ būti įtrauktas kaip pasirinktas laukas iš naujo patvirtinti. 

### <a name="purchase-requisition-rfq-rule"></a>Pirkimo paraiškos RFQ taisyklė

Pirkimo paraiškos taisyklės nurodo kriterijus, pagal kuriuos reikalaujama pirkimo paraiškos eilutės pasiūlymo patvirtinimo (RFQ). Jei eilutė tenkina sąlygas, paraiškos eilutėje rodomas antspaudas „neoficialus RFQ“ arba „oficialus RFQ“.

### <a name="purchase-requisition-control-rule"></a>Pirkimo paraiškos kontrolės taisyklė

Pirkimo paraiškos kontrolės taisyklė yra pasirinktinė taisyklė. Kuriant šio tipo taisykles, parinktis galima nustatyti įvairiuose toliau nurodytuose skirtukuose.

-   Skirtuke **Darbo eigos pateikimas** galite konfigūruoti laukus, kurie turi būti įvesti paraiškos eilutėje, kad paraiška būtų pateikta patvirtinti, kai paraiškos paskirtis yra **Suvartojimas**.
-   Skirtuke **Užsakymo kiekiai** galite konfigūruoti laukus, kurie pirkimo paraiškoje reikalingi esant tam tikroms sąlygoms. Taip pat galite nustatyti užsakymo kiekius.
-   Skirtuke **Datos** galite konfigūruoti, ar apskaitos data turi būti ta pati, kaip pareikalauta data
-   Skirtuke **Adresas** galite nurodyti, ar vartotojas sistemoje gali kurti naujų adresų ir taikyti juos pirkimo paraiškai.

### <a name="requisition-purpose-rule"></a>Paraiškos paskirties taisyklė

Paraiškos paskirties taisyklė yra pasirinktinė taisyklė, nurodanti konkretaus juridinio subjekto leistiną paraiškos paskirties tipą. Jei šioje taisyklėje nenurodyta kita paskirtis, kuriant paraiškas automatiškai nustatomas paraiškų tipas **Suvartojimas**.

### <a name="replenishment-category-access-policy-rule"></a>Papildymo kategorijos prieigos strategijos taisyklė

Papildymo kategorijos prieigos strategijos taisyklė yra pasirinktinė taisyklė, nurodanti produktus, kuriuos naudojant galima tenkinti konkretaus juridinio subjekto paraiškos poreikį, kai paraiškos paskirtis yra **Papildymas**.

### <a name="replenishment-control-rule"></a>Papildymo valdymo taisyklė

Papildymo valdymo taisyklė yra pasirinktinė taisyklė, nurodanti laukus, kuriuos reikia įvesti paraiškos eilutėje, kad paraiška būtų pateikta patvirtinti, kai paraiškos paskirtis yra **Papildymas**.

### <a name="purchase-order-creation-and-demand-consolidation-rule"></a>Pirkimo užsakymo kūrimas ir poreikio konsolidacijos taisyklė

Pirkimo užsakymo kūrimo ir poreikio konsolidavimo taisyklė nurodo, kurias strategijos taisykles reikia naudoti, kai pirkimo užsakymas yra generuojamas iš patvirtintos pirkimo paraiškos. Kuriant šio tipo taisykles, parinktis galima nustatyti įvairiuose toliau nurodytuose skirtukuose.

-   Skirtuke **Pirkimo užsakymo skaidymas** galite nurodyti pirkimo paraiškos eilučių skaidymo į atskirus pirkimo užsakymus kriterijus.
-   Skirtuke **Kainų / nuolaidų perkėlimas** galite nurodyti, kada reikia perskaičiuoti kainos sutartį, kai kuriamas pirkimo užsakymas.
    -   **Tik jei prekybos sutarties nėra** – kainos ir nuolaidos perkeliamos iš pirkimo paraiškos tik jei nėra taikomos prekybos sutarties arba bazinės kainos. Jei yra prekės arba tiekėjo prekybos sutartis arba bazinė kaina, kainos ir nuolaidos yra perskaičiuojamos pagal prekybos sutartį arba bazinę kainą ir taikomos pirkimo užsakymui. Jei nenurodyta kitaip, tai yra numatytasis veikimo būdas.
    -   **Visada** – kainos ir nuolaidos visada perkeliamos iš pirkimo paraiškos.

    Taip pat galite leisti prašytojui keisti atskirų pirkimo paraiškos eilučių kainų ir nuolaidų perkėlimo metodą, nepaisant kainų/nuolaidų perkėlimo taisyklės, kuri yra nurodyta. Pasirinkite parinktį **Leisti rankiniu būdu perrašyti pirkimo paraiškos eilutę**, jei norite įgalinti šią galimybę.
-   Skirtuke **Prekės aprašo perkėlimas** galite prekės aprašą perkelti iš paraiškos, jei ji yra kilusi iš RFQ.
-   Skirtuke **Leistinas kainos nuokrypis** galite nustatyti taisykles, kurios naudojamos siekiant patvirtintas pirkimo paraiškas nukreipti atgal į peržiūros procesą, kai padidėja įsigijimo katalogo prekės kaina. Nustatykite didžiausią sumą, kuria pirkimo paraiškos eilutės prekės grynoji suma gali būti padidinta nuo pirkimo paraiškos patvirtinimo ir pirkimo užsakymo sukūrimo laiko. Grynoji suma apskaičiuojama pagal šią formulę: (\[Kiekis × (Vieneto kaina – Nuolaida) ÷ Kainos vienetas\] + Papildomos pirkimo išlaidos) × (100 – nuolaidos procentas) ÷ 100. Jūsų nustatytą kainos nuokrypį viršijančios pirkimo paraiškos eilutės apdorojamos neautomatiškai. Taisyklės, kurias galite konfigūruoti skirtuke **Klaidų apdorojimas**, nustato, kaip apdorojamos pirkimo paraiškos eilutės.
-   Skirtuke **Klaidų apdorojimas** galite konfigūruoti apdorojimo taisyklę, taikomą pirkimo paraiškai, jei jos patvirtinimas pirkimo užsakymo kūrimo metu nepavyksta dėl tiekėjo klaidos arba kainos nuokrypio klaidos. Pasirinkite vieną iš toliau pateiktų pasirinkčių:
    -   **Veiksmų nėra** – pirkimo paraiškos eilutės lieka puslapyje **Išleisti patvirtintas pirkimo paraiškas**. Pirkimo paraiškos eilučių būsena lieka **Patvirtinta**. Tačiau klaidos turi būti išspręstos, kad pirkimo užsakymas galėtų būti generuojamas pirkimo paraiškos eilutėms.
    -   **Atšaukti pirkimo paraiškos eilutę** – atšaukiamos pirkimo paraiškos eilutės. Prašytojas gali sukurti naują pirkimo paraišką atšauktoms eilutėms, jei jis ar ji vis dar nori prašyti eilutės elementų.
    -   **Kurti naują pirkimo paraiškos eilutę** – kuriamos pirkimo paraiškos eilutės. Generuojamos naujos pirkimo paraiškos, kuriose yra tik pirkimo paraiškos eilutės, kurių tikrinimas nepavyko. Naujai sugeneruotų pirkimo paraiškų būsena yra **Juodraštis**. Šias pirkimo paraiškas galima pateikti pakartotinai peržiūrėti po to, kai tikrinimo klaidos buvo išspręstos. Pirkimo paraiškos eilučių rengėjui yra pranešama, kad eilutės buvo atšauktos, ir kad naujos pirkimo paraiškos buvo sugeneruotos pirkimo paraiškos eilutėms, kurių tikrinimas nepavyko.
-   Skirtuke **Neautomatinis pirkimo užsakymo kūrimas** galite nurodyti parametrus, kurie nustato, ar pirkimo paraiška turi būti apdorojama neautomatiniu būdu, ar ji gali būti automatiškai konvertuojama į pirkimo užsakymą. Parametrus galite taikyti vidaus katalogo prekėms, išorės katalogo prekėms arba ne katalogo prekėms. Pasirinkite vieną iš toliau pateiktų pasirinkčių:
    -   **Kurti pirkimo užsakymus neautomatiškai** – visų pirkimo paraiškų pirkimo užsakymus kurkite neautomatiškai.
    -   **Kurti pirkimo užsakymus automatiškai** – visų patvirtintų pirkimo paraiškų pirkimo užsakymus kurkite automatiškai. Jokios pirkimo paraiškos nelaikomos pirkimo užsakymo kūrimui rankiniu būdu.
    -   **Automatiškai kurti pirkimo užsakymus, išskyrus šių sąlygų susidarymo atvejais** – neautomatiškai kurkite pirkimo paraiškų, atitinkančių jūsų nustatytus kriterijus, pirkimo užsakymus. Visos kitos pirkimo paraiškos, kurios yra patvirtintos, bus automatiškai konvertuojamos į pirkimo užsakymus. Jei pasirinksite **Automatiškai kurti pirkimo užsakymus, išskyrus šių sąlygų susidarymo atvejais**, galite pridėti įsigijimo kategorijas ir tiekėjus norėdami nurodyti, kurios patvirtintos pirkimo paraiškos eilutės yra skirtos apdoroti neautomatiniu būdu. Šią parinktį galite taikyti vidaus katalogo prekėms, išorės katalogo prekėms ir ne katalogo prekėms. Kai pasirenkate įsigijimo kategoriją, bet kokios tos įsigijimo kategorijos subkategorijos taip pat pasirenkamos. Pasirinkite parinktį **Visos** tam tikro tipo pirkimo paraiškos eilutei, jei norite, kad visos to eilutės tipo eilutės būtų apdorojamos neautomatiniu būdu.

    Jei norite, kad pirkimo užsakymai būtų automatiškai generuojami iš patvirtintų pirkimo užklausų paleidus pirkimo užsakymo generavimo paketinę užduotį, pasirinkite parinktį **Vykdyti automatinį pirkimo užsakymo kūrimą kaip paketinę užduotį**. Ši parinktis taikoma tik pirkimo paraiškoms, kurių nereikia apdoroti neautomatiniu būdu. Vykdydami automatinį pirkimo užsakymo generavimą kaip paketinę užduotį, galite planuoti šią veiklą tuo metu, kai ištekliai yra mažiau riboti. Jei pirkimo paraiškos eilutėse pasirinkta parinktis **Būtinas išankstinis apmokėjimas**, pasirinkite parinktį **Kada paraiška nustatoma išankstiniam mokėjimui atlikti**, jei norite, kad patvirtintos pirkimo paraiškos būtų apdorojamos neautomatiniu būdu. Pirkimo paraiškos, kurios skirtos apdoroti neautomatiniu būdu, gali būti filtruojamos, kad jūs galėtumėte peržiūrėti tik tas pirkimo paraiškos eilutes, kurios reikalauja išankstinio apmokėjimo.
-   Skirtuke **Poreikio konsolidavimas** galite nurodyti parametrus, kurie nustato, ar neautomatiniu būdu apdorojamos pirkimo paraiškos gali būti naudojamos pirkimo paraiškai konsoliduoti. Parametrus galite taikyti vidaus katalogo prekėms, išorės katalogo prekėms arba ne katalogo prekėms. Pasirinkite vieną iš toliau pateiktų pasirinkčių:
    -   **Neleisti poreikio konsolidacijos** – negalima konsoliduoti jokių patvirtintų pirkimo paraiškos eilučių poreikio. Ši parinktis yra įjungta pagal numatytuosius parametrus ir taikoma tik pirkimo paraiškos eilutėms, kurioms reikalingas pirkimo užsakymo kūrimo neautomatinis apdorojimas.
    -   **Visada leisti poreikio konsolidaciją** – galima konsoliduoti visų patvirtintų pirkimo paraiškos eilučių poreikį. **Pastaba:** jei skirtuke **Poreikio konsolidavimas** pasirinksite parinktį **Visada leisti poreikio konsolidaciją**, o skirtuke **Neautomatinis pirkimo užsakymo kūrimas** pasirinksite parinktį **Automatiškai kurti pirkimo užsakymus**, visos pirkimo paraiškos bus apdorojamos neautomatiniu būdu.
    -   **Leisti poreikio konsolidaciją esant šioms sąlygoms** – nurodykite kriterijus, pagal kuriuos nustatoma, ar galima konsoliduoti patvirtintų pirkimo paraiškos eilučių poreikį. Kiekvienos rūšies pirkimo paraiškos eilutei galite nustatyti kriterijus pagal įsigijimo kategoriją ir tiekėją. Jei pasirenkate **Leisti poreikio konsolidaciją esant šioms sąlygoms**, galite nustatyti kriterijus pagal įsigijimo kategoriją ir tiekėją kiekvienos rūšies pirkimo paraiškos eilutei. Kai pasirenkate įsigijimo kategoriją, bet kokios tos įsigijimo kategorijos subkategorijos taip pat pasirenkamos. Jei pasirenkate parinktį **Visos** konkrečiam eilutės tipui, galima konsoliduoti visų to eilutės tipo pirkimo paraiškos eilučių poreikį.





