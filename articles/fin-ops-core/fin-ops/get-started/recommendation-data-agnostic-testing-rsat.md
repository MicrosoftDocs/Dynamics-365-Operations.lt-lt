---
title: Duomenų agnostinis tikrinimas naudojant „Regression Suite Automation Tool“
description: Šiame straipsnyje aptariamos rekomendacijos dėl agnostinio duomenų tikrinimo naudojant Regression Suite Automation Tool.
author: FrankDahl
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.custom: 21761
ms.openlocfilehash: f4322cb76d1d83c02ec9d4dcb997a1cd4730d090
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269598"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a>Duomenų agnostinis tikrinimas naudojant „Regression Suite Automation Tool“

[!include [banner](../includes/banner.md)]

Nors AMK programos funkcinis tikrinimas negali būti visiškai agnostinis duomenų atžvilgiu, yra keli tikrinimo etapai ir metodai. Bandymo etapai  

- „SysTest“ sistema
- ATL sistema
- „Regression Suite Automation Tool“ (RSAT)

[![Tikrinimo klasifikacijos piramidė.](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)

## <a name="overview"></a>Peržiūra
-   **„SysTest“ sistema** – „SysTest“ sistema yra patikima tikrinant rašymo vienetus. Kadangi tikrinant vienetus paprastai tikrinami metodai arba funkcijos, jie visada turi būti agnostiniai duomenų atžvilgiu ir priklausyti tik nuo tikrinant įvestų duomenų.
-   **ATL sistema** – „Microsoft“ yra ATL sistema, kuri yra „SysTest“ sistemos abstrakcija ir gerokai palengvina bei supaprastina funkcinio tikrinimo rašymą. Ši sistema turėtų būti naudojama rašant komponentų tikrinimus ar paprastus integravimo tikrinimus.
-   **RSAT** – RSAT naudojamas integravimo tikrinimui ir verslo ciklo tikrinimui atlikti. Verslo ciklo tikrinimas, taip pat vadinamas regresijos patvirtinimo tikrinimu, priklauso nuo esamų duomenų. Tačiau šie tikrinimai gali tapti agnostiniai duomenų atžvilgiu, jei atsižvelgsite į papildomus veiksnius. 

    - o Kai vienetų ir komponentų tikrinimai yra žemo lygio ir gali būti visiškai agnostiniai duomenų atžvilgiu (neatsižvelgiant į esamą duomenų rinkinį), verslo ciklo ar regresijos patvirtinimo tikrinimai priklauso nuo tam tikrų esamų duomenų. Šie duomenys apima sąranką, konfigūracijos nustatymus (parametrus) ir pagrindinius duomenis (klientas, tiekėjai, prekės ir pan.), bet ne operacijų duomenis. Įsitikinkite, kad jei tikrinant bet kuris iš minėtų elementų keičiamas, jis būtų atstatytas atliekant galutinį tikrinimą.
    - Pasirinkite pagrindinius duomenis pagal tam tikrus kriterijus, užuot pasirinkdami tam tikrą įrašą. Pavyzdžiui, jei norite pasirinkti prekę, remdamiesi jos dimensijų reikšmėmis ir turimomis atsargomis, filtruokite produktų sąrašą pagal šias reikšmes, pasirinkite pirmą prekę ir nukopijuokite numerį, kuris bus naudojamas atliekant būsimą tikrinimą. Jei tai paprasta pagrindinių duomenų eilutė, pvz., klientas, tiekėjas arba prekė, ją galima sukurti vykdant automatizavimą ir naudoti atliekant būsimus tikrinimus taikant sujungimą. 
    - o Įveskite unikalius identifikatorius, pvz., SF numerius, per numeraciją arba naudodami „Microsoft Excel“ funkcijas, pvz., =TEXT(NOW(),"yyyymmddhhmm"). Ši funkcija pateiks unikalų numerį kas minutę, kad galėtumėte sekti, kada veiksmas įvyko. Juos galima naudoti nurodant kintamuosius, pvz., produktų kvitų numerius ir tiekėjų SF numerius. Šie tikrinimai ir toliau veikia toje pačioje duomenų bazėje, jų atkurti nereikia.
    - Visada nustatykite aplinkos **Redagavimo režimo** reikšmę **Skaityti** arba **Redaguoti** kaip pirmą tikrinimo atvejį, nes numatytoji parinktis yra **Automatinis**. Nustačius parinktį **Automatinis**, visada naudojamas ankstesnis parametras, dėl ko tikrinimo rezultatas gali būti nepatikimas. 
 
    [![Puslapis Parinktys, skirtukas Efektyvumas.](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)
 
    - Tvirtinkite tik atsifiltravę tam tikrą operaciją, užuot tvirtindami bendrai. Pavyzdžiui, ieškodami įrašų skaičiaus, filtruokite pagal operacijos numerį arba operacijos datą, kad tvirtinant visos kitos operacijos nebūtų įtrauktos. 
    - Jei tikrinate kliento balansą arba biudžetą, pirmiausia įrašykite reikšmę, paskui įtraukite savo operacijos reikšmę, kad patvirtintumėte numatytą rezultatą, užuot tikrinę fiksuotą numatomą reikšmę. 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
