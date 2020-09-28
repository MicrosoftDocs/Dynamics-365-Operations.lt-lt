---
title: Projektų išteklių nustatymas
description: Šioje temoje pateikiama informacija apie projekto išteklių nustatymą arba prašymą.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760618"
---
# <a name="set-up-project-resources"></a>Projektų išteklių nustatymas

[!include [banner](../includes/banner.md)]

Turite nustatyti kalendorių ir jį susieti su darbuotoju. Kalendorius naudojamas projektui planuoti ir projektui rezervuotų išteklių darbo laikui. Nustatydami kalendorių ir optimizuodami išteklius projektų vadovai gali koreguoti išteklių paskirstymą. Atsižvelgiant į kalendoriaus grafiką, ištekliams gali būti taikomi apribojimai. Puslapyje **Kalendoriai** galite nustatyti kalendorių.

Kai darbuotoją nustatote kaip projekto išteklių, galite pasirinkti iš įmonėje, kuriai nustatote išteklius, dirbančių darbuotojų. Taip pat galite pasirinkti iš kitų savo organizacijos įmonių darbuotojų. Šie darbuotojai vadinami vidiniais įmonės ištekliais.

Toliau nurodytose procedūrose paaiškinama, kaip savo įmonėje nustatyti darbuotoją kaip projekto išteklių ir kaip nustatyti vidinį įmonės projekto išteklių.

## <a name="set-up-a-worker-as-a-project-resource"></a>Darbuotojo nustatymas projekto ištekliumi

1. Puslapio **Darbuotojai** sąraše **Darbuotojai** pasirinkite darbuotoją, kurį pridedate kaip projekto išteklių, ir atidarykite darbuotojo įrašą.
2. Veiksmų srityje pasirinkite **Projektas** &gt; **Sąranka** &gt; **Projekto sąranka**.
3. Pasirinkite kalendorių ir uždarykite puslapį.

Kaip išankstinio priskyrimo tipą taip pat galite nurodyti numatytuosius ištekliaus projektus. Išankstiniai priskyrimai gali būti naudojami, kai išteklių vadovas ar projekto vadovas iš anksto žino, su kuriais projektais dirbs išteklius. Išankstiniai priskyrimai taip pat gali būti paremti projekto rėmėjo ar kliento prašymu. Norėdami iš anskto priskirti projektą, puslapyje **Priskirti projektus**, skirtuke **Projektai**, sąraše **Likę projektai** pasirinkite atitinkamą projektą.

## <a name="set-up-an-intercompany-resource"></a>Vidinių įmonės išteklių nustatymas

Kai nustatote darbuotoją kaip vidinį įmonės išteklių, turite užbaigti sąranką tiek skolinančioje įmonėje, tiek besiskolinančioje įmonėje.

### <a name="in-the-lending-company"></a>Skolinančioje įmonėje

1. Jei naudojate „Finance“, patikrinkite, ar pasirinkta skolinanti įmonė, o po to atlikite ankstesniame skyriuje nurodytą procedūrą „Darbuotojo nustatymas projekto ištekliumi“.
2. Puslapyje **Įmonės vidaus apskaita** pasirinkite **Naujas**.
3. Lauke **Juridinio subjekto ID** pasirinkite skolinančią įmonę. Atitinkamai užpildykite likusius laukus ir pasirinkite **Įrašyti**.
4. Puslapyje **Perkėlimo kaina** pasirinkite **Naujas**.
5. Lauke **Besiskolinantis juridinis subjektas** pasirinkite atitinkamą įmonę.
6. Norėdami besiskolinančiai įmonei paskolinti tik tą išteklių, kurį sukūrėte šio skyriaus pradžioje, lauke **Išteklius** pasirinkite sukurto ištekliaus pavadinimą. Norėdami, kad besiskolinančiai įmonei būtų prieinami visi ištekliai, lauką **Išteklius** palikite tuščią.
7. Puslapio **Projektų valdymo ir apskaitos parametrai** skirtuke **Vidinė įmonė** parinktį **Įjungti vidinės įmonės išteklių planavimą ir tabelius** nustatykite kaip **Taip**.

### <a name="in-the-borrowing-company"></a>Besiskolinančioje įmonėje

- Puslapyje **Išteklių sąrašas**, ieškos filtre įveskite sukurto skolinančiai įmonei skirto ištekliaus pavadinimą, kad patikrintumėte, ar pavadinimas įtrauktas į besiskolinančiai įmonei skirtą išteklių sąrašą.

## <a name="request-project-resources"></a>Projektų išteklių prašymas
Projektų išteklių planavimo funkcija gali naudotis tik išteklių vadovai, norėdami platinti personalo išteklius įsipareigojimuose arba projektuose. Norėdami įjungti šią funkciją, atlikite toliau nurodytas užduotis arba patvirtinkite, kad jos atliktos.

- Nustatyti numeracijas.
- Nustatyti projektų valdymo ir apskaitos darbo eigas.
- Įjunkite išteklių užklausų darbo eigas.

Atlikę pirmiau nurodytas užduotis, galite atlikti reikiamas kitas užduotis.

- Sukurkite išteklių užklausą iš apytiksliai suplanuotų personalo išteklių.
- Stebėti išteklių užklausas.
- Vykdyti išteklių užklausas.
- Pateikti personalo ištekliaus iš WBS užklausą.
- Užregistruokite išteklius projektui nepateikdami personalo išteklių užklausos.
