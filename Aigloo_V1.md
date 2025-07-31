# Aigloo Build
<img width="947" height="511" alt="image" src="https://github.com/user-attachments/assets/57ecd38a-9861-4c47-a215-62ada1fa512b" />
<img width="686" height="724" alt="image" src="https://github.com/user-attachments/assets/6679b953-3fe1-41cf-95b9-2bbb21126a5a" />
<img width="1006" height="604" alt="image" src="https://github.com/user-attachments/assets/1b55648c-2797-4104-ac44-b6df7f35453f" />
<img width="465" height="637" alt="image" src="https://github.com/user-attachments/assets/f71c01b9-1529-4895-a8f3-3092532e46a9" />


## System Capabilities
### Compute
**Heavy compute/AI inference node**:
> MacStudio M3 Ultra | 256gb Unified Memory | 28 core CPU | 60 core GPU | 32 Core Neural Engine | 819 GB/s Memory Bandwith | 1TB SSD

**Moderate compute/AI inference node**:
> MacBook Pro M1 Max | 64gb Unified Memory | 10 Core CPU | 32 Core GPU | 1TB SSD

**Orchestration/Dispatch node**:
> MacMini M4 | 16gb Unified Memory | 10 Core GPU | 10 Core CPU | 256GB SSD
>> SanDisk 2TB Extreme Portable SSD - Up to 1050MB/s, USB-C, USB 3.2 Gen 2

**Thin Client**:
> MacBook Air M4 | 16gb Unified Memory | 10 Core GPU | 10 Core CPU | 256GB SSD

### Toplology
```
                            ================
                            Aigloo Toplology
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx


[Solar Power]    [Grid]                                  [Internet]
    |--------------|                                          |
    |                                                         |
    V                                                         |
[Battery]                                                     |   [WAP]
     |---------------|--------------------|-----------------| |     A                        
     |               |                    |                 | |     |
     V               V                    V                 V V     |
[MacStudio]      [MacMini]          [MacBook Pro]          [Ethernet Switch]
  |   |           A | | A               |     |                     |
  |  [TB 5 Out]---| | | |-------[TB 4 Out]    |                     |
  |                 V |                       V                     |
  |              [SSD]|                     [1GbE]<-----------------|
  |                   V                                             |
  |                 [1GbE]<-----------------------------------------|
  V                                                                 | 
[10GbE]<------------------------------------------------------------|                      
```

### Power
- Battery: EcoFlow River 2 | 768 watt hours
- Solar: EF ECOFLOW 160 Watt Portable Solar Panel | N-TYPE solar technology achieves 25% solar conversion efficiency.
  
### Networking
- ThunderBolt 4 mesh network from MacMini to MacStudio and MacBook Pro
- TP-Link, 1GbE, 8 port, managed etherenet switch
  - Internet IN for at home use
  - WAP OUT for off grid network node
- TP-Link Omada Access Point
### Peripherals
- 6x 80mm cooling fans (4 intake x 2 exhaust)
- ThermPro wirelss thermometer

## Performance
### AI Capabilities
- MacStudio can provide inference for one 250b parameter models or multiple 30b-70b models simultaneously.
- MacBook Pro can provide inference for on 30b-70b model or multiple 2b-8b (nano size) models simultaneously.

### Off Grid Capabilities
- Design allows for intelligent power scaling during off grid use.
  - SSH from MacBook Air $\rightarrow$ MacMini. ThunderBolt 4 from MacMini $\rightarrow$ MacBookPro. This chain optimizes power use for general tasks.
  - MacStudio can be used intermittently for periods of heavy inference/compute.
- Full system can run continuosuly for ~3hrs on only the EcoFlow River 2
- On a sunny day, a solar panel removes all power constraints.

### Cooling
- Strategic fan and machine placement to promote cold air intake and heat exhaust.
- Insulative thermal mass of the cooler offers a stable envelope that is less effected ambient temperature.
- Running max AI inference on the MacStudio with the `Aigloo` lid closed reaches an internal temperature of 93 degrees, 60% MacStudio fan speed, and ~150 degree hottest CPU and GPU cores respectively.
