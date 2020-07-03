---
title: Kliento portalo vartotojų kūrimas ir valdymas
description: Šioje temoje paaiškinama, kaip sukurti kliento portalo vartotojų paskyras ir nustatyti jų teises.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: c56e41b8ea5039531205083b5b42aff05e05cf66
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413991"
---
# <a name="create-and-manage-customer-portal-users"></a>Kliento portalo vartotojų kūrimas ir valdymas

Parengtame naudoti sprendime nėra būdo vartotojams patiems užsiregistruoti svetainėse, sukurtose naudojant kliento portalą. Norėdami prisijungti ir naudoti svetainę, vartotojai turi gauti administratoriaus pakvietimą. „Microsoft“ tyčia užblokavo galimybę vartotojams registruotis savarankiškai.

Norint, kad vartotojas galėtų naudotis svetaine, pirmiausia reikia sukurti to vartotojo kontakto įrašą. Šiame įraše nurodoma, kuriai kliento paskyrai ir juridiniam subjektui priklauso vartotojas. Ši informacija yra būtina siekiant užtikrinti, kad vartotojas galėtų kurti ir peržiūrėti pardavimo užsakymus.

Kai vartotojai užsiregistruoja patys, jiems automatiškai sukuriami kontaktų įrašai. Todėl negalite užtikrinti, kad vartotojas pasirinks tinkamą kliento paskyrą ir juridinį subjektą. Pakvietimo procesas suteikia administratoriui galimybę priskirti teisingą kliento paskyrą ir juridinį subjektą kontakto įrašui prieš išsiunčiant pakvietimą. Jei ketinate pritaikyti priemonę taip, kad vartotojai galėtų registruotis savarankiškai, būtinai atsižvelkite į galimas pasekmes.

## <a name="prerequisite-setup"></a>Būtinieji nustatymo veiksmai

„Power Apps“ portaluose esantys kontaktai saugomi kaip įrašai „Common Data Service“ objekte **Kontaktai**. Tada dvigubo rašymo funkcija pagal poreikį sinchronizuoja šiuos įrašus su „Microsoft Dynamics 365 Supply Chain Management“.

![![Kliento portalo kontaktų sistemos schema](media/customer-portal-contacts.png "Kliento portalo kontaktų sistemos schema")](media/customer-portal-contacts.png "System diagram for Customer portal contacts")

Prieš pradėdami kviesti naujus klientus, įsitikinkite, kad dvigubo rašymo funkcijoje įjungėte susiejimą su objektu **Kontaktas**.

## <a name="the-invitation-process"></a>Pakvietimo procesas

Norėdami pakviesti esamą kontaktinį asmenį į klientų portalą, atlikite „Power Apps“ portalų dokumentacijos temoje [Kontaktų pakvietimas į portalus](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) pateiktus veiksmus.

Prieš kviesdami klientą prisijungti prie kliento portalo, įsitikinkite, kad kliento [kontakto įrašas](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) yra pasiekiamas ir nustatytas kaip nurodyta toliau.

1. Lauke **Įmonė** pasirinkite juridinį subjektą, kuriam norite priskirti klientą „Supply Chain Management“ sistemoje.
2. Lauke **Paskyros numeris** pasirinkite kliento paskyros numerį, kuris vartotojui bus priskirtas „Supply Chain Management“ sistemoje.

Sukūrę kontaktą, galėsite jį peržiūrėti „Supply Chain Management“ sistemoje.

Norėdami gauti daugiau informacijos, žr. temą [Portale naudojamo kontakto konfigūravimas](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) „Power Apps“ portalų dokumentacijoje.

## <a name="out-of-box-web-roles-and-entity-permissions"></a>Parengti naudoti žiniatinklio vaidmenys ir objektų teisės

Vartotojų vaidmenis „Power Apps“ portaluose nurodo [žiniatinklio vaidmenys](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) ir [objektų teisės](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions). Kliento portale iš karto yra nustatyti keli vaidmenys. Galite kurti naujus vaidmenis ir modifikuoti arba pašalinti esamus vaidmenis.

### <a name="out-of-box-web-roles"></a>Iš anksto parengti tinklapio vaidmenys

Šiame skyriuje aprašomi žiniatinklio vaidmenys, kurie tiekiami su kliento portalu.

Norėdami gauti daugiau informacijos apie tai, kaip modifikuoti iš anksto parengtus vartotojų vaidmenis, žr. temas [Žiniatinklio vaidmenų kūrimas portaluose](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) ir [Įrašu pagrįstos saugos įtraukimas į portalus naudojant objektų teises](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) „Power Apps“ portalų dokumentacijoje.

#### <a name="administrator"></a>Administratorius

Administratorius prižiūri ir tvarko svetainę. Šis asmuo parengs ir nustatys kliento portalą. Administratorius tvarko portalo IT bei saugos aspektus ir pasirūpina, kad viskas veiktų sklandžiai. Administratorius taip pat gali tinkinti ir (arba) keisti portalą įtraukdamas naujų funkcijų, kurdamas naujus vaidmenis ir atlikdamas kitus pakeitimus.

#### <a name="customer-representative"></a>Kliento atstovas

Kliento atstovas dirba kliento įmonėje ir yra atsakingas už įmonės teikiamų užsakymų valdymą. Kliento atstovas gali matyti visus užsakymus, kurie buvo pateikti įmonei, ir juos pateikusius vartotojus. Be to, kliento atstovas gali matyti informaciją apie bendrą paskyrą ir kurie kontaktai gali teikti užsakymus tos paskyros vardu.

#### <a name="authorized-users"></a>Įgaliotieji vartotojai

Įgaliotieji vartotojai gali pateikti užsakymus ir peržiūrėti jiems pateiktų užsakymų būseną. Tačiau jie negali peržiūrėti kitų įmonės vartotojų pateiktų užsakymų būsenos.

#### <a name="unauthorized-users"></a>Teisių neturintys vartotojai

Teisių neturintys vartotojai negali peržiūrėti jokių duomenų. Jie gali matyti tik viešą informaciją, pvz., sąlygas ir informaciją apie įmonę, kuriai priklauso kliento portalas.

#### <a name="example"></a>Pavyzdys

Toliau pateiktoje lentelėje parodyta, kuriuos pardavimo užsakymus sistemoje gali peržiūrėti konkrečius žiniatinklio vaidmenis turintys vartotojai.

| Pardavimo užsakymas | Administratorius | Kliento atstovas klientui &nbsp;X | Įgaliotasis vartotojas: Jane | Įgaliotasis vartotojas: Sam | Teisių neturintis vartotojas: May |
|---|---|---|---|---|---|
| Kliento&nbsp;X užsakovas:&nbsp;Jane | Taip | Taip | Taip | nr. | nr. |
| Kliento&nbsp;X užsakovas:&nbsp;Sam | Taip | Taip | nr. | Taip | nr. |
| Kliento&nbsp;Y užsakovas:&nbsp;May | Taip | nr. | nr. | nr. | nr. |

> [!NOTE]
> Nors tiek Sam, tiek Jane yra kontaktai, kurie dirba klientui X, jie gali matyti tik tuos užsakymus, kuriuos pateikė patys, ir nieko daugiau. Nors May sistemoje pateikė užsakymą, ji negali matyti to užsakymo kliento portale, nes ji yra teisių neturinti vartotoja. (Be to, ji užsakymą pateikė per kitą kanalą, o ne per kliento portalą.)
