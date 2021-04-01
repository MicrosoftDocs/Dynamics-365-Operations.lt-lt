---
title: Konfigūruoti įrenginių užduoties kortelę
description: Šioje temoje aprašomos įvairios užduoties kortelės įrenginio konfigūravimo parinktys.
author: johanhoffmann
manager: tfehr
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch, JmgRegistrationTouchUserConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: c139fb7daa0f40b6b7afb0a707f714502d3146d1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246362"
---
# <a name="configure-job-card-for-devices"></a>Konfigūruoti įrenginių užduoties kortelę

[!include [banner](../includes/banner.md)]

Darbo kortelės įrenginį naudoja parduotuvės cecho darbuotojai savo kasdieniams darbams registruoti, pvz., užduočių pradžios laikui fiksuoti, grįžtamajam ryšiui apie užduotis pateikti, netiesioginėms veikloms registruoti ir pranešti apie neatvykimą į darbą. Šios registracijos yra itin svarbios stebint eigą bei išlaidas gamybos užsakymams ir darbuotojų atlyginimo dydžio skaičiavimo pagrindas. Šioje temoje aprašomos įvairios užduoties kortelės įrenginių konfigūravimo parinktys.

## <a name="enable-new-features-in-feature-management"></a>Naujų funkcijų įjungimas funkcijų valdymo dalyje

Norėdami naudoti kai kuriuos šioje temoje aprašytus parametrus, juos turite įjungti savo sistemoje. Naudokite puslapį [funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), kad įjungtumėte bet kurias arba visas toliau išvardytas funkcijas.

### <a name="generate-license-plate"></a>Generuoti numerio lentelę

Norėdami naudoti šią funkciją, įjunkite toliau išvardytas funkcijas puslapyje [funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (nurodyta tvarka):

1. Užbaigtos ataskaitos numerio lentelė įtraukta į užduoties kortelės įrenginį
1. Įgalinkite automatinį numerio lentelės numerio generavimą, kai Užduoties kortelės įrenginyje pranešama apie pabaigimą

### <a name="print-label"></a>Spausdinti žymą

Norėdami naudoti šią funkciją, įjunkite toliau išvardytas funkcijas puslapyje [funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (nurodyta tvarka):

1. Užbaigtos ataskaitos numerio lentelė įtraukta į užduoties kortelės įrenginį
1. Spausdinti etiketę iš užduoties kortelės įrenginio

### <a name="allow-locking-of-touch-screen"></a>Leisti užrakinti jutiklinį ekraną

Norėdami naudoti šią funkciją, įjunkite toliau nurodytą funkciją puslapyje [funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- (Peržiūra) Funkcija, skirta užrakinti užduoties kortelės įrenginį ir užduoties kortelės terminalą, kad juos būtų galima dezinfekuoti

## <a name="manage-your-device-configurations"></a>Jūsų įrenginio konfigūracijų tvarkymas

Norėdami nustatyti savo įrenginio konfigūracijas, eikite į **Gamybos kontrolė > Sąranka > Gamybos vykdymas > Konfigūruoti įrenginių užduoties kortelę**. Bus atidarytas puslapis **Konfigūruoti įrenginių užduoties kortelę**, kuriame rodomas esamų konfigūracijų sąrašas. Čia galite atlikti toliau nurodytus veiksmus. 

- Pasirinkti bet kurią įrenginio konfigūraciją, nurodytą kairiajame stulpelyje, ir ją peržiūrėti bei redaguoti.
- Norėdami į sąrašą įtraukti naują įrenginio konfigūraciją, veiksmų srityje pasirinkite **Nauja**. Tada įveskite pavadinimą lauke **Konfigūracija**, kad identifikuotumėte naują konfigūraciją. Čia įvesta vertė negali sutapti su bet kokios kitos įrenginio konfigūracijos verte ir vėliau jos redaguoti negalėsite.

Išsamesnės informacijos apie kiekvieną užduoties kortelės įrenginių konfigūravimo parametrą ieškokite tolesniuose skyriuose.

## <a name="general-settings"></a>Bendrieji parametrai

„FastTab“ **Bendra** leidžia jums konfigūruoti kiekvieną iš įvairių parinkčių, galimų pasirinktai įrenginio konfigūracijai. Galimi šie parametrai:

- **Teikti kiekio ataskaitą išeinant iš darbo** – nustatykite šią parinktį į **Taip**, kad darbuotojai būtų paraginti pateikti grįžtamąjį ryšį apie vykdomas užduotis prieš išeidami iš darbo. Kai parinktis nustatyta į **Ne**, darbuotojai nebus raginami.
- **Užrakinti darbuotoją** – kai ši pasirinktis nustatyta į **Ne**, kiekvienas darbuotojas bus iš karto atjungtas po to, kai atlieka registraciją (pvz., naujos užduoties), o tada įrenginys grįš į prisijungimo puslapį. Kai ši parinktis nustatyta į **Taip**, kiekvienas darbuotojas liks prisijungęs prie užduoties kortelės įrenginio. Tačiau darbuotojas vis dar galės atsijungti neautomatiniu būdu, kad leistų prisijungti kitam darbuotojui, o užduoties kortelės įrenginys toliau veiks su ta pačia sistemos vartotojo paskyra. Daugiau informacijos apie šių tipų paskyras žr. [Priskirti vartotojai](#assigned-users).
- **Brūkšninių kodų skaitytuvas** – nustatykite šią parinktį į **Taip**, kad užduoties kortelės įrenginyje atsirastų parinktis, leidžianti darbuotojams užregistruoti naujos užduoties pradžią nuskenuojant brūkšninį kodą.
- **Naudoti faktinį registravimo laiką** – nustatykite šią parinktį į **Taip**, kad nustatytas kiekvienos naujos registracijos laikas būtų lygus faktiniam laikui, kuriuo registraciją pateikė darbuotojas. Nustatykite į **Ne**, jei norite naudoti prisijungimo laiką. Paprastai nerekomenduojama nustatyti vertę **Taip**, jei įjungėte parinktis **Užrakinti darbuotoją** ir (arba) **Vienas darbuotojas**, kai darbuotojai dažnai būna prisijungę ilgesnį laikotarpį.
- **Vienas darbuotojas** – nustatykite šią pasirinktį į **Taip**, jei tik vienas darbuotojas naudoja kiekvieną užduoties kortelės įrenginį, kuriame ši konfigūracija yra aktyvi. Pasirinkus šią parinktį, parinktis **Užrakinti darbuotoją** automatiškai nustatoma į **Taip**. Be to, pasirinkus šią pasirinktį pašalinamas darbuotojo reikalavimas (ir galimybė) prisijungti naudojant ženklo ID (arba panašų būdą). Vietoje to, darbuotojas prisijungia prie „Supply Chain Management“ naudodamas sistemos vartotojo paskyrą, kuri susieta su *registruojamo laiko darbuotoju* (iš *darbuotojų* lentelės), ir tuo pačiu metu prijungiamas prie užduoties kortelės įrenginio tas darbuotojas.  Daugiau informacijos apie šių tipų paskyras žr. [Priskirti vartotojai](#assigned-users).
- **Leisti darbuotojams nustatyti asmeninius filtrus** – nustatykite šią parinktį į **Taip**, norėdami leisti darbuotojams filtruoti įrenginyje jiems rodomas užduotis. Darbuotojas gali keisti bet kurių trijų filtro kriterijų vertes: **Gamybos vienetas**, **Išteklių grupė** ir **Išteklius**. Įrenginyje bus rodomos tik tos užduotys, kurios suplanuotos ištekliams, atitinkantiems pasirinktus filtro kriterijus. Taip pat galite norimiems arba visiems šiems kriterijams priskirti numatytąsias vertes, kurios bus taikomos net tada, kai ši parinktis nėra pasirinkta.
- **Leisti užrakinti jutiklinį ekraną** – nustatykite šią pasirinktį į **Taip**, norėdami leisti darbuotojams užrakinti užduoties kortelės įrenginio jutiklinį ekraną, kad būtų galima jį nuvalyti. Kai ši parinktis įjungta, į įrenginio prisijungimo puslapį įtraukiamas mygtukas **Užrakinti ir valyti ekraną**. Kai darbuotojas pasirenka šį mygtuką, jutiklinis ekranas laikinai užrakinamas, kad būtų išvengta netyčinių įvesčių, ir rodomas skaičiavimo atgal laikmatis. Dabar darbuotojas gali saugiai nuvalyti prietaisą ir ekraną. Kai atgalinis skaičiavimas baigiasi, jutiklinis ekranas vėl automatiškai atrakinamas.
- **Ekrano užrakto trukmė** – kai įjungta parinktis **Leisti užrakinti jutiklinį ekraną**, naudokite šią parinktį, kad nurodytumėte, kiek sekundžių jutiklinis ekranas bus išjungtas, kad būtų galima jį nuvalyti. Trukmė turi būti nuo 5 iki 120 sekundžių.
- **Gamybos vienetas** – pasirinkite gamybos vienetą, kuris bus taikomas kaip numatytasis užduočių sąrašo, rodomo kiekvienam darbuotojui, filtro kriterijus. Iš pradžių įrenginyje bus rodomos tik tos užduotys, kurios suplanuotos ištekliams, sugrupuotiems pagal pasirinktą gamybos vienetą. Jei parinktis **Leisti darbuotojams nustatyti asmeninius filtrus** įjungta, darbuotojai galės redaguoti šią vertę, priešingu atveju šis filtras bus taikomas visada, kai suaktyvinta ši įrenginio konfigūracija.
- **Išteklių grupė** – pasirinkite išteklių grupę, kuri bus taikoma kaip numatytasis užduočių sąrašo, rodomo kiekvienam darbuotojui, filtro kriterijus. Iš pradžių įrenginyje bus rodomos tik tos užduotys, kurios suplanuotos ištekliams, sugrupuotiems pagal pasirinktą išteklių grupę. Jei parinktis **Leisti darbuotojams nustatyti asmeninius filtrus** įjungta, darbuotojai galės redaguoti šią vertę, priešingu atveju šis filtras bus taikomas visada, kai suaktyvinta ši įrenginio konfigūracija.
- **Išteklius** – pasirinkite išteklių, kuris bus taikomas kaip numatytasis užduočių sąrašo, rodomo kiekvienam darbuotojui, filtro kriterijus. Iš pradžių įrenginyje bus rodomos tik tos užduotys, kurios suplanuotos pasirinktam ištekliui. Jei parinktis **Leisti darbuotojams nustatyti asmeninius filtrus** įjungta, darbuotojai galės redaguoti šią vertę, priešingu atveju šis filtras bus taikomas visada, kai suaktyvinta ši įrenginio konfigūracija.
- **Generuoti numerio lentelę** – nustatykite šią pasirinktį į **Taip**, kad sugeneruotumėte naują numerio lentelę kiekvieną kartą, kai darbuotojas naudoja užduoties kortelės įrenginį, kad praneštų apie baigtą užduotį. Numerio lentelėje nurodytas numeris generuojamas naudojant skaičių seką, kuri nustatyta puslapyje **Sandėlio valdymo parametrai**. Kai nustatyta į **Ne**, darbuotojai turi nurodyti esamą numerio lentelę, kai praneša apie baigtą užduotį.
- **Spausdinti etiketę** – nustatykite šią pasirinktį į **Taip**, kad būtų spausdinama numerio lentelės etiketė, kai darbuotojas naudoja užduoties kortelės įrenginį, kad praneštų apie baigtą užduotį. Etiketės konfigūracija nustatoma dokumento maršruto planavimo dalyje, kaip nurodyta [Numerio lentelės etikečių dokumentų maršrutų planavimo maketas](../warehousing/document-routing-layout-for-license-plates.md).

<a name="assigned-users"></a>

## <a name="assigned-users"></a>Priskirti vartotojai

Naudokite „FastTab“ **Priskirti vartotojai**, kad susietumėte vieną ar daugiau sistemos vartotojų su dabartine įrenginio konfigūracija. Kiekvienam sistemos vartotojui galima priskirti tik vieną užduoties įrenginio konfigūraciją.

Nustatant įrenginį, IT darbuotojas paprastai prisijungia prie „Supply Chain Management“ naudodamas sistemos vartotojo paskyrą. Po to užduoties įrenginio konfigūracija, susieta su tuo sistemos vartotoju, taikoma tol, kol sistemos vartotojas išlieka prisijungęs. Šios sistemos vartotojo paskyros paprastai ribojamos, kad leistų prieigą tik prie užduoties kortelės įrenginio puslapio, o ne prie kitų „Supply Chain Management“ dalių.

Sistemos vartotojui prisijungus ir įkėlus užduoties įrenginio konfigūraciją, darbuotojai gali prisijungti prie užduoties kortelės įrenginio naudodami savo *registruojamo laiko darbuotojo* paskyrą (pavyzdžiui, nuskaitydami savo ženklelyje esantį brūkšninį kodą), kad galėtų pradėti naujas užduotis ir atlikti kitas registracijas. Per dieną gali prisijungti ir atsijungti įvairūs darbuotojai, kol įrenginyje naudojama ta pati įrenginio konfigūracija, nes sistemos vartotojas išlieka prisijungęs prie „Supply Chain Management“ visą dieną.

Tačiau, kaip minėta anksčiau, kai naudojate įrenginio konfigūraciją su parinktimi **Vienas darbuotojas**, patys darbuotojai paprastai prisijungia prie „Supply Chain Management“ naudodami sistemos vartotoją, susietą su jų *registruojamo laiko darbuotojo* paskyra, todėl jie įkelia įrenginio konfigūraciją ir tuo pačiu metu prisijungia prie užduoties kortelės įrenginio kaip darbuotojas.

## <a name="additional-resources"></a>Papildomi ištekliai

[Pranešimas apie baigtą užduotį iš užduoties kortelės įrenginio.](report-finished-job-device.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]