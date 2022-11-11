# Repositório central de Charts Helm

## Principais comandos para criação de um chart

1. Criar um chart com Helm:
   
    ```cmd
    helm create <nome_do_chart>
    ```
2. Validação de syntax:
   
   ```cmd
   helm lint <chart>
   ```
3. Instalação de um chart:

   ```cmd
   helm install <release> <chart>
   ```
   Para criar um namespace caso não exista, durante a instação de um chart:

   ```cmd
   helm install <release> -n <namespace> <chart> --create-namespace
   ```

4. Atualização de um chart:

   ```cmd
   helm upgrade <release> <chart>
   ```

5. Atualização com opção de instalação (se não houver):
   
   ```cmd
   helm upgrade --install <release> <chart>
   ```

6. Simulando a instalação
   
   ```cmd
   helm upgrade --install --dry-run <release> <chart>
   ```
7. Rollback
   
   ```cmd
   helm rollback <RELEASE> [REVISION] [flags]
   ```