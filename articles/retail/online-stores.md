---
title: Interneto parduotuvės kanalo integravimas
description: Šiame straipsnyje pateikiama informacija apie mažmeninės prekybos internetinių parduotuvių kanalus ir kaip juos nustatyti programoje „Dynamics 365 Retail“.
author: kfend
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: e7932879aac6ea4054f6c35de99f11c2662dd472
ms.sourcegitcommit: 595a4ec63a32bd5d4321126bda7cf72a75a930a2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2019
ms.locfileid: "2688814"
---
# <a name="set-up-an-online-store-channel"></a>Interneto parduotuvės kanalo integravimas

[!include [banner](includes/banner.md)]

Šiame straipsnyje pateikiama informacija apie mažmeninės prekybos internetinių parduotuvių kanalus ir kaip juos nustatyti programoje „Dynamics 365 Retail“.

„Retail“ palaiko kelis mažmeninės prekybos kanalus. Šie mažmeninės prekybos kanalai apima interneto parduotuves, skambučių centrus ir mažmeninės prekybos parduotuves (taip pat vadinamas fizinėmis parduotuvėmis). Internetinė parduotuvė suteikia pardavėjui galimybę parduoti produktus internete, todėl klientai gali juos pirkti ne tik iš fizinės parduotuvės, bet ir iš internetinės parduotuvės. Klientams, kurie perka produktus iš internetinės parduotuvės, produktai gali būti pristatyti arba jie gali atsiimti juos vietinėje mažmeninės prekybos parduotuvėje. Galite sukurti internetinę parduotuvę naudodami „Retail“ klientą. Tokiu atveju ši internetinė parduotuvė bus paskelbta trečiosios šalies internetinėje parduotuvėje, kuri yra integruota su „Retail“. Trečiosios šalies internetinės parduotuvės veikia kaip jūsų internetinės parduotuvės pirmasis lygmuo (UI), kuris suteikia galimybę pasirinkti kliento valdymo sistemos (CMS) ir UI pajėgumus. Galimi keli šio tipo integravimai. Internetinės parduotuvės ypatybės, kurias nurodote , valdo interneto parduotuvės veikimą. Pvz., nurodote „Retail“ naršymo kategorijų hierarchiją ir priskiriate naršymo kategorijų hierarchiją internetinei parduotuvei. Kai paskelbiate savo internetinę parduotuvę trečiosios šalies internetinėje parduotuvėje, naršymo kategorijų hierarchija rodoma šioje internetinės parduotuvės versijoje. Pirkėjai naudoja naršymo kategorijų hierarchiją naršydami internetinę parduotuvę ir ieškodami produktų. Norėdami sukurti internetinę parduotuvę, turite nustatyti komponentus, kurie įgalina operacijų apdorojimą parduotuvėje. Pavyzdžiui, turite įtraukti asortimentus, taikyti atributus ir nustatyti mokėjimo bei pristatymo metodus. Taip pat galite nurodyti kainas, akcijas, reklamas, pardavimo sutartis ir pristatymo sąlygas, kurios skiriasi kiekvienoje konkrečioje parduotuvėje. Paskelbę savo internetinę parduotuvę trečiosios šalies internetinėje parduotuvėje, galite sukurti internetinės parduotuvės mažmeninės prekybos produktų katalogus. Produktai kataloge tampa produktų sąrašais internetinėje parduotuvėje. Kai pirkėjas perka produktus iš internetinės parduotuvės, prieinamos atsargos atnaujinamos ir sinchronizuojamos kliento programoje. Be to, sugeneruojami pirkimų pardavimo užsakymai ir nusiunčiami į kliento programą, kad užsakymas būtų įvykdytas ir apdorotas.

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

## <a name="retail-channel-navigation-hierarchies"></a>Mažmeninės prekybos kanalo naršymo hierarchijos

Prieš kurdami internetinę parduotuvę, turite nustatyti mažmeninės prekybos kanalų hierarchiją, kurią norite joje naudoti. Mažmeninės prekybos kanalų naršymo hierarchija nurodo kategorijų hierarchiją, rodomą internetinėje parduotuvėje, kai parduotuvė paskelbiama. Kai paskelbiate mažmeninės prekybos produktų katalogus internetinėje parduotuvėje, produktai kataloge susiejami su kategorijomis mažmeninės prekybos kanalų naršymo hierarchijoje. Pirkėjai naudoja hierarchiją naršyti internetinėje parduotuvėje.

## <a name="organization-hierarchies"></a>Organizacijų hierarchijos

Organizacijos hierarchijos naudojamos mažmeninės prekybos kanalams struktūrizuoti. Organizacijos hierarchijos nurodo ryšius tarp organizacijų, kurios sudaro jūsų verslą. Kai nustatote internetines parduotuves, galite įtraukti jas į organizacijos hierarchiją. Tada parduotuvės bendrina duomenis, kurie naudojami asortimentams, papildymams ir ataskaitoms. Kai sukuriate organizacijos struktūrą, jai priskiriate paskirtį. Paskirtis nurodo, kaip hierarchija naudojama verslo struktūroje. Galite sukurti vieną organizacijos hierarchiją parduotuvės operacijoms ir naudoti tą hierarchiją asortimentams, papildymui ir ataskaitoms. Kitu atveju galite sukurti atskiras kiekvienos paskirties organizacijos hierarchijas. Taip pat galite sukurti kelias hierarchijas, turinčias tą pačią paskirtį, ir priskirti atskirą kanalą kiekvienai iš jų. Jei ketinate skelbti mažmeninės prekybos produktų katalogus internetinėje parduotuvėje, turite įtraukti internetinę parduotuvę bent į asortimentams skirtą organizacijos struktūrą. Produktai kataloge yra parenkami iš asortimentų, kurie yra priskirti internetinei parduotuvei. Paskelbus katalogą, skelbimo procesas palygina asortimento, priskirto internetinei parduotuvei, įsigaliojimo datas su produktais, įtrauktais į katalogą, kad nustatytų, kurie produktai pasiekiami internetinėje parduotuvėje.
