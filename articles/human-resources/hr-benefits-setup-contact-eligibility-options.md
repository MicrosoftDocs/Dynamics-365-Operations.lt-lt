---
title: Asmeninio kontakto tinkamumo parinkčių konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip konfigūruoti asmeninių kontaktų tinkamumo pasirinktis "Microsoft"Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 251a12b0da364744f1d8c84324099708a2f816a1
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749288"
---
# <a name="configure-personal-contact-eligibility-options"></a>Asmeninio kontakto tinkamumo parinkčių konfigūravimas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šiame straipsnyje paaiškinama, kaip konfigūruoti asmeninių kontaktų, kuriuos galima naudoti "Microsoft" išmokose, tipus Dynamics 365 Human Resources. Asmeniniai kontaktai yra asmenys, kurie bus įtraukti į jūsų planus (priklausomieji) arba kurie gaus naudos iš jūsų planų (gavėjai). Priklausomieji įprastai yra sutuoktiniai arba vaikai. Gavėjai gali būti sutuoktiniai, vaikai, patikėtiniai arba tėvai.

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Asmeninių kontaktų tinkamumo parinktys**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Tinkamumo parinktis** | Unikalus tinkamumo parinkties pavadinimas arba kodas, skirtas nustatyti tinkamumo parinktį. |
   | **Aprašas** | Trumpas tinkamumo parinkties aprašas. |
   | **Kontakto tinkamumo kodas** | Sistemos kodas, kuris geriausiai apibūdina asmens tinkamumo parinktį. Galite rinkti iš: <ul><li>Ryšys</li><li>Studentas</li><li>Vyresnis priklausomasis</li><li>Vyresnio amžiaus neįgalus priklausomasis</li></ul> |
   | **Būsena** | Tinkamumo parinkties būsena. Jei tinkamumo parinkties būsena nustatyta kaip neaktyvi, tada negalėsite pasirinkti šio asmeninio kontakto tinkamumo parinkties asmeniniams kontaktams. |
   | **Ryšys** | Nurodo ryšį tarp asmeninio kontakto ir darbuotojo. Šis laukas aktyvus tik tada, kai kontakto tinkamumo kodas nustatytas kaip „Ryšys“. |
   | **Amžius** | Minimalus tinkamo asmeninio kontakto amžius, skirtas išmokų planui. Šis laukas aktyvus tik tada, kai pasirenkate ryšį. Šis terminas lyginamas su apskaičiuotu asmeninio kontakto terminu. Apskaičiuotas terminas yra: (padengimo data – asmeninio kontakto gimimo data / 365). Šis skaičius visada yra sveikasis skaičius. |

4. Pasirinkite **Įrašyti**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
