---
title: Išorinių duomenų naudojimas prognozuojant grynųjų pinigų srautus (peržiūros versija)
description: Šioje temoje aprašomi nustatymo veiksmai, kuriuos reikia atlikti, kad išoriniai duomenys galėtų būti įvedami arba importuojami į pinigų srautų prognozes.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 801327dc54f6d4cfef7a9f062395e29846783e8f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644950"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Išorinių duomenų naudojimas prognozuojant grynųjų pinigų srautus (peržiūros versija)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Išorinius duomenis galima įvesti arba importuoti į pinigų srautų prognozes. Šioje temoje aprašomi nustatymo veiksmai, būdingi išorinių duomenų naudojimui ir įgalinantys išorinius duomenis įtraukti į pinigų srautų prognozę.

## <a name="external-data-setup"></a>Išorinių duomenų nustatymas

Norėdami įvesti parametrus, palaikančius išorinių duomenų naudojimą grynųjų pinigų srautų prognozėse, naudokite skirtuką **Išorinis šaltinis**, esantį puslapyje **Grynųjų pinigų srautų prognozės sąranka** (**Grynųjų pinigų ir banko valdymas \> Grynųjų pinigų srauto prognozavimas**).

Daugiau informacijos, kaip nustatyti skaitiklius, žr. [Grynųjų pinigų srauto prognozė](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).

Norėdami įvesti išorinius pinigų srautų prognozių duomenis, galite naudotis „Excel“ patirtimi, kad galėtumėte įvesti ir modifikuoti išorinius duomenis. Pasirinkite mygtuką **Išoriniai duomenys**, tada pasirinkite **Įtraukti išorinius duomenis** arba **Redaguoti esamus išorinius duomenis**. Atidarę „Microsoft Excel“ failą, galite įvesti informaciją šiuose laukuose.

- **Įrašo ID**
- **Aprašas** (nebūtinas)
- **Išorinis šaltinio pavadinimas** – pasirinkite vieną iš sąrašo reikšmių, kurias nurodėte nustatydami finansines įžvalgas.
- **Juridinis subjektas**
- **Data**
- **Suma operacijos valiuta**
- **Valiutos kodas**
- **Numatytoji dimensija** (pasirinktinai)
- **Dokumento numeris** (pasirinktinai)
- **Sąskaitos numeris** (pasirinktinai)
- **Sąskaitos pavadinimas** (pasirinktinai)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>Išorinių duomenų importavimas naudojant duomenų valdymo sistemą

Naudodami darbo sritį **Duomenų valdymas** ir objektą, pavadintą **Grynųjų pinigų srauto prognozės išorinio šaltinio įrašas**, galite importuoti duomenis, skirtus grynųjų pinigų srautų prognozėms.

Be to, jei reikia perkelti nustatymo duomenis iš vienos aplinkos į kitą, reikia nustatyti šias objektų sritis, kurias galima nustatyti atliekant nustatymo lenteles:

- Grynųjų pinigų srauto prognozės išorinio šaltinio nustatymas
- Grynųjų pinigų srauto prognozės išorinio šaltinio juridinio subjekto nustatymas

#### <a name="privacy-notice"></a>Privatumo pranešimas
Peržiūros versijos (1) gali naudoti mažiau privatumo ir mažiau saugos priemonių nei „Dynamics 365 Finance and Operations“ paslauga, (2) jos nėra įtrauktos į aptarnavimo lygio sutartį (SLA), (3) jos neturėtų būti naudojamos apdoroti asmens duomenims ar kitiems duomenims, kuriems taikomi teisiniai ir atitikimo teisės aktai (4) ir jų palaikymas yra ribotas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]