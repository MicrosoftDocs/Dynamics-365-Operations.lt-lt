---
title: Saugos konfigūracijos koncepcijos, skirtas virtualioms lentelėms pagrįstims integracijų koncepcijos
description: Šiame straipsnyje paaiškinama architektūra, kuriant Microsoft ir kitų Dynamics 365 Human Resources sistemų integravimą.
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759730"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>Saugos konfigūracijos koncepcijos, skirtas virtualioms lentelėms pagrįstims integracijų koncepcijos

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje aprašoma architektūra, kaip naudoti [Microsoft Dataverse virtualias lenteles (objektus)](/dev-itpro/power-platform/virtual-entities-overview) integravimui tarp Dynamics 365 Human Resources trečiosios šalies sistemos sukurti. Daugiausia dėmesio skiriama straipsnio saugos konfigūracijai ir autentifikavimo bei autorizavimo aspektams, kurie reikalingi tarp sistemos ribų, kad būtų galima sukurti funkcionalią, saugią sistemą.

## <a name="prerequisite-reference-articles"></a>Būtinųjų komponentų nuorodos straipsniai

Toliau pateikiami straipsniai pateikia daugiau informacijos apie šiame straipsnyje sąvokas:

- [Virtualių objektų apžvalga](/dev-itpro/power-platform/virtual-entities-overview)
- [Darbo su virtualiomis lentelėmis (objektais) pradžia](/developer/data-platform/virtual-entities/get-started-ve)
- [Kelių nuomininkų autentifikavimo tarp serverių naudojimas (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [Naudoti OAuth autentifikavimą su Microsoft Dataverse (Dataverse)](/developer/data-platform/authenticate-oauth)
- [OAuth 2.0 kliento kredencialų srautas "Microsoft" tapatybės platformoje](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [Autentifikavimas ir autorizavimas](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>Architektūra 

Šioje architektūros diagramoje parodytos pagrindinės koncepcijos, įtrauktos į integravimą, kuriame naudojamos virtualios lentelės (objektai).

![Virtualioji lentele pagrįstas integravimas.](./media/Hosts.jpg)

Čia pateiktas kai kurių ankstesnės diagramos elementų paaiškinimas:

- **"Microsoft" – "Microsoft** " klientų vardu dirba su skirtingais "Dynamics 365" produktais ir veikia su jies.

    - **Azure Active Directory(Azure AD) Nuomininkas C** – Azure AD nuomininkas, priklauso Microsoft. Nuomininkas, kuriame užsiregistravo "Dynamics 365" prašymai.

- **Partnerio integravimas**

    - **Integruojant** sistemą – sistemą, integruotą su Dynamics 365. Tai gali būti algalapio sistema arba bet kuri sistema, pasitiki duomenimis, saugomais "Dynamics 365".
    - **Adapteris** – programinė įranga ar tarnyba, atsakinga už bendravimą su "Dynamics 365" ir integravimo sistema.

        > [!NOTE]
        > Jei adapteriu galės naudoti keli "Dynamics 365" klientai, tikimasi, kad jis bus užregistruotas kaip kelių lygių programa Azure AD.

    - **Azure AD nuomininkas** A Azure AD – nuomininkas, kuris priklauso integravimo partneriui. Nuomininkas, kuriame užregistruotas adapterio programos ID.

- **Abipusis** klientas – klientas Dynamics 365 Human Resources, kuris įdiegia ir integruoja partnerio sprendimą.

    - **"Dynamics 365"** finansai arba žmogiškieji ištekliai – klientui skirtas "Dynamics 365 Finance" arba personalo egzempliorius, kuriame yra kliento duomenys, kurių reikia integruojanti sistema.
    - **Dataverse**– konkretaus kliento aplinka Dataverse, sujungta su finansais arba personalo ištekliais. Dataverse suteikia interneto API, kad būtų galima atlikti sąveiką su "Dynamics 365" duomenimis.
    - **Azure AD nuomininkas B** – kliento nuomininkas Azure AD. Ji veikia kaip tapatybės teikėjas (autorizavimo serveris) ir išduoda atpažinimo ženklus, kurie autorizuos iškininkų iškvietimo kliento egzempliorių Dataverse.

## <a name="basic-request-flow"></a>Pagrindinės užklausos srautas

Šiame skyriuje aprašomas pagrindinis įprastos užklausos, įtrauktos į integravimą, srautas. Anksčiau šiame straipsnyje ji nurodo architektūros diagramą.

Įprasta užklausa reikalauja, kad adapterio užklausa "Dynamics 365" duomenims būtų įrašinėjama ir sinchronizuojama su integravimo sistema.

1. Adapteris išk ragina Dataverse interneto API pateikti užklausą dėl atitinkamų duomenų.

    > [!NOTE]
    > Autentifikavimas yra būtina sąlyga, o atpažinimo ženklų įsigijimas yra pagrindinė proceso dalis. Autentifikavimas bus aprašytas autentifikavimo [ir autorizavimo sistemos ribų](#authentication-and-authorization-at-system-boundaries) skyriuje.

    Šis iškvietimas iš interneto Dataverse API pateikiamas programos duomenų, rodomų virtualioje lentelėje, užklausai. (Žr. 2. Pradinis sinchronizavimas ir 3. Pokyčių sinchronizavimas diagramoje.)

2. Dataverse tvarko užklausą, užklausdama virtualią lentelę per virtualųjį objektą objekto objekto diagramoje ("Virtualiosios lentelės tarpinis serveris"). Užklausa Dataverse perduodama į finansų arba personalo virtualiųjų objektų paslaugą, kad būtų galima užklausti apie duomenis, kurie faktiškai saugomi finansų arba personalo duomenų bazėje.
3. Finansų arba personalo virtualiojo objekto tarnyba išvers virtualiojo objekto užklausą į užklausą dėl finansų arba personalo objekto, kuris atims Dataverse virtualų objektą. Duomenys nuskaitomi iš duomenų bazės, konvertuojami atgal į objekto Dataverse atvaizdą ir grąžinami išk skambinanto asmeniui.
4. Adapteris užbaigia bet kokį reikiamą konvertavimą ir duomenų konvertavimą ir skambina į integruojamą sistemą, kad duomenys išlieka integruojamos sistemos duomenų bazėje. (Žr. 4. Įrašyti duomenis" diagramoje.)

## <a name="authentication-and-authorization-at-system-boundaries"></a>Autentifikavimas ir autorizavimas sistemos ribose

*Autentifikavimas* patvirtina, kad vartotojo arba programos tapatybė patvirtinta ir patvirtina, kad vartotojas arba programa yra tas, kas jis yra. *Autorizavimas* suteikia vartotojui arba programai teisę pasiekti konkrečias programos lygio teises. Daugiau informacijos rasite Autentifikavimas [ir autorizavimas](/azure/active-directory/develop/authentication-vs-authorization).

Dauguma kryžminės sistemos skambučių architektūros diagramoje, anksčiau šiame straipsnyje, apima adapterį. Adapteris turi autentifikuoti save, kad galėtų atlikti šiuos skambučius:

- Skambutis iki Dataverse
- Iškvietimas į integravimo sistemą

Pažiūrėkite sistemos ribas diagramoje. Kiekviena žiniatinklio užklausa tarp sistemų turi būti autentifikuota, o programos lygio autorizavimo tikrinimai turi būti perduoti prieš grąžinant duomenis skambinanto programai. Užklausai dėl "Dynamics 365" virtualios lentelės, kurią atims finansai arba žmogiškieji ištekliai, autentifikavimo ir autorizavimo tikrinimai vykdomi šiomis sistemos ribomis:

- Adapterio ir interneto API Dataverse (OData) galinio punkto iškvietimas
- Iškvietimas tarp virtualiojo Dataverse objekto objektų objektų ir finansų arba personalo virtualiųjų objektų paslaugos

Abiem atvejais pirmiausia atliekami autentifikavimo tikrinimai. Tada atliekami programos lygio autorizavimo tikrinimai, siekiant užtikrinti, kad autentifikuotas vartotojas arba programa turėtų tinkamas programos lygio teises nuskaityti prašomus duomenis.

Autentifikavimas, kurį Dataverse reikia iškviesti, tvarkomas naudojant pateikiamais atpažinimo ženklus, kuriuos į užklausą internetu reikia įtraukti kaip HTTP antraštę Dataverse. Adapteris turi gauti atpažinimo ženklą iš nuomininko B egzemplioriaus Azure AD. (Žr. "1. Gauti atpažinimo ženklą diagramoje.) Azure AD autentifikavimo sraute veikia kaip tapatybės teikėjas.

Adapteris autentifikuoja pateikia savo programos tapatybę (ne slaptą, Azure AD kaip registruotas nuomininke A) ir programos slaptą sertifikatą, kurį turi tik adapterio programa.

Po to, kai vartotojas ar programa yra autentifikuoti ir gali skambinti Dataverse, Dataverse lygio autorizavimo tikrinimai atliekami pagal kiekvieną užklausą. Šie patikrinimai užtikrina, kad skambintojas (adapterio programos tapatybė, diagramoje nurodyta "\<guid A\>") turėtų atitinkamas programos teises. Programos lygio autorizavimas valdomas Dataverse naudojant programos vartotoją, kuris nurodo adapterio programos ID. Programos lygio teisės valdomos suteikiant prieigą prie konkrečių nustatytų Dataverse programos vaidmenų. Šie vaidmenys suteikia programai išsamių teisių.

Išsamesnės informacijos ieškokite daugiau informacijos apie [kelių nuomininkų serverio autentifikavimą](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication).

Jei Dataverse leidžiami -lygio programos teisių tikrinimai, virtualaus objekto iškvietimas į virtualiųjų objektų tarnybos galinį punktą finansų arba personalo aplinkoje. Šiam iškvietimui atlikti naudojamas serverio-serverio (S2S) autentifikavimas. Jis naudoja tapatybę ir slaptą informaciją, sukonfigūruotą finansų ir operacijų virtualiųjų duomenų šaltinio konfigūracijos įraše.

![Finansų ir operacijų virtualiųjų duomenų šaltinio konfigūracijos įrašas sandūrų aplinkoje.](./media/sandbox.jpg)

Daugiau informacijos rasite Virtualiųjų objektų [Dataverse konfigūravimas](/dev-itpro/power-platform/admin-reference).

Iškvietimas iš Dataverse virtualiojo objekto į finansus arba žmogiškuosius išteklius apima adapterio pirminio Dataverse iškvietimo, per kurį reikia per adapterį, tapatybę (tapatybė, kuri nurodyta "\<guid A\>" architektūros diagramoje). Jei virtualiojo objekto duomenų šaltinis tinkamai sukonfigūruotas ir perduota S2S autentifikavimo tikrinimai, virtualiojo objekto paslauga finansuose arba personalo ištekliams paleis užklausą pradinio kiestuvo (adapterio) kontekste \<guid A\>. Programos teisių tikrinimai (autorizavimas) finansų arba žmogiškųjų išteklių lygiu bus atlikti siekiant užtikrinti, kad adapteris turėtų teises, būtinas norint pasiekti duomenų objektus, kurių užklausta naudojant užklausą.

Finansų ir personalo sauga valdoma šiais būdais:

1. Susiekite adapterio tapatybę (\<guid A\>) su konkrečiu finansų arba personalo vartotojas. Šis susiejimas atliktas " **Azure Active Directory" programų** puslapyje. Norėdami gauti daugiau informacijos, užregistruokite [savo išorinę programą](/dev-itpro/data-entities/services-home-page.md#register-your-external-application).
2. Finansų arba personalo vartotojui suteikiant atitinkamus programos lygio vaidmenis, pareigas ir teises. Daugiau informacijos rasite vaidmenimis [pagrįstą saugą](/dev-itpro/sysadmin/role-based-security).

Jei adapterio programai (\<guid A\>) suteikiamos teisės, kurių reikia norint pasiekti reikiamus duomenis, įvyksta šie įvykiai:

1. Užklausa vykdoma.
2. Duomenys verčiami atgal į jo Dataverse objekto puslapį.
3. Duomenys grįžta į adapterį.

> [!IMPORTANT]
> Kūrimo metu adapterį galima paleisti naudojant finansų arba personalo vartotoją, kuris turi administratoriaus vaidmenį. Tačiau gamybos aplinkoje adapteris niekada neturėtų būti vykdomas su administratoriaus teisėmis.

## <a name="key-takeaways"></a>Rakto takeimai

Čia pateikiama keletas svarbių virtualios lentelės ar objekto architektūros reikšmės:

- Virtualiųjų lentelių, kurių atsargines kopijas valdo Žmogiškieji ištekliai, saugos konfigūracija valdoma iš Personalo.
- Klientas ("Abipusis klientas", anksčiau šiame straipsnyje pateiktoje architektūros diagramoje) visiškai kontroliuoja, kokios teisės suteikiamos integruojant adapterio tapatybę (\<guid A\> nurodyta "" diagramoje).
- Klientas yra atsakingas už tinkamą jų personalo aplinkos saugos konfigūraciją. Integravimo partneris, kuris sukuria adapterį, turi pateikti rekomendacijas apie teises, kurių reikia adapteriui.
