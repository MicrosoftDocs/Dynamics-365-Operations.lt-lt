---
title: Atostogų ir neatvykimų tipų konfigūravimas
description: Darbuotojams skiriamų atostogų tipų nustatymas „Dynamics 365 Human Resources“.
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df6e34fe6a23e6f0a8307a035752a35a15a3431c
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198055"
---
# <a name="configure-leave-and-absence-types"></a>Atostogų ir neatvykimų tipų konfigūravimas

Atostogų tipai programoje „Dynamics 365 Human Resources“ apibrėžia neatvykimų, kuriuos gali nurodyti darbuotojai, tipus. Galite pritaikyti atostogų tipus atsižvelgdami į savo organizacijos poreikius. Atostogų tipų pavyzdžiai:

- Apmokamos atostogos (PTO)
- Neapmokamos atostogos
- Apmokėtos atostogos
- Nedarbingumo atostogos
- Nedarbingumo atostogos
- Šeimos atostogos
- Trumpalaikė negalia
- Netekties atostogos

## <a name="add-a-leave-type"></a>Įtraukti atostogų tipą

1. Puslapyje **Atostogos ir neatvykimai** pasirinkite skirtuką **Saitai**.

2. Dalyje **Sąranka**pasirinkite **Atostogų ir neatvykimų tipai**.

3. Pasirinkite **Naujas**.

4. Įveskite atostogų tipo pavadinimą dalyje **Tipas**, pasirinkite darbo eigą dalyje **Darbo eigos ID** ir įveskite aprašą dalyje **Aprašas**.

5. Dalies **Bendra** išplečiamajame sąraše **Kategorija** pasirinkite **Nėra**, **Suplanuota** arba **Nesuplanuota**.

6. Išplečiamajame sąraše **Pajamų kodas** pasirinkite pajamų kodą.

7. Dalyje **Būtina nurodyti priežasties kodą** pasirinkite, ar norite, kad būtų būtina nurodyti priežasties kodą. Jeigu norite, kad būtų būtina nurodyti priežasčių kodus, galbūt jums reikės juos pridėti. Dalyje **Priežasčių kodai** pasirinkite **Pridėti**, pasirinkite priežasties kodą, tada pasirinkite prie jo esantį žymės langelį **Įgalinta**.

8. Dalyje **Riboti prieigą prie pasirinktų vaidmenų** pasirinkite, ar norite riboti prieigą. Tada pasirinkite saugos vaidmenis dalyje **Šio atostogų tipo saugos vaidmenys**. Saugos vaidmenys nustatyti darbo eigoje, kurią pasirinkote dalyje **Darbo eigos ID** anksčiau šios procedūros metu.

9. Pasirinkite **Įrašyti**.

## <a name="configure-leave-type-rules"></a>Atostogų tipo taisyklių konfigūravimas

1. Atostogų tipo apvalinimo parinkčių nustatymas. Parinktys yra tokios: **Nėra**, **Į didesnę reikšmę**, **Į mažesnę reikšmę** ir **Į artimiausią reikšmę**. Taip pat galite nustatyti atostogų tipo apvalinimo tikslumą.

2. Atostogų tipo lauko **Šventinių dienų koregavimas** nustatymas. Pasirinkus šią parinktį, „Human Resources“ naudoja šventinių dienų, kurios būna darbo dienomis, skaičių, kad nustatytų, kaip kaupti atostogas šiam atostogų tipui. Pavyzdžiui, jei Kalėdos yra pirmadienį, „Human Resources“ atims vieną dieną iš atostogų tipo, kai apdoros kaupimus.

   Nustatote šventine dienas darbo laiko kalendoriuje. Daugiau informacijos žr. skyriuje [Darbo laiko kalendoriaus kūrimas](hr-leave-and-absence-working-time-calendar.md)
   
## <a name="configure-preview-features"></a>Peržiūros funkcijų konfigūravimas

Jeigu įgalinote atostogų ir neatvykimų peržiūros funkcijas, jums reikės konfigūruoti ir jų parametrus.

[!include [banner](includes/preview-feature-leave-absence.md)]

1. Pasirinkite atostogų tipą, į kurį bus perkeliami perkėlimo balansai. Taip pat galite sukurti naują atostogų tipą, skirtą perkėlimui. 

## <a name="see-also"></a>Taip pat žiūrėkite

- [Atostogų ir neatvykimų apžvalga](hr-leave-and-absence-overview.md)
- [Atostogų ir neatvykimų plano kūrimas](hr-leave-and-absence-plans.md)
- [Darbo laiko kalendoriaus kūrimas](hr-leave-and-absence-working-time-calendar.md)
