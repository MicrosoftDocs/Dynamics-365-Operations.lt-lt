---
title: Duomenų agnostinis tikrinimas naudojant „Regression Suite Automation Tool“
description: Šioje temoje aptariamos duomenų agnostinio tikrinimo naudojant „Regression Suite Automation Tool“ rekomendacijos.
author: kfend
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: d9a5bce1cc56dfdf66b2ce58c2e740b7c4b3bdfc7f4e75396fe5dc7cb931b6d0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763415"
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