# Aula 14 - Gerenciamento de Memória 🧠

Nesta aula, aprenderemos como o C++ Moderno resolve o problema clássico de vazamentos de memória usando **Smart Pointers** e o conceito de **RAII**.

---

## 💎 O Conceito de RAII

**RAII** (*Resource Acquisition Is Initialization*) é o pilar do C++. Diz que os recursos (memória, arquivos, conexões) devem ser atrelados à vida útil de um objeto. Quando o objeto morre (sai de escopo), o recurso é liberado automaticamente pelo destrutor.

---

## 🧠 Smart Pointers (Ponteiros Inteligentes)

Desde o C++11, raramente usamos `new` e `delete` manualmente. Usamos Smart Pointers que gerenciam a memória sozinhos.

### 1. `std::unique_ptr`
- Representa posse **exclusiva**.
- Não pode ser copiado, apenas movido.
- Libera a memória assim que sai de escopo.
```cpp
#include <memory>
std::unique_ptr<int> ptr = std::make_unique<int>(10);
```

### 2. `std::shared_ptr`
- Permite posse **compartilhada**.
- Usa um contador de referências. A memória só é liberada quando o último `shared_ptr` apontando para ela for destruído.
```cpp
std::shared_ptr<int> s1 = std::make_shared<int>(20);
std::shared_ptr<int> s2 = s1; // Agora dois apontam para o mesmo lugar
```

---

## 🔄 Gerenciamento de Memória Dinâmica (O jeito antigo vs novo)

| Antigo (`new/delete`) | Novo (Smart Pointers) |
| :--- | :--- |
| Propenso a erros (esquecer delete) | Automático e seguro |
| Difícil de rastrear posse | Posse clara e definida |
| Risco de *Dangling Pointers* | Reduzido drasticamente |

---

## 💡 Quando usar cada um?

!!! tip "Unique por Padrão"
    Use `unique_ptr` em 90% dos casos. Ele não tem custo de performance em relação a um ponteiro comum.

!!! warning "Shared Pointers"
    Evite `shared_ptr` se houver possibilidade de **Ciclos de Referência** (A aponta para B e B aponta para A). Nesses casos, a memória nunca será liberada. Para isso, existe o `std::weak_ptr`.

---

## 💻 Exemplo Prático: Fábrica de Objetos Segura

```cpp
#include <iostream>
#include <memory>
#include <string>

class Recurso {
public:
    Recurso() { std::cout << "Recurso Alocado!" << std::endl; }
    ~Recurso() { std::cout << "Recurso Liberado Automaticamente!" << std::endl; }
    void usar() { std::cout << "Usando o recurso..." << std::endl; }
};

int main() {
    {
        std::unique_ptr<Recurso> res = std::make_unique<Recurso>();
        res->usar();
    } // O recurso é liberado AQUI, sem necessidade de delete

    std::cout << "Fim do programa." << std::endl;
    return 0;
}
```

---

## 📝 Exercício de Fixação

1. **Unique**: Aloque dinamicamente uma classe `Arquivo` usando `unique_ptr`.
2. **Shared**: Crie dois `shared_ptr` que apontem para o mesmo objeto e imprima o `use_count()`.
3. **Desafio**: Tente "mover" um `unique_ptr` de uma variável para outra usando `std::move()`.

---

## 🚀 Mini-Projeto da Aula

**Gerenciador de Documentos**:
Crie um sistema onde você pode adicionar "Documentos" a uma lista. Use `std::vector<std::shared_ptr<Documento>>`. Demonstre que, mesmo ao remover um documento da lista, ele só é destruído se não houver mais nenhum outro `shared_ptr` segurando-o em outra parte do programa.