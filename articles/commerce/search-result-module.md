---
title: Ieškos rezultatų modulis
description: Šiame straipsnyje aprašomi ieškos rezultatų moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: d026de098ec182e3f7631c1c19e54b3b36db341f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886963"
---
# <a name="search-results-module"></a>Ieškos rezultatų modulis

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šiame straipsnyje aprašomi ieškos rezultatų moduliai ir aprašoma, kaip įtraukti juos į svetainės puslapius Microsoft Dynamics 365 Commerce.

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

Norėdami įtraukti ieškos rezultatų modulį į svetainės generatoriaus kategorijos puslapį, atlikite šiuos veiksmus.

1. Eikite į **Šablonai** ir pasirinkite **Naujas**, kad sukurtumėte naują šabloną.
1. Teksto laukelyje **Naujas šablonas** įveskite pavadinimą **Paieškos rezultatai** ir tada rinkitės **Gerai**.
1. Teksto atminties **atminties** atminties lape pasirinkite daugtaškį (...), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite modulį **Numatytasis** puslapis, tada pasirinkite **Gerai**.
1. Modulyje **Numatytasis** puslapis esantis **pagrindiniame atminties** atminties lape pasirinkite daugtaškį (...), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (...), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite modulį **Naršymo nuoroda ir** pasirinkite **Gerai**.
1. Ypatybių juostoje **Džiūvėsėlis** įveskite vertę **1** skirtą **Minimaliems atsitikimams**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (...), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite ieškos **rezultatų modulį**, tada pasirinkite **Gerai**.
1. Ypatybių juostoje **Paieškos rezultatai** įveskite vertę **1** skirtą **Minimalūs atsitikimai** ir tuomet nustatykite visas kitas reikiamas ypatybes paieškos rezultatų moduliui. Nustatydami šias ypatybes šablone užtikrinate, kad bet kokie tinkinimai konkrečios kategorijos puslapyje automatiškai apims šiuos nustatymus.
1. Pasirinkite **Baigti redagavimą**, o tada pasirinkite **Publikuoti**, kad publikuotumėte šabloną.
1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Kurti naują puslapį**, po Puslapio **pavadinimas** įveskite Kategorijos **puslapį** ir pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti šabloną** pasirinkite **Ieškos rezultatų šabloną**, kurį sukūrėte, tada pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti maketą** pasirinkite puslapio maketą (pvz., Lankstusis **maketas**) ir pasirinkite **Pirmyn**.
1. Dalyje **Peržiūrėti ir baigti** peržiūrėkite puslapio konfigūraciją. Jei reikia redaguoti puslapio informaciją, pasirinkite **Atgal**. Jei puslapio informacija teisinga, pasirinkite Kurti **puslapį**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="enable-inventory-awareness-for-the-search-results-module"></a>Įgalinkite atsargų supratimą ieškos rezultatų moduliui

Klientai paprastai tikisi, kad el. komercijos svetainė bus žinoma apie atsargas naršymo metu, kad galėtų nuspręsti, ką daryti, jei nėra produkto atsargų. Ieškos rezultatų modulis gali būti sukonfigūruotas įtraukti atsargų duomenis ir suteikti tokią patirtį:

- Rodyti atsargų prieinamumo žymę kartu su produktu.
- Slėpti ne atsargose produktus iš produktų sąrašo.
- Rodyti produktus, kurie nėra atsargose, produktų sąrašo pabaigoje.
- Filtruoti ieškos rezultatų produktus pagal atsargų lygį.

Norėdami įgalinti šią patirtį, pirmiausia turite **įgalinti patobulintą el. komercijos** produktų aptikimo funkciją, kad ji būtų žinoma apie atsargas funkcijų **valdymo darbo** srityje.

> [!NOTE]
> Išplėstinio **el. komercijos** produktų aptikimo, kuris turi informacijos apie atsargas, funkciją galima naudoti "Commerce" 10.0.20 versijoje ir vėliau.

Atsargų produktų paieška naudoja produkto atributus atsargų prieinamumo informacijai gauti. Kad ši funkcija būtų būtina, turi būti sukurti skirti produkto atributai, į juos turi būti įvesti atsargų duomenys ir jie turi būti įtraukti į interneto kanalą. 

Norėdami sukurti skirtus produkto atributus, kad būtų galima palaikyti atsargų žinomos ieškos rezultatų modulį, atlikite šiuos veiksmus.

1. Būstinę eikite į " **Retail" ir "Commerce \> Retail" ir "Commerce IT \> Products" ir atsargas**.
1. Pasirinkite ir atidarykite **automatiškai įvesti produkto atributus atsargų lygiu**.
1. Dialogo lange įveskite šią informaciją:

    1. Lauke Produkto **atributas ir tipo pavadinimas** nurodykite paskirto produkto atributo, kuris bus sukurtas atsargų duomenims fiksuoti, pavadinimą.
    1. Lauke Atsargų **prieinamumas pagal lauką** pasirinkite kiekio tipą, pagal kurį turėtų būti skaičiuojamas atsargų lygis (pvz., **Faktiškai turima**). 

1. Vykdyti užduotį fone. Dėl to, kad produktų atsargų pakeitimai vyksta klientų aplinkoje, primygtinai rekomenduojame suplanuoti šią užduotį kaip paketinį procesą.

> [!NOTE]
> Norėdami nuosekliai apskaičiuoti atsargų lygį jūsų el. komercijos svetainėje visuose puslapiuose ir moduliuose, **nepamirškite** pasirinkti to paties kiekio tipo pagal "Commerce **Headquarters**" parametrą ir atsargų lygį, pagrįstą "Commerce Site Builder" nustatymu. Norėdami gauti daugiau informacijos apie atsargų parametrų taikymą svetainės kurime, žr. [Atsargų nustatymų taikymas](inventory-settings.md).

Norėdami konfigūruoti interneto kanalo produkto atributus, atlikite šiuos veiksmus. 

1. Būstinėje eikite į "Retail" **ir "Commerce Channel" \> nustatymo kanalo \> kategorijas ir produktų atributus**.
1. Pasirinkite interneto kanalą, norėdami įgalinti žinotų atsargų ieškos rezultatų modulį.
1. Pasirinkite ir atidarykite susietą atributų grupę, tada prie jos pridėkite naujai sukurtą produkto atributą.
1. Jei "Commerce" versijos yra prieš 10.0.27 leidimą, **pasirinkite Nustatyti atributo metaduomenis**, pasirinkite naujai pridėtą produkto atributą, **tada** įjunkite atributą Rodyti kanale, **·** **·** **Galima** patikslinti ir užklausti parinktis.
1. Eikite į **"Retail" ir "Commerce \> Retail" ir "Commerce IT \> Distribution**" grafiką ir vykdykite **užduotį 1150 (Katalogas**). Jei suplanuojate **produkto** atributų su atsargų lygio užduotimi kaip paketinį procesą, rekomenduojame taip pat suplanuoti 1150 užduotį kaip paketinį procesą, kuris vykdomas tuo pačiu dažnumu.

> [!NOTE]
> Produktų, kurie rodomi paieškos rezultatų modulyje, atsargų lygis rodomas bendrojo produkto lygyje, o ne atskirų variantų lygyje. Jis turi tik dvi galimas vertes: "Turima" ir "Atsargų nėra". Faktinė vertės žymė nuskaitoma iš atsargų lygio [šablono apibrėžimo](inventory-buffers-levels.md). Bendrasis produktas laikomas atsargose tik tada, kai visų jo variantų nėra atsargose.

Atlikus visus ankstesnius konfigūravimo veiksmus, ieškos rezultatų puslapiuose esantys tikslinimo priemonės rodys atsargomis pagrįstus filtrus, o ieškos rezultatų modulis pateiks atsargų duomenis po užsakymo. Tada "Commerce" svetainės generatoriuje galite konfigūruoti **Produktų sąrašo puslapių atsargų** parametrus kad būtų galima valdyti, kaip ieškos rezultatų modulis rodo ne turimų atsargų produktus. Daugiau informacijos žr. [Atsargų parametrų taikymas](inventory-settings.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[Numatytojo kategorijos nukreipimo puslapio ir ieškos rezultatų puslapio apžvalga](category-search-page-overview.md)

[Modulių bibliotekos peržiūra](starter-kit-overview.md)

[Greito rodinio modulis](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
