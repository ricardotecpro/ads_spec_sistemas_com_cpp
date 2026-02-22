# Projeto 14 - Chat via Terminal (Go/Rust) 🦀🐹

**Objetivo**: Concorrência e Canais.

## O Desafio (Go)
1.  Crie uma função `servidor(canal)` que recebe mensagens e imprime "Servidor recebeu: X".
2.  Crie 3 Goroutines `clientes`, cada uma enviando 5 mensagens para o canal.
3.  Faça o servidor processar todas concorrentemente.

## O Desafio (Rust - Alternativo)
1.  Crie um programa que use Threads para contar até 10 milhões.
2.  Divida o trabalho em 4 threads.
3.  Use um `Mutex` ou canais para somar o total final com segurança.