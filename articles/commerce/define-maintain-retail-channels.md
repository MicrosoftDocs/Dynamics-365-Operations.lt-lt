---
title: Apibrėžti ir prižiūrėti mažmeninės prekybos kanalus
description: Šioje temoje pateikiama tradicinių parduotuvių, kurios „Dynamics 365 Commerce“ nurodomos kaip parduotuvės, nustatymo proceso apžvalga. Jame pateikiama informacija apie užduotis, kurias turite atlikti prieš ir po parduotuvės nustatymo.
author: mugunthanm
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: ef06d79e1fa4d024dc1de0125cc72bdba5671aad384c7988dc63d407323b7abc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760207"
---
# <a name="define-and-maintain-retail-channels"></a>Mažmeninės prekybos kanalų nustatymas ir tvarkymas

[!include [banner](includes/banner.md)]

Šioje temoje pateikiama tradicinių parduotuvių, kurios „Dynamics 365 Commerce“ nurodomos kaip parduotuvės, nustatymo proceso apžvalga. Jame pateikiama informacija apie užduotis, kurias turite atlikti prieš ir po parduotuvės nustatymo.

„Commerce“ palaiko kelis kanalus, pvz., internetines parduotuves, skambučių centrus ir tradicines parduotuves. Tradicinė parduotuvė vadinama parduotuve. Kiekvienoje parduotuvėje gali būti naudojami savi mokėjimo būdai, kainų grupės, elektroninių kasos aparatų (EKA) registrai, pajamų ir išlaidų sąskaitos bei darbuotojai. Prieš kurdami parduotuvę, turite nustatyti visus šiuos jos elementus. Kai sukuriate parduotuvę, galite priskirti produktus, kuriuos norite, kad ji platintų. Be to, parduotuvei priskiriami darbuotojai, kasos aparatai ir klientai. Galiausiai, įtraukite naują parduotuvę į organizacijos hierarchiją.

## <a name="setting-up-stores"></a>Parduotuvių nustatymas

Prieš nustatydami parduotuvę programoje „Commerce“, turite atlikti kai kurias būtinąsias užduotis. Tada galite sukurti parduotuvę ir pridėti informacijos.

### <a name="prerequisites"></a>Būtinieji komponentai

Prieš nustatydami parduotuvę, turite atlikti tolesnes užduotis.

1. Sukonfigūruokite savo organizacijos struktūrą ir nustatykite mažmeninės prekybos asortimento, papildymo ir ataskaitų teikimo organizacijos hierarchijas.
2. Nustatykite sandėlį, atitinkantį parduotuvę.
3. Nustatykite parduotuvių, parduotuvių išrašų ir išrašų kvitų numeracijas.
4. Konfigūruokite „Commerce“ parametrus.
5. Nustatykite parduotuvėje naudojamus mokėjimo būdus.
6. Norėdami kredito kortelių operacijas apdoroti POS kasos aparatuose, taip pat galite nustatyti mokėjimo paslaugas.
7. Nustatykite PVM grupes.
8. Nustatykite produktus. Vykdant šią užduotį, taip pat nustatomos produktų hierarchijos, produktų variantai ir produktų asortimentai.
9. Nustatykite produktų kainų grupes.
10. Nustatykite produktų kainodarą. Vykdant šią užduotį, taip pat nustatomi kainos koregavimai, nuolaidos ir nuolaidų laikotarpiai.
11. Nustatykite darbuotojus.

    > [!NOTE]
    > Taip pat darbuotojams turite priskirti reikiamas teises, kad jie galėtų prisijungti ir atlikti užduotis naudodami EKA sistemą.

12. Sukonfigūruokite EKA šablonus norėdami priskirti parduotuvei. Ši užduotis apima daug kitų užduočių, pvz., kasos aparatų nustatymą, autonominių profilių nustatymą ir kvitų formatų bei profilių nustatymą.

Peržiūrėkite visas užduotis, įtrauktas į būtinąsias sąlygas, ir atlikite tik jums taikomas užduotis.

### <a name="set-up-a-store"></a>Parduotuvės nustatymas

Atlikę būtinas užduotis, atlikite toliau pateikiamas užduotis, norėdami nustatyti informaciją apie parduotuvę.

1. Sukurkite parduotuvę.
2. Priskirkite parduotuvei PVM grupę.
3. Parduotuvei priskirkite priimtus mokėjimo būdus.
4. Įtraukite informaciją į parduotuvėse siūlomų produktų aprašus. Pavyzdžiui, galite įtraukti raiškiojo teksto ir vaizdų. Ši produktų informacija rodoma įvairiomis aplinkybėmis, pavyzdžiui, POS kasos aparate ar išspausdintose etiketėse.
5. Mažmeninės prekybos parduotuvę pridėkite į numatytąją organizacijos hierarchiją, kuri priskirta **Mažmeninės prekybos asortimento**, **Mažmeninės prekybos papildymo** ar **Mažmeninės prekybos ataskaitų** tikslu.

### <a name="after-you-set-up-a-store"></a>Nustačius parduotuvę

Įvedę parduotuvės informaciją, atlikite nurodytas užduotis norėdami nusiųsti naujus parduotuvės duomenis į EKA.

1. Sukonfigūruokite parduotuvės POS kasos aparatus.
2. Parduotuvei priskirkite produktų asortimentą.
3. Apdorokite asortimentus norėdami sukurti produktų, kurie įtraukti į asortimentą, sąrašą ir padaryti produktus pasiekiamus parduotuvėje.
4. Siųskite duomenis, pvz., numeracijas, aparatūros profilius ir POS ekrano maketus į EKA registrus.
5. Publikuokite parduotuvę norėdami siųsti parduotuvės duomenis į EKA.
6. Vykdykite užduotis norėdami siųsti parduotuvės duomenis į EKA.

## <a name="organization-hierarchies"></a>Organizacijų hierarchijos

„Commerce“ naudoja organizacijos hierarchijas kanalams struktūrizuoti. Organizacijos hierarchijos nurodo ryšius tarp organizacijų, kurios sudaro jūsų verslą. Kai nustatote parduotuves, galite įtraukti jas į organizacijos hierarchiją. Tada parduotuvės bendrina duomenis, kurie naudojami asortimentams, papildymui ir ataskaitoms.

> [!NOTE]
> Norint naudoti „Commerce“ pardavimo funkcijas, turi būti įgalintas konfigūracijos raktas **Kelios siuntimo vietos**. Šį konfigūracijos raktą galima rasti prie **prekybos konfigūracijos** raktų (**Sistemos administravimas** \> **Sąranka** \> **Licencijos konfigūracija**). Tai būtina dėl įvairių tikrinimų pagal pristatymo adresą, sukonfigūruotų pardavimo užsakymo eilutės lygiu.



[!INCLUDE[footer-include](../includes/footer-banner.md)]