---
title: Atsargų paieškos operacija EKA
description: Šioje temoje aprašoma, kaip naudoti atsargų peržvalgos operaciją kasos punkte (EKA) norint peržiūrėti turimų produktų atsargas parduotuvėse ir „Dynamics 365 Commerce“ sandėliuose.
author: boycezhu
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: c0f753febb0d347015fde1374148835f90df55a3
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353785"
---
# <a name="inventory-lookup-operation-in-pos"></a>Atsargų paieškos operacija EKA

[!include [banner](includes/banner.md)]

Šioje temoje aprašoma, kaip naudoti atsargų peržvalgos operaciją kasos punkte (EKA) norint peržiūrėti turimų produktų atsargas parduotuvėse ir „Dynamics 365 Commerce“ sandėliuose.

Tikslus visos organizacijos atsargų vaizdas realiuoju laiku parduotuvių atstovams padeda teikti savalaikį ir veiksmingą aukščiausios kokybės klientų aptarnavimą. Svarbiausias yra tas momentas, kai klientas yra pasirengęs priimti pirkimo sprendimą. Parduotuvių kasininkams mažmeninėje prekyboje svarbu po ranka turėti realiuoju laiku matomą atsargų informaciją, kad galėtų tiksliai planuoti produktų pristatymą ir paėmimą.

Atsargų peržvalgos operacija naudojant „Commerce“ EKA padeda mažmenininkams pasiekti veikimo reikalavimus ir gauti žinių prijungiant parduotuves su „Commerce Headquarters". Ši funkcija pateikia parduotuvių ir sandėlių produktų atsargų prieinamumo rodinį. Ji taip pat padeda mažmenininkams pasiekti papildomo efektyvumo ir sumažinti išlaidas tobulinant atsargų planavimą realiuoju laiku.

Kai atsargų peržvalgos operacija pradedama naudojant EKA programą, EKA kasininkas, užklausdama dėl atsargų informacijos, naudoja skaitinę klaviatūrą. Jei įvestas produktas turi variantų, kasininkas gali pasirinktinai pasirinkti dimensijas ar kitas vertes, kad galėtų patikrinti konkretaus produkto varianto atsargų informaciją.

## <a name="inventory-lookup-list-view-for-individual-products"></a>Atskirų produktų atsargų peržvalgos sąrašo rodinys

Atskiro produkto atsargų peržvalgos operacija pateikia atsargų peržvalgos sąrašo rodinį, kuriame pateikiama ši vietų sąrašo produkto informacija:

- **Atsargos** – nurodo produkto „turimas faktinis" kiekį.
- **Rezervuotas** – nurodo „faktiškai rezervuotą" kiekį, nuskaityą iš būstinės.
- **Užsakymas** – nurodo „iš viso užsakytą" kiekį, nuskaityą iš būstinės.
- **Vienetas** – nurodo atsargų matavimo vienetą, sukonfigūruotą būstinėje.

Vietų sąrašo rodinys apima visas parduotuves ir sandėlius, sukonfigūruotus įvykdymo grupėse, su kurias susieta dabartinė parduotuvė, kaip parodyta toliau pateiktame pavyzdyje.

![Atsargų paieškos operacijos sąrašo rodinys.](media/inventory-lookup-list-view.png)

> [!NOTE]
> Įsitikinkite, kad dabartinė parduotuvė įtraukta į susietas įvykdymo grupes.

Toliau nurodyti veiksmai galimi EKA programų juostoje:

- **Rūšiuoti** – šis veiksmas leidžia EKA vartotojui rūšiuoti duomenis sąrašo rodinyje pagal įvairius kriterijus. Rūšiavimas pagal vietą yra numatytoji rūšiavimo pasirinktis. 
  - **Geografinė vieta** (nuo artimiausios vietos iki tos vietos, palyginti su dabartine parduotuve)
  - **Pavadinimas** (didėjimo ar mažėjimo tvarka)
  - **Parduotuvės numeris** (didėjimo ar mažėjimo tvarka)
  - **Atsargos** (mažėjimo tvarka)
  - **Užsakyta** (mažėjimo tvarka)
  - **Užsakyta** (mažėjimo tvarka)
- **Filtras** – šis veiksmas leidžia EKA vartotojo peržiūrėti filtruotus duomenis tam tikroje vietoje.
- **Rodyti parduotuvės pasiekiamumą** – šis veiksmas leidžia EKA vartotojui peržiūrėti prieinamus prieinamus atsargų (ATP) kiekius pasirinktoje parduotuvėje.
- **Rodyti parduotuvės vietą** – šiuo veiksmu atidaromas atskiras puslapis, kuriame rodomas pasirinktos parduotuvės žemėlapio rodinys, adresas ir parduotuvės valandos.
- **Paėmimo parduotuvė** - Šis veiksmas sukuria kliento užsakymą, skirtą produkto variantui, kuris bus paimtas iš pasirinktos parduotuvės ir nukreipia vartotoją į operacijos ekraną.
- **Produkto siuntimas** - Šis veiksmas sukuria kliento užsakymą, skirtą produkto variantui, kuris bus siunčiamas iš pasirinktos parduotuvės ir nukreipia vartotoją į operacijos ekraną.
- **Peržiūrėti visus variantus** – jei produktas turi variantų, šis veiksmas perjungiamas iš sąrašo rodinio į matricos rodinį, kuriame rodoma informacija apie visų produkto variantų atsargas.
- **Įtraukti į operaciją** – šiuo veiksmu produktas pridedamas prie krepšelio ir nukreipia vartotoją į operacijos ekraną.

> [!NOTE]
> Vietos rūšiavimo atstumą tarp vietos ir dabartinės parduotuvės lemia „Commerce Headquarters" apibrėžtos koordinatės (platumos ir ilgumos). Informacija apie parduotuvę apibrėžiama pirminiame su parduotuve susieto valdymo vieneto adrese. Ne parduotuvės sandėliui vietos informacija nustatoma sandėlio adrese. Jei dabartinė parduotuvė neturi apibrėžtų koordinačių, pagal vietą nustatyta rūšiavimo pasirinktis sąrašo viršuje rodys dabartinę parduotuvę, o tada surūšiuos kitas vietas pagal pavadinimą.

> [!NOTE]
> **Rodyti parduotuvės pasiekiamumą**, **Rodyti parduotuvės vietą**, **Paėmimas parduotuvėje** ir **Produkto siuntimo** veiksmai nėra prieinami ne parduotuvės vietose.

## <a name="inventory-lookup-matrix-view-for-variants"></a>Variantų atsargų peržvalgos matricos rodinys

Taip pat bendrojo produkto su variantais atsargų peržvalgos operacija taip pat pateikia dimensijomis pagrįstą matricos rodinį, kuriame rodoma informacija apie visų pasirinktos vietos bendrojo produkto variantų atsargas. Pagal numatytąjį matricos rodinį yra rodomi esamos parduotuvės duomenys. Galite naudoti **parduotuvės** veiksmą programos juostoje atsargų informacijai ieškoti kitose parduotuvėse, sukonfigūruotose įvykdymo grupėse, su kurias susieta dabartinė parduotuvė.

Šiame pavyzdyje vaizdas rodo EKA atsargų peržvalgos matricos rodinį.

![Atsargų paieškos operacijos matricos rodinys.](media/inventory-lookup-matrix-view.png)

Matricos rodinyje kiekvienas langelis rodo atskirą variantą, o apatiniame dešiniajame kampe rodo turimų atsargų (faktinių) vertę, o taip pat rezervuoja faktiškai **rezervuotas** ir **užsakytas** (bendro užsakymo) vertes viršutiniame kairiajame kampe. Įvairių turimų verčių reikšmė yra paaiškinta toliau pateiktoje lentelėje.

| Turima vertė                            | Aprašas |
|------------------------------------------|-------------|
| Skaitinė vertė, didesnė už 0 (nulį) | Variantas išleistas pasirinktoje vietoje, langelyje galite atlikti papildomus veiksmus. |
| **0** (nulis)                             | Variantas išleistas pasirinktoje vietoje, bet pasirinktos vietoje šios prekės nėra. Tačiau langelyje Jūs galite atlikti papildomus veiksmus. |
| **netaikoma** arba neaktyvus langelis              | Variantas nebuvo išleistas pasirinktoje vietoje, papildomų veiksmų langelyje atlikti negalite. |

Dimensijų verčių rodymo tvarka matricos rodinyje yra pagrįsta dimensijos rodymo užsakymo konfigūravimu „Commerce Headquarters". Galite keisti dimensijos rodymo užsakymo konfigūraciją pasirinkdami naują naudotimą dimensiją. 

Galimi veiksmai yra prieinami matricos rodymo laukelyje:

- **Parduoti dabar** – šiuo veiksmu pasirenkamas variantas prie krepšelio ir nukreipia vartotoją į operacijos ekraną.
- **Paėmimo parduotuvė** - Šis veiksmas sukuria kliento užsakymą, pasirinktam variantui, kuris bus paimtas iš pasirinktos parduotuvės ir nukreipia vartotoją į operacijos ekraną.
- **Produkto siuntimas** - Šis veiksmas sukuria kliento užsakymą, pasirinktam variantui, kuris bus siunčiamas iš pasirinktos parduotuvės ir nukreipia vartotoją į operacijos ekraną.
- **Pasiekiamumas** – šiuo veiksmu vartotojas pereis į atskirą puslapį, kuriame rodomi pasirinktos parduotuvės pasirinkto varianto ATP kiekiai.
- **Rodyti visas vietas** - is veiksmas perjungia į standartinį atsargų prieinamumo sąrašo rodinį, kuriame rodoma pasirinkto varianto atsargų informacija.
- **Peržiūrėti išsamią produkto informaciją** – šiuo veiksmu vartotojas nukreipiamas į pasirinkto varianto produkto informacijos puslapį (PDP).

## <a name="access-inventory-lookup-from-other-pages-in-pos"></a>Pasiekti atsargų peržvalgą iš kitų EKA puslapių

EKA vartotojai gali pasiekti atsargų peržvalgos operaciją iš kitų EKA puslapių.

Šiame pavyzdyje vaizdas rodo EKA atsargų peržvalgos rezultatai iš PDP.

![Atsargų peržvalga produkto informacijos puslapyje.](media/inventory-lookup-from-product-details-page.png)

Norėdami paleisti atsargų peržvalgos matricos rodinį, kuriame rodoma visų produkto variantų atsargų prieinamumo informacija, galite naudoti bendrojo produkto PDP veiksmą **Peržiūrėti visus variantus**. Kiekvienam produktui PDP rodo dabartinės parduotuvės turimų atsargų (turimas faktines) vertę. Be to, galite pasirinkti **kitų parduotuvių atsargų** saitą, kad paleisite atsargų peržvalgos operaciją, norėdami patikrinti produkto atsargų prieinamumą kitose parduotuvėse ar sandėliuose.

> [!NOTE]
> Mygtuką **Peržiūrėti visus variantus** veiksmą PDP galima naudoti tik tame pagrindinių produktų elemente, kuriuose yra produkto variantų. Jo nėra konkrečiuose produktuose ar rinkiniuose.

Galima konfigūruoti atsargų peržvalgos operaciją, kuri EKA operacijos ekrane rodoma kaip saitas mygtukyno puslapyje. Po konfigūravimo, kai vartotojas pasirenka krepšelio eilutę ir tada pasirenka **atsargų peržvalgos** mygtuką, bus rodomas pasirinkto produkto atsargų peržvalgos sąrašo rodinys. Daugiau informacijos apie mygtukyno konfigūravimą naudojant EKA ekrano maketo dizainerio įrankį ieškokite [EKA vartotojo sąsajos vaizdo konfigūracijose](pos-screen-layouts.md).

## <a name="inventory-lookup-with-channel-side-calculation"></a>Atsargų peržvalga naudojant kanalo skaičiavimą

Naudojant „Commerce release 10.0.9" ir anksčiau, galima faktinė atsargų peržvalgos operacijos **vertė nuskaitoma** iš „Commerce Headquarters" per realaus laiko paslaugų iškvietimą. „Commerce“ release 10.0.10 ir vėliau galite konfigūruoti EKA atsargų peržvalgos operaciją, kad būtų naudojamas kanalo skaičiavimas „Commerce“ serveryje galimai faktinei vertei nustatyti, o tai gali suteikti tikslesnį ir tikslesnį turimų atsargų įvertinimą, faktoringu operacijų duomenyse, kurie dar nesinchronizuojami su būstiniu. Daugiau informacijos apie kanalo atsargų skaičiavimą ir susijusią EKA konfigūraciją būstinėje ieškokite [mažmeninės prekybos kanalų atsargų prieinamumo skaičiavimas](calculated-inventory-retail-channels.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[EKA vartotojo sąsajos vaizdinio elemento konfigūracijos](pos-screen-layouts.md)

[Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](calculated-inventory-retail-channels.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
