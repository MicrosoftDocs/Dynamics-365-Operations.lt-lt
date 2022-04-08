---
title: Globalizavimo funkcijų komponentai
description: Šioje temoje pateikta globalizavimo priemonių komponentų apžvalga.
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
ms.openlocfilehash: 87d7dd231b9ccda7761c91f129659c18039f3299
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371961"
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