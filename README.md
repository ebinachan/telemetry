# telemetry

Updated metrics.json for Cisco's telemetry collector, Pipeline.

Sample sensor list:

```
telemetry model-driven
 destination-group PIPELINE1
  address-family ipv4 10.0.0.1 port 5432
   encoding self-describing-gpb
   protocol tcp
  !
 !
 destination-group PIPELINE2
  address-family ipv4 10.0.0.1 port 5433
   encoding self-describing-gpb
   protocol tcp
  !
 !
 sensor-group SG_BGP
  sensor-path Cisco-IOS-XR-ipv4-bgp-oper:bgp/instances/instance/instance-active/default-vrf/process-info
  sensor-path Cisco-IOS-XR-ipv4-bgp-oper:bgp/instances/instance/instance-active/default-vrf/sessions/session
 !
 sensor-group SG_FIA
  sensor-path Cisco-IOS-XR-asr9k-fsi-oper:fabric-stats/nodes/node/statses/stats
 !
 sensor-group SG_NPU
  sensor-path Cisco-IOS-XR-asr9k-np-oper:hardware-module-np/nodes/node/nps/np/counters
  sensor-path Cisco-IOS-XR-asr9k-np-oper:hardware-module-np/nodes/node/nps/np/load-utilization
  sensor-path Cisco-IOS-XR-asr9k-np-oper:hardware-module-np/nodes/node[node-name="0/0/CPU0"]/nps/np/fast-drop
 !
 sensor-group SG_NPU5M
  sensor-path Cisco-IOS-XR-asr9k-np-oper:hardware-module-np/nodes/node/nps/np/tcam-summary
 !
 sensor-group SG5MINS
  sensor-path Cisco-IOS-XR-asr9k-sc-envmon-oper:environmental-monitoring/racks/rack/slots/slot/modules/module/sensor-types/sensor-type[type='temp']/sensor-names/sensor-name/value-detailed
 !
 sensor-group SG_OPTICS
  sensor-path Cisco-IOS-XR-controller-optics-oper:optics-oper/optics-ports/optics-port[name='Optics0/3/0/0']/optics-info
  sensor-path Cisco-IOS-XR-controller-optics-oper:optics-oper/optics-ports/optics-port[name='Optics0/3/0/1']/optics-info
  sensor-path Cisco-IOS-XR-controller-optics-oper:optics-oper/optics-ports/optics-port[name='Optics0/3/0/3']/optics-info
  sensor-path Cisco-IOS-XR-dwdm-ui-oper:dwdm/ports/port[name='dwdm0/2/0/20/0']/info
  sensor-path Cisco-IOS-XR-pmengine-oper:performance-management/dwdm/dwdm-ports/dwdm-port[name='dwdm0/2/0/20/0']/dwdm-current/dwdm-minute15/dwdm-minute15-optics/dwdm-minute15-optic
 !
 sensor-group SG_GENERAL
  sensor-path Cisco-IOS-XR-flowspec-oper:flow-spec/summary
  sensor-path Cisco-IOS-XR-flowspec-oper:flow-spec/vrfs/vrf/afs/af/flows/flow
  sensor-path Cisco-IOS-XR-l2vpn-oper:l2vpnv2/active/bridge-summary
  sensor-path Cisco-IOS-XR-l2vpn-oper:l2vpnv2/active/xconnect-summary
  sensor-path Cisco-IOS-XR-wdsysmon-fd-oper:system-monitoring/cpu-utilization
  sensor-path Cisco-IOS-XR-nto-misc-shmem-oper:memory-summary/nodes/node/summary
  sensor-path Cisco-IOS-XR-subscriber-pppoe-ma-oper:pppoe/nodes/node/summary-total
  sensor-path Cisco-IOS-XR-clns-isis-oper:isis/instances/instance/statistics-global
  sensor-path Cisco-IOS-XR-asr9k-lpts-oper:platform-lptsp-ifib/nodes/node/police/police-info
  sensor-path Cisco-IOS-XR-ipv4-pim-oper:pim/active/vrfs/vrf[vrf-name="default"]/summary
  sensor-path Cisco-IOS-XR-ipv4-igmp-oper:igmp/active/vrfs/vrf[vrf-name="default"]/group-summary
  sensor-path Cisco-IOS-XR-ip-daps-oper:address-pool-service/nodes/node/pools/pool/allocated-addresses
  sensor-path Cisco-IOS-XR-asr9k-lpts-oper:platform-lptsp-ifib-static/node-statics/node-static/police/static-info
  sensor-path Cisco-IOS-XR-ip-rib-ipv4-oper:rib/vrfs/vrf[vrf-name='default']/afs/af/safs/saf/ip-rib-route-table-names/ip-rib-route-table-name/protocol/bgp/as/information
  sensor-path Cisco-IOS-XR-ip-rib-ipv6-oper:ipv6-rib/vrfs/vrf[vrf-name='default']/afs/af/safs/saf/ip-rib-route-table-names/ip-rib-route-table-name/protocol/bgp/as/information
 !
 sensor-group SG_L2VPN_COUNTERS
  sensor-path Cisco-IOS-XR-l2vpn-oper:l2vpnv2/active/bridge-domains/bridge-domain[bridge-domain-name="v1401"]/bridge-acs/bridge-ac[interface-name="Bundle-Ether1.1401"]/attachment-circuit/statistics
 !
 sensor-group SG_COUNTERS
  sensor-path Cisco-IOS-XR-pfi-im-cmd-oper:interfaces/interface-xr/interface[interface-name='Bundle-Ether1.109']
  sensor-path Cisco-IOS-XR-pfi-im-cmd-oper:interfaces/interface-xr/interface[interface-name='Bundle-Ether1.2600']
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='Bundle-Ether202']/latest/data-rate
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='Bundle-Ether1.2600']/latest/data-rate
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='Bundle-Ether8.2600']/latest/data-rate
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='TenGigE0/3/0/0']/latest/data-rate
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='TenGigE0/3/0/1']/latest/data-rate
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='TenGigE0/3/0/3']/latest/data-rate
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='Bundle-Ether202']/latest/generic-counters
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='Bundle-Ether1.2600']/latest/generic-counters
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='Bundle-Ether8.2600']/latest/generic-counters
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='TenGigE0/3/0/0']/latest/generic-counters
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='TenGigE0/3/0/1']/latest/generic-counters
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='TenGigE0/3/0/3']/latest/generic-counters
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='TenGigE0/3/0/4.2600']/latest/data-rate
  sensor-path Cisco-IOS-XR-infra-statsd-oper:infra-statistics/interfaces/interface[interface-name='TenGigE0/3/0/4.2600']/latest/generic-counters
 !
 subscription SUB5MINS
  sensor-group-id SG5MINS sample-interval 300000
  destination-id PIPELINE1
  source-interface Loopback0
 !
 subscription SUB1MINS_FIA
  sensor-group-id SG_FIA sample-interval 60000
  destination-id PIPELINE1
  source-interface Loopback0
 !
 subscription SUB1MINS_NPU
  sensor-group-id SG_NPU sample-interval 60000
  destination-id PIPELINE1
  source-interface Loopback0
 !
 subscription SUB5MINS_NPU
  sensor-group-id SG_NPU5M sample-interval 300000
  destination-id PIPELINE1
  source-interface Loopback0
 !
 subscription SUB1MINS_OPTICS
  sensor-group-id SG_OPTICS sample-interval 60000
  destination-id PIPELINE2
  source-interface Loopback0
 !
 subscription SUB1MINS_GENERAL
  sensor-group-id SG_GENERAL sample-interval 60000
  destination-id PIPELINE1
  source-interface Loopback0
 !
 subscription SUB1MINS_COUNTERS
  sensor-group-id SG_COUNTERS sample-interval 60000
  destination-id PIPELINE3
  source-interface Loopback0
 !
 subscription SUB1MINS_L2VPN_COUNTERS
  sensor-group-id SG_L2VPN_COUNTERS sample-interval 60000
  destination-id PIPELINE4
  source-interface Loopback0
 !
 ```
