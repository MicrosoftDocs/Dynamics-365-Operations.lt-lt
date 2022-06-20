---
title: Globalizavimo funkcijų komponentai
description: Šiame straipsnyje pateikiama globalizavimo priemonių komponentų apžvalga.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5525332fe3f1a3ea96da630dc34bab82e4117f99
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891494"
---
# <a name="globalization-feature-components"></a>Globalizavimo funkcijų komponentai

[!include [banner](../includes/banner.md)]

Globalizavimo funkcija yra komponentų rinkinys, nurodantis elektroninių ataskaitų (ER) konfigūracijų duomenų pakeitimo taisykles. Šie komponentai apima elektroninių dokumentų apdorojimo instrukcijas ir jų siuntimą arba gavimą iš išorinių kanalų. Jose taip pat yra sąlygos, apibrėžiančios, kada turi būti vykdoma gaunamų verslo duomenų funkcija.

Visi komponentai priklauso vienas nuo kito. Globalizavimo funkcijos padeda lengvai kurti ir išlaikyti šią priklausomybę bei palaikyti komponentų rinkinio ciklo valdymą ir versijų valdymą.

## <a name="access-electronic-invoicing-feature-components"></a>Prieiga prie elektroninių SF išrašymo priemonės komponentų 

1. Prisijungti prie savo reguliavimo kongigūravimo paslaugų (RCS) paskyros.
2. RCS pasirinkus dalį **Funkcijos**, esančią darbo srityje **Funkcijos**, pasirinkite plytelę **Elektroninių SF priedas**.

    Globalizavimo funkcijos turi keletą komponentų. Elektroninių **SF išrašymo priemonių** puslapyje yra atskiras kiekvieno komponento skirtukas.

    - **Versija** – šis komponentas palaiko funkcijos ciklo valdymą. Galite naudoti ją skirtingų šios priemonės versijų būsenai valdyti.
    - **Konfigūracijos – šis komponentas** leidžia valdyti, peržiūrėti ir redaguoti susijusias ER formato ir formato konvertavimo konfigūracijas, naudojamas apdorojimo pardavimo galimybėse.
    - **Sąrankos** – šis komponentas leidžia globalizacijos paslaugų vartotojams, pavyzdžiui, el. SF paslaugos, tvarkyti susijusios funkcijos versijos sąranką. Todėl jis palaiko lanksčią bendravimo ir atsakymų taisyklių konstrukciją.
    - **Aplinkos – šis komponentas** leidžia globalizavimo tarnybų vartotojams, pvz., el. SF išrašymo paslauga, valdyti aplinką, kurioje naudojamas funkcijos versijos nustatymas. Tai taip pat leidžia vartotojams, kurie turės prieigą prie funkcijos versijos nustatymo, suteikti įgaliojimą.
    - **Organizacijos** – šis komponentas leidžia vartotojams bendrai naudoti šią funkciją su išorinėmis organizacijomis.
    - **Žymės** – šis komponentas leidžia pažymėti priemones, kurias galima naudoti kaip nuorodos globalizavimo planą.
