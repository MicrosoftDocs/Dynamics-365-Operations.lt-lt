---
title: ER šablonų atsarginių kopijų saugykla
description: Šiame straipsnyje paaiškinama, kaip naudoti elektroninių ataskaitų (ER) atsarginę saugyklą šablonams atkurti.
author: kfend
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.custom: 27621
ms.assetid: ''
ms.search.form: ERWorkspace, ERSolutionTable
ms.openlocfilehash: 61e6119c50ee79d8623d1b49d273fb8c07f88944
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281909"
---
# <a name="backup-storage-of-er-templates"></a>ER šablonų atsarginių kopijų saugykla

[!include [banner](../includes/banner.md)]

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md) leidžia verslo vartotojams konfigūruoti siunčiamų dokumentų formatus pagal įvairių šalių bei regionų teisinius reikalavimus. Sukonfigūruotiems ER formatams galima naudoti iš anksto apibrėžtus šablonus, kurie leidžia generuoti įvairių formatų siunčiamus dokumentus, pvz., „Microsoft Excel“ darbaknyges, „Microsoft Word“ dokumentus arba PDF dokumentus. Šablonai yra užpildomi duomenimis, kurių generuojamiems dokumentams reikalauja sukonfigūruotas duomenų srautas.

Kiekvienas sukonfigūruotas formatas gali būti publikuojamas kaip ER sprendimo dalis. Kiekvieną ER sprendimą galima eksportuoti iš vieno finansų ir operacijų egzemplioriaus ir importuoti į kitą egzempliorių.

ER sistema naudoja dokumentų valdymo [konfigūravimą, kad išsamūs](../../fin-ops/organization-administration/configure-document-management.md) dabartinių finansų ir operacijų egzemplioriaus šablonai būtų išsaugoti. Atsižvelgiant į ER sistemos nustatymus, kaip fizinę pirminę šablonų saugyklos vietą galima pasirinkti „Microsoft Azure“ didelių dvejetainių objektų saugyklą arba „Microsoft SharePoint“ aplanką. (Norėdami gauti daugiau informacijos, žr. [Elektroninių ataskaitų (ER) sistemos konfigūravimas](electronic-reporting-er-configure-parameters.md).) „DocuValue“ lentelėje kiekvienam šablonui saugomas atskiras įrašas. Kiekviename įraše esančiame lauke **AccessInformation** saugomas šablono failo, esančio sukonfigūruotoje saugyklos vietoje, kelias.

Tvarkydami savo finansų ir operacijų egzempliorius galite nuspręsti perkelti dabartinį egzempliorių į kitą vietą. Pavyzdžiui, galite perkelti gamybos egzempliorių į naują smėlio dėžės aplinką. Jei sukonfigūruosite, kad ER sistema saugotų šablonus didelių dvejetainių objektų saugykloje, DocuValue lentelėje, esančioje naujojoje smėlio dėžės aplinkoje, bus nuoroda į didelių dvejetainių objektų saugyklos egzempliorių gamybos aplinkoje. Tačiau šio egzemplioriaus negalima pasiekti iš smėlio dėžės aplinkos, nes perkėlimo procesas nepalaiko artefaktų perkėlimo didelių dvejetainių objektų saugykloje. Todėl, pasirinkus ER formatą, kuris naudoja šabloną generuoti verslo dokumentams, įvyksta išimtis ir informuojama apie trūkstamą šabloną. Taip pat rekomenduojama naudoti ER valymo įrankį, kad panaikintumėte, o tada iš naujo importuotumėte ER konfigūraciją, kurioje yra šablonas. Kadangi gali būti kelios ER formato konfigūracijos, šis procesas gali užtrukti.

ER šablonų atsarginių kopijų saugyklos funkcija gali padėti kurti šablonus, kad juos visada galėtumėte panaudoti verslo dokumentams generuoti.

> [!NOTE]
> Šią funkciją galima naudoti tik tada, kai kaip fizinė ER šablonų saugyklos vieta yra pasirinkta didelių dvejetainių objektų saugykla.

## <a name="automated-recovery-and-notification"></a>Automatizuotas atkūrimas ir pranešimas

Naudojant šią funkciją, kiekvienas naujos ER formato konfigūracijos šablonas dabartinėje aplinkoje automatiškai įrašomas į šablonams skirtą atsarginių kopijų saugojimo vietą (duomenų bazės lentelė ERDocuDatabaseStorage), kai įvyksta šie įvykiai:

- Importuojate naują ER formato konfigūraciją, kurioje yra šablonas.
- Užbaigiate ER formato konfigūracijos, kurioje yra šablonas, juodraštinę versiją.

Atsarginės šablonų kopijos perkeliamos į naują finansų ir operacijų egzempliorių kaip programos duomenų bazės dalis.

Jei ER formato šablono, pavyzdžiui, norint apdoroti tiekėjo mokėjimus, reikia siunčiamų dokumentų generavimui, įskaitant mokėjimo pažymos ir kontrolės ataskaitų generavimą, tačiau reikiamo šablono nepavyksta rasti pirminėje saugojimo vietoje, įvyksta šie įvykiai:

- Jei šablonas yra atsarginių kopijų saugojimo vietoje, jis automatiškai iš atsarginių kopijų saugojimo vietos atkuriamas pirminėje saugojimo vietoje ir yra naudojamas vykdymui.
- Kiekvienam vartotojui, kuriam priskirtas vaidmuo **Elektroninių ataskaitų kūrėjas** arba **Sistemos administratorius**, veiksmų centre pranešama apie problemą dėl trūkstamo šablono. Rodomas pranešimas priklauso nuo parametro **Automatiškai kaip paketą vykdyti sugadintų šablonų atkūrimo procedūrą**:

    - Jei nustatyta šio parametro reikšmė **išjungta**, pranešime rekomenduojama pradėti paketinį procesą, kad būt automatiškai išspręstos panašios problemos, susijusios su kitais ER formato konfigūracijos šablonais. Pranešime yra nuoroda, kurią galite naudoti, kad pradėtumėte paketinį procesą.
    - Jei šio parametro reikšmė yra **Įjungta**, pranešime informuojama apie problemą dėl trūkstamų šablonų ir kad buvo automatiškai suplanuotas naujas paketinis procesas **Atkurti sugadintus šablonus iš vidinės duomenų bazės atsarginės kopijos**. Šis paketinis procesas automatiškai ištaisys panašias problemas su kitas šablonais.

Norėdami nustatyti parametrą **Automatiškai kaip paketą vykdyti sugadintų šablonų atkūrimo procedūrą**, atlikite šiuos veiksmus:

1. Finansinėse ir operacijose atidarykite puslapį **Organizacijos administravimas \> Elektroninės \> ataskaitos konfigūracijos**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Dialogo lange **Vartotojo parametrai** nustatykite reikiamą parametro **Automatiškai kaip paketą vykdyti sugadintų šablonų atkūrimo procedūrą** reikšmę.

> [!NOTE]
> Šis parametras nurodomas kaip būdingas konkrečiam programos vartotojui ir prisijungusiai įmonei.

![ER konfigūracijų puslapis.](./media/GER-BackupTemplates-1.png)

Toliau esančiame paveikslėlyje pateiktas pranešimo, kuris rodomas, kai nustatyta parametro **Automatiškai kaip paketą vykdyti sugadintų šablonų atkūrimo procedūrą** reikšmė yra **Įjungta**, pavyzdys.

![Tiekėjo mokėjimų žurnalo puslapis.](./media/GER-BackupTemplates-2.png)

Toliau esančiame paveikslėlyje parodytas paketinis procesas **Atkurti sugadintus šablonus iš vidinės duomenų bazės atsarginės kopijos** puslapyje **Paketinė užduotis**.

![Paketinės užduoties puslapis.](./media/GER-BackupTemplates-3.png)

Įvykdytų **Atkurti sugadintus šablonus iš vidinės duomenų bazės atsarginės kopijos** paketinių procesų vykdymo žurnalas apima informaciją apie šablonus, kurie buvo atkurti iš atsarginės kopijos saugojimo vietos į pirminę saugojimo vietą.

![Paketinės užduoties retrospektyvos puslapis.](./media/GER-BackupTemplates-4.png)

Esant numatytiesiems nustatymams, automatinio šablonų, naudojamų ER formato konfigūracijose, atsarginių kopijų kūrimo procesas yra įjungtas. Norėdami, kad šablonų atsarginės kopijos nebūtų daromos, nustatykite parinkties **Nebekurti šablono atsarginių kopijų** reikšmę **Taip**; ši parinktis pasiekiama kortelėje **Priedai**, esančioje puslapyje **Elektroninių ataskaitų parametrai**. Šį puslapį galite atidaryti iš darbo srities **Elektroninės ataskaitos**.

Norėdami nustatyti parinkties **Nebekurti šablonų atsarginių kopijų** reikšmę **Taip** ir nebesaugoti anksčiau sukurtų šablonų atsarginių kopijų, pasirinkite **Valyti atsarginių kopijų saugyklą** puslapyje **Elektroninių ataskaitų parametrai**.

Jei atnaujinote savo aplinką į finansų ir operacijų versiją 10.0.5 (2019 m. spalio mėn.) ir norite perkelti į naują aplinką, kurioje yra ER formato konfigūracijos, kurias galima vykdyti, **·** **prieš** vykdant perkėlimą pasirinkite Užpildyti atsarginį saugojimą elektroninių ataskaitų parametrų puslapyje. Šiuo mygtuku pradedamas visų galimų šablonų atsarginių kopijų kūrimo procesas, kad jie galėtų būti išsaugoti šablonų ER atsarginių kopijų saugojimo vietoje.

![Elektroninių ataskaitų parametrų puslapis.](./media/GER-BackupTemplates-5.png)

## <a name="manual-recovery"></a>Rankinis atkūrimas

Eikite į **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Atkurti sugadintus šablonus**, norėdami neautomatiniu būdu inicijuoti ER šablonų atkūrimo iš atsarginės saugyklos vietos į pirminę saugyklos vietą procesą. Prieš pradėdami šį procesą, puslapyje **Atkurti sugadintus šablonus** galite nurodyti, ar procesas bus vykdomas interaktyviai, ar bus planuojamas paketinis vykdymas.

## <a name="supported-deployments"></a>Palaikomi diegimai

10.0.5 versijoje ER šablonų funkcijos atsarginis saugojimas galimas tik diegiant debesį.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų (ER) sistemos konfigūravimas](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
