```
classDiagram
    class Animal {
        - nome: string
        - idade: int
        + emitirSom(): void
    }

    class Cachorro {
        + corPelo: string
        + latir(): void
    }

    class Gato {
        + corPelo: string
        + miar(): void
    }

    class Passaro {
        + tamanhoAsa: float
        + voar(): void
    }

    class AnimalMarinho {
        - profundidadeMaxima: int
        + nadar(): void
    }

    class Baleia {
        + comprimento: float
        + emitirSom(): void
    }

    Animal <|-- Cachorro
    Animal <|-- Gato
    Animal <|-- Passaro
    Animal <|-- AnimalMarinho
    AnimalMarinho <|-- Baleia
```
