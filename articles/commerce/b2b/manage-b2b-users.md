---
title: Valdykite verslo partnerio vartotojus B2B el. komercijos svetainėse
description: Šioje temoje aprašoma, kaip administratoriai gali redaguoti, įtraukti ir naikinti verslo partnerio vartotojus verslo su verslu (B2B) el. komercijos svetainėse.
author: josaw1
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 090dc9af49840e559b4c1ad1500718fde9764aa2
ms.sourcegitcommit: 6bf9e18989e6d77497a9dda1c362f324b3c2fbf2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/27/2021
ms.locfileid: "7713698"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Valdykite verslo partnerio vartotojus B2B el. komercijos svetainėse

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip administratoriai gali redaguoti, įtraukti ir naikinti verslo partnerio vartotojus verslo su verslu (B2B) el. komercijos svetainėse.

B2B el. komercijos svetainėms reikia, kad organizacijos registruotųsi siekiant tapti verslo partneriais. Po to, kai organizacija pateikia išsamią registracijos informaciją B2B el. komercijos svetainei, ji pereina pro kvalifikavimo procesą. Jei organizacija yra sėkmingai kvalifikuota, ji yra įtraukiama kaip verslo partneris.

Po to, kai organizacija yra įtraukiama kaip verslo partneris, jos vartotojas pradėjęs užklausą tapti verslo partneriu yra nustatomas kaip administratorius vartotojas ir jam suteikiamos teisės papildomai įtraukti kitus įgaliotus B2B el. komercijos svetainės asmenis. Šie įgalioti vartotojai tuomet gali padaryti užsakymus verslo partnerio vardu.

## <a name="turn-on-the-b2b-e-commerce-capabilities-feature-in-commerce-headquarters"></a>Įjunkite B2B el. komercijos galimybių funkciją „Commerce“ štabe

B2B el. komercijos galimybių funkcija „Commerce“ štabe leidžia organizacijoms įtraukti verslo partnerius ir nustatyti administratorius vartotojus. Ši funkcija taip pat leidžia administratoriams kurti ir valdyti verslo partnerių vartotojus ir komandas bei priskirti jiems konkrečius vaidmenis. Galiausiai, jos leidžia verslo partnerio vartotojams kurti užsakymo šablonus ir naudoti esančius užsakymus siekiant iš naujo sutvarkyti produktus.

Norėdami įjungti B2B el. komercijos galimybių funkciją „Commerce“ štabe, atlikite šiuos žingsnius.

1. Eikite į **Darbo sritys \> Funkcijų valdymas**.
1. Skirtuke **Visi** filtruokite **Modulio** laukelį naudodami sąvoką **Mažmeninė prekyba ir komercija**.
1. Raskite ir pasirinkite funkciją pavadinimu **Įjungti B2B el. komercijos galimybių naudojimą** ir tuomet rinkitės **Įjungti dabar**.

## <a name="create-a-number-sequence-and-add-it-to-commerce-shared-parameters"></a>Kurkite skaičių seką ir įtraukite ją į „Commerce“ bendrintus parametrus

Numeracija naudojama bendrųjų duomenų įrašų ir operacijų įrašų, kuriems reikia identifikatorių, nuskaitomiems unikaliems identifikatoriams sugeneruoti. Daugiau informacijos apie numeracijas rasite [Numeracijų apžvalga](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Norėdami sukurti skaičių seką ir ją įtraukti į „Commerce“ bendrintus parametrus „Commerce“ štabe, imkitės šių veiksmų.

1. Eikite į **Mažmeninė prekyba ir komercija \> Štabo nustatymas \> Skaičių sekos \> Skaičių sekos** ir sukurkite skaičių seką.
1. Eikite į **Mažmena ir komercija \> Būstinės nustatymai \> Parametrai \> Bendrinti komercijos parametrai**, ir įtraukite naują skaičių seką į **Kliento hierarchijos ID** nuorodą.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Nustatykite administratorių vartotoją kaip naują verslo partnerį

Potencialus verslo partneris gali pradėti įtraukimo procesą į B2B el. komercijos svetainę pateikdamas įtraukimo užklausą per nuorodą saite. Kai potencialus verslo partnerio vartotojas pasirenka nuorodą, jis gali patiekti išsamią informaciją, kurios reikia įtraukimui ir prisijungimui. Pateikus užklausą, pasirodo pateikimo patvirtinimo puslapis. Jei pateikimas patvirtintas, užklausos teikėjas (kuris yra vartotojas pradėjęs įtraukimo užklausą) tampa verslo partnerio administratoriaus vartotoju.

Norėdami patvirtinti ir nustatyti verslo partnerio administratorių vartotoją „Commerce“ būstinėje, atlikite šiuos veiksmus.

1. Eikite į **Mažmenos ir komercijos IT \> Paskirstymo grafikas**.
1. Vykdykite **P-0001** darbą, kad ištrauktumėte visus verslo partnerio įtraukimo prašymus į „Commerce“ būstinę.
1. Po to, kai **P-0001** darbas buvo sėkmingai įvykdytas, eikite į **Mažmenos ir komercijos IT \> Klientas** ir vykdykite **Sinchronizuoti klientus ir verslo partnerius iš nesinchroninio režimo** darbo. Po to, kai šis darbas sėkmingai įvykdytas, įtraukimo prašymai sukuriami kaip perspektyvos įrašai „Commerce“ būstinėje. Laukelis **Tipo ID** šių įrašų yra nustatytas **B2B perspektyvoje**.
1. Eikite į **Klientai \> Visos perspektyvos** ir tada atverkite perspektyvų puslapį.
1. Rinkitės perspektyvos įrašą naujam verslo partneriui, kuris atvers perspektyvos išsamios informacijos puslapį.
1. Skirtuke **Bendri** rinkitės **Konvertuoti \> Tvirtinti/Atmesti** siekiant patvirtinti ar atmesti įtraukimo užklausą. Pasirodžius patvirtinimo pranešimui, tvirtinkite, kad norite tęsti procesą ir tvirtinti užklausą. El. paštas yra tuomet nusiunčiamas pareiškėjo el. pašto adresu siekiant patvirtinti, kad jo organizacija patvirtinta kaip verslo partneris.

    Kai patvirtinate užklausą, **Būsenos** perspektyvos įrašo laukelis yra nustatytas **Patvirtintu**. Taip pat, du nauji kliento įrašai yra sukuriami sistemoje: **Organizacijos tipo** kliento įrašas verslo partnerio organizacijai ir **Asmens tipas** kliento įrašo besikreipiančiam asmeniui (tai reiškia, verslo partnerio vartotojas, kuris pateikė užklausą). Kliento hierarchijos įrašas verslo partneriui taip pat sukuriamas. <!--(Please refer to the Org modeling of B2B customer section in this document for more information)-->

1. Eikite į **Mažmenos ir komercijos IT \> Platinimo grafikas** ir vykdykite **1010** (**Klientų**) darbą, kad stumtumėte naujai sukurtą klientą ir kliento hierarchijos įrašus į kanalo duomenų bazę.

Po to, kai užklausa patvirtinta ir klientas ir jo hierarchijos įrašai sinchronizuojami į kanalo duomenų bazę, užklausos teikėjas gali prisijungti prie B2B el. komercijos svetainės naudodamas el. pašto adresą patiektą pateikiant užklausą. Vartotojai gali naudoti prisijungimo eigą siekiant nustatyti slaptažodį jų paskyrai. Norėdami susieti tapatybės tiekėjo („Azure AD B2C”) įrašą su B2B kliento įrašu, sukurtu prisijungiant arba prisiregistruojant, vadovaukitės instrukcijomis, pateiktomis skyriuje [Įgalinti automatinį tapatybės įrašų susiejimą su klientų paskyromis](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>Pranešti apie B2B potencialius klientus, kai jie patvirtinami arba atmetami

Kai patvirtinsite arba atmesite B2B potencialaus kliento siuntimo užklausą, galėsite automatiškai siųsti pranešimą klientui el. paštu. 

Norėdami „Commerce Headquarters" nustatyti el. pašto pranešimus dėl įvykių, kurių potencialus klientas patvirtino B2B potencialų klientą, arba B2B potencialaus kliento atmesto pranešimo tipo, atlikite šiuos veiksmus.

1. Sukurkite el. laiškų, kurie bus siunčiami potencialaus kliento el. laiškams, šablonus, kai bus suaktyvintas B2B potencialaus kliento patvirtintas arba B2B potencialaus kliento atmestas pranešimo tipas.

    Norėdami gauti informacijos apie vietos rezervavimo ženklus, kuriuos B2B potencialus klientas patvirtino ir B2B potencialus klientas atmetė pranešimų tipus, žr. [pranešimų tipus](../email-templates-transactions.md#notification-types). Daugiau informacijos apie el. paštų šablonų kūrimą ieškokite skyriuje [El. pašto šablono kūrimas](../email-templates-transactions.md#create-an-email-template). 

1. Įtraukite B2B potencialaus kliento patvirtintą ir B2B potencialaus kliento atmestų pranešimų tipus į jūsų el. pašto pranešimų profilį ir susiekite juos su el. laiškų šablonais, kuriuos sukūrėte. Dėl išsamesnės informacijos, kaip nustatyti el. paštu siunčiamų pranešimų šablonus, ieškokite [El. paštu siunčiamo pranešimo šablono nustatykite](../email-notification-profiles.md). 

## <a name="onboard-additional-business-partner-users"></a>Įtraukimo papildomi verslo partnerio vartotojai

Verslo partnerio administratorius vartotojas gali įtraukti papildomus verslo partnerio vartotojus į B2B el. komercijos svetainę, kaip būtina.

Norėdami įtraukti papildomus verslo partnerio administratorius į vartotojus B2B el. komercijos svetainėje, imkitės šių veiksmų.

1. Prisijunkite prie B2B el. komercijos svetainės kaip administratorius.
1. Eikite į **Mano paskyra \> Organizacijos vartotojai \> Peržiūrėti informaciją** ir tada rinkitės **Įtraukti vartotoją**.
1. Įveskite būtiną informaciją ir tada rinkitės **Įrašyti**. Naujo vartotojo būsena nustatyta į **Laukianti**.

    Po to, kai **P-0001** ir **Sinchronizuoti klientus ir verslo partnerius iš nesinchroninio režimo** darbai yra vykdomi **Asmens tipo** kliento įraše naujam sukurtam vartotojui „Commerce“ būstinėje. Šis kliento įrašas taip pat susietas su svarbiu verslo partnerio kliento hierarchijos įrašu. Taip pat, el. laiškas nusiunčiamas naujam vartotojo el. pašto adresui, kad jį įspėtų, jog jie buvo įtraukti kaip verslo partnerio organizacijos vartotojai ir gali prisijungti prie B2B el. komercijos svetainės.

1. Vykdykite **1010** (**Klientų**) darbus siekiant sinchronizuoti naują verslo partnerio vartotoją į kanalo duomenų bazę.

Po to, kai kliento įrašas yra sinchronizuojamas, vartotojo būsena B2B el. komercijos svetainėje yra nustatyta į **Aktyvią** ir naujas vartotojas gali prisijungti prie B2B el. komercijos svetainės naudodamas savo el. pašto adresą. Vartotojai gali naudoti prisijungimo eigą siekiant nustatyti slaptažodį jų paskyrai. Norėdami susieti tapatybės tiekėjo („Azure AD B2C”) įrašą su B2B kliento įrašu, sukurtu prisijungiant arba prisiregistruojant, vadovaukitės instrukcijomis, pateiktomis skyriuje [Įgalinti automatinį tapatybės įrašų susiejimą su klientų paskyromis](../identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Redaguoti verslo partnerio vartotojo išsamią informaciją

Norėdami redaguoti verslo partnerio vartotojų išsamią informaciją, vadovaukitės šiais žingsniais.

1. Prisijunkite prie B2B el. komercijos svetainės kaip administratorius.
1. Eikite į **Mano paskyra \> Organizacijos vartotojai \> Peržiūrėti išsamią informaciją**, rinkitės **Redaguoti** mygtuką (pieštuko simbolis), atlikite būtinus pakeitimus ir tada rinkitės **Įrašyti**. Keitimai įsigalioji tik po to, kai **P-0001**, **Sinchronizuoti klientus ir verslo partnerius iš nesinchroninio režimo** ir **1010** (**Klientai**) darbai buvo vykdyti.

## <a name="remove-a-business-partner-user"></a>Pašalinti verslo partnerio vartotoją

Kaip būtina, administratorius gali pašalinti esančius verslo partnerio organizacijos vartotojus iš vartotojų sąrašo, kurie gali prieiti prie B2B el. komercijos svetainės.

Norėdami pašalinti verslo partnerio vartotoją, vadovaukitės šiais žingsniais.

1. Prisijunkite prie B2B el. komercijos svetainės kaip administratorius.
1. Eikite į **Mano paskyra \> Organizacijos vartotojai \> Peržiūrėti informaciją** ir tada rinkitės **Pašalinti** mygtuką („X“ simbolis). Pasirodžius patvirtinimo pranešimui, tvirtinkite, kad norite pašalinti vartotoją. Keitimai įsigalioja tik po to, kai **P-0001**, **Sinchronizuoti klientus ir verslo partnerius iš nesinchroninio režimo** ir **1010** (**Klientai**) darbai buvo vykdyti.

> [!NOTE]
> Jums pašalinus vartotoją iš vartotojų sąrašo, kurie gali prieiti prie B2B el. komercijos svetainės, atitinkamas kliento įrašas yra pašalinamas iš kliento partnerio kliento hierarchijos įrašo. Nepaisant to, kliento įrašas nėra panaikinamas iš „Commerce“ būstinės.

## <a name="onboard-business-partner-and-users-in-commerce-headquarters"></a>Įtraukimas verslo partneris ir vartotojai „Commerce“ būstinėje

Administratoriai gali įtraukti verslo partnerius ir vartotojus tiesiai „Commerce“ būstinėje.

Norėdami įtraukti verslo partnerius ir vartotojus tiesiai „Commerce“ būstinėje, atlikite šiuos veiksmus.

1. Kurkite **Tipo organizacija** kliento įrašą verslo partnerio organizacijai.
1. Kurkite **Tipo asmuo** kliento įrašus verslo partnerio vartotojams. Įsitikinkite, kad pirminis el. pašto adresas yra nurodytas kiekvienam klientui.
1. Kiekvienam **Tipui asmens** kliento įrašas turi būti paskirtas kaip administratoriaus vartotojas verslo partnerio organizacijai, **Mažmenos** „FastTab“, nustatykite **B2B administratoriaus** parinktį į **Taip**.
1. Kurkite kliento hierarchijos ID. Tada lauke **Pavadinimas** įveskite pavadinimą.
1. Laukelyje **Organizacija** įveskite verslo partnerio organizacijai klientą.
1. Rinkitės **Įtraukti** ir tada rinkitės klientą **Pavadinimo** laukelyje.
1. Kartokite šį veiksmą, kad įtrauktumėte papildomus klientus į hierarchiją.

## <a name="additional-information"></a>Papildoma informacija

- Visi darbai paminėti šioje temoje gali būti konfigūruojami siekiant vykdyti grafiką paketo formate. Lūkesčiai, kad verslo partneris konfigūruos paketo darbus yra būtinas.
- Dabar tik vienas vartotojas ar kliento įrašas gali būti paskirtas kaip administratoriaus vartotojas ir tas vaidmuo gali būti keičiamas tik „Commerce“ štabe. Esama palaikymo savitarnos paslaugų galimybėms, kurios leidžia verslo partneriams nustatyti kelis administratorius ar keisti administratorius B2B el. komercijos svetainėms.
<!--- The modules and labels of the different fields referenced in the screenshots for e-commerce are only for illustration purposes. Customers have complete control on the placement of the B2B related modules and the labels.-->
- Nepaisant to, kad išlaidų apribojimus gali nustatyti vartotojai, jų įgalinimas užsakymo metu įrašo tvarkymas dar nėra įgyvendintas.
- Visa verslo logika ir patvirtinimas vartotojo patirčiai B2B el. komercijos svetainėje yra paremtas konfigūravimu kliento įrašui, kuris patalpintas į žemėlapį, kurį vartotojas turi „Commerce“ štabe.

## <a name="additional-resources"></a>Papildomi ištekliai

[Nustatykite B2B el. komercijos saitą](set-up-b2b-site.md)

[Kurkite organizacijos modeliavimo hierarchijas B2B organizacijoms](org-model.md)

[Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams](payment-method.md)

[Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams](quantity-limits.md)

[Numeracijų apžvalga](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
