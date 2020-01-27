---
title: „Commerce“ peržiūros aplinkos parengimas
description: Šioje temoje paaiškinama, kaip parengti „Microsoft Dynamics 365 Commerce“ peržiūros aplinką.
author: psimolin
manager: annbe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934753"
---
# <a name="provision-a-commerce-preview-environment"></a>„Commerce“ peržiūros aplinkos parengimas

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šioje temoje paaiškinama, kaip parengti „Microsoft Dynamics 365 Commerce“ peržiūros aplinką.

Prieš pradedant rekomenduojame bent peržvelgti visą šią temą, kad suprastumėte, koks tai procesas ir kas aprašoma šioje temoje.

> [!NOTE]
> Jei dar negavote prieigos prie „Dynamics 365 Commerce“ peržiūros, galite prašyti prieigos prie peržiūros [„Commerce“ svetainėje](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Peržiūrėti

Norėdami sėkmingai parengti savo „Commerce“ peržiūros aplinką, turite sukurti projektą, kuriame būtų konkretaus produkto pavadinimas ir tipas. Aplinka ir „Retail Cloud Scale Unit“ (RCSU) taip pat turi tam tikrų konkrečių parametrų, kuriuos turite naudoti, vėliau parengdami „e-Commerce“. Šios temos instrukcijose aprašomi visi būtini veiksmai, kuriuos turite atlikti, ir parametrai, kuriuos turite naudoti.

Sėkmingai parengę „Commerce“ peržiūros aplinką, turite atlikti keletą veiksmų po parengimo, kad ją paruoštumėte. Kai kurie veiksmai yra pasirinktiniai, atsižvelgiant į tai, kokius sistemos aspektus norite įvertinti. Visada galite atlikti pasirinktinius veiksmus vėliau.

Informacijos apie tai, kaip sukonfigūruoti „Commerce“ peržiūros aplinką po to, kai ją parengsite, rasite skyriuje [„Commerce“ peržiūros aplinkos konfigūravimas](cpe-post-provisioning.md). Informacijos apie tai, kaip sukonfigūruoti „Commerce“ peržiūros aplinkos pasirinktines funkcijas, rasite skyriuje [„Commerce“ peržiūros aplinkos pasirinktinių funkcijų konfigūravimas](cpe-optional-features.md).

Jei turite klausimų dėl parengimo veiksmų arba kyla problemų, praneškite apie tai „Microsoft“ [„Microsoft Dynamics 365 Commerce“ peržiūros „Yammer“ grupėje](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Būtinieji komponentai

Toliau pateikiamos būtinosios sąlygos turi būti įvykdytos prieš parengiant „Commerce“ peržiūros aplinką.

- Turite prieigą prie „Microsoft Dynamics Lifecycle Services“ (LCS) portalo.
- Buvote priimti į „Dynamics 365 Commerce“ peržiūros programą.
- Turite reikiamas teises kurti **Galimi išankstiniai pardavimai** arba **Perkelti, kurti sprendimus ir sužinoti** projektą.
- Esate vaidmens **Aplinkos administratorius** arba **Projekto savininkas** narys projekte, kuriame parengsite aplinką.
- Turite administratoriaus prieigą prie savo „Microsoft Azure“ prenumeratos arba galite susisiekti su prenumeratos administratoriumi, kuris gali atlikti du veiksmus, reikalaujančius administratoriaus teisių, jūsų vardu.
- Turite savo „Azure Active Directory“ („Azure AD“) nuomotojo ID.
- Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip „e-Commerce“ sistemos administratoriaus grupė, ir turite jos ID.
- Sukūrėte „Azure AD“ saugos grupę, kuri gali būti naudojama kaip įvertinimų ir apžvalgų moderatoriaus grupė, ir turite jos ID. (Ši saugos grupė gali sutapti su „e-Commerce“ sistemos administravimo grupe.)

### <a name="find-your-azure-ad-tenant-id"></a>„Azure AD“ nuomotojo ID radimas

Jūsų „Azure AD“ nuomotojo ID yra visuotinai unikalų identifikatorius (GUID), panašus į šį pavyzdį: **„72f988bf-86f1-41af-91ab-2d7cd011db47“**.

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a>„Azure AD“ nuomotojo ID radimas „Azure“ portale

1. Prisijunkite prie [„Azure“ portalo](https://portal.azure.com/).
1. Įsitikinkite, kad pasirinktas tinkamas katalogas.
1. Kairėje esančiame meniu pasirinkite **„Azure Active Directory“**.
1. Dalyje **Valdyti** pasirinkite **Ypatybės**. „Azure AD“ nuomotojo ID rodomas dalyje **Katalogo ID**.

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a>„Azure AD“ nuomotojo ID radimas naudojant OpenID „Connect“ metaduomenis

Sukurkite OpenID URL, pakeitę **\{YOUR\_DOMAIN\}** savo domenu, pvz., `microsoft.com`. Pavyzdžiui, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` taps `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.

1. Eikite į OpenID URL, kuriame nurodytas jūsų domenas.

    Savo „Azure AD“ nuomotojo ID rasite keliose ypatybių vertėse.

1. Raskite **authorization\_endpoint** ir išskleiskite GUID, rodomą iškart po `login.microsoftonline.com/`.

### <a name="find-your-azure-ad-security-group-id"></a>„Azure AD“ saugos grupės ID radimas

„Azure AD“ saugos grupės ID yra GUID, panašus į šį pavyzdį: **„436ea7f5-ee6c-40c1-9f08-825c5811066a“**.

Atliekant šią procedūrą laikoma, kad esate grupės, kurios ID bandote rasti, narys.

1. Atidarykite [„Graph“ naršyklę](https://developer.microsoft.com/graph/graph-explorer#).
1. Pasirinkite **Prisijungti naudojant „Microsoft“** ir prisijunkite, naudodami savo kredencialus.
1. Kairėje pasirinkite **rodyti daugiau pavyzdžių**.
1. Dešiniojoje srityje įjunkite **Grupės**.
1. Uždarykite dešiniąją sritį.
1. Pasirinkite **visos grupės, kurioms priklausau**.
1. Lauke **Atsakymo peržiūra** raskite savo grupę. Saugos grupės ID rodomas po ypatybės **„id“**.

## <a name="provision-your-commerce-preview-environment"></a>Jūsų „Commerce“ peržiūros aplinkos parengimas

Šiose procedūrose paaiškinama, kaip parengti „Commerce“ peržiūros aplinką. Sėkmingai jas atlikus, „Commerce“ peržiūros aplinka bus paruošta konfigūruoti. Visos čia aprašytos veiklos vyksta LCS portale.

> [!IMPORTANT]
> Peržiūros prieiga yra susieta su LCS paskyra ir organizacija, kurią nurodėte prašyme dėl peržiūros. Norėdami parengti „Commerce“ peržiūros aplinką, turite naudoti tą pačią paskyrą. Jei „Commerce“ peržiūros aplinkoje tenka naudoti kitą LCS paskyrą arba nuomotoją, turite pateikti šiuos duomenis įmonei „Microsoft“. Kontaktinės informacijos ieškokite toliau šioje temoje, skyriuje [„Commerce“ peržiūros aplinkos palaikymas](#commerce-preview-environment-support).

### <a name="grant-access-to-e-commerce-applications"></a>Prieigos prie el. prekybos programų suteikimas

> [!IMPORTANT]
> Prisijungiantis asmuo turi būti „Azure AD“ nuomotojo administratorius, kuris turi „Azure AD“ nuomotojo ID. Jei šis veiksmas nebus sėkmingai atliktas, nepavyks atlikti kitų parengimo veiksmų.

Norėdami įgalioti „e-Commerce“ programas pasiekti „Azure“ prenumeratą, atlikite toliau nurodytus veiksmus.

1. Sudėliokite URL toliau pateikiamu formatu.

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. Nukopijuokite ir įklijuokite URL į naršyklę arba teksto rengyklę ir pakeiskite **\{AAD\_TENANT\_ID\}** į savo „Azure AD“ nuomotojo ID. Tuomet atidarykite URL.
1. Prisijungimo prie „Azure AD“ dialogo lange prisijunkite ir patvirtinkite, kad **Dynamics 365 Commerce (Peržiūra)** norite suteikti prieigą prie prenumeratos. Pamatysite puslapį, kuriame nurodoma, ar operacija buvo sėkminga.

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>Patvirtinimas, kad peržiūros funkcijos prieinamos ir įjungtos LCS

Norėdami patvirtinti, kad peržiūros funkcijos yra prieinamos ir įjungtos LCS, atlikite toliau pateikiamus veiksmus.

1. Prisijunkite prie [LCS portalo](https://lcs.dynamics.com), naudodami LCS paskyrą, kurią naudojote prašydami suteikti prieigą prie peržiūros.
1. LCS pagrindiniame puslapyje slinkite į dešinę iki pat galo ir pasirinkite plytelę **Peržiūros versijos funkcijų valdymas**.

    ![Peržiūros versijos valdymo plytelė](./media/preview1.png)

1. Slinkite žemyn iki **Asmeninės peržiūros funkcijos** ir patvirtinkite, kad toliau pateikiamos funkcijos yra galimos ir įjungtos.

    - El. prekybos vertinimas
    - „Commerce“ peržiūros programos aplinkos

    ![Privačiosios vertinimo versijos funkcijos](./media/preview2.png)

1. Jei šios funkcijos sąraše nerodomos, susisiekite su „Microsoft“ ir pateikite savo darbo el. pašto adresą, LCS paskyrą ir nuomotojo informaciją. Kontaktinės informacijos ieškokite skyriuje [„Commerce“ peržiūros aplinkos palaikymas](#commerce-preview-environment-support).

### <a name="create-a-new-project"></a>Kurti naują projektą

Norėdami sukurti naują projektą LCS, atlikite toliau pateikiamus veiksmus.

1. LCS pagrindiniame puslapyje pasirinkite pliuso ženklą (**„+“**), kad sukurtumėte projektą.
1. Dešiniojoje srityje atlikite vieną iš toliau pateikiamų veiksmų.

    - Jei esate partneris, pasirinkite **Perkelti, kurti sprendimus ir sužinoti**.
    - Jei esate klientas, pasirinkite **Galimas išankstinis pardavimas**.

1. Įveskite pavadinimą, aprašą ir pramonės šaką.
1. Lauke **Produkto pavadinimas** pasirinkite **Dynamics 365 Retail**.
1. Lauke **Produkto versija** pasirinkite **Dynamics 365 Retail**.
1. Lauke **Metodika** pasirinkite **„Dynamics Retail“ visuotinio diegimo metodika**.
1. Pasirinktinai: galite importuoti vaidmenis ir vartotojus iš esamo projekto.
1. Pasirinkite **Kurti**. Pateikiamas projekto rodinys.

### <a name="add-the-azure-connector"></a>„Azure“ jungties įtraukimas

Norėdami įtraukti „Azure“ jungti į savo LCS projektą, atlikite toliau nurodytus veiksmus.

1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei esate partneris, pasirinkite plytelę **Projekto parametrai** dešinės pusės gale.
    - Jei esate klientas, viršutiniame meniu pasirinkite **Projekto parametrai**.

1. Pasirinkite **„Azure“ jungtys**.
1. Pasirinkite **Įtraukti**, norėdami įtraukti „Azure“ jungtį.
1. Įvesti vardą.
1. Įveskite savo „Azure“ prenumeratos ID.
1. Įjunkite parinktį **Konfigūruoti, kad būtų galima naudoti „Azure“ išteklių tvarkytuvą (ARM)**.
1. Įsitikinkite, kad vertė **„Azure“ prenumeratos AAD nuomotojo domenas ( arba ID)** yra tinkama. Pagal poreikį kreipkitės į „Azure“ prenumeratos administratorių.
1. Pasirinkite **Toliau**.
1. Sekite puslapyje pateikiamas instrukcijas, kad suteiktumėte reikiamoms programoms prieigą prie jūsų prenumeratos. Pagal poreikį kreipkitės į „Azure“ prenumeratos administratorių.

    1. Prisijunkite prie [„Azure“ portalo](https://portal.azure.com/).
    1. Įsitikinkite, kad pasirinktas tinkamas katalogas, o tada kairėje esančiame meniu pasirinkite **Prenumeratos**.
    1. Sąraše raskite tinkamą prenumeratą ir ją pasirinkite. Pagal poreikį naudokite ieškos funkciją.
    1. Meniu pasirinkite **Prieigos valdymas (IAM)**.
    1. Dešinėje, dalyje **Įtraukti vaidmens priskyrimą** pasirinkite **Įtraukti**. Rodoma sritis **Įtraukti vaidmens priskyrimą**.
    1. Lauke **Vaidmuo** pasirinkite **Bendraautorius**.
    1. Lauke **Priskirti prieigą prie** palikite numatytąją reikšmę, **„Azure AD“ vartotojas, grupė arba paslaugos narys**.
    1. Dalyje **Pasirinkti** įveskite **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Sąraše pasirinkite **„Dynamics Deployment Services“ \[wsfed-enabled\]**.
    1. Pasirinkite **Įrašyti**.

1. Pasirinkite **Toliau**.
1. Sekite puslapyje pateikiamas instrukcijas, kad suteiktumėte reikiamoms programoms prieigą prie jūsų prenumeratos. Pagal poreikį kreipkitės į „Azure“ prenumeratos administratorių.
1. Pasirinkite **Toliau**.
1. Lauke **„Azure“ regionas** pasirinkite **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2**.
1. Pasirinkite **Prisijungti**. Jūsų „Azure“ jungtis turi pasirodyti sąraše.

### <a name="import-the-commerce-preview-demo-base-extension"></a>„Commerce“ peržiūros demonstracinio pagrindinio plėtinio importavimas

Norėdami importuoti „Commerce“ peržiūros demonstracinį pagrindinį plėtinį į savo projektą, atlikite toliau nurodytus veiksmus.

1. Atidarykite projekto pagrindinį puslapį, pasirinkę projekto pavadinimą viršuje.
1. Atlikite vieną iš toliau nurodytų veiksmų.

    - Jei esate partneris, pasirinkite plytelę **Turto biblioteka** dešinės pusės gale.
    - Jei esate klientas, viršutiniame meniu pasirinkite **Turto biblioteka**.

1. Pasirinkite **Programinės įrangos diegimo paketas** iš sąrašo kairėje pusėje.
1. Pasirinkite **Importuoti**.
1. Dalyje **Bendrai naudojamo turto biblioteka** turto sąraše pasirinkite **„Commerce“ peržiūros demonstracinis pagrindinis plėtinys**.
1. Pasirinkite **Paimti**. Grįšite į turto biblioteką ir turėtumėte matyti plėtinį sąraše.

Toliau pateikiamoje iliustracijoje parodyti veiksmai, kurių reikia imtis LCS puslapyje **Turto biblioteka**.

![„Commerce“ peržiūros demonstracinio pagrindinio plėtinio importavimas](./media/import.png)

### <a name="deploy-the-environment"></a>Aplinkos diegimas

Atlikite toliau pateikiamus veiksmus, norėdami įdiegti aplinką.

> [!NOTE]
> Gali būti, kad nereikės atlikti 6, 7 ir (arba) 8 veiksmų, nes puslapiai, kuriuose yra viena parinktis, praleidžiami. Rodinyje **Aplinkos parametrai** patvirtinkite, kad tekstas **„Dynamics 365 Commerce“ (Peržiūra) – Demonstracinė versija (10.0.6 su 30 platformos naujinimu)** rodomas tiesiai virš lauko **Aplinkos pavadinimas**. Žr. iliustraciją, pateikiamą po 8 veiksmo.

1. Viršutiniame meniu pasirinkite **Aplinkos diegimo debesyje įrankis**.
1. Pasirinkite **Įtraukti**, kad įtrauktumėte aplinką.
1. Lauke **Programos versija** pasirinkite **10.0.6**.
1. Lauke **Platformos versija** pasirinkite **30 platformos naujinimas**.

    ![Programos ir platformos versijų pasirinkimas](./media/project1.png)

1. Pasirinkite **Toliau**.
1. Pasirinkite aplinkos topologiją **Demonstracinė versija**.

    ![1 aplinkos topologijos pasirinkimas](./media/project2.png)

1. Pasirinkite aplinkos topologiją **„Dynamics 365 Commerce“ (Peržiūra) – Demonstracinė versija**. Jei anksčiau sukonfigūruosite vieną „Azure“ jungtį, ji bus naudojama šioje aplinkoje. Jei sukonfigūravote keletą „Azure“ jungčių, galite pasirinkti, kurią jungtį naudoti: **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2**. (Geriausiam betarpiškam našumui užtikrinti rekomenduojame pasirinkti **Vakarų JAV 2**.)

    ![2 aplinkos topologijos pasirinkimas](./media/project3.png)

1. Puslapyje **Diegti aplinką** įveskite aplinkos pavadinimą. Nekeiskite išplėstinių parametrų.

    ![Puslapis Diegti aplinką](./media/project4.png)

1. Pagal poreikį pakoreguokite VM dydį. (Rekomenduojame VM sandėliavimo vienetą \[SKU\] **„D13 v2“**.)
1. Peržiūrėkite kainodaros ir licencijavimo sąlygas, tada pažymėkite žymės langelį, kad patvirtintumėte, jog su jomis sutinkate.
1. Pasirinkite **Toliau**.
1. Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Diegti**. Grįšite į rodinį **Aplinkos diegimo debesyje įrankis**, o jūsų aplinka turėtų būti rodoma sąraše.

    Jūsų pageidaujama aplinka bus rodoma eilėje ir paskui diegiama. Aplinkos darbo eigoms užbaigti prireiks laiko. Todėl patikrinkite vėl maždaug po šešių–devynių valandų.

1. Prieš tęsdami įsitikinkite, kad jūsų aplinkos būsena yra **Įdiegta**.

### <a name="initialize-rcsu"></a>Paleiskite RCSU.

Norėdami inicijuoti RCSU, atlikite toliau nurodytus veiksmus.

1. Rodinyje **Aplinkos diegimo debesyje įrankis** sąraše pasirinkite savo aplinką.
1. Aplinkos rodinyje dešinėje pasirinkite **Visa išsami informacija**. Rodomas aplinkos išsamios informacijos rodinys.
1. Dalyje **Aplinkos funkcijos** pasirinkite **Valdyti**.
1. Skirtuke **„Retail“** pasirinkite **Inicijuoti**. Rodomas RCSU inicijavimo parametrų rodinys.
1. Lauke **Regionas** pasirinkite **Rytų JAV**, **Rytų JAV 2**, **Vakarų JAV** arba **Vakarų JAV 2**.
1. Lauke **Versija** sąraše pasirinkite **Nurodykite versiją**, tada pasirodžiusiame lauke nurodykite **9.16.19262.5**. Būtinai nurodykite būtent tą versiją, kuri nurodyta čia. Priešingu atveju vėliau teks atnaujinti RCSU į tinkamą versiją.
1. Įjunkite parinktį **Taikyti plėtinį**.
1. Plėtinių sąraše pasirinkite **„Commerce“ peržiūros demonstracinis pagrindinis plėtinys**.
1. Pasirinkite **Inicijuoti**.
1. Diegimo patvirtinimo puslapyje patikrinkite, ar išsami informacija yra tiksli, ir pasirinkite **Taip**. Grįšite į rodinį **„Retail“ valdymas**, kuriame pasirinktas skirtukas **„Retail“**. Jūsų RCSU jau buvo rengimo eilėje.
1. Prieš tęsdami įsitikinkite, kad jūsų RCSU būsena yra **Pavyko**. Inicijavimas trunka maždaug dvi–penkias valandas.

### <a name="initialize-e-commerce"></a>El. prekybos inicijavimas

Norėdami inicijuoti „e-Commerce“, atlikite toliau nurodytus veiksmus.

1. Skirtuke **„e-Commerce“ (Peržiūra)** peržiūrėkite sutikimą dėl peržiūros, tada pasirinkite **Sąranka**.
1. Lauke **„e-Commerce“ nuomotojo pavadinimas** įveskite pavadinimą. Tačiau įsidėmėkite, kad šis pavadinimas bus rodomas kai kuriuose URL, nukreiptuose į jūsų „e-Commerce“ egzempliorių.
1. Lauke **„Retail Cloud Scale Unit“ pavadinimas** sąraše pasirinkite savo RCSU. (Sąraše turėtų būti tik viena parinktis.)

    Laukas **„e-Commerce“ geografija** nustatomas automatiškai ir vertės keisti negalima.

1. Pasirinkite **Pirmyn**, kad tęstumėte.
1. Lauke **Palaikomi pagrindinių kompiuterių vardai** įveskite bet kurį tinkamą domeną, pvz., `www.fabrikam.com`.
1.  Lauke **AAD saugos grupė sistemos administratoriui** įveskite keletą pirmų norimos naudoti saugos grupės pavadinimo raidžių. Pasirinkite padidinamojo stiklo piktogramą, kad būtų rodomi ieškos rezultatai. Pasirinkite saugos grupę sąraše.
2.  Lauke **AAD saugos grupė įvertinimų ir apžvalgų moderatoriui** įveskite keletą pirmų norimos naudoti saugos grupės pavadinimo raidžių. Pasirinkite padidinamojo stiklo piktogramą, kad būtų rodomi ieškos rezultatai. Pasirinkite saugos grupę sąraše.
1. Parinktį **Įjungti įvertinimų ir apžvalgų paslauga** palikite įjungtą.
1. Jei jau atlikote „Microsoft Azure Active Directory“ („Azure AD“) sutikimo veiksmą, aprašytą skyriuje „Prieigos prie „e-Commerce“ programų suteikimas“, pažymėkite žymės langelį, kad patvirtintumėte savo sutikimą. Jei šio veiksmo dar neatlikote, turite tai padaryti prieš tęsdami inicijavimą. Norėdami atidaryti sutikimo dialogo langą ir atlikti veiksmą, pažymėkite šalia žymės langelio esančiame tekste esantį saitą.
1. Pasirinkite **Inicijuoti**. Grįžtate į rodinį **„Retail“ valdymas**, kuriame pasirinktas skirtukas **„e-Commerce“ (Peržiūra)**. „E-Commerce“ inicijavimas pradėtas.
1. Prieš tęsdami, palaukite, kol „e-Commerce“ inicijavimo būsena bus **Inicijuota sėkmingai**.
1. Dalyje **Saitai** apatiniame dešiniajame kampe pasižymėkite toliau pateikiamų saitų URL.

    * **„e-Commerce“ svetainė** – saitas į jūsų „e-Commerce“ svetainės šaknį.
    * **„e-Commerce“ svetainės valdymo įrankis** – saitas į svetainės valdymo įrankį.

## <a name="commerce-preview-environment-support"></a>„Commerce“ peržiūros aplinkos palaikymas

Jei atlikdami parengimo veiksmus patiriate problemų, apsilankykite [„Microsoft Dynamics 365 Commerce“ peržiūros versijos „Yammer“ grupėje](https://aka.ms/Dynamics365CommercePreviewYammer) dėl pagalbos.

Jei, bandant pasiekti „Yammer“ grupę, kyla problemų, su „Microsoft“ galite susisiekti el. pašto adresu <Dynamics365Commerce@microsoft.com>. Šis el. pašto adresas nėra aktyviai stebimas. Todėl atsakyti galime ne iš karto.

## <a name="next-steps"></a>Kiti veiksmai

Norėdami tęsti „Commerce“ peržiūros aplinkos parengimo ir konfigūravimo procesą, žr. skyrių [„Commerce“ peržiūros aplinkos konfigūravimas](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Papildomi ištekliai

[„Commerce” peržiūros aplinkos apžvalga](cpe-overview.md)

[„Commerce” peržiūros aplinkos konfigūravimas](cpe-post-provisioning.md)

[Pasirenkamų „Commerce” peržiūros aplinkos funkcijų konfigūravimas](cpe-optional-features.md)

[DUK apie „Commerce” peržiūros aplinką](cpe-faq.md)

[„Microsoft Lifecycle Services“ (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[„Retail Cloud Scale Unit“ (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[„Microsoft Azure“ portalas](https://azure.microsoft.com/features/azure-portal)

[„Dynamics 365 Commerce“ svetainė](https://aka.ms/Dynamics365CommerceWebsite)

[„Dynamics 365 Retail“ žinyno ištekliai](../retail/index.md)
