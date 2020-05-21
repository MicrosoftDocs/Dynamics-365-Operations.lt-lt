---
title: Prognozės modelių kūrimas projektų biudžetams
description: Šioje temoje aprašoma, kaip sukurti likusių biudžetų prognozės modelį.
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321784"
---
# <a name="create-forecast-models-for-project-budgets"></a>Prognozės modelių kūrimas projektų biudžetams 

[!include [banner](../includes/banner.md)]

Šioje temoje aprašoma, kaip sukurti likusių biudžetų prognozės modelį. Projekte, kuriam taikoma biudžeto kontrolė, naudojama dviejų tipų biudžetai: pradinis ir likęs. Kai kuriate projekto biudžetą, turite nurodyti pradinio ir likusio biudžeto prognozės modelius, kurie buvo sukurti puslapyje **Prognozės modeliai**. Projekto biudžetas, pagrįstas nurodytais modeliais, sukuriamas, kai projekto biudžetas užfiksuojamas.

> [!NOTE]
> Prognozės modelyje, kuris naudojamas biudžeto kontrolei, negali būti submodelių ir jo negalima naudoti kaip submodelio.

1. Pasirinkite **Projektų valdymas ir apskaita** > **Sąranka** > **Prognozės**  > **Prognozės modeliai**.
2. Pasirinkite **Naujas**, kad sukurtumėte naują prognozės modelį, tada įveskite modelio ID numerį ir naujo modelio pavadinimą. 
3. Nustatykite parinktį **Sustabdyta** į **Taip**, kad būtų išvengta bet kokių prognozės modelio prognozės eilučių pakeitimų. 
4. Jei prognozės eilutės, su kuriomis susietas modelis, turi generuoti pinigų srauto prognozes DK, nustatykite **Įtraukti į pinigų srautų prognozes** į **Taip**. 
5. Norėdami naudoti projekto datą kaip SF datą, nustatykite **Prognozės SF data** į **Taip**. 
6. Lauke **Biudžeto tipas** pasirinkite vieną iš toliau nurodytų modelių tipų.

   - **Pradinis biudžetas** – naudokite pradinio biudžeto sumas, kurios užfiksuojamos, kai pradinis biudžetas sukuriamas ir patvirtinamas.
   - **Biudžeto likutis** – naudokite likusias biudžeto sumas projekto laikotarpiu. Balansai šiame prognozės modelyje yra sumažinami faktinių operacijų ir padidinami arba sumažinami tikslinant biudžetą.
   - **Perkėlimas** – naudokite projekto perkeliamo biudžeto sumas. Perkėlimas yra pasirinktinis procesas, kuris gali būti vykdomas norint perkelti nepanaudotas biudžeto sumas iš vienų finansinių metų į kitus.

7. Nustatykite tolesnes parinktis kaip reikia.

   - Norėdami naudoti projekto datą kaip SF datą, įjunkite **Prognozės SF data**.
   - Įjunkite **NG prognozė**, kad būtų prognozuojama remiantis nebaigta gamyba (NG), tada pasirinkite NG tipą. 
   - Galite palikti numatytąją **Biudžeto tipas** reikšmę **Nėra** arba įvesti naują tipą. Pakeitus įrašą, biudžeto tipo pakeisti negalima.     
    > [!NOTE]
    > Pakeitus numatytąjį biudžeto tipą, visos kitos parinktys nebus pasiekiamos naujinimuose ir negalėsite pakartotinai naudoti šio prognozės modelio. 
   


 

