---
title: Gamybos cecho vykdymo sąsajos konfigūravimas
description: Šioje temoje aprašoma, kaip sukurti vieną ar daugiau gamybos cecho vykdymo sąsajos konfigūracijų. Atidarius gamybos cecho vykdymo sąsają, ji automatiškai įkelia pasirinktą konfigūraciją ir užduoties filtrą, būdingus naršyklei ir įrenginiui. Konfigūracijoje nustatote strategijas, kurios turi būti taikomos konkrečiam naudojimui.
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgProductionFloorExecutionConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d34f9c235df480658a0935d731f7267a87894067
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556319"
---
# <a name="configure-the-production-floor-execution-interface"></a>Gamybos cecho vykdymo sąsajos konfigūravimas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Cecho darbuotojai naudoja gamybos cecho vykdymo sąsają savo kasdieniams darbams registruoti, pvz., užduočių pradžios laikui fiksuoti, atsiliepimams apie užduotis pateikti, netiesioginėms veikloms registruoti ir pranešti apie neatvykimą į darbą. Šios registracijos yra itin svarbios stebint eigą bei išlaidas gamybos užsakymams ir darbuotojų atlyginimo dydžio skaičiavimo pagrindas.

Atidarius gamybos cecho vykdymo sąsają, ji automatiškai įkelia pasirinktą konfigūraciją ir užduoties filtrą, būdingus naršyklei ir įrenginiui. Konfigūracijoje nustatote strategijas, kurios turi būti taikomos konkrečiam naudojimui. Štai keletas panaudojimo pavyzdžių.

- Naudodami įmonės salėje esantį įrenginį darbuotojai registruojasi atėję į biurą ir išeidami iš jo.
- Naudodami ceche esantį įrenginį mašinų operatoriai registruojasi pradedami ir užbaigdami užduotis. Jie taip pat registruoja pertraukas ir netiesioginę veiklą.

Šioje temoje aprašomos įvairios užduoties kortelės įrenginių konfigūravimo parinktys.

## <a name="turn-on-the-production-floor-execution-interface-and-its-related-optional-features"></a>Įjunkite gamybos aukšto vykdymo sąsają ir su ja susijusias pasirenkamas funkcijas

Gamybos aukšto vykdymo sąsaja pati kartu su keletu pasirenkamų nustatymų yra aprašomi šioje temoje ir turi būti įjungti jūsų sistemoje prieš tai, kai galėsite juos naudoti. Naudokite [Funkcijos valdymo](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) puslapį tam, kad įjungtumėte bet kurią funkciją aprašyta tolesniuose poskyriuose.

### <a name="the-production-floor-execution-interface"></a>Gamybos aukšto vykdymo sąsaja

Tai yra pirminė šioje temoje aprašyta funkcija. Ji įtraukia gamybos aukšto vykdymo sąsają į jūsų sistemą. Norėdami ją įjungti, įjunkite tolesnę funkciją [Funkcijos valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Gamybos aukšto vykdymas

### <a name="generate-license-plates"></a>Kurti licencijos plokšteles

Šios funkcijos leidžia licencijos plokštelės funkcijas veikti gamybos aukšto vykdymo sąsajoje. Jei norėtumėte jas naudoti, įjunkite tolesnes funkcijas [funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (tokia tvarka):

1. Užbaigtos ataskaitos numerio lentelė įtraukta į užduoties kortelės įrenginį
1. Įgalinkite automatinį numerio lentelės numerio generavimą, kai Užduoties kortelės įrenginyje pranešama apie pabaigimą

### <a name="print-labels"></a>Spausdinti etiketes

Šios funkcijos leidžia žymės spausdinimo funkcijas veikti gamybos aukšto vykdymo sąsajoje. Jei norėtumėte jas naudoti, įjunkite tolesnes funkcijas [funkcijų valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (tokia tvarka):

1. Užbaigtos ataskaitos numerio lentelė įtraukta į užduoties kortelės įrenginį
1. Spausdinti etiketę iš užduoties kortelės įrenginio

### <a name="allow-locking-the-touch-screen"></a>Leisti užrakinti jutiklinį ekraną

Ši funkcija įtraukia mygtuką į gamybos aukšto vykdymo sąsają, kuri leidžia darbuotojams valyti liečiamąjį ekraną. Norėdami ją naudoti, įjunkite tolesnę funkciją [Funkcijos valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Funkcija skirta užrakinti darbo kortelės prietaisą ir darbo kortelės terminalą jų valymui

### <a name="asset-management-functionality-for-the-production-floor-execution-interface"></a>Turto valdymo funkcijos gamybos vietos vykdymo sąsajai

Ši funkcija įtraukia turto valdymo skirtuką į gamybos vietos vykdymo sąsają. Darbuotojai gali naudoti šį skirtuką norėdami pasirinkti turtą, prijungtą prie įrenginio išteklių, kurie yra pasirinktame užduočių sąrašo filtre. Darbuotojas gali peržiūrėti pasirinkto įrenginio turto būseną ir sveikatą iš skaitiklio verčių (ne daugiau keturių pasirinktų skaitiklių). Norėdami naudoti šią funkciją, įjunkite tolesnę funkciją [Funkcijos valdyme](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):

- Turto valdymo funkcijos gamybos vietos vykdymo sąsajai

## <a name="work-with-production-floor-execution-configurations"></a>Darbas su gamybos cecho vykdymo konfigūracijomis

Norėdami kurti ir tvarkyti įrenginio konfigūracijas, eikite į **Gamybos kontrolė \> Sąranka \> Gamybos vykdymas \> Gamybos cecho vykdymo konfigūravimas**. Puslapyje **Gamybos cecho vykdymo konfigūravimas** rodomas esamų konfigūracijų sąrašas. Šiame puslapyje galite atlikti toliau pateiktus veiksmus.

- Pasirinkite bet kurią gamybos cecho konfigūraciją, nurodytą kairiajame stulpelyje, ir ją peržiūrėkite bei redaguokite.
- Norėdami į sąrašą įtraukti naują įrenginio konfigūraciją, veiksmų srityje pasirinkite **Nauja**. Tada įveskite pavadinimą lauke **Konfigūracija**, kad identifikuotumėte naują konfigūraciją. Jūsų įvestas pavadinimas negali sutapti su bet kokios kitos įrenginio konfigūracijos pavadinimu ir vėliau jo redaguoti negalėsite.

Tada konfigūruokite įvairius pasirinktos įrenginio konfigūracijos parametrus. Galimi šie laukai:

- **Tik atėjus į darbą ir išėjus iš darbo** – nustatykite šią parinktį į *Taip*, norėdami sukurti supaprastintą sąsają, leidžiančią naudoti tik atėjimo ir išėjimo iš darbo funkcijas. Taip išjungsite daugelį kitų šio puslapio parinkčių. Prieš įgalindami šią parinktį, pirmiausia turite pašalinti visas eilutes iš „FastTab” **Skirtuko pasirinkimas**.
- **Teikti kiekio ataskaitą išeinant iš darbo** – nustatykite šią parinktį į *Taip*, kad darbuotojai būtų paraginti pateikti atsiliepimų apie vykdomas užduotis prieš išeidami iš darbo. Kai parinktis nustatyta į *Ne*, darbuotojai nebus raginami.
- **Užrakinti darbuotoją** – kai ši parinktis nustatyta į *Ne*, darbuotojai bus atjungiami iš karto jiems pateikus registraciją (pvz., naujos užduoties). Tada įrenginys pereis prie prisijungimo puslapio. Kai ši parinktis nustatyta į *Taip*, darbuotojai liks prisijungę prie užduoties kortelės įrenginio. Tačiau darbuotojas gali atsijungti rankiniu būdu, kad kitas darbuotojas galėtų prisijungti, jei užduoties kortelės įrenginys vykdomas naudojant tą pačią sistemos vartotojo paskyrą. Daugiau informacijos apie šių tipų paskyras žr. [Priskirti vartotojai](config-job-card-device.md#assigned-users).
- **Naudoti faktinį registravimo laiką** – nustatykite šią parinktį į *Taip*, norėdami nustatyti kiekvienos naujos registracijos laiką į laiką, kada darbuotojas pateikė registraciją. Jei ši parinktis nustatyta į *Ne*, naudojamas prisijungimo laikas. Paprastai norėsite nustatyti šią parinktį į *Taip*, jei nustatėte parinktis **Užrakinti darbuotoją** ir (arba) **Vienas darbuotojas** į *Taip* ir jei darbuotojai dažnai būna prisijungę ilgesnį laikotarpį.
- **Vienas darbuotojas** – nustatykite šią pasirinktį į *Taip*, jei tik vienas darbuotojas naudoja kiekvieną užduoties kortelės įrenginį, kuriame ši konfigūracija yra aktyvi. Nustačius šią parinktį į *Taip*, parinktis **Užrakinti darbuotoją** automatiškai nustatoma į *Taip*. Be to, pasirinkus šį parametrą pašalinamas darbuotojo reikalavimas (ir galimybė) prisijungti naudojant ženklo ID (arba kitą panašų ID). Vietoje to, darbuotojas prisijungia prie „Microsoft Dynamics 365 Supply Chain Management“ naudodamas sistemos vartotojo paskyrą, kuri susieta su *registruojamo laiko darbuotoju* (iš *darbuotojų* lentelės), ir tuo pačiu metu prijungiamas prie užduoties kortelės įrenginio kaip tas darbuotojas.
- **Leisti užrakinti jutiklinį ekraną** – nustatykite šią pasirinktį į *Taip*, norėdami leisti darbuotojams užrakinti užduoties kortelės įrenginio jutiklinį ekraną, kad būtų galima jį nuvalyti. Nustačius šią parinktį į *Taip*, į įrenginio prisijungimo puslapį įtraukiamas mygtukas **Užrakinti ir valyti ekraną**. Kai darbuotojas pasirenka šį mygtuką, jutiklinis ekranas laikinai užrakinamas, kad būtų išvengta netyčinių įvesčių. Taip pat rodomas skaičiavimo atgal laikmatis. Tada darbuotojas gali saugiai nuvalyti įrenginį ir ekraną. Kai atgalinis skaičiavimas baigiasi, jutiklinis ekranas vėl automatiškai atrakinamas.
- **Ekrano užrakto trukmė** – kai parinktis **Leisti užrakinti jutiklinį ekraną** nustatyta į *Taip*, naudokite šią parinktį norėdami nurodyti, kiek sekundžių jutiklinis ekranas bus išjungtas, kad būtų galima jį nuvalyti. Trukmė turi būti nuo 5 iki 120 sekundžių.
- **Generuoti numerio lentelę** – nustatykite šią pasirinktį į *Taip*, norėdami generuoti naują numerio lentelę kiekvieną kartą, kai darbuotojas naudoja užduoties kortelės įrenginį, kad praneštų apie baigtą užduotį. Numerio lentelėje nurodytas numeris generuojamas naudojant skaičių seką, kuri nustatyta puslapyje **Sandėlio valdymo parametrai**. Kai ši parinktis nustatyta į *Ne*, darbuotojai turi nurodyti esamą numerio lentelę pranešdami apie baigtą užduotį.
- **Spausdinti žymą** – nustatykite šią parinktį į *Taip*, kad būtų spausdinama numerio lentelės žyma, kai darbuotojas naudoja užduoties kortelės įrenginį, kad praneštų apie baigtą užduotį. Žymos konfigūracija nustatoma dokumento maršruto planavimo dalyje, kaip nurodyta [Numerio lentelės žymų dokumentų maršrutų planavimo maketas](../warehousing/document-routing-layout-for-license-plates.md).
- **Skirtuko pasirinkimas**  – Naudokite nustatymus šiame skyriuje, kad pasirinktumėte, kurie skirtukai turi būti rodomi gamybos aukšto vykdymo sąsajoje, kai esama konfigūracija įjungta. Galite sukurti tiek skirtukų, kiek jums reikia ir tada įtraukti bei organizuoti juos kaip norite. Dėl informacijos, kaip sukurti skirtukus ir dirbti su nustatymais čia, žr. [Kurti gamybos aukšto vykdymo sąsają](production-floor-execution-tabs.md).

## <a name="clean-up-job-configurations"></a>Užduočių konfigūracijų valymas

Kai cecho prižiūrėtojas nustato gamybos cecho vykdymo sąsają, jis pasirenka konfigūraciją ir užduoties filtrą. Šie pasirinkimai saugomi „Supply Chain Management” nuorodų lentelėje, o naršyklė naudoja ID, saugomą vietiniame slapuke, kad būtų galima rasti teisingą tos lentelės eilutę. Be to, lentelė registruoja datą ir laiką, kada darbuotojas paskutinį kartą prisijungė prie kiekvieno įrenginio.

Paketinė užduotis periodiškai išvalo įrenginių, neužregistravusių veiklos per pastarąsias 60 dienų, nuorodų lentelės įrašus. Taip pat galite bet kada rankiniu būdu valyti įrašus, atlikdami toliau pateiktus veiksmus.

1. Eikite į **Gamybos kontrolė \> Sąranka \> Gamybos vykdymas \> Gamybos cecho vykdymo konfigūravimas**.
1. Veiksmų srityje pasirinkite **Valyti kliento konfigūracijas**.
1. Dialogo lange **Valyti kliento konfigūracijas** nustatykite lauką **Dienų skaičius** į neaktyvumo dienų skaičių (iki šios dienos), į kurį reikia atsižvelgti. Pašalinsite visas įrenginių, kurie nebuvo aktyvūs tuo metu, konfigūracijas ir prisijungimo įrašus.
1. Pasirinkite **Gerai**, norėdami išvalyti atitinkamas konfigūracijas pagal parametrą **Dienų skaičius**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]