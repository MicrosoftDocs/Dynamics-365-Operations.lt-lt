---
title: Mažmeninė parduotuvė nerodoma atsiėmimo parduotuvių sąraše
description: Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai parduotuvės nėra parduotuvių, kuriose galima atsiimti prekes, sąraše.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 9974b3e10bbdcd2e8a8723a3be4b70401bb9e546
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801608"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Mažmeninė parduotuvė nerodoma atsiėmimo parduotuvių sąraše

[!include [banner](../../includes/banner.md)]

Šioje temoje pateikiamos trikčių diagnostikos gairės, kurios gali padėti, kai parduotuvės nėra parduotuvių, kuriose galima atsiimti prekes, sąraše.

## <a name="description"></a>aprašymas

Mažmeninės prekybos parduotuvė, kur galima atsiimti prekes, nerodoma sąraše.

## <a name="resolution"></a>Skiriamoji geba

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>Konfigūruokite „Commerce” būstinė parduotuvės adreso ilgumą ir platumos

Norėdami konfigūruoti, „Commerce” būstinės parduotuvės adreso ilgumą ir platumos, atlikite šiuos veiksmus.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalai \> Parduotuvės \> Visos parduotuvės**.
1. Raskite parduotuvę, kurią norite matyti el. komercijos svetainės atsiėmimo parinktyse. Užsirašykite savo **Valdymo vieneto numeris** vertę.
1. Eikite į **Organizacijos valdymas \> Organizacijos \> Valdymo vienetai**.
1. Ieškokite valdymo vieneto numerio, kurį pažymėjote anksčiau, tada ieškos rezultatuose pasirinkti valdymo vienetą.
1. „FasTab” skirtuke **Adresai** pasirinkite **Daugiau parinkčių**  ir tada pasirinkite **Išplėstiniai**.
1. „FastTab” skirtuke **Bendra**, įsitikinkite, kad laukai **Ilguma** ir **Platuma** yra teisingai nustatyti. Atlikdami šį veiksmą, įsitikinkite, kad vertės teisingai nurodytos kaip teigiami arba neigiami skaičiai.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Įvykdymo grupių konfigūravimas „Commerce” būstinėje

Norėdami konfigūruoti įvykdymo grupes, „Commerce” būstinėje, atlikite šiuos žingsnius.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Kanalai \> Internetinės parduotuvės**.
1. Pasirinkite internetinę parduotuvę, kurią norite sukonfigūruoti.
1. Veiksmų srityje pasirinkite skirtuką **Nustatyti**, tada pasirinkite **Vykdymo grupės priskyrimas**.
1. Puslapyje **Įvykdymo grupės paskyrimas**, pasirinkite interneto parduotuvės įvykdymo grupę.
1. Dalyje **Sąranka** įsitikinkite, kad įvykdymo grupei skirta mažmeninės prekybos parduotuvė tinkamai sukonfigūruota.

## <a name="additional-resources"></a>Papildomi ištekliai 

[Valdymo vieneto kūrimas](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[Interneto kanalo nustatymas](../channel-setup-online.md)
