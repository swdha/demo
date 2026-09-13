graph TD
    N((Input: N)) --> C1((Copy))
    One((Input: 1)) --> C2((Copy))
    
    C1 --> Rel((> 0))
    C1 --> BR1((BR))
    
    C2 --> BR2((BR))
    
    Rel -- Bool --> BR1
    Rel -- Bool --> BR2
    
    BR1 -- F --> Sink1((Sink))
    BR2 -- F --> Out((OUT))
    
    BR1 -- T --> C3((Copy))
    BR2 -- T --> Mul(( * ))
    
    C3 --> Dec((DEC))
    C3 --> Mul
    
    Dec --> C1
    Mul --> C2
