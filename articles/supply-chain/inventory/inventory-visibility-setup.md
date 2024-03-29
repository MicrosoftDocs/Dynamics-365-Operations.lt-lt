---
title: Įdiekite Inventoriaus matomumo papildinį
description: Šiame straipsnyje aprašoma, kaip įdiegti "Microsoft" atsargų matomumo priedą Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c08568b14d7f5c79a1d3609107a88f905498ce2b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762787"
---
# <a name="install-and-set-up-inventory-visibility"></a>„Inventory Visibility“ diegimas ir nustatymas

[!include [banner](../includes/banner.md)]

Šiame straipsnyje aprašoma, kaip įdiegti "Microsoft" atsargų matomumo priedą Dynamics 365 Supply Chain Management.

Kad įdiegtumėte [Microsoft Dynamics atsargų matomumo priedą](https://lcs.dynamics.com/v2), turite naudoti ciklo tarnybas. Vykdymo ciklo tarnybos yra bendradarbiavimo portalas, kuriame teikiama aplinka ir reguliariai atnaujintų tarnybų rinkinys, padėsiančių valdyti programų finansų ir operacijų programėlių vykdymo ciklą. Dėl daugiau informacijos, žr. [„Lifecycle Services“ ištekliai](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> Rekomenduojame prisijungti prie vartotojų grupės Atsargų matomumas, kurioje galima rasti naudingų instrukcijų, gauti naujausius naujinimus ir registruoti bet kokius klausimus, kurie gali kilti dėl atsargų matomumo naudojimo. Norėdami prisijungti, siųskite el. laišką atsargų matomumo [produkto komandai inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) tiekimo grandinės valdymo aplinkos ID.

## <a name="inventory-visibility-prerequisites"></a>Atsargų matomumo išankstinės sąlygos

Prieš jums įdiegiant inventoriaus matomumo papildinį, atlikite šiuos veiksmus:

- Įgę vykdymo ciklo tarnybų diegimo projektą, kuriame įdiegta bent viena aplinka.
- Įsitikinkite, kad baigtos būtinosios priedų nustatymo sąlygos, pateikiamos skyriuje Priedų apžvalga buvo patenkintos. Informacijos apie šias būtinąsias sąlygas rasite [Priedų apžvalga](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Atsargų matomumui nereikia dvigubo rašymo susiejimo.

> [!NOTE]
> Šiuo metu palaikomos šalys ir regionai yra Kanada (HOU, ECA), Jungtinės Valstijos (ISPANIJOS, ESS), Europos Sąjunga (NEU, WEU), Jungtinė Karalystė (SUK,VZK) ir Australija (HOU, SEAU), Japonija (EJP, WJP) ir Brazilija (SBR, SCUS).

Jei turite kokių klausimų apie šias būtinąsias sąlygas, susisiekite su papildinio produkto komanda [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Įdiekite Inventoriaus matomumo papildinį

Prieš įdiegsdami priedą, užregistruokite programą ir pridėkite kliento slaptažodį Azure Active Directory (Azure AD) pagal savo „Azure" abonementą. Instrukcijų ieškokite Registruoti [programą ir Pridėti kliento](/azure/active-directory/develop/quickstart-register-app) ir [Įtraukti kliento raktą](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Būtinai užsirašykite programos **(kliento) ID**, **·** **kliento slapto ir nuomininko ID** reikšmių pastabą, nes vėliau jų prireiks.

> [!IMPORTANT]
> Jei turite daugiau nei vieną ciklo tarnybų aplinką, kiekvienai iš jų sukurkite Azure AD kitą programą. Jei norėdami įdiegti atsargų matomumo priedą skirtingoms aplinkai naudojate tą patį programos ID ir nuomininko ID, atpažinimo ženklo išdavimas bus taikomas senesnėms aplinkai. Todėl galioja tik paskutinė įdiegtis.

Kai užregistruojate programą ir pridedate kliento slaptą seką, atlikite šiuos veiksmus, kad įdiegtumėte atsargų „Azure AD“ matomumo priedą.

1. Prisijunkite prie [ciklo tarnybų](https://lcs.dynamics.com/Logon/Index).
1. Pagrindiniame puslapyje pasirinkite projektą, kuriame jūsų aplinka talpinta.
1. Projekto puslapyje pasirinkite aplinką, kurioje norite įdiegti papildinį.
1. Aplinkos puslapyje slinkite žemyn, kol pamatysite skyrių **Aplinkos priedai** skyriuje **„Power Platform“ integravimas** skyriuje. Ten galite rasti aplinkos „Dataverse“ pavadinimą. „Dataverse“ patvirtinkite, kad aplinkos pavadinimas yra tas, kurį norite naudoti atsargų matomumui.

    > [!NOTE]
    > Šiuo metu palaikomos Dataverse tik aplinkos, kurios sukurtos naudojant ciklo tarnybas. Jei jūsų Dataverse aplinka buvo sukurta kokiu nors kitu būdu (pavyzdžiui, PowerApps naudojant administravimo centrą) ir jei ji susieta su jūsų tiekimo grandinės valdymo aplinka, pirmiausia, prieš diegdami atsargų matomumo priedą, turite išspręsti susiejimo problemą.
    >
    > Gali būti, kad jūsų dvigubo rašymo aplinka susieta Dataverse su egzemplioriumi, kol ciklo tarnybos nėra nustatytos Power Platform integruoti. Šis susiejimo neatitikimas gali sukelti netikėtą veikimo būdą. Rekomenduojame, kad ciklo tarnybų aplinkos informacija atitiktų tai, prie ko prijungiojote dvigubo rašymo būdu, kad tą patį ryšį galėtų naudoti verslo įvykiai, virtualiosios lentelės ir priedai. Informacijos [apie tai, kaip išspręsti susiejimo](../../fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup.md#linking-mismatch) problemą, rasite susiejimų neatitikimą. Išsprendę susiejimo problemą galite toliau diegti atsargų matomumą.

1. Skyriuje **Aplinkos papildiniai** pasirinkite **Diegti naują papildinį**.

    ![Ciklo tarnybų aplinkos puslapis](media/inventory-visibility-environment.png "Ciklo tarnybų aplinkos puslapis")

1. Rinkitės **Diegti naują papildinį** nuorodą. Pasirodo esamų atvirų papildinių sąrašas.
1. Sąraše rinkitės **Atsargų matomumas**.
1. Tada nustatykite šiuos laukus savo aplinkai:

    - **AAD programos (kliento) ID** – Įveskite „Azure AD“ programos ID, kurią sukūrėte ir anksčiau užsirašėte.
    - **ADD nuomotojo ID** – Įveskite anksčiau pasižymėtą nuomotojo ID.

    ![Įtraukite į papildinių puslapį](media/inventory-visibility-setup.png "Įtraukite į papildinių puslapį")

1. Sutikite su sąlygomis ir terminais pasirinkę **Sąlygos ir terminai** žymimą laukelį.
1. Pasirinkti **Diegti**. Papildinio būsena bus rodoma kaip **diegiama**. Tada, kai diegimas bus baigtas, paleiskite iš naujo puslapį. Būsena turi pasikeisti į **Įdiegta**.
1. Kairiajame „Dataverse“ naršymo lange **pasirinkite** Programėlių **skyrių ir patikrinkite** ar atsargų matomumas sėkmingai „Power Apps“ įdiegtas. Jei **Programos** skyrius neegzistuoja, susisiekite su atsargumo matomumo produkto komanda [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!NOTE]
> Jei sistema įspės, kad neturite teisės įdiegti atsargų matomumo ciklo tarnybose, kreipkitės į administratorių, kad pakeistumėte savo teisę.
>
> Jei iš ciklo tarnybų puslapio reikia daugiau nei valandos, jūsų vartotojo abonementui tikriausiai trūksta teisės diegti sprendimus aplinkoje Dataverse. Norėdami išspręsti problemą, atlikite šiuos veiksmus:
>
> 1. Atšaukite atsargų matomumo priedo diegimo procesą iš ciklo tarnybų puslapio.
> 1. Prisijunkite prie administravimo [Microsoft 365 centro ir](https://admin.microsoft.com) įsitikinkite, kad vartotojo abonementui, kurį Dynamics 365 Unified Operations norite naudoti norėdami įdiegti papildą, priskirta "Plano" licencija. Jei reikia, priskirkite licenciją.
> 1. Prisiregistruokite administravimo [Power Platform centre](https://admin.powerplatform.microsoft.com) naudodami reikiamą vartotojo abonementą. Tada įdiekite atsargų matomumo priedą, atlikdami šiuos veiksmus:
>     1. Pasirinkite aplinką, kurioje norite įdiegti priedą.
>     1. Pasirinkite " **Dynamics 365" programėles**.
>     1. Pasirinkite **įdiegti programą**.
>     1. Pasirinkti **atsargų matomumą**
>
> 1. Baigę diegti grįžkite į **ciklo tarnybų puslapį ir pabandykite dar kartą iš naujo įdiegti atsargų matomumo** priedą.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Nustatyti atsargų matomumą „Supply Chain Management“ dalyje

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Aplinkos matomumo integravimo paketo diegimas

Jei naudojate „Supply Chain Management” 10.0.17 ar senesnę versiją, susisiekite su atsargų matomumo samdymo palaikymo komanda el. paštu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), kad gautumėte paketo failą. Tada įdiekite paketą ciklo tarnybose.

> [!NOTE]
> Jei diegiant įvyksta versijų neatitikimo klaida, turite rankiniu būdu importuoti X++ projektą į savo programavimo aplinką. Tada sukurkite diegiamą paketą savo programavimo aplinkoje ir įdiekite jį savo gamybos aplinkoje.
>
> Kodas įtrauktas į „Supply Chain Management” 10.0.18 versiją. Jei naudojate tą ar vėlesnę versiją, įdiegti nereikia.

Įsitikinkite, kad šios priemonės yra įjungtos jūsų „Supply Chain Management” aplinkoje. (Pagal numatytuosius nustatymus jos yra įjungtos.)

| Funkcijos aprašymas | Kodo versija | Klasės kaitaliojimas |
|---|---|---|
| Atsargų dimensijų naudojimo „InventSum“ lentelėje įjungimas arba išjungimas      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Atsargų dimensijų naudojimo „InventSumDelta“ lentelėje įjungimas arba išjungimas | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Atsargų matomumo integravimo nustatymas

Įdiegę priedą paruoškite tiekimo grandinės valdymo sistemą dirbti su ja, atlikdami nurodytus veiksmus.

1. „Supply Chain Management“ atverkite **[Funkcijų valdymas](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** darbo sritį ir tada įjunkite tokias funkcijas:
    - *Atsargų matomumo integravimas* – Būtinas.
    - *Atsargų matomumo integravimas su rezervavimo korespondentinė sąskaita* – rekomenduojama, bet pasirinktinai. Reikia 10.0.22 arba naujesnės versijos. Dėl daugiau informacijos, žr. [Inventoriaus matomumo rezervavimas](inventory-visibility-reservations.md).

1. Eikite į **Atsargų valdymas \> Nustatymas \> Atsargų ir sandėlio integravimo parametrai**.
1. Atidarykite skirtuką **Bendra** ir atlikite šiuos parametrus:
    - **Atsargų matomumo galinis punktas** – įveskite aplinkos, kurioje vykdomas atsargų matomumas, URL. Daugiau informacijos žr. [Surasti paslaugų galinį tašką](inventory-visibility-configuration.md#get-service-endpoint).
    - **Didžiausias įrašų skaičius vienoje užklausoje** – nustatykite didžiausią įrašų, kuriuos reikia įtraukti į vieną užklausą, skaičių. Turite įvesti teigiamą s integerį, mažesnį arba lygų 1000. Numatytoji vertė yra 512. Primygtinai rekomenduojame išsaugoti numatytąją vertę, nebent gavote „Microsoft Support" rekomendacijų arba esate tikri, kad ją reikia pakeisti.

1. Jei įgalinote pasirinktinį *atsargų matomumo integravimą su rezervavimo korespondentinės* sąskaitos funkcija, atidarykite skirtuką **Rezervavimas ir atlikite** šiuos parametrus:
    - **Įgalinti rezervavimo korespondentinę sąskaitą** – nustatykite kaip *Taip*, norėdami įgalinti šią funkciją.
    - **Rezervavimo korespondentinis modifikatorius** – pasirinkite atsargų operacijos būseną, kuri koresponduos rezervavimus, atliktas atsargų matomumo metu. Šis parametras nustato užsakymo apdorojimo etapą, kuris suaktyvina kompensavimus. Etapą seka užsakymo atsargų operacijos būsena. Pasirinkite vieną iš šių pasirinkčių:
        - *Užsakyta* – kai operacijos būsena Yra, sukūrus užsakymą, *užsakymas* atsiųs korespondentinę užklausą. Korespondentinis kiekis bus sukurto užsakymo kiekis.
        - *Rezervas* – kai *operacijos būsena Rezervuota,* Užsakytas užsakymas siųs korespondentinę užklausą, kai ji rezervuota, paimta, užregistruotas važtaraštis arba išrašyta SF. Užklausa bus suaktyvinta tik vieną kartą, pirmojo žingsnio atveju, kai bus įvyksta nurodytas procesas. Korespondentinis kiekis bus kiekis, kai atsargų operacijos būsena atitinkamoje užsakymo eilutėje pasikeičia iš *Užsakyta* į *Rezervuota* (arba vėlesnė būsena).

1. Eikite į **Atsargų valdymas \> Periodinis \> Atsargų matomumo integravimas** ir įjunkite užduotį. Visi atsargų keitimo įvykiai iš „Supply Chain Management” dabar bus užregistruoti atsargų matomumo srityje.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Išdiekite Inventoriaus matomumo papildinį

Norėdami pašalinti atsargų matomumo priedą, atlikite šiuos veiksmus:

1. Prisijunkite prie „Supply Chain Management“.
1. Pereikite prie **atsargų valdymo periodinio \> atsargų \> matomumo integravimo ir** išjunkite užduotį.
1. Eikite į ciklo tarnybas ir atidarykite aplinkos, kurioje norite pašalinti papildinį, puslapį ([taip pat žr. parinktį Atsargų matomumo priedas](#install-add-in)).
1. Pasirinkite **Pašalinti**.
1. Pašalinimo procesas dabar nutraukia atsargų matomumo priedą, išregistruojami iš ciklo tarnybų ir panaikinami laikini duomenys, saugomi atsargų matomumo priedo duomenų talpykloje. Tačiau pirminiai atsargų duomenys, kurie buvo sinchronizuoti su jūsų abonementu Dataverse, vis dar saugomi ten. Norėdami panaikinti šį duomenis, atlikite likusią procedūrą.
1. Atidarykite [Power Apps](https://make.powerapps.com).
1. Naršymo **juostoje** pasirinkite Aplinka.
1. Pasirinkite aplinką Dataverse, kuri yra ryšį su jūsų ciklo tarnybų aplinka.
1. Eikite **į** sprendimus ir panaikinkite šiuos sprendimus šia tvarka:
    1. "Dynamics 365" atsargų matomumas – prieraišo žymę
    1. "Dynamics 365" atsargų matomumas – įprasti
    1. "Dynamics 365" atsargų matomumas – programa
    1. "Dynamics 365" atsargų matomumas – valdikliai
    1. "Dynamics 365" atsargų matomumas – pagrindinis 

    Kai panaikinate šiuos sprendimus, duomenys, saugomi lentelėse, taip pat bus panaikinti.

> [!NOTE]
> Jei atkursite tiekimo grandinės valdymo duomenų bazę, išdiegę atsargų matomumo priedą ir norėsite iš naujo įdiegti papildinį, įsitikinkite, Dataverse kad panaikinate senus savo abonemente saugomus atsargų matomumo duomenis (kaip aprašyta ankstesnėje procedūroje), prieš įdiegdami papildinį iš naujo. Taip išvengsite duomenų nenuoseklumo problemų, kurios kitu atveju galėtų įvykti.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a> Prieš atkurdami tiekimo grandinės valdymo duomenų Dataverse bazę išvalykite atsargų matomumo duomenis

Jei naudojate atsargų matomumą ir tada atkūrote tiekimo grandinės valdymo duomenų bazę, atkurtoje duomenų bazėje gali būti duomenų, kurie nebeatitinka anksčiau sinchronizuotų su atsargų matomumo duomenimis Dataverse. Dėl šių duomenų nenuoseklumo gali kilti sistemos klaidų ir kitų problemų. Todėl svarbu prieš atkurdami tiekimo grandinės Dataverse valdymo duomenų bazę visada išvalyti visus atsargų matomumo duomenis.

Jei reikia atkurti tiekimo grandinės valdymo duomenų bazę, naudokite šią procedūrą:

1. Pašalinti atsargų matomumo priedą ir pašalinti visus susijusius duomenis Dataverse, [kaip aprašyta "Šalinti atsargų matomumo priedą"](#uninstall-add-in)
1. Atkurkite savo tiekimo grandinės valdymo duomenų bazę, pvz., [kaip aprašyta duomenų bazės tam tikrą laiką atkurti (PITR)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md)[arba į tam tikrą laikotarpį atkurta gamybos duomenų bazė į sandbox aplinką](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md).
1. Jei vis tiek norite jį naudoti, [...](#install-add-in)[iš naujo įdiekite ir nustatykite atsargų matomumo priedą, kaip aprašyta priedo atsargų matomumo įdiegime ir Nustatyti atsargų matomumo integravimą](#setup-inventory-visibility-integration)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
