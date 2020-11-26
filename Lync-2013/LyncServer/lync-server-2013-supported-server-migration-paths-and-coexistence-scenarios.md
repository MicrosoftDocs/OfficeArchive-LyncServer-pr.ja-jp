---
title: 'Lync Server 2013: サポートされるサーバー移行パスと共存のシナリオ'
description: 'Lync Server 2013: サポートされているサーバー移行パスと共存シナリオ。'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server migration paths and coexistence scenarios
ms:assetid: 2a6a730f-7f80-45f9-9540-3edfdaa265fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425764(v=OCS.15)
ms:contentKeyID: 48183686
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 44d0a40ac6cc6570cf79b56dc896277c83909b5d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423632"
---
# <a name="supported-server-migration-paths-and-coexistence-scenarios-in-lync-server-2013"></a><span data-ttu-id="aa7a8-103">Lync Server 2013 でサポートされるサーバー移行パスと共存のシナリオ</span><span class="sxs-lookup"><span data-stu-id="aa7a8-103">Supported server migration paths and coexistence scenarios in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aa7a8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aa7a8-104">

<span> </span></span></span>

<span data-ttu-id="aa7a8-105">_**最終更新日:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="aa7a8-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="aa7a8-106">Lync Server 2013 は、次のいずれかの移行をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-106">Lync Server 2013 supports migration from either of the following:</span></span>

  - <span data-ttu-id="aa7a8-107">Microsoft Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="aa7a8-107">Microsoft Lync Server 2010</span></span>

  - <span data-ttu-id="aa7a8-108">Microsoft Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="aa7a8-108">Microsoft Office Communications Server 2007 R2</span></span>

<span data-ttu-id="aa7a8-109">これらの以前のバージョンの両方を実行している環境からの移行はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-109">Migration from an environment running both of these previous versions is not supported.</span></span> <span data-ttu-id="aa7a8-110">Microsoft Office Communications Server 2007 や Live Communications Server 2005 などの以前のバージョンからの移行はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-110">Migration from earlier versions, such as Microsoft Office Communications Server 2007 or Live Communications Server 2005, is not supported.</span></span> <span data-ttu-id="aa7a8-111">以前の展開にグループチャットが含まれていた場合は、個別に移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-111">If your previous deployment included Group Chat, you must migrate it separately.</span></span>

<div>

## <a name="migration-methods"></a><span data-ttu-id="aa7a8-112">移行方法</span><span class="sxs-lookup"><span data-stu-id="aa7a8-112">Migration Methods</span></span>

<span data-ttu-id="aa7a8-113">すべての Lync Server トポロジとサーバーロールの移行がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-113">Migration of all Lync Server topologies and server roles is supported.</span></span> <span data-ttu-id="aa7a8-114">Standard Edition server から Enterprise Edition server に移行することで、1つのトポロジから別のトポロジに移行することができます。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-114">You can migrate from one topology to a different topology, including from Standard Edition server to Enterprise Edition server.</span></span>

<span data-ttu-id="aa7a8-115">Lync Server 2013 は、次の移行方法のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-115">Lync Server 2013 supports only the following migration method:</span></span>

  - <span></span>  
    <span data-ttu-id="aa7a8-116">**サイドバイサイド移行。**</span><span class="sxs-lookup"><span data-stu-id="aa7a8-116">**Side-by-side migration.**</span></span> <span data-ttu-id="aa7a8-117">サイドバイサイドの移行では、Lync Server 2013 は既存の Microsoft Lync Server 2010 または Office Communications Server 2007 R2 の展開と共に展開され、その後、操作を新しいサーバーに移してユーザーを Lync Server 2013 に移行します。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-117">In side-by-side migration, Lync Server 2013 is deployed alongside an existing Microsoft Lync Server 2010 or Office Communications Server 2007 R2 deployment, and then you transfer operations to the new servers and move users to Lync Server 2013.</span></span> <span data-ttu-id="aa7a8-118">この方法を使うには、移行時にハードウェアやソフトウェアを含めた追加のサーバープラットフォーム、およびシステム名とプール名が新しい構成で異なる必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-118">This method requires additional server platforms, including hardware and software, during migration, and system names and pool names are different in the new configuration.</span></span> <span data-ttu-id="aa7a8-119">以前のバージョンに戻す必要がある場合は、操作を前のサーバーに戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-119">If it becomes necessary to roll back to the previous version, you can shift operations back to the previous servers.</span></span>

<span data-ttu-id="aa7a8-120">Active Directory ドメインサービスフォレスト間の移行はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-120">Migration across Active Directory Domain Services forests is not supported.</span></span>

<span data-ttu-id="aa7a8-121">推奨される移行パスは、段階的なアプローチです。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-121">The recommended migration path is a phased approach.</span></span> <span data-ttu-id="aa7a8-122">以前のリリースから移行する方法について詳しくは、「段階的なコンポーネントの展開」をご覧ください。移行ドキュメントの次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-122">For details about migrating from a previous release, including the appropriate phasing of component deployment, see the following topics in the Migration documentation:</span></span>

  - [<span data-ttu-id="aa7a8-123">Lync Server 2010 から Lync Server 2013 への移行</span><span class="sxs-lookup"><span data-stu-id="aa7a8-123">Migration from Lync Server 2010 to Lync Server 2013</span></span>](migration-from-lync-server-2010-to-lync-server-2013.md)

  - [<span data-ttu-id="aa7a8-124">Office Communications Server 2007 R2 から Lync Server 2013 への移行</span><span class="sxs-lookup"><span data-stu-id="aa7a8-124">Migration from Office Communications Server 2007 R2 to Lync Server 2013</span></span>](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md)

  - [<span data-ttu-id="aa7a8-125">Lync Server 2010、グループ チャットまたは Office Communicatins Server 2007 R2 グループ チャットから Lync Server 2013、常設チャット サーバーへの移行</span><span class="sxs-lookup"><span data-stu-id="aa7a8-125">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md)

</div>

<span id="BKMK_PhasedMigration"></span>

<div>

## <a name="coexistence-scenarios"></a><span data-ttu-id="aa7a8-126">共存シナリオ</span><span class="sxs-lookup"><span data-stu-id="aa7a8-126">Coexistence Scenarios</span></span>

<span data-ttu-id="aa7a8-127">Lync Server 2013 は、Lync Server 2010 の展開または Office Communications Server 2007 R2 の展開のコンポーネントと共存させることができます。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-127">Lync Server 2013 can coexist with components of either a Lync Server 2010 deployment or an Office Communications Server 2007 R2 deployment.</span></span> <span data-ttu-id="aa7a8-128">Lync Server 2010 と Office Communications Server 2007 R2 の両方 (3 つのバージョンの同時展開) での Lync Server 2013 の同時展開はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-128">Concurrent deployment of Lync Server 2013 with both Lync Server 2010 and Office Communications Server 2007 R2 (concurrent deployment of all three versions) is not supported.</span></span>

<span data-ttu-id="aa7a8-129">以前の Lync Server 2010 または Office Communications Server 2007 R2 の展開が、新しい Lync Server 2013 の展開で一時的に coexists される段階的な移行では、混合バージョンルーティングのサポートは制限されています。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-129">During a phased migration in which a previous Lync Server 2010 or Office Communications Server 2007 R2 deployment coexists temporarily with the new Lync Server 2013 deployment, support for mixed version routing is limited.</span></span> <span data-ttu-id="aa7a8-130">詳細については、移行に関するドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-130">For details, see the Migration documentation.</span></span>

<span data-ttu-id="aa7a8-131">Lync Server 2013 データベースインスタンスには、Microsoft SQL Server 2008 R2 または Microsoft SQL Server 2012 を実行している個別のコンピューターと個別のコンピューターを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-131">You must use separate and distinct computers running Microsoft SQL Server 2008 R2 or Microsoft SQL Server 2012 for your Lync Server 2013 database instances.</span></span> <span data-ttu-id="aa7a8-132">Lync Server 2010 または Office Communications Server 2007 R2 フロントエンドプールに使用している Lync Server 2013 フロントエンドプールに対して、同じインスタンスの SQL Server を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-132">You cannot use the same instance of SQL Server for a Lync Server 2013 Front End pool that you use for a Lync Server 2010 or Office Communications Server 2007 R2 Front End pool.</span></span> <span data-ttu-id="aa7a8-133">Lync Server 2010 または Office Communications Server 2007 R2 を既に展開している展開のために、トポロジビルダーで Lync Server 2013 を定義して構成した場合、トポロジビルダーでは、既にトポロジで使用されている Lync Server 2013 のインスタンスを定義することはできません。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-133">If you define and configure Lync Server 2013 in Topology Builder for a deployment that already has Lync Server 2010 or Office Communications Server 2007 R2 deployed, Topology Builder will not allow you to define an instance of a Lync Server 2013 that is already in use in the topology.</span></span>

<span data-ttu-id="aa7a8-134">次のメッセージが表示され、この問題が発生したことを通知するメッセージが表示されます。 " \[ サーバーの sql server FQDN には、 \] 既に sql インスタンスホスティング役割のユーザーストアが含まれています。"</span><span class="sxs-lookup"><span data-stu-id="aa7a8-134">Topology Builder will display the following message to inform you of this issue: "The SQL server \[FQDN of the server\] already contains a SQL instance hosting role 'User Store."</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="aa7a8-135">Lync Server 2013 の展開に新しく追加されたサーバーの役割を展開する場合は、移行ドキュメントと展開ドキュメントの説明に従って既存の展開をアップグレードして、計画ドキュメントと展開ドキュメントの説明に従って、新しいサーバーロールを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-135">If you intend to deploy server roles that are new to your Lync Server 2013 deployment, you should first upgrade your existing deployment as described in the Migration documentation and the Deployment documentation, and then deploy the new server roles as described in the Planning documentation and Deployment documentation.</span></span> <span data-ttu-id="aa7a8-136">グループチャットの以前のバージョンを移行する場合は、Lync Server 2010 または Office Communications Server 2007 R2 から他のすべてのコンポーネントを移行するプロセスを完了した後で、最後に移行します。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-136">If you are migrating a previous version of Group Chat, migrate it last, after completing the process for migrating all other components from Lync Server 2010 or Office Communications Server 2007 R2.</span></span>



</div>

<span data-ttu-id="aa7a8-137">特定の共存要件、および Lync Server 2010 または Office Communications Server 2007 R2 および Lync Server 2013 コンポーネントの共存と移行の詳細については、「 [Lync server 2010 から Lync server 2013 への移行](migration-from-lync-server-2010-to-lync-server-2013.md) と [office Communications server 2007 R2 から lync server 2013 へ](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md) の移行について」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-137">For specific coexistence requirements and other details about coexistence and migration of Lync Server 2010 or Office Communications Server 2007 R2 and Lync Server 2013 components, see [Migration from Lync Server 2010 to Lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) and [Migration from Office Communications Server 2007 R2 to Lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md) in the Migration documentation.</span></span> <span data-ttu-id="aa7a8-138">クライアントの混在バージョンサポートの詳細については、「 [Lync Server 2013 での以前の展開でサポートされているクライアント](lync-server-2013-supported-clients-from-previous-deployments.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa7a8-138">For details about mixed version support for clients, see [Supported clients from previous deployments in Lync Server 2013](lync-server-2013-supported-clients-from-previous-deployments.md).</span></span>

<span data-ttu-id="aa7a8-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aa7a8-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

