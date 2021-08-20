---
title: „Dynamics 365” globalizavimo paslaugos
description: Šioje temoje apžvelgiamos „Microsoft Dynamics 365” globalizavimo paslaugos.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8fa82f741471a8314d01972b3ae3393eea4fd6b47bde647bf4ecdaebfea814a3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775075"
---
# <a name="dynamics-365-globalization-services"></a>„Dynamics 365” globalizavimo paslaugos

[!include [banner](../includes/banner.md)]

Šios globalizavimo paslaugos gali būti sukonfigūruotos taip, kad išplėstų galimybes, egzistuojančias kai kuriose „Microsoft Dynamics 365” internetinės paslaugos:

- **„Regulatory Configuration Service” (RCS)** palaiko įvairių tipų elektroninių dokumentų ir ataskaitų konfigūraciją. RCS teikia patobulintą Elektroninių ataskaitų (ER) dizaino įrankio versiją, kur konfigūracijos saugykla yra atskira tarnyba. Daugiau informacijos rasite [„Regulatory Configuration Service”](rcs-overview.md).
- **Elektroninių sąskaitų faktūrų išrašymas** sujungia konfigūruojamus transformacijų, skaitmeninių parašų ir konfigūruojamų integravimų, skirtų ryšiui su išorinėmis žiniatinklio tarnybomis, įskaitant sertifikavimo ir atsakų tvarkymą, formatus. Daugiau informacijos rasite [Elektroninių sąskaitų faktūrų išrašymas](e-invoicing-service-overview.md).
- **Mokesčių skaičiavimas** suteikia patobulintą lankstumą palaikydama kelias mokesčio ID, mokesčių kodo nustatymą, mokesčių skaičiavimo dizaino įrankį ir vykdymo laiko variklį, naudojamus atitikti painius mokesčių reguliavimus visame pasaulyje. Daugiau informacijos rasite [Mokesčių skaičiavimas](global-tax-calcuation-service-overview.md).

Šios globalizavimo paslaugos teikia visiškai parengtą naudoti integravimą su šiomis „Dynamics 365” internetinėmis paslaugomis.

| Internetinės paslaugos | RCS | Elektroninių SF išrašymas | Mokesčių skaičiavimas (peržiūros versija) |
|----------------|-----|----------------------|---------------------------|
| „Dynamics 365 Finance” | Taip | Taip | Taip | 
| „Dynamics 365 Supply Chain Management” | Taip | Taip | Taip | 
| „Dynamics 365 Project Operations“ | Taip | Taip | Netaikoma | 
| „Dynamics 365 Commerce” | Taip | Netaikoma | Netaikoma | 

> [!NOTE]
> Dėl „Azure” geografinių vietų („geos”) pasiekiamumo RCS skirtumų, šios paslaugos konfigūracija gali sukelti kliento duomenų perkėlimą už taikomai „Dynamics 365” internetinei paslaugai pasirinkto „geo” ribų. Daugiau informacijos rasite, [„Dynamics 365” ir „Power Platform”: Pasiekiamumas, duomenų vieta, kalba ir lokalizavimas](https://aka.ms/rcs/D365Productavailabilityguide).