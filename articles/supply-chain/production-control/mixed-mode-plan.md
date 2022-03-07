---
title: 'Įvairių režimų planavimas: prekių surinkimo, apdirbamosios gamybos ir „lean“ tiekimo suderinimas'
description: Šioje temoje pateikiama informacija apie mišriojo režimo planavimą.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a199d5ac7633aba894ffbc17db015100ae93d895
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566772"
---
# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a>Įvairių režimų planavimas: prekių surinkimo, apdirbamosios gamybos ir „lean“ tiekimo suderinimas

[!include [banner](../includes/banner.md)]

Šioje temoje pateikiama informacija apie mišriojo režimo planavimą. Mišriojo režimo planavime galite modeliuoti savo tiekimo grandinę remdamiesi medžiagų srautu. „Dynamics 365 Supply Chain Management“ užtikrina, kad medžiagų srautas atitiktų jūsų modelius, nepriklausomai nuo pasirinktos tiekimo strategijos („kanban“, gamybos užsakymai, paketiniai užsakymai arba perkėlimo užsakymai). 

Neatsižvelgdami į produkto struktūrą galite pasirinkti bendrąją produkto tiekimo strategiją.  

Pavyzdžiui, galite valdyti „kanban“ surinkimo srityje, į kurią medžiagos tiekiamos naudojant gamybos užsakymus, „kanban“, perkėlimus, paketinius užsakymus arba bet kurias kitas tiekimo grandinės savybėms tinkamas priemones, tačiau ir toliau galite peržiūrėti visas tiekiamas medžiagas. Dėl šios galimybės optimizuojami tiekimo grandinės procesai ir pagerinamas tiekimo grandinės procesų matomumas.  

Bendrajame planavime naudojamų tiekimo strategijų išsamumą lemia saugojimo dimensijos, kurios įjungiamos kaip padengimo dimensijos. Jei norėsite įjungti bendrąjį planavimą, kad valdytumėte papildymo ir tiekimo į įvairių tipų vietas procesus (pavyzdžiui, suskirstydami gamybos vietą įvairiems gamybos vienetams arba suskirstydami įvairių tipų medžiagų ir pagamintų prekių sandėlius), kaip padengimo dimensijas rekomenduojame įjungti dimensijas Vieta ir Sandėlis. Be to, kaip padengimo dimensijos galima neįtraukti dimensijos Sandėlis. Tokiu atveju naudojant patobulinto sandėlio valdymo funkcijas, visi sandėlyje atliekami perkėlimai valdomi vykdant sandėlio darbo procesą, o visus tarp sandėlių atliekamus perkėlimus galima valdyti naudojant išėmimo „kanban“.

## <a name="supply-policies"></a>Tiekimo strategijos
Taikant įvairių režimų planavimo funkciją valdomas produkto tiekimo procesas, ir kaip, remiantis tiekimu, išleidžiami išvestiniai poreikiai (komplektavimo specifikacijos \[KS\] prekių suvartojimas). Pagal užsakymo tipą sistemoje automatiškai surandamos poreikius atitinkančios medžiagos.  

Tiekimo strategijas galima apibrėžti produkto lygiu arba poreikius atitinkančiu išsamumo lygiu. Tiekimo strategijų išsamumas nustatomas puslapyje **Numatytieji užsakymo parametrai**.  

Tiekimo strategijas galima valdyti pagal produktą, prekės dimensijas (konfigūraciją, spalvą ir dydį), vietą ir sandėlį. Šis sąrankos procesas atliekamas puslapyje **Prekės padengimas**.  

Taikant numatytąjį užsakymo tipą valdoma, koks bus sukuriamas užsakymo bendrasis planavimas.  

Programoje „Supply Chain Management“ palaikomos kelios vienu metu taikomos tiekimo strategijos, neatsižvelgiant į tiekimo grandinės modelį. Galite taikyti gamybos užsakymus, kurie gaunami naudojant „kanban“. Be to, galite naudoti paketinį užsakymą, kuriame turi būti įtrauktas perkeliant arba naudojant „kanban“ tiekiamas produktas.  

Programoje „Supply Chain Management“ užtikrinama, kad medžiagų srautas atitiks modelį.  

Kai jau apibrėžta tiekimo strategija, medžiagos paėmimo sandėlis apdorojimo laiku priskiriamas dinamiškai.  

„kanban“ naudojami trumpai, todėl jie paprastai nekuriami naudoti būsimame laikotarpyje. Kad būtų visiškai stebimi tiekimo grandinės procesai, pradėta taikyti nauja planavimo koncepcija „suplanuotas „kanban“, kuri naudojama iškeltiems poreikiams apskaičiuoti bei kurią naudojant užtikrinama, kad informacija apie poreikius būtų gaunama remiantis tais pačiais loginiais veiksmais, kurie naudojami kuriant faktinį „kanban“.  

Tie patys loginiai veiksmai atliekami taikant visų kitų tipų tiekimo strategijas. Taigi ilgalaikio medžiagų planavimo procesas vykdomas atliekant tuos pačius loginius veiksmus, kuriuos po gamybos ir tiekimo procesų patvirtinimo tikitės atlikti apdorodami faktinius užsakymus.

## <a name="materials-allocation-cross-supply-policy--resource-consumption-on-boms"></a>Medžiagų paskirstymo tiekiant į įvairias vietas strategija – KS išteklių suvartojimas
Išteklių suvartojimas yra svarbi funkcija. Naudojant išteklių suvartojimo funkciją medžiagų paėmimo sandėlis bus pasirenkamas dinamiškai remiantis tiekimo strategija (užsakymo tipu), be to, bus paprasčiau tvarkomi pagrindiniai duomenys.  

Naudojant išteklių suvartojimo funkciją sandėlis, iš kurio paimamos medžiagos, turi būti priskirtas pagal produkto tiekimo būdą. Kitaip tariant, apdorojimo laiku sistemoje surandami ištekliai, kurie turėtų būti naudojami gamybos procese. Tada pagal šiuos išteklius sistemoje surandamas paėmimo sandėlis.  

Jei užduotis nepriklausoma nuo tiekimo strategijos, o tiekimo procesas bus pakeistas, nereikia pakeisti KS informacijos. Atlikus ad hoc pakeitimus, programoje „Supply Chain Management“ užtikrinama, kad medžiagos būtų gaunamos iš tinkamo sandėlio.

## <a name="process-manufacturing--the-production-type"></a>Apdirbamoji gamyba – gamybos tipas
Kad būtų lanksčiai išnaudojamos visos įvairių režimų planavimo galimybės, su visais produktais rekomenduojama naudoti gamybos tipą KS. Tada galima naudoti gamybos užsakymus, „kanban“, perkėlimo užsakymus arba pirkimo užsakymus produktui tiekti. Vykdydami apdirbamosios gamybos procesą turite naudoti gamybos tipą **Formulė**, **Sudėtinis produktas**, **Šalutinis produktas** arba **Planavimo prekė**. Su šiais gamybos tipais negalima naudoti „kanban“ ir gamybos užsakymų.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]