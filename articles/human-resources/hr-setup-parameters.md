---
title: „Human Resources“ parametrų konfigūravimas
description: Šioje temoje aiškinama, kaip nustatyti konkrečius įmonės parametrus programoje „Dynamics 365 Human Resources“.
author: andreabichsel
ms.date: 06/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 24d30aa06805b530cc069be0517279a11dff9ed4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356541"
---
# <a name="configure-human-resources-parameters"></a>„Human Resources“ parametrų konfigūravimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kai kurie žmogiškųjų išteklių parametrai naudojami keliose įmonėse, o kiti – konkrečioje įmonėje. Šioje temoje aiškinama, kaip nustatyti konkrečius įmonės personalo parametrus.

Personalo parametrams nustatyti naudojami du puslapiai. Jei parametrai yra bendrai naudojami keliose įmonėse, galite naudoti puslapį **Bendrai naudojami žmogiškųjų išteklių parametrai**. Jei parametrai skirti konkrečiai įmonei (kitaip tariant, parametrai taikomi prie vienai įmonei), naudokite puslapį **Personalo parametrai**.

![Eikite į personalo parametrus.](./media/hr-employee-self-service-human-resources-parameters.png)

Puslapyje **Personalo parametrai** parametrai suskirstyti į šešis toliau pateiktus skirtukus.

- **Bendri**
- **Įdarbinimas** (šio skirtuko „Dynamics 365 Human Resources“ nėra)
- **Kompensacija**
- **Numeracija**
- **FMLA**
- **Darbuotojų savitarna**
- **Vadovų savitarna**
- **Išmokų valdymas**
- **Atostogos ir neatvykimai**
- **Mokėjimo būdai**

Kiekviename skirtuke yra informacijos, susijusios su viena įmone.

## <a name="general"></a>Bendri

Skirtuko **Bendra** parametrai apibrėžia informacijos apie neatvykimą, sužalojimus ir ligas bei naujus darbuotojus, rodymą. Šio skirtuko parametrai taip pat nustato kai kuriuos numatytuosius įrašus, rodomus, kai dirbate. Tiksliau šiame skirtuke galima:

- Pasirinkti spalvą, kurią taikysite atidarytoms neatvykimo operacijoms.
- Nurodyti ataskaitoms naudotiną stilių aprašą.
- Įgalinti integravimą tarp mokymo kursų ir neatvykimų registravimo.
- pasirinkti neatvykimo kodą, naudojamą šiam integravimui valdyti,
- nurodyti, ar ilgai laikyti sužalojimo ir ligos atvejų incidentus,
- nurodyti numatytąjį identifikavimo numerį, rodomą pasamdžius naują darbuotoją.
- Nurodykite datą, naudojamą darbo stažo apskaičiavimui. 

![Skirtukas Bendra.](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Įdarbinimas

Skirtuko **Įdarbinimas** parametrai apibrėžia dokumentų tipus, naudojamus pretendentams siunčiamai korespondencijai. Taip pat galima nurodyti įdarbinimo projektą, naudojamą neprašytoms paraiškoms.

Nurodytas skirstymo pagal terminus laikotarpis nustato įdarbinimo projektus, įtrauktus į išklotinę **Suskirstyti pagal terminus projektai**, esančią darbo srityje **Įdarbinimo valdymas**. Nurodytas prašymo pateikimo termino įspėjimo laikotarpis yra naudojamas įdarbinimo projektams, kurių prašymo pateikimo terminas artėja, rodyti išklotinėje **Prašymo pateikimo terminas artėja**, esančioje darbo srityje **Įdarbinimas**.

Daugiau informacijos apie įdarbinimą žr. skyriuje [Kandidatų į darbo vietas įdarbinimas](hr-personnel-recruit.md).

## <a name="compensation"></a>Kompensacija

Programoje „Dynamics 365 Finance“ skirtuko **Kompensacija** nustatymai apibrėžia, ar naudotojai turi patvirtinti, kad nori išsaugoti informaciją fiksuotosios arba kintamosios atlyginimo dalies plane. Jei pasirinksite **Įgalinti tikrinimo įrašymą**, uždarydami su kompensacija susijusį puslapį vartotojai gaus pranešimą, kuriame klausiama, ar jie nori įrašyti įrašą. Kai kuriuose kompensacijos valdymo puslapiuose naudotojai informacijos naikinti negali. Reikalaudami, kad naudotojai patvirtintų, jog jie nori įrašyti informaciją, galėsite riboti informaciją, kuri įrašoma, bet kurios vėliau negalima panaikinti. Jei išdalysite žymės langelį **Aktyvinti įrašymo tvirtinimą**, įrašai išsaugomi iš karto, galimai anksčiau nei tai padaro naudotojas. Jei naudojate našumo valdymą, skirtuke **Kompensacija** taip pat galite pasirinkti vertinimo modelį, kuris bus naudojamas vietoje modelio, vertinant našumą priskirto kompensavimo planams.

Personalo dalyje naudodami skirtuką **Kompensacija** galite pasirinkti apriboti prieigą prie kompensacijos planų ir nustatyti numatytąją valiutą.

Daugiau informacijos apie kompensaciją žr. skyriuje [Kompensacijų planų apžvalga](hr-compensation-overview.md).

![Atlyginimo skirtukas.](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a>Numeracija

Nustatymai skirtuke **Numerių seka** apibrėžia sekas, naudojama automatiniam ID priskyrimui personalo prekėms, pvz.:

- Prašymai
- Neatvykimo registracijos
- Kompensavimo proceso rezultatai
- Atvejų numeriai
- Kursai
- Kurso darbotvarkės

Norėdami prižiūrėti numeracijų nuorodas ir kodus, naudokite **Numeracijos** sąrašo puslapį (pasirinkite **Organizacijos administravimas > Numeracijos > Numeracijos**).

Daugiau informacijos žr. skyriuje [Numeracijos apžvalga](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

> [!NOTE]
> Išdirbtų valandų skaičius negali viršyti 1 250, o įdarbinimo trukmė negali viršyti 12 mėnesių. Šios didžiausios galimos reikšmės atitinka Jungtinių Amerikos Valstijų federalinę teisę.

![Numeracijų skirtukas.](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

Skirtuke FMLA nustatote FMLA tinkamumo reikalavimus ir FMLA atostogų valandas. Dėl daugiau informacijos, žr. [Konfigūruoti atostogų ir nebuvimo parametrus](hr-leave-and-absence-parameters.md).

![FMLA skirtukas.](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Darbuotojų savitarna

Skirtuko **Darbuotojo savitarna** nustatymai veikia tai, kaip darbuotojo savitarnos paslauga rodoma darbuotojams. Šiame skirtuke galima:

- keisti darbuotojo savitarnos darbo srities pavadinimą,
- pasirinkti, kurią informaciją vadovas gali įvesti darbuotojams,
- pridėti naudingų nuorodų darbuotojams,
- apriboti leidimus darbuotojams pridėti ar redaguoti įmonės kontaktinius duomenis. Daugiau informacijos žr. skyriuje [Asmens informacijos redagavimo apribojimas](hr-employee-self-service-restrict-editing.md).

Daugiau informacijos apie tai, kaip nustatyti darbuotojo savitarną, žr. skyriuje [Darbuotojo ir vadovo savitarnos apžvalga](hr-employee-manager-self-service-overview.md).

![Darbuotojų savitarnos skirtukas.](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Vadovų savitarna

Skirtuko **Vadovo savitarna** nustatymai daro įtaką tam, ką vadovai mato savo vadovo savitarnoje. Šiame skirtuke galima konfigūruoti šias parinktis:

- Įrašų, kurių galiojimas baigiasi, diapazonas
- Informaciją, kurią vadovai gali peržiūrėti įrašų su besibaigiančiu galiojimu srityje
- Ar vadovai gali peržiūrėti atviras pareigas išplėstinėms ataskaitoms
- Esamų darbuotojų rodiniai
- Naudingos nuorodos vadovams

Daugiau informacijos apie tai, kaip nustatyti vadovo savitarną, žr. skyriuje [Darbuotojo ir vadovo savitarnos apžvalga](hr-employee-manager-self-service-overview.md).

![Vadovo savitarnos skirtukas.](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Išmokų valdymas

Išmokų valdymo skirtuke galima konfigūruoti el. pašto parinktis išmokų valdymui. Informacijos apie tai, kaip nustatyti ir naudoti išmokų valdymą, žr. skyriuje [Išmokų valdymo apžvalga](hr-benefits-management-overview.md).

![Išmokų valdymo skirtukas.](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Atostogos ir neatvykimai

Daugiau informacijos apie atostogų ir neatvykimo nustatymą ir naudojimą žr. skyriuje [Atostogų ir neatvykimo apžvalga](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Mokėjimo būdai

Skirtuke **Mokėjimo būdai** galima pasirinkti jūsų įmonės palaikomus mokėjimo būdus. Daugiau informacijos apie kompensacijos konfigūravimą žr. skyriuje [Kompensacijų planų apžvalga](hr-compensation-overview.md).

![Mokėjimo būdų skirtukas.](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
