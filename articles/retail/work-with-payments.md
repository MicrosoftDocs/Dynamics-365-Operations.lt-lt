---
title: "Mokėjimo būdai skambučių centre"
description: "Šioje temoje paaiškinami įvairūs mokėjimo būdai, kuriuos galite naudoti „Dynamics 365 for Retail“ skambučių centre."
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 52b3e2e78a03ac67507ee65a03e0884e5ed44678
ms.openlocfilehash: 321d03d154c224b55ffedbe55a2d5952c2b29d9a
ms.contentlocale: lt-lt
ms.lasthandoff: 11/14/2017

---

# <a name="payment-methods-in-a-call-center"></a>Mokėjimo būdai skambučių centre

[!include[banner](includes/banner.md)]


Šioje temoje paaiškinami įvairūs mokėjimo būdai, kuriuos galite naudoti „Dynamics 365 for Retail“ skambučių centre.

Skambučių centruose taip pat gali būti naudojami kituose kanaluose naudojami mokėjimo būdai, pvz., grynaisiais pinigais, čekiais, kredito kortelėmis ir dovanų kortelėmis. Nustačius skambučių centro mokėjimo būdą, skambučių centro vartotojams jis rodomas kaip viena iš parinkčių dalyje **Payments**, esančioje puslapyje **Pardavimo užsakymas**. Be to, galite nustatyti kuponus norėdami klientams pasiūlyti nuolaidų, kai jie pateikia užsakymą jūsų organizacijos skambučių centrui. Kuponuose gali būti naudojama fiksuota nuolaidos suma arba prekės kainos ar bendro užsakymo procentinė dalis. Pvz., suma pagrįstas kuponas gali pasiūlyti klientams 75,00 nuolaidą, kai klientas išleidžia 750,00 arba daugiau. Galite kurti skirtingų tipų kuponus, nustatyti pirminius / antrinius kuponus ir kopijuoti arba anuliuoti kuponą. Norėdami kurti kuponus, naudokite toliau pateiktos lentelės parinktis.

|                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Atributas**             | Lauke **Apmokėjimo vertės koeficientas** įveskite numatytą kupono apmokėjimo vertę kaip procentą, tada pasirinkite, ar kuponas yra vienkartinio naudojimo, ar bus automatiškai išduotas pakartotinai, ar būdingas klientui.                                                                                                                                                                                                                                                                                                                                                                                       |
| **Galioja**                 | Laukuose **Pradžios data** ir **Pabaigos data** įveskite pirmą ir paskutinę kupono galiojimo dienas.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **Įtraukti taisykles / neįtraukti taisyklių** | Laukuose **Katalogai** ir **Prekės** pasirinkite, ar kurie nors katalogai arba prekės įtraukti į kuponą, ar ne. Jei pasirinkote **Įtraukti** arba **Neįtraukti**, spustelėkite **Nustatyti**, pasirinkite **Įtraukti / neįtraukti katalogų** arba **Įtraukti / neįtraukti produktų** ir įveskite informaciją apie katalogą ar prekę. Jei šiuose laukuose pasirinksite **Nėra**, visi katalogai arba prekės bus įtraukti į kuponą.                                                                                                                                                                                                                          |
| **Įvairios**         | Jei šio kupono negalima naudoti su kitomis nuolaidomis, pažymėkite žymės langelį **Neįtraukiant**. Tada lauke **Pradinis** pasirinkite, kur galima naudoti kuponą Jei tai gamintojo kuponas, pažymėkite žymės langelį **Gamintojo kuponas**.                                                                                                                                                                                                                                                                                                                                                                |
| **Būsimas kuponas**         | Jei šis kuponas kaip pirminis bus susietas su kitais kuponais, pažymėkite žymės langelį **Pirminis kuponas**. Jei šis kuponas turėtų būti susietas su esamu kuponu kaip antrinis kuponas, pasirinkite pirminį kuponą lauke **Pirminio kupono ID**. Pavyzdžiui, galite sukurti artėjančio pavasario katalogo kuponą. Visi kiti pavasario katalogui jūsų sukurti kuponai bus antriniai pavasario katalogo kupono kuponai. Antriniai kuponai gali suteikti 20 procentų nuolaidą naujų klientų užsakymams, 10 procentų nuolaidą naujai išleistai prekei arba 95,00 nuolaidą, jei užsakymas siekia 1 000,00 arba daugiau. |

Jei pateikiate kredito kortelės mokėjimą iš puslapio **Pardavimo užsakymas** ir gaunate pranešimą, kad kortelė nebuvo autorizuota, galite valdyti autorizavimą neautomatiniu būdu. Norėdami patvirtinti, atmesti arba iš naujo pateikti kredito kortelės operaciją, naudokite puslapį **Autorizavimo valdymas**. Galite naudoti skambučių centro parametrų puslapį, norėdami konfigūruoti papildomas mokėjimo apdorojimo parinktis.

-   Čekių sulaikymas finansų darbuotojams suteikia galimybę apdoroti užsakymus, kurie buvo sulaikyti, nes čekis buvo naudojamas kaip mokėjimo būdas ir čekio sulaikymo ribinės reikšmės suma buvo viršyta. Sulaikymą galima panaikinti neautomatiniu būdu arba jis automatiškai baigs galioti sukonfigūruoto laikotarpio pabaigoje.
-   Galite nustatyti ribines reikšmes, kurias viršijus grąžintinas sumokėtas sumas, išduodamas čekiu arba kredito kortele, reikia patvirtinti rankiniu būdu. Grąžintina suma, viršijanti ribinę sumą, įtraukiama į patvirtinimo eilę. Patvirtinus grąžinimą galima išrašyti grąžinamo pardavimo užsakymo SF.





