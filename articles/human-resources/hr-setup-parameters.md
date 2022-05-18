---
title: „Human Resources“ parametrų konfigūravimas
description: Šioje temoje aiškinama, kaip nustatyti konkrečius įmonės parametrus programoje „Dynamics 365 Human Resources“.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1fc8ba3f69f216d66850485b6ba33cd324a57156
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689416"
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

Laikotarpis, nustatytas įdarbinimo projekto **s skirstymo** pagal terminus metu, lemia, kurie įdarbinimo projektai įtraukiami į skirstymo pagal terminus **projektų** išklotinę vietą įdarbinimo **valdymo darbo** srityje. Laikotarpis, nustatytas **prašymo** **termino perspėjimui, naudojamas įdarbinimo projektams, kurių prašymo terminas artėja prie jų prašymo termino, parodyti artėjant prie išklotinės dalies įdarbinimo darbo** srityje.

Daugiau informacijos apie įdarbinimą žr. skyriuje [Kandidatų į darbo vietas įdarbinimas](hr-personnel-recruit.md).

## <a name="compensation"></a>Atlyginimo dalis

Programos "Dynamics 365" finansuose skirtuko Kompensacija parametrai nurodo, ar vartotojai turi patvirtinti, **kad** nori įrašyti pastoviosios, ar kintamosios atlyginimo dalies plano informaciją. Jei pasirinksite **Įgalinti tikrinimo įrašymą**, uždarydami su kompensacija susijusį puslapį vartotojai gaus pranešimą, kuriame klausiama, ar jie nori įrašyti įrašą. Kai kuriuose kompensacijos valdymo puslapiuose naudotojai informacijos naikinti negali. Reikalaudami, kad naudotojai patvirtintų, jog jie nori įrašyti informaciją, galėsite riboti informaciją, kuri įrašoma, bet kurios vėliau negalima panaikinti. Jei išdalysite žymės langelį **Aktyvinti įrašymo tvirtinimą**, įrašai išsaugomi iš karto, galimai anksčiau nei tai padaro naudotojas. Jei naudojate našumo valdymą, skirtuke **Kompensacija** taip pat galite pasirinkti vertinimo modelį, kuris bus naudojamas vietoje modelio, vertinant našumą priskirto kompensavimo planams.

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

Skirtuke Darbuotojų savitarnos **parametrai veikia** tai, kaip **darbuotojų savitarnos paslauga** rodoma darbuotojams. Šiame skirtuke galite atlikti šias užduotis:

- Įveskite darbuotojų savitarnos **darbo srities** pavadinimą
- pasirinkti, kurią informaciją vadovas gali įvesti darbuotojams,
- pridėti naudingų nuorodų darbuotojams,
- apriboti leidimus darbuotojams pridėti ar redaguoti įmonės kontaktinius duomenis. Daugiau informacijos žr. skyriuje [Asmens informacijos redagavimo apribojimas](hr-employee-self-service-restrict-editing.md).

Norėdami gauti daugiau informacijos apie darbuotojų savitarnos paslaugos **nustatyti, žr**. Darbuotojų [ir vadybininko savitarnos paslaugos peržiūrą](hr-employee-manager-self-service-overview.md).

![Darbuotojų savitarnos skirtukas.](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Vadovų savitarna

Skirtuko Vadybininko **savitarnos parametrai daro įtaką** tai, ką vadybininkai matys vadybininko **savitarnoje**. Šiame skirtuke galima konfigūruoti šias parinktis:

- Įrašų, kurių galiojimas baigiasi, diapazonas
- Informaciją, kurią vadovai gali peržiūrėti įrašų su besibaigiančiu galiojimu srityje
- Ar vadovai gali peržiūrėti atviras pareigas išplėstinėms ataskaitoms
- Esamų darbuotojų rodiniai
- Naudingos nuorodos vadovams

Norėdami gauti daugiau informacijos apie tai, kaip nustatyti vadybininko **savitarnos paslaugas**, žr. Darbuotojų [ir vadybininko savitarnos peržiūrą](hr-employee-manager-self-service-overview.md).

![Vadovo savitarnos skirtukas.](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Išmokų valdymas

Skirtuke **Išmokų valdymas galite** konfigūruoti išmokų valdymo el. pašto pasirinktis. Norėdami gauti informacijos apie tai, kaip nustatyti ir naudoti Išmokų valdymą, žr. [Išmokų valdymo apžvalgą](hr-benefits-management-overview.md).

![Išmokų valdymo skirtukas.](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Atostogos ir neatvykimai

Daugiau informacijos apie atostogų ir neatvykimo nustatymą ir naudojimą žr. skyriuje [Atostogų ir neatvykimo apžvalga](hr-leave-and-absence-overview.md).

## <a name="payment-methods"></a>Mokėjimo būdai

Skirtuke **Mokėjimo būdai** galima pasirinkti jūsų įmonės palaikomus mokėjimo būdus. Daugiau informacijos apie kompensacijos konfigūravimą žr. skyriuje [Kompensacijų planų apžvalga](hr-compensation-overview.md).

![Mokėjimo būdų skirtukas.](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
