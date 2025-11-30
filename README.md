# 🏭 Sistema de Logística – Banco de Dados Relacional (Porte Médio)

Este repositório contém um banco de dados relacional completo, projetado para simular o funcionamento de um **Sistema de Logística** de porte médio, com foco em operações reais de transporte rodoviário, rastreamento de entregas, controle de cargas, gestão de motoristas, clientes, veículos e pagamentos.

O cenário foi construído com base em práticas reais do setor logístico e serve como fundamento para **exercícios acadêmicos**, **aprendizado de SQL**, **modelagem relacional**, **testes de SGBD** e **desenvolvimento de sistemas**.

---

## 🚀 Objetivos do Projeto

- Criar um banco de dados relacional funcional e coerente
- Simular operações reais de empresas de logística
- Permitir análises operacionais, financeiras e gerenciais
- Servir como base para estudos acadêmicos
- Demonstrar boas práticas de modelagem (DER + normalização)

---

## 🧱 Tecnologias Utilizadas

- **MySQL 8.x**  
- **Modelo Relacional (3FN)**  
- **SQL (DDL + DML)**  
- Compatível com:
  - MySQL Workbench  
  - DBeaver  
  - phpMyAdmin  
  - DB-Fiddle (MySQL 8.0)

---

## 🗂 Estrutura do Banco de Dados

O sistema contém 15 tabelas classificadas por área:

### 🔐 **1. Segurança e Acesso**
| Tabela | Função |
|--------|--------|
| `perfil_acesso` | Perfis do sistema (Admin, Financeiro, etc.) |
| `usuario_sistema` | Usuários internos do sistema |

---

### 🏘 **2. Localização**
| Tabela | Função |
|--------|--------|
| `cidade` | Base de cidades |
| `endereco` | Endereços de clientes, motoristas e rotas |

---

### 📋 **3. Cadastros**
| Tabela | Função |
|--------|--------|
| `cliente` | Clientes PF e PJ |
| `motorista` | Motoristas cadastrados |
| `tipo_veiculo` | Tipos de veículos |
| `veiculo` | Frota da empresa |

---

### 🚚 **4. Operação Logística**
| Tabela | Função |
|--------|--------|
| `status_entrega` | Status da entrega (pendente, em trânsito, etc.) |
| `rota` | Rotas com origem/destino |
| `entrega` | Tabela principal de fretes |
| `carga` | Itens transportados |
| `ocorrencia_entrega` | Avarias, atrasos, devoluções |

---

### 💰 **5. Financeiro e Comunicação**
| Tabela | Função |
|--------|--------|
| `pagamento` | Pagamentos do frete |
| `notificacao` | Notificações enviadas a clientes/usuários |

---

## 🧩 Visão Geral do Modelo (DER)

O DER completo do sistema pode ser estruturado da seguinte forma:

- Relacionamentos 1:N entre:
  - Cliente → Entrega  
  - Motorista → Entrega  
  - Veículo → Entrega  
  - Entrega → Carga  
  - Entrega → Ocorrência  
  - Entrega → Pagamento  

- Relacionamentos N:1 para:
  - Entrega → Rota  
  - Rota → Endereços (origem/destino)

---

## 📌 Arquivo SQL Completo

O script contendo o **banco de dados completo** (DDL + DML + 100+ dados reais) está no arquivo:

