---
title: Išorinių duomenų naudojimas prognozuojant grynųjų pinigų srautus
description: Šioje temoje aprašomi nustatymo veiksmai, kuriuos reikia atlikti, kad išoriniai duomenys galėtų būti įvedami arba importuojami į pinigų srautų prognozes.
author: rcarlson
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 855f428ae8ce79f2b7ce9a6f3347cd454bad9566
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386467"
---
# <a name="use-external-data-in-cash-flow-forecasts"></a>Išorinių duomenų naudojimas prognozuojant grynųjų pinigų srautus

[!include [banner](../includes/banner.md)]

Išorinius duomenis galima įvesti arba importuoti į pinigų srautų prognozes. Šioje temoje aprašomi nustatymo veiksmai, būdingi išorinių duomenų naudojimui ir įgalinantys išorinius duomenis įtraukti į pinigų srautų prognozę.

## <a name="external-data-setup"></a>Išorinių duomenų nustatymas

Norėdami įvesti parametrus, palaikančius išorinių duomenų naudojimą grynųjų pinigų srautų prognozėse, naudokite skirtuką **Išorinis šaltinis**, esantį puslapyje **Grynųjų pinigų srautų prognozės sąranka** (**Grynųjų pinigų ir banko valdymas \> Grynųjų pinigų srauto prognozavimas**).

Daugiau informacijos, kaip nustatyti skaitiklius, žr. [Grynųjų pinigų srauto prognozė](../cash-bank-management/cash-flow-forecasting.md).

Norėdami įvesti išorinius pinigų srautų prognozių duomenis, galite naudotis „Excel“ patirtimi, kad galėtumėte įvesti ir modifikuoti išorinius duomenis. Pasirinkite mygtuką **Išoriniai duomenys**, tada pasirinkite **Įtraukti išorinius duomenis** arba **Redaguoti esamus išorinius duomenis**. Atidarę „Microsoft Excel“ failą, galite įvesti informaciją šiuose laukuose.

- **Įrašo ID**
- **Aprašas** (nebūtinas)
- **Išorinis šaltinio pavadinimas** – pasirinkite vieną iš sąrašo reikšmių, kurias nurodėte nustatydami „Finance Insights”.
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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
