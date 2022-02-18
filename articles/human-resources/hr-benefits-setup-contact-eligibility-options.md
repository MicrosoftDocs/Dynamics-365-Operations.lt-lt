---
title: Asmeninio kontakto tinkamumo parinkčių konfigūravimas
description: Šioje temoje paaiškintas asmeninių kontaktų tinkamumo parinkčių konfigūravimas programoje „Microsoft Dynamics 365 Human Resources“.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad9dc9d12bcc419c3925b0f78566d9f3eb0a1e35
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070355"
---
# <a name="configure-personal-contact-eligibility-options"></a>Asmeninio kontakto tinkamumo parinkčių konfigūravimas


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šioje temoje paaiškinama, kaip sukonfigūruoti asmeninių kontaktų tipus, kuriuos galima panaudoti išmokoms gauti „Microsoft Dynamics 365 Human Resources“. Asmeniniai kontaktai yra asmenys, kurie bus įtraukti į jūsų planus (priklausomieji) arba kurie gaus naudos iš jūsų planų (gavėjai). Priklausomieji įprastai yra sutuoktiniai arba vaikai. Gavėjai gali būti sutuoktiniai, vaikai, patikėtiniai arba tėvai.

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
   | **Amžius** | Maksimalus terminas, per kurį asmeninis kontaktas turi teisę gauti išmokų planą. Šis laukas aktyvus tik tada, kai pasirenkate ryšį. Šis terminas lyginamas su apskaičiuotu asmeninio kontakto terminu. Apskaičiuotas terminas yra: (padengimo data – asmeninio kontakto gimimo data / 365). Šis skaičius visada yra sveikasis skaičius. |

4. Pasirinkite **Įrašyti**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
