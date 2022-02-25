---
title: Valdykite verslo partnerio vartotojus B2B el. komercijos svetainėse
description: Šioje temoje aprašoma, kaip įtraukti, Microsoft Dynamics 365 Commerce naikinti ir redaguoti verslo partnerio vartotojus "Business-To-Business" (B2B) el. komercijos žiniatinklio svetainėse ir "Commerce Headquarters".
author: josaw1
ms.date: 02/17/2022
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
ms.openlocfilehash: def8d4de082ceb4be77ed7e8898cbef82d52b749
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323460"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites"></a>Valdykite verslo partnerio vartotojus B2B el. komercijos svetainėse

[!include [banner](../../includes/banner.md)]

Šioje temoje aprašoma, kaip įtraukti, Microsoft Dynamics 365 Commerce naikinti ir redaguoti verslo partnerio vartotojus "Business-To-Business" (B2B) el. komercijos žiniatinklio svetainėse ir "Commerce Headquarters".

> [!NOTE]
> B2B [verslo partnerių valdymas, naudojant klientų hierarchijų](partners-customer-hierarchies.md) temą, yra šio dokumento būtina sąlyga. 

B2B el. komercijos svetainėms reikia, kad organizacijos registruotųsi siekiant tapti verslo partneriais. Kai organizacija pateikia registracijos informaciją B2B el. komercijos svetainei, registracijos užklausa vyksta kvalifikacijos procese. Jei organizacija yra sėkmingai kvalifikuota, ji yra įtraukiama kaip verslo partneris.

Po to, kai organizacija yra įtraukiama kaip verslo partneris, jos vartotojas pradėjęs užklausą tapti verslo partneriu yra nustatomas kaip administratorius vartotojas ir jam suteikiamos teisės papildomai įtraukti kitus įgaliotus B2B el. komercijos svetainės asmenis. Šie įgalioti vartotojai tuomet gali padaryti užsakymus verslo partnerio vardu.

## <a name="set-up-the-administrator-user-for-a-new-business-partner"></a>Nustatykite administratorių vartotoją kaip naują verslo partnerį

Potencialūs verslo partneriai gali inicijuoti iniciavimo procesą B2B el. komercijos svetainėje, pateikdami atkavimo užklausą naudodami B2B svetainės saitą. Tada jie gali naudoti pritaikomą formą norėdami pateikti informaciją, kuri reikalinga norint įvesti ir registruotis. Pateikus užklausą, pasirodo pateikimo patvirtinimo puslapis. Jei pateikimas patvirtintas, įmonė, kuri buvo pateikta dėl užklausos, tampa verslo partneriu, o užklausos prašymas (vartotojas, inicijavontis užklausą) tampa verslo partnerio administratoriaus vartotojas.

Norėdami patvirtinti verslo partnerio užklausą "Commerce Headquarters", atlikite šiuos veiksmus.

1. Eikite į **Mažmenos ir komercijos IT \> Paskirstymo grafikas**.
1. Vykdykite **P-0001** darbą, kad ištrauktumėte visus verslo partnerio įtraukimo prašymus į „Commerce“ būstinę.
1. Sėkmingai paleidus **P-0001** užduotį, **eikite į "Retail" ir "Commerce IT \> "** klientą ir **vykdykite užduotį Sinchronizuoti klientus ir kanalų užklausas**. Sėkmingai paleidus šią užduotį, veiklos planavimo užklausos sukuriamos kaip "Commerce Headquarters **" B2B** potencialių klientų tipo potencialūs klientai. 
1. Eikite į **Klientų \> visus potencialius klientus** ir pasirinkite naujo verslo partnerio potencialaus kliento įrašą, kad atidarytumėte potencialaus kliento informacijos puslapį.
1. Skirtuke **Bendra pasirinkite** Konvertuoti patvirtinti **\>/ Atmesti,** kad patvirtintuumėte indavimo užklausą. Kai pasirodo patvirtinimo pranešimas, patvirtinkite, kad norite tęsti procesą, ir patvirtinkite užklausą. Patvirtinimo lauke Potencialaus **kliento** įrašas esantis būsena pasikeičia į **Patvirtinta**. El. paštas yra tuomet nusiunčiamas pareiškėjo el. pašto adresu siekiant patvirtinti, kad jo organizacija patvirtinta kaip verslo partneris. Taip pat sukuriama klientų hierarchija, kur užklausos prašymas įtraukiamas kaip verslo partnerio administratorius.

    > [!NOTE]
    > Šiuo metu patvirtinimo el. laiškas iš karto siunčiamas patvirtinus. Tačiau "Commerce" funkcijos leidžia administratoriui rankiniu būdu paleisti el. laiškus.

1. Pereikite į " **Retail" ir "Commerce IT \> Distribution**" grafiką ir **paleiskite 1010 (klientai)** užduotį, norėdami į kanalų duomenų bazę perstumti naujus klientų ir klientų hierarchijos įrašus.

> [!NOTE]
> Siekiant užtikrinti, kad į kanalo duomenų bazę siunčiami nauji kliento įrašai, bent viena su klientu susijusi adresų knygelė turėtų būti įtraukta į klientų adresų knyg knygę, susietą su interneto parduotuve. Galite automatizuoti šį procesą konfigūruodami numatytosios interneto parduotuvės kliento adresų knyg knygę, kad sistema kopijuoja adresų knygelės vertę kiekvienam naujam klientui.

Kai klientų hierarchijos įrašai sinchronizuojami su kanalo duomenų baze, užklausos prašymas gali prisijungti prie B2B el. komercijos svetainės, naudodamas el. pašto adresą, kuris buvo pateiktas jiems pateikiant eilę. Vartotojai gali naudoti prisijungimo eigą siekiant nustatyti slaptažodį jų paskyrai. Informacijos, kaip įgalinti Azure Active Directory (Azure AD) B2C tapatybės tiekėjo įrašą susieti su B2B kliento įrašu, kuris buvo sukurtas tvirtinant potencialų klientą, [ieškokite Įgalinti automatinį susiejimą](../identity-record-linking.md).

## <a name="notify-b2b-prospects-when-they-are-approved-or-rejected"></a>Pranešti apie B2B potencialius klientus, kai jie patvirtinami arba atmetami

Kai patvirtinate arba atmetate B2B potencialaus kliento inkasavimo užklausą, potencialaus kliento el. paštu siunčiamas pranešimas gali būti automatiškai siunčiamas.

Norėdami "Commerce Headquarters" nustatyti el. pašto pranešimus dėl įvykių, kurių potencialus klientas **patvirtino B2B potencialų klientą, arba B2B** **potencialaus** kliento atmesto pranešimo tipo, atlikite šiuos veiksmus.

1. Sukurkite el. laiškų **, kurie bus siunčiami potencialaus kliento el. laiškams, šablonus, kai bus suaktyvintas B2B** **potencialaus kliento patvirtintas arba B2B potencialaus** kliento atmestas pranešimo tipas. Informacijos apie vietos rezervavimo ženklus, kuriuos palaiko šie pranešimų tipai, ieškokite pranešimų [tipai.](../email-templates-transactions.md#notification-types) Daugiau informacijos apie el. paštų šablonų kūrimą ieškokite skyriuje [El. pašto šablono kūrimas](../email-templates-transactions.md#create-an-email-template).
1. Įtraukite **B2B potencialaus** **kliento patvirtintą ir B2B** potencialaus kliento atmestų pranešimų tipus į jūsų el. pašto pranešimų profilį, tada susiekite juos su el. laiškų šablonais, kuriuos sukūrėte. Dėl išsamesnės informacijos, kaip nustatyti el. paštu siunčiamų pranešimų šablonus, ieškokite [El. paštu siunčiamo pranešimo šablono nustatykite](../email-notification-profiles.md).

## <a name="onboard-additional-business-partner-users"></a>Įtraukimo papildomi verslo partnerio vartotojai

Verslo partnerio administratorius vartotojas gali įtraukti papildomus verslo partnerio vartotojus į B2B el. komercijos svetainę, kaip būtina.

Norėdami įtraukti papildomus verslo partnerio administratorius į vartotojus B2B el. komercijos svetainėje, imkitės šių veiksmų.

1. Prisijunkite prie B2B el. komercijos svetainės kaip administratorius.
1. Eikite į **Mano paskyra \> Organizacijos vartotojai \> Peržiūrėti informaciją** ir tada rinkitės **Įtraukti vartotoją**.
1. Įveskite būtiną informaciją ir tada rinkitės **Įrašyti**. Naujo vartotojo būsena nustatyta į **Laukianti**.

**Paleidus P-0001** **ir Sinchronizuoti klientų ir kanalo užklausų užduotis,** **"Commerce Headquarters" sukuriamas** naujo vartotojo asmens tipo kliento įrašas. Šis kliento įrašas taip pat susietas su svarbiu verslo partnerio kliento hierarchijos įrašu. Taip pat, el. laiškas nusiunčiamas naujam vartotojo el. pašto adresui, kad jį įspėtų, jog jie buvo įtraukti kaip verslo partnerio organizacijos vartotojai ir gali prisijungti prie B2B el. komercijos svetainės.

Tada paleiskite **1010 (klientų)** užduotį sinchronizuoti naują verslo partnerio vartotoją su kanalo duomenų baze.

Po to, kai kliento įrašas sinchronizuojamas, vartotojo būsena B2B el. komercijos **svetainėje** yra aktyvi ir naujas vartotojas gali prisijungti B2B el. komercijos svetainėje naudodamas savo el. pašto adresą. Vartotojai gali naudoti prisijungimo eigą siekiant nustatyti slaptažodį jų paskyrai. Informacijos, kaip įgalinti Azure AD B2C tapatybės tiekėjo įrašą susieti su B2B kliento įrašu, sukurtu "Commerce Headquarters", [ieškokite Įgalinti automatinį susiejimą](/dynamics365/commerce/identity-record-linking.md).

## <a name="edit-business-partner-user-details"></a>Redaguoti verslo partnerio vartotojo išsamią informaciją

Norėdami redaguoti verslo partnerio vartotojų išsamią informaciją, vadovaukitės šiais žingsniais.

1. Prisijunkite prie B2B el. komercijos svetainės kaip administratorius.
1. Eikite į **Mano paskyra \> Organizacijos vartotojai \> Peržiūrėti išsamią informaciją**, rinkitės **Redaguoti** mygtuką (pieštuko simbolis), atlikite būtinus pakeitimus ir tada rinkitės **Įrašyti**. Pakeitimai įsigalioja tik po to, kai **P-0001**, **sinchronizuoti klientų ir kanalų užklausas** ir **vykdyti 1010 (klientų)** užduotis.

## <a name="remove-a-business-partner-user"></a>Pašalinti verslo partnerio vartotoją

Kaip būtina, administratorius gali pašalinti esančius verslo partnerio organizacijos vartotojus iš vartotojų sąrašo, kurie gali prieiti prie B2B el. komercijos svetainės.
Norėdami pašalinti verslo partnerio vartotoją, vadovaukitės šiais žingsniais.
- Prisijunkite prie B2B el. komercijos svetainės kaip administratorius.
- Eikite **į Dalį Mano > organizacijos vartotojų \>** peržiūrėti informaciją ir pasirinkite mygtuką **Pašalinti** ("X" simbolis). Pasirodžius patvirtinimo pranešimui, tvirtinkite, kad norite pašalinti vartotoją. Pakeitimas įsigalioja tik po to, kai P-0001 **,** sinchronizuoti klientų ir kanalų užklausas ir **1010 (klientų)** užduotys yra **paleistos**.

> [!NOTE]
> Jums pašalinus vartotoją iš vartotojų sąrašo, kurie gali prieiti prie B2B el. komercijos svetainės, atitinkamas kliento įrašas yra pašalinamas iš kliento partnerio kliento hierarchijos įrašo. Nepaisant to, kliento įrašas nėra panaikinamas iš „Commerce“ būstinės.

## <a name="onboard-existing-customers-as-business-partners-on-the-b2b-e-commerce-website"></a>Esamų klientų, kaip verslo partnerių B2B el. komercijos svetainėje, svetainė

Administratoriai gali įtraukti verslo partnerius ir vartotojus tiesiai „Commerce“ būstinėje. Ši galimybė naudinga norint savo esamus verslo partnerius įtraukti į "B2B" el. komercijos svetainę.

Norėdami įtraukti verslo partnerius ir vartotojus tiesiai „Commerce“ būstinėje, atlikite šiuos veiksmus.

1. Sukurkite arba pasirinkite organizacijos tipo klientą **,** norimą įtraukti kaip verslo partnerį.
1. Sukurkite arba pasirinkite asmens tipo klientą **, kurį** norite įtraukti kaip verslo partnerio administratorius arba vartotojas. Įsitikinkite, kad pagrindiniai el. pašto adresai yra susieti su klientais. Šie el. pašto adresai naudojami norint prisijungti prie svetainės. 

    > [!NOTE]
    > Sistema turi turėti galimybę rasti unikalų kliento įrašą vartotojams, kurie turėtų turėti galimybę prisijungti svetainėje. Jei sistema suranda daugiau nei vieną klientą, kurio pagrindinis el. pašto adresas juridiniame subjekte yra tas pats, vartotojas negalės prisiregistruoti svetainėje.

1. Kurkite kliento hierarchijos ID.
1. Lauke **Pavadinimas** įveskite pavadinimą.
1. Laukelyje **Organizacija** įveskite verslo partnerio organizacijai klientą.
1. Hierarchijos **"** FastTab" pasirinkite **Įtraukti**.
1. **Lauke Vardas** pasirinkite asmens tipo **klientą**.
1. Pasirinkite kliento **,** kuris turėtų būti paskirtas administratoriumi, administratoriaus vaidmenį.
1. Pakartokite šį procesą, norėdami į hierarchiją įtraukti daugiau klientų.

## <a name="additional-information"></a>Papildoma informacija

- Visi darbai paminėti šioje temoje gali būti konfigūruojami siekiant vykdyti grafiką paketo formate. Lūkesčiai, kad verslo partneris konfigūruos paketo darbus yra būtinas.
- Dabar tik vienas vartotojas ar kliento įrašas gali būti paskirtas kaip administratoriaus vartotojas ir tas vaidmuo gali būti keičiamas tik „Commerce“ štabe. Esama palaikymo savitarnos paslaugų galimybėms, kurios leidžia verslo partneriams nustatyti kelis administratorius ar keisti administratorius B2B el. komercijos svetainėms.
- Nepaisant to, kad išlaidų apribojimus gali nustatyti vartotojai, jų įgalinimas užsakymo metu įrašo tvarkymas dar nėra įgyvendintas.
- Visa verslo logika ir patvirtinimas vartotojo patirčiai B2B el. komercijos svetainėje yra paremtas konfigūravimu kliento įrašui, kuris patalpintas į žemėlapį, kurį vartotojas turi „Commerce“ štabe.

## <a name="additional-resources"></a>Papildomi ištekliai

[B2B el. prekybos svetainės nustatymas](set-up-b2b-site.md)

[Valdyti B2B verslo partnerius naudojant klientų hierarchijas](partners-customer-hierarchies.md)

[Konfigūruoti kliento sąskaitos mokėjimo metodą B2B el. komercijos saitams](payment-method.md)

[Nustatykite produkto kiekio apribojimus B2B el. komercijos saitams](quantity-limits.md)

[Numeracijų apžvalga](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
