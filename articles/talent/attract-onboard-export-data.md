---
title: Duomenų eksportavimas iš „Attract“ ir „Onboard“
description: Duomenų eksportavimas iš „Dynamics 365 Talent“ – „Attract“ ir „Onboard“.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461940"
---
# <a name="export-data-from-attract-and-onboard"></a>Duomenų eksportavimas iš „Attract“ ir „Onboard“

[!include [banner](includes/banner.md)]

Kaip paskelbta [„Dynamics 365 Talent: Attract“ ir „Dynamics 365 Talent: Onboard“ programų panaikinime](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), panaikiname „Dynamics 365 Talent: Attract“ ir „Dynamics 365 Talent: Onboard“ nuo 2022 m. vasario 1 d. Siekiant padėti pereiti į kitą produktą, abiejose programose dabar yra duomenų eksportavimo galimybės.

## <a name="export-data-from-attract"></a>Duomenų eksportavimas iš „Attract“

Galite eksportuoti duomenis be prieigos prie savo aplinkos apribojimų. Galbūt norėsite tai atlikti testavimo tikslais arba norėdami suprasti savo duomenų struktūrą. Kai būsite pasiruošę perkėlimui, apribokite prieigą prie savo „Attract“ aplinkos vadovaudamiesi instrukcijomis po šia procedūra. Nepamirškite iš naujo eksportuoti savo duomenų. 

1. Eikite į [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Dalyje **Duomenų eksportavimas** pasirinkite **Prašyti duomenų eksportavimo**.

   ![[Prašyti duomenų eksportavimo iš „Attract“](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. Kai bus rodomas pranešimo langas **Jūsų prašymas apdorojamas**, pasirinkite **Gerai**. Duomenų eksportavimas gali užtrukti iki 20 minučių, priklausomai nuo eksportavimo dydžio.

4. Kai eksportavimas baigiamas, prie jo pasirinkite mygtuką **Atsisiųsti**. 

   >[!NOTE]
   >Visų duomenų eksportavimas galioja septynias dienas, kurioms praėjus nebegalioja saitas **Atsisiuntimas**.</br>
   
Atsisiuntime yra .zip failas su jūsų „Attract“ duomenimis, įskaitant toliau nurodytus aplankus.

| Aplanko pavadinimas | Aprašymas |
| --- | --- |
| Administratoriaus parametrai | „Attract“ administravimo centro konfigūracijos. |
| Kandidatai | Visi kandidatai, įtraukti į užduočių arba talentų telkinius. |
| El. laiško šablonai | Visi aplinkoje sukonfigūruoti el. laiškų šablonai. |
| Darbo pasiūlymų paketų šablonai | Visų sukurtų darbo pasiūlymų paketų šablonai, taip pat jų susijusios konfigūracijos. |
| Darbo pasiūlymo taisyklių rinkiniai |  Visų taisyklių rinkinių failai, kuriuos įkėlėte pasiūlymų valdymui. |
| Darbo pasiūlymų šablonai | Visi darbo pasiūlymų dokumentų šablonai, sukurti aplinkoje. |
| Laisvos darbo vietos | Visi sukurti darbai. Panaikinti darbai neeksportuojami. Poaplankiuose yra kandidatų paraiškos su poaplankiais kandidatų paraiškų priedams ir pasiūlymų paketais, jei taikoma. |
| Darbo pasiūlymų šablonai | Darbo apdorojimo šablonai, sukonfigūruoti aplinkoje. |
| Talentų telkiniai | Visi sukurti talentų telkiniai, jų bendraautorių sąrašai ir talentų telkinių sąrašai. |
| Darbininkai | Visų darbuotojų, kurie yra aplinkoje, sąrašas ir darbuotojų vaidmenys. |
| (šakninis aplankas) | JSON schemos failas, aprašantis duomenų struktūros laukus. |

### <a name="restrict-access-to-attract"></a>Prieigos prie „Attract“ apribojimas

Kai esate pasiruošę perkėlimui, apribokite ne administratorių prieigą prie „Attract“ aplinkos ir eksportuokite duomenis.

>[!IMPORTANT]
>Prieiga prie „Attract“ aplinkos apribojama visam laikui ir apribojimo negalima atšaukti. Jei norite, kad ne administratorių vartotojai galėtų toliau naudotis jūsų aplinka, praleiskite šį veiksmą.

1. Eikite į [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Norėdami apriboti ne administratorių prieigą prie „Attract“ aplinkos, dalyje **Apriboti prieigą prie šios programos** pasirinkite **Apriboti prieigą dabar**. Apribojus prieigą, taip pat anuliojamos visos užregistruotos aktyvios užduotys.

   ![[Ne administratorių prieigos prie „Attract“ apribojimas](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. Kai matote įspėjimą **Tai yra nuolatinis pakeitimas**, pasirinkite **Apriboti prieigą**, kad visam laikui apribotumėte ne administratorių vartotojų prieigą prie šios aplinkos. Jei nesate pasirengę atlikti šio veiksmo, pasirinkite **Atšaukti**.

   ![[Įspėjimas, kad apribota prieiga yra nuolatinis pakeitimas](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >Administratoriai gali toliau naudotis duomenų eksportavimo ir ataskaitų pagal asmenis puslapiais po to, kai apribojote prieigą prie „Attract“ aplinkos.

## <a name="export-data-from-onboard"></a>Eksportuoti duomenis iš „Onboard”

Kai būsite pasiruošę, galite atsisiųsti šablonus, vadovus ir kandidato duomenis iš „Onboard“.

1. Eikite į [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).

2. Dalyje **Duomenų eksportavimas** pasirinkite **Prašyti duomenų eksportavimo**. 

   ![[Prašyti duomenų eksportavimo iš „Onboard“](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. Kai bus rodomas pranešimo langas **Jūsų prašymas apdorojamas**, pasirinkite **Gerai**. Duomenų eksportavimas gali užtrukti iki 20 minučių, priklausomai nuo eksportavimo dydžio.

4. Kai eksportavimas baigiamas, prie jo pasirinkite mygtuką **Atsisiųsti**. 

   ![[Atsisiųsti eksportuotus duomenis iš „Onboard”](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >Duomenis galite eksportuoti septynias dienas. Po septynių dienų, saitas **Atsisiuntimas** nebegalioja, todėl turite prašyti naujo eksportavimo, jei reikia iš naujo atsiųsti duomenis. Paleidus naują duomenų eksportavimą, visi esami atsisiuntimai nustos galioti po naujo eksportavimo.

Atsisiuntimas yra .zip failas, kuriame yra:

- Aplankas **Šablonai**, kuriame yra jūsų „Onboard“ šablonai „Word“ dokumentų formatu.

- Aplankas **Guides**, kuriame yra jūsų „Onboard“ vadovai „Word“ dokumentų formatu.

## <a name="see-also"></a>Taip pat žiūrėkite

[„Dynamics 365 Talent: Attract“ ir „Dynamics 365 Talent: Onboard“ programų panaikinimas](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)