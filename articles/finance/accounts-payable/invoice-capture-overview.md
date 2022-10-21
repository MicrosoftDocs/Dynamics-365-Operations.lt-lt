---
title: SF fiksavimo sprendimo peržiūra
description: Šiame straipsnyje pateikiama informacija apie SF fiksavimo sprendimą.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691004"
---
# <a name="invoice-capture-solution"></a>SF fiksavimo sprendimas

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šiame straipsnyje pateikiama informacija apie SF fiksavimo sprendimą, kuris automatiškai sukuria tiekėjo SF iš skaitmeninių SF vaizdų.

Mokėtinų sumų (AP) padalinys valdo ir apdoroja gautų prekių ir paslaugų SF. AP buhalteris tikrina tiekėjo SF duomenis dėl šių priežasčių:

- Norėdami išvengti papildomų pastangų, jei laikotarpio uždarymo metu reikia pakoreguoti ar pataisyti
- Laiku apmokėti tiekėjo SF ir neleisti finansinių nuostolių dėl klaidos arba apgaulės

Optinė ženklų atpažinimo (OCR) labai pasinaudojo įvairios pramonės šakos per praėjusius metus. Dabar įprasta spausdintus tekstus spausdinti skaičiais, kad juos būtų galima elektroniniu būdu redaguoti, ieškoti, kas tiksliau saugoti ir rodyti internete. Skaitmeninis tekstas gali būti naudojamas įrenginių procesuose, pvz., skaičiavimo, įrenginių konvertavimo, teksto konvertavimo į darbą, pagrindinių duomenų ir duomenų gavybos tekstuose.

Programos įžvalgų (AI) technologija įgalino modernius OCR sprendimus skaityti skirtingus SF formatus iš skirtingų tiekėjų reikalaujant daug personalo veiksmų. Daugiau įmonių atpažįsta, kad gali įrašyti pastangas ir pagerinti tikslumą apdorodamos SF automatiškai, o ne apdoroja jas rankiniu būdu.

## <a name="system-landscape"></a>Sistemos horizontaliai

Šiame pavyzdyje parodyti pagrindiniai SF fiksavimo sprendimo komponentai ir veiksmai.

[![SF fiksavimo sprendimo komponentai ir veiksmai.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Būtini vaidmenys

Toliau pateikiamoje lentelėje parodyti vaidmenys, kurių reikia norint nustatyti ir naudoti SF fiksavimo sprendimą.

| Vaidmuo          | Veiksmai | Sistemos | Vaidmenų pavadinimai |
|---------------|---------|---------|-----------|
| Administratorius | <ul><li>Nustatykite aplinkas Microsoft Power Platform.</li><li>Įdiekite sprendimus Microsoft Power Platform.</li><li>Nustatyti "Dynamics 365" ir "Dynamics 365" ryšius AI Builder.</li><li>Nustatyti vietas Azure Data Lake Storage.</li></ul> | <ul><li>Dynamics 365</li><li>„Microsoft Power Platform“</li><li>„Azure Data Lake Storage“</li></ul> | <ul><li>"Dynamics 365" administratorius</li><li>„Power Platform“ administratorius</li><li>Saugojimo BLOB duomenų savininkas</li></ul> |
| AI kūrėjas      | <ul><li>Prižiūrėti srautus.</li><li>Kurti pasirinktinius AI modelius.</li></ul> | <ul><li>„Microsoft Power Platform“</li></ul> | <ul><li>Pilietis, asmenys</li></ul> |
| AP klerkas      | <ul><li>Peržiūrėkite ir imkite veiksmus tiekėjo SF išdėstymo srityje.</li><ul> | <ul><li>„Microsoft Power Platform“</li></ul> | <ul><li>Naujas AP klerko vaidmuo Power Platform</li></ul> |
| AP klerkas      | <ul><li>Vykdyti kasdienes operacijas kaip AP klerkas.</li><li>Eiti į tiekėjo SF išdėstymo sritį.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Mokėtinų sumų klerkas</li></ul> |
  
Norėdami gauti daugiau informacijos apie SF fiksavimo diegimą, žr. [Įdiegti SF fiksavimą](../accounts-payable/install-invoice-capture.md).  
