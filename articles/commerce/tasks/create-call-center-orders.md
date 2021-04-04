---
title: " Skambučių centro užsakymų kūrimas"
description: Ši procedūra padeda ieškoti kliento, kurti naują užsakymą, ieškoti produkto ir surinkti mokėjimą iš kliento.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ecf6fe97287fcfb3c070215b563542878175789c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264289"
---
# <a name="create-call-center-orders"></a> Skambučių centro užsakymų kūrimas

[!include [banner](../includes/banner.md)]

Ši procedūra padeda ieškoti kliento, kurti naują užsakymą, ieškoti produkto ir surinkti mokėjimą iš kliento. Šioje procedūroje naudojama demonstracinių duomenų įmonė USRT ir ji yra skirta pardavimo užsakymo klerkui. Išankstinės sąlygos: vartotojas, vykdantis procedūrą, yra nustatomas kaip skambučių centro vartotojas ir skelbiamas Fabrikam pusės metų katalogas su bent vienu šaltinio kodu jame.

1. Eikite į **Mažmeninė prekyba ir prekyba \> Klientai \> Klientų aptarnavimas**.
2. Lauke **Ieškos tekstas** įveskite kliento ieškos kriterijus.
    * Atlikdami šio pavyzdžio procedūrą įveskite „Karen“ ir pasirinkite **skirtuką**.  
3. Pasirinkite Ieškoti.
    * Kadangi demonstraciniuose duomenyse tik yra tik vienas klientas vardu Karen, šis rezultatas bus automatiškai pažymėtas.  
4. Pasirinkite **Naujas pardavimo užsakymas**.
5. Išplėskite arba sutraukite antraštės sekciją **Pardavimo užsakymas**.
6. Pasirinkite katalogo šaltinio kodą.
    * Jei nėra jokių aktyvių šaltinio kodų, galite praleisti šį veiksmą.  
7. Pasirinkite **Pridėti eilutę**.
8. Lauke **Prekės numeris** įveskite prekės ieškos terminą.
    * Atlikdami šio pavyzdžio procedūrą, įveskite dalinį prekės numerį „8111“ ir paspauskite skirtuką. Pasirodys prekės ieškos langas.  
9. Pasirinkite produktą, kurį norite įtraukti į pardavimo užsakymą.
10. Įveskite pardavimo kiekį.
11. Pasirinkite **Kurti**.
12. Pasirinkite **Baigti**, norėdami užfiksuoti kliento mokėjimą.
13. Pasirinkite **Įtraukti**.
    * Parinktis Įtraukti saitą yra skirtuke Mokėjimai. Išplėskite skirtuką Mokėjimai, jei jis sutrauktas.  
14. Pasirinkite mokėjimo būdą.
    * Atlikdami šią procedūrą, parinkite grynųjų pinigų mokėjimo metodą.  
15. Uždarykite puslapį.
16. Įveskite sumą.
    * Atlikdami šią procedūrą, įveskite sumą, lygią užsakymo balansui, kuris rodomas puslapyje Pardavimo užsakymo suvestinė, kairėje sumos lauko pusėje. Šis veiksmas leis įvykdyti užsakymą kaip visiškai apmokėtą.  
17. Pasirinkite **Gerai**.
18. Pasirinkite **Pateikti**.

## <a name="additional-resources"></a>Papildomi ištekliai

[Tinkinti perlaidų el. paštus pagal pristatymo būdą](../customize-email-delivery-mode.md)

[Pristatymo režimo keitimas EKA](../pos-change-delivery-mode.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]