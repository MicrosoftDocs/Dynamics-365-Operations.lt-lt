---
title: Sistemos nukreiptas klasterio paėmimas
description: Šioje temoje apžvelgiamas sistemos nukreiptas klasterio paėmimas „ Microsoft Dynamics 365 Supply Chain Management“.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkCluster, WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0838405bcb5ee0d8e582093fbbd69553228cb2b6
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016038"
---
# <a name="system-directed-cluster-picking"></a>Sistemos nukreiptas klasterio paėmimas

[!include [banner](../includes/banner.md)]

Klasterio paėmimas yra vieneto paėmimo procesas, kuris leidžia paimti prekes keletui užsakymų vienu metu, grupuojant juos į paėmimo klasterius. Tada paėmimo vietą teks aplankyti tik vieną kartą. Paprastai ši funkcija naudojama paimant nedidelius užsakymus arba kiekius, kurie yra mažesni už atvejo kiekius.

Kai nustatytas sistemos nukreiptas klasterio paėmimas, galima paimti darbo antraščių klasterius, remiantis sistemos sukurtu klasteriu. Sistema paima užsakymų klasterius, kurių vietų skaičius neviršija klasterio šablone nurodyto skaičiaus. Todėl galite paimti keletą užsakymų tuo pačiu metu, nekurdami klasterio rankiniu būdu.

Sistemos nukreiptas klasterio paėmimas – tai klasterių kūrimo rankiniu būdu, kai klasterio šablonas naudojamas klasteriui kurti, alternatyva. Prieš pradedant naudoti klasterio šabloną, jame reikia apibrėžti keletą su sąranka susijusių eilučių.

- **Vietų skaičius** atitinka užsakymų, kurie bus įtraukti į klasterį, skaičių. Todėl jis atitinka krepšių skaičių.
- **Skaidyti klasterį** nustato, kada klasterį reikia suskaidyti.
- **Generuoti klasterio ID** kontroliuoja, ar klasterio ID bus sugeneruotas sistemos, ar įvestas vartotojo.
- **Rūšiavimo patikros tipas** nustato, ar reikia atlikti vietų tikrinimą.

Naujas mobiliojo įrenginio meniu elementas naudojamas atliekant sistemos nukreiptą klasterio paėmimą. **Klasterio profilis ID** turi būti nurodytas pažymėtai **Nukreipė** parinkčiai. Be to, sistemos nukreiptos darbo sekos užklausos gali grupuoti užsakymus pagal konkrečius įmonės kriterijus. Todėl galite dar labiau optimizuoti darbo užsakymų priskyrimą nurodydami pritaikytus rūšiavimo kriterijus naudodami sistemos nukreiptas darbo sekos užklausas.

Įjungus sistemos nukreiptą klasterio atrinkimą, sandėlio darbininkams pateikiamas klasteris, kuriame užsakymų paėmimas iš anksto priskirtas klasterio pozicijai. Todėl darbininkai gali pradėti paimti prekę keletui darbo užsakymų, apsilankydami paėmimo vietoje tik vieną kartą. Sistemos nukreipto klasterio paėmimo procesas sutampa su vartotojo nukreipto klasterio paėmimo procesu.

## <a name="enable-the-system-directed-cluster-picking-feature"></a>Įjunkite sistemos nukreiptą klasterio paėmimo funkciją

Norėdami pasinaudoti šia funkcija, ją turite įjungti savo sistemoje. Administratoriai gali naudoti [funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) puslapį, kad patikrintų funkcijos būseną ir įjungtų ją, jei reikia. Čia funkcija yra nurodyta kaip:

- **Modulis** – Sandėlio valdymas
- **Funkcijos pavadinimas** – sistemos nukreiptas klasterio paėmimas

Šiai funkcijai naudoti būtina įjungti priklausančią funkciją. Priklausanti funkcija yra:

- **Modulis** – Sandėlio valdymas
- **Funkcijos pavadinimas** – organizacijoje naudojama sistemos nukreipta darbo eiga

## <a name="set-up-system-directed-cluster-picking"></a>Sistemos nukreipto klasterio paėmimo sąranka

### <a name="create-cluster-profiles"></a>Klasterių šablonų kūrimas

Klasterių šablonai kontroliuoja, kaip sistema sukuria kiekvieną klasterį. Jei reikia skirtingų klasterių, kiekvienam mobiliojo įrenginio meniu elementui reikia sukurti atskirą klasterio šabloną.

1. Eikite į **Sandėlio valdymas \> Sąranka \> Mobilusis įrenginys \> Klasterio šablonai**.
2. Pasirinkite **Naujas**.
3. Lauke **Klasterio šablono ID** įveskite **2 vietos**.
4. Lauke **Pavadinimas** įveskite **2 vietos**.
5. **Bendra** „FastTab” skirtuke įveskite šią informaciją:

    - **Generuoti klasterio ID** – pasirinkite **Taip**. Ši pasirinktis nustato, ar sistema automatiškai sukuria klasterio ID, ar vartotojas jį sukuria paėmimo pradžioje. 
    - **Aktyvuoti pozicijas** – pasirinkite **Taip**. Ši pasirinktis nustato, ar vietų pavadinimai generuojami automatiškai, atsižvelgiant į vietų pavadinimų sąranką. Jei nustatyta šios parinkties vertė **Ne** , naudojamas vietos numerio lentelės ID.
    - **Pozicijų skaičius** – pasirinkite **2**. Šiame lauke nustatomas didžiausias vietų, kurias galima įtraukti į klasterį, skaičius (t. y., didžiausias dėžių, krepšių ir t. t. skaičius).
    - **Pozicijos pavadinimas** – pasirinkite **Skaitinis** , kad pozicijos būtų pavadintos naudojant ištisinius skaičius. Jei pasirinksite **Abėcėlė** , vietoms bus suteikiami pavadinimai abėcėlės tvarka.
    - **Skaidyti klasterį:** – pasirinkite **Dėti**. Šiame lauke nustatoma, kada klasteris skaidomas. 
    - **Rūšiavimo patikros tipas:** – pasirinkite **Pozicijos nuskaitymas**. Šiame lauke nustatoma, ar tikrinamas dėjimo į vietą veiksmas.
        
6. **Klasterių rūšiavimas** „FastTab“ galite nustatyti rūšiavimo kriterijus sukurdami naują eilutę ir įvesdami šią informaciją:

    - **Sekos numeris** – pasirinkite **1**. Šis laukas nustato seką, pagal kurią sistema rūšiuoja. Vertė įvedama automatiškai, bet galite ją pakeisti pagal poreikį.
    - **Lauko pavadinimas** – įveskite **WMSVietosId**. Šiame lauke nustatomas laukas, kuris eilutėje naudojamas rūšiavimo kriterijams nustatyti.
    - **Rūšiavimas** – pasirinkite **Didėjančia tvarka**. Šiame lauke apibrėžiama, ar rūšiuojama didėjimo, ar mažėjimo tvarka.

### <a name="create-a-mobile-device-menu-item"></a>Mobiliojo įrenginio meniu elemento kūrimas

Norėdami sukurti naują mobiliojo įrenginio meniu elementą sistemos nukreiptam klasterio paėmimui atlikti ir susieti klasterio šablono ID su mobiliojo įrenginio meniu elementu, atlikite šiuos veiksmus.

1. Eikite į **Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu elementai**.
1. Pasirinkite **Naujas**.
1. Antraštės dalyje įveskite šią informaciją:
    - **Meniu elemento pavadinimas** – SD klasteris
    - **Pareigos** – SD klasteris
    - **Režimas** – Darbas
    - **Naudoti esamą darbą** – Taip

1. **Bendra** „FastTab” skirtuke įveskite šią informaciją:
    - **Nukreipė** – sistemos nukreiptas klasterio paėmimas
    - **Generuoti numerio lentelę** – Taip
    - **Klasterio profilio ID** – 2 pozicija

1. „FastTab“ **Darbo klasės** nustatykite tinkamą darbo klasę šiam mobiliojo įrenginio meniu elementui, nustatydami toliau pateikiamus laukus.
    - **Darbo klasės ID** – Pardavimai
    - **Darbo užsakymo tipas** – Pardavimų užsakymai

1. **Mobiliojo įrenginio meniu elementai** Veiksmų srityje pasirinkite **Sistemos nukreiptos darbo sekos užklausos** ir atlikite šiuos veiksmus, kad nurodytumėte naują sistemos nukreiptą darbo sekos užklausą:
    - Pasirinkite **Naujas** Veiksmų srityje.
    - **Sekos numeris** – 1
    - **Aprašas** – Darbo prioritetas – Darbo ID

1. Veiksmų srityje pasirinkite **Redaguoti užklausą**
1. Pasirinkite skirtuką **Rūšiavimas**
1. Pasirinkite **Pridėti** , kad pridėtumėte naują eilutę, tada įveskite šią informaciją:
    - **Lentelė** – Darbas
    - **Išvestinė lentelė** – Darbas
    - **Laukas** – Darbo prioritetas
    - **Ieškos kryptis** – Didėjanti tvarka
1. Pasirinkite **Pridėti** , kad pridėtumėte antrą eilutę, tada įveskite šią informaciją:
    - **Lentelė** – Darbas
    - **Išvestinė lentelė** – Darbas
    - **Laukas** – Darbo ID
    - **Ieškos kryptis** – Didėjanti tvarka

1. Sistema dabar rūšiuos darbo ID klasteryje, pirmiausia pagal darbo prioritetą, paskui pagal darbo ID.

### <a name="set-up-a-mobile-device-menu"></a>Mobiliojo įrenginio meniu nustatymas

1. Eikite į **Sandėlio valdymas > Sąranka > Mobilusis įrenginys > Mobiliojo įrenginio meniu**.
1. Pridėkite **SD klasteris** meniu elementą, kurį ką tik sukūrėte Mobiliojo įrenginio meniu.
1. Pasirinkite **Siunčiama** meniu.
1. Pasirinkite **Redaguoti** iš Veiksmų srities.
1. Slinkite, kol rasite **SD klasteris**.
1. Pasirinkite **SD klasteris** , rodyklė, rodanti į **Meniu struktūra** sąrašą, bus įjungta.
1. Pasirinkite **rodyklė** mygtuką, kad perkeltumėte **SD klasteris** meniu elementą į **Siunčiama** meniu struktūrą.
1. Pasirinkite **SD klasteris** iš **Meniu struktūra** sąrašo, tada pasirinkite **Į VIRŠŲ** arba **Į APAČIĄ** rodykles, kad perkeltumėte meniu elementą į pageidaujamą poziciją mobiliojo įrenginio meniu.

## <a name="scenario"></a>Scenarijus

### <a name="create-picking-work"></a>Paėmimo darbo kūrimas

Prieš nustatant sistemos nukreiptą klasterio paėmimą, turite sukurti tinkamą siuntimo darbą. Anksčiau sukurtame klasterio profilyje nurodytos dvi klasterio vietos. Todėl turite sukurti bent du darbo ID. Šiuo atveju sukursite du pardavimų užsakymus, rezervo atsargas, išleisite pardavimų užsakymus sandėliui ir tada rankiniu būdu apdorosite bangą.

1. Eikite į **Pardavimai ir rinkodara > Pardavimų užsakymai > Visi pardavimų užsakymai**.
1. Pasirinkite **Nauja** Veiksmų srityje, kad sukurtumėte pirmąjį pardavimo užsakymą.
    - Atsivėrus **Sukurti pardavimo užsakymą** meniu, įveskite šią informaciją:
        - **Klientas** „FastTab”, įveskite **Kliento paskyra** - **JAV-004**.
        - **Bendra** „FastTab” įveskite **Sandėlis** - **62**.
        - Pasirinkite **Gerai** , kad uždarytumėte meniu ir sukurtumėte pardavimo užsakymą.
    - **Pardavimo užsakymo eilutės** „FastTab” pasirinkite **Pridėti eilutę** , jei nauja eilutė nėra automatiškai pridedama, ir įveskite šią informaciją:
        - **Prekės numeris** – A0001
        - **Kiekis** – 1
        - Pasirinkite **Įtraukti eilutę** , kad įtrauktumėte antrą eilutę.
        - **Prekės numeris** – A0002
        - **Kiekis** – 3
    - Rezervuokite atsargas, skirtas abiems jūsų ką tik sukurtoms eilutėms.
        - Pasirinkite **1-a eilutė**.
        - **Pardavimo užsakymo eilutės** Veiksmų srityje pasirinkite **Atsargos** ir tada iš sąrašo pasirinkite **Rezervacija**.
        - **Rezervavimas** formoje pasirinkite **Rezervuoti partiją** atsargų rezervavimui.
        - Užverkite **Rezervacija** formą pabaigus rezervaciją.
        - Pakartokite šiuos žingsnius, kad rezervuotumėte atsargas, skirtas **2-a eilutė**.
1. Pasirinkite **Nauja** Veiksmų srityje, kad sukurtumėte antrąjį pardavimo užsakymą
    - Atsivėrus **Sukurti pardavimo užsakymą** meniu, įveskite šią informaciją:
        - **Klientas** „FastTab” įveskite **Kliento paskyra** - **JAV-005**.
        - **Bendra** „FastTab” įveskite **Sandėlis** - **62**.
        - Pasirinkite **Gerai** , kad uždarytumėte meniu ir sukurtumėte pardavimo užsakymą
    - **Pardavimo užsakymo eilutės** „FastTab” pasirinkite **Pridėti eilutę** , jei nauja eilutė nėra automatiškai pridedama, ir įveskite šią informaciją:
        - **Prekės numeris** – A0001
        - **Kiekis** – 4
        - Pasirinkite **Įtraukti eilutę** , kad įtrauktumėte antrą eilutę.
        - **Prekės numeris** – A0002
        - **Kiekis** – 2
    - Rezervuokite atsargas, skirtas abiems jūsų ką tik sukurtoms eilutėms.
        - Pasirinkite **1-a eilutė**.
        - **Pardavimo užsakymo eilutės** Veiksmų srityje pasirinkite **Atsargos** ir tada iš sąrašo pasirinkite **Rezervacija**.
        - **Rezervavimas** formoje pasirinkite **Rezervuoti partiją** atsargų rezervavimui.
        - Užverkite **Rezervacija** formą pabaigus rezervaciją.
        - Pakartokite šiuos žingsnius, kad rezervuotumėte atsargas, skirtas **2-a eilutė**.
    - Uždarykite pardavimo užsakymą ir grįžkite į **Visi pardavimų užsakymai** sąrašo puslapį.
1. Raskite du jūsų ką tik sukurtus pardavimų užsakymus (gali prireikti atnaujinti puslapį). Lentelėje pasirinkite abu pardavimo užsakymus naudodami sekcijos žymės langelį.
    - **Visi pardavimų užsakymai** Veiksmų srityje pasirinkite **Sandėlis** skirtuką.
    - **Veiksmai** grupėje pasirinkite **Išleisti į sandėlį** , kad išleistumėte abu pardavimų užsakymus į sandėlį.
1. Kai išleidimo į sandėlį procesas baigtas, bus rodomas informacinis pranešimas.
    - Bus sukurtos kiekvieno pardavimo užsakymo siuntos.
    - Banga bus sukurta ir abi siuntos bus priskirtos bangai. Pasižymėkite **Bangos ID**.
1. Eikite į **Sandėlio valdymas > Siunčiamos bangos > Siuntų bangos > Visos bangos**.
    - **Visos bangos** sąraše raskite ir pasirinkite **Bangos ID** , kurią sukūrėte ankstesniame veiksme.
    - Veiksmų srityje pasirinkite skirtuką **Banga**.
    - **Banga** grupėje pasirinkite **Procesas** , kad apdorotumėte bangą ir sukurtumėte **Darbas**.
    - Pasibaigus apdorojimui, bus rodomi informaciniai pranešimai, rodantys, kad darbas sukurtas ir banga užregistruota.
1. **Pasirinktina** : eikite į **Sandėlio valdymas > Darbas > Darbo informacija** , kad peržiūrėtumėte sukurtą darbą. Sukuriami du skirtingi darbo ID. Kiekviename darbo ID yra dvi paėmimo eilutės.

### <a name="run-the-mobile-device-flow"></a>Mobiliojo įrenginio srauto vykdymas

1. Prisijunkite prie vartotojo mobiliojo įrenginio sandėlyje **62**.
1. **Pagrindinis meniu** pasirinkite **Siunčiama**.
1. **Siunčiama** meniu pasirinkite **SD klasteris** , kad pradėtumėte paėmimą.
    - Sukuriamas klasteris ir prie jo pridedami jūsų anksčiau sukurti du darbo ID. Jei sukūrėte daugiau kaip du darbo ID, į klasterį įtraukiami tik pirmieji du. Atkreipkite dėmesį, kad darbo ID įtraukiami į klasterį didėjimo tvarka, kaip nurodyta užklausos sąrankoje.

    > [!NOTE]
    > Naujas klasteris sukuriamas automatiškai, tik jei anksčiau buvo sukurta pakankamai papildomų darbo ID. Priešingu atveju rodomas šis pranešimas: „Nepakanka darbo klasteriui“.

    - Pasirinkus meniu, rodomas pirmas paėmimo ekranas. Sistema sujungia visas atitinkančias paėmimo eilutes iš dviejų darbo ID ir nukreipia jus į paėmimo vietą vieną kartą, kad galėtumėte įvykdyti abu užsakymus vienu paėmimu. Šis procesas atliekamas taip pat, kaip ir vartotojo nukreiptas klasterio paėmimo procesas.

1. Patvirtinkite pirmojo paėmimo vietą ir prekę pasirinkdami **Gerai**.
    - Paėmimo kiekis bus bendra prekės, rodomos klasterio pardavimų užsakymuose, suma.
1. Įveskite pareigų pavadinimą (skaičių arba abėcėlės raidę), kad patvirtintumėte, jog pozicijai paimtas prekių kiekis buvo padėtas tinkamoje pozicijoje.
1. Pakartokite šį procesą, kol visi prekių kiekiai bus paimti ir padėti į tinkamą poziciją.
1. Paskutinis mobiliajame įrenginyje atliktinas veiksmas yra **Padėti** klasterį į galutinę vietą. Pasirinkite **Gerai**
    - Patvirtinus padėjimo operaciją, klasteris uždaromas ir skaidomas, atsižvelgiant į vertę, kurią nustatėte klasterio šablono lauke **Skaidyti klasterį**. Darbo ID taip pat yra uždaromi.
1. Mobiliajame įrenginyje rodomas pranešimas „Klasteris baigtas“.
