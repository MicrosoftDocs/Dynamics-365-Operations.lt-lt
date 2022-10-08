---
title: Produktų palyginimo moduliai
description: Šiame straipsnyje aprašomi produktų palyginimo moduliai ir nurodoma, kaip juos įdiegti, kad klientai galėtų atlikti produktų palyginimus el. komercijos Microsoft Dynamics 365 Commerce žiniatinklio svetainėse.
author: ashishmsft
ms.date: 10/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 9ff45f3fbcc86b21f336d580582adef586417de4
ms.sourcegitcommit: 66b954827826706ea2ba00c2afd5d694ad92148d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/03/2022
ms.locfileid: "9618391"
---
# <a name="product-comparison-modules"></a>Produktų palyginimo moduliai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašomi produktų palyginimo moduliai ir nurodoma, kaip juos įdiegti, kad klientai galėtų atlikti produktų palyginimus el. komercijos Microsoft Dynamics 365 Commerce žiniatinklio svetainėse.

> [!NOTE]
> Produktų palyginimo ir produktų palyginimo mygtukų moduliai galimi Dynamics 365 Commerce versijos 10.0.29 leidime. Juos galima naudoti ir "verslas vartotojui" (B2C) ir "verslas verslui" (B2B) žiniatinklio svetainėse.

Produktų palyginimo funkcijos leidžia pardavėjams palyginti išsamią produktų informaciją produktų palyginimo puslapyje, kad būtų lengviau priimti sprendimus dėl pirkimo. Ši funkcija konfigūruota "Commerce" svetainės generatoriuje naudojant produktų palyginimo modulį. Produktų sąrašo puslapiuose (PLPs), pvz., kategorijos rezultatuose, paieškos rezultatuose ir produktų rinkinių puslapiuose, galite konfigūruoti produktų palyginimo mygtuką, kuris leidžia pardavėjams įtraukti produktus į palyginimo padėklą. Ši funkcija konfigūruota svetainės generatoriuje naudojant produktų palyginimo mygtukų modulį, kuris veikia kaip sparčiojo [rodinio modulis](quick-view-module.md).

Kai svetainės vartotojai prideda produktų, kuriuos reikia palyginti, pasirinkdami juos produkto skirtuke, palyginimo padėklas rodomas puslapio apačioje. Palyginimo padėklas rodo produktus, kuriuos šiuo metu lyginant pirkėjas, ir trumpas produktų peržiūras. Svetainės vartotojai taip pat gali įtraukti produktus iš informacijos apie produktą puslapių (PDPs) ir įtraukti konkrečius produktų variantus, kad būtų galima palyginti su pagrindiniais produktais.

Kai klientai į palyginimo padėklą įtraukia keletą produktų, jie gali pasirinkti **Lyginti,** kad būtų nukreipti į produktų palyginimo puslapį. Produktų palyginimo puslapyje rodoma išsami kiekvieno pasirinkto produkto informacija, kad klientai galėtų palyginti vaizdus, kainas, produkto dimensijas (dydį, stilių ir spalvą), sudėtiaus vertinimo informaciją ir kitus produkto atributus.

Toliau pateikta iliustracija pateikia produkto palyginimo mygtukų pavyzdžius, šalinimą iš palyginimo mygtuko, palyginimo padėklą ir produktų palyginimo puslapį.

![Produktų palyginimo apžvalga, kurioje rodomas produkto palyginimo mygtukas, pašalinimas iš palyginimo mygtuko, palyginimo padėklo sritis ir produktų palyginimo puslapis.](./media/Product-Comparison-Overview.png)

> [!NOTE]
> - Produktų palyginimo puslapyje lyginamas numatytasis produkto ypatybės ir visi atributai, kuriuos galima peržiūrėti šio produkto PDP.
> - Tokių ypatybės kaip pristatymo būdas, turimos atsargos ir matavimo vienetas negali būti peržiūrimos produktų palyginimo puslapyje.
> - Klientai gali įtraukti produktus iš skirtingų kategorijų į palyginimo padėklą, nes produktai yra iš to paties katalogo.
> - Produktų palyginimo funkcija šiuo metu yra apribota produktų palyginimu individualioje kataloge. Svetainės vartotojai negali atlikti kryžminio katalogo palyginimų.
> - Turite užtikrinti, kad visų produktų **palyginimo modulių** ypatybė Atvaizduoti modulį kliento pusėje yra išvalyta.
> - Turite užtikrinti, kad puslapių lygio kaupimas talpykloje būtų išjungtas visuose puslapiuose, kuriuose naudojamas produktų palyginimo modulis. Šiuose puslapiuose yra PDPs, PLPs ir produktų palyginimo puslapiai. Daugiau informacijos rasite Konfigūruoti puslapio [kaupimą talpykloje](e-commerce-extensibility/page-caching.md).

Šioje iliustracijoje pateikiamas produktų palyginimo puslapio pavyzdys.

![Produktų palyginimo puslapis.](./media/Product-Comparison-Page.png)

## <a name="add-the-product-comparison-module-to-a-new-product-comparison-page"></a>Įtraukti produktų palyginimo modulį į naują produktų palyginimo puslapį

Galite sukurti skirtą produktų palyginimo puslapį pridėdami produktų palyginimo modulį prie puslapio teksto. Be įgalintų klientų palyginti skirtingų produktų informaciją, galite konfigūruoti produktų palyginimo modulį, kad suteikite klientams galimybę greitai užbaigti pirkimą po to, kai jie palygina produktus. Produktų palyginimo modulyje taip pat **yra** tuščias palyginimo atminties laukas, kuriame galite įtraukti turinio blokavimo modulį, kuris aprašo tuščią būseną (pvz., "Jūsų produktų palyginimas tuščias").

Norėdami įtraukti produktų palyginimo modulį į naują produktų palyginimo puslapį, atlikite šiuos veiksmus.

1. Eikite į **Puslapiai** ir pasirinkite **Naujas**, kad sukurtumėte naują puslapį.
1. Dialogo lange **Kurti naują puslapį** po **Puslapio** pavadinimas įveskite tinkamą puslapio pavadinimą (pvz., **Produktų palyginimas**) ir pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti šabloną** pasirinkite atitinkamą šabloną (pvz., šabloną, kurį naudoja numatytasis kategorijos puslapis) ir pasirinkite **Pirmyn**.
1. Dalyje **Pasirinkti maketą** pasirinkite puslapio maketą (pvz., Lankstusis **maketas**) ir pasirinkite **Pirmyn**.
1. Dalyje **Peržiūrėti ir baigti** peržiūrėkite puslapio konfigūraciją. Jei turite redaguoti puslapio informaciją, pasirinkite **Atgal**. Jei puslapio informacija teisinga, pasirinkite Kurti **puslapį**.
1. Pagrindiniame laiko **atminties atminties** lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite konteinerio **modulį**, tada pasirinkite **Gerai**.
1. Konteinerio **laiko** atminties atminties dalyje pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite produktų palyginimo **modulį**, tada pasirinkite **Gerai**.
1. Sparčiojo **rodinio mygtukų** atrinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite sparčiojo produkto **rodinio modulį**, tada pasirinkite **Gerai**.
1. Dešinėje ypatybės srityje sukonfigūruokite produkto sparčiojo **rodinio modulio** ypatybes.
1. Tuščiame **palyginimo** laiko atminties atminties lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite turinio bloko **modulį**, tada pasirinkite **Gerai**.
1. Dešinėje ypatybės srityje sukonfigūruokite turinio bloko **modulio** ypatybes. 
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

Šioje iliustracijoje pateikiamas tuščio palyginimo puslapio, palyginimo svetainės generatoriuje, pavyzdys.

![Produktų palyginimo modulis.](./media/Product-comparison-module.png)

## <a name="add-a-product-comparison-button-to-product-tiles-on-search-and-category-results-pages"></a>Įtraukti produktų palyginimo mygtuką į produkto pagal paiešką ir kategorijos rezultatų puslapius

Produktų palyginimo mygtukas leidžia vartotojams greitai įtraukti produktą į palyginimo padėklą, kai jie naršyti produktus sąrašo puslapyje. Jie gali įtraukti vieną ar daugiau produktų į palyginimo padėklą iš sąrašo puslapio neprieidami prie PDP.

Produktų palyginimo mygtuką palaiko produktų rinkinio, paieškos rezultatų ir PDP pirkimo dėžės moduliai.

Norėdami įtraukti produktų palyginimo mygtuką į produkto pagal paiešką ir kategorijos rezultatų puslapius, atlikite šiuos veiksmus.

1. Svetainės generatoriuje eikite į **puslapius** ir atidarykite kategorijos puslapį, prie kurio norite pridėti produktų palyginimo mygtuką.
1. Pagrindiniame laiko **atminties atminties** lape pasirinkite daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti** modulius pasirinkite ieškos **rezultatų modulį**, tada pasirinkite **Gerai**.
1. Ieškos rezultatų **modulio** produktų palyginimo mygtuko **atrinkite** daugtaškį (**...**), tada pasirinkite Įtraukti **modulį**.
1. Dialogo lange **Pasirinkti modulius** pasirinkite produktų palyginimo **mygtukų** modulį, tada pasirinkite **Gerai**.
1. Dešinėje ypatybės srityje sukonfigūruokite produktų palyginimo **mygtuko modulio** ypatybes.
1. Norėdami peržiūrėti puslapį, pasirinkite **Įrašyti** ir **Peržiūrėti**.
1. Pasirinkite **Baigti redagavimą**, kad užregistruotumėte puslapį, o tada pasirinkite **Publikuoti**, kad publikuotumėte jį.

## <a name="add-a-product-comparison-preview-panel-module-to-pages-on-your-website"></a>Produktų palyginimo peržiūros skydo modulio pridėjimas prie jūsų svetainės puslapių

Produktų palyginimo peržiūros skydo modulis suteikia klientams galimybę peržiūrėti produktus, kuriuos jie įtraukia į palyginimą arba iš jo pašalinami. Peržiūros skyde taip pat yra parinktys, galimos tiesiogiai naršyti palyginimo puslapį arba išvalyti visą produktų sąrašą. 

Rekomenduojame įgalinti peržiūros skydą visuose puslapiuose, kur įgalintas **produktų palyginimo** mygtukas. Modulis gali būti **pridėtas** prie produktų palyginimo mygtuko kaip atminties modulis arba gali būti naudojamas kaip atskiras modulis, kurį galima konfigūruoti bet kuriame puslapyje, net jei nėra funkcijų įtraukti ar pašalinti lygintinas produktus. 

Turite rankiniu būdu įtraukti produktų palyginimo peržiūros skydo modulį į puslapį. Turėtumėte įtraukti tik vieną peržiūros skydo modulį į puslapį. Jei į puslapį įtraukiate keletą modulio egzempliorių, pirmasis modulis bus atvaizduotas, o likusios egzemplioriaus nebus paisoma.

![Produktų palyginimo peržiūros skydas](./media/product-comparison-preview-panel-2.png)

Jei nurodysite produktų palyginimo limitą, galėsite pasirinkti įjungti teksto ženklus peržiūros skyde, kuris parodo, kiek produktų gali būti pridėta prie palyginimo. Į palyginimą įtraukti produktai pakeičiami vietos rezervavimo ženklais. Norėdami konfigūruoti produktų palyginimo ribą ir įgalinti rezervavimo ženklus, **svetainės generatoriuje eikite į svetainės > ir** **atlikite keitimus produktų palyginimų** skyriuje. Konfigūracija bus taikoma visiems visų puslapių peržiūros skydams. 


## <a name="specify-the-maximum-number-of-products-to-show-in-the-comparison-tray"></a>Nurodykite didžiausią produktų, kurie bus rodomi palyginimo padėkle, skaičių

Galite nurodyti didžiausią produktų skaičių, rodytinas palyginimo padėkle, nustatę svetainės **parametrų \> plėtinius** svetainės generatoriuje. Galite konfigūruoti atskiras didžiausias ribas, skirtas darbalaukio ir mobiliojo kompiuterio rodiniams. Numatyta, kad jokia riba nebus įvykdyta, jei nebus nustatyta jokia maksimali riba.

> [!NOTE]
> Norint sukurti optimalų naršymo patirtį, **rekomenduojame nustatyti didžiausią produktų skaičių palyginimo padėkle kaip 2** **, jei tai yra mobiliojo rodinio prievadas, o kaip 4**, jei norite sumažinti horizontaliosios slinkties, kuri yra reikalinga, kiekį.

Norėdami nurodyti didžiausią produktų skaičių palyginimo padėkle, atlikite šiuos veiksmus.

1. Svetainės generatoriuje eikite į svetainės **parametrų \> plėtinius**.
1. Palyginimo **ribos produktų** – darbalaukio įrenginių ypatybėje įveskite didžiausią produktų, kurie turi būti rodomi darbalaukio rodinio palyginimo padėkle, skaičių.
1. Norėdami nustatyti produktų **palyginimo limitą** – mobiliųjų įrenginių ir planšetinių įrenginių ypatybėje, įveskite didžiausią produktų, kurie turi būti rodomi mobiliojo įrenginio ir planšetinio kompiuterio rodinio palyginimo padėkle, skaičių.
1. Komandų juostoje pasirinkite Įrašyti ir **publikuoti**.

![Svetainės parametrai, norint apriboti palyginimo padėklo produktus.](./media/Site-settings-to-limit-products-in-comparison-tray.png)
