---
title: "Apibrėžti konkretaus kanalo nuolaidas"
description: "Pardavėjai dažnai nustato skirtingas nuolaidas skirtinguose kanaluose. Šioje temoje apžvelgtos sąvokas, kurias turite žinoti, norėdami sukurti konkretaus kanalo nuolaidą."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailAffiliationPriceGroup, RetailCatalogPriceGroup, RetailChannelPriceGroup, RetailDiscountPriceGroup, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailStoreItemPriceList, RetailStoreTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16401
ms.assetid: d807fd51-86aa-47a0-8e00-6c5ddd21ff6b
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: b2f59db59ea49925c3bb5e1d75beee95191220d0
ms.lasthandoff: 03/31/2017


---

# <a name="define-channel-specific-discounts"></a>Apibrėžti konkretaus kanalo nuolaidas

Pardavėjai dažnai nustato skirtingas nuolaidas skirtinguose kanaluose. Šioje temoje apžvelgtos sąvokas, kurias turite žinoti, norėdami sukurti konkretaus kanalo nuolaidą. 

<a name="channel-specific-discounts"></a>Konkretaus kanalo nuolaidos
--------------------------

Pardavėjai dažnai siūlo įvairių nuolaidų skirtingais kanalais. Tai gali padaryti vietos rinkos sąlygas arba susidoroti su konkuruojančių pardavėjų.

Mažmeninės prekybos ir komercijos Microsoft Dynamics 365 operacijų naudoja kainų grupes apibrėžti kanalo būdingų nuolaidas. Kainų grupės gali būti priskirtos vienam ar keliems toliau nurodytiems objektams: kanalams, katalogams, priskyrimams ir lojalumo programoms. Šiame straipsnyje aptariami kanalai, tačiau tos pačios koncepcijos taikomos katalogų nuolaidoms, priskyrimų nuolaidoms ir lojalumo nuolaidoms.

## <a name="price-groups"></a>Kainų grupės
\[antraštės id = "priedas\_256084" suderinti = "alignnone" Plotis = "640"\][![kaina grupėms](./media/price-groups-1024x608.png)](./media/price-groups.png) kaina grupės nuorodos mažmeninės prekybos\[/antraštė\]

Aukščiau diagrama parodo santykį tarp subjektų, kurie gali būti operacijos (kanalo, katalogas, priklausomybė, klientų, lojalumo kortelė) ir įvairios nuolaidos, kuris gali būti konfigūruojamas. Visų operacijų atsirasti kanalą, kad kanalas yra garantuojamas dalyvauti operacijos. Likę objektai yra neprivalomi. Kiekviename bendrųjų duomenų puslapyje yra saitas į susijusių kainų grupių puslapį, kuriame galite peržiūrėti kainų grupes ir pagal poreikį jų pridėti. Kaina grupė naudojama sieti keturių skirtingų subjektų nuolaidos, kainų koregavimų ir prekybos sutartis. Mes rekomenduojame, kad galite planuoti strategiją, kaip jums vardas savo kainų grupės išlaikyti juos organizuoja. Viena galimybė būtų atskirti skirtingų tipų naudoti raidę ar skaičių priešdėlis ar priesaga. Pvz., 1-xxxxx kanalo kaina grupėms ir 2-xxxxx katalogo kaina grupėms. Yra keturi užklausų puslapiai, kuriuose dėmesys skiriamas kiekvienam mažmeninės prekybos objektui, su kuriuo gali būti susietos nuolaidos.

-   **Mažmeninės prekybos kanalo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų kanalų ir nuolaidų sąrašas.
-   **Katalogo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų katalogų ir nuolaidų sąrašas.
-   **Lojalumo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų lojalumo programų ir nuolaidų sąrašas.
-   **Priskyrimo kainų grupės** – šiame puslapyje rodomas kiekvienos kainų grupės kartu susietų priskyrimų ir nuolaidų sąrašas.

## <a name="example-channel-discount-set-up"></a>Kanalo nuolaidos sąrankos pavyzdys
Toliau pateiktame pavyzdyje iliustruojamos užduotys, atliekamos nustatant kanalo nuolaidą.

1.  Šiame pavyzdyje turite kanalą pavadinimu **Hiustonas** ir ketinate sukurti naują nuolaidą pavadinimu **Atgal į mokyklą.**
2.  Kadangi kainodaros ir nuolaidų strategija apima kanalo nuolaidų galimybę, kurdami kanalą visada sukuriate konkretaus kanalo kainų grupę.
3.  Turite kainų grupę **Hiustono KG**, ir ji priskirta **Hiustono** kanalui.
4.  Sukūrę naująją nuolaidą **Atgal į mokyklą**, **Nuolaidos** puslapio viršuje turite spustelėti **Kainų grupės**. Atsidarys **Nuolaidos kainų grupių** puslapis. Toliau spustelėkite **Naujas** ir pasirinkite kainų grupę **Hiustono KG**.
5.  Dabar galite įgalinti nuolaidą ir ją perduoti į kanalą.

 

<a name="see-also"></a>Taip pat žiūrėkite
--------

[Price adjustments and discounts](price-adjustments-discounts.md)


