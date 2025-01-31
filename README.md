# 📌 dio_api_tempo

Bem-vindo ao repositório **dio_api_tempo**, uma API de previsão do tempo desenvolvida como parte do **Bootcamp Microsoft Certification Challenge #2 AZ-204** da **DIO**. Este projeto faz parte do desafio prático sobre **deploy de APIs na nuvem**, utilizando tecnologias modernas para garantir escalabilidade e eficiência.

---

## 📂 Estrutura do Projeto

A organização do código segue a seguinte estrutura:

```
dio_api_tempo/
│── Controllers/
│   └── WeatherForecastController.cs  # Controlador responsável pelas previsões do tempo
│── Models/
│   └── WeatherForecast.cs  # Modelo de dados para a previsão do tempo
│── Program.cs  # Arquivo principal que configura e inicia a aplicação
│── appsettings.json  # Configuração da aplicação
│── appsettings.Development.json  # Configuração específica para ambiente de desenvolvimento
│── Dockerfile  # Configuração para criação da imagem Docker
│── pipeline.yml  # Definição do pipeline de CI/CD
```

---

## 🚀 Como Executar a Aplicação

Para rodar a API localmente, siga os passos abaixo:

### 🔹 1. Clonar o Repositório

```sh
git clone https://github.com/seu-usuario/dio_api_tempo.git
cd dio_api_tempo
```

### 🔹 2. Restaurar Dependências e Compilar

```sh
dotnet restore
dotnet build
```

### 🔹 3. Executar a Aplicação

```sh
dotnet run --project dio_api_tempo
```

A API estará acessível em:  
📍 **`http://localhost:5063`**

---

## 🌤️ Endpoints Disponíveis

A API expõe os seguintes endpoints:

| Método | Endpoint             | Descrição                                      |
|--------|----------------------|----------------------------------------------|
| `GET`  | `/weatherforecast`   | Retorna uma lista de previsões do tempo    |

---

## 🐳 Executando com Docker

Caso prefira executar a aplicação dentro de um container Docker, siga os passos:

### 🔹 1. Criar a Imagem Docker

```sh
docker build -t dio_api_tempo .
```

### 🔹 2. Rodar o Container

```sh
docker run -p 8080:80 dio_api_tempo
```

A API estará disponível em:  
📍 **`http://localhost:8080`**

---

## ⚙️ Pipeline de CI/CD

O projeto inclui um pipeline de CI/CD configurado no **Azure Pipelines** através do arquivo [`pipeline.yml`](./pipeline.yml).  
Este pipeline executa as seguintes etapas:

1. **Restaurar dependências** (`dotnet restore`)
2. **Compilar o projeto** (`dotnet build`)
3. **Executar testes** (caso existam)
4. **Publicar a imagem Docker** no repositório de contêineres

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Caso tenha sugestões de melhorias ou encontre algum problema, **abra uma issue** ou envie um **pull request**.

---

## 📜 Licença

Este projeto é distribuído sob a licença **MIT**. Consulte o arquivo [`LICENSE`](./LICENSE) para mais detalhes.

🔹 _Projeto desenvolvido no Bootcamp Microsoft Certification Challenge #2 AZ-204 - DIO._