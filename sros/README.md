# TiMOS/SROS telemetry


Sample sensor list:

```
/state/port[port-id=*]/statistics/in-discards
/state/port[port-id=*]/statistics/in-errors
/state/port[port-id=*]/statistics/in-octets
/state/port[port-id=*]/statistics/in-packets
/state/port[port-id=*]/statistics/out-discards
/state/port[port-id=*]/statistics/out-errors
/state/port[port-id=*]/statistics/out-octets
/state/port[port-id=*]/statistics/out-packets

/state/port[port-id=*]/transceiver/digital-diagnostic-monitoring/temperature/current
/state/port[port-id=*]/transceiver/digital-diagnostic-monitoring/transmit-output-power/current
/state/port[port-id=*]/transceiver/digital-diagnostic-monitoring/received-optical-power/current
/state/port[port-id=*]/transceiver/digital-diagnostic-monitoring/received-optical-power/low-alarm

# /state/port[port-id=*]/transceiver/digital-diagnostic-monitoring/lane[lane-id=*]/received-optical-power/current


/state/port[port-id=*]/statistics/egress-queue/queue[queue-id=*]/forward-unicast-octets
/state/port[port-id=*]/statistics/egress-queue/queue[queue-id=*]/forward-multicast-octets
/state/port[port-id=*]/statistics/egress-queue/queue[queue-id=*]/drop-unicast-packets
/state/port[port-id=*]/statistics/egress-queue/queue[queue-id=*]/drop-multicast-packets

/state/port[port-id=*]/egress/voq[queue-id=*]/forward-octets
/state/port[port-id=*]/egress/voq[queue-id=*]/drop-packets

```