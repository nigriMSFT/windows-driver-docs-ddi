---
UID: NF:netpoweroffload.NetPowerOffloadGetArpParameters
title: NetPowerOffloadGetArpParameters function (netpoweroffload.h)
description: The NetPowerOffloadGetArpParameters function gets parameters for an IPv4 ARP low power protocol offload to a net adapter.
tech.root: netvista
ms.date: 10/03/2019
keywords: ["NetPowerOffloadGetArpParameters function"]
ms.keywords: NetPowerOffloadGetArpParameters
req.header: netpoweroffload.h
req.include-header: netadaptercx.h 
req.target-type: Universal
req.target-min-winverclnt: Windows 10, version 2004
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: netadaptercxstub.lib
req.dll: 
req.irql: PASSIVE_LEVEL
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
ms.custom: Vb
f1_keywords:
 - NetPowerOffloadGetArpParameters
 - netpoweroffload/NetPowerOffloadGetArpParameters
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - netadaptercxstub.lib
api_name:
 - NetPowerOffloadGetArpParameters
product:
 - Windows
---

# NetPowerOffloadGetArpParameters function


## -description

The **NetPowerOffloadGetArpParameters** function gets parameters for an IPv4 ARP low power protocol offload to a net adapter.

## -parameters

### -param PowerOffload [_In_]

The NETPOWEROFFLOAD object that represents this ARP protocol offload.

### -param Parameters [_Inout_]

A pointer to a driver-allocated and initialized [**NET_POWER_OFFLOAD_ARP_PARAMETERS**](../netpoweroffload/ns-netpoweroffload-_net_power_offload_arp_parameters.md) structure that receives the ARP parameter information.


## -remarks

Call [**NET_POWER_OFFLOAD_ARP_PARAMETERS_INIT**](../netpoweroffload/nf-netpoweroffload-net_power_offload_arp_parameters_init.md) to initialize the [**NET_POWER_OFFLOAD_ARP_PARAMETERS**](../netpoweroffload/ns-netpoweroffload-_net_power_offload_arp_parameters.md) structure before calling this function.

The client driver must only call **NetPowerOffloadGetArpParameters** during a power transition, typically from its *[EVT_WDF_DEVICE_ARM_WAKE_FROM_SX](../wdfdevice/nc-wdfdevice-evt_wdf_device_arm_wake_from_sx.md)*, *[EVT_WDF_DEVICE_ARM_WAKE_FROM_S0](../wdfdevice/nc-wdfdevice-evt_wdf_device_arm_wake_from_s0.md)*, or *[EVT_NET_DEVICE_PREVIEW_POWER_OFFLOAD](../netdevice/nc-netdevice-evt_net_device_preview_power_offload.md)* callback function. Otherwise, the call results in a system bugcheck.

## -see-also

[Configuring power management](/windows-hardware/drivers/netcx/configuring-power-management)

[**NET_POWER_OFFLOAD_ARP_PARAMETERS**](../netpoweroffload/ns-netpoweroffload-_net_power_offload_arp_parameters.md)

[**NET_POWER_OFFLOAD_ARP_PARAMETERS_INIT**](../netpoweroffload/nf-netpoweroffload-net_power_offload_arp_parameters_init.md)
