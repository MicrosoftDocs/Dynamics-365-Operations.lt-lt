---
title: Grynųjų pinigų nominaliųjų verčių konfigūracija, skirta elektroniniam kasos aparatui (EKA)
description: Grynųjų pinigų nominaliosios vertės banknotams ir monetoms gali būti nurodomi operacijų skyriuje, kurį naudos kasininkai, pardavimo darbuotojai ir vadybininkai parduotuvėje per EKA.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.industry: Retail
ms.search.form: RetailStoreTable, RetailStoreCashDeclarationTable
ms.openlocfilehash: c61cde76bf2bfe3ff48b306a8a161fa27f50ac41
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273699"
---
# <a name="configure-cash-denominations-for-the-point-of-sale-pos"></a>Grynųjų pinigų nominaliųjų verčių konfigūracija, skirta elektroniniam kasos aparatui (EKA)

[!include [banner](includes/banner.md)]

Grynųjų pinigų nominaliosios vertės banknotams ir monetoms gali būti nurodomi operacijų skyriuje, kurį naudos kasininkai, pardavimo darbuotojai ir vadybininkai parduotuvėje per EKA. Šias nominaliąsias vertes galima naudoti skaičiuojant grynuosius dienos pabaigos mokėjimų deklaracijoms arba greitai taikant mokėjimą pardavimui.

## <a name="define-denominations"></a>Nominaliųjų verčių apibrėžimas

Nominaliųjų verčių apibrėžimai nustatomi kiekvienai parduotuvei atskirai parduotuvės ypatybių puslapyje pasirinkus parinktį **Nustatyti** \> **Grynųjų pinigų deklaravimas**.

![Parinktis Grynųjų pinigų deklaravimas.](./media/image1-denomination.png)

Norėdami apibrėžti nominaliąsias vertes:

1. Spustelėkite **Naujas**.
1. Nurodykite tipą (monetos arba banknotai).
1. Nurodykite sumą (vertę).

![Puslapis Deklaruotų grynųjų pinigų nominalioji vertė.](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Funkcijų šablono konfigūravimas

Mokant grynaisiais pinigais EKA, vartotojas gali naudoti banknotų nominaliąsias vertes, kad galėtų greitai vesti kliento mokamą sumą. Funkcijų šablone galima konfigūruoti dvi pasirinktis, nurodančias nominaliąsias vertes EKA.

- **Didesnė arba lygi mokėtina suma** – pagal numatytuosius nustatymus EKA bus rodomos tik nominaliosios vertės, kurios yra didesnės už mokamą sumą, kad būtų galima mokėti vienu palietimu. Jeigu mokėtina suma yra $7,50, EKA rodys šias nominaliąsias vertes: $10, $20, $50 ir $100. Palietus bet kurią iš šių sumų bus automatiškai sukuriamas tos sumos pardavimo mokėjimas. $1 ir $5 vertės nėra rodomos, nes šios sumos yra mažesnės nei mokėtina suma.
- **Visos nominaliosios vertės** – pasirinkite šią pasirinktį norėdami visada matyti banknotų nominaliąsias vertes EKA, neatsižvelgiant į mokėtiną sumą. Tai reiškia, kad vartotojas gali naudoti banknotų derinius, kad pasiektų mokėtiną sumą. Pavyzdžiui, jei mokėtina suma yra $25,00, vartotojas gali pasirinkti $20 ir $5, kad užbaigtų pardavimą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
