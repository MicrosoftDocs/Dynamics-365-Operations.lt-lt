---
title: Susipažinkite su datos ir laiko laukais
description: Supraskite, ko tikėtis naudojant laukus Data ir laikas programoje „Microsoft Dynamics 365 Human Resources”.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e87781762112955902d8a5807092a842f53f6af
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/06/2021
ms.locfileid: "6356565"
---
# <a name="understand-date-and-time-fields"></a>Susipažinkite su datos ir laiko laukais

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Datos ir laiko** laukai yra pagrindinės „Dynamics 365 Human Resources” sąvokos. Svarbu suprasti, kaip dirbti su **Data ir laiku** duomenimis formose, „Dataverse“ ir išorės šaltiniuose.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Skirtumo tarp laukų Data bei Data ir laikas duomenų tipų supratimas

Laukuose **Data ir laikas** yra laiko juostos informacija, o laukuose **Data** laukuose jos nėra. Laukuose **Data** laukuose rodoma ta pati informacija bet kurioje vietoje. Kai įvedate datą į lauką **Data**, „Human Resources” įrašo tą pačią datą į duomenų bazę.

Kai duomenys rodomi lauke **Data ir laikas**, „Human Resources” koreguoja datą ir laiką pagal vartotojo laiko juostą, nustatytą formoje **Vartotojo parinktys** (**Bendra > Sąranka > Vartotojo parinktys**). Datos ir laiko informacija, kurią įvedate lauke, gali skirtis nuo informacijos, įrašytos duomenų bazėje.

[![Forma „Vartotojo pasirinktys”.](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Datos ir laiko laukų formose supratimas 

**Data ir laikas** duomenys yra rodomi ekrane nėra tokie patys kaip duomenys laikomi duomenų bazėje, jei vartotojo laiko zona nėra nustatyta koordinuotame universaliame laike (UTC). Laukuose **Data ir laikas** duomenys visada saugomi kaip UTC.

[![Darbininko forma UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Datos ir laiko laukų duomenų bazėje supratimas 

Kai „Human Resources“ rašo **Datos ir laiko** vertę į duomenų bazę, jie laiko duomenis UTC. Tai leidžia vartotojams matyti visus lauko **Data ir laikas** duomenis, susijusius su jų vartotojo parinktyse apibrėžta laiko juosta.
 
Aukščiau pateiktame pavyzdyje pradžios laikas yra laiko taškas, o ne konkreti data. Keisdamas laiko juostą prisijungęs vartotojas iš GMT +12:00 į GMT UTC, tas pats įrašas rodo 04/30/2019 12:00:00, o ne 05/01/2019 12:00:00.
  
Toliau pateiktame pavyzdyje darbuotojo 000724 įdarbinimas tampa aktyvus tuo pačiu metu, neatsižvelgiant į laiko juostą. Darbuotojas bus aktyvus 2019-04-30 GMT laiko juostoje, kuri yra tokia pati kaip 2019-05-01, GMT +12:00 laiko juosta. Abu nurodo tą patį laiko tašką, o ne konkrečią datą. 

[![Darbininko forma GMT.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Datos ir laiko duomenys duomenų valdymo sistemoje, „Excel Dataverse” ir „Power BI” 

Duomenų valdymo sistema, „Excel” papildinys, „Dataverse” ir „Power BI” ataskaitos yra sukurti taip, kad galėtų sąveikauti su duomenimis duomenų bazės lygiu. Kadangi nėra jokio kliento, kuris taiso **Datos ir laiko** vartotojo duomenis laiko zonai, visos **Datos ir laiko** vertės yra UTC, kurios gali vesti į kai kurias neteisingas prielaidas įvedant ar peržiūrint duomenis.  
 
**Datos ir laiko** duomenys pateikti per DMF, „Excel“ ar „Dataverse“ yra priimami būti UTC duomenų bazės. Tai gali sukelti tam tikrą painiavą, kai pateikta lauko **Data ir laikas** reikšmė nėra tokia, kokios tikėtasi, nes duomenis peržiūrintis vartotojas nenustatęs vartotojo laiko juostos į UTC. 
 
Tas pats gali įvykti atvirkštiniu procesu, kai duomenys yra eksportuojami. Duomenys **Data ir laikas** eksportuoti DMF objekte gali skirtis nei tie, kurie rodomi „Dynamics“ kliente. 
 
Naudojant išorės šaltinius, tokius kaip DMF tam, kad peržiūrėtumėte ir suteiktumėte leidimą duomenims, atminkite, kad **Datos ir laiko** vertės yra laikomos pagal nutylėjimą UTC nepriklausomai nuo vartotojo kompiuterio ar esamo vartotojo laiko zonos ar jos nustatymų. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Atvejų, kai tas pats įrašas rodomas skirtingose produkto srityse, pavyzdžiai 

**„Human Resources“ vartotojo laiko zona nustatyta į UTC**

[![Darbuotojo forma nustatyta į UTC.](./media/worker-form3.png)](./media/worker-form3.png)

**„Human Resources” vartotojo laiko zona nustatyta į GMT + 12:00** 

[![Darbuotojo forma nustatyta į GMT.](./media/worker-form4.png)](./media/worker-form4.png)

**„Excel”, naudojant „OData”**

[![„Excel” naudojant „OData”.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF paruošimas**

[![DMF paruošimas.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF eksportavimas**

[![DMF Eksportavimas](./media/DMFexport.png)](./media/DMFexport.png)

**„Excel”, naudojant „Dataverse”**

[![„Excel” naudojant „Dataverse”.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[Datos ir laiko duomenys](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Vartotojo pageidaujamos laiko zonos](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]