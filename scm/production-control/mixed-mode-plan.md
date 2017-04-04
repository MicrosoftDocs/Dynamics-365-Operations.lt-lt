---
title: "Mišrus režimas planavimas - sujungti atskirų, procesų ir liesos"
description: "Šiame straipsnyje pateikiama informacija apie mišriojo režimo planavimą. Mišriojo režimo planavime galite modeliuoti savo tiekimo grandinę remdamiesi medžiagų srautu. Microsoft Dynamics 365 operacijų būdu užtikrinama, kad medžiagų srautą taip savo modelius, nepriklausomai nuo to, tiekimo politiką, kuri būtų pasirinktas (kanbans, gamybos užsakymus, pirkimo užsakymus, partijos užsakymuose arba perd.)."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d635421112f6d1e79a47090de3ffc4178b36b132
ms.lasthandoff: 03/31/2017


---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Mišrus režimas planavimas - sujungti atskirų, procesų ir liesos

Šiame straipsnyje pateikiama informacija apie mišriojo režimo planavimą. Mišriojo režimo planavime galite modeliuoti savo tiekimo grandinę remdamiesi medžiagų srautu. Microsoft Dynamics 365 operacijų būdu užtikrinama, kad medžiagų srautą taip savo modelius, nepriklausomai nuo to, tiekimo politiką, kuri būtų pasirinktas (kanbans, gamybos užsakymus, pirkimo užsakymus, partijos užsakymuose arba perd.). 

Neatsižvelgdami į produkto struktūrą galite pasirinkti bendrąją produkto tiekimo strategiją.  

Pavyzdžiui, galite valdyti „kanban“ surinkimo srityje, į kurią medžiagos tiekiamos naudojant gamybos užsakymus, „kanban“, perkėlimus, paketinius užsakymus arba bet kurias kitas tiekimo grandinės savybėms tinkamas priemones, tačiau ir toliau galite peržiūrėti visas tiekiamas medžiagas. Dėl šios galimybės optimizuojami tiekimo grandinės procesai ir pagerinamas tiekimo grandinės procesų matomumas.  

Bendrajame planavime naudojamų tiekimo strategijų išsamumą lemia saugojimo dimensijos, kurios įjungiamos kaip padengimo dimensijos. Jei norėsite įjungti bendrąjį planavimą, kad valdytumėte papildymo ir tiekimo į įvairių tipų vietas procesus (pavyzdžiui, suskirstydami gamybos vietą įvairiems gamybos vienetams arba suskirstydami įvairių tipų medžiagų ir pagamintų prekių sandėlius), kaip padengimo dimensijas rekomenduojame įjungti dimensijas Vieta ir Sandėlis. Be to, kaip padengimo dimensijos galima neįtraukti dimensijos Sandėlis. Tokiu atveju naudojant patobulinto sandėlio valdymo funkcijas, visi sandėlyje atliekami perkėlimai valdomi vykdant sandėlio darbo procesą, o visus tarp sandėlių atliekamus perkėlimus galima valdyti naudojant išėmimo „kanban“.

## <a name="supply-policies"></a>Tiekimo strategijos
Dinamika 365 operacijų mišraus režimo planavimo kontroliuoja, kaip produktas yra pateikiami ir, remiantis tiekimo, kaip išvestiniai poreikiai (vartojimo prekių iš bill medžiagų \[KS\]) yra išleidžiamos. Pagal užsakymo tipą sistemoje automatiškai surandamos poreikius atitinkančios medžiagos.  

Tiekimo strategijas galima apibrėžti produkto lygiu arba poreikius atitinkančiu išsamumo lygiu. Tiekimo strategijų išsamumas nustatomas puslapyje **Numatytieji užsakymo parametrai**.  

Tiekimo strategijas galima valdyti pagal produktą, prekės dimensijas (konfigūraciją, spalvą ir dydį), vietą ir sandėlį. Šis sąrankos procesas atliekamas puslapyje **Prekės padengimas**.  

Taikant numatytąjį užsakymo tipą valdoma, koks bus sukuriamas užsakymo bendrasis planavimas.  

Nepriklausomai nuo to, kaip tiekimo grandinėje yra modeliuojama, Dynamics 365 operacijoms palaiko savo tiekimo politikos derinys. Galite taikyti gamybos užsakymus, kurie gaunami naudojant „kanban“. Be to, galite naudoti paketinį užsakymą, kuriame turi būti įtrauktas perkeliant arba naudojant „kanban“ tiekiamas produktas.  

Dinamika 365 operacijoms užtikrina, kad medžiagų srautą taip modelis.  

Kai jau apibrėžta tiekimo strategija, medžiagos paėmimo sandėlis apdorojimo laiku priskiriamas dinamiškai.  

„kanban“ naudojami trumpai, todėl jie paprastai nekuriami naudoti būsimame laikotarpyje. Kad būtų visiškai stebimi tiekimo grandinės procesai, pradėta taikyti nauja planavimo koncepcija „suplanuotas „kanban“, kuri naudojama iškeltiems poreikiams apskaičiuoti bei kurią naudojant užtikrinama, kad informacija apie poreikius būtų gaunama remiantis tais pačiais loginiais veiksmais, kurie naudojami kuriant faktinį „kanban“.  

Tie patys loginiai veiksmai atliekami taikant visų kitų tipų tiekimo strategijas. Taigi ilgalaikio medžiagų planavimo procesas vykdomas atliekant tuos pačius loginius veiksmus, kuriuos po gamybos ir tiekimo procesų patvirtinimo tikitės atlikti apdorodami faktinius užsakymus.

## <a name="materials-allocation-crosssupply-policy--resource-consumption-on-boms"></a>Medžiagų paskirstymas crosssupply politika – išteklių sunaudojimas KS
Išteklių vartojimas yra svarbi funkcija. Naudojant išteklių suvartojimo funkciją medžiagų paėmimo sandėlis bus pasirenkamas dinamiškai remiantis tiekimo strategija (užsakymo tipu), be to, bus paprasčiau tvarkomi pagrindiniai duomenys.  

Naudojant išteklių suvartojimo funkciją sandėlis, iš kurio paimamos medžiagos, turi būti priskirtas pagal produkto tiekimo būdą. Kitaip tariant, apdorojimo laiku sistemoje surandami ištekliai, kurie turėtų būti naudojami gamybos procese. Tada pagal šiuos išteklius sistemoje surandamas paėmimo sandėlis.  

Jei užduotis nepriklausoma nuo tiekimo strategijos, o tiekimo procesas bus pakeistas, nereikia pakeisti KS informacijos. Ad hoc pakeitimų, Dynamics 365 operacijoms todėl įsitikinkite, kad medžiagų yra gaunami iš dešinės sandėlio.

## <a name="process-manufacturing--the-production-type"></a>Apdirbamoji gamyba – gamybos tipas
Suteikia visišką lankstumą mišrių režimu, mes rekomenduojame naudoti gamybos KS tipo visiems produktams. Tada galite naudoti gamybos užsakymų, kanbans, perd. arba pirkimo užsakymų tiekti produktą. Vykdydami apdirbamosios gamybos procesą turite naudoti gamybos tipą **Formulė**, **Sudėtinis produktas**, **Šalutinis produktas** arba **Planavimo prekė**. Su šiais gamybos tipais negalima naudoti „kanban“ ir gamybos užsakymų.


