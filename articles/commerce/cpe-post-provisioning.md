---
title: „Dynamics 365 Commerce“ vertinimo aplinkos konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip sukonfigūruoti Microsoft Dynamics 365 Commerce įvertinimo aplinką po jos konfigūravimo.
author: psimolin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 19d88139e35554bce68bc6203141957b96e439a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892335"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a>„Dynamics 365 Commerce“ vertinimo aplinkos konfigūravimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip sukonfigūruoti Microsoft Dynamics 365 Commerce įvertinimo aplinką po jos konfigūravimo.

Atlikite šiame straipsnyje nurodytas procedūras tik su nustatę savo komercijos vertinimo aplinką. Dėl informacijos, kaip nustatyti savo Komercijos vertinimo aplinką po jos nustatymo, žr. [Komercijos vertinimo aplinkos nustatymas](provisioning-guide.md).

Po to kai jūsų Komercijos vertinimo aplinka buvo parengta iki galo, papildomas jos parengimo konfigūravimo žingsniai turi būti pateikti iki tol, kol pradėsite vertinti aplinką. Norėdami atlikti šiuos veiksmus, turite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS) ir „Dynamics 365 Commerce“.

## <a name="before-you-start"></a>Prieš pradedant

1. Prisijunkite prie [LCS portalo](https://lcs.dynamics.com).
1. Nueikite į savo projektą.
1. Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.
1. Sąraše pasirinkite savo aplinką.
1. Aplinkos informacijoje dešinėje, pasirinkite **Prisijungti prie aplinkos**. Būsite nukreipti į komercijos būstinę.
1. Įsitikinkite, kad viršutiniame dešiniajame kampe pasirinktas juridinis subjektas **USRT**.
1. Eikite **į "\>** **Commerce" parametrų konfigūracijos parametrus ir įsitikinkite, kad yra ProductSearch.UseAzureSearch** **įrašas ir kad nustatyta reikšmė Teisinga**. Jei nėra šio įrašo, galite jį įtraukti, **nustatyti** reikšmę teisinga ir pasirinkti "Commerce **\> Scale" vieneto,** susieto su jūsų el. komercijos svetaine, kanalo duomenų bazės visą duomenų sinchronizavimą.
1. Eikite į " **Retail" ir "Commerce \> Headquarters" \> nustatymą "Commerce Scheduler \> Initialize Commerce scheduler"**. Inicijuokite **"Commerce Scheduler**" iškeliamą meniu, nustatykite parinktį **Naikinti esamą konfigūraciją** **kaip Taip**, tada pasirinkite **Gerai**.
1. Norėdami įtraukti kanalus į "Commerce Scale Unit", **eikite į "Retail" ir "Commerce Headquarters \>" sąranką "Commerce \> Scheduler \> Channel" duomenų** bazę, tada kairiojoje srityje pasirinkite "Commerce Scale Unit". **"Retail" kanale** "FastTab" įtraukite **interneto parduotuvę AW**, **AW verslo interneto** **parduotuvę ir Fabrikam išplėstinius interneto parduotuvės kanalus**. Pasirinktinai galite įtraukti parduotuves, jei naudojate EKA (pvz., Seattle, **San Francisco** ir **San Jose**). **·**

Po parengimo veiksmų komercijos būstinėje, įsitikinkite, kad **USRT** juridinis asmuo yra visuomet pasirinktas.

## <a name="configure-the-point-of-sale"></a>Sukonfigūruokite prekybos tašką

### <a name="associate-a-worker-with-your-identity"></a>Darbuotojo susiejimas su jūsų tapatybe

Tam, kad susietumėte darbuotoją su savo tapatybe, atlikite šiuos veiksmus Komercijos būstinėje.

1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Darbuotojai \> Darbininkai**.
1. Sąraše raskite ir pasirinkite šį įrašą **000713 - Andrew Collette**.
1. Veiksmų juostoje pasirinkite **Komercija**.
1. Pasirinkite **Susieti esamą tapatybę**.
1. Lauko **Ieškoti naudojant el. paštą** dešinėje esančiame lauke **El. paštas** įveskite savo el. pašto adresą.
1. Pasirinkite **Ieškoti**.
1. Pasirinkite įrašą su savo vardu.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Įrašyti**.

### <a name="activate-cloud-pos"></a>Aktyvinti debesies EKA

„Cloud POS“ įjungimui, atlikite šiuos veiksmus LCS.

1. Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.
1. Sąraše pasirinkite savo aplinką.
1. Aplinkos informacijoje dešinėje, pasirinkite **Prisijungti prie debesies prekybos taško**.
1. Pasirinkite **Kitas** tam, kad atvertumėte **Prieš pradžią** teksto laukelį.
1. Palikite **Serverio URL** laukelį tokį, koks yra. Pasirinkite **Toliau**.
1. Prisijunkite naudodami savo „Microsoft Azure Active Directory“ („Azure AD“) paskyrą.
1. **Parduotuvės pavadinimo** laukelyje pasirinkite **San Franciskas** ir tuomet pasirinkite **Kitas**.
1. Dalyje **Registras ir įrenginys** pasirinkite **SANFRAN-1**.
1. Pasirinkite **Aktyvinti**. Esate atjungiami ir nukreipiami į EKA prisijungimo puslapį.
1. Dabar galite prisijungti prie debesies EKA funkcijų naudodami operatoriaus ID **000713** ir slaptažodį **123**.

## <a name="set-up-your-site-in-commerce"></a>Svetainės nustatymas programoje „Commerce“

Jūsų vertinimo vietos komercijoje nustatymo pradžiai, atlikite šiuos žingsnius.

1. Prisijunkite prie vietos kūrėjo naudodami URL, kurį užsirašėte pradėdami „e-Commerce“ parengimo metu (žr. [Pradėti „e-Commerce“](provisioning-guide.md#initialize-e-commerce)).
1. Pasirinkite svetainę **„Fabrikam“**, kad atidarytumėte svetainės sąrankos dialogo langą.
1. Pasirinkite domeną, kurį įvedėte inicijuodami el. prekybą.
1. Kaip numatytąjį kanalą pasirinkite **„Fabrikam“ išplėstinė internetinė parduotuvė**. (Įsitikinkite, kad pasirinkote **išplėstinę** internetinę parduotuvę.)
1. Kaip numatytąją kalbą pasirinkite **lt-lt**.
1. Lauko **Kelias** reikšmę palikite tokią, kokia yra.
1. Pasirinkite **Gerai**. Atsiranda svetainės puslapių sąrašas.
1. Svetainei (kuri nukreipia į AW interneto parduotuvės kanalą) ir verslo svetainei (**AdventureWorks** kuri nukreipia į AW **verslo** interneto parduotuvės kanalą) **AdventureWorks** pakartokite veiksmus nuo 2 iki 7 **.** **Jei Fabrikam svetainės laukas Path** yra tuščias, turite pridėti dviejų teritorijų maršrutus AdventureWorks (pvz., "aw" ir "awbusiness").

## <a name="enable-jobs"></a>Užduočių įgalinimas

Norėdami programoje „Commerce“ įjungti užduotis, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie aplinkos (būstinėje).
1. Naudodami kairėje esantį meniu, nueikite į **Mažmeninė prekyba ir prekyba \> Užklausos ir ataskaitos \> Paketines užduotys**.

    Likusius šios procedūros veiksmus reikia atlikti su kiekviena iš tolesnių užduočių.

    * Apdoroti mažmeninės prekybos el. paštu siunčiamą pranešimą
    * Produkto prieinamumas
    * P-0001
    * Užsakymų sinchronizavimo užduotis

1. Naudodami spartųjį filtrą, užduoties galite ieškoti pagal pavadinimą.
1. Jei darbo būsena yra **Vykdoma**, atlikite šiuos žingsnius:

    1. Pasirinkite įrašą.
    1. Veiksmų srities skirtuke **Paketinė užduotis** pasirinkite **Keisti būseną**.
    1. Pasirinkite **Atšaukti**, tuomet pasirinkite **Gerai**.

1. Jei užduoties būsena yra **Išskaitta**, atlikite šiuos veiksmus:

    1. Pasirinkite įrašą.
    1. Veiksmų srities skirtuke **Paketinė užduotis** pasirinkite **Keisti būseną**.
    1. Pasirinkite **Laukiama**, tada – **Gerai**.

Pasirinktinai, taip pat galite nustatyti sutapimo intervalą ties (1) minute šiems veiksmams:

* Mažmenos užsakymo elektroninio pašto pranešimo darbo apdorojimas
* P-0001 darbas
* Užsakymų sinchronizavimo užduotis

### <a name="run-full-data-synchronization"></a>Vykdyti visą duomenų sinchronizavimą

Visų duomenų sinchronizavimo komercijoje vykdymui, atlikite šiuos veiksmus komercijos būstinėje.

1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Būstinės sąranka \> Prekybos tvarkaraštis \> Kanalo duomenų bazė**.
1. Pasirinkite kanalą pavadinimu **scXXXXXXXXX**.
1. Veiksmų srityje pasirinkite **Visas duomenų sinchronizavimas**.
1. Įveskite **9999** kaip paskirstymo grafiką.
1. Pasirinkite **Gerai**.
1. Pasirinkite **Gerai**.

### <a name="test-credit-card-information-to-do-test-purchases"></a>Bandomosios kredito kortelės informacija bandomiesiems pirkimams atlikti

Norėdami svetainėje atlikti bandomąsias operacijas, galite naudoti tolesnę bandomosios kredito kortelės informaciją.

- **Kortelės numeris:** 4111-1111-1111-1111
- **Galiojimo pabaigos data:** 10/30
- **Kortelės tikrinimo vertės (CVV) kodas:** 737

> [!IMPORTANT]
> Bandomojoje svetainėje niekada esant jokioms aplinkybėms nenaudokite faktinės kredito kortelės informacijos.

## <a name="next-steps"></a>Kiti veiksmai

Po parengimo ir konfigūravimo žingsnių atlikimo, galite pradėti naudoti savo vertinimo aplinką. Naudokite komercijos vietos kūrėjo URL tam, kad eitumėte į autorizavimo patirtį. Naudokite komercijos vietos kūrėjo URL tam, kad eitumėte į mažmenos kliento vietos patirtį.

Tam, kad sukonfigūruotumėte pasirenkamas jūsų Komercijos vertinimo aplinkos savybes, žr. [Konfigūruoti pasirenkamas savybes savo Komercijos vertinimo aplinkoje](cpe-optional-features.md).

> [!NOTE]
> Į „Commerce” vertinimo aplinkas yra iš anksto įkeltas „Azure Active Directory“ („Azure AD)” verslas – vartotojui (B2C) nuomotojas demonstraciniais tikslais. Vertinimo aplinkose nėra būtina konfigūruoti savo „Azure AD B2C” nuomotojo. Tačiau jeigu norėdami naudoti savo „Azure AD” B2C nuomotoją konfigūruojate vertinimo aplinką, naudodami „Azure” portalą į „Azure AD” B2C programą būtinai įtraukite ``https://login.commerce.dynamics.com/_msdyn365/authresp`` kaip atsakymo URL.

## <a name="troubleshooting"></a>Trikčių šalinimas

### <a name="site-builder-channel-list-is-empty-when-configuring-site"></a>Konfigūruojant svetainę svetainės generatoriaus kanalų sąrašas tuščias

Jei svetainės generatorius nerodo jokių interneto parduotuvės kanalų, būstinėje įsitikinkite, kad kanalai buvo įtraukti į "Commerce Scale Unit [", kaip aprašyta anksčiau skyriuje Prieš pradedant](#before-you-start) pradėti. Taip pat paleiskite **"Commerce Scheduler"** naudodami nustatytą **naikinti esamą** konfigūracijos reikšmę kaip **Taip**.  Kai šie veiksmai atlikti, **kanalo** duomenų bazės puslapyje ("Retail" ir "Commerce Headquarters **" nustatymas "\> Commerce \> Scheduler \> Channel"** duomenų bazė) **paleiskite 9999** užduotį "Commerce Scale Unit".

### <a name="color-swatches-are-not-rendering-on-the-category-page-but-are-rendering-on-the-product-details-page-pdp-page"></a>Spalvų nepastebėjimo negalima atvaizduoti kategorijos puslapyje, bet jie atvaizduojami produkto informacijos puslapyje (PDP) puslapyje

Norėdami užtikrinti, kad spalvos ir dydžio sekės yra nustatytos patikslinti, atlikite šiuos veiksmus.

1. Būstinėje eikite į "Retail" **ir "Commerce Channel" \> nustatymo kanalo \> kategorijas ir produktų atributus**.
1. Kairiajame lange pasirinkite interneto parduotuvės kanalą, tada pasirinkite Nustatyti atributo **metaduomenis**.
1. Nustatykite **atributą Rodyti kanalo pasirinktį** **kaip Taip**, nustatykite parinktį **Galima patikslinti** **– Taip**, tada pasirinkite **Įrašyti**. 
1. Grįžkite į interneto parduotuvės kanalo puslapį ir pasirinkite Publikuoti **kanalo naujinimus**.
1. Pereikite prie **"Retail" ir "Commerce \> Headquarters" nustatymo \> "Commerce Scheduler \> Channel** **" duomenų bazės ir paleiskite 9999** užduotį "Commerce Scale Unit".

### <a name="business-features-dont-appear-to-be-turned-on-for-the-adventureworks-business-site"></a>Verslo priemonės neįjungtos verslo AdventureWorks svetainėje

Būstinę įsitikinkite, kad interneto parduotuvės kanalas sukonfigūruotas, kai **kliento tipas nustatytas** kaip **B2B**. **Jei nustatytas kliento** tipas **B2C**, reikia sukurti naują kanalą, nes esamo kanalo redaguoti negalima. 

Demonstracinis duomenys, išsiųsti "Commerce" versijoje 10.0.26 **ir anksčiau, buvo klaida, kai buvo netinkamai sukonfigūruotas "AW Business"** internetinės saugyklos kanalas. Darbo būdas skirtas kurti naują kanalą, kurio **parametrai** ir konfigūracijos yra tokie patys, išskyrus kliento tipą, kuris turi būti nustatytas kaip **B2B**.

## <a name="additional-resources"></a>Papildomi ištekliai

[„Dynamics 365 Commerce“ vertinimo aplinkos peržiūra](cpe-overview.md)

[Parenkite „Dynamics 365 Commerce“ vertinimo aplinką](provisioning-guide.md)

[Konfigūruokite pasirinktas savybes „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-optional-features.md)

[Sukonfigūruokite „BOPIS“ „Dynamics 365 Commerce“ vertinamoje aplinkoje](cpe-bopis.md)

[„Dynamics 365 Commerce“ vertinimo aplinkos DUK](cpe-faq.md)

[„Microsoft Lifecycle Services“ (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[„Retail Cloud Scale Unit“ (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[„Microsoft Azure“ portalas](https://azure.microsoft.com/features/azure-portal)

[„Dynamics 365 Commerce“ svetainė](https://aka.ms/Dynamics365CommerceWebsite)

[„Commerce” B2C nuomotojo sąranka](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
