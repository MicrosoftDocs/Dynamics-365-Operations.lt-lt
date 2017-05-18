---
title: "Skambučių centro katalogo kūrimas"
description: "Šiame straipsnyje apžvelgiamas skambučių centro katalogo kūrimo procesas."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 30a782611a47e662de4f8c30c29e613b44dcc953
ms.contentlocale: lt-lt
ms.lasthandoff: 04/26/2017


---

# <a name="create-a-call-center-catalog"></a>Skambučių centro katalogo kūrimas

[!include[banner](includes/banner.md)]


Šiame straipsnyje apžvelgiamas skambučių centro katalogo kūrimo procesas. 

Skambučių centre naudodami produktų katalogus galite identifikuoti produktus, kuriuos norite siūlyti klientams. Skambučių centruose paprastai naudojami spausdinti katalogai. Spausdintas katalogas maketuojamas ir tvarkomas ne „Microsoft Dynamics 365 for Operations“. Tačiau galite kurti ir saugoti katalogą skaitmenine forma „Dynamics 365 for Operations“ dalyje Mažmeninė prekyba ir prekyba naudodami tas pačias formas, kurias naudojate interneto mažmeninės prekybos katalogams nustatyti. Prieš kuriant katalogą, reikia nustatyti produktų asortimentus ir priskirti juos skambučių centrui. Tada įtraukite produktų į katalogą rinkdamiesi juos iš asortimentų. Įtraukus produktų į katalogą ir baigus katalogą, reikia patikrinti duomenis tikrinant katalogą. Tada reikia pateikti katalogą peržiūrai ir patvirtinimui. Kai katalogas patvirtintas, jis gali būti publikuojamas. Sukūrę skambučių centro katalogą, galite padaryti momentinę katalogo duomenų nuotrauką, kai katalogas publikuojamas. Ši momentinės kopijos funkcija suteikia galimybę pasiekti konkrečią katalogo versiją, net jei vėliau katalogas pakeičiamas ir atnaujinamas. Be to, skambučių centro katalogus galima nustatyti taip, kad juose būtų toliau nurodytos pasirinktinės funkcijos.

-   **Šaltinio kodai** – kodai, naudojami stebint klientų atsaką į konkrečius katalogų laiškus.
-   **Nemokami produktai** – produktai, įtraukti į kliento užsakymą be jokio papildomo mokesčio. Šie produktai automatiškai įtraukiami į užsakymą, kai užsakyme įvedamas katalogo šaltinio kodas.
-   **Scenarijai** – tekstai, kuriuos skambučių centro darbuotojas skaito klientui, kai kuriamas pardavimo užsakymas. Scenarijai gali apimti sveikinimus arba pasiūlymus pirkti.
-   **Papildomo arba kryžminio pardavimo prekės** – prekės, rodomos kaip pasiūlymas, kai į užsakymą įtraukiamas konkretus produktas.

Šias parinktis būtina nustatyti prieš katalogą tvirtinant ir publikuojant.

## <a name="prerequisites"></a>Būtinieji komponentai
Prieš pradėdami turite įvykdyti toliau nurodytas užduotis.

-   Nustatykite produktus ir produktų asortimentus.
-   Nustatykite mažmeninės prekybos produktus.
-   Nustatykite asortimentą.
-   Sukurkite skambučių centrą.
-   Nustatykite skambučių centrą.
-   Įtraukite skambučių centrą į organizacijos hierarchiją.
-   Kurkite arba modifikuokite organizacijos hierarchiją.

## <a name="create-a-catalog"></a>Katalogo kūrimas
Iš pradžių reikia sukurti katalogą, įtraukti į jį produktų, tada peržiūrėti ir atnaujinti produktų atributus.

## <a name="validate-the-catalog"></a>Patikrinkite katalogą
Baigę katalogo nustatymą, turite jį patikrinti. Tikrinimo proceso metu tikrinama, ar duomenys, kurių reikia kanalo atributams ir produktų atributams, yra išsamūs ir tinkami, ir ar katalogą galima publikuoti.

## <a name="submit-the-catalog-for-review-and-approval"></a>Katalogo pateikimas paržiūrėti ir patvirtinti
Patikrinus katalogą galite jį pateikti peržiūrėti ir tvirtinti. Prieš registruojant katalogą reikia jį patvirtinti. Galite konfigūruoti darbo eigą, kad katalogai būtų patvirtinti automatiškai arba rankiniu būdu.

## <a name="optional-add-source-codes-free-products-and-scripts"></a>Pasirinktinai: šaltinio kodų, nemokamų produktų ir scenarijų įtraukimas
Į skambučių centro katalogą galite įtraukti šiuos elementus. Šie elementai yra pasirinktiniai.

-   **Šaltinio kodus** gali naudoti įmonės, kurios teikia spausdintus katalogus, norėdamos sekti kliento reakciją į konkrečius katalogus. Šaltinio kodai dažnai išspausdinami katalogo nugarėlėje ir įvedami į pardavimo užsakymą, kai klientas perka. Norėdami šaltinio kodą įtraukti į katalogą, pirmiausia turite sukurti tikslinę rinką. Tikslinė rinka paprastai yra susieta su turimu arba nuomojamu adresų sąrašu.
-   **Nemokami produktai** yra akcijos prekės, nemokamai įtraukiamos į kliento užsakymą, kai katalogas yra nurodomas.
-   **Scenarijai** gali būti naudojami siekiant padėti darbuotojui bendrauti su klientais katalogo arba katalogo produkto kontekste.

## <a name="publish-the-catalog"></a>Katalogo publikavimas
Publikuodami katalogą skambučių centre užbaigiate produkto informacijos rengimą kataloge. Be to, publikavimas rodo, kad katalogas yra paruoštas visiems papildomiems veiksmams, kuriuos galbūt norėsite atlikti. Pavyzdžiui, galite kurti spausdintą katalogą. Katalogą publikuoti galite neautomatiniu būdu arba naudodami paketinį vykdymą, kai publikuojama pagal grafiką. Prieš publikuojant katalogą jis turi būti patikrintas ir patvirtintas. Norėdami keisti katalogą, kai jis publikuotas, turite atsisakyti katalogo, o tada publikuoti jį dar kartą.




