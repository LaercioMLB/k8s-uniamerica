# 📘 Guia de Comandos Básicos do `kubectl`

O `kubectl` é a principal ferramenta de linha de comando para interagir com o Kubernetes. Abaixo estão os comandos mais importantes organizados por categoria.

## 🔍 Consultar Recursos

| Comando | Descrição |
|--------|-----------|
| `minikube dashboard` | Para abrir a dashboard do minikube para fazer alterações. |
| `kubectl get pods` | Lista todos os pods no namespace atual |
| `kubectl get services` ou `kubectl get svc` | Lista todos os serviços |
| `kubectl get deployments` | Lista todos os deployments |
| `kubectl get nodes` | Lista todos os nós do cluster |
| `kubectl describe pod <nome-do-pod>` | Mostra detalhes de um pod específico |
| `kubectl get all` | Mostra todos os recursos do namespace atual |
| `kubectl get events` | Mostra eventos recentes do cluster |

## 🚀 Criar e Aplicar Recursos

| Comando | Descrição |
|--------|-----------|
| `kubectl apply -f arquivo.yaml` | Aplica (cria ou atualiza) recursos definidos no arquivo |
| `kubectl create deployment <nome> --image=<imagem>` | Cria um deployment usando uma imagem container |
| `kubectl expose deployment <nome> --type=LoadBalancer --port=80` | Expõe o deployment como um serviço acessível |

## 🛠️ Gerenciar Recursos

| Comando | Descrição |
|--------|-----------|
| `kubectl delete pod <nome-do-pod>` | Deleta um pod específico |
| `kubectl delete deployment <nome>` | Remove um deployment |
| `kubectl delete -f arquivo.yaml` | Deleta recursos definidos no arquivo YAML |

## 📦 Trabalhar com Pods

| Comando | Descrição |
|--------|-----------|
| `kubectl logs <nome-do-pod>` | Exibe os logs de um pod |
| `kubectl exec -it <nome-do-pod> -- bash` | Acessa um pod via terminal (se o bash estiver disponível) |
| `kubectl port-forward pod/<nome-do-pod> 8080:80` | Redireciona uma porta local para uma porta do pod |

## ⚙️ Configurações e Contextos

| Comando | Descrição |
|--------|-----------|
| `kubectl config get-contexts` | Lista todos os contextos configurados |
| `kubectl config use-context <contexto>` | Define qual contexto usar |
| `kubectl config current-context` | Mostra o contexto atual |

## 🧪 Debug e Inspeção

| Comando | Descrição |
|--------|-----------|
| `kubectl explain <recurso>` | Explica a estrutura de um recurso (ex: `kubectl explain pod`) |
| `kubectl get pod <nome> -o yaml` | Mostra a definição YAML de um recurso |
| `kubectl top pod` | Mostra métricas de uso de recursos (requer Metrics Server) |

## 📁 Outras Dicas

- Use `-n <namespace>` para trabalhar em outros namespaces:
  ```bash
  kubectl get pods -n kube-system
