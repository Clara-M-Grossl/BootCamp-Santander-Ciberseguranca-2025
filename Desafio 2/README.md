# Desafio 2: Simulação de Malware para Estudo e Defesa em Python

**Projeto desenvolvido como parte do Santander Bootcamp Cibersegurança 2025, em parceria com a Digital Innovation One (DIO).**

---

### O Que é Este Projeto?

Este repositório é o resultado do **Desafio Prático 2** do nosso Bootcamp. O objetivo principal foi **entender e simular** o funcionamento de duas ameaças digitais comuns – **Ransomware** e **Keylogger** – usando a linguagem **Python**.

 **Lembrete:** Todo o código aqui é **EXCLUSIVAMENTE EDUCACIONAL**. Os testes foram feitos em um ambiente 100% controlado e seguro, com arquivos fictícios. Usar estas técnicas de forma maliciosa é ilegal e antiético.

---

### Ransomware

Nesta seção, simulamos o ciclo completo de um ataque de Ransomware: criptografar arquivos e depois recuperá-los. O foco é entender a **Criptografia Simétrica** na prática.

#### Arquivos Principais

| Arquivo | O que ele faz | Conceito-Chave |
| :--- | :--- | :--- |
| `ransomware/ransomware.py` | Criptografa os arquivos na pasta `test_files/` e cria a mensagem simulada de "resgate" (`LEIA ISSO.txt`). | **Criptografia Simétrica** (`cryptography.fernet`) |
| `ransomware/descriptografar.py` | Usa a chave (`chave.key`) para reverter o processo e restaurar os arquivos originais. | **Recuperação de Dados** |

---

### Keylogger

Aqui, estudamos como um Keylogger funciona, capturando as teclas digitadas para entender como detectá-lo e nos proteger.

#### Arquivos Principais

| Arquivo | O que ele faz | Biblioteca |
| :--- | :--- | :--- |
| `keylogger/keylogger.py` | Rastreia eventos do teclado e salva o log em `log.txt` (uso apenas em ambiente de teste). | **`pynput`** |
| `keylogger/keylogger_email.py` | Demonstração **conceitual** de como o log poderia ser enviado (exfiltração) em um ambiente controlado. | **`smtplib`** |

---

### Defesa e Boas Práticas

A melhor parte deste desafio é a reflexão sobre a defesa. Ninguém quer ser vítima! Aqui estão as lições principais para a proteção:

| Ameaça | Medida de Prevenção |
| :--- | :--- |
| **Ransomware** | **Backup 3-2-1:** A regra de ouro! Mantenha 3 cópias dos dados, em 2 mídias diferentes, sendo 1 **offline/imutável**. |
| **Keylogger** | **Antivírus/EDR** com análise comportamental (para detectar a tentativa de "ouvir" o teclado). Uso de **Gerenciadores de Senhas**. |
| **Geral** | **Atualizações de Segurança** (patches) em dia e **Conscientização** (saber identificar um email de *phishing*). |

---
