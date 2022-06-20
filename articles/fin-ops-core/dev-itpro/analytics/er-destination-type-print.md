---
title: Spausdintuvo ER paskirties vietos tipas
description: Šiame straipsnyje paaiškinama, kaip konfigūruoti spausdintuvo paskirties vietą kiekvienam aplanko arba failo komponentui elektroninės ataskaitos (ER) formatu.
author: NickSelin
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 826455d0901a45ef26755fd323ee2a2737b5eec0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845576"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Spausdintuvo paskirties vieta

[!include [banner](../includes/banner.md)]

Galite siųsti sugeneruotą dokumentą tiesiogiai į tinklo spausdintuvą, kad jis būtų atspausdintas tiesiogiai.

## <a name="prerequisites"></a>Būtinieji komponentai

Prieš pradėdami, turite įdiegti ir sukonfigūruoti Dokumento maršruto planavimo agentą, o paskui užregistruoti tinklo spausdintuvus. Daugiau informacijos žr. [Dokumento maršruto planavimo agento diegimas siekiant įjungti tinklo spausdinimą](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>Spausdintuvo paskirties vietos įgalinimas

Norėdami, kad **spausdintuvo** Microsoft Dynamics paskirties vieta būtų pasiekiama dabartiniame 365 finansų egzemplioriuje, **eikite į funkcijų valdymo** darbo sritį ir įjunkite šias funkcijas šia tvarka:

1. Konvertuoti siunčiamus elektroninių ataskaitų dokumentus iš „Microsoft Office“ formatų („Excel“ / „Word“) į PDF
2. Dokumento maršruto planavimo agentas kaip siunčiamų dokumentų elektroninių ataskaitų teikimo vieta

[![Spausdintuvo paskirties vietos funkcijos įjungimas srityje Funkcijų valdymas.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Taikymas

#### <a name="pdf-printing"></a>PDF spausdinimas

Naudojant finansų versijas prieš 10.0.18 versiją, spausdintuvo paskirties vietą galima konfigūruoti tik naudojant failo komponentus, **·** **kurie naudojami išvesties formatu (PDF** **susijungimas arba PDF** failo formato elementai) Microsoft Office Excel arba Word formato (**Excel** failo formato elementas). Kai išeiga sugeneruojama PDF formatu, ji siunčiama į spausdintuvą. Kai išvestis sugeneruojama Office **formatu naudojant Excel** failo formato elementą, ji automatiškai konvertuojama į PDF formatą, o tada siunčiama į spausdintuvą.

Tačiau kaip 10.0.18 versiją galite **konfigūruoti** bendrosios rinkmenos formato elemento spausdintuvo **paskirties** vietą. Šis formato elementas dažniausiai naudojamas išeigai generuoti TXT arba XML formatu. Galite konfigūruoti ER formatą, **·** **kuriame** bendrosios rinkmenos formato elementas yra šakninis formato elementas, ir tik įdėtojo elemento pagal jį dvejetainio turinio formato elementas. Tokiu atveju bendrosios rinkmenos formato **elementas išvestų formatu, kurį nurodėte susiejimu,** kurį konfigūruojate dvejetainio **turinio** formato elementui. Pavyzdžiui, šį susiejimą [galite](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format)[konfigūruoti](../../fin-ops/organization-administration/configure-document-management.md), kad užpildytų šį elementą dokumentų valdymo priedo turiniu PDF arba Office (Excel arba Word) formatu. Galite išspausdinti išvestį naudodami sukonfigūruotą spausdintuvo **paskirties** vietą. 

> [!NOTE]
> Kai pasirenkate **\\** **bendrosios** rinkmenos formato elementą spausdintuvo paskirties vietai konfigūruoti, dizaino metu nėra būdo užtikrinti, kad pasirinktas elementas produkcijos išeigą PDF formatu arba išvestį, kurį galima konvertuoti į PDF formatą. Todėl gaunate tokį įspėjimo pranešimą: "Įsitikinkite, kad išvestis, sugeneruota pasirinkto formato komponento, gali būti konvertuojama į PDF. Priešingu atveju atžymėkite parinktį Konvertuoti į PDF. Turite atlikti veiksmus, kad išvengtumėte vykdymo problemų, kai spausdinant vykdyklės metu pateikiama ne PDF ar ne PDF konvertuojama išvestis. Jei tikitės gauti išvestį Office (Excel arba Word) formatu, reikia **pasirinkti pasirinktį Konvertuoti į PDF**.
>
> Versijoje 10.0.26 **ir vėlesnėje versijoje naudodami parinktį Konvertuoti į PDF** turite **pasirinkti sukonfigūruotos spausdintuvo paskirties vietos dokumento maršruto tipo parametrą** PDF **·** **·**.

#### <a name="zpl-printing"></a>ZPL spausdinimas

Versijoje 10.0.26 **·** **\\** **ir vėliau galite konfigūruoti bendrosios rinkmenos formato elemento spausdintuvo paskirties vietą pasirinkdami dokumento maršruto tipo parametro** ZPL.**·** Šiuo atveju, **pasirinkties Konvertuoti į PDF** nepaisoma vykdymo metu, o TXT arba XML išvestis siunčiama tiesiogiai į pasirinktą spausdintuvą naudojant dokumento maršruto agento (DRA) dokumento maršruto agento (DRA [)](install-document-routing-agent.md) sutartį. Šią funkciją naudokite ER formatui, kuris nurodo ZPL II žymės maketą įvairioms etiketėms spausdinti.

[![Dokumento maršruto tipo parametras nustatomas dialogo lange Paskirties parametrai.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Daugiau informacijos apie šią funkciją ieškokite naujo [ER sprendimo, kaip spausdinti ZPL etiketes, kūrimas](er-design-zpl-labels.md).

### <a name="limitations"></a>Apribojimai

Paskirties vieta **Spausdintuvas** galima tik naudojant įdiegtis debesyje.

### <a name="use-the-printer-destination"></a>Paskirties vietos Spausdintuvas naudojimas

1. Parinktyje **Įjungta** nustatykite **Taip**, kad sugeneruotas dokumentas būtų nusiųstas į spausdintuvą.
2. Lauke **Spausdintuvo pavadinimas** pasirinkite reikiamą tinklo spausdintuvą.
3. Parinktyje **Įrašyti spausdinimo archyve?** nustatykite **Taip**, norėdami sugeneruotą išvestį saugoti spausdinimo archyve, kad ją būtų galima spausdinti vėliau. Norėdami vėliau peržiūrėti suarchyvuotą išvestį, eikite į **Organizacijos administravimas** \> **Užklausos ir ataskaitos** \> **Ataskaitų archyvas**.

[![Paskirties vietos Spausdintuvas naudojimas.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> Nebūtina įjungti parinktį **Konvertuoti į PDF**, kai konfigūruojate paskirties vietą **Spausdintuvas**. Spausdinant bus konvertuojama į PDF, net jei parinktis yra išjungta.

Norėdami naudoti konkrečią [puslapio padėtį](electronic-reporting-destinations.md#SelectPdfPageOrientation), kai spausdinate siuntimo dokumentą „Excel” formatu, turite įjungti parinktį **Konvertuoti į PDF**. Kai nustatote parinktį **Konvertuoti į PDF** kaip **Taip**, laukas **Puslapio padėtis** tampa pasiekiamas. Lauke **Puslapio padėtis** galite pasirinkti puslapio padėtį.

## <a name="additional-resources"></a>Papildomi ištekliai

- [Elektroninių ataskaitų (ER) apžvalga](general-electronic-reporting.md)
- [Elektroninių ataskaitų (ER) paskirties vietos](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
