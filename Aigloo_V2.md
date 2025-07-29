[DRAFT]

```
{-Satellite Backhaul-}
         |
         | 
   |     |
 - o -   |
   |     |
         |
 SOLAR   |   5G Transmit  ----- GAA -----/ /----- GAA ------|
 / / /   |       =                                          |
   |     |       |                                          | 
   |     |       |                                          |
[ Aigloo DataCenter ]                                       |
         |       |                                          |           [MacMini M4 Hypervisor]   
         |       |                                     [iPhone SE] -------|  |  |
         |       |--------------|                                            |  |
         |                      |                        [Switch] -----------|  |
[ MacStudio M3 Ultra ]          |                            |                  |
     |              |           |                            |                [SSD]
     |           [10GbE] --- [Switch]                        |
     |                                      [ ISP ] --- [Router/Modem]
[DGX Spark]                                               |  |  |
                                                          |  |  |--------------------------|   
                                                          |  |------------|                |
                                                          |               |                | 
                                                   [Thin Client 1]  [Thin Client 2]  [Thin Client 3]
```
