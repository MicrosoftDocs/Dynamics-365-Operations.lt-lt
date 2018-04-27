---
title: "Tiekėjo bendradarbiavimo mobilioji darbo sritis"
description: "Šioje temoje pateikiama informacijos apie tiekėjų bendradarbiavimo mobiliąją darbo sritį. Ši darbo sritis padeda jūsų tiekėjams matyti naujausią jiems patvirtinti atsiųstų pirkimo užsakymų informaciją. Jie taip pat gali peržiūrėti informaciją apie naujus ir atnaujintus pirkimo užsakymus ir kontaktus."
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267074
ms.assetid: 1d293b3a-2fa2-418d-9347-78c2809d67fe
ms.search.region: global
ms.author: mkirknel
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 83fcf1d0432d5afa71d6f9d7d22cea5a583777bf
ms.contentlocale: lt-lt
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-collaboration-mobile-workspace"></a>Tiekėjo bendradarbiavimo mobilioji darbo sritis

[!INCLUDE [banner](../includes/banner.md)]

Šioje temoje pateikiama informacijos apie **Tiekėjų bendradarbiavimo** mobiliąją darbo sritį. Ši darbo sritis padeda jūsų tiekėjams matyti naujausią jiems patvirtinti atsiųstų pirkimo užsakymų informaciją. Jie taip pat gali peržiūrėti informaciją apie naujus ir atnaujintus pirkimo užsakymus ir kontaktus.

Ši mobilioji darbo sritis skirta naudoti kartu su mobiliąja programa „Microsoft Dynamics 365 for Unified Operations“.

## <a name="overview"></a>Apžvalga 
**Tiekėjų bendradarbiavimo** mobilioji darbo sritis suteikia tiekėjams informacijos apie naujus pirkimo užsakymus, tad jie gali juos peržiūrėti ir reaguoti naudodami „Microsoft Dynamics 365 for Finance and Operations“ žiniatinklio klientą. 

>[!NOTE]
> Mobilioji darbo sritis turėtų būti naudojama kaip tiekėjų bendradarbiavimo žiniatinklio sąsajos papildymas, bet ne pakaitalas. 

Jūsų tiekėjai gali naudoti **Tiekėjų bendradarbiavimo** mobiliąją darbo sritį norėdami peržiūrėti naujus jiems patvirtinti išsiųstus pirkimo užsakymus. Joje rodoma pirkimo užsakymų informacija, pvz., produktai, kiekiai ir pageidaujamos pristatymo datos. Kainų informacija taip pat pasiekiama atsižvelgiant į kiekvieno tiekėjo konfigūraciją. 

Vartotojas, kuris prisijungia kaip tiekėjas, matys, į kuriuos pirkimo užsakymus atsakyta ir kurie dar laukia kliento veiksmų. Pavyzdžiui, pirkimo užsakymas gali laukti kliento veiksmo, nes tiekėjas pasiūlė kitą pristatymo datą, bet klientas su ta data dar nesutiko. Tiekėjui taip pat bus pateikiamas patvirtintų pirkimo užsakymų, kurių produktai dar nepristatyti, sąrašas. 

Norėdamas atsakyti į pirkimo užsakymą, tiekėjas turi naudoti tiekėjų bendradarbiavimo žiniatinklio sąsają, kuri pasiekiama naudojant žiniatinklio klientą. Čia tiekėjas gali gauti ir daugiau informacijos apie užsakymą, pvz., apie dokumentų priedus, pristatymo adresą kiekvienoje eilutėje ar su tiekėju susijusius mokesčius. 

Tiekėjai, turintys specialų saugos vaidmenį, galės matyti tiekėjo sąskaitoje užregistruotus kontaktinius asmenis. Tas pats saugos vaidmuo leidžia tiekėjui matyti bet kurios pateiktos vartotojo užklausos būseną. 

Tiekėjo bendradarbiavimo žiniatinklio sąsaja žiniatinklio kliente turi būti naudojama norint sukurti naujų kontaktų ir pateikti naujų vartotojų užklausų. 

**Tiekėjų bendradarbiavimo** mobiliojoje darbo srityje tiekėjas gali atlikti šias užduotis:

-   Peržiūrėkite naujus tiekėjui nusiųstus pirkimo užsakymus.
-   Peržiūrėkite pirkimo užsakymus, į kuriuos tiekėjas atsakė ir kurie laukia kliento veiksmo.
-   Peržiūrėkite pirkimo užsakymus, kurie buvo patvirtinti, bet dar ne iki galo gauti.
-   Peržiūrėkite kontaktinio asmens informaciją, užregistruotą tiekėjo sąskaitoje. (Šiai užduočiai reikia papildomo saugos vaidmens.)
-   Peržiūrėkite informaciją apie vartotojo užklausą, kurią pateikė tiekėjas, ir stebėkite užklausos būseną. (Šiai užduočiai reikia papildomo saugos vaidmens.)

## <a name="prerequisites"></a>Būtinieji komponentai
Būtinosios sąlygos skiriasi ir priklauso nuo jūsų organizacijoje visuotinai įdiegtos „Microsoft Dynamics 365“ versijos.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>Būtinosios sąlygos, jeigu naudojate „Microsoft Dynamics 365 for Finance and Operations“ 
Jei jūsų organizacijoje visuotinai įdiegtas „Microsoft Dynamics 365 for Finance and Operations“, sistemos administratorius turi paskelbti mobiliąją darbo sritį **Tiekėjų bendradarbiavimas**. Instrukcijų ieškokite dalyje [Mobiliosios darbo srities publikavimas](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Būtinosios sąlygos, jei naudojate „Microsoft Dynamics 365 for Operations“ 1611 versiją su 3 platformos naujinimu arba naujesnę versiją
Jei jūsų organizacijoje visuotinai įdiegta „Microsoft Dynamics 365 for Operations‟ 1611 versija su 3 platformos naujinimu arba naujesnė versija, sistemos administratorius turi įvykdyti tolesnes būtinąsias sąlygas. 

<table>
<thead>
<tr class="header">
<th>Būtinoji sąlyga</th>
<th>Vaidmuo</th>
<th>aprašymas</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>KB 3216943 reikia įdiegti, jei naudojate platformos 3 naujinimą.</td>
<td>Sistemos administratorius</td>
<td>KB 3216943 yra dvejetainis naujinimas, būtinas, jei naudojate platformos 3 naujinimą. Norėdamas įdiegti šią KB, sistemos administratorius turi atlikti šiuos veiksmus.
<ol>
<li>Atsisiųskite KB 3216943 iš „Microsoft Dynamics“ „Lifecycle Services“ (LCS).</li>
<li>Įdiekite dvejetainį naujinimą, kuris pristatomas kaip įdiegiamas paketas. Informacijos apie tai, kaip taikyti įdiegiamą paketą, rasite <a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Visuotinai įdiegiamo paketo taikymas</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Reikia įdiegti KB 4013633.</td>
<td>Sistemos administratorius</td>
<td>KB 4013633 yra X++ naujinimas arba metaduomenų karštoji pataisa, kurioje yra mobilioji darbo sritis <strong>Turimos atsargos</strong>. Norėdamas įdiegti KB 4013633, sistemos administratorius turi atlikti tolesnius veiksmus.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Atsisiųsti metaduomenų karštąją pataisą iš LCS</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Įdiekite metaduomenų karštąją pataisą</a>.</li><li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Sukurkite diegiamą paketą</a>, kuriame yra modelis <strong>SCMMobile</strong>, o tada įkelkite diegiamą paketą į LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Visuotinai diegiamo paketo taikymas</a>.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>Tiekėjų bendradarbiavimo</strong> mobilioji darbo sritis turi būti paskelbta.</td><td>Sistemos administratorius</td>
<td>Žr. <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiliosios darbo srities publikavimas</a>.</td>
</tr>
<tr class="even">
<td>Su tiekėju susijęs vartotojas turi pasiekti tiekėjų bendradarbiavimo žiniatinklio sąsają žiniatinklio kliente ir nustatyti tiekėjo bendradarbiavimo vartotoją.</td><td>Pirkimo specialistai ir sistemos administratorius</td>
<td>Atlikę pateiktose temose aprašytus veiksmus nustatykite tiekėjų bendradarbiavimo žiniatinklio sąsają ir ją naudodami vykdykite veiklą.
<ul>
<li><a href="vendor-collaboration-work-external-vendors.md">Tiekėjų bendradarbiavimo sąsajos naudojimas veiklai su išoriniais tiekėjais vykdyti</a></li>
<li><a href="manage-vendor-collaboration-users.md">Tiekėjo bendradarbiavimo vartotojų valdymas</a></li>
<li><a href="set-up-maintain-vendor-collaboration.md">Tiekėjo bendradarbiavimo nustatymas ir tvarkymas</a></li>
<li><a href="vendor-collaboration-work-customers-dynamics-365-operations.md">Tiekėjų bendradarbiavimo sąsajos naudojimas dirbant su klientais programoje „Finance and Operations“</a></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiliosios programos atsisiuntimas ir diegimas

Atsisiųskite ir įdiekite mobiliąją programą „Dynamics 365 for Unified Operations“:

-   [„Android“ telefonams](https://go.microsoft.com/fwlink/?linkid=850662)
-   [„iPhone“ telefonams](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Prisijunkite prie mobiliosios programos
1.  Paleiskite programą savo mobiliajame įrenginyje.
2.  Įveskite savo „Microsoft Dynamics 365“ URL.
4.  Kai prisijungsite pirmą kartą, bus rodomas raginimas įvesti savo vartotojo vardą ir slaptažodį. Įveskite savo kredencialus.
5.  Prisijungus rodomos galimos jūsų įmonės darbo sritys. Atkreipkite dėmesį, kad sistemos administratoriui paskelbus naują darbo sritį vėliau turėsite atnaujinti mobiliųjų darbo sričių sąrašą.

    [![Patraukite norėdami atnaujinti](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="use-the-vendor-collaboration-mobile-workspace"></a>Tiekėjų bendradarbiavimo mobiliosios darbo srities naudojimas
Kai pasirinksite **Tiekėjų bendradarbiavimo** darbo sritį, matysite pateiktas pasirinktis.

![Tiekėjo bendradarbiavimo mobilioji darbo sritis](./media/vendor-collaboration-mobile-app.png)

**Tiekėjų bendradarbiavimo** darbo sritis apima nurodytus puslapius.

### <a name="contacts"></a>Kontaktai
Puslapyje **Kontaktai** galite peržiūrėti visus tiekėjo sąskaitoje nustatytus kontaktus. Joje rodomas kontaktinio asmens vardas, pagrindinis el. pašto adresas ir vartotojo pseudonimas, jei kontaktinis asmuo jį turi. Šiame puslapyje taip pat nurodoma, ar kontaktinio asmens vartotojo paskyra yra aktyvi. Kai pasirenkate kontaktą, pamatysite kontaktinę informaciją, pvz., juridinius subjektus, kurių kontaktas asmuo yra. Be to, matysite kontaktinę informaciją, pvz., telefono numerį arba alternatyvų el. pašto adresą.

### <a name="user-requests"></a>Vartotojų užklausos
Puslapyje **Vartotojų užklausos** galite peržiūrėti visas naudojant tiekėjų bendradarbiavimo žiniatinklio sąsają pateiktas vartotojų užklausas. Taip pat galite stebėti tų užklausų būseną. Pasirinkus vartotojo užklausą galima peržiūrėti užklausoje pateiktą informaciją, įtraukti ar išjungti vartotoją, keisti saugą bei peržiūrėti prašytus vartotojo saugos vaidmenis.

### <a name="purchase-orders-ready-for-review"></a>Parengti peržiūrėti pirkimo užsakymai
Puslapyje **Parengti peržiūrėti pirkimo užsakymai** galite peržiūrėti visus kliento išsiųstus pirkimo užsakymus, į kuriuos dar nėra atsakyta. Galite peržiūrėti pasirinktą užsakymo informaciją, pvz., apie pageidautus produktus ir kada tie produktai turėtų būti pristatyti. Kainų informacija taip pat pasiekiama atsižvelgiant į tiekėjo konfigūraciją.

Be to, galite peržiūrėti, ar į pirkimo užsakymą įtraukta pastabų arba priedų. Tačiau norėdami atidaryti pastabas ir priedus, turite naudoti tiekėjų bendradarbiavimo žiniatinklio sąsają žiniatinklio kliente. Pasirinkę **Pirkimo užsakymo eilutė** peržiūrėsite visas eilutes ir jų išsamią informaciją. Kiekvienoje eilutėje indikatorius nurodys, ar yra įtraukta pastabų arba priedų bei ar pristatymo adresas skiriasi nuo antraštėje rodomo pristatymo adreso.

Norėdami atsakyti į pirkimo užsakymą turėsite naudoti tiekėjų bendradarbiavimo žiniatinklio sąsają žiniatinklio kliente.

### <a name="awaiting-customer-action"></a>Laukiama kliento veiksmo
Puslapyje **Laukiama kliento veiksmo** galite rasti pirkimo užsakymus, į kuriuos atsakėte jūs arba kitas asmuo, galintis pasiekti tiekėjų bendradarbiavimo sąsają. Šiame sąraše pirkimo užsakymai pateikiami tik tada, kai klientui reikia atlikti kurį nors iš toliau nurodytų pirkimo užsakymo veiksmų:

-   Jei pirkimo užsakymas buvo atmestas, klientas turi atnaujinti arba atšaukti pradinį užsakymą, tada išsiųsti jį dar kartą. Kai pirkimo užsakymas išsiunčiamas dar kartą, jis neberodomas puslapyje **Laukiama kliento veiksmo**.
-   Jei pirkimo užsakymas buvo priimtas su pakeitimais, klientas turi atnaujinti pradinį užsakymą ir iš naujo jį išsiųsti peržiūrėti arba jį atnaujinti atsižvelgdamas į pageidaujamus pakeitimus bei iš karto patvirtinti. Abiem atvejais pirkimo užsakymas bus neberodomas puslapyje **Laukiama kliento veiksmo**.
-   Jei pirkimo užsakymas buvo priimtas, bet vis tiek rodomas puslapyje **Laukiama kliento veiksmo**, tada pirkimo užsakymas nebuvo automatiškai patvirtintas jį priėmus. Dabar laukiama, kol pirkimo agentas pakeis užsakymo būseną į **Patvirtinta**. Paprastai pirkimo užsakymas laikomas sutartimi tarp kliento ir tiekėjo, sudaroma, kai tik tiekėjas priima užsakymą. Todėl atnaujinimas į būseną **Patvirtinta** dažniausiai yra tik formalumas.

Kai pasirenkate pirkimo užsakymą, pateikiama papildomos informacijos apie atsakymą. Galite peržiūrėti išsamią kiekvienos eilutės informaciją ir atliktą veiksmą. Eilutės būsena nurodo, kuris iš toliau nurodytų atsakymų buvo pateiktas:

-   Priimta
-   Atmesta
-   Priimta su pakeitimais
-   Pakeistas / pakaitas
-   Išskaidytas grafike / grafiko eilutė

Atkreipkite dėmesį, kad laukas **Pristatymas** nustatomas į **Taip** arba **Ne** siekiant nurodyti, ar eilutės bus pristatomos. Eilutė gali būti nepristatoma dėl tokių priežasčių:

- Eilutė buvo atmesta.
- Buvo atliktas pakeitimas ir pradinės eilutės nesitikima pristatyti kaip buvo pageidaujama gautame užsakyme.
- Eilutė buvo padalyta į kelias grafiko eilutes, o pradinės eilutės nesitikima pristatyti kaip buvo pageidaujama gautame užsakyme.

Rodomi visi pakeitimai, atlikti užsakymo eilutės atsakyme. Tačiau nerodomos įkeltos pastabos ir priedai. Norėdami peržiūrėti pastabas ir priedus, turite naudoti tiekėjų bendradarbiavimo žiniatinklio sąsają žiniatinklio kliente.

### <a name="open-confirmed-orders"></a>Atidaryti patvirtintus užsakymus
Kai klientas patvirtins pirkimo užsakymą (t. y. jo būsena bus pakeista į **Patvirtinta**), užsakymas pasirodys atidarytame patvirtiname užsakyme. Šiame sąraše jis bus rodomas tol, kol bus užregistruotas kaip gautas kliento.

