---
title: Susipažinkite su datos ir laiko laukais
description: Šioje temoje paaiškinama, ko tikėtis, kai naudojate "Microsoft" laukus Data ir laikas Dynamics 365 Human Resources.
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
ms.openlocfilehash: 06c783c1e4a2961f1445909ea03d557c0985064e
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728594"
---
# <a name="understand-date-and-time-fields"></a>Susipažinkite su datos ir laiko laukais

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Datos ir laiko** laukai yra pagrindinė Microsoft sąvoka Dynamics 365 Human Resources. Svarbu suprasti, kaip dirbti su datos ir laiko duomenimis puslapiuose, puslapiuose **·** ir Dataverse išoriniuose šaltiniuose.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Skirtumo tarp laukų Data bei Data ir laikas duomenų tipų supratimas

**Laukuose Data** ir laikas yra laiko juostos informacija, **·** o datos laukuose nėra. **Datos** laukuose ta pati informacija rodoma bet kurioje vietoje. Kai lauke Data įvedate **·** datą, ta pati data įrašoma į duomenų bazę.

Kai duomenys rodomi lauke Data ir laikas, data ir laikas koreguojami pagal vartotojo laiko juostą, kuri pasirinkta vartotojo pasirinkčių puslapyje **·** **·** **(Bendrosios \> nustatymo vartotojo \>** pasirinktys). Data ir laiko informacija, kurią įvedate lauke, gali nesutiti su informacija, įrašyta į duomenų bazę.

[![ Vartotojo pasirinkčių puslapis.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Puslapių laukų Datos ir laikas supratimas 

**Data ir laikas** duomenys yra rodomi ekrane nėra tokie patys kaip duomenys laikomi duomenų bazėje, jei vartotojo laiko zona nėra nustatyta koordinuotame universaliame laike (UTC). Laukuose **Data ir laikas** duomenys visada saugomi kaip UTC.

[![ Darbuotojo puslapio UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Datos ir laiko laukų duomenų bazėje supratimas 

Kai **duomenų bazėje įrašyta** datos ir laiko vertė, duomenys saugomi kaip UTC. Todėl vartotojai gali matyti bet **kuriuos Datos ir laiko** duomenis, susijusius su laiko juosta, kuri nustatyta jų vartotojo pasirinktyse.
 
Aukščiau pateiktame pavyzdyje pradžios laikas yra laiko taškas, o ne konkreti data. Keisdamas laiko juostą prisijungęs vartotojas iš GMT +12:00 į GMT UTC, tas pats įrašas rodo 04/30/2019 12:00:00, o ne 05/01/2019 12:00:00.

Toliau pateiktame pavyzdyje 000724 darbuotojo darbas tampa aktyvus tuo pačiu metu, nepaisant laiko juostos. Darbuotojas bus aktyvus 2019-04-30 GMT laiko juostoje, kuri yra tokia pati kaip 2019-05-01, GMT +12:00 laiko juosta. Abu nurodo tą patį laiko tašką, o ne konkrečią datą. 

[![ Darbuotojo puslapio GMT.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Datos ir laiko duomenys duomenų valdymo sistemoje, „Excel Dataverse” ir „Power BI” 

Duomenų valdymo sistema (DMF), "Excel" papildinį ir ataskaitas galima valdyti tiesiogiai Dataverse su duomenimis duomenų bazės Power BI lygiu. Kadangi nėra jokio kliento, kuris taiso **Datos ir laiko** vartotojo duomenis laiko zonai, visos **Datos ir laiko** vertės yra UTC, kurios gali vesti į kai kurias neteisingas prielaidas įvedant ar peržiūrint duomenis.
 
Kai **datos ir laiko duomenys pateikiami per DMF, Excel arba duomenų bazę laikoma, kad** jie pateikti Dataverse UTC. Tačiau jei vartotojų, kurie tikisi duomenų, vartotojo laiko zona nustatyta kaip UTC, pateikta datos ir laiko vertė nebus pateikta kaip tikėjotės, todėl vartotojai gali būti **·** painiojami. 
 
Tas pats gali įvykti atvirkštiniu procesu, kai duomenys yra eksportuojami. Duomenys **Data ir laikas** eksportuoti DMF objekte gali skirtis nei tie, kurie rodomi „Dynamics“ kliente. 
 
Naudojant išorės šaltinius, tokius kaip DMF tam, kad peržiūrėtumėte ir suteiktumėte leidimą duomenims, atminkite, kad **Datos ir laiko** vertės yra laikomos pagal nutylėjimą UTC nepriklausomai nuo vartotojo kompiuterio ar esamo vartotojo laiko zonos ar jos nustatymų. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Atvejų, kai tas pats įrašas rodomas skirtingose produkto srityse, pavyzdžiai 

**„Human Resources“ vartotojo laiko zona nustatyta į UTC**

[![ Darbuotojo puslapis nustatytas kaip UTC.](./media/worker-form3.png)](./media/worker-form3.png)

**„Human Resources” vartotojo laiko zona nustatyta į GMT + 12:00** 

[![ Darbuotojo puslapis nustatytas kaip GMT.](./media/worker-form4.png)](./media/worker-form4.png)

**„Excel”, naudojant „OData”**

[![„Excel” naudojant „OData”.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF paruošimas**

[![ DMF paruošimas.](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF eksportavimas**

[![ DMF Eksportavimas](./media/DMFExport.png)](./media/DMFExport.png)

**„Excel”, naudojant „Dataverse”**

[![„Excel” naudojant „Dataverse”.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[Datos ir laiko duomenys](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Vartotojo pageidaujamos laiko zonos](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
