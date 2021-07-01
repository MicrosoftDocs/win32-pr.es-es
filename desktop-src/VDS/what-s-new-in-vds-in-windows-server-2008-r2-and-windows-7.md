---
description: Obtenga información sobre los nuevos cambios de Virtual Disk Service (VDS) en Windows Server 2008 R2 y Windows 7.
ms.assetid: 4ab37529-8d56-47a3-ad3d-0197cabd4f87
title: Novedades de VDS en Windows Server 2008 R2 y Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9050b157e9ce3c78550fdcffbd688988b7eacf90
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119660"
---
# <a name="whats-new-in-vds-in-windows-server-2008-r2-and-windows-7"></a><span data-ttu-id="22f28-103">Novedades de VDS en Windows Server 2008 R2 y Windows 7</span><span class="sxs-lookup"><span data-stu-id="22f28-103">What's New in VDS in Windows Server 2008 R2 and Windows 7</span></span>

<span data-ttu-id="22f28-104">\[A partir de Windows 8 y Windows Server 2012, la interfaz [COM](virtual-disk-service-portal.md) del servicio virtual de disco se sustituye por el servicio [de almacenamiento de Windows API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="22f28-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="22f28-105">Windows Server 2008 R2 y Windows 7 presentan los siguientes cambios en el servicio de disco virtual (VDS):</span><span class="sxs-lookup"><span data-stu-id="22f28-105">Windows Server 2008 R2 and Windows 7 introduce the following changes to the Virtual Disk Service (VDS):</span></span>

- [<span data-ttu-id="22f28-106">Nuevas interfaces VDS</span><span class="sxs-lookup"><span data-stu-id="22f28-106">New VDS Interfaces</span></span>](#new-vds-interfaces)
- [<span data-ttu-id="22f28-107">Nuevas enumeraciones VDS</span><span class="sxs-lookup"><span data-stu-id="22f28-107">New VDS Enumerations</span></span>](#new-vds-enumerations)
- [<span data-ttu-id="22f28-108">Nuevas estructuras VDS</span><span class="sxs-lookup"><span data-stu-id="22f28-108">New VDS Structures</span></span>](#new-vds-structures)
- [<span data-ttu-id="22f28-109">Modificaciones en enumeraciones VDS existentes</span><span class="sxs-lookup"><span data-stu-id="22f28-109">Modifications to Existing VDS Enumerations</span></span>](#modifications-to-existing-vds-enumerations)
- [<span data-ttu-id="22f28-110">Modificaciones en estructuras VDS existentes</span><span class="sxs-lookup"><span data-stu-id="22f28-110">Modifications to Existing VDS Structures</span></span>](#modifications-to-existing-vds-structures)

## <a name="new-vds-interfaces"></a><span data-ttu-id="22f28-111">Nuevas interfaces VDS</span><span class="sxs-lookup"><span data-stu-id="22f28-111">New VDS Interfaces</span></span>

<dl>

[<span data-ttu-id="22f28-112">**IVdsDisk3**</span><span class="sxs-lookup"><span data-stu-id="22f28-112">**IVdsDisk3**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdisk3)  
[<span data-ttu-id="22f28-113">**IVdsDiskPartitionMF2**</span><span class="sxs-lookup"><span data-stu-id="22f28-113">**IVdsDiskPartitionMF2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)  
[<span data-ttu-id="22f28-114">**IVdsDrive2**</span><span class="sxs-lookup"><span data-stu-id="22f28-114">**IVdsDrive2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsdrive2)  
[<span data-ttu-id="22f28-115">**IVdsHwProviderStoragePools**</span><span class="sxs-lookup"><span data-stu-id="22f28-115">**IVdsHwProviderStoragePools**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)  
[<span data-ttu-id="22f28-116">**IVdsLun2**</span><span class="sxs-lookup"><span data-stu-id="22f28-116">**IVdsLun2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdslun2)  
[<span data-ttu-id="22f28-117">**IVdsLunNumber**</span><span class="sxs-lookup"><span data-stu-id="22f28-117">**IVdsLunNumber**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)  
[<span data-ttu-id="22f28-118">**IVdsOpenVDisk**</span><span class="sxs-lookup"><span data-stu-id="22f28-118">**IVdsOpenVDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsopenvdisk)  
[<span data-ttu-id="22f28-119">**IVdsStoragePool**</span><span class="sxs-lookup"><span data-stu-id="22f28-119">**IVdsStoragePool**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)  
[<span data-ttu-id="22f28-120">**IVdsSubSystem2**</span><span class="sxs-lookup"><span data-stu-id="22f28-120">**IVdsSubSystem2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdssubsystem2)  
[<span data-ttu-id="22f28-121">**IVdsSubSystemInterconnect**</span><span class="sxs-lookup"><span data-stu-id="22f28-121">**IVdsSubSystemInterconnect**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdssubsysteminterconnect)  
[<span data-ttu-id="22f28-122">**IVdsVDisk**</span><span class="sxs-lookup"><span data-stu-id="22f28-122">**IVdsVDisk**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvdisk)  
[<span data-ttu-id="22f28-123">**IVdsVdProvider**</span><span class="sxs-lookup"><span data-stu-id="22f28-123">**IVdsVdProvider**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvdprovider)  
[<span data-ttu-id="22f28-124">**IVdsVolume2**</span><span class="sxs-lookup"><span data-stu-id="22f28-124">**IVdsVolume2**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvolume2)  
[<span data-ttu-id="22f28-125">**IVdsVolumeMF3**</span><span class="sxs-lookup"><span data-stu-id="22f28-125">**IVdsVolumeMF3**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf3)  


## <a name="new-vds-enumerations"></a><span data-ttu-id="22f28-126">Nuevas enumeraciones VDS</span><span class="sxs-lookup"><span data-stu-id="22f28-126">New VDS Enumerations</span></span>

<dl>

[<span data-ttu-id="22f28-127">**VDS_DISK_OFFLINE_REASON**</span><span class="sxs-lookup"><span data-stu-id="22f28-127">**VDS_DISK_OFFLINE_REASON**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_disk_offline_reason)  
[<span data-ttu-id="22f28-128">**VDS_FORMAT_OPTION_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="22f28-128">**VDS_FORMAT_OPTION_FLAGS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_format_option_flags)  
[<span data-ttu-id="22f28-129">**VDS_INTERCONNECT_FLAG**</span><span class="sxs-lookup"><span data-stu-id="22f28-129">**VDS_INTERCONNECT_FLAG**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_interconnect_flag)  
[<span data-ttu-id="22f28-130">**VDS_RAID_TYPE**</span><span class="sxs-lookup"><span data-stu-id="22f28-130">**VDS_RAID_TYPE**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_raid_type)  
[<span data-ttu-id="22f28-131">**VDS_STORAGE_POOL_STATUS**</span><span class="sxs-lookup"><span data-stu-id="22f28-131">**VDS_STORAGE_POOL_STATUS**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)  
[<span data-ttu-id="22f28-132">**VDS_STORAGE_POOL_TYPE**</span><span class="sxs-lookup"><span data-stu-id="22f28-132">**VDS_STORAGE_POOL_TYPE**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type)  
[<span data-ttu-id="22f28-133">**VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG**</span><span class="sxs-lookup"><span data-stu-id="22f28-133">**VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_sub_system_supported_raid_type_flag)  
[<span data-ttu-id="22f28-134">**VDS_VDISK_STATE**</span><span class="sxs-lookup"><span data-stu-id="22f28-134">**VDS_VDISK_STATE**</span></span>](/windows/desktop/api/Vds/ne-vds-vds_vdisk_state)  


## <a name="new-vds-structures"></a><span data-ttu-id="22f28-135">Nuevas estructuras VDS</span><span class="sxs-lookup"><span data-stu-id="22f28-135">New VDS Structures</span></span>

<dl>

[<span data-ttu-id="22f28-136">**VDS_CREATE_VDISK_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="22f28-136">**VDS_CREATE_VDISK_PARAMETERS**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_create_vdisk_parameters)  
[<span data-ttu-id="22f28-137">**VDS_DISK_FREE_EXTENT**</span><span class="sxs-lookup"><span data-stu-id="22f28-137">**VDS_DISK_FREE_EXTENT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_disk_free_extent)  
[<span data-ttu-id="22f28-138">**VDS_DISK_PROP2**</span><span class="sxs-lookup"><span data-stu-id="22f28-138">**VDS_DISK_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_disk_prop2)  
[<span data-ttu-id="22f28-139">**VDS_DRIVE_PROP2**</span><span class="sxs-lookup"><span data-stu-id="22f28-139">**VDS_DRIVE_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_drive_prop2)  
[<span data-ttu-id="22f28-140">**VDS_HINTS2**</span><span class="sxs-lookup"><span data-stu-id="22f28-140">**VDS_HINTS2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_hints2)  
[<span data-ttu-id="22f28-141">**VDS_POOL_ATTRIBUTES**</span><span class="sxs-lookup"><span data-stu-id="22f28-141">**VDS_POOL_ATTRIBUTES**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes)  
[<span data-ttu-id="22f28-142">**VDS_POOL_CUSTOM_ATTRIBUTES**</span><span class="sxs-lookup"><span data-stu-id="22f28-142">**VDS_POOL_CUSTOM_ATTRIBUTES**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes)  
[<span data-ttu-id="22f28-143">**VDS_STORAGE_POOL_DRIVE_EXTENT**</span><span class="sxs-lookup"><span data-stu-id="22f28-143">**VDS_STORAGE_POOL_DRIVE_EXTENT**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)  
[<span data-ttu-id="22f28-144">**VDS_STORAGE_POOL_PROP**</span><span class="sxs-lookup"><span data-stu-id="22f28-144">**VDS_STORAGE_POOL_PROP**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop)  
[<span data-ttu-id="22f28-145">**VDS_SUB_SYSTEM_PROP2**</span><span class="sxs-lookup"><span data-stu-id="22f28-145">**VDS_SUB_SYSTEM_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop2)  
[<span data-ttu-id="22f28-146">**VDS_VDISK_PROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="22f28-146">**VDS_VDISK_PROPERTIES**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_vdisk_properties)  
[<span data-ttu-id="22f28-147">**VDS_VOLUME_PROP2**</span><span class="sxs-lookup"><span data-stu-id="22f28-147">**VDS_VOLUME_PROP2**</span></span>](/windows/desktop/api/Vds/ns-vds-vds_volume_prop)  


## <a name="modifications-to-existing-vds-enumerations"></a><span data-ttu-id="22f28-148">Modificaciones en enumeraciones VDS existentes</span><span class="sxs-lookup"><span data-stu-id="22f28-148">Modifications to Existing VDS Enumerations</span></span>

<span data-ttu-id="22f28-149">[**VDS_ASYNC_OUTPUT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_async_output_type) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-149">[**VDS_ASYNC_OUTPUT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_async_output_type) enumeration added values:</span></span>

 <span data-ttu-id="22f28-150">**VDS_ASYNCOUT_CREATE_VDISK**</span><span class="sxs-lookup"><span data-stu-id="22f28-150">**VDS_ASYNCOUT_CREATE_VDISK**</span></span>  
<span data-ttu-id="22f28-151">**VDS_ASYNCOUT_ATTACH_VDISK**</span><span class="sxs-lookup"><span data-stu-id="22f28-151">**VDS_ASYNCOUT_ATTACH_VDISK**</span></span>  
<span data-ttu-id="22f28-152">**VDS_ASYNCOUT_COMPACT_VDISK**</span><span class="sxs-lookup"><span data-stu-id="22f28-152">**VDS_ASYNCOUT_COMPACT_VDISK**</span></span>  
<span data-ttu-id="22f28-153">**VDS_ASYNCOUT_MERGE_VDISK**</span><span class="sxs-lookup"><span data-stu-id="22f28-153">**VDS_ASYNCOUT_MERGE_VDISK**</span></span>  
<span data-ttu-id="22f28-154">**VDS_ASYNCOUT_EXPAND_VDISK**</span><span class="sxs-lookup"><span data-stu-id="22f28-154">**VDS_ASYNCOUT_EXPAND_VDISK**</span></span>  


<span data-ttu-id="22f28-155">[**VDS_CONTROLLER_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status) valor agregado de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-155">[**VDS_CONTROLLER_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status) enumeration added value:</span></span>

<span data-ttu-id="22f28-156">**VDS_CS_REMOVED**</span><span class="sxs-lookup"><span data-stu-id="22f28-156">**VDS_CS_REMOVED**</span></span>  


<span data-ttu-id="22f28-157">[**VDS_DISK_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag) valor agregado de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-157">[**VDS_DISK_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag) enumeration added value:</span></span>

<span data-ttu-id="22f28-158">**VDS_DF_BOOT_FROM_DISK**</span><span class="sxs-lookup"><span data-stu-id="22f28-158">**VDS_DF_BOOT_FROM_DISK**</span></span>  
<span data-ttu-id="22f28-159">**VDS_DF_CURRENT_READ_ONLY**</span><span class="sxs-lookup"><span data-stu-id="22f28-159">**VDS_DF_CURRENT_READ_ONLY**</span></span>  


<span data-ttu-id="22f28-160">[**VDS_DRIVE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-160">[**VDS_DRIVE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag) enumeration added values:</span></span>

<span data-ttu-id="22f28-161">**VDS_DRF_ASSIGNED**</span><span class="sxs-lookup"><span data-stu-id="22f28-161">**VDS_DRF_ASSIGNED**</span></span>  
<span data-ttu-id="22f28-162">**VDS_DRF_UNASSIGNED**</span><span class="sxs-lookup"><span data-stu-id="22f28-162">**VDS_DRF_UNASSIGNED**</span></span>  
<span data-ttu-id="22f28-163">**VDS_DRF_HOTSPARE_IN_USE**</span><span class="sxs-lookup"><span data-stu-id="22f28-163">**VDS_DRF_HOTSPARE_IN_USE**</span></span>  
<span data-ttu-id="22f28-164">**VDS_DRF_HOTSPARE_STANDBY**</span><span class="sxs-lookup"><span data-stu-id="22f28-164">**VDS_DRF_HOTSPARE_STANDBY**</span></span>  


<span data-ttu-id="22f28-165">[**VDS_DRIVE_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status) valor agregado de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-165">[**VDS_DRIVE_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status) enumeration added value:</span></span>

<span data-ttu-id="22f28-166">**VDS_DRS_REMOVED**</span><span class="sxs-lookup"><span data-stu-id="22f28-166">**VDS_DRS_REMOVED**</span></span>  


<span data-ttu-id="22f28-167">[**VDS_FILE_SYSTEM_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_file_system_type) valor agregado de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-167">[**VDS_FILE_SYSTEM_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_file_system_type) enumeration added value:</span></span>

<span data-ttu-id="22f28-168">**VDS_FST_EXFAT**</span><span class="sxs-lookup"><span data-stu-id="22f28-168">**VDS_FST_EXFAT**</span></span>  


<span data-ttu-id="22f28-169">[**VDS_HEALTH**](/windows/desktop/api/Vds/ne-vds-vds_health) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-169">[**VDS_HEALTH**](/windows/desktop/api/Vds/ne-vds-vds_health) enumeration added values:</span></span>

<span data-ttu-id="22f28-170">**VDS_H_REPLACED**</span><span class="sxs-lookup"><span data-stu-id="22f28-170">**VDS_H_REPLACED**</span></span>  
<span data-ttu-id="22f28-171">**VDS_H_PENDING_FAILURE**</span><span class="sxs-lookup"><span data-stu-id="22f28-171">**VDS_H_PENDING_FAILURE**</span></span>  
<span data-ttu-id="22f28-172">**VDS_H_DEGRADED**</span><span class="sxs-lookup"><span data-stu-id="22f28-172">**VDS_H_DEGRADED**</span></span>  


<span data-ttu-id="22f28-173">[**VDS_HWPROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hwprovider_type) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-173">[**VDS_HWPROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hwprovider_type) enumeration added values:</span></span>

<span data-ttu-id="22f28-174">**VDS_HWT_SAS**</span><span class="sxs-lookup"><span data-stu-id="22f28-174">**VDS_HWT_SAS**</span></span>  
<span data-ttu-id="22f28-175">**VDS_HWT_HYBRID**</span><span class="sxs-lookup"><span data-stu-id="22f28-175">**VDS_HWT_HYBRID**</span></span>  


<span data-ttu-id="22f28-176">[**VDS_LUN_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-176">[**VDS_LUN_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) enumeration added values:</span></span>

<span data-ttu-id="22f28-177">**VDS_LF_READ_CACHE_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="22f28-177">**VDS_LF_READ_CACHE_ENABLED**</span></span>  
<span data-ttu-id="22f28-178">**VDS_LF_WRITE_CACHE_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="22f28-178">**VDS_LF_WRITE_CACHE_ENABLED**</span></span>  
<span data-ttu-id="22f28-179">**VDS_LF_MEDIA_SCAN_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="22f28-179">**VDS_LF_MEDIA_SCAN_ENABLED**</span></span>  
<span data-ttu-id="22f28-180">**VDS_LF_CONSISTENCY_CHECK_ENABLED**</span><span class="sxs-lookup"><span data-stu-id="22f28-180">**VDS_LF_CONSISTENCY_CHECK_ENABLED**</span></span>  
<span data-ttu-id="22f28-181">**VDS_LF_SNAPSHOT**</span><span class="sxs-lookup"><span data-stu-id="22f28-181">**VDS_LF_SNAPSHOT**</span></span>  


<span data-ttu-id="22f28-182">[**VDS_LUN_PLEX_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-182">[**VDS_LUN_PLEX_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type) enumeration added values:</span></span>

<span data-ttu-id="22f28-183">**VDS_LPT_RAID2**</span><span class="sxs-lookup"><span data-stu-id="22f28-183">**VDS_LPT_RAID2**</span></span>  
<span data-ttu-id="22f28-184">**VDS_LPT_RAID3**</span><span class="sxs-lookup"><span data-stu-id="22f28-184">**VDS_LPT_RAID3**</span></span>  
<span data-ttu-id="22f28-185">**VDS_LPT_RAID4**</span><span class="sxs-lookup"><span data-stu-id="22f28-185">**VDS_LPT_RAID4**</span></span>  
<span data-ttu-id="22f28-186">**VDS_LPT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="22f28-186">**VDS_LPT_RAID5**</span></span>  
<span data-ttu-id="22f28-187">**VDS_LPT_RAID6**</span><span class="sxs-lookup"><span data-stu-id="22f28-187">**VDS_LPT_RAID6**</span></span>  
<span data-ttu-id="22f28-188">**VDS_LPT_RAID03**</span><span class="sxs-lookup"><span data-stu-id="22f28-188">**VDS_LPT_RAID03**</span></span>  
<span data-ttu-id="22f28-189">**VDS_LPT_RAID05**</span><span class="sxs-lookup"><span data-stu-id="22f28-189">**VDS_LPT_RAID05**</span></span>  
<span data-ttu-id="22f28-190">**VDS_LPT_RAID10**</span><span class="sxs-lookup"><span data-stu-id="22f28-190">**VDS_LPT_RAID10**</span></span>  
<span data-ttu-id="22f28-191">**VDS_LPT_RAID15**</span><span class="sxs-lookup"><span data-stu-id="22f28-191">**VDS_LPT_RAID15**</span></span>  
<span data-ttu-id="22f28-192">**VDS_LPT_RAID30**</span><span class="sxs-lookup"><span data-stu-id="22f28-192">**VDS_LPT_RAID30**</span></span>  
<span data-ttu-id="22f28-193">**VDS_LPT_RAID50**</span><span class="sxs-lookup"><span data-stu-id="22f28-193">**VDS_LPT_RAID50**</span></span>  
<span data-ttu-id="22f28-194">**VDS_LPT_RAID53**</span><span class="sxs-lookup"><span data-stu-id="22f28-194">**VDS_LPT_RAID53**</span></span>  
<span data-ttu-id="22f28-195">**VDS_LPT_RAID60**</span><span class="sxs-lookup"><span data-stu-id="22f28-195">**VDS_LPT_RAID60**</span></span>  


<span data-ttu-id="22f28-196">[**VDS_LUN_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_type) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-196">[**VDS_LUN_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_type) enumeration added values:</span></span>

<span data-ttu-id="22f28-197">**VDS_LT_RAID2**</span><span class="sxs-lookup"><span data-stu-id="22f28-197">**VDS_LT_RAID2**</span></span>  
<span data-ttu-id="22f28-198">**VDS_LT_RAID3**</span><span class="sxs-lookup"><span data-stu-id="22f28-198">**VDS_LT_RAID3**</span></span>  
<span data-ttu-id="22f28-199">**VDS_LT_RAID4**</span><span class="sxs-lookup"><span data-stu-id="22f28-199">**VDS_LT_RAID4**</span></span>  
<span data-ttu-id="22f28-200">**VDS_LT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="22f28-200">**VDS_LT_RAID5**</span></span>  
<span data-ttu-id="22f28-201">**VDS_LT_RAID6**</span><span class="sxs-lookup"><span data-stu-id="22f28-201">**VDS_LT_RAID6**</span></span>  
<span data-ttu-id="22f28-202">**VDS_LT_RAID01**</span><span class="sxs-lookup"><span data-stu-id="22f28-202">**VDS_LT_RAID01**</span></span>  
<span data-ttu-id="22f28-203">**VDS_LT_RAID03**</span><span class="sxs-lookup"><span data-stu-id="22f28-203">**VDS_LT_RAID03**</span></span>  
<span data-ttu-id="22f28-204">**VDS_LT_RAID05**</span><span class="sxs-lookup"><span data-stu-id="22f28-204">**VDS_LT_RAID05**</span></span>  
<span data-ttu-id="22f28-205">**VDS_LT_RAID10**</span><span class="sxs-lookup"><span data-stu-id="22f28-205">**VDS_LT_RAID10**</span></span>  
<span data-ttu-id="22f28-206">**VDS_LT_RAID15**</span><span class="sxs-lookup"><span data-stu-id="22f28-206">**VDS_LT_RAID15**</span></span>  
<span data-ttu-id="22f28-207">**VDS_LT_RAID30**</span><span class="sxs-lookup"><span data-stu-id="22f28-207">**VDS_LT_RAID30**</span></span>  
<span data-ttu-id="22f28-208">**VDS_LT_RAID50**</span><span class="sxs-lookup"><span data-stu-id="22f28-208">**VDS_LT_RAID50**</span></span>  
<span data-ttu-id="22f28-209">**VDS_LT_RAID51**</span><span class="sxs-lookup"><span data-stu-id="22f28-209">**VDS_LT_RAID51**</span></span>  
<span data-ttu-id="22f28-210">**VDS_LT_RAID53**</span><span class="sxs-lookup"><span data-stu-id="22f28-210">**VDS_LT_RAID53**</span></span>  
<span data-ttu-id="22f28-211">**VDS_LT_RAID60**</span><span class="sxs-lookup"><span data-stu-id="22f28-211">**VDS_LT_RAID60**</span></span>  
<span data-ttu-id="22f28-212">**VDS_LT_RAID61**</span><span class="sxs-lookup"><span data-stu-id="22f28-212">**VDS_LT_RAID61**</span></span>  


<span data-ttu-id="22f28-213">[**VDS_OBJECT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_object_type) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-213">[**VDS_OBJECT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_object_type) enumeration added values:</span></span>

<span data-ttu-id="22f28-214">**VDS_OT_STORAGE_POOL**</span><span class="sxs-lookup"><span data-stu-id="22f28-214">**VDS_OT_STORAGE_POOL**</span></span>  
<span data-ttu-id="22f28-215">**VDS_OT_VDISK**</span><span class="sxs-lookup"><span data-stu-id="22f28-215">**VDS_OT_VDISK**</span></span>  
<span data-ttu-id="22f28-216">**VDS_OT_OPEN_VDISK**</span><span class="sxs-lookup"><span data-stu-id="22f28-216">**VDS_OT_OPEN_VDISK**</span></span>  


<span data-ttu-id="22f28-217">[**VDS_PORT_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_port_status) valor agregado de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-217">[**VDS_PORT_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_port_status) enumeration added value:</span></span>

<span data-ttu-id="22f28-218">**VDS_DRS_REMOVED**</span><span class="sxs-lookup"><span data-stu-id="22f28-218">**VDS_DRS_REMOVED**</span></span>  


<span data-ttu-id="22f28-219">[**VDS_PROVIDER_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-219">[**VDS_PROVIDER_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag) enumeration added values:</span></span>

<span data-ttu-id="22f28-220">**VDS_PF_SUPPORT_MIRROR**</span><span class="sxs-lookup"><span data-stu-id="22f28-220">**VDS_PF_SUPPORT_MIRROR**</span></span>  
<span data-ttu-id="22f28-221">**VDS_PF_SUPPORT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="22f28-221">**VDS_PF_SUPPORT_RAID5**</span></span>  


<span data-ttu-id="22f28-222">[**VDS_PROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_provider_type) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-222">[**VDS_PROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_provider_type) enumeration added values:</span></span>

<span data-ttu-id="22f28-223">**VDS_PT_VIRTUALDISK**</span><span class="sxs-lookup"><span data-stu-id="22f28-223">**VDS_PT_VIRTUALDISK**</span></span>  
<span data-ttu-id="22f28-224">**VDS_PT_MAX**</span><span class="sxs-lookup"><span data-stu-id="22f28-224">**VDS_PT_MAX**</span></span>  


<span data-ttu-id="22f28-225">[**VDS_SERVICE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_service_flag) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-225">[**VDS_SERVICE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_service_flag) enumeration added values:</span></span>

<span data-ttu-id="22f28-226">**VDS_SVF_SUPPORT_MIRROR**</span><span class="sxs-lookup"><span data-stu-id="22f28-226">**VDS_SVF_SUPPORT_MIRROR**</span></span>  
<span data-ttu-id="22f28-227">**VDS_SVF_SUPPORT_RAID5**</span><span class="sxs-lookup"><span data-stu-id="22f28-227">**VDS_SVF_SUPPORT_RAID5**</span></span>  


<span data-ttu-id="22f28-228">[**VDS_SUB_SYSTEM_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-228">[**VDS_SUB_SYSTEM_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) enumeration added values:</span></span>

<span data-ttu-id="22f28-229">**VDS_SF_SUPPORTS_LUN_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="22f28-229">**VDS_SF_SUPPORTS_LUN_NUMBER**</span></span>  
<span data-ttu-id="22f28-230">**VDS_SF_SUPPORTS_MIRRORED_CACHE**</span><span class="sxs-lookup"><span data-stu-id="22f28-230">**VDS_SF_SUPPORTS_MIRRORED_CACHE**</span></span>  
<span data-ttu-id="22f28-231">**VDS_SF_READ_CACHING_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="22f28-231">**VDS_SF_READ_CACHING_CAPABLE**</span></span>  
<span data-ttu-id="22f28-232">**VDS_SF_WRITE_CACHING_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="22f28-232">**VDS_SF_WRITE_CACHING_CAPABLE**</span></span>  
<span data-ttu-id="22f28-233">**VDS_SF_MEDIA_SCAN_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="22f28-233">**VDS_SF_MEDIA_SCAN_CAPABLE**</span></span>  
<span data-ttu-id="22f28-234">**VDS_SF_CONSISTENCY_CHECK_CAPABLE**</span><span class="sxs-lookup"><span data-stu-id="22f28-234">**VDS_SF_CONSISTENCY_CHECK_CAPABLE**</span></span>  


<span data-ttu-id="22f28-235">[**VDS_TRANSITION_STATE**](/windows/desktop/api/Vds/ne-vds-vds_transition_state) valor agregado de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-235">[**VDS_TRANSITION_STATE**](/windows/desktop/api/Vds/ne-vds-vds_transition_state) enumeration added value:</span></span>

<span data-ttu-id="22f28-236">**VDS_TS_RESTRIPING**</span><span class="sxs-lookup"><span data-stu-id="22f28-236">**VDS_TS_RESTRIPING**</span></span>  


<span data-ttu-id="22f28-237">[**VDS_VERSION_SUPPORT_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_version_support_flag) valores agregados de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-237">[**VDS_VERSION_SUPPORT_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_version_support_flag) enumeration added values:</span></span>

<span data-ttu-id="22f28-238">**VDS_VSF_2_0**</span><span class="sxs-lookup"><span data-stu-id="22f28-238">**VDS_VSF_2_0**</span></span>  
<span data-ttu-id="22f28-239">**VDS_VSF_2_1**</span><span class="sxs-lookup"><span data-stu-id="22f28-239">**VDS_VSF_2_1**</span></span>  
<span data-ttu-id="22f28-240">**VDS_VSF_3_0**</span><span class="sxs-lookup"><span data-stu-id="22f28-240">**VDS_VSF_3_0**</span></span>  


<span data-ttu-id="22f28-241">[**VDS_VOLUME_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_volume_status) valor agregado de enumeración:</span><span class="sxs-lookup"><span data-stu-id="22f28-241">[**VDS_VOLUME_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_volume_status) enumeration added value:</span></span>

<span data-ttu-id="22f28-242">**VDS_VS_OFFLINE**</span><span class="sxs-lookup"><span data-stu-id="22f28-242">**VDS_VS_OFFLINE**</span></span>  


## <a name="modifications-to-existing-vds-structures"></a><span data-ttu-id="22f28-243">Modificaciones en estructuras VDS existentes</span><span class="sxs-lookup"><span data-stu-id="22f28-243">Modifications to Existing VDS Structures</span></span>

<span data-ttu-id="22f28-244">[**VDS_CONTROLLER_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification) estructura ha agregado **valores ulEvent:**</span><span class="sxs-lookup"><span data-stu-id="22f28-244">[**VDS_CONTROLLER_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification) structure added **ulEvent** values:</span></span>

<span data-ttu-id="22f28-245">VDS_NF_CONTROLLER_MODIFY</span><span class="sxs-lookup"><span data-stu-id="22f28-245">VDS_NF_CONTROLLER_MODIFY</span></span>  
<span data-ttu-id="22f28-246">VDS_NF_CONTROLLER_REMOVED</span><span class="sxs-lookup"><span data-stu-id="22f28-246">VDS_NF_CONTROLLER_REMOVED</span></span>  


<span data-ttu-id="22f28-247">[**VDS_DRIVE_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification) estructura ha agregado **el valor ulEvent:**</span><span class="sxs-lookup"><span data-stu-id="22f28-247">[**VDS_DRIVE_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification) structure added **ulEvent** value:</span></span>

<span data-ttu-id="22f28-248">VDS_NF_DRIVE_REMOVED</span><span class="sxs-lookup"><span data-stu-id="22f28-248">VDS_NF_DRIVE_REMOVED</span></span>  


<span data-ttu-id="22f28-249">[**VDS_PORT_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) estructura ha agregado **valores ulEvent:**</span><span class="sxs-lookup"><span data-stu-id="22f28-249">[**VDS_PORT_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) structure added **ulEvent** values:</span></span>

<span data-ttu-id="22f28-250">VDS_NF_PORT_MODIFY</span><span class="sxs-lookup"><span data-stu-id="22f28-250">VDS_NF_PORT_MODIFY</span></span>  
<span data-ttu-id="22f28-251">VDS_NF_PORT_REMOVED</span><span class="sxs-lookup"><span data-stu-id="22f28-251">VDS_NF_PORT_REMOVED</span></span>  


 

 
