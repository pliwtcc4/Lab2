```mermaid
sequenceDiagram
    participant Attacker
    participant Botnet
    participant WebServer
    participant Firewall

    Attacker->>Botnet: Sends commands to attack
    Botnet->>WebServer: Sends many HTTP requests
    Botnet->>WebServer: Sends many HTTP requests
    Botnet->>WebServer: Sends many HTTP requests
    Botnet->>WebServer: Sends many HTTP requests
    Botnet->>WebServer: Sends many HTTP requests
    WebServer->>Firewall: Asks for help to block traffic
    Firewall->>WebServer: Tries to filter traffic
    WebServer->>Firewall: Server overload (too much traffic)
    Firewall->>WebServer: Tries to block extra traffic
    Note over Firewall: Firewall tries blocking IPs

    %% Highlight IP blocking action
    Firewall-->>Firewall: Block bad IPs (Botnet)
    Firewall->>WebServer: IP blocking applied

    Note right of WebServer: Web server becomes unresponsive due to too much traffic
```
1. The attacker must create a Botnet using several compromised devices that the attacker can control. When the attacker has created the Botnet and selected a target they will then send a command to the Botnet to attack the Webserver. 
2. The Botnet executes the command to attack the Webserver by flooding it with a large amount of requests.  
3. The Webserver tries to respond to the large number of requests, but is overwhelmed and is now uncapable of responding to real requests. 
4. The Firewall may detect an unusually high amount of traffic and attempt to intervene by blocking IP addresses. Success varies based on type of DDoS attack.    




