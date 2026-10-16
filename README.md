# 🛡️ JARVIS Master — Auditoria Técnica SIPIA / Selo UNICEF

**Ferramenta de Apoio Técnico e Diagnóstico de Infraestrutura de TI para Unidades de Atendimento Socioeducativo e Conselhos Tutelares.**

---

## 📌 Contexto e Necessidade do Projeto

Este projeto foi desenvolvido pela equipe de Suporte de TI da **Secretaria Municipal de Assistência Social (SMAS) de Várzea Grande - MT** para atender com urgência e rigor técnico às exigências da **C.I. Nº 277/SMAS/GAB/VG/2026** e do **Procedimento SIMP nº 016539-006/2025** do Ministério Público do Estado de Mato Grosso (relativo à conformidade do Selo UNICEF).

### A Necessidade
Durante as inspeções e visitas de campo nos Conselhos Tutelares e unidades da rede de proteção social, é necessário avaliar de forma padronizada, rápida e auditável se os computadores da rede municipal possuem as condições técnicas necessárias para operar o **SIPIA (Sistema de Informação para Infância e Adolescência)**. 

A criação desta ferramenta automatizada responde às seguintes necessidades:
1. **Padronização da Coleta:** Evitar diagnósticos manuais e passíveis de falhas em campo.
2. **Conformidade Legal e Ministerial:** Gerar laudos técnicos padronizados para prestação de contas ao Ministério Público e órgãos de controle.
3. **Agilidade em Campo:** Executar testes rápidos de conectividade, acessibilidade ao portal do SIPIA, e capacidade de hardware sem a necessidade de instalar dependências pesadas ou o interpretador Python nas máquinas locais dos conselhos.
4. **Consolidação de Dados:** Permitir a rápida compilação de relatórios por unidade para envio à gestão municipal.

---

## 🚀 Funcionalidades Principais

- **Diagnóstico Automático de Hardware:** Validação de memória RAM, uso de CPU e espaço em disco para verificação de requisitos mínimos.
- **Teste de Conectividade e Rede:** Coleta de IP local, gateway, DNS e checagem de acesso à internet.
- **Auditoria de Acesso ao SIPIA:** Verificação de status HTTP, latência (ping) e acessibilidade ao portal oficial (`sipiact.mdh.gov.br`).
- **Tratamento de Tolerância a Falhas (UTF-8/Encoding):** Código otimizado para rodar em diferentes versões do Windows sem interromper a execução devido a caracteres especiais de console.
- **Geração Multi-Formato de Relatórios:** Exportação instantânea dos resultados em arquivos `.txt`, `.docx` (Word) e `.pdf`.
- **Módulo RAG (Base do Manual SIPIA):** Consulta integrada a diretrizes técnicas, manuais do sistema e documentos normativos locais.
- **Interface Web e CLI:** Possibilidade de execução via linha de comando ou painel web simplificado para visualização local.

---

## 💻 Configuração Mínima do Computador para Acesso ao SIPIA (Web)

Para que os computadores de campo estejam aptos ao acesso e operação da plataforma **SIPIA-CT**, a máquina avaliada deve atender aos seguintes critérios mínimos:

| Componente | Requisito Mínimo Recomendado |
| :--- | :--- |
| **Processador (CPU)** | Dual-Core 1.5 GHz (Intel Celeron, Core i3 ou equivalente AMD) |
| **Memória RAM** | Mínimo de 2 GB (Recomendado 4 GB para melhor desempenho) |
| **Armazenamento** | 10 GB a 20 GB de espaço livre em disco |
| **Navegador Web** | Google Chrome ou Mozilla Firefox atualizados com JavaScript e Cookies ativos |
| **Conexão** | Banda larga estável (mínimo 1 a 2 Mbps por terminal) |

---

## 🛠️ Como Executar em Campo

### Execução Portátil (via Pen Drive / Script)
Não é necessário instalar o Python nos computadores das unidades inspecionadas. O agente pode ser executado diretamente em modo portátil:

1. **Gerar Relatório Automático de Auditoria:**
   ```bash
   python jarvis_master.py --relatorio