---
title: NF-e pasirinktinio sertifikato patvirtinimas
description: Šioje temoje pateikiama informacija apie NF-e pasirinktinio sertifikato suaktyvinimą ir naudojimą.
author: gionoder
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813973"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="e80e5-103">NF-e pasirinktinio sertifikato patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="e80e5-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e80e5-104">Įjungus NF-e pasirinktinio sertifikato tikrinimo funkciją, pasirinktinis patvirtinimas leidžia palaikyti ryšį su žiniatinklio tarnybomis.</span><span class="sxs-lookup"><span data-stu-id="e80e5-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="e80e5-105">Šis ryšys reikalingas norint perduoti NF-e ir vykdyti SEFAZ autorizavimą.</span><span class="sxs-lookup"><span data-stu-id="e80e5-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="e80e5-106">Sertifikato V5 ypatybę **Serverio autentifikavimo paskirtis** suteikia Brazilijos šakninio sertifikato institucija.</span><span class="sxs-lookup"><span data-stu-id="e80e5-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="e80e5-107">Esant numatytiesiems parametrams, ši ypatybė yra išjungta ir turi būti įjungta rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="e80e5-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="e80e5-108">Kai kuriais atvejais automatinio sertifikato atnaujinimo funkcija gali išjungti šią ypatybę, kad ji nebūtų suaktyvinta.</span><span class="sxs-lookup"><span data-stu-id="e80e5-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="e80e5-109">Jei taip nutinka, tai turi įtakos TLS ryšiui, kuris tampa nebepatikimas.</span><span class="sxs-lookup"><span data-stu-id="e80e5-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="e80e5-110">Tai taip pat turi įtakos galimybei išduoti NF-e gamybos aplinkoms Minas Žeraiso (MG) ir Paranos (PR) valstijose.</span><span class="sxs-lookup"><span data-stu-id="e80e5-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="e80e5-111">Šis naujinimas leidžia naudoti alternatyvų sprendimą sertifikato patvirtinimui, o tai reiškia galimybę užmegzti saugų ryšį.</span><span class="sxs-lookup"><span data-stu-id="e80e5-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]