---
title: EUR-00012 ES įrašo sertifikato išdavimas
description: Ši procedūra padės įgalinti ES įrašo sertifikatą, konfigūruoti kliento sąskaitą, kad būtų galima naudoti įrašų sertifikatus ir išduoti sertifikatą.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41ede621fdb36d39efc79788cd2da77aacfc282895dd84d572b99f4528456643
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768240"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a>EUR-00012 ES įrašo sertifikato išdavimas

[!include [banner](../../includes/banner.md)]
Ši procedūra padės įgalinti ES įrašo sertifikatą, konfigūruoti kliento sąskaitą, kad būtų galima naudoti įrašų sertifikatus ir išduoti sertifikatą. Ši procedūra buvo sukurta naudojant demonstracinių duomenų įmonės DEMF.


## <a name="enable-entry-certificate-management"></a>Įgalinti įrašo sertifikato valdymo funkciją
1. Pasirinkite Gautinos sumos > Nustatymai > Gautinų sumų parametrai.
2. Spustelėkite skirtuką Siuntos.
3. Išplėskite skyrių Įrašo sertifikatas.
4. Lauke Įgalinti įrašo sertifikato valdymą pasirinkite Taip.
5. Lauke Įgalinti įrašo sertifikato išdavimą pasirinkite Taip.
6. Spustelėkite skirtuką Numeracijos.
7. Sąraše raskite ir pasirinkite Įrašo sertifikato eilutė.
8. Lauke Numeracijos kodas įveskite arba pasirinkite vertę.

## <a name="set-up-a-customer"></a>Kliento nustatymas
1. Pasirinkite Gautinos sumos > Klientai > Visi klientai.
2. Norėdami rasti įrašus, naudokite spartųjį filtrą. Pvz., filtruokite lauką Sąskaita naudodami vertę „DE-015“.
3. Atidarykite kliento sąskaitos informaciją.
4. Spustelėkite Redaguoti.
5. Išplėskite skyrių SF ir pristatymas.
6. Lauke Įrašo sertifikatas būtinas pasirinkite Taip.
7. Lauke Išduoti įrašo sertifikatą pasirinkite Taip.
8. Spustelėkite Įrašyti.

## <a name="create-an-eu-entry-certificate-automatically"></a>ES įrašo sertifikato automatinis kūrimas
1. Pasirinkite Gautinos sumos > Užsakymai > Visi pardavimo užsakymai.
2. Spustelėkite Naujas.
3. Lauke Kliento sąskaita įveskite arba pasirinkite reikšmę.
4. Spustelėkite Gerai.
5. Lauke Prekės numeris įveskite arba pasirinkite reikšmę.
6. Spustelėkite Įrašyti.
7. Veiksmų srityje spustelėkite Paimti ir pakuoti.
8. Spustelėkite Registruoti važtaraštį.
9. Išplėskite skyrių Parametrai.
10. Lauke Kiekis pasirinkite Visi.
11. Išvalykite žymės langelį Išduoti įrašo sertifikatą.
    * Įrašo sertifikatas gali būti išduotas registruojant važtaraštį arba išrašant užsakymo SF. Palikite atžymėtą žymės langelį Išduoti įrašo sertifikatą, jei norite, kad jis būtų išduotas vėliau.  
12. Spustelėkite GERAI.
13. Spustelėkite GERAI.
14. Veiksmų srityje spustelėkite Sąskaita faktūra.
15. Spustelėkite Sąskaita faktūra.
    * Patikrinkite, ar skyriuje Apžvalga pažymėti žymės langeliai Įrašo sertifikatas būtinas ir Išduoti įrašo sertifikatą.  Taip pat galite pažymėti žymės langelį Spausdinti įrašo sertifikatą, kad galėtumėte sertifikatą atsispausdinti.  
16. Spustelėkite GERAI.
17. Spustelėkite GERAI.
18. Veiksmų srityje spustelėkite Sąskaita faktūra.
19. Spustelėkite Sąskaita faktūra.
20. Veiksmų srityje spustelėkite Sąskaita faktūra.
21. Spustelėkite Rodyti išduotus įrašų sertifikatus.
22. Spustelėkite Spausdinti.
23. Uždarykite puslapį.
24. Spustelėkite keisti būseną.
25. Lauke Nauja būsena pasirinkite parinktį.
26. Spustelėkite GERAI.
27. Uždarykite puslapį.

## <a name="create-an-eu-entry-certificate-manually"></a>ES įrašo sertifikato kūrimas rankiniu būdu
1. Veiksmų srityje spustelėkite Sąskaita faktūra.
2. Spustelėkite Kurti įrašo sertifikatą.
3. Spustelėkite Gerai.
4. Veiksmų srityje spustelėkite Sąskaita faktūra.
5. Spustelėkite Rodyti išduotus įrašų sertifikatus.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]