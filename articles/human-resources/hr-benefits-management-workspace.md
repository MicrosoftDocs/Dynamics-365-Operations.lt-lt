---
title: Išmokų valdymo darbo sritis
description: Šiame straipsnyje aprašoma išmokų valdymo darbo sritis, esančią Dynamics 365 Human Resources.
author: twheeloc
ms.date: 01/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-24
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 975b620dc911d154f6f67420a957bd72c02321ed
ms.sourcegitcommit: 6b013a423ed91973d60a895330046db2a07d92c4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/12/2022
ms.locfileid: "9472719"
---
# <a name="benefits-management-workspace"></a>Išmokų valdymo darbo sritis

Šiame straipsnyje aprašoma išmokų **valdymo darbo** sritis, esančią Dynamics 365 Human Resources.

Darbo srityje **Išmokų valdymas** trumpai apžvelgiami išmokų elementai, į kuriuos reikia atkreipti dėmesį. Šiame puslapyje matoma:

- Prekių sumos, su kuriomis reikia atlikti tam tikrus veiksmus
- Darbuotojai su nepatvirtintais pasirinkimais
- Darbuotojai, kurie neseniai buvo užregistruoti išmokoms gauti
- Darbuotojai su būsimais gyvenimo įvykiais
- Naujai samdyti darbuotojai, kurie nėra užregistruoti
- Darbuotojai su aktyviais gyvenimo įvykiais
- Darbuotojai su atviromis registracijomis, kurie nepasirinko jokių planų

![Išmokų valdymo darbo sritis.](./media/hr-benefits-management-workspace.png)

## <a name="view-action-items"></a>Peržiūrėti veiksmų elementus

Savo veiksmų elementus galite peržiūrėti pasirinkdami plytelę arba skirtuką. Jei pasirinksite skirtuką, galėsite peržiūrėti ir pasirinkti darbuotojus darbo srities puslapio dešinėje.

![Veiksmų elementai.](./media/hr-benefits-management-workspace-action-items.png)

Pasirinkę plytelę pereisite prie tos srities puslapio. Pavyzdžiui, pasirinkus bet kurią iš šių plytelių rodomas puslapis **Darbininkų išmokų planai** darbuotojams, su kuriais reikia imtis veiksmų:

- **Nepatvirtinti pasirinkimai**
- **Atidaromos registracijos be pažymėtų planų**
- **Užregistruota į išmokas**
- **Naujų samdomų darbuotojų neužregistruota**

![Darbininkų išmokų planai.](./media/hr-benefits-management-workspace-plans.png)

Pasirinkę plyteles **Aktyvūs gyvenimo įvykiai** arba **Gyvenimo įvykiai ateityje** pereis prie aktyvių arba ateities gyvenimo įvykių sąrašo.

![Gyvenimo įvykiai.](./media/hr-benefits-management-workspace-life-events.png)

## <a name="processing"></a>Apdorojama

Registracijos tinkamumui, gyvenimo įvykiams ar tarifo keitimo atnaujinimams apdoroti naršymo meniu pasirinkite tinkamą elementą.

![Apdorojama.](./media/hr-benefits-management-workspace-processing.png)

Norėdami peržiūrėti proceso rezultatus, puslapyje pasirinkite **Proceso rezultatai**.

![Proceso rezultatai.](./media/hr-benefits-management-workspace-process-results.png)

Daugiau informacijos apie išmokų apdorojimą žr.:

- [Registracijos tinkamumo apdorojimas](hr-benefits-process-enrollment-eligibility.md)
- [Gyvenimo įvykių keitimų apdorojimas](hr-benefits-process-life-event-changes.md)
- [Gyvenimo įvykių tinkamumo apdorojimas](hr-benefits-process-life-event-eligibility.md)
- [Gyvenimo įvykių apdorojimas](hr-benefits-process-life-events.md)
- [Tarifo keitimų apdorojimas](hr-benefits-process-rate-changes.md)

## <a name="change-period"></a>Keisti laikotarpį

Norėdami peržiūrėti kitą išmokų laikotarpį, pasirinkite jį išskleidžiamajame sąraše **Laikotarpis**.

![Keisti laikotarpį.](./media/hr-benefits-management-workspace-period.png)


## <a name="open-enrollment-tab"></a>atidaryti registraciją

Savo veiksmų elementus galite peržiūrėti pasirinkdami plytelę arba skirtuką. Jei pasirinksite skirtuką, galėsite peržiūrėti ir pasirinkti darbuotojus darbo srities puslapio dešinėje.
Skirtuke **Atidaryta registracija** pateikiama pagrindinė atvirų registracijų proceso metrikos informacija. 

Informacija apie atvirą registraciją bus rodoma 30 dienų prieš **registracijos pradžios datą**. Tai yra nustatyta **Laikotarpiai** nustatyme **Išmokų valdymas** > **Nuorodos** > **Laikotarpiai**, lauke **registracijos pradžios datos**.  Norėdami pakeisti šį parametrą, eikite į **personalo bendrinamus parametrus** > **·** > **Išmokų valdymo atviros registracijos parinktys** ir atnaujinkite **lauko** Skaičių.  

Ši informacija yra prieinama skirtuke **Atidaryti registraciją**:
 - Darbuotojai, nepradėję atviro registracijos proceso
 - Darbuotojai, kurie turi apdorojamus sprendimus
 - Darbuotojai, kurie turi atliktą rinkimo procesą
 - Nepatvirtinti pasirinkimai

**Suvestinės išklotinės**

- **Nepradėta** – **Nepradėta** išklotinė rodo darbuotojų, kurie nepradėjo registracijos proceso, skaičių. Išklotinė **Nepradėta** dalis yra filtruotas sąrašas, kuriame rodomi tik tie darbuotojai, kurie nepasirinko jokių atvirų registracijos plano laikotarpio planų, jų atsisakyta arba išregistruoti. Privalomi planai yra ignoruojami ir neįtraukiami, nes jie pasirinkti pagal darbuotojo numatytuosius nustatymus.  Norėdami pamatyti darbuotojų, kurie nepradėjo atviros registracijos proceso, sąrašą darbuotojo išmokų plano puslapyje, galite detalizuoti **šią išklotąją dalyje**.

  > [!NOTE]
  > Jei nenorite sekti plano tipo atviros registracijos eigos, **Plano tipas**, galite neįtraukti eidami į **Išmokų valdymas** > **Nuorodos** > **Darbuotojo savitarnos paslaugos** > **Išmokų planų plytelės nustatymas** ir naujinimas **Sekimo atidarymo įsitraukimo progresas**.  Pavyzdžiui, galite turėti sukurtų planų, kurių **plano tipas** = **Kita**. Šie planai gali būti pasirinktiniai planai, kurių registravimo eigos sekti nenorite. Jei nepasirinksite šio plano tipo, šių tipų planų bus nepaisoma skirtuke Atviras registravimo sekimas arba baigimas **Atviras įsitraukimas** skirtukas. Šis parametras taikomas planų tipui, kuris pasirenkamas visiems laikotarpiams ir juridiniams subjektams.

- **Vykdoma** – vykdoma **išklotinė** dalis pateikia darbuotojų, kurie turi pasirinkimas, skaičių. Vykdoma **išklotinė dalis** yra filtruotas sąrašas, kuriame rodomi tik darbuotojai, kurių bent vienas planas yra atsisakytas arba pasirinktas. Privalomi planai yra ignoruojami ir neįtraukiami, nes jie pasirinkti pagal darbuotojo numatytuosius nustatymus. Galite detalizuoti iš šios išklotinės dalies, kad pamatytumėte pasirinktus ir atsisakytas planus darbuotojo **išmokų planų masinio atnaujinimo** puslapyje.

- **Įtrauktas į išmokas** – **įtrauktas į išmokų** išklotinė dalis pateikia darbuotojų, kurie visiškai yra įtraukti į išmokas, skaičių. Įtrauktas į **išmokų išklotinį** tekstą yra filtruotas sąrašas, kuriame rodomi darbuotojai, kurie pasirinko arba atsi siekiant atsisakyti visų planų. Į užklausą nebus įtraukti planai, kurie nėra sekami, kad būtų galima pradėti registraciją **darbuotojų savitarnos parametrų** puslapyje. Galite detalizuoti iš šios išklotinės dalies, kad darbuotojo išmokų planų **puslapyje būtų rodomas** darbuotojų sąrašas.

- **Nepatvirtinti pasirinkimai** – **nepatvirtintų pasirinkimų** išklotinė dalis rodo darbuotojų, kurių planai pasirinkti arba kurių reikia patvirtinti, skaičių. Galite detalizuoti iš šios išklotinės dalies, kad būtų rodomas darbuotojo **išmokų planų masinio naujinimo** puslapis.

**Veikla**

- **Nepradėta** – **Nepradėta** skirtukas rodo darbuotojų sąrašą, kurie nepradėjo registracijos proceso, skaičių. Išklotinė **Nepradėta** dalis yra filtruotas sąrašas, kuriame rodomi tik tie darbuotojai, kurie nepasirinko jokių atvirų registracijos plano laikotarpio planų, jų atsisakyta arba išregistruoti. Privalomi planai yra ignoruojami ir neįtraukiami, nes jie pasirinkti pagal darbuotojo numatytuosius nustatymus. Norėdami, kad būtų rodomas išsamios darbuotojo išmokų planų informacijos puslapis **galite detalizuoti darbuotoją**.

- **Rinkimas vykdomas** – vykdomi **rinkimai** skirtukas rodo darbuotojų, kurie turi pasirinkimas, sąrašą. Vykdoma **Rinkimo dalis** yra filtruotas sąrašas, kuriame rodomi tik darbuotojai, kurių bent vienas planas yra atsisakytas arba pasirinktas. Privalomi planai yra ignoruojami ir neįtraukiami, nes jie pasirinkti pagal darbuotojo numatytuosius nustatymus. Norėdami, kad būtų rodomas išsamios darbuotojo išmokų planų informacijos puslapis **galite detalizuoti darbuotoją**.

## <a name="view-more-options"></a>Peržiūrėti daugiau parinkčių

Jei norite peržiūrėti daugiau informacijos ir (ar) papildomi veiksmai veiksmų, kurių galite imtis, pasirinkite **Nuorodos**.

![Saitai.](./media/hr-benefits-management-workspace-links.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[Išmokų valdymo apžvalga](hr-benefits-management-overview.md)
