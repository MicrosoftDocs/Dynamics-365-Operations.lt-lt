---
title: Apibrėžti šaltinio dokumento audito strategijas
description: Šiame straipsnyje paaiškinama, kaip nustatyti ir vykdyti audito strategijos taisykles.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b8aa106cd5a5596f6b9a6663390e03ebc3f91a7b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872534"
---
# <a name="define-audit-policies-for-source-documents"></a>Apibrėžti šaltinio dokumento audito strategijas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti ir vykdyti audito strategijos taisykles. Pavyzdyje naudojamos viešbučio tipo išlaidų ataskaitos. Šioje procedūroje naudojama demonstracinė įmonė USMF. Kad būtų galima atlikti šias užduotis, auditoriaus vaidmenį sudaro tinkamos teisės.

1. Naršymo srityje eikite į **Moduliai > Audito darbo sritis > Konfigūravimas > Strategijos taisyklės tipas**.
2. Pasirinkite **Naujas**.
3. Lauke **Taisyklės pavadinimas** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Lauke **Užklausos pavadinimas** pasirinkite **Išlaidų ataskaitos eilutė**
6. Lauke **Užklausos tipas** pasirinkite **Agregavimas**
7. Lauke **Juridinis subjektas** pasirinkite **Juridinis subjektas**
8. Lauke **Dokumento datos nuoroda** pasirinkite **Modifikavimo data ir laikas**
9. Pasirinkite **Įrašyti**.
10. Naršymo srityje eikite į **Moduliai > Audito darbo sritis > Konfigūravimas > Audito strategijos**.
11. Pasirinkite **Naujas**.
12. Lauke **Pavadinimas** įveskite reikšmę.
13. Išplėskite skyrių **Organizacijų strategijos**.
14. Medyje pasirinkite **„Contoso Entertainment System“, JAV**, tada pasirinkite **Įtraukti**.
15. Medyje pasirinkite **„Contoso Consulting“, JAV**, tada pasirinkite **Įtraukti**.
16. Medyje pasirinkite **„Contoso Retail“, JAV**, tada pasirinkite **Įtraukti**.
17. Sutraukite skyrių **Organizacijų strategijos**.
18. Išplėskite skyrių **Strategijų taisyklės**.
19. Sąraše raskite ir pasirinkite anksčiau sukurtą strategijos taisyklę.
20. Pasirinkite **Kurti strategijos taisyklę**.
21. Lauke **Įsigaliojimo data** įveskite datą ir laiką.
22. Pasirinkite **Filtras**.
23. Sąraše pasirinkite eilutę parinkčiai **Išlaidų kategorija** ir nustatykite išsamią informaciją į **Viešbutis**.
24. Lauke **Kriterijai** įveskite arba pasirinkite reikšmę.
25. Pasirinkite skirtuką **Agregavimas**.
26. Pasirinkite **Įtraukti**.
27. Sąraše pasirinkite parinkties **Operacijos suma** lauko reikšmę.
28. Lauke **Laukas** įveskite arba pasirinkite reikšmę.
29. Lauke **AggregateFunction** pasirinkite **Suma**.
30. Pasirinkite skirtuką **Grupuoti pagal**.
31. Pasirinkite **Įtraukti**.
32. Sąraše pasirinkite reikšmę parinkčiai **Darbuotojas**.
33. Pasirinkite **Įtraukti**.
34. Sąraše pasirinkite reikšmę parinkčiai **Išlaidų kategorija**.
35. Lauke **Laukas** įveskite arba pasirinkite reikšmę.
36. Pažymėkite skirtuką **Having**.
37. Pasirinkite **Įtraukti**.
38. Pasirinkite **Operacijos suma**.
39. Lauke **Laukas** įveskite arba pasirinkite reikšmę.
40. Lauke **AggregateFunction** pasirinkite **Suma**.
41. Lauke **Kriterijai** įveskite `>2000`.
42. Pasirinkite **Gerai**.
43. Pasirinkite **Tikrinti**.
44. Lauke **Dokumento žymėjimo pradžios data** įveskite datą ir laiką.
45. Lauke **Dokumento žymėjimo pabaigos data** įveskite datą ir laiką.
46. Pasirinkite **Paleisti tikrinimą**.
47. Veiksmų srityje pasirinkite **Audito strategija**.
48. Pasirinkite **Papildomos parinktys**.
49. Lauke **Pradžios data** įveskite datą ir laiką.
50. Lauke **Pabaigos data** įveskite datą ir laiką.
51. Pasirinkite **Paketas**.
52. Išplėskite skyrių **Vykdyti fone**.
53. Pasirinkite **Taip** lauke **Paketinis vykdymas**.
54. Pasirinkite **Gerai**.
55. Naršymo srityje eikite į **Moduliai > Audito darbo sritis > Audito atvejai**.
56. Sąraše raskite ir pasirinkite norimą įrašą.
57. Išplėskite skyrių **Sąsajos**.
58. Sąraše raskite ir pasirinkite norimą įrašą.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
