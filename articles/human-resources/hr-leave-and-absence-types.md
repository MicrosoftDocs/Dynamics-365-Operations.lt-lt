---
title: Atostogų ir neatvykimų tipų konfigūravimas
description: Darbuotojams skiriamų atostogų tipų nustatymas „Dynamics 365 Human Resources“.
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e35c5fed886ebf9a453c22b3e04ca9ffe50b6d70
ms.sourcegitcommit: e88ecaccd82afa3a915e41df1d4287d99da6a48a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/29/2022
ms.locfileid: "9805210"
---
# <a name="configure-leave-and-absence-types"></a>Atostogų ir neatvykimų tipų konfigūravimas

[!include [preview banner](../includes/preview-banner.md)]

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

1. Atostogų ir **neatvykimo darbo** srityje pasirinkite skirtuką **Saitai** .
2. Dalyje **Sąranka** pasirinkite **Atostogų ir neatvykimų tipai**.
3. Pasirinkite **Nauja**.
4. Įveskite atostogų tipo pavadinimą dalyje Tipas **, įveskite** aprašymą dalyje **Aprašymas ir** darbo eigą pasirinkite darbo **eigos ID** lauke. Pagal atostogų tipą pasirinkite užklausos tipą lauke **Užklausos** tipas. Pavyzdžiui, pasirinkite Atostogų **laikas**  **arba Atostogos**.
5. Dalies **Bendra** išplečiamajame sąraše **Kategorija** pasirinkite **Nėra**, **Suplanuota** arba **Nesuplanuota**.
6. Išplečiamajame sąraše **Pajamų kodas** pasirinkite pajamų kodą.
7. Pasirinkite **, ar norite** reikalauti priežasties kodo, dalyje Priežasties kodas. Jei norite reikalauti priežasties kodų, gali tekti juos įtraukti. Dalyje **Priežasčių kodai** pasirinkite **Pridėti**, pasirinkite priežasties kodą, tada pasirinkite prie jo esantį žymės langelį **Įgalinta**.
8. Jei užklausos tipas yra Atostogų **laikas**, atlikite šiuos veiksmus:

      1. Dalyje **Atidaryta** baigta pasirinkite, ar vartotojai gali kurti atvirus lapus.
      2. Jei **įgalintas** atviras laikas, galite pasirinkti, ar grįžtant iš neatvykimo darbuotojai turi pateikti pranešimą apie grąžinimą į darbą.
      3. Jei darbuotojai turi pateikti pranešimą dėl grąžinimo į darbą, galite įgalinti įgalinti grąžinimą **į darbo įspėjimą**. Įgalinus **grąžinimo į darbą pranešimą**, automatiškai **įgalinamas** priedas ir jo negalima išjungti.

9. Jei vartotojai turėtų įkelti dokumentus, kai jie kuria ar atnaujina atostogų užklausas, galite įgalinti **priedą**.
10. Dalyje **Apriboti prieigą prie pasirinktų vaidmenų** pasirinkite, ar norite apriboti prieigą. Tada šio **atostogų tipo saugos vaidmenyse** pasirinkite saugos vaidmenis. Saugos vaidmenys nustatomi darbo eigoje, kurią pasirinkote anksčiau šios **procedūros darbo eigos ID** .
11. Dalyje **Kalendoriaus** spalva pasirinkite spalvą, kuri bus rodoma šio tipo atostogų atostogų ir neatvykimo kalendoriuose.
11. Dalyje **Sustabdymo ryšiai** pasirinkite, ar šis atostogų tipas turėtų sulaikyti kitą atostogų tipą, ar jį sustabdė kitas atostogų tipas. Kai atostogų prašymas bus pateiktas suspendavimo atostogų tipui, jam bus automatiškai sukurtos suspendavimo atostogos.
12. Pasirinkite **Įrašyti**.

## <a name="configure-leave-type-rules"></a>Atostogų tipo taisyklių konfigūravimas

1. Nustatyti apvalinimo pasirinktis atostogų **ir neatvykimų tipui** . Parinktys yra tokios: **Nėra**, **Į didesnę reikšmę**, **Į mažesnę reikšmę** ir **Į artimiausią reikšmę**. Taip pat galite nustatyti atostogų tipo apvalinimo tikslumą.
2. Atostogų tipo lauko **Šventinių dienų koregavimas** nustatymas. Pasirinkus šią parinktį, bus naudojamas šventinių dienų, kurios būna darbo dienomis, skaičius, kad nustatytų, kaip kaupti atostogas šiam atostogų tipui. Pavyzdžiui, jei Kalėdos yra pirmadienį, „Human Resources“ atims vieną dieną iš atostogų tipo, kai apdoros kaupimus.

   Nustatote šventine dienas darbo laiko kalendoriuje. Daugiau informacijos rasite [Darbo laiko kalendoriaus kūrimas](hr-leave-and-absence-working-time-calendar.md).
   
 3. Nustatykite **Perkeliamų atostogų tipą** atostogų tipui. Pasirinkus šią parinktį, visi perkeliami likučiai bus perkelti į nurodytą atostogų tipą. Perkeliamų atostogų tipas taip pat turi būti nurodytas atostogų plane. 
 
4. Apibrėžkite **Galiojimo taisykles** atostogų tipui. Konfigūruodami šią parinktį, galite pasirinkti dienų ar mėnesių vienetą ir nustatyti galiojimo trukmę. Galiojimo taisyklės įsigaliojimo data naudojama norint nustatyti, kada pradėti paketinę užduotį, kuri apdoroja atostogų galiojimo pabaigą arba datą, kada įsigalioja taisyklė. Galiojimo laiko pabaiga visada bus kaupimo laikotarpio pradžios data. Pavyzdžiui, jei kaupimo laikotarpio pradžios data yra 2021 m. rugpjūčio 3 d., o galiojimo taisyklė buvo nustatyta 6 mėnesiams, taisyklė bus apdorota remiantis galiojimo poslinkiu iš kaupimo laikotarpio pradžios datos, todėl ji bus vykdoma 2022 m. vasario 3 d. Visi galiojimo pabaigos metu esantys atostogų likučiai bus atimami iš atostogų tipo ir bus įtraukti į atostogų likutį.
 
## <a name="configure-the-required-attachment-per-leave-type"></a>Konfigūruoti reikalingą priedą atostogų tipui

> [!NOTE]
> Norėdami naudoti **Reikiamo priedo** lauką, pirmiausia turite įjungti funkciją **Konfigūruoti reikiamą atostogų užklausų priedą** Funkcijų valdyme. Daugiau informacijos apie tai, kaip įjungti funkcijas, rasite [Funkcijų valdymas](hr-admin-manage-features.md).

1. Puslapio **Atostogos ir neatvykimai** skirtuko **Saitai** dalyje **Nustatymas** pasirinkite **Atostogų ir neatvykimų tipai**.

2. Sąraše pasirinkite **atostogų ir** neatvykimo tipą. Bendrajame **skyriuje** naudokite lauką Priedas, kuris būtinas norint nurodyti, **ar** priedas turi būti įkeltas, kai darbuotojas pateikia naują atostogų užklausą pagal pasirinktą atostogų tipą. 

Darbuotojai turės įkelti priedą, kai pateiks naują atostogų užklausą, kurios atostogų tipui įgalintas **Reikalaujamas priedas** laukas. Norėdami peržiūrėti priedą, kuris buvo įkeltas kaip atostogų užklausos dalis, atostogų užklausų tvirtintojai gali naudoti **Priedų** parinktį jiems priskirtiems darbo elementams. Jei atostogų užklausą galima pasiekti naudojant „Microsoft Teams” Personalo programą, parinktis **Peržiūrėti informaciją** gali būti naudojama peržiūrėti atostogų užklausos informacijai ir priedams.

## <a name="configure-leave-units-hoursdays-per-leave-type"></a>Konfigūruoti atostogų vienetus (valandos/dienos) kiekvienam atostogų tipui

> [!NOTE]
> Norėdami naudoti atostogų vienetų atostogų tipui funkciją, pirmiausia turite įjungti funkciją **Konfigūruoti atostogų vienetus atostogų tipui** Funkcijų valdyme. Daugiau informacijos apie tai, kaip įjungti funkcijas, rasite [Funkcijų valdymas](hr-admin-manage-features.md).

> [!IMPORTANT]
> Pagal numatytuosius nustatymus, juridinio subjekto atostogų tipai naudoja atostogų vienetus iš atostogų parametrų konfigūravimo juridinio subjekto lygiu.
> 
> Atostogų ir neatvykimų tipo atostogų vienetą galima modifikuoti tik tada, jei nėra jokių to atostogų tipo atostogų operacijų.
> 
> Funkcijos išjungti negalima po to, kai ji buvo įjungta.

1. Puslapio **Atostogos ir neatvykimai** skirtuko **Saitai** dalyje **Nustatymas** pasirinkite **Atostogų ir neatvykimų tipai**.

2. Iš sąrašo pasirinkite atostogų ir neatvykimo tipą. Tada skyriaus **Bendra** lauke **Vienetas** pasirinkite atostogų vienetą. Galite pasirinkti **Valandos** arba **Dienos**.

3. Pasirinktinai: jei lauke **Vienetas** pasirinkote **Valandos**, galite naudoti lauką **Įgalinti pusės dienos apibrėžimą**, kad nurodytumėte, ar darbuotojai gali pasirinkti pirmą ar antrą dienos pusę, jei jie prašo išleidimo iš darbo pusei dienos.

Darbuotojai, kurie pateikia naują atostogų užklausą, gali pasirinkti skirtingus atostogų tipus, sudarančius jų atostogų užklausą. Tačiau visi atostogų tipai, pasirinkti kaip vienos atostogų užklausos dalis, turi turėti tą patį atostogų vienetą. Darbuotojai gali peržiūrėti kiekvieno atostogų tipo atostogų vienetą **Prašyti išleidimo iš darbo** formoje.

## <a name="see-also"></a>Taip pat žiūrėkite

- [Atostogų ir neatvykimų apžvalga](hr-leave-and-absence-overview.md)
- [Atostogų ir neatvykimų plano kūrimas](hr-leave-and-absence-plans.md)
- [Darbo laiko kalendoriaus kūrimas](hr-leave-and-absence-working-time-calendar.md)
- [Atostogų sustabdymas](hr-leave-and-absence-suspend-leave.md)
- [Sukurkite darbo eigą atostogų pirkimo ir pardavimo užklausai](hr-leave-and-absence-buy-sell-workflow.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
