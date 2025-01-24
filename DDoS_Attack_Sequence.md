'''mermaid
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
'''



