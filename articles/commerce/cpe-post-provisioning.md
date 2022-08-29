---
title: „Dynamics 365 Commerce“ smėlio dėžės aplinkos konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip sukonfigūruoti Microsoft Dynamics 365 Commerce sandūrų aplinką po jos konfigūravimo.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: ae6a8c63721ac32f525e1846a10c0b2caeb08f9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270378"
---
# <a name="configure-a-dynamics-365-commerce-sandbox-environment"></a>„Dynamics 365 Commerce“ smėlio dėžės aplinkos konfigūravimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje paaiškinama, kaip sukonfigūruoti Microsoft Dynamics 365 Commerce sandūrų aplinką po jos konfigūravimo.

Atlikite šiame straipsnyje nurodytas procedūras tik su nustatę "Commerce sandbox" aplinką. Daugiau informacijos apie "Commerce sandbox" aplinkos parengimą rasite " [Commerce sandbox" aplinkoje](provisioning-guide.md).

Konfigūruojant "Commerce sandbox" aplinką iki pabaigos turi būti atlikti papildomi po konfigūravimo naudojami konfigūracijos veiksmai, prieš pradedant naudoti aplinką. Norėdami atlikti šiuos veiksmus, turite naudoti „Microsoft Dynamics Lifecycle Services“ (LCS) ir „Dynamics 365 Commerce“.

## <a name="before-you-start"></a>Prieš pradedant

1. Prisijunkite prie [LCS portalo](https://lcs.dynamics.com).
1. Nueikite į savo projektą.
1. Sąraše pasirinkite savo aplinką.
1. Aplinkos informacijoje dešinėje, pasirinkite **Prisijungti prie aplinkos**. Būsite nukreipti į komercijos būstinę.
1. Įsitikinkite, kad viršutiniame dešiniajame kampe pasirinktas juridinis subjektas **USRT**. Šis juridinis subjektas buvo iš anksto sukonfigūruotas demonstraciniai duomenyse.
1. Eikite **į "\>** **Commerce" parametrų konfigūracijos parametrus ir įsitikinkite, kad yra ProductSearch.UseAzureSearch** **įrašas ir kad nustatyta reikšmė Teisinga.** Jeigu šio įrašo nėra, pridėkite jį ir nustatykite vertę kaip **teisingą**.
1. Eikite į " **Retail" ir "Commerce \> Headquarters" \> nustatymą "Commerce Scheduler \> Initialize Commerce scheduler"**. Inicijuokite **"Commerce Scheduler**" iškeliamą meniu, nustatykite parinktį **Naikinti esamą konfigūraciją** **kaip Taip**, tada pasirinkite **Gerai**.
1. Kad parduotuvės ir el. prekybos kanalai veiktų tinkamai, jie turi būti įtraukti į "Commerce Scale Unit". Pereikite prie " **Retail" ir "Commerce \> Headquarters" nustatymo \> "Commerce Scheduler \> Channel**" duomenų bazės, tada kairiojoje srityje pasirinkite "Commerce Scale Unit". **"Retail" kanale** "FastTab" įtraukite interneto parduotuvę AW **,** AW verslo **interneto** parduotuvę ir Fabrikam išplėstinius interneto parduotuvės kanalus **,** jei planuojate naudoti šiuos el. prekybos kanalus. Pasirinktinai galite įtraukti ir parduotuves, jei naudojate kasos taškus (EKA) (pvz., **Seattle**, **San Francisco** ir / arba **San Jose**).
1. Norėdami užtikrinti, kad visi pakeitimai sinchronizuoti su kanalo duomenų baze, pasirinkite " **Commerce \> Scale Unit" kanalo** duomenų bazės visą duomenų sinchronizavimą.

Po parengimo veiksmų komercijos būstinėje, įsitikinkite, kad **USRT** juridinis asmuo yra visuomet pasirinktas.

## <a name="configure-the-point-of-sale"></a>Sukonfigūruokite prekybos tašką

### <a name="associate-a-worker-with-your-identity"></a>Darbuotojo susiejimas su jūsų tapatybe

Tam, kad susietumėte darbuotoją su savo tapatybe, atlikite šiuos veiksmus Komercijos būstinėje.

1. Naudodami kairėje esantį meniu, nueikite į **Moduliai \> Mažmeninė prekyba ir prekyba \> Darbuotojai \> Darbininkai**.
1. Sąraše raskite ir pasirinkite šį įrašą **000713 - Andrew Collette**. Šis pavyzdys– vartotojas yra susietas su San Francisco parduotuve, kuri bus naudojama kitame skyriuje.
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

## <a name="set-up-your-e-commerce-sites"></a>Nustatyti savo el. komercijos svetaines

Yra trys galimos el. komercijos demonstracinės svetainės: Fabrikam, Adventure Works ir Adventure Works Business. Norėdami sukonfigūruoti kiekvieną demonstracinę svetainę, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie vietos kūrėjo naudodami URL, kurį užsirašėte pradėdami „e-Commerce“ parengimo metu (žr. [Pradėti „e-Commerce“](provisioning-guide.md#initialize-e-commerce)).
1. Norėdami atidaryti svetainės nustatymo dialogo langą, pasirinkite svetainę (**Fabrikam**, **Adventure** Works **arba Adventure Works Business**).
1. Pasirinkite domeną, kurį įvedėte inicijuojant "Commerce".
1. Būstinoje pasirinkite iš anksto sukonfigūruotą interneto parduotuvės kanalą (**Fabrikam išplėstinę** interneto parduotuvę, **AW** **interneto parduotuvę arba AW verslo** interneto parduotuvę), kuri atitinka numatytąjį kanalą.
1. Kaip numatytąją kalbą pasirinkite **lt-lt**.
1. Konfigūruoti maršruto laukus. Tai gali būti palikta tuščia vienoje svetainėje, bet ją reikės sukonfigūruoti, jei kelios teritorijos turės tokį patį domeno pavadinimą. Pavyzdžiui, `https://www.constoso.com` jei domeno pavadinimas yra, Adventure Works () galite naudoti tuščią Fabrikam (`https://contoso.com`) maršrutą ir Adventure Works (`https://contoso.com/aw`) naudoti "aw" bei Adventure Works verslo svetainės () "awbusiness"`https://contoso.com/awbusiness`.
1. Pasirinkite **Gerai**. Atsiranda svetainės puslapių sąrašas.
1. Pasirinktinai pakartokite 2–7 žingsnius, kad konfigūruokite kitas parodomas svetaines pagal poreikį.

## <a name="enable-jobs"></a>Užduočių įgalinimas

Norėdami programoje „Commerce“ įjungti užduotis, atlikite toliau nurodytus veiksmus.

1. Prisiregistruokite prie būstinės aplinkos.
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

Baigus konfigūravimo ir konfigūravimo veiksmus, galima pradėti naudoti sandūrų aplinką. Naudokite komercijos vietos kūrėjo URL tam, kad eitumėte į autorizavimo patirtį. Naudokite komercijos vietos kūrėjo URL tam, kad eitumėte į mažmenos kliento vietos patirtį.

Norėdami konfigūruoti pasirinktines "Commerce sandbox" aplinkos funkcijas, žr. " [Commerce sandbox" aplinkos pasirinktinių funkcijų konfigūravimas](cpe-optional-features.md).

Norint įgalinti el. komercijos vartotojus prisiregistruoti prie el. komercijos svetainės, reikia papildomos konfigūracijos, Azure Active Directory kad būtų galima įgalinti svetainės autentifikavimą tarp vartotojų (B2C). Norėdami gauti daugiau instrukcijų [, komercijoje nustatykite B2C nuomininką](set-up-b2c-tenant.md).

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

[Sandėlio Dynamics 365 Commerce aplinkos parengimas](provisioning-guide.md)

[Konfigūruokite pasirinktines sandūrų Dynamics 365 Commerce aplinkos priemones](cpe-optional-features.md)

[Konfigūruoti BOPIS sandūrų Dynamics 365 Commerce saugyklos aplinkoje](cpe-bopis.md)

[„Microsoft Lifecycle Services“ (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[„Retail Cloud Scale Unit“ (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[„Microsoft Azure“ portalas](https://azure.microsoft.com/features/azure-portal)

[„Dynamics 365 Commerce“ svetainė](https://aka.ms/Dynamics365CommerceWebsite)

[„Commerce” B2C nuomotojo sąranka](set-up-B2C-tenant.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
