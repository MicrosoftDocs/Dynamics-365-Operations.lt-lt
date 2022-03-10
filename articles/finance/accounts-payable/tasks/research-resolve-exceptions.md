---
title: Išimčių nagrinėjimas ar šalinimas
description: Tiekėjo SF strategijos vykdomos, kai registruojate tiekėjo SF naudodami puslapį Tiekėjo SF ir kai atidarote tiekėjo SF puslapį Strategijos pažeidimai.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32ff53198f61e1d1af3c437e9488c2a246cf820a
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/12/2022
ms.locfileid: "8110024"
---
# <a name="research-or-resolve-exceptions"></a>Išimčių nagrinėjimas ar šalinimas

[!include [banner](../../includes/banner.md)]

Tiekėjo SF strategijos paleidžiamos, kai užregistruojate tiekėjo **SF** naudodami tiekėjo SF puslapį ir kai atidarote tiekėjo SF **strategijos pažeidimų** puslapį. Taip pat galite sukonfigūruoti, kad tiekėjo SF darbo eiga vykdytų tiekėjo SF strategijas kiekvieną kartą, kai į darbo eigą pateikiate SF. 

Tiekėjo SF strategijos netaikomos SF, kurios sukurtos SF registre **arba SF** **žurnale**. 

SF gretinimo tikrinimas naudoja ne tiekėjo SF strategijas, bet yra nustatomas mokėtinų **sumų parametrų** puslapyje.

Šiame įraše naudojama demonstracinė įmonė USMF. Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo. Prieš pradėdami įsitikinkite, kad pasirinktas **SF gretinimo** konfigūracijos raktas.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Pasiruošti kurti tiekėjo SF strategijas
1. Eikite į **Mokėtinos sumos > Sąranka > Mokėtinų sumų parametrai**
2. Spustelėkite skirtuką **SF** tikrinimas.
3. Pažymėkite arba išvalykite žymės **langelį Automatiškai atnaujinti SF antraštės** būseną.
4. Spustelėkite **Gerai**.
5. Lauke **Registruoti SF su nesutapimais** pasirinkite parinktį.
6. Uždarykite puslapį.
7. Eikite **į tiekėjo > strategijų > nustatymo informaciją**.
8. Spustelėkite **Parametrai**.
9. Spustelėkite **Pridėti**.
10. Uždarykite puslapį.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Kurti tiekėjo SF strategijos taisyklių tipus
1. Eikite **į tiekėjo > strategijos > tipų mokėtinų sumų nustatymą**.
2. Spustelėkite **Naujas**.
3. Lauke **Taisyklės pavadinimas** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Lauke Užklausos **pavadinimas spustelėkite** išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
6. Sąraše raskite ir pasirinkite norimą įrašą.
7. Sąraše spustelėkite saitą pasirinktoje eilutėje.
8. Spustelėkite **Įrašyti**.
9. Uždarykite puslapį.

## <a name="define-a-vendor-invoice-policy"></a>Apibrėžti tiekėjo SF strategiją
1. Eikite **į tiekėjo > strategijų > nustatymo informaciją**.
2. Spustelėkite **Naujas**.
3. Lauke **Pavadinimas** įveskite reikšmę.
4. Lauke **Aprašo laukas** surinkite reikšmę.
5. Išplėskite arba sutraukite sekciją **Strategijos organizacijos**.
6. Medyje pasirinkite „Contoso Entertainment System USA‟.
7. Spustelėkite **Pridėti**.
8. Išplėskite arba sutraukite sekciją **Strategijos taisyklės**.
9. Spustelėkite **Kurti strategijos taisyklę**.
10. Lauke **Strategijos taisyklės aprašas** įveskite reikšmę.
11. Spustelėkite **Filtras**.
12. Spustelėkite **Pridėti**.
13. Sąraše pažymėkite pasirinktą eilutę.
14. Norėdami atidaryti **peržvalgą**, lauke Lentelė spustelėkite išplečiamąjį mygtuką.
15. Sąraše spustelėkite saitą pasirinktoje eilutėje.
16. Lauke Išvestinė **lentelė** spustelėkite išplečiamąjį mygtuką, kad atidarytumėte peržvalgą.
17. Sąraše spustelėkite saitą pasirinktoje eilutėje.
18. Lauke spustelėkite **išplečiamąjį** mygtuką, kad atidarytumėte peržvalgą.
19. **Lauke įveskite** vertę.
20. Uždarykite puslapį.
21. Lauke **Kriterijai** įveskite reikšmę.
22. Spustelėkite **Gerai**.
23. Spustelėkite **Gerai**.
24. Uždarykite puslapį.
25. Uždarykite puslapį.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
