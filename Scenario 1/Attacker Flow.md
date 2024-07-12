  ```mermaid
  sequenceDiagram
    participant Attacker
    participant Delta Emma
    participant CnCServer
    participant BackendServer
    participant User

    activate Attacker
    Attacker->>DeltaEmmaHealthApp: Identify Delta Emma app
    DeltaEmmaHealthApp->>Attacker: Application identified
    deactivate Attacker

    activate Attacker
    Attacker->>DeltaEmmaHealthApp: Craft exploit for known vulnerabilities
    DeltaEmmaHealthApp->>Attacker: Exploit crafted
    deactivate Attacker

    activate Attacker
    Attacker->>DeltaEmmaHealthApp: Deploy phishing campaign targeting app users
    DeltaEmmaHealthApp->>User: Phishing email sent
    activate User
    User->>DeltaEmmaHealthApp: Clicks on malicious link/download attachment
    DeltaEmmaHealthApp->>User: Malware downloaded
    deactivate User
    deactivate Attacker

    activate Attacker
    Attacker->>DeltaEmmaHealthApp: Trick users into downloading malware
    DeltaEmmaHealthApp->>BackendServer: Malicious payload executed
    BackendServer->>CnCServer: Communication established
    CnCServer->>BackendServer: Commands issued
    BackendServer->>CnCServer: Actions performed
    deactivate Attacker
