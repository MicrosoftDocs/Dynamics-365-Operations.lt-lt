---
title: Neatvykimų vadovo vaidmens konfigūravimas
description: Šioje temoje paaiškinama, kaip nustatyti neatvykimų vadovo vaidmenį darbuotojo atostogų valdymui.
author: hasrivas
ms.date: 07/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace, LeaveAbsenceManager
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8a8250b36d2774ac308637253b780592df316cd
ms.sourcegitcommit: 86d38cf57abe768e5bccde48b28280bc2224080c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/19/2021
ms.locfileid: "6639611"
---
# <a name="configure-the-absence-manager-role"></a>Neatvykimų vadovo vaidmens konfigūravimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [preview feature](./includes/preview-feature.md)]

Kai kuriose organizacijose asmenų vadovai gali nevaldyti savo komandos atostogų. Vietoj to, neatvykimų vadovas gali valdyti šį procesą kelių padalinių ir komandų nariams. Neatvykimų vadovai turi šias atostogų valdymo galimybes:

- Peržiūrėti ir patvirtinti išleidimą iš darbo, remiantis alternatyvia hierarchija.
- Peržiūrėti komandos narių balansus.
- Peržiūrėti neatvykimų kalendorių.

## <a name="turn-on-the-feature"></a>Funkcijos įjungimas

1. Darbo srityje **Sistemos administravimas** pasirinkite **Funkcijų valdymas**.

2. Skirtuke **Funkcijų valdymas** įgalinkite **(Peržiūra) Neatvykimų vadovas atostogų valdymui** funkciją.

## <a name="define-a-custom-hierarchy"></a>Pasirinktinės hierarchijos apibrėžimas

Neatvykimų vadovo funkcija naudoja pasirinktinę hierarchiją, kurią reikia sukonfigūruoti.

1. Darbo srityje **Organizacijos administravimas** pasirinkite **Pareigų hierarchijos tipai**.

2. Sukurkite pareigų hierarchijos tipą, pavadintą **Atostogos**.

3. Darbo srities **Atostogos ir neatvykimai** dalyje **Saitai** pasirinkite **Atostogų ir Neatvykimų parametrai**.

4. Skirtuko **Bendra** išplečiamajame sąraše **Neatvykimų hierarchija** pasirinkite anksčiau sukurtą **Atostogų** hierarchijos tipą. Šį Atostogų hierarchijos susiejimą reikia atlikti kiekvienam juridiniam subjektui, kuriame bus naudojama neatvykimų vadovo funkcija.

Kai hierarchijos tipas apibrėžtas, pareigų hierarchijos ataskaita turi būti priskirta pareigoms.

1. Darbo srityje **Organizacijos administravimas** pasirinkite **Visos pareigos**.

2. Pasirinkite pareigas, kurias reikia įtraukti į Atostogų hierarchiją.

3. Skirtuke **Ryšiai** pasirinkite **Įtraukti**.

4. Lauke **Hierarchijos pavadinimas** pasirinkite **Atostogos**.

5. Lauke **Ataskaitos pareigoms** pasirinkite pareigas. Jums pasirinkus pareigas, darbuotojo vardas užpildomas automatiškai.

## <a name="assign-the-absence-manager-role-to-a-user"></a>Neatvykimų vadovo vaidmens priskyrimas vartotojui

Neatvykimų vadovo vaidmuo turi būti priskirtas, kad jis galėtų patvirtinti arba atmesti darbuotojų atostogų užklausas.

1. Darbo srityje **Sistemos administratorius** pasirinkite **Saitai**.

2. Skyriuje **Vartotojai** pasirinkite **Vartotojų** saitą.

3. Iš vartotojų sąrašo pasirinkite vartotoją, kuriam norite priskirti neatvykimų vadovo vaidmenį.

4. Skirtuke **Vartotojo vaidmuo** pasirinkite **Priskirti vaidmenis**.

5. Iš sąrašo pasirinkite **Neatvykimų vadovo** vaidmenį. Tada pasirinkite **Gerai**.

    > [!IMPORTANT]
    > Įsitikinkite, kad darbuotojo vaidmuo taip pat buvo priskirtas vartotojui, kuriam priskiriate neatvykimų vadovo vaidmenį. Kitu atveju darbuotojas negalės naudotis šia funkcija.

6. Sukūrę Atostogų hierarchiją, galite ją peržiūrėti atlikę šiuos veiksmus:

    1. Darbo srityje **Organizacijos Administravimas** pasirinkite **Pareigų hierarchija**.
    
    2. Lauke **Hierarchijos tipas** pasirinkite **Atostogos**.

## <a name="absence-manager-workspace"></a>Neatvykimų vadovo darbo sritis

Darbo srities **Darbuotojo savitarna** skirtuke **Neatvykimų vadovas** rodoma neatvykimų informacija apie darbuotojus, kurie buvo priskirti neatvykimų vadovui Atostogų hierarchijoje.

Skirtuke **Atostogos ir neatvykimai** kiekvienam darbuotojui galimos šios parinktys:

- **Išleidimas iš darbo** – peržiūrėti pasirinkto darbuotojo balansus, patvirtintus išleidimus iš darbo ir išleidimo iš darbo užklausas.
- **Atostogų balansai** – peržiūrėti pasirinkto darbuotojo skirtingų atostogų planų balansų sąrašą.

## <a name="approve-time-off-requests"></a>Laisvo laiko prašymų patvirtinimas

Neatvykimų vadovai gali patvirtinti arba atmesti darbuotojų išleidimo iš darbo užklausas. Jei reikia, jie taip pat gali kurti užklausas darbuotojų vardu.

> [!IMPORTANT]
> Kad neatvykimų vadovai galėtų patvirtinti arba atmesti išleidimo iš darbo užklausas, atostogų užklausų darbo eiga turi būti sukonfigūruota priskirti jiems peržiūrėti atostogų užklausų darbo elementus.
>
> 1. Puslapyje **Personalo darbo eigos** pasirinkite arba sukurkite atostogų užklausos darbo eigą.
> 2. Pasirinkite **Hierarchijos susiejimo** parinktį, o tada **Hierarchijos pavadinimas** lauke pasirinkite **Atostogos**.
> 3. Atnaujinkite darbo eigą darbo eigų dizaino įrankyje. Dalyje **Priskyrimo tipas** pasirinkite **Hierarchijos** parinktį, o tada **Hierarchijos pasirinkimo** skirtuke pasirinkite **Konfigūruojama hierarchija**.
>
> Informacijos apie tai, kaip sukurti atostogų prašymo darbo eigą, rasite [Atostogų užklausos darbo eigos kūrimas](hr-leave-and-absence-workflow.md).

1. Darbo srityje **Darbuotojo savitarna** pasirinkite **Neatvykimų vadovo** skirtuką.

2. Skirtuke **Neatvykimų vadovas** pasirinkite norimą darbuotoją.

3. Pasirinkite **Išsami informacija** ir **Išleidimas iš darbo**.

4. Suraskite išleidimo iš darbo užklausą ir pasirinkite **Patvirtinimo** parinktį. Tada galite pažymėti parinktį patvirtinti arba atšaukti išleidimo iš darbo užklausą.

Būsena **Atšaukta** reiškia, kad užklausa buvo atmesta. Būsena **Atlikta** reiškia, kad užklausa buvo patvirtinta.

## <a name="view-time-off-in-the-calendar"></a>Peržiūrėti išleidimus iš darbo kalendoriuje

Vartotojai, turintys neatvykimų vadovo vaidmenį, gali peržiūrėti išleidimo iš darbo užklausas savo kalendoriuje. Atlikite toliau nurodytus veiksmus, jei norite pasiekti atostogų kalendorių.

> [!IMPORTANT]
> Sistemos administratorius turi sukonfigūruoti neatvykimų vadovo kalendoriaus rodinio parinktis. Puslapio **Atostogų ir neatvykimų parametrai** skirtuke **Kalendorius** yra parinktys slėpti arba rodyti gimtadienius, neatvykimus be informacijos, leistus neatvykimus ir laukiančius atostogų prašymus. Taip pat yra parinktis filtruoti kalendoriaus rodinio parinktį pagal darbuotojo tipą.

1. Darbo srityje **Darbuotojo savitarna** pasirinkite **Neatvykimų vadovas**, o tada **Neatvykimų vadovo kalendorius**.

2. Lauke **Data** įveskite norimas datas.

3. Jei reikia, atnaujinkite rodinio parinktis.

Neatvykimų vadovo kalendoriuje rodomi visi darbuotojų, kurie yra atskaitingi neatvykimų vadovui, įrašai Atostogų hierarchijoje.

## <a name="see-also"></a>Taip pat žiūrėkite

- [Atostogų ir neatvykimų apžvalga](hr-leave-and-absence-overview.md)
- [Prašymo išeiti atostogų darbo eigos kūrimas](hr-leave-and-absence-workflow.md)
- [Komandos ir įmonių kalendorių peržiūra](hr-employee-self-service-calendar.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
