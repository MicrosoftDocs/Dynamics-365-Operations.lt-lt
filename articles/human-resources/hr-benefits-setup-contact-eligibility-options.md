---
title: Asmeninio kontakto tinkamumo parinkčių konfigūravimas
description: Šiame straipsnyje paaiškinama, kaip konfigūruoti asmeninių kontaktų tinkamumo pasirinktis "Microsoft" Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/22/2022
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
ms.openlocfilehash: e3e393002901f31c035a54bd8036ed20ecdf9e00
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803890"
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
   | **Amžius** |Nurodomas maksimalus išmokų plano tinkamo asmeninio kontakto amžius. Šis laukas aktyvus tik tada, kai pasirenkate ryšį. Šis terminas lyginamas su apskaičiuotu asmeninio kontakto terminu. Apskaičiuotas terminas yra: (padengimo data – asmeninio kontakto gimimo data / 365). Šis skaičius visada yra sveikasis skaičius.
Perkrovos **priklausomo asmeninio** kontakto tinkamumo pasirinktis, šiame lauke pateikiamas minimalus amžius. Pvz., jei pagal 18 metų priklausomybę taikoma pasirinktis "viršiavimas" taikoma 18 **metų**, priklausomieji, pažymėti kaip priklausomieji, kurie yra pažymėti kaip 18 ar senesni, bus kuriems taikoma tinkamumo pasirinktis.  |

4. Pasirinkite **Įrašyti**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
