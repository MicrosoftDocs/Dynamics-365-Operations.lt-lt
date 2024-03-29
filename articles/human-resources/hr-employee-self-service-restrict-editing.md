---
title: Asmeninės informacijos redagavimo apribojimas
description: Apribokite darbuotojus redaguoti kontaktinius „Dynamics 365 Human Resources“ duomenis.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c82114f6600345ee5e2eb9c1c0629ae6c8f0b9a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877691"
---
# <a name="restrict-editing-of-personal-information"></a>Asmeninės informacijos redagavimo apribojimas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

Šiame straipsnyje aprašoma, kaip apriboti darbuotojų kontaktinės informacijos redagavimą Dynamics 365 Human Resources. Galbūt norėsite neleisti darbuotojams redaguoti tam tikros kontaktinės informacijos, pvz., darbo vietos ar el. pašto adreso.

> [!NOTE]
> Kad galėtumėte naudoti šią funkciją, pirmiausia funkcijų valdymo srityje įjunkite funkciją **(Peržiūra) Darbuotojams apriboti prieigą prie adreso ir kontaktinės informacijos pridėjimo ar redagavimo pasirinktais tikslais**. Daugiau informacijos apie peržiūros versijos funkcijų įjungimą žr. skyrių [Funkcijų valdymas](hr-admin-manage-features.md).<br><br>![Įjungti peržiūros funkciją.](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>Pasirinkite informaciją, kurią darbuotojas gali pridėti arba redaguoti

1. Žmogiškuosiuose ištekliuose, pasirinkite **Personalo valdymas**, pasirinkite **Nuorodos** ir tuomet pasirinkite **Žmogiškųjų išteklių parametrai**.

   ![Eikite į personalo parametrus.](./media/hr-employee-self-service-human-resources-parameters.png)

2. Puslapyje **Personalo parametrai** pasirinkite skirtuką **Darbuotojų savitarna**.

   ![Rinkitės Darbuotojo savitarna.](./media/hr-employee-self-service-tab.png)

3. Skirtuke **Darbuotojo savitarna** atžymėkite visą informaciją skyriuje **Adresas ir kontaktinė informacija**, kurios nenorite leisti darbuotojams pridėti ar redaguoti. Šiame pavyzdyje atžymėjome verslo **Įmonės** kontaktinę informaciją.

   ![Įmonės kontaktinės informacijos redagavimo ribojimas.](./media/hr-employee-self-service-restrict-business.png)

4. Pasirinkite **Įrašyti**.

   ![Įrašyti pakeitimus.](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Darbuotojo patirtis

Apriboję darbuotojo teises pridėti ar redaguoti kontaktinius duomenis, jis informaciją matys, bet jos keisti negalės.

Šiame pavyzdyje, kai darbuotojams neleidžiama redaguoti **Įmonės** ontaktinių duomenų, jie šią informaciją matys **Darbuotojų savitarnoje**:

![Įmonės kontaktinių duomenų peržiūra.](./media/hr-employee-self-service-restrict-view.png)

Tačiau jiems pasirinkus įmonės kontaktinius duomenis, sritis **Redaguoti adresą** bus skirta tik skaityti ir jokių laukelių jie keisti negalės.

![Įmonės kontaktiniai duomenys rodomi kaip skirti tik skaityti.](./media/hr-employee-self-service-restrict-read-only.png)

Be to, darbuotojui pasirinkus **Pridėti**, kad jis pridėtų naują adresą, jis negalės pasirinkti **Įmonė** išskleidžiamajame laukelyje **Paskirtis**.

![Darbuotojas negali pridėti įmonės adreso.](./media/hr-employee-self-service-restrict-add.png)

Darbuotojai tą patį pamatys ir pasirinkę **Kontaktiniai duomenys** puslapyje **Asmeninė informacija** ir pridėdami naują adresą. Išskleidžiamajame laukelyje **Paskirtis** rodomi tik informacijos, kurią galima pridėti, tipai. 

![Darbuotojas paskirties išskleidžiamajame laukelyje įmonės pasirinkti negali.](./media/hr-employee-self-service-restrict-purpose.png)

**Kontaktiniai duomenys** nėra rodomi tinklelyje **Paskirtis**.

![Paskirtis rodoma kontaktinių duomenų tinklelyje.](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Taip pat žiūrėkite

[Darbuotojų ir vadovų savitarnos apžvalga](hr-employee-manager-self-service-overview.md)<br>
[„Human Resources“ parametrų konfigūravimas](hr-setup-parameters.md)<br>
[Redaguoti asmeninę informaciją](hr-employee-manager-self-service-edit-personal-information.md)
