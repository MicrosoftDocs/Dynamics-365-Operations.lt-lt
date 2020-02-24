---
title: Asmeninių kontaktų tinkamumo parinkčių konfigūravimas
description: Asmeninių kontaktų tinkamumo parinkčių konfigūravimas programoje „Microsoft Dynamics 365 Human Resources“. Asmeniniai kontaktai gali būti gavėjai arba priklausomieji.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a50c5e54d224a2f8607284eb105381ffb6ef7ad9
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009961"
---
# <a name="configure-personal-contact-eligibility-options"></a>Asmeninių kontaktų tinkamumo parinkčių konfigūravimas

[!include [banner](includes/preview-feature.md)]

Šiame straipsnyje paaiškinama, kaip konfigūruoti asmeninių kontaktų tipus, siekiant gauti išmokas programoje „Microsoft Dynamics 365 Human Resources“. Asmeniniai kontaktai gali būti gavėjai arba priklausomieji. 

1. Darbo srities **Išmokų valdymas** dalyje **Sąranka** pasirinkite **Asmeninių kontaktų tinkamumo parinktys**.

2. Pasirinkite **Naujas**.

3. Nurodyti šių laukų vertes:

   | Laukas | Aprašymas |
   | --- | --- |
   | **Tinkamumo parinktis** | Unikalus tinkamumo parinkties pavadinimas arba kodas, skirtas nustatyti tinkamumo parinktį. |
   | **Aprašas** | Trumpas tinkamumo parinkties aprašas. |
   | **Kontakto tinkamumo kodas** | Sistemos kodas, kuris geriausiai apibūdina asmens tinkamumo parinktį. Galite rinkti iš: <ul><li>Ryšys</li><li>Studentas</li><li>Vyresnis priklausomasis</li><li>Vyresnio amžiaus neįgalus priklausomasis</li></ul> |
   | **Būsena** | Tinkamumo parinkties būsena. Jei tinkamumo parinkties būsena nustatyta kaip neaktyvi, negalėsite pasirinkti šio asmeninio kontakto tinkamumo parinkties, skirtos asmeniniams kontaktams. |
   | **Ryšys** | Nurodo ryšį tarp asmeninio kontakto ir darbuotojo. Šis laukas aktyvus tik tada, kai kontakto tinkamumo kodas nustatytas kaip „Ryšys“. |
   | **Amžius** | Maksimalus terminas, per kurį asmeninis kontaktas turi teisę gauti išmokų planą. Šis laukas aktyvus tik tada, kai pasirenkate ryšį. Šis terminas lyginamas su apskaičiuotu asmeninio kontakto terminu. Apskaičiuotas terminas yra: (padengimo data – asmeninio kontakto gimimo data / 365). Šis skaičius visada yra sveikasis skaičius. |

4. Pasirinkite **Įrašyti**. 
