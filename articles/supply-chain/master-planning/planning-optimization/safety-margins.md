---
title: Laiko rezervai
description: Šiame straipsnyje aprašoma, kaip veikia laiko rezervas atliekant bendrąjį planavimą.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-9-14
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 87b38276a2723374969a67c5413dde15537d04ec
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740447"
---
# <a name="safety-margins"></a>Laiko rezervai

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip veikia laiko rezervas atliekant bendrąjį planavimą.

## <a name="safety-margins-overview"></a>Laiko rezervų peržiūra

Laiko rezervų paskirtis yra įgalinti sąranką, suteikiančią buferio laiko siekiant viršyti įprastą gamybos laiką. Pavyzdžiui, kai medžiaga turi būti išpakuota ar patikrinta po to, kai ji atvyksta iš tiekėjo, negalima tiesiog įtraukti papildomo laiko į pirkimo gamybos laiką, nes tokiu atveju papildomas buferio laikas bus priskirtas tiekėjui. Šiame pavyzdyje galima naudoti gavimo laiko rezervą siekiant užtikrinti, kad tiekėjas pristatytų anksčiau. Šis metodas teikia buferio laiko, kad prekes būtų galima apdoroti viduje.

Yra trys laiko rezervų tipai:

- **Užsakymo laiko rezervas** – tiekimo užsakymo pateikimo buferio laikas
- **Gavimo laiko rezervas** – gaunamo tiekimo tvarkymo buferio laikas
- **Išdavimo laiko rezervas** – siuntų tvarkymo buferio laikas

Toliau pateiktoje iliustracijoje parodyta, kaip šie laiko rezervai taikomi laikui bėgant.

![Laiko rezervai.](media/safety-margins-1.png)

Visi laiko rezervai apibrėžiami dienomis. Numatytoji vertė yra *0* (nulis), nurodanti, kad netaikomas laiko rezervas. Jei nustatote kelis laiko rezervus, jie visi įtraukiami į bendrą laiką nuo tiekimo *užsakymo datos* iki paklausos *poreikio datos*. Pavyzdžiui, sąrankoje nenustatytas gamybos laikas, o visi trys laiko rezervų tipai nustatyti į vieną dieną. Tokiu atveju nuo tiekimo užsakymo datos ir paklausos poreikio datos bus trys dienos, taigi, jei užsakymo data yra liepos 1 d., poreikio data būtų liepos 4 d.

### <a name="receipt-margin"></a>Gavimo laiko rezervas

Gavimo laiko rezervas yra turbūt labiausiai naudojamas iš trijų laiko rezervų. Jis taikomas *pristatymo datai* ir atgal nuo *poreikio datos*. Kitaip tariant, produktai turi būti gauti nurodytą gavimo laiko rezervo dienų skaičių iki poreikio datos.

Toliau pateiktoje iliustracijoje pabrėžiamas gavimo laiko rezervas.

![Gavimo laiko rezervas.](media/safety-margins-2.png)

Gavimo laiko rezervas paprastai naudojamas kaip buferis, siekiant užtikrinti sandėlio registravimo laiką arba kitus daug laiko reikalaujančius procesus, kurie nėra fiksuojami kaip bendrojo gamybos laiko dalis sistemoje. Pirkimo atveju vienas privalumas yra tai, kad pirkimo užsakymo *pristatymo data* atitinkamai perkeliama į priekį. Jei pratęsite gamybos laiką, užuot naudoję laiko rezervą, tiekėjo vis tiek bus paprašyta pristatyti paskutinę minutę.

Atkreipkite dėmesį, kad gavimo laiko rezervas nekeičia tiekimo *poreikio datos*. Todėl gavimo laiko rezervas nėra tiesiogiai matomas, kai lyginamos paklausos ir tiekimo poreikio datos (pvz., puslapyje **Grynieji poreikiai**). Pvz., jei nustatytas keturių dienų gavimo laiko rezervas, o pirkimo užsakymo eilutės gavimas penkioliktą 15 mėnesio dieną, bendrasis planavimas apskaičiuoja koreguotą gavimo datą, kuri yra devyniolikta mėnesio diena.

Atkreipkite dėmesį, kad gavimo laiko rezervas nėra taikomas, kai tiekimui naudojamos turimos atsargos. Visos turimos atsargos laikomos pasiekiamomis nedelsiant, neatsižvelgiant į tai, kada jos buvo gautos.

### <a name="reorder-margin"></a>Užsakymo laiko rezervas

Toliau pateiktoje iliustracijoje pabrėžiamas užsakymo laiko rezervas.

![Užsakymo laiko rezervas.](media/safety-margins-3.png)

Užsakymo laiko rezervas įtraukiamas prieš visų suplanuotų užsakymų prekių gamybos laiką bendrojo planavimo metu. Todėl tai užtikrina papildomą laiką, kurio reikia pateikti tiekimo užsakymui. Šis laiko rezervas paprastai naudojamas kaip buferis, siekiant užtikrinti patvirtinimo procesų ir kitų vidinių procesų, reikalingų kuriant tiekimo užsakymus, laiką. Užsakymo laiko rezervas pateikiamas tarp tiekimo *užsakymo datos* ir *pradžios datos*.

### <a name="issue-margin"></a>Išdavimo laiko rezervas

Toliau pateiktoje iliustracijoje pabrėžiamas išdavimo laiko rezervas.

![Išdavimo laiko rezervas.](media/safety-margins-4.png)

Išdavimo laiko rezervas atimamas iš paklausos poreikio datos bendrojo planavimo metu. Tai padeda užtikrinti, kad turėtumėte laiko reaguoti į gaunamus poreikio užsakymus ir juos išsiųsti. Šis laiko rezervas paprastai naudojamas kaip buferis, siekiant užtikrinti siuntimo ir susijusių siunčiamų sandėlio procesų laiką.

Atkreipkite dėmesį, kad kai taikomas išdavimo laiko rezervas, nesutampa susijusios tiekimo ir paklausos poreikio datos. Vietoj to jos skiriasi pagal išdavimo laiko rezervą, nes išdavimo laiko rezervas įtraukiamas tarp tiekimo *poreikio datos* ir paklausos *poreikio datos*.

## <a name="set-up-safety-margins"></a>Laiko rezervų nustatymas

### <a name="turn-safety-margins-on-or-off"></a>Įjungti arba išjungti saugos maržas

Jei norite naudoti šią funkciją, ją turite įjungti savo sistemoje. Kaip ir tiekimo grandinės valdymo versija 10.0.29, ši funkcija yra privaloma ir jos išjungti negalima. Jei jūsų versija senesnė nei 10.0.29, tada *·*[administratoriai](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gali įjungti arba išjungti šią funkciją ieškodami planavimo optimizavimo funkcijos maržų funkcijų valdymo darbo srityje.

### <a name="define-safety-margins"></a>Laiko rezervų nustatymas

Laiko rezervų sąranka yra lanksti. Juos galima nustatyti ir *padengimo grupėje*, ir *bendrajame plane*. Svarbu, kad suprastumėte, jog laiko rezervai įtraukiami vienas ant kito. Pavyzdžiui, dviejų dienų gavimo laiko rezervas padengimo grupėje ir trijų dienų bendrajame plane užtikrins penkias dienas galiojantį gavimo laiko rezervą.

Galimybė nustatyti laiko rezervą bendrajame plane gali būti naudinga, kai norite imituoti ilgesnį gamybos laiką arba tam tikro plano neapibrėžtumą nekeisdami kasdienio planavimo.

#### <a name="coverage-group-safety-margins"></a>Padengimo grupių laiko rezervai

Norėdami taikyti laiko rezervą padengimo grupei, atlikite toliau pateiktus veiksmus.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Padengimo grupės**.
1. Sąrašo srityje pasirinkite norimą padengimo grupę.
1. Skyriaus **Laiko rezervai dienomis** „FastTab” **Kita** naudokite toliau pateiktus laukus, kad nustatytumėte reikiamus laiko rezervus (dienomis).

    - Gavimo laiko rezervas, pridėtas prie pareikalavimo datos
    - Išdavimo laiko rezervas, atimtas iš pareikalavimo datos
    - Keisti maržos, įtrauktos į prekės gamybos laiką, tvarką

#### <a name="master-plan-safety-margins"></a>Bendrųjų planų laiko rezervai

Norėdami taikyti laiko rezervą bendrajam planui, atlikite toliau pateiktus veiksmus.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Planai \> Bendrieji planai**.
1. Sąrašo srityje pasirinkite norimą bendrąjį planą.
1. „FastTab” **Laiko rezervai dienomis** naudokite toliau pateiktus laukus, kad nustatytumėte reikiamus laiko rezervus (dienomis).

    - Gavimo laiko rezervas, pridėtas prie pareikalavimo datos
    - Išdavimo laiko rezervas, atimtas iš pareikalavimo datos
    - Keisti maržos, įtrauktos į prekės gamybos laiką, tvarką

### <a name="define-whether-calculations-are-based-on-calendar-days-or-work-days"></a>Nurodykite, ar skaičiavimai pagrįsti kalendorinėmis dienomis, ar darbo dienomis

Galite nustatyti visus laiko rezervus, kad jie būtų apskaičiuojami pagal kalendorines dienas arba darbo dienas.

1. Eikite į **Bendrasis planavimas \> Sąranka \> Bendrojo planavimo parametrai**.
1. Skyriaus **Laiko rezervai dienomis** skirtuke **Bendra** nustatykite parinktį **Darbo dienos** į *Taip*, kad laiko rezervai būtų apskaičiuoti pagal darbo dienas. Nustatykite parinktį į *Ne*, kad laiko rezervai būtų apskaičiuoti pagal kalendorines dienas.

Pavyzdžiui, kalendorius yra atidarytas nuo pirmadienio iki penktadienio ir uždarytas nuo šeštadienio iki sekmadienio. Jei yra vienos dienos laiko rezervas, pirmadienio poreikio data pateikia praėjusio penktadienio pristatymo datą, nes šeštadienis ir sekmadienis nėra darbo dienos.

Kalendorius, naudojamas darbo dienoms nustatyti, priklauso nuo sąrankos ir tiekimo tipo. Jį gali valdyti padengimo grupės, sandėlio ir tiekėjo kalendoriai.

> [!NOTE]
> Jei *sandėlis* nėra padengimo dimensijos dalis (kitaip tariant, planavimas paremtas tik *svetaine*), sandėlio kalendorius nenaudojamas.

Sistema gali tvarkyti sąranką, kurioje apibrėžti vienas arba daugiau kalendorių. Toliau esančiuose poskirsniuose aprašomi galimi deriniai, kuriuos galima naudoti rezultatui valdyti.

#### <a name="calendar-that-is-used-for-the-duration"></a>Kalendorius, naudojamas trukmei

Nustatyti kalendoriai valdo faktinį bendrąjį gamybos laiką kalendorinėmis dienomis nuo tiekimo užsakymo datos iki paklausos poreikio datos. Naudojami toliau pateikti kalendoriaus prioritetai.

- **Pirkimo gamybos laikas** – atsižvelgiama tik į padengimo grupės kalendorių.
- **Gavimo laiko rezervas** – naudojamas padengimo grupės kalendorius, jei jis nustatytas. Kitu atveju bus naudojamas sandėlio kalendorius.
- **Išdavimo laiko rezervas** – naudojamas padengimo grupės kalendorius, jei jis nustatytas. Kitu atveju bus naudojamas sandėlio kalendorius.
- **Užsakymo laiko rezervas** – atsižvelgiama tik į padengimo grupės kalendorių.

#### <a name="calendar-that-is-used-for-the-final-date"></a>Kalendorius, naudojamas galutinei datai

Toliau pateiktos taisyklės taikomos siekiant nustatyti, ar planavimo mechanizmas gali naudoti nurodytos datos tipo nurodytą datą.

- **Pirkimo gavimo data** – naudojamas tiekėjo kalendorius, jei jis nustatytas. Kitu atveju naudojamas padengimo grupės kalendorius, jei jis nustatytas. Jei nei vienas iš šių kalendorių nenustatytas, naudojamas sandėlio kalendorius.
- **Perkėlimo gavimo data** – naudojamas padengimo grupės kalendorius, jei jis nustatytas. Kitu atveju bus naudojamas sandėlio kalendorius.
- **Gamybos gavimo data** – naudojamas padengimo grupės kalendorius, jei jis nustatytas. Kitu atveju bus naudojamas sandėlio kalendorius.
- **Poreikio išdavimo atvira data** – naudojamas sandėlio kalendorius, jei jis nustatytas. Kitu atveju naudojamas padengimo grupės kalendorius.
- **Užsakymo atvira data** – naudojamas padengimo grupės kalendoriaus ir tiekėjo kalendoriaus derinys (sankirta). Abu kalendoriai turi būti atidaryti, kad būtų galima naudoti datą. Jei tik vienas iš šių kalendorių nustatytas, naudojamas tik tas kalendorius.

#### <a name="calendar-setup-overview-matrix"></a>Kalendoriaus nustatymo peržiūros matrica

Toliau pateikiamoje iliustracijoje vaizduojama matrica, kurioje apibendrinama, kurie kalendoriai taikomi, kai apskaičiuojami laiko rezervai.. (Pasirinkite nuotrauką, kad būtų atidaroma didelės skiriamosios gebos versija.) Toliau pateiktos santrumpos ir spalvos naudojamos nustatyti, kur nurodytas kiekvienas kalendoriaus tipas:

- **Padengimo grupė (CG):** žalia
- **Sandėlis (WH):** geltona
- **Tiekėjas (V):** mėlyna

[![Kalendoriaus nustatymo peržiūros matrica.](media/safety-margins-calendar-matrix.png)](media/safety-margins-calendar-matrix-high.png)

## <a name="calculating-delays"></a>Atidėjimų skaičiavimas

Visi trys laiko rezervai įtraukiami, kai sistema nustato, ar užsakymas atidėtas.

Pavyzdžiui, prekės gamybos laikas yra viena diena , o gavimo laiko rezervas yra trys dienos. Šios prekės pardavimo užsakymas nustatomas taip, kad jis reikalingas šiandien. Šiuo atveju atidėjimas skaičiuojamas kaip *gamybos laikas* + *gavimo laiko rezervas* = keturios dienos. Todėl, jei šiandien yra rugpjūčio 14 d., keturios atidėjimo dienos nustato pristatymą į rugpjūčio 18 d. Toliau pateikiamoje iliustracijoje vaizduojamas šis pavyzdys.

![Atidėjimo skaičiavimo pavyzdys.](media/safety-margins-delays.png)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]