```mermaid
stateDiagram-v2
    [*] --> Pendente : Abrir chamado
    Pendente --> EmAndamento : Técnico assume
    EmAndamento --> AguardandoPeca : Falta material
    AguardandoPeca --> EmAndamento : Peça chegou
    EmAndamento --> Concluido : Serviço finalizado
    Concluido --> [*]

    Pendente --> Cancelado : Solicitação cancelada
    Cancelado --> [*]
```
