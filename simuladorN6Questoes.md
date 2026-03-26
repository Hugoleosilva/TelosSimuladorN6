# Simulador POO - Nível 6

## 1. Identificação de atributos e métodos

Considere o seguinte trecho de código:

class_name Enemy  
var health: int  
var velocity: int  
var direction: String  

func move():  
func jump():  

Quais são os atributos e quais são os métodos dessa classe? 

Atributos:
- health
- velocity
- direction

Métodos:
- move()
- jump()

Explicação: Atributos são variáveis que armazenam os dados (estado) de um objeto. Métodos são funções definidas na classe que representam as ações ou comportamentos que o objeto pode executar.

---

## 2. Conceito de Classe

O que é uma classe em Programação Orientada a Objetos?

A) Um objeto específico na memória  
**B) Um modelo que define atributos e comportamentos**  
C) Um tipo de variável  
D) Um método especial  

Explicação: **B.** Uma classe é um modelo (ou molde) usado para criar objetos. Ela define quais atributos (dados) e métodos (comportamentos) esses objetos terão.

---

## 3. Análise de acesso (instâncias diferentes)

Observe o código abaixo:

Enemy e1 = new Enemy();  
Enemy e2 = new Enemy();  

e1.health = 50;  

Qual será o valor de e2.health? **100**

Explicação: Cada objeto criado com "new" é uma instância independente na memória. Alterar um atributo de um objeto não afeta outro, mesmo sendo da mesma classe.

---

## 4. Acesso a atributo privado

Considere:

class Enemy {  
    private int _health = 100;  
}  

Enemy e = new Enemy();  

Qual será o valor de e._health? **Erro de acesso (não é possível acessar diretamente)**

Explicação: Atributos privados não podem ser acessados diretamente fora da classe. Esse é um princípio de encapsulamento, que protege os dados e exige o uso de métodos públicos (como getters) para acesso controlado.

---

## 5. Herança

Considere o código:

class Enemy {  
    int health = 100;  

    void display() {  
        System.out.println("Enemy com vida: " + health);  
    }  
}  

class BossEnemy extends Enemy {  
    int specialAttack = 50;  
}  

Por que a chamada boss.display() funciona?  
**Porque BossEnemy herda de Enemy**

Explicação: A herança permite que uma classe filha reutilize atributos e métodos da classe pai. Por isso, um objeto da classe filha pode acessar métodos definidos na classe pai.

---

## 6. Polimorfismo

Considere o código:

class Enemy {  
    void move() {  
        System.out.println("Movendo");  
    }  
}  

class JumpingEnemy extends Enemy {  
    @Override  
    void move() {  
        System.out.println("Pulando");  
    }  
}  

Enemy e = new JumpingEnemy();  
e.move();  

O que será exibido? **Pulando**

Explicação: No polimorfismo, o método executado depende do tipo real do objeto em tempo de execução. Mesmo que a variável seja do tipo da classe pai, o método sobrescrito na classe filha será chamado.

---

## 7. Verdadeiro ou Falso

( V ) Métodos podem alterar atributos  
( F ) Métodos não podem receber parâmetros  
( V ) Métodos representam comportamentos  

Explicação: Métodos representam comportamentos de uma classe. Eles podem modificar atributos do objeto e também podem receber parâmetros, que são usados para passar dados necessários para a execução do método.

---

## 8. Diferença entre objetos

Enemy e1 = new Enemy();  
Enemy e2 = new Enemy();  

e1 e e2 são o mesmo objeto? **Não**

Explicação: Mesmo sendo da mesma classe, cada objeto criado é uma instância distinta na memória. Portanto, eles não são o mesmo objeto.