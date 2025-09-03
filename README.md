# Criação de Máquina Virtual no Azure

Este documento descreve o processo de criação da máquina virtual **lab1** no Microsoft Azure.

---

## 1. Seleção da Imagem
- **Sistema Operacional:** Ubuntu Server 24.04 LTS – Gen2  
- **Arquitetura:** x64  

---

## 2. Configuração Básica
- **Nome da VM:** lab1  
- **Grupo de Recursos:** lab1_group  
- **Região:** East US 2  
- **Disponibilidade:** Zona auto-selecionada  
- **Segurança:**  
  - Inicialização segura: **Habilitada**  
  - vTPM: **Habilitado**  

---

## 3. Tamanho da VM
- **Tipo:** Standard B1s  
- **Configuração:** 1 vCPU, 1 GiB de memória  

---

## 4. Autenticação e Acesso
- **Método de Autenticação:** Chave pública SSH  
- **Usuário:** evaldobutzke  
- **Formato da chave:** RSA  
- **Portas abertas:** SSH (22)  

---

## 5. Configuração de Rede
- **IP Público:** Gerado automaticamente  
- **Interface de Rede:** Conectada ao grupo de recursos criado  

---

## 6. Gerenciamento
- **Microsoft Defender para Nuvem:** Básico (gratuito)  
- **Backup:** Desabilitado  
- **Desligamento Automático:** Desativado  

---

## 7. Monitoramento
- **Diagnóstico de Inicialização:** Ativado  
- **Alertas:** Desativados  
- **Monitoramento de Integridade do Aplicativo:** Desativado  

---

## 8. Conexão
A conexão foi realizada via **Azure Cloud Shell** utilizando SSH:

```bash
az ssh vm --resource-group lab1_group --vm-name lab1 --subscription <ID-da-Subscrição>
