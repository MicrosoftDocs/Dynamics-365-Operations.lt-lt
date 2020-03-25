---
title: Interneto parduotuvės kanalo integravimas
description: Šiame straipsnyje pateikiama informacija apie internetinės parduotuvės kanalus ir kaip juos nustatyti naudojant „Dynamics 365 Commerce“.
author: kfend
manager: AnnBe
ms.date: 03/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b719e40720b091eec879edf332ab63db710a1ebc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096899"
---
# <a name="set-up-an-online-store-channel"></a>Interneto parduotuvės kanalo integravimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie internetinės parduotuvės kanalus ir kaip juos nustatyti naudojant „Dynamics 365 Commerce“.

„Commerce“ palaiko kelis mažmeninės prekybos kanalus. Šiuos kanalus sudaro internetinės parduotuvės, skambučių centrai ir mažmeninės prekybos parduotuvės (dar vadinamos tradicinėmis parduotuvėmis). Internetinė parduotuvė suteikia pardavėjui galimybę parduoti produktus internete, todėl klientai gali juos pirkti ne tik iš fizinės parduotuvės, bet ir iš internetinės parduotuvės. Jei klientai perka produktus iš internetinės parduotuvės, jie gali būti jiems atsiųsti, arba klientai gali juos išsirinkti vietinėje parduotuvėje. 

Sukuriate internetinę parduotuvę „Commerce“ kliente. Tada ši internetinė parduotuvė skelbiama trečiųjų šalių internetinėje parduotuvėje, kuri integruota į „Commerce“. Trečiosios šalies internetinės parduotuvės veikia kaip jūsų internetinės parduotuvės pirmasis lygmuo (UI), kuris suteikia galimybę pasirinkti kliento valdymo sistemos (CMS) ir UI pajėgumus. Galimi keli šio tipo integravimai. 

Internetinės parduotuvės ypatybės, kurias nurodote , valdo interneto parduotuvės veikimą. Pavyzdžiui, nustatote naršymo kategorijų hierarchiją ir priskiriate ją internetinei parduotuvei. Kai paskelbiate savo internetinę parduotuvę trečiosios šalies internetinėje parduotuvėje, naršymo kategorijų hierarchija rodoma šioje internetinės parduotuvės versijoje. Pirkėjai naudoja naršymo kategorijų hierarchiją naršydami internetinę parduotuvę ir ieškodami produktų. 

Norėdami sukurti internetinę parduotuvę, turite nustatyti komponentus, kurie įgalina operacijų apdorojimą parduotuvėje. Pavyzdžiui, turite įtraukti asortimentus, taikyti atributus ir nustatyti mokėjimo bei pristatymo metodus. Taip pat galite nurodyti kainas, akcijas, reklamas, pardavimo sutartis ir pristatymo sąlygas, kurios skiriasi kiekvienoje konkrečioje parduotuvėje. 

Paskelbę internetinę parduotuvę trečiųjų šalių internetinėje parduotuvėje, galite sukurti internetinės parduotuvės produktų katalogus. Produktai kataloge tampa produktų sąrašais internetinėje parduotuvėje. Kai pirkėjas perka produktus iš internetinės parduotuvės, prieinamos atsargos atnaujinamos ir sinchronizuojamos kliento programoje. Be to, sugeneruojami pirkimų pardavimo užsakymai ir nusiunčiami į kliento programą, kad užsakymas būtų įvykdytas ir apdorotas.

## <a name="set-up-an-online-store"></a>Interneto parduotuvės nustatymas

Norėdami nustatyti internetinę parduotuvę, turite atlikti toliau nurodytus veiksmus.

1. Sukurkite internetinę parduotuvę.
2. Įtraukite internetinę parduotuvę į atitinkamas organizacijos hierarchijas.
3. Įtraukite asortimentus, kurie apima produktus, prieinamus internetinėje parduotuvėje.
4. Priskirkite arba sukurkite internetinės parduotuvės kainų grupes.
5. Nustatykite pristatymo būdus, kurie prieinami internetinėje parduotuvėje.
6. Priskirkite mokėjimo metodus, kurie priimami internetinėje parduotuvėje.
7. Jei leidžiate pirkėjams užsisakyti produktus ir atsiimti juos vietinėje parduotuvėje, priskirkite parduotuvių lokatorių grupes internetinei parduotuvei.
8. Priskirkite kanalų, produktų ir pardavimo užsakymų atributus internetinei parduotuvei. Kanalų atributai taikomi visai internetinei parduotuvei, produktų atributai taikomi produktams, kurie siūlomi internetinėje parduotuvėje, o pardavimo užsakymų atributai taikomi pardavimo užsakymams, kurie generuojami iš internetinės parduotuvės.
9. Susiekite atributus, kad nustatytumėte ypatybes, kurios nurodo, kaip atributai veikia internetinėje parduotuvėje. Pvz., galite nustatyti atributus, kurių bus reikalaujama arba kurių galima ieškoti.
10. Paskelbkite internetinę parduotuvę trečiosios šalies internetinėje parduotuvėje, kad galėtumėte sukurti norimą savo parduotuvės struktūrą.

    > [!IMPORTANT]
    > Kad galėtumėte paskelbti interneto parduotuvę, turite nustatyti internetinės parduotuvės paskirstymo vietą.

## <a name="commerce-channel-navigation-hierarchies"></a>„Commerce“ kanalo naršymo hierarchijos

Prieš sukurdami internetinę parduotuvę, turite apibrėžti „Commerce“ kanalo naršymo hierarchiją, naudojamą internetinei parduotuvei. Kanalo naršymo hierarchija žymi kategorijų hierarchiją, kuri rodoma jau paskelbtoje internetinėje parduotuvėje. Kai internetinėje parduotuvėje paskelbiate prekių katalogus, produktai kataloge yra priskiriami kategorijoms, esančioms kanalo naršymo hierarchijoje. Pirkėjai naudoja hierarchiją naršyti internetinėje parduotuvėje.

## <a name="organization-hierarchies"></a>Organizacijų hierarchijos

Organizacijos hierarchijos yra naudojamos „Commerce“ kanalams sudaryti ir santykiams tarp organizacijų, kurios sudaro jūsų verslą, apibūdinti. Kai nustatote internetines parduotuves, galite įtraukti jas į organizacijos hierarchiją. Tada parduotuvės bendrina duomenis, kurie naudojami asortimentams, papildymams ir ataskaitoms. 

Kai sukuriate organizacijos struktūrą, jai priskiriate paskirtį. Paskirtis nurodo, kaip hierarchija naudojama verslo struktūroje. Galite sukurti vieną organizacijos hierarchiją parduotuvės operacijoms ir naudoti tą hierarchiją asortimentams, papildymui ir ataskaitoms. 

Kitu atveju galite sukurti atskiras kiekvienos paskirties organizacijos hierarchijas. Taip pat galite sukurti kelias hierarchijas, turinčias tą pačią paskirtį, ir priskirti atskirą kanalą kiekvienai iš jų. Jei internetinėje parduotuvėje ketinate skelbti prekių katalogus, turėtumėte bent jau įtraukti internetinę parduotuvę į organizacijos hierarchiją, skirtą asortimentui. Produktai kataloge yra parenkami iš asortimentų, kurie yra priskirti internetinei parduotuvei. Paskelbus katalogą, skelbimo procesas palygina asortimento, priskirto internetinei parduotuvei, įsigaliojimo datas su produktais, įtrauktais į katalogą, kad nustatytų, kurie produktai pasiekiami internetinėje parduotuvėje.

## <a name="additional-resources"></a>Papildomi ištekliai

[Jūsų domeno vardo konfigūravimas](configure-your-domain-name.md)

[Naujos e. prekybos svetainės visuotinis diegimas](deploy-ecommerce-site.md)

[E. prekybos svetainės kūrimas](create-ecommerce-site.md)

[Interneto svetainės susiejimas su kanalu](associate-site-online-store.md)

[„Robots.txt” failų tvarkymas](manage-robots-txt-files.md)

[Masinis URL peradresavimų nusiuntimas](upload-bulk-redirects.md)

[B2C nuomotojo nustatymas „Commerce“ aplinkoje](set-up-B2C-tenant.md)

[Vartotojo prisijungimo pasirinktinių puslapių sąranka](custom-pages-user-logins.md)

[„Commerce” aplinkos kelių B2Ck nuomotojų konfigūravimas](configure-multi-B2C-tenants.md)

[Turinio pristatymo tinklo (CDN) palaikymo įtraukimas](add-cdn-support.md)

[Parduotuvės nustatymo pagal vietą įgalinimas](enable-store-detection.md)
