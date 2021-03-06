---
title: Atostogų ir neatvykimų tipų konfigūravimas
description: Darbuotojams skiriamų atostogų tipų nustatymas „Dynamics 365 Human Resources“.
author: andreabichsel
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39e4c4b9c83ca648c21ac20bd20b739af8a6b9ed
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271132"
---
# <a name="configure-leave-and-absence-types"></a>Atostogų ir neatvykimų tipų konfigūravimas

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

2. Dalyje **Sąranka** pasirinkite **Atostogų ir neatvykimų tipai**.

3. Pasirinkite **Naujas**.

4. Įveskite atostogų tipo pavadinimą dalyje **Tipas**, pasirinkite darbo eigą dalyje **Darbo eigos ID** ir įveskite aprašą dalyje **Aprašas**.

5. Dalies **Bendra** išplečiamajame sąraše **Kategorija** pasirinkite **Nėra**, **Suplanuota** arba **Nesuplanuota**.

6. Išplečiamajame sąraše **Pajamų kodas** pasirinkite pajamų kodą.

7. Dalyje **Būtina nurodyti priežasties kodą** pasirinkite, ar norite, kad būtų būtina nurodyti priežasties kodą. Jeigu norite, kad būtų būtina nurodyti priežasčių kodus, galbūt jums reikės juos pridėti. Dalyje **Priežasčių kodai** pasirinkite **Pridėti**, pasirinkite priežasties kodą, tada pasirinkite prie jo esantį žymės langelį **Įgalinta**.

8. Dalyje **Riboti prieigą prie pasirinktų vaidmenų** pasirinkite, ar norite riboti prieigą. Tada pasirinkite saugos vaidmenis dalyje **Šio atostogų tipo saugos vaidmenys**. Saugos vaidmenys nustatyti darbo eigoje, kurią pasirinkote dalyje **Darbo eigos ID** anksčiau šios procedūros metu.

9. Srityje **Kalendoriaus spalva** pasirinkite, kokia spalva bus naudojama šiam atostogų tipui atostogų ir neatvykimų kalendoriuose. 

10. Dalyje **Suspendavimo ryšiai** pasirinkite, ar norite, kad šis atostogų tipas suspenduotų kitą atostogų tipą, ar jį suspenduotų kitas atostogų tipas. Kai atostogų prašymas bus pateiktas suspendavimo atostogų tipui, jam bus automatiškai sukurtos suspendavimo atostogos. 

10. Pasirinkite **Įrašyti**.

## <a name="configure-leave-type-rules"></a>Atostogų tipo taisyklių konfigūravimas

1. Atostogų tipo apvalinimo parinkčių nustatymas. Parinktys yra tokios: **Nėra**, **Į didesnę reikšmę**, **Į mažesnę reikšmę** ir **Į artimiausią reikšmę**. Taip pat galite nustatyti atostogų tipo apvalinimo tikslumą.

2. Atostogų tipo lauko **Šventinių dienų koregavimas** nustatymas. Pasirinkus šią parinktį, „Human Resources“ naudoja šventinių dienų, kurios būna darbo dienomis, skaičių, kad nustatytų, kaip kaupti atostogas šiam atostogų tipui. Pavyzdžiui, jei Kalėdos yra pirmadienį, „Human Resources“ atims vieną dieną iš atostogų tipo, kai apdoros kaupimus.

   Nustatote šventine dienas darbo laiko kalendoriuje. Daugiau informacijos žr. skyriuje [Darbo laiko kalendoriaus kūrimas](hr-leave-and-absence-working-time-calendar.md)
   
 3. Nustatykite **Perkeliamų atostogų tipą** atostogų tipui. Pasirinkus šią parinktį, visi perkeliami likučiai bus perkelti į nurodytą atostogų tipą. Perkeliamų atostogų tipas taip pat turi būti nurodytas atostogų plane. 
 
4. Apibrėžkite **Galiojimo taisykles** atostogų tipui. Konfigūruodami šią parinktį, galite pasirinkti dienų ar mėnesių vienetą ir nustatyti galiojimo trukmę. Galiojimo taisyklės įsigaliojimo data naudojama norint nustatyti, kada pradėti paketinę užduotį, kuri apdoroja atostogų galiojimo pabaigą arba datą, kada įsigalioja taisyklė. Galiojimo laiko pabaiga visada bus kaupimo laikotarpio pradžios data. Pavyzdžiui, jei kaupimo laikotarpio pradžios data yra 2021 m. rugpjūčio 3 d., o galiojimo taisyklė buvo nustatyta 6 mėnesiams, taisyklė bus apdorota remiantis galiojimo poslinkiu iš kaupimo laikotarpio pradžios datos, todėl ji bus vykdoma 2022 m. vasario 3 d. Visi galiojimo pabaigos metu esantys atostogų likučiai bus atimami iš atostogų tipo ir bus įtraukti į atostogų likutį.
 
## <a name="see-also"></a>Taip pat žiūrėkite

- [Atostogų ir neatvykimų apžvalga](hr-leave-and-absence-overview.md)
- [Atostogų ir neatvykimų plano kūrimas](hr-leave-and-absence-plans.md)
- [Darbo laiko kalendoriaus kūrimas](hr-leave-and-absence-working-time-calendar.md)
- [Atostogų sustabdymas](hr-leave-and-absence-suspend-leave.md)
- [Sukurkite darbo eigą atostogų pirkimo ir pardavimo užklausai](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
