---
title: Valdyti verslo partnerio vartotojus B2B el. komercijos žiniatinklio svetainėse naudojant "Dynamics 365" pardavimą
description: Šiame straipsnyje aprašoma, kaip naudoti Microsoft Dynamics 365 pardavimą siekiant tvarkyti verslo partnerio patvirtinimus "Verslas Dynamics 365 Commerce verslui" (B2B) žiniatinklio svetainėms.
author: ShalabhjainMSFT
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.search.industry: retail
ms.search.form: ''
ms.openlocfilehash: d178e619fca7915286181aa803376cd564f60a26
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278657"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Valdyti verslo partnerio vartotojus B2B el. komercijos žiniatinklio svetainėse naudojant "Dynamics 365" pardavimą

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti Microsoft Dynamics 365 pardavimą siekiant tvarkyti verslo partnerio patvirtinimus "Verslas Dynamics 365 Commerce verslui" (B2B) žiniatinklio svetainėms. Organizacijos, jau investuotos į "Dynamics 365" pardavimo sprendimą, gali naudoti savo galimų klientų ir galimybių sąvokas B2B el. komercijos verslo partnerio patvirtinimo procesui.

B2B verslo partnerio patvirtinimo proceso foninės informacijos ieškokite [B2B el. komercijos žiniatinklio svetainėse tvarkykite verslo partnerio vartotojus](manage-b2b-users.md).

Potencialūs verslo partneriai gali inicijuoti iniciavimo procesą B2B el. komercijos svetainėje, pateikdami atkavimo užklausą naudodami B2B svetainės saitą. Kai užklausa pateikta ir atitinkamos užduotys (**pvz., P-0001** **ir sinchronizuoti užsakymus ir kanalo užklausas) paleidžiamos "Commerce Headquarters**", **"Commerce Headquarters**" puslapyje "Visi potencialūs klientai" įrašomi tarpinių užklausų. Tada verslo partnerio potencialaus kliento patvirtinimo procesą galima užbaigti lauke Pardavimas.

Kai įgalintas pardavimo ir komercijos integravimas, commerce sukūrus verslo partnerio potencialų klientą pardavimas bus sukurtas *kaip* galimas klientas.

Šiame pavyzdyje pateikiamas pardavimo verslo partnerio potencialaus kliento potencialaus kliento galimų klientų kūrimo puslapio pavyzdys.

![Galimo kliento kūrimo puslapis "Dynamics 365" pardavimas.](../media/LeadInSales.png)

Pavyzdyje kontaktinis **asmuo parodomas** asmuo, kuris pateikė užklausą dėl darbo, **o įmonės skyrius** rodo organizaciją. Laiko juostos skyriaus pastaba **nurodo**, kad galimą klientą sugeneravo dvigubo rašymo infrastruktūra. Kadangi jį sukūrė dvigubo įrašymo infrastruktūra, šis galimas klientas nebus rodomas išplečiamajame **sąraše** Mano atidaryti galimi klientai. Vietoj to jis bus rodomas naujame rodinyje, pavadintame "Visi komercijos **B2B galimi klientai"**.

Standartiniam galimų klientų kvalifikacijos procesui pardavimo metu, kai vartotojas "kvalifikuos" galimą klientą, *galimybės* įrašą, *·* *kontakto* įrašą ir sąskaitos įrašą. Dvigubo rašymo infrastruktūra naudojama įrašyti kontaktą ir sąskaitos įrašus į Commerce. Kontaktas kuriamas kaip asmens tipo *klientas*, o įmonė kuriama kaip organizacijos tipo *klientas*. Jei vartotojas galimybės atveju pasirenka Uždaryti kaip laimėta **, potencialus klientas patvirtinamas**"Commerce". Patvirtinus potencialų klientą bus sukurta klientų hierarchija.

Visi likę verslo procesai įvyksta "Commerce". Šie procesai apima el. laiškų siuntimą verslo partneriui, vartotojų kredito limito valdymo apibrėžimą ir daugiau vartotojų įtraukimą į B2B svetainę. Tačiau, jei vartotojas diskvalifikuoja galimą klientą arba pažymi galimybę kaip prarastą, o ne reiškia galimo kliento įvertinimą, "Commerce" potencialus klientas pažymimas kaip atmestas, o klientui siunčiamas atmetimo el. laiškas, skirtas klientui.

## <a name="enable-integration-between-sales-and-commerce"></a>Įgalinti integravimą tarp pardavimo ir komercijos

Integravimas tarp pardavimų ir komercijos remiasi dvigubo rašymo infrastruktūra. Dėl to turi būti įgalintas dvigubas rašymas ir darbas, kad klientai, sukurti vienoje sistemoje, būtų įrašyti į kitą sistemą. Daugiau informacijos apie dvigubo rašymo infrastruktūrą ieškokite dvigubo [rašymo peržiūra](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview).

Baigus dvigubo rašymo nustatymą, diegimo partneris [Microsoft AppSource](https://appsource.microsoft.com/)[gali ieškoti sprendimo, pavadinto dvigubo rašymo "Commerce" sprendimais](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview). Įdiekite paketą naudodami standartinį diegimo vedlį, tada, sukurdami potencialų klientą B2B svetainėje, patikrinkite jį. Kai potencialus klientas sukuriamas, patikrinkite, **ar užklausa rodoma visuose potencialaus kliento duomenyse, o tada patikrinkite, ar potencialus klientas yra rodomas kaip galimas pardavimo klientas**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Valdykite verslo partnerio vartotojus B2B el. komercijos svetainėse](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
