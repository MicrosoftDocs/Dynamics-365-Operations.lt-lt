---
title: Mobilioji darbo sritis Pirkimo užsakymų tvirtinimas
description: Šiame straipsnyje pateikiama informacija apie pirkimo užsakymo patvirtinimo mobiliąją darbo sritį, kuri leidžia peržiūrėti pirkimo užsakymus ir atsakyti į juos veiksmais. Pavyzdžiui, pirkimo užsakymą galite patvirtinti arba atmesti.
author: GalynaFedorova
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 224d3ce5c9163e95de817a3446a57f07c85df757
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863859"
---
# <a name="purchase-order-approval-mobile-workspace"></a>Mobilioji darbo sritis Pirkimo užsakymų tvirtinimas

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../../fin-ops-core/dev-itpro/includes/mobile-app-deprecation-banner.md)]

Šiame straipsnyje pateikiama informacija apie pirkimo užsakymo **patvirtinimo mobiliąją** darbo sritį. Šioje darbo srityje galite peržiūrėti pirkimo užsakymus ir į juos reaguoti veiksmais. Pavyzdžiui, pirkimo užsakymą galite patvirtinti arba atmesti.
 
## <a name="overview"></a>Apžvalga 
Pirkimo užsakymai, kuriuos reikia patvirtinti, pereina tvirtinimo darbo eigą. Darbo eigą gali sudaryti įvairūs veiksmai, kuriuos turi atlikti vienas ar keli asmenys. Pavyzdžiui, asmens gali būti reikalaujama atlikti užduotį ar patvirtinti pirkimo užsakymą. 

Naudodami mobiliąją darbo sritį **Pirkimo užsakymų tvirtinimas** galite lengvai peržiūrėti pirkimo užsakymus ir į juos reaguoti savo mobiliajame įrenginyje. Šioje darbo srityje taip pat galite atlikti tuos pačius darbo eigų veiksmus, kuriuos galite atlikti žiniatinklio kliente.

## <a name="prerequisites"></a>Būtinieji komponentai
Būtinosios sąlygos skiriasi ir priklauso nuo jūsų organizacijoje įdiegtos „Supply Chain Management” versijos.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Būtinosios sąlygos naudojant „Supply Chain Management” 
Jei jūsų organizacijoje įdiegta „Supply Chain Management“, sistemos administratorius turi publikuoti mobiliąją darbo sritį **Pirkimo užsakymų tvirtinimas**. Instrukcijų ieškokite dalyje [Mobiliosios darbo srities publikavimas](../../fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Būtinosios sąlygos, jei naudojate „Microsoft Dynamics 365 for Operations“ 1611 versiją su 3 platformos naujinimu arba naujesnę versiją
Jei jūsų organizacijoje visuotinai įdiegta „Microsoft Dynamics 365 for Operations“ 1611 versija su 3 platformos naujinimu arba naujesnė versija, sistemos administratorius turi įvykdyti tolesnes būtinąsias sąlygas. 

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
<td>Įdiegti KB 4017918.</td>
<td>Sistemos administratorius</td>
<td>KB 4017918 yra X++ naujinimas arba karštoji metaduomenų pataisa su mobiliąja darbo sritimi <strong>Pirkimo užsakymų tvirtinimas</strong>. Norėdamas įdiegti KB 4017918, sistemos administratorius turi atlikti tolesnius veiksmus.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Atsisiųsti metaduomenų karštąją pataisą iš „Microsoft Dynamics Lifecycle Services“ (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Įdiekite metaduomenų karštąją pataisą</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Sukurkite diegiamą paketą</a>, kuriame yra modelis <strong>SCMMobile</strong>, o tada įkelkite diegiamą paketą į LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Visuotinai diegiamo paketo taikymas</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publikuoti mobiliąją darbo sritį <strong>Pirkimo užsakymų tvirtinimas</strong>.</td>
<td>Sistemos administratorius</td>
<td>Žr. <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiliosios darbo srities publikavimas</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiliosios programos atsisiuntimas ir diegimas
Atsisiųskite ir įdiekite mobiliąją programą „Finance and Operations”.

- [„Android“ telefonams](https://go.microsoft.com/fwlink/?linkid=850662)
- [„iPhone“ telefonams](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>Prisijunkite prie mobiliosios programos

1. Paleiskite programą savo mobiliajame įrenginyje.
2. Įveskite savo „Microsoft Dynamics 365“ URL.
3. Kai prisijungsite pirmą kartą, bus rodomas raginimas įvesti savo vartotojo vardą ir slaptažodį. Įveskite savo kredencialus.
4. Prisijungus rodomos galimos jūsų įmonės darbo sritys. Atkreipkite dėmesį, kad sistemos administratoriui paskelbus naują darbo sritį vėliau turėsite atnaujinti mobiliųjų darbo sričių sąrašą.

![Darbo sritis Pirkimo užsakymų tvirtinimas galimų darbo sričių sąraše.](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>Jums priskirtų užsakymų peržiūra
1. Savo mobiliajame įrenginyje pasirinkite darbo sritį **Pirkimo užsakymų tvirtinimas**.
2. Pasirinkite **Man priskirti užsakymai**, kad matytumėte visus pirkimo užsakymus, su kuriais jūsų prašoma atlikti veiksmus pirkimo užsakymų tvirtinimo darbo eigoje.
3. Pasirinkite užsakymą. Puslapyje **Išsami užsakymo informacija** matysite užsakymo antraštės informaciją ir eilutes. Nurodymus taip pat galite rasti darbo eigos užduotyje.
4. Pasirinkite **Apskaitos paskirstymai**, kad atidarytumėte puslapį **Antraštės apskaitos paskirstymai**.
5. Grįžkite į puslapį **Išsami užsakymo informacija** ir pasirinkite eilutę. Išsamios užsakymo eilučių informacijos dalyje taip pat galite ištyrinėti konkrečių eilučių apskaitos paskirstymus.

## <a name="complete-an-action-on-the-purchase-order"></a>Veiksmo su pirkimo užsakymu atlikimas
Peržiūrėję jums priskirtą pirkimo užsakymą ir perskaitę darbo eigos instrukcijas, turėtumėte būti pasirengę atlikti veiksmus.

1. Savo mobiliajame įrenginyje pasirinkite darbo sritį **Pirkimo užsakymų tvirtinimas**.
2. Pasirinkite **Man priskirti užsakymai**, kad matytumėte visus pirkimo užsakymus, su kuriais jūsų prašoma atlikti veiksmus pirkimo užsakymų tvirtinimo darbo eigoje.
3. Pasirinkite užsakymą ir peržiūrėkite išsamios informacijos puslapį.
4. Pasirinkite **Veiksmai**, kad būtų rodomi galimi veiksmai. Galimi veiksmai priklauso nuo jums priskirtos užduoties.

    | Užduoties veiksmas    | Patvirtinimo veiksmas  |
    |----------------|------------------|
    | Baigti       | Tvirtinti          |
    | Grąžinti         | Atmesti           |
    | Reikalauti keitimo | Reikalauti keitimo   |
    | Perėmėjas       | Perėmėjas         |

5. Pasirinkite atitinkamą veiksmą.
6. Puslapyje **Užduoties baigimas** įveskite komentarą. Atkreipkite dėmesį, kad pasirinkę veiksmą **Perduoti** turite pasirinkti vartotoją, kuriam reikia perduoti užduotį.
7. Pasirinkite **Atlikta**. Atnaujinus darbo sritį, pirkimo užsakymo jūsų sąraše nebebus. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
