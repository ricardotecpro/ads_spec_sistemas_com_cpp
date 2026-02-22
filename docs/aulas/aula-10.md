# Aula 10 - Construtores e Destrutores 🏗️

Nesta aula, aprenderemos como gerenciar o ciclo de vida de um objeto: desde o seu nascimento (construção) até o seu fim (destruição).

---

## 🏗️ Construtores

Um **Construtor** é um método especial que é chamado automaticamente quando criamos um objeto. Ele tem o **mesmo nome da classe** e não possui tipo de retorno.

### Construtor Padrão (Default)
Iniciado sem parâmetros.
```cpp
class Robo {
public:
    Robo() { std::cout << "Robo ativado!" << std::endl; }
};
```

### Construtor Parametrizado
Iniciado com valores específicos.
```cpp
class Pessoa {
private:
    std::string nome;
public:
    Pessoa(std::string n) : nome(n) {} // Lista de Inicialização
};
```

---

## 💣 Destrutor

O **Destrutor** é chamado quando o objeto sai de escopo ou é deletado. Seu nome começa com um til (`~`). É o lugar perfeito para liberar memória ou fechar arquivos.

```cpp
class BancoDados {
public:
    ~BancoDados() { std::cout << "Conexão encerrada com segurança." << std::endl; }
};
```

---

## 📜 Regra dos Três (Rule of Three)

No C++ clássico, se você precisar definir um dos três, provavelmente precisará definir todos para evitar bugs de memória:
1. **Destrutor**
2. **Construtor de Cópia**
3. **Operador de Atribuição**

---

## 🧠 Lista de Inicialização

!!! tip "Performance"
    Use sempre a lista de inicialização (`: atrib(valor)`) em vez de atribuir valores dentro do corpo do construtor. Isso é mais eficiente pois evita a criação de um objeto temporário vazio.

!!! info "Sobrecarga"
    Você pode ter vários construtores para a mesma classe, permitindo criar objetos de diferentes formas.

---

## 💻 Exemplo Prático: Gerenciador de Log

```cpp
#include <iostream>
#include <string>

class Logger {
private:
    std::string prefixo;
public:
    // Construtor com valor padrão
    Logger(std::string p = "LOG") : prefixo(p) {
        std::cout << "[" << prefixo << "] Logger Iniciado." << std::endl;
    }

    // Destrutor
    ~Logger() {
        std::cout << "[" << prefixo << "] Logger Finalizado." << std::endl;
    }

    void log(std::string mensagem) {
        std::cout << "[" << prefixo << "] " << mensagem << std::endl;
    }
};

int main() {
    {
        Logger meuLog("SISTEMA");
        meuLog.log("Iniciando processamento...");
    } // O Logger é destruído AQUI ao sair das chaves
    
    std::cout << "Fim da execução." << std::endl;
    return 0;
}
```

---

## 📝 Exercício de Fixação

1. **Construtor**: Crie uma classe `Carro` onde o construtor peça a marca e o ano.
2. **Destrutor**: Adicione um destrutor à classe `Carro` que imprima "Carro [Marca] enviado para o desmanche".
3. **Desafio**: Implemente uma classe `Buffer` que aloque dinamicamente um array no construtor e use o destrutor para garantir que a memória seja liberada.

---

## 🚀 Mini-Projeto da Aula

**Sistema de Sessão de Usuário**:
Crie uma classe `Sessao` que armazene o ID do usuário. O construtor deve registrar o horário de login (pode ser um texto simples) e o destrutor deve registrar o horário de logout. Simule múltiplos logins no `main` usando blocos `{}` para ver os objetos sendo criados e destruídos.