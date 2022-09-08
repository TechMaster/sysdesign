---
title: "1.3 Mermaid"
date: 2022-08-07T17:38:18+07:00
draft: false
---

{{< mermaid class="text-center">}}
sequenceDiagram
    Alice->>Bob: Hello Bob, how are you?
    alt is sick
        Bob->>Alice: Not so good :(
    else is well
        Bob->>Alice: Feeling fresh like a daisy
    end
    opt Extra response
        Bob->>Alice: Thanks for asking
    end
{{< /mermaid >}}

{{< mermaid class="text-center">}}
flowchart LR
    id1[(Database)]
    id2([This is the text in the box])
    id3{{This is the text in the box}}
    id1-->|connect|id2
    id2-->|query|id3
    id3-->id1
{{< /mermaid >}}

{{< mermaid class="text-center">}}
flowchart TB
    c1-->a2
    subgraph one
    a1-->a2
    end
    subgraph two
    b1-->b2
    end
    subgraph three
    c1-->c2
    end
{{< /mermaid >}}

{{< mermaid class="text-center">}}
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra

    class Animal{
        +int age
        +String gender
        +isMammal()
        +mate()
    }
    
    class Duck{
        +String beakColor
        +swim()
        +quack()
    }
    class Fish{
        -int sizeInFeet
        -canEat()
    }
    class Zebra{
        +bool is_wild
        +run()
    }
{{< /mermaid >}}

{{< mermaid class="text-center">}}
erDiagram
    CAR ||--o{ NAMED-DRIVER : allows
    CAR {
        string allowedDriver FK "The license of the allowed driver"
        string registrationNumber
        string make
        string model
    }
    PERSON ||--o{ NAMED-DRIVER : is
    PERSON {
        string driversLicense PK "The license #"
        string firstName
        string lastName
        int age
    }
{{< /mermaid >}}