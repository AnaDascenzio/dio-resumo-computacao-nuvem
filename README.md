# ✨ Princípios Básicos da Computação em Nuvem

## 💰 CapEx vs OpEx

### CapEx (Capital Expenditure - Despesa de Capital)
- Investimento **inicial alto** em infraestrutura (servidores, redes, data centers).
- Recurso é comprado e **pertence à empresa**.
- **Exemplo**: Comprar servidores físicos para um data center próprio.

### OpEx (Operational Expenditure - Despesa Operacional)
- Modelo de **pagamento sob demanda** (pay-as-you-go).
- Infraestrutura é **alugada**, não há aquisição de ativos.
- Mais **flexível e escalável**.
- **Exemplo**: Usar serviços da AWS ou Azure e pagar mensalmente conforme o uso.

---

## ☁️ Modelos de Nuvem

### 🔓 Nuvem Pública
- Infraestrutura **compartilhada** entre múltiplos usuários.
- Mantida por provedores como AWS, Azure, Google Cloud.
- **Alta escalabilidade**, **baixo custo inicial**, **menos controle direto**.
- Ideal para: startups, testes, serviços web, etc.

### 🔒 Nuvem Privada
- Infraestrutura **dedicada a uma única organização**.
- Pode ser local (on-premises) ou hospedada por terceiros.
- **Maior controle**, **segurança reforçada**, mas **custo mais alto**.
- Ideal para: instituições financeiras, órgãos governamentais, etc.

### 🔁 Nuvem Híbrida
- Combinação de nuvem pública e privada.
- Permite mover cargas de trabalho entre os dois ambientes conforme a necessidade.
- **Equilíbrio entre controle e escalabilidade**.
- Ideal para: empresas que precisam de flexibilidade e segurança.


# 🚀 Passo a Passo: Criar uma Máquina Virtual na Microsoft Azure

## 1. Acesse o Portal da Azure
- Acesse: [https://portal.azure.com](https://portal.azure.com)
- Faça login com sua conta Microsoft.

## 2. Navegue até "Máquinas Virtuais"
- Use o menu lateral ou a barra de pesquisa para encontrar **"Máquinas Virtuais"**.

## 3. Clique em "Criar" > "Máquina virtual"
- Isso abrirá o formulário de criação de uma nova VM.

## 4. Configure as Informações Básicas
- **Assinatura** e **Grupo de Recursos**: selecione ou crie.
- **Nome da VM**
- **Região**: escolha a mais próxima do seu público-alvo.
- **Imagem**: selecione o sistema operacional (ex: Ubuntu, Windows Server).
- **Tamanho**: defina com base na necessidade de CPU/RAM.
- **Usuário administrador**: defina nome e senha ou chave SSH.

## 5. Configurações de Disco
- Escolha o tipo de disco para o SO (por exemplo: SSD padrão).
- Discos adicionais podem ser adicionados depois, se necessário.

## 6. Configurar Rede
- Utilize VNet e Sub-rede padrão ou personalize.
- Mantenha o IP público habilitado se desejar acesso remoto.
- Habilite portas como:
  - **22 (SSH)** para Linux
  - **3389 (RDP)** para Windows

## 7. Revisar + Criar
- Revise todas as configurações inseridas.
- Clique em **"Criar"** para iniciar a criação da VM.

## 8. Acompanhe a Criação
- Aguarde a implantação da máquina virtual (pode levar alguns minutos).

## 9. Conecte-se à VM
- **Linux**: `ssh usuario@ip_da_vm`
- **Windows**: use o Remote Desktop (RDP) com o IP da VM.
