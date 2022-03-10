---
title: Bendroji trikčių šalinimo informacija
description: Šioje temoje pateikiama bendroji trikčių šalinimo informacija apie dvigubo rašymo integravimą tarp „Finance and Operations“ programų ir Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6f5b9f26990e2f4db9bf69040a6c4be31400b40
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062343"
---
# <a name="general-troubleshooting"></a>Bendroji trikčių šalinimo informacija

[!include [banner](../../includes/banner.md)]



Šioje temoje pateikiama bendroji trikčių šalinimo informacija apie dvigubo rašymo integravimą tarp „Finance and Operations“ programų ir Dataverse.

> [!IMPORTANT]
> Kai kurioms šioje temoje nagrinėjamoms problemoms spręsti gali reikėti sistemos administratoriaus vaidmens arba „Microsoft Azure Active Directory” („Azure AD”) nuomotojo administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Įgalinkite ir peržiūrėkite priedo sekimo žurnalą „Dataverse”, kad peržiūrėtumėte klaidos informaciją

**Reikiamas vaidmuo, norint įjungti sekimo žurnalą ir peržiūrėti klaidas:** sistemos administratorius

Norėdami įjungti sekimo žurnalą, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Customer Engagement” programos, atidarykite puslapį **Parametrai**, o tada dalyje **Sistema** pasirinkite **Administravimas**.
2. Puslapyje **Administravimas** pasirinkite **Sistemos parametrai**.
3. Skirtuko **Tinkinimas** stulpelyje **Priedo ir pasirinktinės darbo eigos veiklos sekimas** pasirinkite **Viskas**, kad įgalintumėte priedo sekimo žurnalą. Jei norite registruoti sekimo žurnalus tik tada, kai įvyksta išimtys, vietoje to galite pasirinkti **Išimtis**.


Norėdami peržiūrėti sekimo žurnalą, atlikite toliau nurodytus veiksmus.

1. Prisijunkite prie „Customer Engagement” programos, atidarykite puslapį **Parametrai**, o tada dalyje **Tinkinimas** pasirinkite **Priedo sekimo žurnalas**.
2. Raskite sekimo žurnalus, kuriuose stulpelis **Tipo pavadinimas** nustatytas kaip **„Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin”**.
3. Dukart spustelėkite elementą, kad peržiūrėtumėte visą žurnalą, tada „FastTab” **Vykdymas** peržiūrėkite tekstą **Pranešimų blokas**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Įgalinkite derinimo režimą, kad pašalintumėte tiesioginio sinchronizavimo problemas „Finance and Operations“ programose

**Reikiamas vaidmuo, norint peržiūrėti klaidas:** sistemos administratorius

Dvigubo rašymo klaidos, kylančios iš Dataverse gali būti rodomas programėlėje „Finance and Operations“. Norėdami įjungti daugiažodį klaidų registravimą atlikite toliau nurodytus veiksmus.

1. Visoms projektų konfigūracijoms programoje „Finance and Operations“ yra vėliavėlė **IsDebugMode** ant **DualWriteProjectConfiguration** stalo.
2. Atidarykite **„DualWriteProjectConfiguration”** naudodami „Excel“ papildinį. Norėdami naudoti priedą, įgalinkite projektavimo režimą „Finance and Operations Excel“ priede ir pridėkite **DualWriteProjectConfiguration** prie lapo. Daugiau informacijos žr. skyriuje [Objekto duomenų peržiūra ir atnaujinimas programoje „Excel“](../../office-integration/use-excel-add-in.md).
3. Projekte nustatykite **IsDebugMode** kaip **Taip**.
4. Vykdyti scenarijų, kuris generuoja klaidas.
5. Daugiažodžiai žurnalai saugomi lentelėje **DualWriteErrorLog**.
6. Norėdami peržvelgti duomenis lentelių naršyklėje, naudokite šį saitą: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, jei reikia, pakeiskite `999`.
7. Atnaujinkite dar kartą pagal [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), pasiekiamą platformos naujiniui Nr. 37 ir naujesniems. Jei įdiegėte šią pataisą, derinimo režimu bus fiksuojama daugiau žurnalų.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Patikrinkite „Finance and Operations“ programos sinchronizavimo klaidas virtualioje mašinoje

**Reikiamas vaidmuo, norint peržiūrėti klaidas:** sistemos administratorius

1. Prisijunkite prie „Microsoft Dynamics“ portale „Lifecycle Services“ (LCS).
2. Atidarykite LCS projektą, kurį pasirinkote dvigubo rašymo testavimui atlikti.
3. Pasirinkite plytelę **Aplinkos diegimo debesyje įrankis**.
4. Naudokite nuotolinį darbalaukį, kad prisijungtumėte prie virtualios mašinos (VM), skirtos programai „Finance and Operations“. Naudokite vietinę paskyrą, kurį yra rodoma LCS.
5. Atidarykite įvykių peržiūros programą.
6. Pasirinkite **Programų ir paslaugų žurnalai \> „Microsoft“ \> „Dynamics“ \> „AX-DualWriteSync“ \> Veikia**.
7. Peržiūrėti naujausių klaidų sąrašą.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Atsieti ir susieti kitą Dataverse aplinką iš „Finance and Operations“ programos

**Būtinas vaidmuo norint atsieti aplinką:** Programos „Finance and Operations“ sistemos administratorius arba Dataverse.

1. Prisijunkite prie programėlės „Finance and Operations“.
2. Eikite į **Darbo sritys \> Duomenų valdymas** ir pasirinkite plytelę **Dvigubas rašymas**.
3. Pasirinkite visus veikiančius susiejimus, tada pasirinkite **Stabdyti**.
4. Pasirinkite **Atsieti aplinką**.
5. Kad patvirtintumėte operaciją, pasirinkite **Taip**.

Dabar galite susieti naują aplinką.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Nepavyko peržiūrėti pardavimo užsakymo eilutės informacijos formos 

Sukurę pardavimo užsakymą „Dynamics 365 Sales”, paspaudę **+ Įtraukti produktus** galite būti nukreipti į „Dynamics 365 Project Operations” užsakymo eilutės formą. Nėra būdo toje formoje peržiūrėti pardavimo užsakymo eilutės formą **Informacija**. Parinktis **Informacija** neatsiranda toliau esančiame išplečiamajame lauke **Nauja užsakymo eilutė**. Taip nutinka, nes jūsų aplinkoje įdiegta „Project Operations”.

Norėdami iš naujo įgalinti formos parinktį **Informacija**, atlikite toliau pateiktus veiksmus.

1. Pereikite į **Užsakymo eilutė** lentelę.
2. Formų mazge raskite formą **Informacija**.
3. Pasirinkite formą **Informacija** ir spustelėkite **Įgalinti saugos vaidmenis**.
4. Pakeiskite saugos parametro parinktį į **Rodyti visiems**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Kaip įjungti ir įrašyti tinklo sekimą, kad sekimus būtų galima pridėti prie palaikymo kvitų

Palaikymo komandai gali reikėti peržiūrėti tinklo sekimus, siekiant diagnozuoti ir pašalinti kai kurias triktis. Norėdami sukurti tinklo sekimą, atlikite toliau nurodytus veiksmus.

### <a name="chrome"></a>Chrome

1. Atidarytame skirtuke paspauskite **F12** arba pasirinkite **Programavimo įrankiai**, kad atidarytumėte programavimo įrankius.
2. Atverkite skirtuką **Tinklas** ir filtro teksto lauke įveskite **integ**.
3. Vykdykite savo scenarijų ir atsižvelkite į registruojamas užklausas.
4. Dešiniuoju pelės mygtuku spustelėkite įrašus ir pasirinkite **Įrašyti viską kaip HAR su turiniu**.

### <a name="microsoft-edge"></a>„Microsoft Edge“

1. Atidarytame skirtuke paspauskite **F12** arba pasirinkite **Programavimo įrankiai**, kad atidarytumėte programavimo įrankius.
2. Atidarykite skirtuką **Tinklas**.
3. Vykdykite scenarijų.
4. Pasirinkite **įrašyti**, kad eksportuotumėte rezultatus kaip HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
