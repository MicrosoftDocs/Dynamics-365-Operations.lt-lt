---
title: Funkcinių vietų kūrimas
description: Šioje temoje paaiškinta, kaip kurti funkcines vietas turto valdyme.
author: josaw1
manager: tfehr
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationCopyStructure, EntAssetFunctionalLocationCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37da9d59e4e9cf84238f6798a1aa7de72ff91f02
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888841"
---
# <a name="create-functional-locations"></a>Funkcinių vietų kūrimas

[!include [banner](../../includes/banner.md)]

 

Šioje temoje paaiškinta, kaip kurti funkcines vietas turto valdyme.

Kuriant funkcinės vietos struktūrą žinokite, kad sukūrus funkcinę vietą nebus galima perkelti jos iš pradinės vietos. Tai reiškia, kad prieš pradėdami jas kurti turto valdyme derėtų atidžiai apsvarstyti funkcinių vietų struktūrą. Jei funkcinė vieta netinka, ją galima panaikinti, jeigu ji dar nebuvo pradėta naudoti.

Kad būtų galima dirbti su funkcinėmis vietomis, būtina sukurti dvi funkcinių vietų „kategorijas“:

- Sukurkite *vieną* numatytąją funkcinę vietą be antrinių vietų. Ši funkcinė vieta naudojama tik kaip standartinė turto vieta kuriant naują turtą.  
- Sukurkite funkcinių vietų struktūras, būtinas siekiant valdyti jūsų įmonės priežiūros užduotis.

## <a name="create-a-default-functional-location"></a>Numatytosios funkcinės vietos kūrimas

Funkcinių vietų naudojimą pradėkite nuo vienos numatytosios vietos sukūrimo, kuri bus naudojama kuriant naują turtą. Ši funkcinė vieta yra ta, kurią pasirenkate dalies **Turto valdymas** > **Sąranka** > **Turto valdymo parametrai** > **Turtas** nuoroda > lauke **Numatytoji funkcinė vieta**. Numatytąją funkcinę vietą galima naudoti kuriant naują turtą ir dar nesukūrus ta turtui funkcinės vietos struktūros.

1. Pasirinkite **Turto valdymas** > **Bendra** > **Funkcinės vietos** > **Visos funkcinės vietos**.  
2. Dalyje **Visos funkcinės vietos** pasirinkite **Nauja**.
3. Lauke **Funkcinė vieta** įterpkite ID, pvz., „0000“ arba „Numatytoji“, kad nurodytumėte, jog tai yra speciali funkcinė vieta.
4. Lauke **Pavadinimas** įterpkite numatytosios funkcinės vietos pavadinimą.
5. *Nepasirinkite* pirminio elemento lauke **Pirminis** – palikite šį lauką tuščią.
6. Lauke **Funkcinės vietos tipas** pasirinkite funkcinės vietos tipą, kuris bus naudojamas numatytai funkcinei vietai. Daugiau informacijos apie funkcinių vietų tipų nustatymą žr. [Funkcinių vietų tipai](../setup-for-functional-locations/functional-location-types.md).
7. Pasirinkite **Gerai**. Nereikėtų įtraukti papildomų šios funkcinės vietos duomenų, nes ji naudojama tik kaip laikina naujo turto vieta, kol įdiegsite turtą savo įmonės naudojamose funkcinėse vietose.

## <a name="create-functional-locations"></a>Funkcinių vietų kūrimas

Toliau pateiktoje procedūroje aprašoma, kaip kurti funkcines vietas, reikalingas priežiūros valdymui jūsų įmonėje.

1. Pasirinkite **Turto valdymas** > **Bendra** > **Funkcinės vietos** > **Visos funkcinės vietos**. Galite kurti funkcinę vietą iš tinklelio rodinio arba informacijos rodinio.
2. Pasirinkite mygtuką **Nauja**.
3. Lauke **Funkcinė vieta** įterpkite ID.
4. Lauke **Pavadinimas** įterpkite funkcinės vietos pavadinimą.
5. Jei funkcinė vieta yra antrinė struktūros vieta, pasirinkite pirminę vietą lauke **Pirminis**.
6. Pasirinkite tipą lauke **Funkcinės vietos tipas**.
7. Pasirinkite **Gerai**.
8. Pasirinkite funkcinę vietą ir spustelėkite mygtuką **Redaguoti**, kad įtrauktumėte papildomos informacijos.

>[!NOTE]
>Atsižvelgiant į funkcinės vietos ciklo būsenų nustatymą, gali tekti sukurti visas funkcinės vietos antrines vietas, tada prieš pradedant diegti turtą pakeisti funkcinės vietos ciklo būseną. Daugiau informacijos apie turto diegimą žr. [Turto diegimas funkcinėse vietose](../functional-locations/install-objects-on-functional-locations.md). Norėdami sužinoti daugiau apie funkcinės vietos ciklo būsenas, žr. [Funkcinės vietos ciklo būsenos](../setup-for-functional-locations/functional-location-stages.md).

Rodinyje Informacija bus rodomi „FastTab“, kuriuose galėsite įtraukti ir redaguoti informaciją apie funkcinę vietą.

## <a name="general-information"></a>Bendroji informacija

Šiame skyriuje pateikta pagrindinių ir antrinių vietų funkcinių vietų struktūroje informacijos apžvalga. Skyriuje **Informacija** pateiktas turto atributų, priežiūros planų ir turto, susijusio su funkcine vieta, skaičius. Dalyje **Atsargos** galite pasirinkti vietą ir sandėlį, su kuriuo susijusi funkcinė vieta. Vieta ir sandėlis naudojami kartu su darbo užsakymo prekių prognozėmis. Kuriant prekių prognozę automatiškai naudojama turto funkcinės vietos ir sandėlio informacija. Skyriuje **Ciklo būsena** rodoma informacija apie funkcinės vietos ciklo būseną.

## <a name="installed-assets"></a>Įdiegti turto elementai

Daugiau informacijos apie turto diegimą žr. [Turto diegimas funkcinėse vietose](../functional-locations/install-objects-on-functional-locations.md). Jei norite matyti daugiau „FastTab“ mygtukų, galite naudoti šio „FastTab“ mygtuką **Rodinys**. Laukai **Galioja nuo** ir **Antrinis turtas** gali būti rodomi tinklelyje.

## <a name="asset-attribute-requirements"></a>Reikalavimai turto atributams

Šiame „FastTab“ galite įtraukti konkrečius atributo reikalavimus turtui, kurį diegiate funkcinėje vietoje. Šie reikalavimai skirti tik pateikti informaciją. Jie netrukdo diegti turto su kitais atributų reikalavimais. Pasirinkite **Įtraukti eilutę**, tada pasirinkite atributo tipą. Įterpkite atitinkamą **Reikšmę**, pasirinkite ribinę reikšmę lauke **Ribinės reikšmės kriterijai**, tada išsaugokite įrašą.

## <a name="maintenance-plans-and-maintenance-rounds"></a>Priežiūros planai ir priežiūros ciklai

Čia galite įtraukti priežiūros planus ir priežiūros ciklus į funkcinę vietą, įskaitant pradžios datą. Funkcinėje vietoje įdiegtas turtas gali turėti nustatytus kitus priežiūros planus. Visi priežiūros planai ir priežiūros ciklai gali būti naudojami planuojant turto kalendoriaus įrašus funkcinei vietai ir šiuo metu įdiegtam turtui.

>[!NOTE]
>Jei atnaujinsite turto tipų, turto prekių ženklų ir turto modelių nustatymą priežiūros planų išsamiame rodinyje **Visos funkcinės vietos** > „FastTab“ **Priežiūros planai** suplanavę priežiūros planus, esami priežiūros grafiko įrašai, susiję su ta funkcine vieta, bus automatiškai panaikinti. Norėdami kurti naujus grafiko įrašus, kurie atitiktų atnaujintą priežiūros plano nustatymą funkcinėje vietoje, būtina paleisti naują priežiūros plano grafiką tai funkcinei vietai. 

## <a name="address"></a>Adresas

Įterpkite funkcinės vietos adresą „FastTab“ **Adresas**. Adresai funkcinėse vietose yra paveldimi. Tai reiškia, kad jeigu antrinė vieta neturi nurodyto adreso, naudojamas pagrindinės vietos adresas.

## <a name="workers"></a>Darbininkai

Šiame „FastTab“ galima įtraukti darbuotojų, susijusių su funkcine vieta, taip pat galima pasirinkti funkcinę vietą kaip pagrindinę darbuotojo vietą. 

## <a name="attributes"></a>Atributai

Šiame „FastTab“ galite nustatyti funkcinės vietos atributų reikšmes. Šie atributai gali būti naudojami siekiant apibūdinti funkcinei vietai būdingas ypatybes ar savybes, pvz., struktūrines ypatybes, pastato tipą, vietovės aprašymus, vietos buvimą po žeme ar virš žemės paviršiaus.

Pasirinkite **Įtraukti eilutę**, tada pasirinkite atributo tipą. Tada įterpkite **Reikšmę**, susijusią su atributo tipu, ir išsaugokite įrašą.

## <a name="financial-dimensions"></a>Finansinės dimensijos

Funkcinei vietai galima pasirinkti finansines dimensijas. Siekiant leisti automatinį finansinių dimensijų atnaujinimą iš funkcinės vietos, galima nustatyti [Funkcinės vietos tipus](../setup-for-functional-locations/functional-location-types.md). Tai reiškia, kad finansinėje dimensijoje įdiegtas turtas automatiškai gauna funkcinei vietai skirtas finansines dimensijas. Tai naudinga, jei norite skirtingų išlaidų centrų atsižvelgiant į vietas.

Kai pagrindinėje funkcinėje vietoje atnaujinami **Svetainės**, **Sandėlio**, **Adreso** ir **Finansinių dimensijų** duomenys, susijusios antrinės funkcinės vietos gali būti atitinkamai atnaujinamos, jei atnaujindami atliksite pasirinkimą. Atidaromas dialogo langas, kuriame pateiktos naujinimo parinktys.

## <a name="copy-a-functional-location-structure"></a>Funkcinės vietos struktūros kopijavimas

Jei įmonė turi kelias funkcines vietas su panašiomis vietos struktūromis, galite naudoti kopijavimo funkciją turto valdyme, kad greitai sukurtumėte kelias panašias vietos hierarchijas. Kopijuojant konkrečią funkcinę vietą ar visą struktūrą, nauja vieta ar struktūra turi tą patį pavadinimą kaip ir ta, nuo kurios kopijuojama. Atlikus kopijavimo procedūrą galima lengvai pakeisti pavadinimą arba kitus naujos funkcinės vietos parametrus, jei tai leidžia pasirinkta naujos funkcinės vietos ciklo būsena.

1. Dalyje **Visos funkcinės vietos** pasirinkite norimą kopijuoti funkcinę vietą. Pvz., jei norite kopijuoti visą funkcinės vietos struktūrą, įskaitant antrines vietas, pasirinkite viršutinę vietą (pagrindinį elementą).
2. Pasirinkite mygtuką **Kopijuoti funkcinės vietos struktūrą**. Vieta, kurią pasirinkote sąrašo puslapyje, rodoma lauke **Kopijuoti iš**.
3. Lauke **Nauja funkcinė vieta** įterpkite naujos vietos pavadinimą.
4. Lauke **Pirminis elementas, kuriame įklijuojama** reikėtų įterpti tik pirminio elemento ID, jei kuriama vieta turėtų būti esamos funkcinės vietos struktūros dalis.
5. Spustelėkite **Gerai**. Nauja funkcinės vietos struktūra rodoma dalyje **Visos funkcinės vietos**.

>[!NOTE]
>Kopijuojant funkcinės vietos struktūrą, naujos struktūros funkcinės vietos ciklo būsenos nustatomos į „pirmąją būseną“, kurią sukūrėte funkcinėms vietoms. Ar galima pervardyti arba panaikinti funkcinę vietą naudojant mygtukus **Pervardyti** ir **Naikinti** dalyje **Visos funkcinės vietos**, priklauso nuo funkcinės vietos esamos ciklo būsenos.

## <a name="delete-a-functional-location"></a>Funkcinės vietos naikinimas

Funkcinė vieta su susijusiomis antrinėmis vietomis gali būti panaikinta, jei nė vienoje iš bandomų panaikinti funkcinių vietų nebuvo įdiegtas joks turtas ir jei tai leidžia dabartinė funkcinės vietos ciklo būsena.

1. Dalyje **Visos funkcinės vietos** pasirinkite norimą naikinti funkcinę vietą.
2. Jei reikia, atnaujinkite funkcinę vietą į funkcinės vietos ciklo būseną, leidžiančią naikinti funkcinę vietą.
3. Pasirinkite **Naikinti**.

>[!NOTE]
>Jei negalite panaikinti funkcinės vietos, galite tvarkyti naikinimą šiuo tikslu nustatydami funkcinės vietos ciklo būseną. Pavyzdžiui, galite nustatyti etapą „Nurašyta“ arba „Panaikinta“, kuris neturėtų būti aktyvus etapas, formoje **Funkcinės vietos ciklo būsenos**.
