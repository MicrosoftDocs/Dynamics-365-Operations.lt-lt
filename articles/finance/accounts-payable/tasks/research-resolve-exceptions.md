---
title: Išimčių nagrinėjimas ar šalinimas
description: Tiekėjo SF strategijos vykdomos, kai registruojate tiekėjo SF naudodami puslapį Tiekėjo SF ir kai atidarote tiekėjo SF puslapį Strategijos pažeidimai.
author: abruer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: abc8dc112ab577ddcbd208f898a8d4e487bc2998
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827775"
---
# <a name="research-or-resolve-exceptions"></a>Išimčių nagrinėjimas ar šalinimas

[!include [banner](../../includes/banner.md)]

Tiekėjo SF strategijos vykdomos, kai registruojate tiekėjo SF naudodami puslapį Tiekėjo SF ir kai atidarote tiekėjo SF puslapį Strategijos pažeidimai. Taip pat galite sukonfigūruoti, kad tiekėjo SF darbo eiga vykdytų tiekėjo SF strategijas kiekvieną kartą, kai į darbo eigą pateikiate SF. 

Tiekėjo SF strategijos netaikomos SF, kurios sukurtos SF registre ar SF žurnale. 

SF gretinimo tikrinimo metu tiekėjo SF strategijos nenaudojamos – jis nustatomas puslapyje Mokėtinų sumų parametrai.

Šiame įraše naudojama demonstracinė įmonė USMF. Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo. Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Pasiruošti kurti tiekėjo SF strategijas
1. Pasirinkite Mokėtinos sumos > Sąranka > Mokėtinų sumų parametrai.
2. Spustelėkite skirtuką SF tikrinimas.
3. Pažymėkite arba atžymėkite žymės langelį Automatiškai atnaujinti sąskaitos faktūros antraštės būseną.
4. Spustelėkite Gerai.
5. Lauke Registruoti SF su nesutapimais pasirinkite parinktį.
6. Uždarykite puslapį.
7. Pasirinkite Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos.
8. Spustelėkite Parametrai.
9. Spustelėkite btnAdd.
10. Uždarykite puslapį.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Kurti tiekėjo SF strategijos taisyklių tipus
1. Pasirinkite Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos taisyklių tipai.
2. Spustelėkite Naujas.
3. Lauke Taisyklės pavadinimas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Lauke Užklausos pavadinimas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Spustelėkite Įrašyti.
9. Uždarykite puslapį.

## <a name="define-a-vendor-invoice-policy"></a>Apibrėžti tiekėjo SF strategiją
1. Pasirinkite Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos.
2. Spustelėkite Naujas.
3. Lauke Pavadinimas surinkite reikšmę.
4. Lauke Aprašas įveskite reikšmę.
5. Išplėskite arba sutraukite dalį Strategijos organizacijos.
6. Medyje pasirinkite „Contoso Entertainment System USA‟.
7. Spustelėkite Pridėti.
8. Išplėskite arba sutraukite dalį Strategijos taisyklės.
9. Spustelėkite Kurti strategijos taisyklę.
10. Lauke Strategijos taisyklės aprašas surinkite reikšmę.
11. Spustelėkite Filtras.
12. Spustelėkite Pridėti.
13. Sąraše pažymėkite pasirinktą eilutę.
14. Lauke Lentelė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
15. Sąraše spustelėkite saitą pasirinktoje eilutėje.
16. Lauke Išvestinė lentelė spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
17. Sąraše spustelėkite saitą pasirinktoje eilutėje.
18. Lauke Laukas spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
19. Lauke Laukas surinkite reikšmę.
20. Uždarykite puslapį.
21. Lauke Kriterijai surinkite reikšmę.
22. Spustelėkite GERAI.
23. Spustelėkite GERAI.
24. Uždarykite puslapį.
25. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]