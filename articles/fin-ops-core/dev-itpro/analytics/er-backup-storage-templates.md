---
title: ER šablonų atsarginių kopijų saugykla
description: Šioje temoje paaiškinta, kaip naudoti elektroninių ataskaitų (ER) atsarginių kopijų saugyklą šablonų atkūrimui.
author: NickSelin
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 932ba44b4223bf9c9d93ffb19e17f6e57bb303b5
ms.sourcegitcommit: bbb64b3475eef155b3f9d1bdc440545da8a7182f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553096"
---
# <a name="backup-storage-of-er-templates"></a>ER šablonų atsarginių kopijų saugykla

[!include [banner](../includes/banner.md)]

[Elektroninių ataskaitų (ER) sistema](general-electronic-reporting.md) leidžia verslo vartotojams konfigūruoti siunčiamų dokumentų formatus pagal įvairių šalių bei regionų teisinius reikalavimus. Sukonfigūruotiems ER formatams galima naudoti iš anksto apibrėžtus šablonus, kurie leidžia generuoti įvairių formatų siunčiamus dokumentus, pvz., „Microsoft Excel“ darbaknyges, „Microsoft Word“ dokumentus arba PDF dokumentus. Šablonai yra užpildomi duomenimis, kurių generuojamiems dokumentams reikalauja sukonfigūruotas duomenų srautas.

Kiekvienas sukonfigūruotas formatas gali būti publikuojamas kaip ER sprendimo dalis. Kiekvienas ER sprendimas gali būti eksportuojamas iš vieno „Finance and Operations“ egzemplioriaus ir importuojamas į kitą egzempliorių.

ER sistema naudoja [dokumentų valdymo sistemą](../../fin-ops/organization-administration/configure-document-management.md) saugoti esamam „Finance and Operations“ egzemplioriui reikalingus šablonus. Atsižvelgiant į ER sistemos nustatymus, kaip fizinę pirminę šablonų saugyklos vietą galima pasirinkti „Microsoft Azure“ didelių dvejetainių objektų saugyklą arba „Microsoft SharePoint“ aplanką. (Norėdami gauti daugiau informacijos, žr. [žr. ER sistemos konfigūravimas](electronic-reporting-er-configure-parameters.md).) DocuValue lentelėje kiekvienam šablonui saugomas atskiras įrašas. Kiekviename įraše esančiame lauke **AccessInformation** saugomas šablono failo, esančio sukonfigūruotoje saugyklos vietoje, kelias.

Valdydami savo „Finance and Operations“ egzempliorius, galbūt nuspręsite perkelti dabartinį egzempliorių į kitą vietą. Pavyzdžiui, galite perkelti gamybos egzempliorių į naują smėlio dėžės aplinką. Jei sukonfigūruosite, kad ER sistema saugotų šablonus didelių dvejetainių objektų saugykloje, DocuValue lentelėje, esančioje naujojoje smėlio dėžės aplinkoje, bus nuoroda į didelių dvejetainių objektų saugyklos egzempliorių gamybos aplinkoje. Tačiau šio egzemplioriaus negalima pasiekti iš smėlio dėžės aplinkos, nes perkėlimo procesas nepalaiko artefaktų perkėlimo didelių dvejetainių objektų saugykloje. Todėl, pasirinkus ER formatą, kuris naudoja šabloną generuoti verslo dokumentams, įvyksta išimtis ir informuojama apie trūkstamą šabloną. Taip pat rekomenduojama naudoti ER valymo įrankį, kad panaikintumėte, o tada iš naujo importuotumėte ER konfigūraciją, kurioje yra šablonas. Kadangi gali būti kelios ER formato konfigūracijos, šis procesas gali užtrukti.

ER šablonų atsarginių kopijų saugyklos funkcija gali padėti kurti šablonus, kad juos visada galėtumėte panaudoti verslo dokumentams generuoti.

> [!NOTE]
> Šią funkciją galima naudoti tik tada, kai kaip fizinė ER šablonų saugyklos vieta yra pasirinkta didelių dvejetainių objektų saugykla.

Naudojant šią funkciją, kiekvienas naujos ER formato konfigūracijos šablonas dabartinėje aplinkoje automatiškai įrašomas į šablonams skirtą atsarginių kopijų saugojimo vietą (duomenų bazės lentelė ERDocuDatabaseStorage), kai įvyksta šie įvykiai:

- Importuojate naują ER formato konfigūraciją, kurioje yra šablonas.
- Užbaigiate ER formato konfigūracijos, kurioje yra šablonas, juodraštinę versiją.

Šablonų atsarginės kopijos perkeliamos į naują „Finance and Operations“ egzempliorių kaip programos duomenų bazės dalis.

Jei ER formato šablono, pavyzdžiui, norint apdoroti tiekėjo mokėjimus, reikia siunčiamų dokumentų generavimui, įskaitant mokėjimo pažymos ir kontrolės ataskaitų generavimą, tačiau reikiamo šablono nepavyksta rasti pirminėje saugojimo vietoje, įvyksta šie įvykiai:

- Jei šablonas yra atsarginių kopijų saugojimo vietoje, jis automatiškai iš atsarginių kopijų saugojimo vietos atkuriamas pirminėje saugojimo vietoje ir yra naudojamas vykdymui.
- Kiekvienam vartotojui, kuriam priskirtas vaidmuo **Elektroninių ataskaitų kūrėjas** arba **Sistemos administratorius**, veiksmų centre pranešama apie problemą dėl trūkstamo šablono. Rodomas pranešimas priklauso nuo parametro **Automatiškai kaip paketą vykdyti sugadintų šablonų atkūrimo procedūrą**:

    - Jei nustatyta šio parametro reikšmė **išjungta**, pranešime rekomenduojama pradėti paketinį procesą, kad būt automatiškai išspręstos panašios problemos, susijusios su kitais ER formato konfigūracijos šablonais. Pranešime yra nuoroda, kurią galite naudoti, kad pradėtumėte paketinį procesą.
    - Jei šio parametro reikšmė yra **Įjungta**, pranešime informuojama apie problemą dėl trūkstamų šablonų ir kad buvo automatiškai suplanuotas naujas paketinis procesas **Atkurti sugadintus šablonus iš vidinės duomenų bazės atsarginės kopijos**. Šis paketinis procesas automatiškai ištaisys panašias problemas su kitas šablonais.

Norėdami nustatyti parametrą **Automatiškai kaip paketą vykdyti sugadintų šablonų atkūrimo procedūrą**, atlikite šiuos veiksmus:

1. „Finance and Operations“ atidarykite **Organizacijos administravimas \> Elektroninės ataskaitos \> Konfigūracijų puslapis**.
2. Puslapio **Konfigūracijos** veiksmų srities skirtuke **Konfigūracijos**, grupėje **Papildomi parametrai** pasirinkite **Vartotojo parametrai**.
3. Dialogo lange **Vartotojo parametrai** nustatykite reikiamą parametro **Automatiškai kaip paketą vykdyti sugadintų šablonų atkūrimo procedūrą** reikšmę.

> [!NOTE]
> Šis parametras nurodomas kaip būdingas konkrečiam programos vartotojui ir prisijungusiai įmonei.

![ER konfigūracijų puslapis](./media/GER-BackupTemplates-1.png)

Toliau esančiame paveikslėlyje pateiktas pranešimo, kuris rodomas, kai nustatyta parametro **Automatiškai kaip paketą vykdyti sugadintų šablonų atkūrimo procedūrą** reikšmė yra **Įjungta**, pavyzdys.

![Tiekėjo mokėjimų žurnalo puslapis](./media/GER-BackupTemplates-2.png)

Toliau esančiame paveikslėlyje parodytas paketinis procesas **Atkurti sugadintus šablonus iš vidinės duomenų bazės atsarginės kopijos** puslapyje **Paketinė užduotis**.

![Paketinės užduoties puslapis](./media/GER-BackupTemplates-3.png)

Įvykdytų **Atkurti sugadintus šablonus iš vidinės duomenų bazės atsarginės kopijos** paketinių procesų vykdymo žurnalas apima informaciją apie šablonus, kurie buvo atkurti iš atsarginės kopijos saugojimo vietos į pirminę saugojimo vietą.

![Paketinės užduoties retrospektyvos puslapis](./media/GER-BackupTemplates-4.png)

Esant numatytiesiems nustatymams, automatinio šablonų, naudojamų ER formato konfigūracijose, atsarginių kopijų kūrimo procesas yra įjungtas. Norėdami, kad šablonų atsarginės kopijos nebūtų daromos, nustatykite parinkties **Nebekurti šablono atsarginių kopijų** reikšmę **Taip**; ši parinktis pasiekiama kortelėje **Priedai**, esančioje puslapyje **Elektroninių ataskaitų parametrai**. Šį puslapį galite atidaryti iš darbo srities **Elektroninės ataskaitos**.

Norėdami nustatyti parinkties **Nebekurti šablonų atsarginių kopijų** reikšmę **Taip** ir nebesaugoti anksčiau sukurtų šablonų atsarginių kopijų, pasirinkite **Valyti atsarginių kopijų saugyklą** puslapyje **Elektroninių ataskaitų parametrai**.

Jei savo aplinką atnaujinote į „Finance and Operations“ 10.0.5 (2019 m. spalio) versiją ir norite pereiti prie naujos aplinkos, kuri apima vykdytinas ER formato konfigūracijas, prieš vykdydami perkėlimą, pasirinkite **Užpildyti atsarginių kopijų saugyklą** puslapyje **Elektroninių ataskaitų parametrai**. Šiuo mygtuku pradedamas visų galimų šablonų atsarginių kopijų kūrimo procesas, kad jie galėtų būti išsaugoti šablonų ER atsarginių kopijų saugojimo vietoje.

![Elektroninių ataskaitų parametrų puslapis](./media/GER-BackupTemplates-5.png)

## <a name="supported-deployments"></a>Palaikomi diegimai

„Finance and Operations“ 10.0.5 versijoje ER šablonų atsarginių kopijų saugojimo funkcija yra prieinama tik debesyje veikiančioms sistemoms.

## <a name="additional-resources"></a>Papildomi ištekliai

[Elektroninių ataskaitų apžvalga](general-electronic-reporting.md)

[Elektroninių ataskaitų sistemos konfigūravimas](electronic-reporting-er-configure-parameters.md)
