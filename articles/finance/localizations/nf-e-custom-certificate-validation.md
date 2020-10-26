---
title: NF-e pasirinktinio sertifikato patvirtinimas
description: Šioje temoje pateikiama informacija apie NF-e pasirinktinio sertifikato suaktyvinimą ir naudojimą.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 3c88c4adafb78b807842b0b41c69b19cf2b7aa23
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973097"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="8ff83-103">NF-e pasirinktinio sertifikato patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="8ff83-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ff83-104">Įjungus NF-e pasirinktinio sertifikato tikrinimo funkciją, pasirinktinis patvirtinimas leidžia palaikyti ryšį su žiniatinklio tarnybomis.</span><span class="sxs-lookup"><span data-stu-id="8ff83-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="8ff83-105">Šis ryšys reikalingas norint perduoti NF-e ir vykdyti SEFAZ autorizavimą.</span><span class="sxs-lookup"><span data-stu-id="8ff83-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="8ff83-106">Sertifikato V5 ypatybę **Serverio autentifikavimo paskirtis** suteikia Brazilijos šakninio sertifikato institucija.</span><span class="sxs-lookup"><span data-stu-id="8ff83-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="8ff83-107">Esant numatytiesiems parametrams, ši ypatybė yra išjungta ir turi būti įjungta rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="8ff83-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="8ff83-108">Kai kuriais atvejais automatinio sertifikato atnaujinimo funkcija gali išjungti šią ypatybę, kad ji nebūtų suaktyvinta.</span><span class="sxs-lookup"><span data-stu-id="8ff83-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="8ff83-109">Jei taip nutinka, tai turi įtakos TLS ryšiui, kuris tampa nebepatikimas.</span><span class="sxs-lookup"><span data-stu-id="8ff83-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="8ff83-110">Tai taip pat turi įtakos galimybei išduoti NF-e gamybos aplinkoms Minas Žeraiso (MG) ir Paranos (PR) valstijose.</span><span class="sxs-lookup"><span data-stu-id="8ff83-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="8ff83-111">Šis naujinimas leidžia naudoti alternatyvų sprendimą sertifikato patvirtinimui, o tai reiškia galimybę užmegzti saugų ryšį.</span><span class="sxs-lookup"><span data-stu-id="8ff83-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>


