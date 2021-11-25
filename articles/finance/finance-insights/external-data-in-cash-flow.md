---
title: Išorinių duomenų naudojimas prognozuojant grynųjų pinigų srautus
description: Šioje temoje aprašomi nustatymo veiksmai, kuriuos reikia atlikti, kad išorinius duomenis būtų galima įvesti arba importuoti į pinigų srautų prognozes.
author: rcarlson
ms.date: 11/03/2021
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
ms.openlocfilehash: dbfa04228cf63c0874a7d69af4e2b932544c0d7f
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/04/2021
ms.locfileid: "7753007"
---
# <a name="use-external-data-in-cash-flow-forecasts"></a>Išorinių duomenų naudojimas prognozuojant grynųjų pinigų srautus

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Išorinius duomenis galima įvesti arba importuoti į pinigų srautų prognozes. Šioje temoje aprašomi nustatymo veiksmai, būdingi išorinių duomenų naudojimui ir įgalinantys išorinius duomenis įtraukti į pinigų srautų prognozę.

## <a name="external-data-setup"></a>Išorinių duomenų nustatymas

Norėdami **įvesti** **·** **\>\>** parametrus, palaikančius išorinių duomenų naudojimą pinigų srautų prognozės prognozėse, naudokite skirtuką Išorinis šaltinis puslapyje Pinigų srautų prognozės nustatymas ( Grynųjų pinigų ir banko valdymas Pinigų srautų prognozės nustatymas ).

Išorinius duomenis galima įvesti arba importuoti į pinigų srautų prognozes. Prieš įvedant arba importuojant išorinius duomenis, reikia nustatyti išorinius šaltinius. Skirtuke **Išorinis šaltinis** nustatykite išorinių pinigų srautų kategorijas. Kategorija gali būti **Siunčiama** arba **Gaunama**. **Likvidumas** turi būti pasirinktas kaip registravimo tipas. **Tinklelyje Juridinio subjekto parametrai** pasirinkite juridinius subjektus ir atitinkamas pagrindines sąskaitas, kurioms taikomos išorinių pinigų srautų kategorijos.

Daugiau informacijos apie tai, kaip nustatyti pinigų srautų prognozes, ieškokite [Pinigų srautų prognozavimas](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Įvesti išorinius duomenis

Norėdami įvesti ir modifikuoti pinigų srautų prognozių išorinius duomenis, galite naudoti **parinktį Atidaryti naudojant "Excel".** Puslapyje Pinigų srautų prognozės nustatymas pasirinkite **mygtuką Išoriniai** **·** duomenys, tada pasirinkite **Pridėti išorinius duomenis** arba Redaguoti **esamus išorinius duomenis**. Atidarę „Microsoft Excel“ failą, galite įvesti informaciją šiuose laukuose.

- **Įrašo ID** (unikalus)
- **Aprašas** (nebūtinas)
- **Išorinio šaltinio pavadinimas** – pasirinkite vieną iš reikšmių sąraše, kurį nustatėte nustatydami "Finance insights".
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
