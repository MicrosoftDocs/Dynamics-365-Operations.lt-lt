---
title: Vietos ir šalies ryšių tipo įtraukimas
description: Šioje temoje paaiškinta, kaip įtraukti naują vietą ir šalies ryšio tipą.
author: ShivamPandey-msft
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: a69ace892c55948305419a089cb91ac5b1e3c066177f8ce2ca441f1dd01c2af0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728870"
---
# <a name="add-location-and-party-relationship-types"></a>Vietos ir šalies ryšių tipo įtraukimas 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a>Vietų vaidmenų įtraukimas

Norėdami galite įtraukti naujų vietos vaidmenų adresą ir kontaktinę informaciją dviem būdais:

-  Įtraukite jį puslapyje **Adreso ir kontaktinės informacijos paskirtis**. Naujas vaidmuo bus įrašytas į lentelę **LogisticsLocationRole**, kurios tipas = 0, tai rodo, kad vaidmuo nėra sistemos vaidmuo, nurodytas į **LogisticsLocationRoleType** išvardijimo ir jo plėtinius. Vartotojas galės naudotis šiuo vaidmeniu kurdamas adresą arba kontaktinę informaciją.

    ![Adreso ir turinio informacijos paskirtis.](media/Address-Contact.PNG)

-  Įtraukite jį į išvardijimo plėtinį **LogisticsLocationRoleType** ir leiskite jam automatiškai įvesti duomenų bazės sinchronizavimo proceso metu.

    1.  Sukurkite išvardijimo **LogisticsLocationRoleType** plėtinį ir įtraukite naująjį vaidmenį į plėtinį. 
  
        ![„LogisticsLocationRoleType” išvardijimo išplėtimas.](media/Logistics.PNG)

    2. Sukurkite naują naujojo vaidmens išteklių failą ir tada jo ypatybėms priskirkite vertę.
     
     ![Naujas išteklių failas.](media/Resource.PNG)
        
    3.  Sukurkite automatinio duomenų įvedimo klasę ir pateikite apdorojimo programos metodą automatiniam naujojo vaidmens įvedimui. 

        ![Automatinis duomenų įvedimas.](media/Dirdata.PNG)

    4.  Norėdami patikrinti naujojo vietos vaidmens automatinį įvedimą, galite sukurti vykdomą klasę ir iškviesti DirDataPopulation::insertLogisticsLocationRoles() in Main(). Atlikę šį procesą, pamatysite naująjį vaidmenį automatiškai įvestą lentelėje **LogisticsLocationRole**, kurios tipas \>0. Naujasis vaidmuo bus rodomas puslapyje **Adreso ir kontaktinės informacijos paskirtis**.

        ![Naujos vietos įterpimas.](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a>Šalių ryšių tipų įtraukimas 

Yra du būdai, kaip įtraukti naują ryšio tipą:

-   Įtraukite jį puslapyje **Ryšių tipai**. Naujasis ryšys bus įrašytas į **DirRelationshipTypeTable**, kurios sistemos tipas = 0.

    ![Ryšių tipai.](media/Relationship.PNG)

-  Įtraukite jį į išvardijimo plėtinį **DirSystemRelationshipType** ir leiskite jam automatiškai įvesti duomenų bazės sinchronizavimo proceso metu.

    1.  Sukurkite išvardijimo **DirSystemRelationshipType** plėtinį ir įtraukite naująjį ryšio tipą.

    2. Sukurkite šio naujo tipo iniciatorių. Pagrindiniame kode rasite keletą pavyzdžių, vienas iš jų yra **DirRelationshipTypeChildInitialize**. Tai yra šalies ryšio, kurio tipas „Antrinis“, iniciatoriaus klasė. Galite pradėti nuo savo iniciatoriaus, nukopijavę ir įklijavę šį kodą ir tuomet atnaujinę paryškintas sritis.
    
    ![„DirRelationshipChild” inicializatorius.](media/DirRelationship.PNG)

    3.  Norėdami patikrinti naujojo ryšio tipo automatinį įvedimą, galite sukurti vykdomą klasę ir iškviesti DirDataPopulation::insertDirRelationshipTypes() in Main(). Naująjį ryšio tipą turėtumėte pamatyti **DirRelationshipTypeTable**, be to, naujasis ryšio tipas bus pasiekiamas puslapyje **Ryšių tipai**.

        ![Vykdoma klasė.](media/Runnable.PNG)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]