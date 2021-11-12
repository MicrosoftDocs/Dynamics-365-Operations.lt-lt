---
title: Ieškokite rezultatų modulio
description: Šioje temoje aprašomi paieškos rezultatų moduliai ir aprašoma, kaip juos įtraukti į saito puslapius „Microsoft Dynamics 365 Commerce“.
author: anupamar-ms
ms.date: 10/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: dc4a01e520379a74ca3b21c1d588531412e762be
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647517"
---
# <a name="search-results-module"></a>Ieškos rezultatų modulis

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šioje temoje aprašomi paieškos rezultatų moduliai ir aprašoma, kaip juos įtraukti į saito puslapius „Microsoft Dynamics 365 Commerce“.

Paieškos rezultatų modulis grąžina produkto paieškos rezultatus ir taikomų perdirbimo įrankių sąrašą produktams. Paieškos rezultatų moduliai „Dynamics 365 Commerce“ saituose gali būti naudojami siekiant apimti puslapius šiais scenarijais:

- Paieškos rezultatai, kuriuos pradėjo vartotojo paieška
- Paieškos rezultatai, kurie rodo konkretų produktų rinkinį, tokį kaip „Į parduotuvę panašios paieškos“
- Produktų, priklausančių kategorijai, sąrašai

Daugiau informacijos apie kategoriją ir paieškos rezultatų puslapius rasite [Numatytos kategorijos užsklandos puslapis ir paieškos rezultatų puslapio apžvalga](category-search-page-overview.md).

Tolesnis paveikslėlis rodo paieškos rezultatų puslapio pavyzdį kategorijai „Fabrikam“ saite.

![Paieškos rezultatų puslapio pavyzdys „Fabrikam“ svetainėje.](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a>Paieškos rezultatų modulio ypatybės

Tolesnėje lentelėje išvardytos paieškos rezultato modulių ypatybės kartu su jų vertėmis ir aprašais.

| Ypatybė | Reikšmės | aprašymas |
|----------|--------|-------------|
| Prekių skaičius viename puslapyje | Sveikasis skaičius | Prekių skaičius, kuris turi būti rodomas kiekviename puslapyje. |
| Leisti atgal į PDP | **Teisinga** arba **Klaidinga** | Jei ši ypatybė nustatyta į **Teisinga**, kai vartotojas pasirenka produktą paieškos rezultatų puslapyje, atvertas džiūvėsėlio naršymas produkto išsamios informacijos puslapyje (PDP) rodys „Grįžti į rezultatus“ nuorodą. |
| Išplėsti tikslinimo meniu | **Visi**, **1**, **2**, **3** ar **4** | Pagrindinių apdirbėjų skaičius, kuris turi būti išplečiamas užkrovus puslapį. Pavyzdžiui, jei ši ypatybė yra nustatyta į **3**, pirmieji trys apdirbėjai puslapyje bus išplėsti. |
| Slėpti kategorijų hierarchijos rodymą | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatyta į **Teisinga**, kategorijos hierarchija rodoma puslapyje bus paslėpta. Ši ypatybė turi būti nustatyta į **Teisingą** jei naudojate [džiūvėsėlio modulį](add-breadcrumb.md) tam, kad jis parodytų kategorijos hierarchiją.|
| Į paieškos rezultatus įtraukite produkto atributus | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatyta į **Teisinga**, atributai bus grąžinami produktams paieškos rezultatuose. Nepaisant to, kad šie atributai gali būti rodomi „Commerce“ saite, būtinas plėtinys.|
| Rodyti priskyrimo kainas | **Teisinga** arba **Klaidinga** | Jei ši ypatybė yra nustatyta į **Teisinga**, prisijungimo kainos produktams bus rodomos paieškos rezultatuose, kai prisijungęs vartotojas naršo puslapyje. |
| Tikslinimo skydo naujinimas | **Teisinga** arba **Klaidinga** | Jei ši ypatybė nustatyta kaip **Teisinga**, tikslinimo skydas bus atnaujintas pasirinkus tikslinimo priemones. Šiuo režimu kai kurios kelių pasirinkimų tikslinimo priemonės elgsis kaip vieno pasirinkimo tikslinimo priemonės, atnaujinus tikslinimo skydą. |

> [!IMPORTANT]
> „Commerce” 10.0.16 versijos leidime ir vėlesniuose konfigūracija **Rodyti priskyrimo kainas** galima naudoti norint rodyti priskyrimo kainas puslapyje.
>
> „Commerce” 10.0.20 versijos leidime ir vėlesniuose konfigūraciją **Naujinti tikslinimo skydą** galima naudoti norint atnaujinti tikslinimo skydą tikslinimo priemonės pasirinkimo metu.

## <a name="supported-modules"></a>Palaikomi moduliai

Paieškos rezultatų modulis palaiko [greito rodinio modulį](quick-view-module.md), kuris leidžia vartotojams peržiūrėti produkto informaciją ir įtraukti prekes į vežimėlį iš paieškos rezultatų puslapio.

## <a name="add-a-search-results-module-to-a-category-page"></a>Įtraukite paieškos rezultatų modulį į kategorijų puslapį

Norėdami įtraukti paieškos rezultatų modulį į kategorijų puslapį, atlikite šiuos žingsnius.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Teksto laukelyje **Naujas šablonas** įveskite pavadinimą **Paieškos rezultatai** ir tada rinkitės **Gerai**.
1. Vietoje **tekstas** pasirinkite daugtaškį (...), ir tada rinkitės **Įtraukite modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Numatytasis puslapis**, tada pasirinkite **Gerai**.
1. Vietoje **Pagrindinis** modulyje **Numatytas puslapis** rinkitės daugtaškį (...) ir tada rinkitės **Įtraukite modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Konteineris**, tada pasirinkite **Gerai**.
1. Vietoje **Talpykla** pasirinkite daugtaškį (...), ir tada rinkitės **Įtraukite modulį**.
1. Dialogo lange **Įtraukti modulį** pasirinkite modulį **Naršymo kelias**, tada pasirinkite **Gerai**.
1. Ypatybių juostoje **Džiūvėsėlis** įveskite vertę **1** skirtą **Minimaliems atsitikimams**.
1. Vietoje **Talpykla** pasirinkite daugtaškį (...), o tada pasirinkite **Įtraukite modulį**.
1. Teksto laukelyje **Įtraukti modulį** pasirinkite **Paieškos rezultatai** modulį, o tada pasirinkite **Gerai**.
1. Ypatybių juostoje **Paieškos rezultatai** įveskite vertę **1** skirtą **Minimalūs atsitikimai** ir tuomet nustatykite visas kitas reikiamas ypatybes paieškos rezultatų moduliui. Nustatydami šias ypatybes šablone užtikrinate, kad bet kokie tinkinimai konkrečios kategorijos puslapyje automatiškai apims šiuos nustatymus.
1. Pasirinkite **Baigti redagavimą**, o tada pasirinkite **Publikuoti**, kad publikuotumėte šabloną.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Teksto laukelyje **Rinkitės šabloną** pasirinkite **Paieškos rezultatai** sukurtą šabloną, įveskite **Kategorijos puslapis** skirtą **Puslapio pavadinimas** ir tada rinkitės **Gerai**. Kadangi visos vertės yra nustatytos šablone, puslapis yra parengtas publikuoti.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Įgalinkite atsargų supratimą ieškos rezultatų moduliui

Klientai paprastai tikisi, kad el. prekybos svetainė naršymo metu turės informacijos apie atsargas, kad galėtų nuspręsti, ką daryti, jei nėra produkto atsargų. Ieškos rezultatų modulį galima pagerinti, kad jame būtų atsargų duomenys ir būtų pateikta tokia patirtis:

- Rodoma atsargų prieinamumo žymė kartu su produktais.
- Būtų slepiami prekyboje neturimi produktai.
- Pardavime neturimi produktai būtų rodomi ieškos rezultatų sąrašo pabaigoje.
    
Norėdami įgalinti šią patirtį, Prekybos Centre turite sukonfigūruoti šiuos būtinuosius parametrus.

### <a name="enable-the-enhanced-e-commerce-product-discovery-to-be-inventory-aware-feature"></a>Įgalinkite patobulintą el. prekybos produktų aptikimą, kad būtų galima žinoti apie atsargas

> [!NOTE]
> **Patobulintas el. prekybos produktų aptikimas, kad būtų žinoma apie atsargas** funkcija, galima Prekybos versijos 10.0.20 leidime.

Norėdami įgalinti **Patobulinto el. prekybos produktų aptikimo funkciją, kad būtų žinoma apie atsargas** funkciją Prekybos Centruose, atlikite šiuos veiksmus.

1. Eikite į **Darbo sritys \> Funkcijų valdymas**.
1. Ieškokite **Patobulinto el. prekybos produktų aptikimą, kad būtų galima žinoti apie atsargas** funkcijos ir tada ją įgalinkite.

### <a name="configure-the-populate-product-attributes-with-inventory-level-job"></a>Konfigūruokite Užpildyto produkto atributus su atsargų lygo užduotimi

**Užpildyto produkto atributai su atsargų lygiu** užduotis sukuria naują produkto atributą, kad būtų galima fiksuoti atsargas, ir tada nustato tą atributą į kiekvieno bendrojo produkto vėliausią atsargų lygio vertę. Kadangi parduodamo produkto ar asortimento atsargų prieinamumas pasikeičia, primygtinai rekomenduojame suplanuoti užduotį kaip paketinį procesą.

Norėdami sukonfigūruoti **Užpildyto produkto atributus su atsargų lygio** užduotimi Prekybos Centruose, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Prekyba ir prekybos IT \> Produktai ir atsargos**.
1. Pasirinkite **Užpildyti produkto atributus su atsargų lygiu**.
1. **Užpildyti produkto atributus su atsargų lygiu** dialogo lange atlikite šiuos veiksmus:

    1. **Parameterai**, **Produkto atributas ir tipo pavadinimas** lauke nurodykite paskirto produkto atributo, kuris bus sukurtas norint fiksuoti atsargas, pavadinimą.
    1. **Parametrai**, **Atsargų prieinamumas, remiantis** lauke pasirinkite kiekį, pagal kurį turėtų būti skaičiuojamas atsargų lygis (pvz. **Fiziškai prieinamos**).
    1. Dalyje **Vykdyti fone** sukonfigūruokite užduotį, kad ji būtų vykdoma fone ir pasirinktinai įjunkite **Paketinio vykdymo** parinktį. 

> [!NOTE]
> Norėdami nuosekliai apskaičiuoti atsargų lygį PDPs ir produktų sąrašo puslapiuose jūsų el. prekybos svetainėje, būtinai pasirinkite tą pačią kiekio parinktį **Atsargų pasiekiamumas, remiantis** parametrui Prekybos Centruose ir **Atsargų lygis, remiantis** nustatymui Prekybos svetainės generatoriui. Norėdami gauti daugiau informacijos apie atsargų parametrų taikymą svetainės kurime, žr. [Atsargų nustatymų taikymas](inventory-settings.md).

### <a name="configure-the-new-product-attribute"></a>Konfigūruokite naują produkto atributą

Po to, kai paleidžiama **Užpildyti produkto atributus su atsargų lygiu** užduotis, turite sukonfigūruoti naujai sukurtą produkto atributą el. prekybos svetainėje, kurioje norite įgalinti atsargų supratimą apie ieškos rezultatų modulį.

Norėdami konfigūruoti naują produkto atributą Prekybos Centruose, atlikite šiuos žingsnius.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalo sąranka \> Kanalo kategorijos ir produkto atributai** ir pasirinkite el. prekybos svetainę.
1. Pasirinkite ir atidarykite susijusią atributų grupę, įtraukite į ją naujai sukurtą produkto atributą, tada uždarykite puslapį.
1. Pasirinkite **Nustatyti atributo metaduomenis**, pasirinkite naujai pridėtą produkto atributą, tada įjunkite **Rodyti atributą kanale**, **Nuskaitomas**, **Galima patikslinti** ir **Galima užklausti** parinktis.

> [!NOTE]
> Produktų, kurie rodomi paieškos rezultatų modulyje, atsargų lygis įvedamas bendrojo produkto lygyje, o ne atskirų variantų lygyje. Jis turi tik dvi galimas vertes: "Turima" ir "Atsargų nėra". Faktinis verčių tekstas yra nuskaitomas iš [atsargų lygio profilio](inventory-buffers-levels.md) apibrėžimo. Bendrasis produktas laikomas atsargose tik tada, kai visų jo variantų nėra atsargose. Varianto atsargų lygis nustatomas remiantis produkto atsargų lygio profilio apibrėžimu. 

Atlikus visus ankstesnius konfigūravimo veiksmus, ieškos rezultatų puslapiuose esantys tikslinimo priemonės rodys atsargomis pagrįstus filtrus, o ieškos rezultatų modulis pateiks atsargų duomenis po užsakymo. Tada "Commerce" svetainės generatoriuje galite konfigūruoti **Produktų sąrašo puslapių atsargų** parametrus kad būtų galima valdyti, kaip ieškos rezultatų modulis rodo ne turimų atsargų produktus. Daugiau informacijos žr. [Atsargų parametrų taikymas](inventory-settings.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga](category-search-page-overview.md)

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Greito rodinio modulis](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
