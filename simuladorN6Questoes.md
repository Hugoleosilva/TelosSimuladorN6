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

---

## 2. Conceito de Classe

O que é uma classe em Programação Orientada a Objetos?

A) Um objeto específico na memória  
B) Um modelo que define atributos e comportamentos  
C) Um tipo de variável  
D) Um método especial  

---

## 3. Análise de acesso (instâncias diferentes)

Observe o código abaixo:

Enemy e1 = new Enemy();  
Enemy e2 = new Enemy();  

e1.health = 50;  

Qual será o valor de e2.health?

---

## 4. Acesso a atributo privado

Considere:

class Enemy {  
    private int _health = 100;  
}  

Enemy e = new Enemy();  

Qual será o valor de e._health?

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

O que será exibido?

---

## 7. Verdadeiro ou Falso

( ) Métodos podem alterar atributos  
( ) Métodos não podem receber parâmetros  
( ) Métodos representam comportamentos  

---

## 8. Diferença entre objetos

Enemy e1 = new Enemy();  
Enemy e2 = new Enemy();  

e1 e e2 são o mesmo objeto?