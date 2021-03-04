---
title: Kurti čekius, kurių būsena Tuščia
description: Šioje temoje paaiškinama, kaip kurti tuščius banko sąskaitos čekius puslapyje „Čekiai“.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: aa1c4c33b977c0173da98aee409389b9242980fb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976462"
---
# <a name="create-checks-that-have-blank-status"></a>Kurti čekius, kurių būsena Tuščia

[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip kurti tuščius čekius. Pavyzdžiui, galite sukurti tuščią čekį, kad įrašytumėte sugadintą čekį, kurio negalima naudoti mokant.

Puslapyje **„Čekiai“** atliekamos čekių priežiūros užduotys. Pavyzdžiui, galite kurti naujus čekių numerius ir naikinti čekius. Taip pat galite kurti čekius, kurių būsena **Tuščia**. Sukūrus tuščius čekius, jų negalima naikinti ar pakartotinai naudoti sistemoje.

> [!NOTE]
> Ši funkcija pasiekiama puslapyje **„Čekiai“** tik įjungus funkciją **„Kurti čekius, kurių būsena Tuščia puslapyje „Kurti čekius“** puslapyje **Funkcijų valdymas**. Jei funkcija neįjungta, čekiai, kurių būsena **Tuščia**, gali būti kuriami tik naudojant dialogo langą **Mokėjimas čekiu** mokėjimų generavimo proceso metu Mokėtinose sumose.

Norėdami atidaryti puslapį **Čekiai**, eikite į skirtuką **Grynųjų pinigų ir banko valdymas \> Banko sąskaitos \> Banko sąskaitos**, tada skirtuko **Valdyti mokėjimus** srityje „Veiksmas“ grupėje **Susijusi informacija** pasirinkite **Čekiai**. Arba eikite į skirtuką **Grynųjų pinigų ir banko valdymas \> Užklausos ir ataskaitos \> Čekiai**.

Tada, norėdami sukurti čekius, kurių būsena **Tuščia**, srityje „Veiksmas“ pasirinkite **Kurti tuščius čekius**. Kol sistemoje kuriami tušti čekiai, susieta banko sąskaita laikinai yra neaktyvi. Taip sumažinama rizika, kad mokėjimai bus sugeneruoti tuo pačiu metu, kai bus sukurti tušti čekiai. Kai apdorojimas baigiamas, susieta banko sąskaita iš naujo aktyvinama.
