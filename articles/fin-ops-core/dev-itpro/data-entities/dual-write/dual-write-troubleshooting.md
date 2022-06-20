---
title: Bendroji trikčių šalinimo informacija
description: Šiame straipsnyje pateikiama bendroji trikčių diagnostikos informacija, skirta dvigubo rašymo integravimui tarp finansų ir operacijų programėlių ir Dataverse.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 620f6f999859eff0ccd8aeb1cff12ddd56fa9926
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853661"
---
# <a name="general-troubleshooting"></a>Bendroji trikčių šalinimo informacija

[!include [banner](../../includes/banner.md)]



Šiame straipsnyje pateikiama bendroji trikčių diagnostikos informacija, skirta dvigubo rašymo integravimui tarp finansų ir operacijų programėlių ir Dataverse.

> [!IMPORTANT]
> Kai kurioms šio straipsnio adresams gali reikėti sistemos administratoriaus vaidmens arba "Microsoft Azure Active Directory " () nuomininkų Azure AD administratoriaus kredencialų. Kiekvienai problemai skirtoje dalyje paaiškinama, ar reikia konkretaus vaidmens ar kredencialų.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Įgalinkite ir peržiūrėkite priedo sekimo žurnalą „Dataverse”, kad peržiūrėtumėte klaidos informaciją

Sekimo žurnalai gali būti naudingi trikčių diagnostikos dvigubo rašymo tiesioginio sinchronizavimo tarp finansų &operacijų ir tiesioginio sinchronizavimo problemų Dataverse. Žurnaluose galima pateikti konkrečią informaciją komandoms, kurios teikia "Dynamics 365" techninės ir inžinerijos palaikymo paslaugas. Šiame straipsnyje aprašoma, kaip įgalinti sekimo žurnalus ir kaip juos peržiūrėti. Sekimo žurnalai valdomi "Dynamics 365" parametrų puslapyje ir reikia administratoriaus lygio teisių, kad būtų galima keisti ir peržiūrėti. 

**Reikiamas vaidmuo, norint įjungti sekimo žurnalą ir peržiūrėti klaidas:** sistemos administratorius

### <a name="turn-on-the-trace-log"></a>Įjungti sekimo žurnalą
Norėdami įjungti sekimo žurnalą, atlikite toliau nurodytus veiksmus.

1.  Prisiregistruokite prie "Dynamics 365", tada viršutinėje **naršymo** juostoje pasirinkite Parametrai. Puslapyje Sistemos spustelėkite **Administravimas**.
2.  Administravimo puslapyje spustelėkite Sistemos **parametrai**.
3.  Pasirinkite skirtuką **Pritaikymas** ir Priedas, tada pasirinktinės darbo srauto veiklos sekimo skyriuje išplečiamasis sąrašas pakeiskite į **Visi**. Taip bus sekama visa veikla ir pateikiamas išsamus komandų, kurios turi peržiūrėti galimas problemas, duomenų rinkinys.

> [!NOTE]
> Išplečiamajame sąraše nustatoma išimtis **,** sekimo informaciją bus pateikta tik įvykstant išimtims (klaidoms).

Kai bus įjungta, priedo sekimo žurnalai bus renkami tol, kol, grįžtant į šią vietą ir pasirinkus Išjungta, jie bus išjungti rankiniu **būdu**.

### <a name="view-the-trace-log"></a>Peržiūrėti sekimo žurnalą
Norėdami peržiūrėti sekimo žurnalą, atlikite toliau nurodytus veiksmus.

1. Puslapyje "Dynamics 365" parametrai viršutinėje **naršymo** juostoje pasirinkite Parametrai. 
2. Puslapio **sekcijoje Pritaikymai** **pasirinkiteVz** Trace Log.
3. Sekimo žurnalų sąraše galite rasti įrašų, paremtų tipo pavadinimu ir (arba) pranešimo pavadinimu.
4. Atidarykite norimą įrašą, jei norite peržiūrėti visą žurnalą. Pranešimų bloke, kuris yra vykdymo skyriuje, bus pateikta turima informacija apie priedą. Jei galima, informacija apie išimtį taip pat bus pateikta. 

Galite nukopijuoti sekimo žurnalų turinį ir įklijuoti juos į kitą programą, pvz., Notepad ar kitus įrankius, kad galėtumėte peržiūrėti žurnalus ar tekstinius failus, kad būtų lengviau pamatyti visą turinį. 

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Įjungti derinimo režimą tiesioginio sinchronizavimo trikčių šalinimui finansinėse ir operacijų programėlėse

**Reikiamas vaidmuo, norint peržiūrėti klaidas:** sistemos administratorius

Dvigubo rašymo klaidos, kurios buvo kilusios Dataverse, gali būti rodomos finansų ir operacijų programoje. Norėdami įjungti daugiažodį klaidų registravimą atlikite toliau nurodytus veiksmus.

1. Visų projektų konfigūracijų finansų ir operacijų **programoje lentelėje DualWriteProjectConfiguration yra vėliavėlė** IsDebugMode **·**.
2. Atidarykite **„DualWriteProjectConfiguration”** naudodami „Excel“ papildinį. Norėdami naudoti priedą įjunkite kūrimo režimą finansų ir operacijų "Excel **" papildinyje ir pridėkite DualWriteProjectConfiguration** į lapą. Daugiau informacijos žr. skyriuje [Objekto duomenų peržiūra ir atnaujinimas programoje „Excel“](../../office-integration/use-excel-add-in.md).
3. Projekte nustatykite **IsDebugMode** kaip **Taip**.
4. Vykdyti scenarijų, kuris generuoja klaidas.
5. Daugiažodžiai žurnalai saugomi lentelėje **DualWriteErrorLog**.
6. Norėdami peržvelgti duomenis lentelių naršyklėje, naudokite šį saitą: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`, jei reikia, pakeiskite `999`.
7. Atnaujinkite dar kartą pagal [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), pasiekiamą platformos naujiniui Nr. 37 ir naujesniems. Jei įdiegėte šią pataisą, derinimo režimu bus fiksuojama daugiau žurnalų.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Tikrinti finansų ir operacijų programos virtualiojoje mašinoje sinchronizavimo klaidas

**Reikiamas vaidmuo, norint peržiūrėti klaidas:** sistemos administratorius

1. Prisijunkite prie „Microsoft Dynamics“ portale „Lifecycle Services“ (LCS).
2. Atidarykite LCS projektą, kurį pasirinkote dvigubo rašymo testavimui atlikti.
3. Pasirinkite plytelę **Aplinkos diegimo debesyje įrankis**.
4. Norėdami prisijungti prie finansų ir operacijų programos virtualiosios mašinos (VM), naudokite nuotolinį darbalaukį. Naudokite vietinę paskyrą, kurį yra rodoma LCS.
5. Atidarykite įvykių peržiūros programą.
6. Pasirinkite **Programų ir paslaugų žurnalai \> „Microsoft“ \> „Dynamics“ \> „AX-DualWriteSync“ \> Veikia**.
7. Peržiūrėti naujausių klaidų sąrašą.

## <a name="dual-write-ui-landing-page-showing-blank"></a>Dvigubo rašymo vartotojo sąsajos puslapis rodomas tuščias
Atverdami dvigubo rašymo Microsoft Edge puslapį ar "Skirtukų chrom" naršyklėje, pagrindinis puslapis neįkeliamas, o jūs matote tuščią puslapį arba klaidą, pvz., "Kažkas negerai".
Devtoolse įvyko klaida konsolės žurnaluose:

>bundle.eed39124e62c58ef34d2.js:37 DOMException: nepavyko nuskaityti ypatybės sessionStorage iš Langas: prieiga prie šio dokumento uždrausta. t.storeInSessionStorage ( ) nauju t (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:16:136860 https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:69:20103) eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:44115) Eo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:58728) jo (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:65191) metu Nr. (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:84692) arba (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:85076) Ss (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91750) ir (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:91130 s ) hs (https://dataintegrator.trafficmanager.net/bundle.eed39124e62c58ef34d2.js:37:90151)

Vartotojo sąsajos naudoja naršyklę seanso saugykla, kad saugoma kai kurių ypatybių vertė, skirta pagrindinio puslapio įkėlimui. Kad tai veiktų, svetainės naršyklėje turi būti leidžiami trečiosios šalies sausainiai. Klaida yra indikatyvi vartotojo sąsajos, kurios nepavyko pasiekti seanso saugykla, indikatyvi. Gali būti du scenarijai, su kuriais susiduriama su šia problema:

1.  Vartotojo SĄSAJĄ atidarote atpažinus "Edge/Chrom" ir trečiosios šalies sausainius" incognito režimu.
2.  Jūs visiškai užblokavote trečiosios šalies sausainius –Edge/Chrom.

### <a name="mitigation"></a>Mažinimo priemonė
Naršyklės nustatymuose turi būti leidžiami trečiosios šalies sausainiai.

### <a name="google-chrome-browser"></a>"Vz." chromuotas naršyklė
1-asis variantas:
1.  Eikite į parametrus įvesdami chrome://settings/ į adresų juostą, tada eikite į Privatumas ir sauga -> Sausainiai ir kiti svetainės duomenys.
2.  Pasirinkite Leisti visus sausainius. Jei nenorite to daryti, pereikite prie antros pasirinkties.

2-asis variantas:
1.  Eikite į parametrus įvesdami chrome://settings/ į adresų juostą, tada eikite į Privatumas ir sauga -> Sausainiai ir kiti svetainės duomenys.
2.  Jei pasirinkta "Blokuoti trečiosios šalies sausainius", "Blokuoti trečiosios šalies sausainius" arba "Blokuoti trečiosios šalies sausainius", eikite į "Sites", kuri visada gali naudoti sausainius, ir spustelėkite **Įtraukti**. 
3.  Įtraukite finansų & operacijų programėlių svetainės pavadinimą – https://<your_FinOp_instance>.cloudax.dynamics.com. Įsitikinkite, kad pažymėsite žymės langelį "Visi sausainiai" tik šioje svetainėje. 

### <a name="microsoft-edge-browser"></a>Microsoft Edge Naršyklės
1.  Pereikite prie Parametrų – > Svetainės teisės - > sausainius ir svetainės duomenis.
2.  Išjungti parinktį Blokuoti trečiosios šalies sausainius.  

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Atsieti ir susieti kitą Dataverse aplinką nuo finansų ir operacijų programos

**Būtinas vaidmuo norint atsieti aplinką: sistemos** administratorius finansų ir operacijų programai arba Dataverse.

1. Prisiregistruokite finansų ir operacijų programoje.
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

## <a name="how-to-ensure-data-integration-is-using-the-most-current-finance-and-operations-schema"></a>Kaip užtikrinti duomenų integravimą naudojant dabartinę finansų ir operacijų schemą

Duomenų integravimo metu gali kilti problemų dėl naujausias schemas. Toliau pateikti veiksmai padės atnaujinti finansų ir operacijų programėlių objektų sąrašą ir duomenų integratoriaus objektus.

### <a name="refresh-entity-list-in-finance-and-operations-environment"></a>Atnaujinti objektų sąrašą finansų ir operacijų aplinkoje
1.  Prisiregistruokite prie savo finansų ir operacijų aplinkos.
2.  Pasirinkite **Duomenų valdymą**.
3.  Duomenų valdymo viduje pasirinkite Sistemos **parametrus**.
4.  Puslapyje Duomenų **importavimo / eksportavimo sistemos** parametrai pasirinkite skirtuką **Objekto parametrai** ir pasirinkite Atnaujinti **objektų sąrašą**. Atsižvelgiant į susijusių objektų skaičių, atnaujinimas gali užtrukti ilgiau nei 30 minučių.
5.  Eikite į **duomenų valdymą** ir pasirinkite **Duomenų objektus,** norėdami patikrinti, ar pateikti numatomi objektai. Jei numatomi objektai nėra išvardyti, patikrinkite, ar objektai rodomi jūsų finansų ir operacijų aplinkoje ir, jei reikia, atkurkite trūkstamus objektus.

#### <a name="if-the-refresh-fails-to-resolve-the-issue-delete-and-re-add-the-entities"></a>Jei atnaujinimo nepavyko išspręsti problemos, panaikinkite ir iš naujo įtraukite objektus

> [!NOTE]
> Jums gali reikėti sustabdyti visas apdorojimo grupes, kurios prieš ištrinant aktyviai naudoja objektus.

1.  Pasirinkite **duomenų valdymą** savo finansų ir operacijų aplinkoje ir pasirinkite **Duomenų objektai**.
2.  Ieškoti objektų, turinčių problemų, ir pažymėti paskirties objektą, išdėstymo lentelę, objekto pavadinimą ir kitus parametrus. Panaikinkite objektą arba objektus iš sąrašo.
3.  Pasirinkite **Naujas** ir iš naujo įtraukite objektą arba objektus naudodami 2 veiksmo duomenis. 

#### <a name="refresh-entities-in-data-integrator"></a>Atnaujinti objektus duomenų integratoriu
Prisiregistruokite administravimo Power Platform centre ir pasirinkite duomenų **integravimą**. Atidarykite projektą, kuriame atsiranda problemų, ir pasirinkite Atnaujinti **objektus**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Kaip įjungti ir įrašyti tinklo sekimą, kad sekimus būtų galima pridėti prie palaikymo kvitų

Palaikymo komandai gali reikėti peržiūrėti tinklo sekimus, siekiant diagnozuoti ir pašalinti kai kurias triktis. Norėdami sukurti tinklo sekimą, atlikite toliau nurodytus veiksmus.

### <a name="google-chrome-browser"></a>"Vz." chromuotas naršyklė

1. Atidarytame skirtuke paspauskite **F12** arba pasirinkite **Programavimo įrankiai**, kad atidarytumėte programavimo įrankius.
2. Atverkite skirtuką **Tinklas** ir filtro teksto lauke įveskite **integ**.
3. Vykdykite savo scenarijų ir atsižvelkite į registruojamas užklausas.
4. Dešiniuoju pelės mygtuku spustelėkite įrašus ir pasirinkite **Įrašyti viską kaip HAR su turiniu**.

### <a name="microsoft-edge-browser"></a>Microsoft Edge Naršyklės

1. Atidarytame skirtuke paspauskite **F12** arba pasirinkite **Programavimo įrankiai**, kad atidarytumėte programavimo įrankius.
2. Atidarykite skirtuką **Tinklas**.
3. Vykdykite scenarijų.
4. Pasirinkite **įrašyti**, kad eksportuotumėte rezultatus kaip HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
