---
title: Visuotiniai mobiliojo įrenginio parametrai
description: Šiame straipsnyje paaiškinama, kaip nustatyti mobiliojo įrenginio parametrus sandėlio valdymo parametrų puslapyje.
author: Mirzaab
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e6e03414edd9243fcc4156195928455b30a7cee9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847765"
---
# <a name="global-mobile-device-parameters"></a>Visuotiniai mobiliojo įrenginio parametrai

[!include [banner](../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti visuotinius sandėlio valdymo parametrus, kurie veikia tai, kaip sistema sąveikauja su mobiliaisiais įrenginiais.

Daugiau informacijos apie tai, kaip nustatyti sandėlio darbuotojus, rasite [Sandėlio darbuotojo valdymas](manage-warehouse-workers.md). Išsamesnę informaciją apie licencijos numerio tvarkymą mobiliuosiuose įrenginiuose rasite[Numerio lentelės gavimas naudojant „Warehouse Management” mobiliųjų įrenginių programėlę](warehousing-mobile-device-app-license-plate-receiving.md). Daugiau informacijos apie ciklų skaičiavimo procesus ieškokite [Ciklų skaičiavimas](cycle-counting.md) ir [Ciklų skaičiavimo pavyzdiniai scenarijai](cycle-counting-scenarios.md).

## <a name="open-the-warehouse-management-parameters-page"></a>„Warehouse Management” parametrų puslapio atidarymas

Norėdami atidaryti **„Warehouse management” parametrų** puslapį, eikite į **„Warehouse management” \> Nustatymas \> „Warehouse management” parametrai**. Tada galite nustatyti su mobiliojo įrenginio darbu susijusius laukus, kaip aprašyta kitame šio straipsnio skyriuje.

## <a name="mobile-device-fasttab-on-the-general-tab"></a>Mobiliojo įrenginio „FastTab” skirtuke Bendra

Visuotiniai mobiliojo įrenginio parametrai pateikiami **Mobiliojo įrenginio** „FastTab” skirtuke **Bendra**, esančiame **„Warehouse Management” parametrų** puslapyje. Galimi šie laukai.

| Laukas | Aprašas |
|---|---|
| Mobiliojo įrenginio pranešimo tipas | Pasirinkite pardavimo užsakymo metu darbuotojams rodomos informacijos tipą. |
| Nuskaityto kiekio limitas | Įveskite didžiausią prekių kiekį, kurį darbuotojas gali nuskaityti kiekvieno seanso metu naudodamas mobiliojo įrenginio meniu elementą, kurio **Darbo kūrimo proceso** reikšmė yra *Koregavimas*. Šis laukas neturi įtakos nuskaitymams, kurie atliekami naudojant bet kurio kito tipo meniu elementą. |
| Naudoti mobilųjį įrenginį seansui užregistruoti | Nustatykite šią parinktį į *Taip*, jei norite išsaugoti darbuotojo prisijungimų retrospektyvą. Norėdami peržiūrėti žurnalą, eikite į **Darbo vartotojų seansai \> Užklausos ir ataskaitos \> Mobiliojo įrenginio žurnalai \> Darbo vartotojų seansai**. |
| Saugomų klaidų skaičius | Įveskite didžiausią klaidų įrašų, kuriuos sistema turėtų saugoti, skaičių. Norėdami peržiūrėti klaidų žurnalą, eikite į **Darbo vartotojų seansai \> Užklausos ir ataskaitos \> Mobiliojo įrenginio žurnalai \> Darbo vartotojų seansai**. |
| Numatytasis sandėlio perkėlimų žurnalas | Pasirinkite žurnalą, kuris yra naudojamas, kai darbuotojai naudoja mobilųjį įrenginį produktams perkelti iš vieno sandėlio į kitą. |
| Išorės apžvalgos metu leisti registruoti pirkimo užsakymo eilutę | Nustatykite šią parinktį į *Taip*, jei darbuotojai turėtų naudoti mobilųjį įrenginį norėdami užregistruoti eilutes pirkimo užsakymams, kurių **Patvirtinimo būsenos** reikšmė yra *Išorinė peržiūra*. Nustatykite šią parinktį į *Ne*, jei norite neleisti darbuotojams registruoti išorinėje peržiūroje esančių pirkimo užsakymų eilučių. |
| Įjungti RSAT palaikymą | Laukas įgalina „Warehouse Management” mobiliųjų įrenginių programėlės užduočių validatorių, kuris registruoja ir patikrina kiekvieną veiksmą, kurį atlieka programa. Kadangi šis procesas gali labai sulėtinti sistemos našumą, validatorių turėtumėte įgalinti tik tikrinimo metu. Jūs niekada neturėtumėte jo įgalinti gamybos aplinkoje. |
