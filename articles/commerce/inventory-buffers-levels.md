---
title: Atsargų buferių ir atsargų lygių konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip konfigūruoti atsargų buferius ir atsargų lygius, kurie nustato atsargų prieinamumo pranešimus svetainėse Microsoft Dynamics 365 Commerce.
author: boycezhu
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 5f882debd09a7076a52606f7ca3aca97d9ec8afe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269198"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a>Atsargų buferių ir atsargų lygių konfigūravimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip konfigūruoti atsargų buferius ir atsargų lygius, kurie apibrėžia pranešimus apie atsargų prieinamumą svetainėse Microsoft Dynamics 365 Commerce.

„Dynamics 365 Commerce“ būstinėje saugomi atsargų duomenys ir įvairūs kanalai, pvz., elektroninis kasos aparatas (EKA), el. prekybos vitrinos ir kitos pasirinktinės integruotos programos, kurios asinchroniškai nuskaito ir įveda atsargų informaciją. Dėl to pasiekiamų atsargų reikšmės, gaunamos iš „Commerce“ būstinės turimų atsargų puslapio, naudojant EKA vartotojo sąsają (UI) ir el. prekybos atsargų pasiekiamumo API, ne visada pasiekiamos realiuoju laiku.

Vietoje to, kad el. prekybos vitrinose būtų rodomos faktinės atsargų reikšmės, dauguma mažmenininkų nori rodyti tik pranešimus apie atsargų pasiekiamumo būseną (pvz., „Yra“ arba „Nėra atsargų“), kad informuotų klientus, ar prekę galima įsigyti, ar jos atsargos išseko. Šiuo tikslu reikia įjungti ir sukonfigūruoti atsargų buferius ir atsargų lygius, kurie apibrėžia atsargų pasiekiamumo pranešimus.

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a>Būtina sąlyga: įjunkite atsargų buferius ir atsargų lygių funkciją

Atsargų buferio ir atsargų lygių funkcija kontroliuojama naudojant „Commerce“ būstinės funkcijų valdymą. Norėdami įjungti šią funkciją, atlikite toliau nurodytus veiksmus.

1. Eikite į **Sistemos administravimas** \> **Darbo sritys** \> **Funkcijų valdymas**.
1. Susiraskite funkciją **Įjungti atsargų buferius ir atsargų lygius**, pasirinkite jos eilutę, tada pasirinkite **Įjungti dabar**.

Įjungę funkciją, galite rasti atsargų lygius **„Retail“ ir „Commerce“ \> Atsargų valdymas**.

## <a name="create-and-configure-an-inventory-level-profile"></a>Atsargų lygio profilio kūrimas

*Atsargų lygio profilis* nurodo, ar nurodyta produkto kiekio būsena laikoma kaip „yra atsargų“, „nėra atsargų“ ar kita pasirinktine būsena. Galite kurti ir konfigūruoti kelis kiekvieno juridinio subjekto atsargų lygio profilius. Kiekvienas profilis susideda iš atsargų lygių rinkinio, o kiekvienas lygis apibrėžiamas pagal *diapazoną*, *kodą* ir *etiketę*.

- **Diapazonas** – kiekvienas diapazonas apibrėžiamas nuo *pradžios kiekio* ir *pabaigos kiekio*. Kiekio reikšmė patenka į diapazoną, jei ji yra didesnė nei šio diapazono pradžios kiekis ir ne didesnė nei pabaigos kiekis.
- **Kodas** – kodas yra vidinė santrumpa, nurodanti lygį. Tiesiogiai į atsargų API integruoti klientai gali naudoti kodus, norėdami sukurti papildomą konkretaus atsargų lygio logiką. Pavyzdžiui, jie gali išjungti produkto įsigijimo galimybę, kai jo atsargų lygio kodas yra **OOS** („nebėra atsargų“).
- **Etiketė** – etiketė yra reikšmingas klientu skirtas pranešimas, kuris nurodo atsargų lygį klientams el. prekybos svetainėje.

### <a name="create-an-inventory-level-profile"></a>Atsargų lygio profilio kūrimas

Norėdami sukurti atsargų lygio profilį, atlikite tolesnius veiksmus.

1. Eikite į **„Retail“ ir „Commerce“** \> **Atsargų valdymas** \> **Atsargų lygiai**.
1. Veiksmų srityje pasirinkite **Naujas**, tada įveskite reikšmes laukuose **Profilio ID** ir **Aprašas**.
1. „FastTab“ skirtuke **Diapazonai** pasirinkite **Įtraukti**, kad įtrauktumėte naują lygį, ir įveskite reikšmes lygio stulpeliuose **Pradžios kiekis**, **Pabaigos kiekis**, **Kodas** ir **Etiketė**. Pakartokite šį veiksmą, kad įtrauktumėte daugiau lygių. Jei reikia, galite redaguoti reikšmes duomenų tinklelyje arba galite pasirinkti **Naikinti**, kad pašalintumėte lygį.
1. Veiksmų srityje pasirinkite **Įrašyti**.

Sukūrus naują profilį, automatiškai inicijuojami du atsargų lygiai:

- **OOS** – lygis „nėra atsargų“, kurio apatinė diapazono riba yra neigiama begalybė. Šio lygio pradžios kiekio ir kodo redaguoti negalima.
- **AVAIL** – lygis „yra“, kurio viršutinė diapazono riba yra begalybė. Šio lygio pabaigos kiekio ir kodo redaguoti negalima.

> [!NOTE]
> Profilio apibrėžime negali būti tarpų ar diapazonų persidengimo.

Norėdami sukonfigūruoti lokalizuotas etikečių pranešimo eilutes, galite naudoti veiksmų srities mygtuką **Vertimai**. Tada reikia paleisti paskirstymo grafiko užduotį **1110** (**Visuotinė konfigūracija**), kad sinchronizuotumėte lokalizuotas eilutes su kanalais.

### <a name="configure-an-inventory-level-profile"></a>Atsargų lygio profilio konfigūravimas

Galite konfigūruoti atsargų lygio profilį arba produkto kategorijos lygį, arba atskirą produkto lygį. Kai produkto atsargų lygio profilis sukonfigūruojamas, atsargų lygis nustatomas pagal diapazonus, kurie nurodyti susietame profilyje. Kitu atveju atsargų lygis „yra“ arba „nėra“ nustatomas pagal tai, ar produkto kiekis teigiamas.

Norėdami konfigūruoti kategorijos atsargų lygio profilį, atlikite tolesnius veiksmus.

1. Eikite į **„Retail“ ir „Commerce“** \> **Produktai ir kategorijos** \> **Prekybos produktų hierarchija**.
1. Norėdami konfigūruoti kategorijos atsargų lygio profilį, pasirinkite kategoriją.
1. „FastTab“ skirtuke **Parduodamo produkto ypatybės**, pasirinkite juridinį subjektą.
1. Dalies **„Commerce“ atsargos** lauke **Atsargų lygio profilis** pasirinkite vieną iš iš anksto nustatytų atsargų lygio profilių.

Norėdami išplatinti kategorijos lygio profilio reikšmes žemesnės kategorijos produktams, galite naudoti veiksmų srities mygtuką **Atnaujinti produktus**. Daugiau informacijos žr. [Produktų kategorijų ir produktų valdymas](category-management-product-creation.md).

Norėdami konfigūruoti išleisto produkto atsargų lygio profilį, atlikite tolesnius veiksmus.

1. Eikite į **„Retail“ ir „Commerce“** \> **Produktai ir kategorijos** \> **Patvirtinti produktai pagal kategoriją**.
1. Pasirinkite produktą ir tada atidarykite savo produkto informacijos puslapį.
1. „FastTab“ skirtuko **Parduoti** dalies **„Commerce“ atsargos** lauke **Atsargų lygio profilis** pasirinkite vieną iš iš anksto nustatytų atsargų lygio profilių.

Kai sukuriamas naujas produktas, laukas **Atsargų lygio profilis** kaip ir daugelis kitų produkto lygio atributų, bus nustatytas į reikšmę, sukonfigūruotą kategorijai, su kuria susietas produktas.

> [!NOTE]
> Atsargų lygio profilis yra juridinis subjektas – konkretus atributas. Tos pačios kategorijos ar produkto atsargų lygio profilio vertė gali skirtis, atsižvelgiant į teisinius subjektus.

Norėdami sinchronizuoti atsargų lygio profilių konfigūracijas su kanalais, atlikite tolesnius veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba** \> **Mažmeninės prekybos ir prekybos IT“** \> **Paskirstymo grafikas**.
1. Paleiskite paskirstymo grafiką **1040** (**Produktas**).

## <a name="configure-an-inventory-buffer"></a>Atsargų buferio konfigūravimas

*Atsargų buferis* yra vartotojo nustatyta reikšmė, kuri atima papildomą prekės kiekį iš pradinio kiekio, kad apskaičiuotų įvertintą kiekį. Šis įvertintas kiekis suteikia mažmenininkams saugų buferį, kad jis neparduotų daugiau produkto, nei turimos faktinės atsargos. Galite konfigūruoti atsargų buferį arba produkto kategorijos lygį, arba atskirą produkto lygį. Jeigu atsargų buferis nenurodytas, naudojama numatytoji reikšmė **0** (nulis).

Norėdami konfigūruoti kategorijos atsargų buferį, atlikite tolesnius veiksmus.

1. Eikite į **„Retail“ ir „Commerce“** \> **Produktai ir kategorijos** \> **Prekybos produktų hierarchija**.
1. Norėdami konfigūruoti kategorijos atsargų buferį, pasirinkite kategoriją.
1. „FastTab“ skirtuke **Parduodamo produkto ypatybės**, pasirinkite juridinį subjektą.
1. Dalies **„Commerce“ atsargos** lauke **Atsargų buferis** įveskite teigiamą reikšmę.

Norėdami išplatinti kategorijos lygio buferio reikšmes žemesnės kategorijos produktams, galite naudoti veiksmų srities mygtuką **Atnaujinti produktus**. Daugiau informacijos žr. [Produktų kategorijų ir produktų valdymas](category-management-product-creation.md).

Norėdami konfigūruoti išleistų produktų atsargų buferį, atlikite tolesnius veiksmus.

1. Eikite į **„Retail“ ir „Commerce“** \> **Produktai ir kategorijos** \> **Patvirtinti produktai pagal kategoriją**.
1. Pasirinkite produktą ir tada atidarykite savo produkto informacijos puslapį.
1. „FastTab“ skirtuko **Parduoti** dalies **„Commerce“ atsargos** lauke **Atsargų buferis** įveskite teigiamą reikšmę.

Kai sukuriamas naujas produktas, laukas **Atsargų buferis** bus nustatytas į reikšmę, sukonfigūruotą kategorijai, su kuria susietas produktas.

> [!NOTE]
> Jei sukonfigūruosite atsargų buferį ir atsargų lygio profilius produktui, įvertintas produkto kiekis (t. y. pradinis kiekis, atėmus buferio vertę), bus naudojamas diapazonui skaičiuoti, siekiant nustatyti atsargų lygį.

Norėdami sinchronizuoti atsargų buferių konfigūracijas su kanalais, atlikite tolesnius veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba** \> **Mažmeninės prekybos ir prekybos IT** \> **Paskirstymo grafikas**.
1. Paleiskite paskirstymo grafiką **1040** (**Produktas**).

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a>Atsargų buferių ir atsargų lygių naudojimas el. prekybos scenarijuje

„Commerce“ svetainės kūrimo priemonė naudoja atsargų buferio ir atsargų lygio galimybes „Commerce“ būstinėje, kad galėtų nustatyti atsargų pasiekiamumo pranešimus el. prekybos svetainėse. Daugiau informacijos žr. [Atsargų parametrų taikymas](inventory-settings.md).

Taip pat, jei integruosite trečiosios šalies el. prekybos sprendimą, galite naudoti API **„GetEstimatedAvailability“** ir **„GetEstimatedProductWarehouseAvailability“**, kad produkto atsargų pasiekiamumas būtų rodomas jūsų el. prekybos scenarijuje. Norėdami gauti daugiau informacijos apie šias API, žr. [Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](calculated-inventory-retail-channels.md).

Atsargų buferio ir atsargų lygių įvedimas suteikia šioms API galimybę pateikti atsargų lygio kodus ir etikečių pranešimus, kurie nustatomi atsižvelgiant į iš viso pasiekiamų ir fiziškai pasiekiamų atsargų reikšmes. API gali būti sukonfigūruota taip, kad būtų galima nustatyti, ar atsargų kiekis pateikiamas kartu su pranešimu, ar galimas kiekis sumažinamas atsargų buferio reikšme.

Norėdami sukonfigūruoti produkto pasiekiamumo API atsakymą, atlikite tolesnius veiksmus.

1. Eikite į **„Retail“ ir „Commerce“** \> **Būstinės sąranka** \> **Parametrai** \> **Prekybos parametrai**.
1. Pasirinkite reikšmę skirtuko **Atsargos** dalies **Parduotuvės atsargos** lauke **Produkto pasiekiamumo API el. prekybai**.
1. Norėdami pritaikyti parametrus kanalams, vykdykite paskirstymo grafiko užduotį **1110** (**Visuotinė konfigūracija**).

## <a name="additional-resources"></a>Papildomi ištekliai

[Produktų kategorijų ir produktų valdymas](category-management-product-creation.md)

[Atsargų parametrų taikymas](inventory-settings.md)

[Mažmeninės prekybos kanalų atsargų pasiekiamumo apskaičiavimas](calculated-inventory-retail-channels.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
