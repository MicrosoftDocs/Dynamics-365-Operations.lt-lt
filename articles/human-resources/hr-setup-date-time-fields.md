---
title: Susipažinkite su datos ir laiko laukais
description: Supraskite, ko tikėtis naudojant laukus Data ir laikas programoje „Microsoft Dynamics 365 Human Resources”. Išsiaiškinkite, ko galima tikėtis sąveikaujant su laukų Data ir laikas duomenimis formoje „Human Resources”, išoriniame šaltinyje arba „Common Data Service”.
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 027e46d53fd9704f5483e90409be53c1510e8cd4
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529857"
---
# <a name="understand-date-and-time-fields"></a>Susipažinkite su datos ir laiko laukais

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Datos ir laiko** laukai yra pagrindinės „Dynamics 365 Human Resources” sąvokos. Svarbu suprasti, kaip dirbti su lauko **Data ir laikas** duomenimis „Dynamics 365 Human Resources” formose, „Common Data Service” ir išoriniuose šaltiniuose.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Skirtumo tarp laukų Data bei Data ir laikas duomenų tipų supratimas

Laukuose **Data ir laikas** yra laiko juostos informacija, o laukuose **Data** laukuose jos nėra. Laukuose **Data** laukuose rodoma ta pati informacija bet kurioje vietoje. Kai įvedate datą į lauką **Data**, „Human Resources” įrašo tą pačią datą į duomenų bazę.

Kai duomenys rodomi lauke **Data ir laikas**, „Human Resources” koreguoja datą ir laiką pagal vartotojo laiko juostą, nustatytą formoje **Vartotojo parinktys** (**Bendra > Sąranka > Vartotojo parinktys**). Datos ir laiko informacija, kurią įvedate lauke, gali skirtis nuo informacijos, įrašytos duomenų bazėje.

[![Forma „Vartotojo pasirinktys”](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Datos ir laiko laukų formose supratimas 

Įvedant duomenis lauke **Data ir laikas**, ekrane rodomi duomenys nėra tokie patys kaip duomenų bazėje saugomi duomenys, jei vartotojo laiko juosta nėra nustatyta kaip universalusis laikas (UTC). Laukuose **Data ir laikas** duomenys visada saugomi kaip UTC.

[![Darbininko forma](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Datos ir laiko laukų duomenų bazėje supratimas 

Kai „Human Resources” įrašo lauko **Data ir laikas** reikšmę į duomenų bazę, jis išsaugo duomenis UTC. Tai leidžia vartotojams matyti visus lauko **Data ir laikas** duomenis, susijusius su jų vartotojo parinktyse apibrėžta laiko juosta.
 
Aukščiau pateiktame pavyzdyje pradžios laikas yra laiko taškas, o ne konkreti data. Keičiant prisijungusio vartotojo laiko juostą iš GMT +12:00 į GMT UTC, toks pats ką tik sukurtas įrašas rodo 2019-04-30 12:00:00 vietoj 2019-05-01 12:00:00.
  
Toliau pateiktame pavyzdyje darbuotojo 000724 įdarbinimas tampa aktyvus tuo pačiu metu, neatsižvelgiant į laiko juostą. Darbuotojas bus aktyvus 2019-04-30 GMT laiko juostoje, kuri yra tokia pati kaip 2019-05-01, GMT +12:00 laiko juosta. Abu nurodo tą patį laiko tašką, o ne konkrečią datą. 

[![Darbininko forma](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>Datos ir laiko duomenys duomenų valdymo sistemoje, „Excel Common Data Service” ir „Power BI” 

Duomenų valdymo sistema, „Excel” papildinys, „Common Data Service” ir „Power BI” ataskaitos yra sukurti taip, kad galėtų sąveikauti su duomenimis duomenų bazės lygiu. Kadangi nėra kliento, kad būtų galima koreguoti lauko **Data ir laikas** duomenis pagal vartotojo laiko juostą, visos lauko **Data ir laikas** reikšmės yra UTC, o tai gali sukelti tam tikrų klaidingų prielaidų įvedant arba peržiūrint duomenis.  
 
Duomenų bazė lauko **Data ir laikas** duomenis, pateikiamus per DMF, „Excel” ar „Common Data Service”, laiko UTC. Tai gali sukelti tam tikrą painiavą, kai pateikta lauko **Data ir laikas** reikšmė nėra tokia, kokios tikėtasi, nes duomenis peržiūrintis vartotojas nenustatęs vartotojo laiko juostos į UTC. 
 
Tas pats gali įvykti atvirkštiniu procesu, kai duomenys yra eksportuojami. Lauko **Data ir laikas** duomenys eksportuotame DMF objekte gali skirtis nuo to, kas rodoma „Dynamics” kliente. 
 
Kai naudojate išorinius šaltinius, pvz., DMF, norėdami peržiūrėti arba autorizuoti duomenis, svarbu nepamiršti, kad lauko **Data ir laikas** reikšmės pagal numatytuosius parametrus laikomos UTC, neatsižvelgiant į vartotojo kompiuterio laiko juostą ar dabartinius vartotojo laiko juostos parametrus. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Atvejų, kai tas pats įrašas rodomas skirtingose produkto srityse, pavyzdžiai 

**„Human Resources“ vartotojo laiko zona nustatyta į UTC**

[![Darbininko forma](./media/worker-form3.png)](./media/worker-form3.png)

**„Human Resources” vartotojo laiko zona nustatyta į GMT + 12:00** 

[![Darbininko forma](./media/worker-form4.png)](./media/worker-form4.png)

**„Excel”, naudojant „OData”**

[![„Excel”, naudojant „OData”](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF paruošimas**

[![DMF paruošimas](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF eksportavimas**

[![DMF paruošimas](./media/DMFexport.png)](./media/DMFexport.png)

**„Excel”, naudojant „Common Data Service”**

[![Excel, naudojant „Common Data Service”](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[Datos ir laiko duomenys](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Vartotojo pageidaujamos laiko zonos](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]