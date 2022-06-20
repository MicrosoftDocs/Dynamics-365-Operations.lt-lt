---
title: Išorinių duomenų grynųjų pinigų srautų prognozėse
description: Šiame straipsnyje aprašomi nustatymo veiksmai, kuriuos reikia atlikti, kad išorinius duomenis būtų galima įvesti arba importuoti į pinigų srautų prognozes.
author: RyanCCarlson2
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f0cb05770dc2fbd4e13af261b5f0a0e117a2f6d7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846979"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Išorinių duomenų grynųjų pinigų srautų prognozėse

[!include [banner](../includes/banner.md)]

Išorinius duomenis galima įvesti arba importuoti į pinigų srautų prognozes. Šiame straipsnyje aprašomi nustatymo veiksmai, kurie yra specifiniai išorinių duomenų naudojimui ir kurie įgalina išorinius duomenis įtraukti į pinigų srautų prognozę.

## <a name="external-data-setup"></a>Išorinių duomenų nustatymas

Naudokite skirtuką Išorinis **šaltinis** **·**, kuris yra pinigų srautų prognozės nustatymo puslapyje (**\>\>** Grynųjų pinigų ir banko valdymo pinigų srautų prognozavimo pinigų srautų prognozės nustatymas), norėdami įvesti parametrus, kurie palaiko išorinių duomenų naudojimą pinigų srautų prognozėse.

Išorinius duomenis galima įvesti arba importuoti į pinigų srautų prognozes. Prieš pradedant įvesti ar importuoti išorinius duomenis, turi būti nustatyti išoriniai šaltiniai. Skirtuke **Išorinis šaltinis** nustatykite išorines pinigų srautų kategorijas. Kategorija gali būti arba siunčiama **,** arba **gaunama**. **Likvidumas** turėtų būti pasirinktas kaip registravimo tipas. Juridinio **subjekto parametrų** tinklelyje pasirinkite juridinius subjektus ir atitinkamas pagrindines sąskaitas, kuriems taikomos išorinės pinigų srautų kategorijos.

Daugiau informacijos apie tai, kaip nustatyti pinigų srautų prognozes, ieškokite pinigų [srautų prognozei.](../cash-bank-management/cash-flow-forecasting.md)

## <a name="enter-external-data"></a>Įvesti išorinius duomenis

Norėdami įvesti ir modifikuoti išorinius pinigų srautų prognozių duomenis, galite naudoti excel **programoje Atidaryti**. Pasirinkite mygtuką **Išoriniai duomenys**, esantį pinigų **srautų prognozės** darbo srities puslapyje, tada pasirinkite Įtraukti **išorinius duomenis arba** Redaguoti **esamus išorinius duomenis**. Atidarę „Microsoft Excel“ failą, galite įvesti informaciją šiuose laukuose.

- **Įrašo ID** (unikalus)
- **Aprašas** (nebūtinas)
- **Išorinio šaltinio** pavadinimas – pasirinkite vieną iš verčių sąraše, kurią nustatėte nustatę finansų įžvalgas.
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
