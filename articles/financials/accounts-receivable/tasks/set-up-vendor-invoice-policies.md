---
title: Tiekėjų sąskaitų faktūrų strategijų nustatymas
description: Šioje temoje aprašoma, kaip nustatyti tiekėjo SF strategijas programoje „Dynamics 365 for Finance and Operations“.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 328aafd16496fdbb963c9aa40a5c13005be7a382
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842814"
---
# <a name="set-up-vendor-invoice-policies"></a>Tiekėjų sąskaitų faktūrų strategijų nustatymas

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šioje temoje aprašoma, kaip nustatyti tiekėjo SF strategijas programoje „Dynamics 365 for Finance and Operations“. Tiekėjo SF strategijos vykdomos, kai registruojate tiekėjo SF naudodami puslapį Tiekėjo SF ir kai atidarote tiekėjo SF puslapį Strategijos pažeidimai. Taip pat galite sukonfigūruoti, kad tiekėjo SF darbo eiga vykdytų tiekėjo SF strategijas kiekvieną kartą, kai į darbo eigą pateikiate SF. 

- Tiekėjo SF strategijos netaikomos SF, kurios sukurtos SF registre ar SF žurnale.  
- SF gretinimo tikrinimo metu tiekėjo SF strategijos nenaudojamos – jis nustatomas puslapyje Mokėtinų sumų parametrai.  
- Šiame įraše naudojama demonstracinė įmonė USMF. Šiuos veiksmus paprastai atlieka mokėtinų sumų vadovo arba apskaitos vadovo vaidmuo. Prieš pradėdami įsitikinkite, kad pasirinktas SF gretinimo konfigūracijos raktas.


## <a name="prepare-to-create-vendor-invoice-policies"></a>Pasiruošti kurti tiekėjo SF strategijas
1. Pasirinkite **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.
2. Pasirinkite skirtuką **SF tikrinimas.**.
3. Pažymėkite arba atžymėkite žymės langelį **Automatically update invoice header**.
4. Pasirinkite **Gerai**.
5. Lauke **Post invoice with discrepancies** pasirinkite parinktį.
6. Uždarykite puslapį.
7. Eikite į **Valdymo skiltis > Moduliai > Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos**.
8. Pasirinkite **Parameters**.
9. Pasirinkite **Įtraukti**.
10. Norėdami grįžti į neregistruotų tabelių puslapį, uždarykite puslapį.

## <a name="create-policy-rule-types-for-vendor-invoices"></a>Kurti tiekėjo SF strategijos taisyklių tipus
1. Eikite į **Valdymo skiltį >Moduliai > Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos**.
2. Pasirinkite **Naujas**.
3. Įveskite reikšmes laukuose **Taisyklės vardas** ir **Aprašas**.
4. Lauke **Užklausos pavadinimas** spustelėkite išplečiamojo meniu mygtuką, kad atidarytumėte peržvalgą. Ją atidarę, pasirinkite norimą įrašą.
5. Pasirinkite **Įrašyti**.
6. Norėdami grįžti į neregistruotų tabelių puslapį, uždarykite puslapį.

## <a name="define-a-vendor-invoice-policy"></a>Apibrėžti tiekėjo SF strategiją
1. Eikite į **Valdymo skiltis > Moduliai > Mokėtinos sumos > Strategijos nustatymas > Tiekėjo SF strategijos**.
2. Pasirinkite **Naujas**.
3. Įveskite reikšmes laukuose **Profilis** ir **Aprašas**.
4. Išplėskite arba sutraukite **Policy organizations** dalį.
5. Medyje pasirinkite **Contoso Entertainment System USA**.
6. Pasirinkite **Įtraukti**.
7. Išplėskite arba sutraukite dalį **Policy rules**
8. Pasirinkite **Kurti strategijos taisyklę**.
9. Lauke **Policy rule description** surinkite reikšmę.
10. Pasirinkite **Filter**.
11. Pasirinkite **Įtraukti**. Pasirinkti aktyvų įrašą
12. Laukuose **Lentelė**,**Išvestinė lentelė** ir **Laukas** pasirinkite arba įveskite parinktis iš išplečiamojo meniu.
13. Uždarykite puslapį.
14. Lauke **Criteria**surinkite reikšmę.
15. Pasirinkite **Gerai**.
16. Pasirinkite **Gerai**.
17. Norėdami grįžti į neregistruotų tabelių puslapį, uždarykite puslapius.

