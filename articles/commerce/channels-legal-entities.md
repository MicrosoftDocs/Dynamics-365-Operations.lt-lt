---
title: Kurti juridinius subjektus
description: Šiame straipsnyje aprašoma, kaip kurti juridinius subjektus Microsoft Dynamics 365 Commerce, kurie turi būti sukurti ir konfigūruoti prieš kuriant kanalus.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 160dd82298705eab9edecb9d30d051382b6b4471
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847711"
---
# <a name="create-legal-entities"></a>Kurti juridinius subjektus

[!include [banner](includes/banner.md)]

Šiame straipsnyje aprašoma, kaip kurti juridinius subjektus Microsoft Dynamics 365 Commerce, kurie turi būti sukurti ir konfigūruoti prieš kuriant kanalus.

Juridinis subjektas yra organizacija, turinti registruotą ar įteisintą teisinę struktūrą. Juridiniai subjektai gali sudaryti teisines sutartis ir privalo paruošti išrašus apie savo veiklą.

Įmonė yra juridinio subjekto tipas. Šiuo metu įmonės yra vienintelė juridinių subjektų rūšis, kurią galima kurti, o kiekvienas juridinis subjektas susiejamas su įmonės ID. Šis susiejimas taikomas todėl, kad kai kuriose duomenų modelių funkcinėse programos srityse naudojamas įmonės ID arba *DataAreaId*. Dėl duomenų saugumo, šiose funkcinėse srityse naudojimas ribojamas įmonės viduje. Vartotojai gali gauti prieigą tik prie tos įmonės duomenų, prie kurios yra prisiregistravę. 

Kurdami kanalą, turite nurodyti, kuris juridinis subjektas kuriam kanalui priklauso.

## <a name="create-a-new-legal-entity"></a>Naujo juridinio subjekto kūrimas

Norėdami sukurti naują juridinė subjektą „Dynamics 365 Commerce“, atlikite toliau pateikiamus veiksmus.

1. Naršymo srityje eikite į **Moduliai \>Būstinės sąranka \>Juridiniai subjektai**.
1. Veiksmų srityje pasirinkite **Nauja**. Dešinėje pradedama rodyti sritis **Naujas juridinis subjektas**.
1. Lauke **Pavadinimas** įveskite reikšmę.
1. Lauke **Įmonė** įveskite reikšmę.
1. Lauke **Šalis / regionas** įveskite arba pasirinkite reikšmę.
1. Pasirinkite **Gerai**. 

   ![Juridinio subjekto kūrimas.](media/legal-entities.png)

1. Skyriuje **Bendri** pateikite toliau išvardytą bendrą informaciją apie juridinį subjektą: 
   1. Įveskite ieškos pavadinimą, jei paieškos pavadinimas reikalingas. Ieškos pavadinimas yra alternatyvus pavadinimas, kuris gali būti naudojamas šiam juridiniam subjektui ieškoti. 
   1. Pasirinkite, ar šis juridinis subjektas yra naudojamas kaip konsoliduota įmonė.
   1. Pasirinkite, ar šis juridinis subjektas yra naudojamas kaip pašalinimo įmonė. 
   1. Pasirinkite subjekto **numatytoji kalba**. 
   1. Pasirinkite subjekto **laiko zona**.
1. Skyriuje **Adresai** pasirinkite **Redaguoti**, kad įvestumėte adreso informaciją, pavyzdžiui, gatvės pavadinimą ir numerį, pašto kodą ir miestą.
1. Dalyje **Kontaktinė informacija** įveskite informaciją apie bendravimo metodus, pvz., elektroninio pašto adresus, URL ir telefono numerius.
1. Dalyje **Privalomosios ataskaitos** įveskite registracijos numerius, kurie naudojami privalomosioms ataskaitoms.
1. Dalyje **Registracijos numeriai** įveskite visą informaciją, kurios reikia juridiniam subjektui.
1. Dalyje **Banko sąskaitos informacija** įveskite juridinio subjekto banko sąskaitas ir banko kodus.
1. Dalyje **Užsienio prekyba ir logistika** įveskite juridinio subjekto siuntimo informaciją.
1. Dalyje **Numeracijos** galite peržiūrėti numeracijas, susijusias su juridiniu subjektu. Tai bus tuščia, kad būtų galima pradėti.
1. Skyriuje **Ataskaitų srities vaizdas** peržiūrėkite arba keiskite logotipą ir ataskaitų srities vaizdą, susijusį su juridiniu subjektu.
1. Dalyje **PVM mokėtojo kodas** įveskite registracijos numerius, naudojamus teikiant ataskaitas mokesčių institucijoms.
1. Dalyje **Mokestis 1099** įveskite juridinio subjekto 1099 informaciją.
1. Mokesčių informacijos **skyriuje** įveskite juridinio subjekto mokesčių informaciją.
1. Pasirinkite **Įrašyti**.

Toliau pateiktame vaizde parodytas išsamus juridinio subjekto pavyzdys.

![Juridinio subjekto bendrasis skyrius.](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>Papildomi ištekliai

[Organizacijų ir organizacijų hierarchijų apžvalga](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Organizacijos hierarchijos planavimas](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Organizacijų hierarchijos](channels-org-hierarchies.md)

[Kanalų apžvalga](channels-overview.md)

[Būtinosios kanalo nustatymo sąlygos](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
