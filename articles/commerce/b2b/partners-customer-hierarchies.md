---
title: B2B verslo partnerių valdymas naudojant klientų hierarchijas
description: Šiame straipsnyje aprašoma, kaip naudoti klientų hierarchijas Microsoft Dynamics 365 Commerce, siekiant valdyti verslo partnerius "verslas tarp verslų" (B2B) el. komercijos svetainių.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ddd02045b5df3ce20160a4feaa23339475823d3d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864986"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>B2B verslo partnerių valdymas naudojant klientų hierarchijas

[!include [banner](../../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip naudoti klientų hierarchijas Microsoft Dynamics 365 Commerce, siekiant valdyti verslo partnerius "verslas tarp verslų" (B2B) el. komercijos svetainių.

"Commerce Headquarters" klientų *hierarchijos* objektas naudojamas verslo partnerio organizacijoms, kurios naudos jūsų B2B el. komercijos svetainę, atstovauti. Prieš pradedant naudoti klientų hierarchijas verslo partneriams valdyti, "Commerce Headquarters" turite įgalinti B2B el. komercijos galimybes ir klientų hierarchijos numeraciją.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>Įjungti B2B el. komercijos funkciją "Commerce Headquarters"

Norėdami naudoti B2B el. prekybos galimybes, **pirmiausia turite įgalinti "Commerce Headquarters" funkciją Įgalinti B2B el** . komercijos galimybių naudojimą.

1. Eikite į **Darbo sritys \> Funkcijų valdymas**.
1. Skirtuke **Viskas** naudokite filtro lauką Moduliui: **Mažmeninė prekyba ir Prekyba ieškoti**.
1. Raskite **funkciją Įgalinti B2B eCommerce** pajėgumų naudojimą, pasirinkite ją, **tada** apatiniame dešiniajame kampe pasirinkite Įgalinti dabar.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>Nustatyti kliento hierarchijos numeraciją

Numeracija naudojama bendrųjų duomenų įrašų ir operacijų įrašų, kuriems reikia identifikatorių, nuskaitomiems unikaliems identifikatoriams sugeneruoti. Turite nurodyti numeraciją, kuri bus naudojama klientų hierarchijos ID generuoti. Daugiau informacijos apie numeracijas rasite [Numeracijų apžvalga](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview).

Norėdami "Commerce Headquarters" nustatyti klientų hierarchijos numeraciją, atlikite šiuos veiksmus.

1. Eikite į **"Retail" ir "\> Commerce \> Headquarters" nustatymų numeracijas \> Numeracijos**.
1. Sukurkite naują numeraciją arba pasirinkite esamą numeraciją dar kartą.
1. Eikite į **Mažmeninė prekyba ir prekyba \> „Headquarters“ sąranka \> Parametrai \> „Commerce“ bendrinami parametrai**.
1. Numeracijų **skirtuke** pridėkite numeraciją, kurią sukūrėte arba pasirinkote anksčiau, į kliento **hierarchijos ID** nuorodą.

![Numeracija įtraukta į kliento hierarchijos ID nuorodą.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>Kaip veikia patvirtinimo procesas

Kai verslo partneris reikalauja prisijungti prie B2B el. komercijos svetainės, sistema įrašo užklausą kaip potencialų *klientą*. "Commerce Headquarters" asmuo, pvz., mažmeninės prekybos operacijų vadovas, gali patvirtinti arba atmesti partnerio užklausas. Norėdami gauti daugiau informacijos apie tai, kaip valdyti verslo partnerio užklausas ir potencialių klientų patvirtinimus, [žr. Verslo partnerio vartotojų valdymas B2B el. komercijos žiniatinklio svetainėse](manage-b2b-users.md).

Patvirtinus potencialų klientą sistema sukuria du naujus kliento įrašus:

- Vienas organizacijos tipo kliento įrašas **rodo** organizaciją, prašančią tapti verslo partneriu.
- Vienas asmens tipo kliento **įrašas** rodo asmenį, kuris pateikė užklausą.

Be to, "Retail" ir "Commerce **Customer \> Customer" hierarchijos \> įrašuose sukuriamas naujas hierarchijos įrašas**. Šio klientų hierarchijos įrašo ypatybės yra tokios:

- **Klientų hierarchijos ID – unikalus klientų hierarchijos ID**. Šis ID naudoja numeraciją, kurią nustatote "Commerce" bendrinamuose parametruose.
- **Pavadinimas** – Verslo partnerio organizacijos pavadinimas, kaip nurodytas samdymo užklausoje. Šį lauką galima redaguoti.
- **Tikslas** – Ši nuosavybė yra nustatytas iš anksto nustatytai vertei **B2B organizacija**.
- **Organizacija** – verslo partnerio organizacijos kliento ID.

Asmuo, kuris pateikė gavimo užklausą, įtraukiamas į hierarchijos **"** FastTab", **o** jam priskiriamas administratoriaus vaidmuo. Kai administratorius įtraukia daugiau vartotojų į verslo partnerio organizaciją B2B svetainėje, kiekvienam vartotojui sukuriamas naujas kliento įrašas. Kliento įrašas taip pat įtraukiamas į atitinkamą verslo partnerio klientų hierarchijos įrašą ir **jam** priskiriamas vartotojo vaidmuo.

### <a name="examples"></a>Pavyzdžiai

Asmuo, pavadintas Sam J. "Microsoft" organizacijos vardu pateikia informacijos pateikimo prašymas. Patvirtinus užklausą sukuriami du nauji kliento abonementai: **vienas** iš Sam J asmens tipo ir vienas iš **"Microsoft"** organizacijos tipo.

Kaip parodyta pavyzdyje, taip pat sukuriamas naujas klientų hierarchijos įrašas. Šio įrašo pavadinimas toks pat kaip organizacijos (**"Microsoft"**), o **administratoriaus** vaidmuo priskiriamas Sam J. Kaip administratorius, Sam J. į šią hierarchiją įtraukia visus kitus "Microsoft" B2B svetainės vartotojus ir **priskiria** vartotoją jiems. Šiame pavyzdyje Sush R. buvo įtrauktas kaip vartotojas.

![Klientų hierarchijos įrašo pavyzdys.](../media/CustomerHierarchy2.png)

Norėdami nustatyti, ar klientas susietas su klientų hierarchija, atidarykite kliento įrašą. Kaip parodyta pavyzdyje, **klientų hierarchijos ID** **laukas B2B** **skyriuje, "Retail** FastTab" rodo, ar klientas yra klientų hierarchijos dalis, **o B2B** administratoriaus pasirinktis nurodo, ar klientas yra tos hierarchijos administratorius.

![Kliento įrašo "Retail FastTab" B2B skyriaus, kuriame klientas susietas su hierarchija ir nurodytas kaip administratorius, pavyzdys.](../media/CustomerHierarchyMapping2.png)

Daugeliu atvejų turėtų sutapti visų hierarchijos klientų įrašų ypatybių vertės. Pavyzdžiui, kadangi visi verslo partnerio vartotojai turėtų gauti panašias kainas už produktus, jų kainos grupė ir susieti konfigūravimai turėtų sutapti. Nepaisant to, sistema neįgalina tokio nuoseklumo. Dėl to, atitinkami „Commerce“ štabo vartotojai yra atsakingi už nuosavybės verčių ir konfigūravimo atitikimą visiems klientams toje hierarchijoje.

"Commerce Headquarters" vartotojai gali peržiūrėti visų klientų įrašų ypatybių vertes vieną šalia kitos rodinio hierarchijoje. Kaip pavyzdį **šiame** **pavyzdyje** galite naudoti pasirinktį Bendra, kurią rasite hierarchijos "FastTab" išplečiamajame sąraše Bendra, o tada pasirinkti bet kurį kliento įrašo skyrių, kad būtų rodomos susijusios ypatybės. Vartotojai gali redaguoti ypatybės vertes tiesiogiai šiame rodinyje. Norėdami kopijuoti visas vertes iš administratoriaus kliento įrašo visiems vartotojams, **pasirinkite Perrašyti hierarchijos** **·** "FastTab".

![Klientų hierarchijos įrašo pavyzdys, kuriame rodomas mygtukas Perrašyti ir pasirinktis išplečiamajame sąraše.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
