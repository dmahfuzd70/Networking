### Router Configuration    
    ->en
    ->#conf t
    ->(config)#int fa 0/0
    ->(config-if)#ip add 10.0.0.0 255.0.0.0(FastEhternet interface ip add)
    ->(config-if)#no shut
    ->(config-if)#int s 0/0/0(Serial interface)
    ->(config-if)#ip add 40.0.0.1 255.0.0.0
    ->(config-if)#clock rate 64000
    ->(config-if)#no shut


### Route config:

    ->(config-if)#ip route 50.0.0.0(Desire Network) 255.0.0.0 40.0.0.2(Via)

### Default Routing:
    ->(config-if)#ip route 0.0.0.0(Desire Network) 0.0.0.0 40.0.0.2(Via)

    ->#sh ip route(To check Route status)
