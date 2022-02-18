---
title: Susipažinkite su datos ir laiko laukais
description: Šioje temoje paaiškinama, ko tikėtis naudojant „Microsoft“ datos ir laiko laukus Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
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
ms.openlocfilehash: 7c81155f0c5150af44982f224c8eca2026a78ee7
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8060894"
---
# <a name="understand-date-and-time-fields"></a>Susipažinkite su datos ir laiko laukais

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



**Data ir laikas** laukai yra pagrindinė Microsoft sąvoka Dynamics 365 Human Resources. Svarbu, kad suprastumėte, kaip dirbti **Data ir laikas** duomenys puslapiuose, in Dataverse, ir išoriniuose šaltiniuose.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Skirtumo tarp laukų Data bei Data ir laikas duomenų tipų supratimas

**Data ir laikas** laukuose yra laiko juostos informacija, tuo tarpu **Data** laukai ne. **Data** laukuose rodoma ta pati informacija bet kurioje vietoje. Kai įvesite datą į a **Data** lauke ta pati data įrašoma į duomenų bazę.

Kai duomenys rodomi a **Data ir laikas** lauke, data ir laikas koreguojami pagal vartotojo laiko juostą, kuri pasirinkta **Vartotojo parinktys** puslapis (**Dažnas \> Sąranka \> Vartotojo parinktys**). Datos ir laiko informacija, kurią įvedėte lauke, gali nesutapti su informacija, kuri įrašyta į duomenų bazę.

[![Vartotojo parinkčių puslapis.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Puslapių datos ir laiko laukų supratimas 

**Data ir laikas** duomenys yra rodomi ekrane nėra tokie patys kaip duomenys laikomi duomenų bazėje, jei vartotojo laiko zona nėra nustatyta koordinuotame universaliame laike (UTC). Laukuose **Data ir laikas** duomenys visada saugomi kaip UTC.

[![Darbuotojo puslapis UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Datos ir laiko laukų duomenų bazėje supratimas 

Kada **Data ir laikas** reikšmė įrašoma į duomenų bazę, duomenys saugomi UTC formatu. Todėl vartotojai gali matyti bet kurį **Data ir laikas** duomenis, susijusius su laiko juosta, kuri apibrėžta jų vartotojo pasirinktyse.
 
Aukščiau pateiktame pavyzdyje pradžios laikas yra laiko taškas, o ne konkreti data. Keisdamas laiko juostą prisijungęs vartotojas iš GMT +12:00 į GMT UTC, tas pats įrašas rodo 04/30/2019 12:00:00, o ne 05/01/2019 12:00:00.

Toliau pateiktame pavyzdyje darbuotojo 000724 įdarbinimas tampa aktyvus tuo pačiu metu, nepaisant laiko juostos. Darbuotojas bus aktyvus 2019-04-30 GMT laiko juostoje, kuri yra tokia pati kaip 2019-05-01, GMT +12:00 laiko juosta. Abu nurodo tą patį laiko tašką, o ne konkrečią datą. 

[![Darbuotojo puslapis GMT.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Datos ir laiko duomenys duomenų valdymo sistemoje, „Excel Dataverse” ir „Power BI” 

Duomenų valdymo sistema (DMF), „Excel“ priedas,Dataverse, ir Power BI Visos ataskaitos yra skirtos sąveikai su duomenimis tiesiogiai duomenų bazės lygiu. Kadangi nėra jokio kliento, kuris taiso **Datos ir laiko** vartotojo duomenis laiko zonai, visos **Datos ir laiko** vertės yra UTC, kurios gali vesti į kai kurias neteisingas prielaidas įvedant ar peržiūrint duomenis.
 
Kada **Data ir laikas** duomenys pateikiami per DMF, Excel arba Dataverse, duomenų bazė daro prielaidą, kad ji yra UTC. Tačiau jei duomenis peržiūrinčių naudotojų laiko juosta nenustatyta į UTC, pateikiama **Data ir laikas** reikšmė nebus rodoma taip, kaip tikėtasi, ir vartotojai gali susipainioti. 
 
Tas pats gali įvykti atvirkštiniu procesu, kai duomenys yra eksportuojami. Duomenys **Data ir laikas** eksportuoti DMF objekte gali skirtis nei tie, kurie rodomi „Dynamics“ kliente. 
 
Naudojant išorės šaltinius, tokius kaip DMF tam, kad peržiūrėtumėte ir suteiktumėte leidimą duomenims, atminkite, kad **Datos ir laiko** vertės yra laikomos pagal nutylėjimą UTC nepriklausomai nuo vartotojo kompiuterio ar esamo vartotojo laiko zonos ar jos nustatymų. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Atvejų, kai tas pats įrašas rodomas skirtingose produkto srityse, pavyzdžiai 

**„Human Resources“ vartotojo laiko zona nustatyta į UTC**

[![Darbuotojo puslapis nustatytas į UTC.](./media/worker-form3.png)](./media/worker-form3.png)

**„Human Resources” vartotojo laiko zona nustatyta į GMT + 12:00** 

[![Darbuotojo puslapis nustatytas į GMT.](./media/worker-form4.png)](./media/worker-form4.png)

**„Excel”, naudojant „OData”**

[![„Excel” naudojant „OData”.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF paruošimas**

[![DMF paruošimas.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF eksportavimas**

[![DMF Eksportavimas](./media/DMFExport.png)](./media/DMFExport.png)

**„Excel”, naudojant „Dataverse”**

[![„Excel” naudojant „Dataverse”.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[Datos ir laiko duomenys](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Vartotojo pageidaujamos laiko zonos](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
