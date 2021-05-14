---
title: Konfigūruoti interneto parduotuves
description: Šiame straipsnyje pateikiami saitai į temas, kurios padės centralizuotai konfigūruoti ir valdyti internetinę parduotuvę.
author: kfend
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: 31541
ms.assetid: 7a25f9b4-a0bb-4e8c-95c0-c0799ec0620d
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 1acfe04b7e566ce8b3e3b5570be399621fbea974
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937125"
---
# <a name="configure-online-stores"></a>Konfigūruoti interneto parduotuves

[!include [banner](../includes/banner.md)]

Šiame straipsnyje pateikiami saitai į temas, kurios padės centralizuotai konfigūruoti ir valdyti internetinę parduotuvę.

Toliau pateiktoje lentelėje išvardytos temos padės konfigūruoti prekybos komponentus ir kliento prekybos interneto parduotuvę.

## <a name="configure-an-online-store"></a>Interneto parduotuvės konfigūravimas

| Užduotis                                                | Išsami informacija                                                                                                                                                                                                                                                                                                                                                   | Temos                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Konfigūruoti komponentus.                        | Nustatykite ir tvarkykite prekybos operacijų informaciją. Ši informacija apima parduotuves, mokesčius, produktus, dovanų korteles, akcijas ir nuolaidas.                                                                                                                                                                                                          | [„Retail“ nustatymas ir priežiūra](/dynamicsax-2012/appuser-itpro/setting-up-and-maintaining-retail) („TechNet“ turinys, skirtas „Microsoft Dynamics AX 2012“)                                                                                                                                                                                                                                                                                          |
| Sukonfigūruokite prekybos kanalų naršymo hierarchiją.    | Sukurkite prekybos kanalų naršymo kategorijų hierarchiją, kad nustatytumėte produktų, siūlomų interneto parduotuvėje, kategorijos struktūrą. Nurodykite kategorijų hierarchiją ir priskirkite produktus, produktų atributų grupes ir atributų reikšmes kategorijoms. Tada priskirkite kategorijų hierarchiją interneto parduotuvei.                            | [Mažmeninės prekybos hierarchijos nustatymas](/dynamicsax-2012/appuser-itpro/set-up-a-retail-hierarchy)</br> („TechNet“ turinys, skirtas AX 2012)</br> [Atributų ir atributų tipų nustatymas](/dynamicsax-2012/appuser-itpro/set-up-attributes-and-attribute-types) („TechNet“ turinys, skirtas AX 2012)</br> [Mažmeninės prekybos atributų grupių nustatymas](/dynamicsax-2012/appuser-itpro/set-up-retail-attribute-groups) („TechNet“ turinys, skirtas AX 2012) |
| Įtraukite internetinę parduotuvę į organizacijos hierarchiją. | Kad galėtumėte priskirti sukurtos internetinės parduotuvės produktų asortimentą, vykdyti užsakymus arba generuoti ataskaitas, apimančias informaciją iš tos internetinės parduotuvės, turite priskirti parduotuvę vienai arba daugiau organizacijos hierarchijų. Interneto parduotuvę turite priskirti bent tai organizacijos hierarchijai, kuri apima produktų asortimentą. | [Internetinės parduotuvės nustatymas](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) („TechNet“ turinys, skirtas AX 2012)                                                                                                                                                                                                                                                                                                     |
| Įtraukite pristatymo būdus į internetinę parduotuvę.          | Pasirinkite internetinėje parduotuvėje siūlomus pristatymo būdus.                                                                                                                                                                                                                                                                                                 | [Internetinės parduotuvės nustatymas](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) („TechNet“ turinys, skirtas „Microsoft AX 2012“)                                                                                                                                                                                                                                                                                                     |
| Susiekite atributus ir įtraukite metaduomenis.                   | Pasirinkite parinktis, nurodančias, kaip kiekvienos kategorijos arba kanalo produkto atributai turi veikti internetinėje parduotuvėje svetainėje „Microsoft SharePoint“.                                                                                                                                                                                              | [Internetinės parduotuvės nustatymas](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) („TechNet“ turinys, skirtas AX 2012)                                                                                                                                                                                                                                                                                                     |

## <a name="configure-online-store-products"></a>Internetinės parduotuvės produktų konfigūravimas

| Užduotis                                 | Informacija                                                                                                                                           | Temos                                                                                                                                                                                                                                                                            |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Įtraukite asortimentus į internetinę parduotuvę. | Įtraukite asortimentus, kurie apima produktus, siūlomus internetinėje parduotuvėje.                                                                  | [Internetinės parduotuvės nustatymas](/dynamicsax-2012/appuser-itpro/set-up-an-online-store) („TechNet“ turinys, skirtas AX 2012)                                                                                                                                              |
| Tvarkykite katalogus.                     | Naudokite produktų katalogus, kad nustatytumėte produktus, kuriuos norite siūlyti savo parduotuvėse.                                                              | [Pagrindinės užduotys: mažmeninės prekybos prekių katalogų kūrimas](/dynamicsax-2012/appuser-itpro/key-tasks-create-retail-product-catalogs) („TechNet“ turinys, skirtas „AX 2012“)                                                                                                                           |
| Valdykite kainas.                       | Nustatykite ir naudokite kainų grupes, kurios yra pagrindinis saitas tarp kainų ir nuolaidų bei kanalų, katalogų, priskyrimų ir lojalumo programų. | [Kainų, naudojančių kainų grupes, nustatymas](/dynamicsax-2012/appuser-itpro/setting-up-prices-using-price-groups) („TechNet“ turinys, skirtas AX 2012)</br> [Mokesčių nustatymas](/dynamicsax-2012/appuser-itpro/setting-up-taxes) („TechNet“ turinys, skirtas AX 2012) |
| Valdykite nuolaidas.                    | Nustatykite ir valdykite kainų koregavimus bei keturių tipų nuolaidas.                                                                                  | [Kainų koregavimų ir nuolaidų nustatymas](/dynamicsax-2012/appuser-itpro/setting-up-price-adjustments-and-discounts) („TechNet“ turinys, skirtas AX 2012)                                                                                                                          |
| Valdykite siuntimo išlaidas.             | Nustatykite ir valdykite konkrečias internetinės parduotuvės siuntimo išlaidas.                                                                     | [Internetinių parduotuvių siuntimo išlaidų nustatymas](/dynamicsax-2012/appuser-itpro/set-up-shipping-charges-for-online-stores) („TechNet“ turinys, skirtas AX 2012)                                                                                                                           |
| Valdykite pristatymo būdus.            | Valdykite internetinėje parduotuvėje siūlomus pristatymo būdus.                                                                                        | [Pristatymo būdų nustatymas](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) („TechNet“ turinys, skirtas AX 2012)                                                                                                                                            |

## <a name="set-up-data-exchange-between-commerce-and-the-online-store"></a>Nustatykite prekybos ir interneto parduotuvės duomenų mainus

| Užduotis                                 | Išsami informacija                                                                                                                               | Temos                                                                                                                                                                                                                                                                                  |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nustatykite kanalų integravimo profilius. | Profiliai suteikia galimybę komponentams palaikyti tarpusavio ryšį. Nustatykite profilius prieš konfigūruodami duomenų mainų parametrus. | [Realiojo laiko paslaugos profilio nustatymas](/dynamicsax-2012/appuser-itpro/set-up-a-real-time-service-profile) („TechNet“ turinys, skirtas AX 2012)</br> [Realiojo laiko kanalo profilio nustatymas](/dynamicsax-2012/appuser-itpro/set-up-a-channel-profile) („TechNet“ turinys, skirtas AX 2012) |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]