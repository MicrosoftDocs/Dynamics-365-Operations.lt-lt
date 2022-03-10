---
title: Pardavimo sutarčių įvedimas
description: Šioje temoje aiškinama, kaip sukurti pardavimo sutartį, kuri įpareigoja vieną iš jūsų klientų per tam tikrą laiką nusipirkti produktą už sutartą sumą mainais į specialias nuolaidas.
author: Henrikan
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm, SalesAgreementCustomerReferencesPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee2c1494842c5fd2aa598546ba655c33d6fd3f16
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/29/2021
ms.locfileid: "7568308"
---
# <a name="enter-sales-agreements"></a>Pardavimo sutarčių įvedimas

[!include [banner](../../includes/banner.md)]

Šioje temoje aiškinama, kaip sukurti pardavimo sutartį, kuri įpareigoja vieną iš jūsų klientų per tam tikrą laiką nusipirkti produktą už sutartą sumą mainais į specialias nuolaidas. Šią procedūrą galite vykdyti demonstracinėje duomenų įmonėje USMF arba su savo duomenimis.


## <a name="set-up-sales-agreement-header"></a>Pardavimo sutarties eilutės nustatymas
1. Naršymo srityje eikite į **Moduliai > Pardavimai ir rinkodara > Pardavimo sutartys > Pardavimo sutartys**.
2. Pasirinkite **Naujas**.
3. Lauke **Kliento sąskaita** išplečiamajame meniu pasirinkite norimą įrašą.
4. Lauke **Pardavimo sutarties klasifikacija** pasirinkite norimą įrašą iš išplečiamojo meniu.
5. Išplėskite skyrių **Bendra**.
6. Lauke **Numatytasis įsipareigojimas** pasirinkite **Produkto vertės įsipareigojimas**. Įsipareigojimo tipas yra privalomas kriterijus, kurį turite priskirti sutarčiai, kad nustatytumėte, kaip sutartis bus įvykdyta. Naudojant keturis iš anksto nustatytus tipus galima nustatyti kliento įsipareigojimo tikslą, kuris išreiškiamas kaip kiekis arba vertė. Kiekio įsipareigojimo tipą galima taikyti tik konkrečiam produktui, bet verte grįstus tipus galima taikyti parduodant konkrečius ir nekonkrečius produktus.  
7. Lauke **Galiojimo data** nustatykite datą į būsimą datą, kada norite, kad sutartis nebegaliotų.
8. Pasirinkite **Gerai**.

## <a name="set-up-product-value-commitment-lines"></a>Produkto vertės įsipareigojimo eilučių nustatymas
1. Pasirinkite **Pridėti eilutę**.
2. Lauke **Elemento numeris** išplečiamajame meniu pasirinkite norimą įrašą. Pasirinktas sutarties įsipareigojimo tipas įtakoja, kokią informaciją galite įvesti sutarties eilutėse. Pvz., jei sutartis pagrįsta verte, turite nurodyti bendrą grynąją sumą (sutarta valiuta), už kurią klientas įsipareigoja nusipirkti iš jūsų prekių. Šiame pavyzdyje laukai **Kiekis** ir **Vienetas** nepasiekiami eilutėje, nes kuriate sutartį klientui nusipirkti tam tikrą produkto vertę.   
3. Lauke **Grynoji suma** įveskite piniginę sumą, už kurią klientas įsipareigoja nusipirkti.
4. Lauke **Nuolaidos procentas** įveskite procentinę reikšmę, kuri bus taikoma kliento pardavimo užsakymo eilutėms, susietoms su šia sutartimi.
5. Išplėskite skyrių **Eilutės informacija** section.
6. Pasirinkite **Taip** lauke **Maksimaliai vykdoma**.
    - Pasirinkimas **Maksimaliai vykdoma** reiškia, kad bendra visų pardavimo užsakymo eilučių, kurios naudoja specialias įsipareigojimo kainas, nuolaidas ir (arba) mokėjimo sąlygas, suma neturi viršyti įsipareigojime nurodytos sumos.  
    - Mažiausia ir didžiausia išleidimo sumos nurodo vertės, už kurią reikia parduoti prekių vykdant kiekvieną pasirinktos sutarties pardavimo užsakymą, intervalą.   
7. Išplėskite skyrių **Pardavimo sutarties antraštė**. Jei sutarties būsena nėra nustatyta į **Galioja**, pardavimo užsakymai negali būti susieti su sutartimi ir dėl to negali prisidėti prie sutarties įvykdymo. Šio etapo metu būseną galite neautomatiškai pakeisti. Tačiau įprastai būsena keičiama tvirtinant kliento sutartį.  
8. Veiksmų srityje pasirinkite **Pardavimo sutartis**.
9. Pasirinkite **Patvirtinimas**. Įsitikinkite, kad parinktis **Pažymėti sutartį kaip galiojančią** nustatyta į **Taip**.  
10. Pasirinkite **Taip** lauke **Spausdinti ataskaitą**.
11. Pasirinkite **Gerai**.
12. Uždarykite puslapį. Dabar sutartis galioja. Galite pradėti sieti kliento užsakymus su sutartimi, kad subalansuotumėte atliktą tikslą.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]