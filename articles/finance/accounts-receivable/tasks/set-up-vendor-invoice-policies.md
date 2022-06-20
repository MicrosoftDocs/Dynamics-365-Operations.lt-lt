---
title: Nustatyti tiekėjų SF strategijas
description: Šiame straipsnyje paaiškinama, kaip nustatyti tiekėjo SF strategijas.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 049b38b6feba5f4369d79b89b4c81a8195dd7758
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904736"
---
# <a name="set-up-vendor-invoice-policies"></a>Nustatyti tiekėjų SF strategijas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip nustatyti tiekėjo SF strategijas. Tiekėjo SF strategijos paleidžiamos, kai užregistruojate tiekėjo **SF** naudodami tiekėjo SF puslapį ir kai atidarote tiekėjo SF **strategijos pažeidimų** puslapį. Taip pat galite sukonfigūruoti, kad tiekėjo SF darbo eiga vykdytų tiekėjo SF strategijas kiekvieną kartą, kai į darbo eigą pateikiate SF. 

- Tiekėjo SF strategijos netaikomos SF, kurios sukurtos SF registre ar SF žurnale.  
- SF gretinimo tikrinimas naudoja ne tiekėjo SF strategijas, bet yra nustatomas mokėtinų **sumų parametrų** puslapyje.  
- Šiame įraše naudojama demonstracinė įmonė USMF. Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo. Prieš pradėdami įsitikinkite, kad pasirinktas **SF gretinimo** konfigūracijos raktas.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Pasiruošti kurti tiekėjo SF strategijas
1. Pasirinkite **Naršymo sritis > Moduliai > Mokėtinos sumos > Sąranka > Mokėtinų sumų parametrai**.
2. Pasirinkite skirtuką **SF tikrinimas.**.
3. Pažymėkite arba atžymėkite žymės langelio būseną **Automatiškai atnaujinti sąskaitos faktūros antraštę**.
4. Pasirinkite **Gerai**.
5. Lauke **Registruoti SF su nesutapimais** pasirinkite parinktį.
6. Uždarykite puslapį.
7. Eikite į **Naršymo sritis > Moduliai > Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos**.
8. Pasirinkite **Parametrai**.
9. Pasirinkite **Įtraukti**.
10. Norėdami grįžti į neregistruotų tabelių puslapį, uždarykite puslapį.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Kurti tiekėjo SF strategijos taisyklių tipus
1. Eikite į **Naršymo sritis > Moduliai > Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos**.
2. Pasirinkite **Naujas**.
3. Įveskite reikšmes laukuose **Taisyklės vardas** ir **Aprašas**.
4. Laukelyje **Užklausos pavadinimas** pasirinkite išskleidžiamąjį mygtuką, kad atidarytumėte peržvalgą. Tada pasirinkite norimą įrašą.
5. Pasirinkite **Įrašyti**.
6. Norėdami grįžti į neregistruotų tabelių puslapį, uždarykite puslapį.

## <a name="define-a-vendor-invoice-policy"></a>Apibrėžti tiekėjo SF strategiją
1. Eikite į **Valdymo skiltis > Moduliai > Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos**.
2. Pasirinkite **Naujas**.
3. Įveskite reikšmes laukuose **Profilis** ir **Aprašas**.
4. Išplėskite arba sutraukite sekciją **Strategijos organizacijos**.
5. Medyje pasirinkite **„Contoso“ pramogų sistema (JAV)**.
6. Pasirinkite **Įtraukti**.
7. Išplėskite arba sutraukite sekciją **Strategijos taisyklės**.
8. Pasirinkite **Kurti strategijos taisyklę**.
9. Lauke **Strategijos taisyklės aprašas** įveskite reikšmę.
10. Pasirinkite **Filtras**.
11. Pasirinkite **Įtraukti**. Pasirinkti aktyvų įrašą
12. Laukuose **Lentelė**,**Išvestinė lentelė** ir **Laukas** pasirinkite arba įveskite parinktis iš išplečiamojo meniu.
13. Uždarykite puslapį.
14. Lauke **Kriterijai** surinkite reikšmę.
15. Pasirinkite **Gerai**.
16. Pasirinkite **Gerai**.
17. Norėdami grįžti į neregistruotų tabelių puslapį, uždarykite puslapius.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
