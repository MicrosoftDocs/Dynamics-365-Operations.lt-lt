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
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240584"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="3c44a-103">NF-e pasirinktinio sertifikato patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="3c44a-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c44a-104">Įjungus NF-e pasirinktinio sertifikato tikrinimo funkciją, pasirinktinis patvirtinimas leidžia palaikyti ryšį su žiniatinklio tarnybomis.</span><span class="sxs-lookup"><span data-stu-id="3c44a-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="3c44a-105">Šis ryšys reikalingas norint perduoti NF-e ir vykdyti SEFAZ autorizavimą.</span><span class="sxs-lookup"><span data-stu-id="3c44a-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="3c44a-106">Sertifikato V5 ypatybę **Serverio autentifikavimo paskirtis** suteikia Brazilijos šakninio sertifikato institucija.</span><span class="sxs-lookup"><span data-stu-id="3c44a-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="3c44a-107">Esant numatytiesiems parametrams, ši ypatybė yra išjungta ir turi būti įjungta rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="3c44a-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="3c44a-108">Kai kuriais atvejais automatinio sertifikato atnaujinimo funkcija gali išjungti šią ypatybę, kad ji nebūtų suaktyvinta.</span><span class="sxs-lookup"><span data-stu-id="3c44a-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="3c44a-109">Jei taip nutinka, tai turi įtakos TLS ryšiui, kuris tampa nebepatikimas.</span><span class="sxs-lookup"><span data-stu-id="3c44a-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="3c44a-110">Tai taip pat turi įtakos galimybei išduoti NF-e gamybos aplinkoms Minas Žeraiso (MG) ir Paranos (PR) valstijose.</span><span class="sxs-lookup"><span data-stu-id="3c44a-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="3c44a-111">Šis naujinimas leidžia naudoti alternatyvų sprendimą sertifikato patvirtinimui, o tai reiškia galimybę užmegzti saugų ryšį.</span><span class="sxs-lookup"><span data-stu-id="3c44a-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]