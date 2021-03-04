---
title: Archyvo ER paskirties vietos tipas
description: Šioje temoje pateikiama informacija apie tai, kaip sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti, kiekvieno APLANKO ar FAILO komponento archyvo paskirties vietą.
author: NickSelin
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 3dee7ec614ec1372feaa1150f5e4ebb14c32f60e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679683"
---
# <a name="archive-er-destination-type"></a>Archyvo ER paskirties vietos tipas

[!include [banner](../includes/banner.md)]

Galite sukonfigūruoti elektroninių ataskaitų (ER) formato, kuris sukonfigūruotas siunčiamiems dokumentams generuoti, kiekvieno **aplanko** arba **failo** komponento archyvo paskirties vietą. Remiantis paskirties vietos nustatymu, sugeneruotas dokumentas saugomas kaip ER užduočių sąrašo įrašo priedas. Rezultatus galite peržiūrėti pasirinkdami **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Elektroninių ataskaitų užduotys**.

Šią parinktį galite naudoti, norėdami siųsti sugeneruotą dokumentą į „Microsoft SharePoint“ aplanką arba „Microsoft Azure“ saugyklą. Nustatykite parinktį **Įgalinta** į **Taip**, norėdami išvestį siųsti į paskirties vietą, kuri nustatoma pagal pasirinkto dokumento tipą. Pasirinkti galima tik tų tipų dokumentus, kurių grupė nustatyta kaip **Failas**. Dokumentų [tipus](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) galite nustatyti pasirinkdami **Organizacijos administravimas** \> **Dokumentų valdymas** \> **Dokumentų tipai**. ER paskirties vietų konfigūracija yra tokia pati, kaip dokumentų valdymo sistemos konfigūracija.

[![Puslapis Dokumentų tipai](./media/ER_Destinations-SharePointDocuType.png)](./media/ER_Destinations-SharePointDocuType.png)

Vieta nurodo, kur failas įrašomas. Įgalinus paskirties vietą **Archyvas**, rezultatus galima įrašyti užduočių archyve. Rezultatus galite peržiūrėti pasirinkdami **Organizacijos administravimas** \> **Elektroninės ataskaitos** \> **Suarchyvuotos elektroninių ataskaitų užduotys**.

> [!NOTE]
> Pasirinkite užduočių archyvo dokumento tipą, perėję į **Organizacijos administravimas** \> **Darbo sritys** \> **Elektroninės ataskaitos** \> **Elektroninių ataskaitų parametrai**. Daugiau informacijos žr. [Elektroninių ataskaitų (ER) sistemos konfigūravimas](electronic-reporting-er-configure-parameters.md#prerequisites-for-er-setup).

## <a name="sharepoint"></a>„SharePoint“

Failą galite įrašyti į nustatytą „SharePoint“ aplanką. Norėdami nustatyti numatytąjį „SharePoint“ serverį, eikite į **Organizacijos administravimas** \> **Dokumentų valdymas** \> **Dokumentų valdymo parametrai**. Skirtuke **„SharePoint“** sukonfigūruokite „SharePoint“ aplanką. Tada galite jį pasirinkti kaip aplanką, kuriame bus įrašyta ER išvestis. **„SharePoint“** vietą reikia pasirinkti šiame dokumento tipe.

[![„SharePoint“ aplanko pasirinkimas](./media/ER_Destinations-SharePointDocuTypeLocation.png)](./media/ER_Destinations-SharePointDocuTypeLocation.png)

## <a name="azure-storage"></a>„Azure“ saugykla

Kai nustatyta dokumento tipo vieta yra **„Azure“ saugykla**, galite įrašyti failą į „Azure“ saugyklą.

> [!NOTE] 
> ER sistema failus nuolat saugo „Azure“ didelių dvejetainių objektų saugykloje – skirtingai nuo duomenų valdymo sistemos, kuri taiko septynių dienų saugojimo strategiją dokumentams, kuriuos reikia apdoroti. Norėdami gauti daugiau informacijos, žr. [Pranešimų būsenos gavimo API](../data-entities/recurring-integrations.md#api-for-getting-message-status)ir [būsenos tikrinimo API ](../data-entities/data-management-api.md#status-check-api). Su ER susiję failai bus saugomi „Azure“ didelių dvejetainių objektų saugykloje kaip programos lentelės įrašų priedai, kiek reikės. Vienas failas bus panaikintas iš „Azure“ didelių dvejetainių objektų saugyklos kartu su programos lentelės įrašu, prie kurio pridėtas šis failas.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)
- [Dokumentų valdymo konfigūravimas](../../fin-ops/organization-administration/configure-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]