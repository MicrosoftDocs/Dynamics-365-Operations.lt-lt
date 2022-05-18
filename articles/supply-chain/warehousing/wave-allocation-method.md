---
title: Bangos paskirstymas
description: Šioje temoje aprašoma, kaip nustatyti bangos paskirstymo veiksmą, įskaitant tai, kaip įgalinti lygiagretų jo apdorojimą.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 08781b26a4e066a026d4efa14670f073b04ec185
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695541"
---
# <a name="wave-allocation"></a>Bangos paskirstymas

[!include [banner](../includes/banner.md)]

Bangos apdorojimas gali užimti daug laiko, o didžiausia apdorojimo laiko dalis bus praleista paskirstymo ir darbo kūrimo veiksmuose.

Dabar galima kiekvieną šių veiksmų vykdyti lygiagrečiai, o tai gali padidinti bangos apdorojimo efektyvumą ir užtikrinti didesnį bangų našumą tame pačiame sandėlyje. Šioje temoje paaiškinama, kaip nustatyti lygiagretų bangos paskirstymo metodo vykdymą. Daugiau informacijos apie tai, kaip nustatyti lygiagretų darbo kūrimo vykdymą rasite [Darbo kūrimo planavimas bangos metu](configure-wave-schedule-work-creation.md).

Anksčiau sandėlyje buvo galima priskirti tik vieną bangą tuo pačiu metu. Šis apribojimas yra pašalintas ir pakeistas nauju apribojimu, kuris užrakina tik tas prekes ir dimensijas, kurios rezervavimo hierarchijoje yra virš vietos. Dimensijos, esančios aukščiau vietos, visada apima produkto dimensijas. Pavyzdžiui, jei prekė sukonfigūruota naudojant *Spalvą*, tada galima lygiagrečiai apdoroti jos variantus *Raudona*, *Mėlyna* ir *Geltona*.

Tai reiškia, kad jei tą pačią prekę, kurios tos pačios dimensijos aukščiau vietos, paskirsto viena banga, kitos bangos turės laukti, kol įgys tos pačios prekės ir dimensijų užraktą. Jeigu užrakto nepavyksta gauti laiku, įvyks klaida ir bangos apdorojimas nepavyks.

Norint naudoti lygiagretųjį apdorojimą, bangą reikia vykdyti pakete.

## <a name="performance-improvements"></a>Efektyvumo patobulinimai

Lygiagretaus apdorojimo efektyvumo nauda skirstoma į dvi kategorijas:

- **Padidintas našumas** – bangų našumas paprastai padidėja, net jei nesukonfigūruotas lygiagretusis apdorojimas, ypač scenarijuose, kurių bangose nėra prekių persidengimo.
- **Vienos bangos paskirstymo patobulinimas** – testuojant klientų duomenis buvo nustatyta, jog efektyvumas pagerėja 50% po perėjimo į lygiagretųjį paskirstymą. Lygiagrečiai apdorojama pagal prekes ir dimensijas aukščiau vietos, todėl patobulinimai priklauso nuo to, kiek skirtingų prekių yra bangoje, turimos infrastruktūros ir paskirstymo trukmės ir darbo kūrimo trukmės palyginimo.

## <a name="configure-parallel-allocation"></a>Lygiagrečiojo paskirstymo konfigūravimas

### <a name="warehouse-management-parameters"></a>Sandėlio valdymo parametrai

Norėdami naudoti lygiagretaus paskirstymo apdorojimą, eikite į **Sandėlio valdymas > Nustatymas > Sandėlio valdymo parametrai**, atidarykite skirtuką **Bangos apdorojimas** ir nustatykite šiuos parametrus:

- **Bangos apdorojimo paketų grupė** – pasirinkite paketų grupę, kurią turi naudoti pirminis bangų apdorojimas. Vėlesnis paskirstymo apdorojimas gali būti atliktas naudojant skirtingas paketų grupes.
- **Apdoroti bangas paketais** – nustatykite į *Taip* norėdami naudoti lygiagretųjį apdorojimą.
- **Laukti užrakto (ms)** – Įveskite laiką (milisekundėmis), kiek paskirstymo veiksmas lauks sistemos ištekliaus, kurį užrakino kitas paskirstymo veiksmas. Viršijus laiką, banga neapdorojama ir rodomas klaidos pranešimas. Rekomenduojame leisti mažiausiai keletą sekundžių, kad leistumėte užbaigti vieno loginio vieneto paskirstymą.

Daugiau informacijos apie šias ir kitas bangos apdorojimo pasirinktis puslapyje **Sandėlio valdymo parametrai** rasite [Sandėlio parametrai, skirti bangos apdorojimui](wave-warehouse-parameters.md).

## <a name="wave-process-methods"></a>Bangos apdorojimo metodai

Norėdami nustatyti lygiagretųjį apdorojimą:

1. Eikite į **Sandėlio valdymas > Sąranka > Bangos > Bangos apdorojimo metodai**.
1. Tinklelyje pasirinkite „`allocateWave`” metodą.
1. Veiksmų srityje pasirinkite **Užduoties konfigūracija**.
1. Atsidaro **Bangos skelbimo metodo užduoties konfigūracijos** puslapis. Šiame tinklelyje pateikiamas kiekvienas sandėlis, kuriame sukonfigūravote „`allocateWave`” metodą. Lygiagretusis apdorojimas bus naudojamas tik išvardytiems sandėliams. Jei reikia, naudokite veiksmų srities mygtukus pridėti ar pašalinti sandėliams iš tinklelio. 
1. Kiekvienam sandėliui nustatykite šiuos parametrus:
    - **Didžiausias paketinių užduočių skaičius** – nurodykite paketinių užduočių, kurios turėtų būti naudojamos pasirinkto sandėlio paskirstymui, skaičių. Optimalus paketinių užduočių skaičius priklauso nuo turimos infrastruktūros ir kitų paketinių užduočių, apdorojamų serveryje. Bandymai, atlikti keturių branduolių aplinkoje, skirtai bangos apdorojimui, parodė, kad naudojant aštuonias užduotis gaunami geri rezultatai.
    - **Bangos apdorojimo paketų grupė** – konkrečios paketų grupės gali būti naudojamos skirtingiems sandėliams, siekiant išplėsti paskirstymo apdorojimą sandėliui.

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>Lygiagretinimo visuose juridiniuose subjektuose įjungimas arba išjungimas

Rekomenduojame nustatyti „`allocateWave`” metodą, kuris būtų lygiagrečiai vykdomas visuose juridiniuose subjektuose, nes tai padeda padidinti bangos apdorojimo efektyvumą. Nuo tiekimo grandinės valdymo 10.0.17 versijos, *bangų* lygiagretinimo funkcija Paskirstyti bangą yra įjungta pagal numatytuosius nustatymus visoms naujiems ir atnaujintoms diegimams ir jos negalima išjungti dar kartą. Įgalinus šią funkciją, atsitinka taip:

- Atnaujinamas „`allocateWave`” metodas, kad būtų įtraukiamas užduoties konfigūracijos parametras, leidžiantis jums naudoti **Bangos apdorojimo metodų** puslapį nustatyti tuo pačiu metu vykdomų užduočių skaičių, atitinkantį lygiagrečių apdorojimų skaičių. Dėl to, bangos paskirstymo veiksme sunaudotas laikas (paprastai nuo 30% iki 60% bendro apdorojimo laiko) yra sumažinamas koeficientu, maždaug atitinkantį užduočių skaičių. Taip pat, galima pasirinkti, kuris paketas bus priskirtas šioms užduotims apdoroti. Svarbu pažymėti, kad visi jūsų juridiniai subjektai bus sukonfigūruoti bangų pakete apdorojimui. Sandėliams, kurie jau sukonfigūruoti apdoroti bangas pakete, ir sandėliams, kurie jau sukonfigūruoti naudoti „`allocateWave`” metodą lygiagrečiai, bus išlaikyta esama konfigūracija.
- Pagal numatytuosius nustatymus, visi nauji juridiniai subjektai yra sukonfigūruojami bangų pakete apdorojimui. Visiems naujiems sandėliams, kuriuose įgalinta **Sandėlio valdymo procesų** parinktis, bus sukonfigūruotas „`allocateWave`” metodas lygiagrečiam vykdymui pagal numatytuosius nustatymus.
- Puslapyje **Sandėlio valdymo parametrai** nustatykite **Procesas įrašo pakete** reikšmę į *Taip*, o **Laukti užrakto (ms)** – į numatytąsias 15 sekundžių. Tai reiškia, kad visos bangos bus vykdomos pakete. Paleidus bangą, ji gauna prekės ir dimensijų aukščiau vietos užraktą paskirstymo veiksmo metu. Kai kita bangos apdorojimo užduotis bando gauti tą patį identiško įrašo užraktą, jis blokuojamas iki tol, kol bus užbaigtas dabartinis procesas. Parametruose **Laukti užrakto (ms)** nustatomas maksimalus laikas, kiek sistema lauks prieš išleisdama užraktą.

Lygiagretusis paskirstymo apdorojimas reikalauja bangos apdorojimą vykdyti pakete. Todėl sumažinsite bangos apdorojimo efektyvumą, jei išjungsite parametrą **Procesas įrašo pakete**, ypač jei bangos apdorojimas naudoja lygiagretųjį procesą, kaip nurodyta atitinkamos bangos metodų užduoties konfigūracijoje.

Jei reikia, galite anuliuoti kiekvieną iš šių parametrų, nustatytų pagal numatytuosius nustatymus, kai jūsų egzemplioriuje automatiškai įgalinta *Bangos lygiagretinimas bangos paskirstymo metodui* funkcija. Norėdami tai atlikti, atlikite toliau pateiktus veiksmus.

- Eikite į **Sandėlio valdymas \> Sąranka \> Sandėlio valdymo parametrai**. Skirtuke **Bangos apdorojimas** taikykite pageidaujamas funkcijų **Bangų apdorojimas paketais** ir **Laukite užrakto (ms)** reikšmes.
- Eikite į **Sandėlio tvarkymas \> Sąranka \> Bangos \> Bangos apdorojimo metodai**. Pasirinkite „`allocateWave`” metodą. Veiksmų srityje pasirinkite **Užduoties konfigūracija** tam, kad atidarytumėte puslapį, kuriame išvardyti visi sandėliai, kuriuose nustatytas lygiagretus metodas. Jeigu reikia, modifikuokite arba panaikinkite kiekvieno sandėlio paketinių užduočių skaičių ir priskirtą bangos grupę.

## <a name="troubleshooting"></a>Trikčių diagnostika

### <a name="troubleshoot-using-the-infolog"></a>Trikčių diagnostika naudojant sistemos pranešimą

Kadangi naudojama paketinė sistema, bangos apdorojimo metu įvykstančios klaidos bus užfiksuotos kaip paketinių užduočių sistemos pranešimų dalis. Norėdami perskaityti su banga susijusias paketines užduotis:

1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
1. Pasirinkite bangą, kurią norite patikrinti.
1. Veiksmų srityje atidarykite skirtuką **Banga** ir iš **Bangos** grupės pasirinkite **Paketinės užduotys**.

Bangos apdorojimas yra savaime taisomas, todėl apie apdorojimo metu aptiktas klaidas turi būti pranešta naudojant sistemos pranešimą.

Įprasta klaida, susijusi su lygiagrečiu apdorojimu, gali būti ta, kad dvi bangos mėgina paskirstyti tą pačią prekę tuo pačiu metu ir viena banga dar neužbaigė paskirstymo, todėl kita banga negali gauti užrakto per nurodytą laiką. Jei taip nutinka, paketinių užduočių žurnale bus informacija, nurodanti, kad nebuvo galima gauti prekės užrakto, tokiu atveju, nepavykusią bangą reikia apdoroti dar kartą.

Kadangi apdorojimas vyksta lygiagrečiai, duomenys turi būti tvarkomi skirtingose lentelėse tam, kad būtų galima sekti apdorojimo būseną. Tai reiškia, kad paketinių užduočių žurnaluose gali būti klaidų, pavyzdžiui, dublikato raktų klaidų.

Paketinių užduočių klaidos taip pat yra paketinių užduočių žurnalo dalis. Pati svarbiausia informacija įprastai pateikiama apačioje.

Retais atvejais, pavyzdžiui, jei SQL ryšys nutrūko, įmanoma, kad bangos apdorojimas taps prieštaringos būsenos, kai atrodys, jog paketinė užduotis veikia, tačiau apdorojimas bus sustabdytas. Banga negali tvarkytis su tokiomis klaidomis, todėl bandoma išvalyti nepavykusias bangas, kai paleidžiama kita banga. Taip pat, jei dabartinė banga yra prieštaringos būsenos, atlikite šiuos veiksmus:

1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
1. Pasirinkite bangą, kurią reikia išvalyti.
1. Veiksmų srityje atidarykite skirtuką **Banga** ir **Bangos** grupėje pasirinkite **Bangos duomenų išvalymas**.

### <a name="troubleshoot-using-the-wave-progress-log"></a>Trikčių diagnostika naudojant bangos eigos žurnalą

Jei **Sandėlio valdymo parametrų puslapyje** įgalinta parinktis **Kurti bangos eigos žurnalą**, tada žurnalo įrašas sukuriamas kiekvieną kartą prasidedant ir baigiantis prekių ir jos dimensijų paskirstymui. Šį žurnalą turėtumėte įgalinti tik tada, kai jis reikalingas, pavyzdžiui, atliekant pradinį bandymą arba trikčių diagnostiką. Įgalinę šią parinktį, galite peržiūrėti žurnalą atlikdami šiuos veiksmus:

1. Eikite į **Sandėlio valdymas \> Siuntimo bangos \> Siuntos bangos \> Visos bangos**.
1. Pasirinkite bangą, kurią norite patikrinti.
1. Veiksmų srityje atidarykite skirtuką **Banga** ir **Bangos** grupėje pasirinkite **Eiga**.
