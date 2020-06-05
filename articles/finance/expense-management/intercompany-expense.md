---
title: Vidinės įmonės išlaidos
description: Darbininkas, kurį yra įdarbinęs vienas organizacijos juridinis subjektas, gali dirbti kitam tos pačios organizacijos juridiniam subjektui. Šioje situacijoje, naudodami vidinės įmonės išlaidų funkciją, darbininko išlaidas galite priskirti tam juridiniam subjektui, kuriam darbas buvo atliekamas.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 07e425707eb20730f10246a27799f4deeef93f97
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/21/2020
ms.locfileid: "3390889"
---
# <a name="intercompany-expenses"></a>Vidinės įmonės išlaidos

[!include [banner](../includes/banner.md)]

Darbininkas, kurį yra įdarbinęs vienas organizacijos juridinis subjektas, gali dirbti kitam tos pačios organizacijos juridiniam subjektui. Šioje situacijoje, naudodami vidinės įmonės išlaidų funkciją, darbininko išlaidas galite priskirti tam juridiniam subjektui, kuriam darbas buvo atliekamas. Juridinis subjektas, kuris įdarbina darbuotoją, vadinamas skolinančiuoju juridiniu subjektu. Juridinis subjektas, kuriam priskiriamos darbininko išlaidos, vadinamas besiskolinančiuoju juridiniu subjektu. 

Kad darbininkas galėtų kurti ir teikti išlaidas už darbą, atliekamą kitam juridiniam subjektui, skolinančiojo juridinio subjekto dalies puslapyje **Išlaidų valdymo parametrai** pasirinkite parinktį **Leisti vidinės įmonės išlaidų eilutes**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Vidinės įmonės išlaidų mokesčių registravimas

[!include [banner](../includes/banner.md)]

Jei savo išlaidų ataskaitoje norite naudoti mokesčių grupes, kurios yra susietos su skolinančiuoju (šaltinio) juridiniu subjektu, o ne su besiskolinančiuoju (paskirties) juridiniu subjektu, turėsite tai sukonfigūruoti Didžiosios knygos PVM sąrankoje. Kai Didžiosios knygos parametro **Vidinės įmonės mokesčių registravimo juridinis subjektas** reikšmė nustatyta kaip **Šaltinis**, o parametro **Taikyti PVM mokesčio apmokestinimo taisykles** reikšmė nustatyta kaip **Ne**, bus naudojamas skolinančiam juridiniam subjektui taikomas mokesčių derinys. Kai tas pats parametras nustatytas kaip **Paskirtis**, bus naudojamas besiskolinančiam juridiniam subjektui taikomas mokesčių derinys. Jei tai yra JAV juridiniai subjektai, kai parametras nustatytas kaip **Šaltinis**, laukas **Gautinas PVM** taip pat turi būti sukonfigūruotas naujajame puslapyje **DK registravimo grupės**. Apskaitos mechanizmas naudos šio lauko informaciją su mokesčiu susijusiam apskaitos įrašui.   
Toks pat veiksmas atliekamas su išlaidų eilutėmis, užregistruotomis su projektu arba be jo.  
