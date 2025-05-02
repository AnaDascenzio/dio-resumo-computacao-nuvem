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


# Modelos de Serviço na Nuvem (Azure)

No contexto da nuvem, o **Azure** oferece diferentes modelos de serviços que atendem às diversas necessidades de infraestruturas e aplicações. Os principais modelos são **SaaS**, **PaaS** e **IaaS**. Abaixo, abordamos cada um desses modelos com foco em máquinas virtuais e como eles se aplicam no **Azure**.

## 1. **IaaS (Infraestrutura como Serviço)**

**IaaS** é o modelo que fornece **infraestrutura de TI sob demanda** através da nuvem. Nele, a responsabilidade pela **infraestrutura física** fica com o provedor de nuvem, enquanto o usuário gerencia os recursos virtuais (máquinas, redes, armazenamento) e as camadas superiores.

### No contexto do **Azure**:
- **Máquinas Virtuais (VMs)**: O Azure oferece máquinas virtuais que podem ser configuradas de acordo com as necessidades do usuário (ex.: Windows, Linux, etc.).
- **Rede Virtual (VNet)**: Configuração e isolamento da rede para as máquinas virtuais.
- **Armazenamento**: Possibilidade de usar **discos persistentes** para armazenar dados e **blobs** para arquivos.
- **Escalabilidade**: VMs podem ser dimensionadas automaticamente para atender a diferentes níveis de demanda.

### Características:
- **Controle total sobre o sistema operacional e aplicativos**.
- **Flexibilidade** para escolher diferentes configurações de hardware e software.
- **Responsabilidade do usuário**: O cliente é responsável pela instalação, configuração e manutenção do sistema operacional, software e segurança.

---

## 2. **PaaS (Plataforma como Serviço)**

**PaaS** oferece **uma plataforma completa** para desenvolvimento, execução e gestão de aplicativos. O provedor de nuvem cuida da infraestrutura e do sistema operacional, enquanto o usuário foca apenas no **desenvolvimento de aplicativos**.

### No contexto do **Azure**:
- **Serviços de Aplicativos**: Oferece uma plataforma gerenciada para criar, implantar e escalar aplicativos web, APIs e backends móveis.
- **Azure Kubernetes Service (AKS)**: Uma plataforma gerenciada para a execução de contêineres, facilitando a orquestração de aplicativos em larga escala.
- **Banco de Dados Gerenciado**: Como o **Azure SQL Database**, que é um banco de dados relacional totalmente gerenciado e escalável.

### Características:
- **Sem gerenciamento de infraestrutura**: O provedor cuida da manutenção da infraestrutura, segurança e atualizações.
- **Escalabilidade automática**: A plataforma pode ajustar a quantidade de recursos automaticamente conforme a demanda.
- **Foco no desenvolvimento de aplicativos**: O usuário não precisa se preocupar com o sistema operacional ou hardware subjacente.

---

## 3. **SaaS (Software como Serviço)**

**SaaS** é um modelo em que o **software** é fornecido e gerenciado pelo provedor de nuvem, acessado através da internet. O cliente apenas utiliza o software sem se preocupar com a infraestrutura, sistema operacional ou qualquer outra configuração.

### No contexto do **Azure**:
- **Microsoft 365**: Suite de aplicativos como Word, Excel e Teams, disponibilizados como SaaS.
- **Power BI**: Ferramenta de análise de dados oferecida como serviço na nuvem.
- **Azure DevOps Services**: Plataforma SaaS para colaboração no desenvolvimento de software, incluindo CI/CD, versionamento de código e gerenciamento de projetos.

### Características:
- **Sem necessidade de instalação ou manutenção**: O software é acessado diretamente da nuvem.
- **Gerenciamento completo pelo provedor**: O provedor cuida de tudo, incluindo atualizações, patches de segurança e manutenção.
- **Acesso de qualquer lugar**: Os aplicativos podem ser acessados a partir de qualquer dispositivo com acesso à internet.

---

## Conclusão

- **IaaS** oferece o maior nível de controle e flexibilidade, permitindo que você configure máquinas virtuais e recursos de infraestrutura conforme necessário.
- **PaaS** abstrai a infraestrutura e o sistema operacional, permitindo um foco maior no desenvolvimento de aplicativos.
- **SaaS** é a solução mais simples, onde você apenas usa o software já pronto e totalmente gerenciado pelo provedor de nuvem.

A escolha entre esses modelos depende do nível de controle que você deseja ter sobre sua infraestrutura e aplicativos. No caso de **máquinas virtuais**, o Azure oferece uma forte base de **IaaS**, enquanto também suporta modelos **PaaS** e **SaaS** para atender às necessidades específicas de cada tipo de aplicação.

