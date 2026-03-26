# Simulator Télos – Nível #6

## Modelagem de Objetos e Design Orientado a Objetos

Sejam bem-vindos ao Simulator – Nível #6! Neste nível, você teve a oportunidade de aprender conceitos sobre a programação orientada a objetos, e os princípios de desenvolvimento de jogos. Que tal agora colocar todo esse conhecimento em um projeto mão na massa? 😊

## Contextualização

Você foi convocado a fazer parte de uma equipe que está trabalhando no desenvolvimento de um jogo de aventura em 2D. O projeto está em andamento: parte dos cenários e os personagens principais já foram criados com seus funcionamentos básicos. Porém, surge um problema: os inimigos do jogo, essenciais para criar uma experiência desafiadora e divertida, não estão funcionando como esperado.

Os inimigos atualmente são previsíveis. Eles seguem padrões de movimento simples, sem inteligência ou complexidade, tornando o jogo fácil e sem graça. Percebemos uma falta de desafios e variedade nos confrontos.

É hora de agir. O sucesso desse jogo depende de uma experiência de combate interessante. O foco está em criar uma classe inimigo que traga mais dinâimismo aos cenários.

## Descrição

Seu objetivo como desenvolvedor é criar uma classe pai chamada **Enemy**, que conterá atributos e métodos comuns a todos os inimigos. Subclasses específicas de inimigos herdarão dessa classe base e poderão implementar habilidades únicas que adicionam variedade e complexidade ao comportamento de cada tipo de inimigo. O sistema deve ser preferencialmente desenvolvido em **C#** e deve seguir o paradigma de Programação Orientada a Objetos.

---

## 1. Classe Inimigo (Base)

**Atributos:**
- `health`
- `velocity`

**Métodos:**
- `receiveDamage(damage)`: Reduz a saúde do inimigo.
- `displayStatus()`: Exibe os atributos atuais do inimigo.
- `move()`: Movimenta o inimigo pelo cenário.
- `isDead()`: Verifica se a saúde do inimigo chegou a zero.

---

## 2. Subclasses de Inimigo

Cada subclasse representará um tipo específico de inimigo com habilidades distintas. Implementar **pelo menos 2 subclasses**, podendo utilizar alguma das sugestões abaixo, mas não somente:

### ■ EnemyWithAttack
- **Descrição:** Esse inimigo consegue atacar o personagem principal.
- **Atributos adicionais:** `attack`
- **Método especial:** `attackPlayer(damage)` - executa o ataque.

### ■ FlyingEnemy
- **Descrição:** Esse inimigo voa.
- **Atributos adicionais:** `altitude`
- **Método especial:** `fly()` - Executa o voo.

### ■ JumpingEnemy
- **Descrição:** Esse inimigo pula.
- **Atributos adicionais:** `altitude`
- **Método especial:** `jump()` - Executa o salto.

### ■ StealthyEnemy
- **Descrição:** Esse inimigo fica invisível.
- **Método especial:** `invisible()` - Executa a invisibilidade.

---

## 3. Critérios de Avaliação

### 1. Encapsulamento
- **Critério:** Atributos como `health` devem ser acessíveis apenas através de métodos apropriados (getters/setters) ou diretamente, se for permitido pelo design.
- **Aceitação:** Não deve ser possível modificar atributos de forma direta e indiscriminada, a menos que isso faça parte do design da classe. Métodos como `receiveDamage()` e `attack()` devem ser usados para modificar o estado do inimigo.
- **Exemplo:** O método `receiveDamage(damage)` é responsável por modificar a saúde do inimigo.

### 2. Herança
- **Critério:** A classe base `Enemy` deve ser projetada para que subclasses possam herdar e sobrescrever métodos conforme necessário.
- **Aceitação:** Deve ser possível criar subclasses, como `JumpingEnemy`, etc., que herdam métodos da classe `Enemy` e os alteram quando necessário.
- **Exemplo:** O método `move()` pode ser sobrescrito em uma subclasse, como `JumpingEnemy`, que adiciona a funcionalidade de pular.

### 3. Polimorfismo
- **Critério:** O polimorfismo deve ser aplicado para permitir que diferentes tipos de inimigos possam ser tratados de maneira genérica, mas com comportamentos específicos.
- **Aceitação:** O método `move()` deve poder ser chamado para qualquer instância de `Enemy` ou suas subclasses, mas o comportamento pode ser diferente (ex: o `FlyingEnemy` voa).
- **Exemplo:** Mesmo que o tipo exato de `Enemy` não seja conhecido, métodos como `attack()` e `move()` devem funcionar conforme o tipo específico de inimigo.

### 4. Abstração
- **Critério:** A classe `Enemy` deve abstrair comportamentos comuns para todos os inimigos, como mover, receber dano e verificar se está morto, enquanto os detalhes específicos são implementados nas subclasses.
- **Aceitação:** A classe `Enemy` não deve conter implementações de habilidades especiais (ex: esquivar-se, regenerar), mas sim apenas as ações básicas que todos os inimigos compartilham.
- **Exemplo:** A classe `Enemy` contém o método `receiveDamage()`, mas as subclasses podem adicionar comportamentos específicos, como o `RegenerativeEnemy` regenerar vida após determinado tempo.

---

## 5. Desafio Bônus! (OPCIONAL)

- Criar um **boss**! O boss pode ser uma classe especializada que herda da classe base `Enemy`, mas com habilidades especiais e mecânicas que o diferenciam de inimigos normais.
- **Sugestão:** Implementar um método especial `infuriate()`, em que o boss muda completamente suas habilidades e ataques quando a saúde cai abaixo de um certo valor.
- Ao invés de o boss ser apenas uma subclasse de `Enemy`, você pode usar **composição** para adicionar habilidades especiais como regeneração, invocação de lacaios, ou até manipulação do ambiente.
- **Critério:** O céu é o limite!
- **Aceitação:** Conceituação e organização funcional.

---

## Tempo de desenvolvimento

Espera-se que a equipe seja capaz de desenvolver esta aplicação em um prazo máximo de 4 dias (4 horas de dedicação por dia). Sugere-se o seguinte cronograma de desenvolvimento (que pode ser modificado livremente pela equipe):

- **Dia 1:** 2h - Desenvolvimento da classe base. 2h - Desenvolvimento da subclasse 1.
- **Dia 2:** 2h - Desenvolvimento da subclasse 1. 2h - Desenvolvimento da subclasse 2.
- **Dia 3:** 2h - Desenvolvimento da subclasse 2. 2h - Testes manuais.
- **Dia 4:** 4h - Tarefa bônus (opcional), revisão, ajustes e testes manuais da aplicação.

---

## Avaliação

A avaliação desta atividade levará em consideração os critérios a seguir:

1. Os alunos devem demonstrar que conseguiram utilizar a lógica de programação orientada a objetos para resolver o problema de maneira efetiva com uma aplicação computacional.
2. Os alunos devem ser capazes de realizar a interação do usuário com a aplicação utilizando as funções de entrada e saída da Godot Engine.
3. Os alunos devem dividir adequadamente as funcionalidades em métodos separados.
4. Os alunos devem ser capazes de solucionar os problemas computacionais de maneira criativa.

---

## Competências avaliadas

Para o desenvolvimento deste Simulator, são necessárias aos alunos as seguintes competências:

- Uso dos pilares da programação orientada a objetos:
  - Abstração
  - Encapsulamento
  - Herança
  - Polimorfismo
- Interações com a Godot Engine